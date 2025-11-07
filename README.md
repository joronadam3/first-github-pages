```markdown
# first-github-pages

This repository contains a simple GitHub Pages site. Below are step-by-step instructions to enable GitHub Pages for this repository and how to access the published site without using a custom domain.

1) Prepare site content
- Create a file named `index.html` at the repository root (or inside a `docs/` folder). Example minimal `index.html` content:

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>first-github-pages</title>
  </head>
  <body>
    <h1>Hello from GitHub Pages</h1>
    <p>This page is served from the <code>first-github-pages</code> repository.</p>
  </body>
</html>
```

- If you use a static site generator (Jekyll, Hugo, etc.), make sure the generated static files are present in the branch/folder you will publish from.

2) Commit and push your site files
- From the command line (example using `main`):

  git add index.html
  git commit -m "Add site index.html for GitHub Pages"
  git push origin main

- Or place the files in `docs/` and push to the branch you will select in Settings.

3) Enable GitHub Pages (web UI)
- Open the repository settings: https://github.com/joronadam3/first-github-pages
- Click the "Settings" tab, then in the left sidebar choose "Pages".
- Under "Build and deployment" → "Source", select the branch (e.g., `main`) and the folder:
  - "/ (root)" if `index.html` is at the repository root
  - "/docs" if it is inside a `docs/` folder
- Click "Save" or "Save and Deploy". GitHub will build and publish the site; this can take a minute.

4) Optional: Publish from a `gh-pages` branch
- Create and push a `gh-pages` branch with your site at the branch root, then select `gh-pages` and "/ (root)" in Settings → Pages.

5) How to access the published page (no custom domain)
- After publishing, your site will be available at:

  https://<github-username>.github.io/<repository-name>/

- For this repository the URL will be:

  https://joronadam3.github.io/first-github-pages/

- If the repo name were `joronadam3.github.io`, the site would be at the root: https://joronadam3.github.io/

6) Tips and troubleshooting
- If you see a 404, wait a minute and refresh; publishing can take a short time.
- Ensure `index.html` exists in the selected branch/folder and that branch is pushed.
- Check the Pages settings page for build errors and enable "Enforce HTTPS" if desired.
- If using Jekyll, note files or folders that begin with `_` may be treated specially.

That's it — follow the steps above and your repository will publish a GitHub Pages site reachable at the URL shown in step 5.
```