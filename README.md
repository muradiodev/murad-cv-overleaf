# Murad Huseynov — CV / Résumé

LaTeX source for my curriculum vitae (résumé), built with the [AltaCV](https://github.com/liantze/AltaCV) class.

## Contents

- **main.tex** — Main document: header, summary, work experience, education, hobbies.
- **page1sidebar.tex** — Sidebar content for page 1 (skills, projects).
- **page2sidebar.tex** — Sidebar content for page 2 (additional projects, languages).
- **altacv.cls** — AltaCV document class (v1.1.3).
- **MYPIC.jpg** — Profile photo (required for `\photo`).

## Requirements

- A LaTeX distribution: [MiKTeX](https://miktex.org/) (Windows) or [TeX Live](https://www.tug.org/texlive/).
- Packages used: `fontawesome`, `geometry`, `lato`, `tikz`, `tcolorbox`, `hyperref`, `biblatex` (and dependencies). MiKTeX/TeX Live will install missing packages on first run if configured to do so.

## Build

From this directory:

```bash
pdflatex -interaction=nonstopmode main.tex
```

Run twice if you change cross-references. Output: **main.pdf**.

### Windows (MiKTeX)

If `pdflatex` is not in your PATH, use the full path:

```powershell
& "$env:LOCALAPPDATA\Programs\MiKTeX\miktex\bin\x64\pdflatex.exe" -interaction=nonstopmode main.tex
```

## Customization

- **Photo:** Replace `MYPIC.jpg` with your image (or add `MYPIC.png`); the template uses `\photo{3cm}{MYPIC}`.
- **Content:** Edit `main.tex` for the main column; `page1sidebar.tex` and `page2sidebar.tex` for the sidebars.
- **Colors:** In `main.tex`, the `\definecolor` and `\colorlet` lines set the theme (e.g. `darkblue`, `Mulberry`).

## Output

The PDF is a two-page CV with a main column (work experience, education, hobbies) and a sidebar (skills, projects, languages).

## License

The CV content is personal. The AltaCV class is distributed under the [LaTeX Project Public License](https://www.latex-project.org/lppl/).
