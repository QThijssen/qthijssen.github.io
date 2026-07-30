# Quinten Thijssen — academic website

Source for Quinten Thijssen's compact personal academic website. The single-page homepage presents a factual overview of his academic profile, selected publications, background, fellowships and recognition, research leadership, and contact links.

The site uses semantic HTML, modern CSS, and a minimal vanilla JavaScript enhancement for the mobile navigation. There is no framework, package manager, external dependency, or build step.

## Local preview

From the repository root:

```text
python -m http.server 8000
```

Then visit `http://localhost:8000/`. A local server is preferred to opening the HTML directly.

## Structure

```text
/
├── index.html
├── 404.html
├── assets/css/main.css
├── assets/js/main.js
├── favicon.svg
├── robots.txt
└── sitemap.xml
```

The homepage contains:

- About
- Selected publications
- Academic background
- Fellowships and recognition
- Contact and academic profiles

Shared presentation lives in `assets/css/main.css`; `assets/js/main.js` only enhances the small-screen menu. The implementation uses plain HTML and CSS with minimal vanilla JavaScript. It is dependency-free and deploys directly as static files.

Selected publications are maintained as semantic `<article>` elements in `index.html`. When updating the list, use exact records from the publisher or another authoritative source. Do not infer or invent titles, author lists, dates, journal details, article status, or URLs.

No public CV PDF is currently included. If one is added, use the stable path `assets/documents/quinten-thijssen-cv.pdf` and update the hero and contact links together.

Navigation and asset references use root-relative URLs because this GitHub user site is published at the domain root. Start the local preview server from this repository's root so those paths resolve correctly.

## Deployment

The repository can be deployed directly through GitHub Pages. The `.nojekyll` file prevents Jekyll processing. The custom domain is `quintenthijssen.com`; DNS and GitHub Pages domain configuration are managed separately.
