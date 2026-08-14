# Cliff Cezar, portfolio site

A personal portfolio built as a topographic map sheet. Contour lines, an elevation profile for the work history, and purple overprint marks for the projects that are not on the printed resume yet.

Plain HTML, CSS, and vanilla JavaScript in one file. No build step, no dependencies, no framework. It just serves.

## Files

```
index.html    the whole site
resume.pdf    linked by the "Open the resume" button
README.md     this file
```

## Run it locally

Open `index.html` in a browser. That is it. If you want a local server:

```bash
python3 -m http.server 5173
# then visit http://localhost:5173
```

If you prefer the CLI:

```bash
npm i -g vercel
vercel
vercel --prod
```

## Custom domain

In the Vercel project, go to **Settings** then **Domains** and add your domain. Vercel gives you the DNS records to paste into your registrar. A `.com` or `.dev` costs about 500 to 900 pesos a year and looks better on applications than a `.vercel.app` link.

## Editing the content

Everything lives in `index.html`, in plain HTML sections that follow the page order:

| Section id | What it holds |
|---|---|
| `hero` markup at the top | Name, tagline, buttons |
| `#legend` | The four line summary of what you do |
| `#traverse` | Work history and education, plus the elevation profile SVG |
| `#survey` | Project cards |
| `#kit` | Skills and languages |
| `#notes` | Interests |
| `#contact` | Email, phone, GitHub, LinkedIn |

To add a project, copy one `<article class="plate">` block and edit it. Add `rev` to the class list and drop in a `<span class="tag">Revision</span>` if you want the purple treatment for something new.

Colors and fonts are CSS variables at the very top of the file, under `:root`.

## A note on the purple

On a real USGS quadrangle, purple overprint means the sheet was revised from newer aerial photos without resurveying the whole map. Here it marks the work that came after the resume was printed. There is a footnote on the page that explains it, so recruiters get the joke instead of wondering.
