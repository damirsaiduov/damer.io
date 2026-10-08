# damer.io — Damir Saiduov

A minimalist, text-first personal home page. One screenful of personality, some stories, and a few underlined links. Inspired by the editorial structure of [olzhas.space](https://olzhas.space/); written for Damir with original text, styling, and graphics.

No frameworks, npm, build steps, external fonts, analytics, or third-party scripts.

## Preview locally

Open `index.html` in your browser. Alternatively, run a local server from this folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish to GitHub Pages

1. Log in to GitHub as `damirsaiduov`.
2. Create a **public** repository named `damer.io` (or `damirsaiduov.github.io`).
3. Upload **all files and folders** from this directory to the repository root, keeping the `assets` directory intact and the `CNAME` file at the root. You can also use Git:

   ```bash
   git init
   git add .
   git commit -m "Launch personal website"
   git branch -M main
   git remote add origin https://github.com/damirsaiduov/damer.io.git
   git push -u origin main
   ```

4. In **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/(root)`, and save.
5. Under **Custom domain**, enter `damer.io` and save. The repository already contains the `CNAME` file with this domain.
6. At your domain registrar, create four **A** records for host `@`:

   | Type | Name | Value |
   | ---- | ---- | ----- |
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |

   Optional: point `www` to `damirsaiduov.github.io` with a CNAME record.
7. After DNS propagation, check **Enforce HTTPS** in GitHub Pages. Make sure the domain is owned by you, and consider verifying it in GitHub's domain settings before connecting DNS.

   GitHub's official guidance: <https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site>

**Important:** This package does not register the domain or publish the site for you. GitHub Pages and DNS changes must be done in your own accounts.

## Edit the words

Open `index.html` and edit the text within `<div class="story">`. Keep links in the form:

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">underlined words</a>
```

- Change colors, font size, and spacing in `assets/style.css`.
- Change time zone or location in `assets/main.js` and the footer text in `index.html`.
- Change the browser favicon in `assets/favicon.svg`.
- Change the social-preview image by replacing `assets/og-card.png`.

## Personal details to double-check before publishing

- Confirm the `over $100k in gross revenue` and `200+ families` figures and the wording about how proceeds were distributed. Revenue, profit, and donations are different accounting measures.
- Confirm `250 registrations` and `10 offline workshops` are accurate.
- Confirm the AI-agent testing sandbox is actually built; the site uses past tense. Once published, add a direct link to its repository in the paragraph.
- Confirm your role on the Astrobot FTC team and your former Tactile Lab RA experience. The FTC hyperlink points to the **program website**, not the Astrobot team's website.
- The Academy has no direct link because none was provided; you can add one when available.

## Files

```
index.html             one-page site, semantic HTML, SEO and OG tags
assets/style.css       responsive typography, hover/focus behavior
assets/main.js         live Kazakhstan time in the footer
assets/favicon.svg     vector browser icon
assets/favicon-32.png  raster fallback icon
assets/og-card.png     social sharing card (1200 × 630)
CNAME                  GitHub Pages custom domain
.nojekyll              prevents Jekyll processing
robots.txt             crawler rules
sitemap.xml            one-page sitemap
README.md              these instructions
```
