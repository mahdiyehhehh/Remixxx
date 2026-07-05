# Remix — Website

A one-page site for Remix (Coffee · Music · Culture), 81-D/1 Main Boulevard, Gulberg III, Lahore.

Plain HTML/CSS/JS — no build step, no framework, no dependencies to install.

## Files

```
index.html      → all page content
styles.css      → design system + layout
script.js       → menu tabs, mobile nav, scroll reveals
images/         → logo + all photos used on the site
```

## Deploy: GitHub → Vercel

1. Create a new **public or private** repo on GitHub (e.g. `remix-website`).
2. Upload every file in this folder to the repo, keeping the `images/` folder intact.
   - Easiest way: on the repo page click **Add file → Upload files**, drag in everything, commit.
3. Go to [vercel.com](https://vercel.com) → **Add New → Project** → import that GitHub repo.
4. Framework preset: choose **Other** (it's a static site, no build command needed).
5. Click **Deploy**. Vercel will give you a live `.vercel.app` URL in under a minute.
6. Optional: in the Vercel project → **Settings → Domains**, add the cafe's own domain if they buy one.

That's it — no environment variables, no backend, nothing else to configure.

## Editing later

- **Prices / menu items**: edit the text inside `#panel-coffee`, `#panel-sandwiches`, `#panel-patisserie` in `index.html`.
- **Bank discounts**: edit the rows inside `#discounts` in `index.html`.
- **Photos**: drop a new image into `images/` and swap the filename in the matching `<img src="...">` tag.
- **Colors**: all colors are CSS variables at the top of `styles.css` under `:root` — change one value there and it updates everywhere.
