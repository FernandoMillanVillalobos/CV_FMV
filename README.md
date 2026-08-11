# Fernando Millán Villalobos — CV (Quarto)

An editable, markdown-based recreation of your CV template. All content lives
in plain text in `index.qmd` — edit it like a normal document, no code
knowledge needed beyond the `:::` div markers that control layout (leave
those alone; edit the text inside them).

## Files

- `index.qmd` — the CV content (this is what you edit)
- `styles.css` — visual styling (colors, spacing, layout). Tweak the
  `:root { --blue: ... }` block at the top to change the accent color.
- `_quarto.yml` — project/render settings

## How to render

1. Install Quarto (free): https://quarto.org/docs/get-started/
2. From this folder, run:

   ```
   quarto render index.qmd
   ```

   This produces `index.html` — open it in any browser, or use
   **Print → Save as PDF** for a print-ready PDF that keeps the layout.

3. To preview live while editing:

   ```
   quarto preview index.qmd
   ```

   This opens a browser tab that auto-refreshes as you save changes.

## Editing tips

- Each job/education entry is wrapped like this — copy/paste a block to add
  a new entry, or delete one to remove it:

  ```
  ::: {.entry}
  ### Job Title
  [Company Name]{.org}

  [🗓 Date range    📍 Location]{.meta}

  - Optional bullet point describing the role
  :::
  ```

- Skill "pills" and language dots work the same way — just copy the pattern
  for a new tag: `[New Skill]{.pill}`
- The accent color, sidebar background, and fonts are all controlled in
  `styles.css` — no need to touch `index.qmd` for a visual restyle.

## Note on PDF output

The `_quarto.yml` includes a basic LaTeX PDF config, but LaTeX doesn't
reproduce the two-column sidebar layout as faithfully as HTML/CSS does.
For best fidelity to the original template, render to HTML and print/export
to PDF from your browser (Chrome/Edge/Firefox handle the CSS grid layout
correctly).
