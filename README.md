# Quinten Thijssen — academic website

Source for Quinten Thijssen's personal academic website. The single-page homepage pairs a welcoming introduction with an editorial selection of research, academic background, and contact links.

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
├── assets/images/
├── assets/js/main.js
├── favicon.svg
├── robots.txt
└── sitemap.xml
```

The homepage contains:

- Personal introduction
- Featured research
- Further selected work
- Academic background
- Contact and academic profiles

Shared presentation lives in `assets/css/main.css`; `assets/js/main.js` only enhances the small-screen menu. The implementation uses plain HTML and CSS with minimal vanilla JavaScript. It is dependency-free and deploys directly as static files.

Selected research features are maintained as semantic `<article>` elements in `index.html`. Each feature contains a real research image, publication metadata, a concise explanation, and verified links. Use exact publication records from the publisher or another authoritative source; do not infer titles, dates, article status, or URLs.

## Image assets

The original assets and optimized WebP derivatives are:

- Portrait: `assets/images/portrait.jpg` and `assets/images/portrait.webp`
- Antagonistic TVAM: `assets/images/research-antagonistic-tvam.png` and `assets/images/research-antagonistic-tvam.webp`
- Fluoropolymer recycling: `assets/images/research-fluoropolymer.png` and `assets/images/research-fluoropolymer.webp`
- Polyester review: `assets/images/research-polyester-review.png` and `assets/images/research-polyester-review.webp`

The `<picture>` elements use WebP first and the original JPG or transparent PNG as a fallback. To replace an image without changing HTML, replace both files in a pair while preserving their filenames and aspect ratio. Recommended minimum source widths are 1000 px for the portrait and 1600 px for each research figure; retain enough resolution for scientific labels to remain legible.

The portrait uses `object-fit: cover` with `object-position: 50% 42%`. Review that position whenever the portrait is replaced so the face retains natural headroom. Research figures use `object-fit: contain` and centered positioning because their labels and diagrams must not be cropped.

Verified contact destinations currently include LinkedIn, Google Scholar (`https://scholar.google.com/citations?user=sNh11noAAAAJ&hl=en`), ORCID, GitHub, and email.

Navigation and asset references use root-relative URLs because this GitHub user site is published at the domain root. Start the local preview server from this repository's root so those paths resolve correctly.

## Deployment

The repository can be deployed directly through GitHub Pages. The `.nojekyll` file prevents Jekyll processing. The custom domain is `quintenthijssen.com`; DNS and GitHub Pages domain configuration are managed separately.
