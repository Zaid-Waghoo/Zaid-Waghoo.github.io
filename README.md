# zaid-waghoo.github.io

Personal site of Zaid Waghoo. Plain HTML and CSS, no framework, no build step.
GitHub Pages serves the files in this repo as they are.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | Home page: bio, links, projects, papers |
| `projects/<name>/index.html` | One page per project, served at `/projects/<name>/` |
| `css/style.css` | The only stylesheet. Fonts and colors are at the top, light and dark |
| `fonts/` | Hanken Grotesk (text) and JetBrains Mono (labels), self-hosted |
| `papers/` | PDFs of published papers |
| `images/` | Images, one folder per project |
| `favicon.svg` | Browser tab icon |
| `404.html` | Shown for missing pages |
| `robots.txt`, `sitemap.xml` | Help search engines find every page |
| `.nojekyll` | Tells GitHub Pages to skip Jekyll and serve files as they are |

## Editing

- Unfinished content is marked `PLACEHOLDER`. Find it all with
  `grep -rn PLACEHOLDER .`
- To add an image: put it in `images/<project>/`, then replace a
  `<figure class="placeholder">` with
  `<figure><img src="/images/<project>/file.jpg" alt="what it shows" width="1200" height="800" loading="lazy"><figcaption>Caption</figcaption></figure>`.
  Set `width` and `height` to the real pixel size so the page does not jump while loading.
- To add a project: copy a folder in `projects/`, update its `<title>`,
  description, canonical URL, and `og:` tags, then add it to `index.html`
  and `sitemap.xml`.

## Preview locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.
