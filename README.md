# Techpointe advisory site

The main site for **techpointe.ai**: one page, no build step, no JavaScript.

| File | What it is |
|---|---|
| `index.html` | The whole page. All text and styling live here. |
| `icon.svg` | Browser-tab icon (the hammer). |
| `og.png` | The image shown when the link is shared. |
| `CNAME` | Tells GitHub Pages the site's address. One line: `techpointe.ai`. |

## Put it live (about 15 minutes, then DNS wait)

GitHub Pages allows one address per repository, so this site needs its own
repository, separate from `machine-speed`.

1. On GitHub: **+ → New repository**. Name it `techpointe-site`, **Public**, no
   boxes ticked. Create it.
2. Click **uploading an existing file**, drag in the four files above (not this
   README if you'd rather keep it out), and **Commit changes**.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
   Branch `main`, folder `/ (root)`. Save.
4. **Settings → Pages → Custom domain**: `techpointe.ai`. Save.
5. At your domain registrar, in the DNS settings for `techpointe.ai`, add:
   - Four **A** records for the bare domain (host `@`):
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME** record: host `www` → `velvethamm3r.github.io`
6. Back in **Settings → Pages**, once the domain check passes, tick
   **Enforce HTTPS**.

## Before you launch

- **Email.** The page links to `dbahrami@techpointe.ai` in three places. Set that
  mailbox up first, or search `index.html` for `techpointe.ai?subject` and
  `mailto:` and change them back to the `.org` address.
- **Machine Speed and newsletter links** point to
  `machinespeed.techpointe.ai` and `newsletter.techpointe.ai`. Move the board
  and the Substack custom domain to those addresses before this page goes
  live, or the links will not open.
- **The "New on Machine Speed" list** in the About section reads the board's
  `new.xml` feed in the visitor's browser and shows the three newest items. If
  the board cannot be reached, a plain sentence shows in its place. The board's
  address is one line near the bottom of `index.html`: `var BOARD = "…"`.

## Editing

Open `index.html` on GitHub, click the pencil, change the text, commit. The live
site updates in about a minute. Prices appear in two places: the "Two-week
sprint" card and the "How engagements work" table.
