# CLAUDE.md — Personal Academic Website

## Project overview

This is Niklas Hänze's personal academic website, built with **Quarto** and deployed via GitHub Pages from the `docs/` output directory. The site presents research, publications, teaching, CV, and conferences.

**Key files:**
- `_quarto.yml` — site configuration (navigation, theme, output settings)
- `html/styles.scss` — custom SCSS on top of Bootstrap "pulse" theme
- `index.qmd` — homepage (jolla template with profile picture)
- `projects/index.qmd` — research interests
- `publications/index.qmd` — publications and working papers
- `teaching/index.qmd` — teaching activities
- `cv/index.qmd` — CV with embedded PDF
- `conferences/index.qmd` — conference participation
- `docs/` — generated output (do not edit manually)

---

## Build system

This is a **Quarto website** project. The standard build command is:

```bash
quarto render
```

To preview with live reload:

```bash
quarto preview
```

Preview runs on port `22222`. Code execution is frozen (`execute: freeze: true`), so R chunks are not re-run unless explicitly unfrozen.

---

## Dos

- Edit `.qmd` files to update content.
- Keep changes consistent with existing formatting in each file.
- Update `_quarto.yml` for structural/navigation changes.
- Modify `html/styles.scss` for styling changes; keep the SCSS variables organized in the defaults section.
- Ask before adding new pages or restructuring navigation.
- **Always run `quarto render` after edits to verify the build is clean.** This does not interfere with Niklas rendering in RStudio — both write to `docs/`, just don't render simultaneously.
- Flag style inconsistencies or visual issues proactively, even if not asked. The goal is a clean and professional site.

## Don'ts

- **Never edit files in `docs/` directly** — this is generated output and will be overwritten on next render.
- **Never delete or overwrite `.qmd` source files without explicit instruction.** For major rewrites, save the original to a `legacy/` folder first.
- Do not modify `cOdZoqILcUKZCU5NvPLEiGmxXz-GKjfcbFnVnUY7KNA.html` — this is a site verification file.
- Do not change the output directory from `docs/` (required for GitHub Pages).
- Do not add R code chunks that execute (freeze is on; unexpected execution may break the build).
- Do not invent or fabricate publication titles, authors, years, or research content — all academic content must come directly from Niklas.
- Do not push to GitHub — Niklas handles git/deployment manually.

---

## Content rules

- **Academic content (publications, research, CV entries) must be provided by Niklas explicitly.** Never generate or infer bibliographic details.
- For publications: Niklas will provide the details; help format them consistently with the existing entries in `publications/index.qmd`.
- For CV: Niklas drops an updated PDF into the project folder; the page embeds it directly — no manual transcription needed.
- Maintain the existing tone: professional academic, concise, third-person neutral where applicable.
- Keep HTML/Markdown formatting consistent with what's already in each page.
- Conference entries follow the pattern in `conferences/index.qmd` — match that format exactly when adding new ones.

---

## Style

- Primary color: teal (`#068194`)
- Link hover: red (`#CF4446`)
- Theme: Bootstrap "pulse" + custom SCSS
- Font size: 1.1em base
- External links open in new window (configured globally)
- No TOC on any page (`toc: false`)
- Proactively flag any visual inconsistencies noticed during other work — goal is a clean, professional appearance throughout.
