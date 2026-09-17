# elroddd_website

Personal site built with [Eleventy](https://www.11ty.dev/). Pages are plain markdown files in `src/`.

## Adding/editing a page

1. Create a new `.md` file in `src/` (e.g. `src/projects.md`).
2. Add front matter at the top:
   ```
   ---
   title: Projects
   layout: base.njk
   ---
   ```
3. Write the page content below in markdown.
4. Add a link to it in the nav: [src/_includes/base.njk](src/_includes/base.njk).

Images/files go in `src/assets/`, reference them as `/assets/filename.png`.

## Local development

```
npm install
npm run serve
```

Opens a local dev server with live reload at `http://localhost:8080`.

## Build

```
npm run build
```

Outputs static files to `_site/`.

## Deploy

Pushing to `main` triggers [.github/workflows/deploy.yml](.github/workflows/deploy.yml), which builds the site and publishes it to GitHub Pages.

**One-time setup:** in the GitHub repo, go to Settings → Pages → Build and deployment → Source, and select **GitHub Actions**.
