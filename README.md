# Phone Store — Price List Site

A single-page site that shows your phone prices, grouped by category and brand.
All the prices live in one plain-text file (`prices.txt`) — edit that file and
the page updates automatically. No coding needed after setup.

## What's in this folder

- `index.html` — the whole website (one page, works on mobile and desktop).
- `prices.txt` — your price list. Edit this whenever prices change.
- `README.md` — this file.

## 1. Put it on GitHub (one-time setup)

1. Go to https://github.com and log in.
2. Click the **+** in the top-right corner → **New repository**.
3. Name it something like `phone-store` (any name is fine). Leave it **Public**
   (GitHub Pages needs a public repo unless you're on a paid plan). Don't add
   a README/gitignore/license — leave those unchecked, since you're uploading
   your own files.
4. Click **Create repository**.
5. On the new repo's page, click **uploading an existing file** (or **Add
   file → Upload files**).
6. Drag in `index.html` and `prices.txt` from this folder (and `README.md` if
   you want it there too).
7. Scroll down and click **Commit changes**.

## 2. Turn on GitHub Pages

1. In your repo, click **Settings** (top menu).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment" → **Source**, choose **Deploy from a branch**.
4. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
5. Wait about 1 minute, then refresh the page. GitHub will show you the live
   URL — it looks like:

   `https://YOUR-USERNAME.github.io/phone-store/`

   That's your single-page phone store, live on the internet.

## 3. Updating prices later

You never need to touch `index.html` again. To change prices:

1. Open your repo on github.com.
2. Click on `prices.txt`.
3. Click the pencil icon (✏️ **Edit this file**) in the top-right of the file view.
4. Edit the lines, following the format explained at the top of the file:

   ```
   Category | Brand | Model | Price
   ```

   Example:

   ```
   Flagship | Apple | iPhone 16 Pro | 999
   ```

5. Scroll down, click **Commit changes**.
6. Refresh your site — the new prices appear within a few seconds (GitHub
   Pages updates automatically after every commit; sometimes it takes up to
   a minute).

You can also add whole new categories just by typing a new category name on
a new line — the page will create a new section for it automatically.

## Notes

- The page reads `prices.txt` with `fetch()`, which only works when served
  over http(s) — that's exactly what GitHub Pages does. If you double-click
  `index.html` on your own computer it won't load prices (browsers block
  that for local files); that's expected and fixes itself once it's on
  GitHub Pages.
- Currency symbol defaults to `$`. To change it, open `index.html`, search
  for `const CURRENCY = "$"` near the top of the `<script>` section, and
  change the symbol.
- Everything is a single HTML file with no build step and no dependencies —
  easy to hand to anyone else to maintain.
