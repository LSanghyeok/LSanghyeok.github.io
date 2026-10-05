# Sanghyeok Lee - Personal Homepage

Static academic homepage for `sanghyeoklee.com`, hosted with GitHub Pages.

## Structure

```text
index.html          About, research interests, and news
cv.html             Web CV and academic service
publications.html   Working papers and publications
css/styles.css      Shared responsive styles
assets/icons/       Interface icons and favicon
assets/images/      Portrait and news images
assets/documents/   Downloadable CV
docs/               Source inventory and capture notes
CNAME               GitHub Pages custom domain
```

The site intentionally uses plain HTML and CSS. There is no build step. The homepage loads POWR's hosted script for the visitor counter and a Flag Counter image for country statistics; all other site behavior is dependency-free. The downloadable CV is stored locally so it remains available with the static site.

## Local Preview

The pages can be opened directly, or served locally when testing links and browser behavior:

```powershell
python -m http.server 4173
```

Then open `http://127.0.0.1:4173/index.html`.

The POWR visitor counter may not render when `index.html` is opened directly with a `file://` URL. Test it through the local server or the deployed site. Keep the app ID `2cebd51a_1745403633` so the embed continues to address the existing counter; if the widget stops loading, copy the current HTML embed code from that app in the POWR dashboard.

## Content Updates

### Publications

1. Add new items to `publications.html` in reverse chronological order.
2. Use `C`, `W`, `J`, `P`, or `U` for the publication type (conference, workshop, journal, preprint, or under review).
3. Link each title to the official paper or arXiv page.
4. Show a compact `Code` action beneath the paper only when a public repository is available and verified.
5. List accepted workshop papers above preprints in the downloadable CV.
6. Update related acceptance news in `index.html` when appropriate.

The homepage's selected publications section is reserved for papers where Sanghyeok Lee is the first author or is explicitly marked as an equal-contribution co-first author. Keep the same reverse chronological order when updating it, but do not display author-role labels in the list.

### CV

Keep entries in reverse chronological order. Reviewer venues are separated into conferences and journals, and venue abbreviations should remain consistent. Replace `assets/documents/Sanghyeok_Lee_CV_2026.pdf` when publishing a revised 2026 CV, and rename the file plus update `cv.html` when the year changes.

### Shared Styles

All pages load `css/styles.css` with the same cache version. Increment the version in every HTML file whenever shared CSS changes.

## Pre-Publish Checklist

- Open About, CV, and Publications at desktop and mobile widths.
- Check that navigation, CV download, publication, profile, and email links work.
- Confirm that images have useful alternative text and no page scrolls horizontally.
- Run `git diff --check` before committing.
- After deployment, verify both `https://sanghyeoklee.com` and `https://www.sanghyeoklee.com`.

## Deployment

GitHub Pages publishes the `main` branch from the repository root. Pushing a commit to `main` triggers deployment. DNS is managed separately through Gabia; do not remove `CNAME` unless the custom domain is intentionally being disconnected.
