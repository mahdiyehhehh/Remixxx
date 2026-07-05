# Remix — Website

A one-page site for Remix (Coffee · Music · Culture), 81-D/1 Main Boulevard, Gulberg Block D1 III, Lahore, 54660, Pakistan.

Plain HTML/CSS/JS — no build step, no framework, no dependencies to install.

## Files

Every file sits flat in the same folder — no subfolders. This is deliberate: uploading from a phone through GitHub's mobile interface can silently drop nested folders, which is what caused the photos not to load last time. Keeping everything at the same level means there's nothing to get lost in transit.

```
index.html
styles.css
script.js
README.md
logo.png
hero-bg-blurred.jpg
drinks-lineup.jpg
sandwich-coffee.jpg
sandwich-spread.jpg
sandwich-tray.jpg
caprese.jpg
interior-seating.jpg
vinyl-comics.jpg
vinyl-wall.jpg
hustle-art.jpg
storefront.jpg
phone.jpg
grabgo.jpg
stairs-sign.jpg
dj.jpg
```

## Deploy: GitHub → Vercel

1. Create a new repo on GitHub (e.g. `remix-website`) — or if you already made one, delete everything currently in it first so old broken paths don't linger.
2. **Upload every file in this folder in one go**, all at the same level (don't create or open any subfolder while uploading). On GitHub's mobile site/app: **Add file → Upload files** → select all of these files at once → commit.
3. Go to [vercel.com](https://vercel.com) → your existing project should auto-redeploy once you push to the repo it's connected to. If it's a fresh repo, **Add New → Project** → import it → Framework preset **Other** → **Deploy**.
4. Give it a minute, then reload your `.vercel.app` URL.

### If images still don't show

- Open the repo on github.com and confirm you see files like `logo.png` and `drinks-lineup.jpg` sitting in the **same list** as `index.html` — not inside any folder icon.
- File names are case-sensitive on Vercel. `Logo.PNG` will not match `logo.png` in the code.
- If GitHub stripped an extension during upload (e.g. `index` instead of `index.html`), rename the file on github.com to add it back.

## What changed in this update

- **Images**: moved out of an `images/` subfolder to sit flat next to `index.html`, since that subfolder wasn't surviving the mobile upload.
- **Menu prices**: every price now carries its own small `8oz` / `12oz` label directly underneath it, so the size is always obvious next to the number — no more separate header row that scrolls out of view.
- **Directions**: the "Get directions" and footer "Directions" links now point to a Google Maps search for the full address (81-D/1 Main Boulevard, Gulberg Block D1 III, Lahore, 54660, Pakistan) instead of the old Instagram short link.

## Editing later

- **Prices / menu items**: edit the text inside `#panel-coffee`, `#panel-sandwiches`, `#panel-patisserie` in `index.html`.
- **Bank discounts**: edit the rows inside `#discounts` in `index.html`.
- **Photos**: drop a new image into this same folder and swap the filename in the matching `<img src="...">` tag (just the filename, no folder prefix).
- **Colors**: all colors are CSS variables at the top of `styles.css` under `:root`.
