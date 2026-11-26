# Tianze Tang — My GitHub website

Course: **Introduction to Digital Services — DIG001IT1AE-3033 (Chengdu)**
Section: **Self study + Test site** · graded task: **My GitHub site** (due 28 November 2026, 05:59)
Brief: build a website yourself, publish it on GitHub Pages, submit **two links** — the code
repository and the first published page. HTML and CSS only; no JavaScript or complicated code.

> This repository is the submission: **7 hand-written pages, 1 stylesheet, 0 lines of JavaScript,
> 0 frameworks, 6 SVG figures (22 kB), 128 kB in total.**

---

## Pages

| File | Content |
|---|---|
| `index.html` | Home: introduction, site map, the coverage table for every study step, learning log |
| `about.html` | About me: facts, honest skills check, how the site was built, technical summary |
| `html.html` | **Notes (HTML)**: what HTML is, the document skeleton, the head, headings and paragraphs, elements/attributes, lists, links and navigation, images, semantic elements |
| `css.html` | **Notes (CSS)**: what CSS is, three ways to include it, selectors, cascade and inheritance, box model, colour, typography, Flex and Grid, responsive design, transitions, custom properties |
| `practice.html` | **Test site**: hover cards, CSS-only tabs (`:target`), progress bars, CSS shapes, gallery, table, accordion, three kinds of link |
| `validation.html` | **Step 8 and 9**: W3C validation results, link check, accessibility checks, responsive and size tests, how the code is commented |
| `contact.html` | Contact: e-mail, GitHub, the two submission links, FAQ |

Assets: `css/style.css` (one stylesheet, 15 numbered sections), `images/*.svg` (6 diagrams drawn for
this project), `.nojekyll` (needed by GitHub Pages).

## How the course requirements are met

| Requirement | Where |
|---|---|
| Scope: 3 pages (home, introduction, contact + one more) | 7 pages, all reachable from the navigation |
| Semantic structure (header, footer, article, headings) | `header` / `nav` / `main` / `section` / `figure` / `footer` on every page |
| Table, list, buttons | 4 tables with `caption`, 3 kinds of list, real `<button>` elements |
| Images on every page | a `<figure>` on each of the 7 pages, all SVG |
| Functional navigation | same bar on every page, current page marked with `aria-current` |
| Optimised media (≈300–400 kB) | 22 kB of images, 128 kB for the whole site |
| Responsive design with media query | breakpoints at 940 px and 700 px |
| Accessible implementation | skip link, focus rings, `alt`, `aria-current`, reduced motion, colour scheme |
| Style in a separate stylesheet | `css/style.css`, linked everywhere, no `<style>` blocks |
| Validation, testing, accessibility | `validation.html` — 0 errors in the W3C validator on all 7 pages |
| Commented code | region markers in HTML, 15 numbered sections in CSS |

## Run it locally

Double-click `index.html` — it works from disk. To be closer to the real thing:

```bash
python -m http.server 8000
# then open http://127.0.0.1:8000
```

## Publish on GitHub Pages

### Option A — the website, no command line

1. Create a new **public** repository, for example `my-site`.
2. On the empty repository page choose **uploading an existing file** and drag in the whole folder
   contents, including `css/`, `images/` and `.nojekyll`.
3. Commit.
4. **Settings → Pages → Source: Deploy from a branch → Branch: `main`, folder `/ (root)` → Save.**
5. After about a minute: `https://<username>.github.io/my-site/`.

### Option B — with git

```bash
git init
git add .
git commit -m "My GitHub website: HTML + CSS"
git branch -M main
git remote add origin https://github.com/<username>/my-site.git
git push -u origin main
```

Then enable Pages as in step 4 above.

## Replace these placeholders before submitting

| File | Placeholder | Replace with |
|---|---|---|
| `contact.html` | `you@example.com` (two places) | your real e-mail address |
| `contact.html` | `your-username` (three places) | your real GitHub username |

## The two links for Moodle

```
repository: https://github.com/<username>/my-site
page:       https://<username>.github.io/my-site/
```

## Implementation notes

- **No JavaScript.** Navigation is plain links, tabs use CSS `:target`, collapsing uses `<details>`,
  animation uses `@keyframes`.
- **No framework, template or site generator.**
- **Images** are SVG: small, sharp at any size, no licensing issues.
- **Accessibility**: skip link, `aria-current`, descriptive `alt`, visible keyboard focus, light and
  dark mode follow `prefers-color-scheme`.
- **Responsive**: 940 px and 700 px; the navigation wraps and grids collapse to one column.
- **Validated**: every page returns 0 errors and 0 warnings in the W3C Nu HTML checker.
