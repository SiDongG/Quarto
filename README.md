# Quarto
Quarto markdown scss and css files. 
For presentation purposes

# Reveal.js / Quarto — Keyboard & Export Reference

Quick reference for presenting and exporting.

## Export to PDF

Reveal.js exports through a special print mode + your browser's print dialog:

1. Add `?print-pdf` to the deck URL, e.g.
   `http://localhost:4903/ProjectUpdateFeb15.html?print-pdf`
2. Open the print dialog — **Cmd+P** (Mac) / **Ctrl+P** (Windows)
3. Set:
   - **Destination:** Save as PDF
   - **Layout:** Landscape
   - **Margins:** None
   - **Background graphics:** ON  ← required, or the cream background and
     callout fills disappear
4. Save

A plain Cmd+P *without* `?print-pdf` only prints the current slide, not the deck.

Note: chalkboard drawings and incremental fragments don't export to PDF (they're
runtime-interactive). This deck uses `incremental: false`, so that's not an issue.
If you ever enable increments, add `pdfSeparateFragments: false` to keep one PDF
page per slide.

## Navigation

| Key | Action |
|---|---|
| `→` `↓` `Space` | Next slide |
| `←` `↑` | Previous slide |
| `Home` / `End` | First / last slide |
| `O` or `Esc` | Slide overview (grid of all slides) |
| `F` | Fullscreen |
| `Alt+click` | Zoom into a spot (hold Alt, click) |

## Presenting

| Key | Action |
|---|---|
| `S` | Speaker view (notes, timer, next-slide preview) |
| `B` or `.` | Pause / black out screen (see conflict note below) |
| `?` | Show the built-in help overlay with the full keymap |

## Highlighting & drawing (installed plugins)

| Key | Action |
|---|---|
| `Q` | Laser pointer — toggle on/off (pointer plugin) |
| `B` | Chalkboard — draw freehand over the current slide |
| `C` | Blank canvas to draw on |
| `Del` | Clear the current drawing |
| `D` | Download chalkboard drawings to a file |

**`B` conflict:** with the chalkboard plugin loaded, `B` opens the chalkboard.
Use `.` if you want to black out the screen instead.

## Menu / jumping around

- The hamburger icon (bottom-left, from `menu: true`) opens a clickable slide list —
  handy when someone asks about an earlier result mid-talk.
- `Esc` also opens the overview grid; click any slide to jump to it.

## Downloading / sharing the deck

- **Share the rendered deck:** the `.html` file Quarto produces next to your `.qmd`
  (e.g. `ProjectUpdateFeb15.html`).
- **Make it a single portable file:** add `embed-resources: true` under `revealjs:`
  in the YAML, re-render, and send that one HTML file (works without the supporting
  `_files/` folder).
- **As PDF:** use the `?print-pdf` process above.
