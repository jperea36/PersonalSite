# Personal site starter

Plain HTML/CSS, no build step, no frameworks. Structured as three sections
(reviews, writing, projects) plus a homepage.

## Structure

```
/
├── index.html              # homepage, links to all three sections
├── reviews/
│   ├── index.html          # review list
│   └── example-book-review.html   # copy this for each new review
├── writing/
│   ├── index.html          # post list
│   └── example-post.html          # copy this for each new post
├── projects/
│   ├── index.html          # project list
│   └── example-project.html       # copy this for each new project
└── assets/
    ├── css/style.css       # single shared stylesheet
    └── img/                # put images here
```

## Adding content

1. Copy the relevant `example-*.html` file, rename it (e.g.
   `dune-review.html`), and edit the content.
2. Add a matching `<li>` entry to that section's `index.html`, linking to
   your new file.

No templating — each page is a plain HTML file that pulls in
`assets/css/style.css`. That's the tradeoff for zero build tooling; it's fine
at this scale (tens of pages). If it grows past that, look at a static site
generator like Eleventy or Hugo, which can auto-generate the listing pages
from markdown files.

## Publishing with GitHub Pages (free)

1. Create a new GitHub repo (public repos get free Pages hosting; private
   repos need a paid plan for Pages).
2. Push this folder's contents to the repo's `main` branch.
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to "Deploy from a branch,"
   branch `main`, folder `/ (root)`.
5. Save. Your site will be live in a minute or two at:
   `https://<your-username>.github.io/<repo-name>/`

If you want it at `https://<your-username>.github.io` directly (no repo name
in the path), name the repo exactly `<your-username>.github.io`.

## Custom domain (optional, not required)

If you later want your own domain instead of the `github.io` URL:
1. Buy a domain from any registrar (~$10–15/year).
2. Add a `CNAME` file at the repo root containing just your domain
   (e.g. `yourdomain.com`).
3. Point the registrar's DNS at GitHub's Pages IPs (GitHub's docs cover the
   exact records: Settings → Pages → "Custom domain" gives you these).

This is optional — the free `github.io` URL works fine to start.
