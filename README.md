# earth-int.com

Static one-page site for the Earth Intelligence Lab. No build step: everything served lives in `public/`.

## View locally

```
python -m http.server 8000 -d public
```

Open http://localhost:8000. (`npx serve public` works too.)

## Hosting on Cloudflare Pages (free plan)

1. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick `janepk12/earth-int.com`.
2. Build settings: Framework preset **None**, Build command **empty**, Build output directory **`public`**.
3. Deploy. Every push to `main` redeploys automatically.
4. Custom domain: Pages project → Custom domains → add `earth-int.com` (the domain's DNS must be on Cloudflare, or add the CNAME they show you).

Free-plan limits that matter here: 20,000 files and 25 MiB per file, 500 builds per month. This site is three files.

## Editing

- Team members: edit the tiles in `public/index.html` (name in `<h3>`, role in `<p>`). For a photo, add a square JPEG to `public/` and change that tile's `src="/placeholder.svg"` to `src="/name.jpg"` and the `alt` to the person's name.
- "What we do" text and interest tags: the `about` section in `public/index.html`.
