# jiangyun-fun.github.io

> Personal homepage of Yun Jiang — bioinformatics engineer at Atantares Corp.

**Live site:** [jiangyun-fun.github.io](https://jiangyun-fun.github.io)

## Overview

A single-page terminal simulation that doubles as a personal homepage. Content is presented as typed-out shell commands and their output — boot sequence, project listings, a neofetch-style skills panel, and contact info.

## Tech Stack

| Layer     | Choice                                  |
| --------- | --------------------------------------- |
| Markup    | Semantic HTML5                          |
| Styling   | Inline CSS (custom properties, keyframes) |
| Scripting | Vanilla JS (dynamic date only)          |
| Font      | JetBrains Mono via Google Fonts         |
| Hosting   | GitHub Pages                            |
| Build     | None — single `index.html`              |

## Local Development

```bash
# Clone
git clone https://github.com/jiangyun-fun/jiangyun-fun.github.io.git
cd jiangyun-fun.github.io

# Serve (any static file server works)
python -m http.server 8000
# Then open http://localhost:8000
```

## Structure

```
jiangyun-fun.github.io/
├── index.html        # Complete page — HTML + CSS + JS inline
├── .prettierignore   # Prevents formatter from breaking white-space:pre content
└── README.md
```

## Design Notes

- **Boot sequence** — lines reveal sequentially via CSS `animation-delay`; reduced-motion users see everything instantly.
- **Monospace alignment** — project descriptions, neofetch keys, and contact labels use fixed-column padding rendered with `white-space: pre`. Prettier is excluded from `index.html` to preserve this alignment.
- **Accessibility** — semantic headings (`<h1>`, `<h2>`) are visually hidden with `.sr-only` but available to screen readers. ASCII art uses `role="presentation"` and `aria-hidden="true"`.

## License

© Yun Jiang. All rights reserved.
