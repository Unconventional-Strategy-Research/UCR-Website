# UCR Website
### Unconventional Strategy Research — Public Site

The public-facing website for Unconventional Strategy Research, hosted on GitHub Pages. Three pages: landing, approach, and lab.

Live: [unconventional-strategy-research.github.io/UCR-Website](https://unconventional-strategy-research.github.io/UCR-Website/)

---

## Pages

| Page | File | What it is |
|------|------|------------|
| Home | `index.html` | Landing page — what USR is and does |
| Approach | `approach.html` | The research methodology and philosophy |
| Lab | `lab.html` | All tools built from the research, with live links and pipeline |

---

## Structure

```
UCR-Website/
├── index.html
├── approach.html
├── lab.html
├── style.css
├── logo_with_star__1_.png
└── resources/
    └── CaseIQ_Lab_Note_001.docx
```

---

## Running Locally

No build step required.

```bash
git clone https://github.com/unconventional-strategy-research/UCR-Website.git
cd UCR-Website
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

For accurate local link resolution, a simple local server is recommended:

```bash
# Python
python3 -m http.server 8000
# then open http://localhost:8000

# Node
npx serve .
# then open http://localhost:3000
```

---

## Deploying

The site deploys automatically via GitHub Pages on every push to `main`.

To configure: **Settings → Pages → Source → Deploy from branch → main → / (root)**

---

## Adding a New Tool to the Lab

1. Add a tool card in the `<!-- LIVE -->` section of `lab.html`, following the existing `.tool-card` pattern
2. Update the stat counters at the top of the tools section
3. If a lab note exists, add it to `resources/` and link it in the tool card using the `.tool-paper-link` component
4. Open a PR with the title: `feat: add [Tool Name] to lab`

---

## Contributing

- Keep `style.css` shared across all pages — page-specific styles go in `<style>` blocks within each file
- All fonts are loaded via Google Fonts in `style.css` — do not add additional font imports per page
- Logo file must remain at root: `logo_with_star__1_.png`
- Lab notes and downloadable resources go in `resources/`

---

## About

USR is a research lab focused on building sharper tools for strategic thinking and decision-making. Every tool in the Lab is a direct output of framework synthesis work — built because building was the best way to understand.

[LinkedIn](https://www.linkedin.com/company/unconventional-strategy-research/) · [GitHub](https://github.com/unconventional-strategy-research)
