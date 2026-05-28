# LaTeX Project Template

This repository is a generic LaTeX template for a final year project, dissertation, or similar report.

## Project Structure

```
├── main.tex                 # Main document file
├── template-metadata.tex    # Editable title-page and front-matter metadata
├── preamble.tex             # Document configuration and packages
├── references.bib           # Bibliography database
├── chapters/                # Chapter files
├── sections/                # Front matter sections
└── images/                  # Image directory
   └── (place images here)
```

## Getting Started

1. **Set the project metadata**
   - Edit `template-metadata.tex` directly.
   - The editable fields are `\thesistitle`, `\thesisauthor`, `\studentid`, `\projectyear`, `\departmentname`, `\facultyname`, `\institutionname`, `\degreeaward`, `\supervisorname`, `\hodname`, `\abstracttext`, `\dedicationtext`, and `\acknowledgmentstext`.

2. **Add content to chapters**
   - Replace the placeholder text in the chapter files with your own material.
   - Start with `01-introduction.tex` and work through sequentially.

3. **Add references**
   - Add your bibliography entries to `references.bib`.
   - Use the format: `\citep{citation_key}` or `\citet{citation_key}`.

4. **Add images**
   - Place images in the `images/` folder.
   - Reference them using `\includegraphics[width=...]{filename}`.

5. **Compile the document**
   - Use `pdflatex main.tex` or your LaTeX editor's compile function.
   - Run twice to update references: `pdflatex main.tex && pdflatex main.tex`.

## Compiling Your Project

### Using command line:
```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### Using Overleaf:
- Upload all files to Overleaf
- Set main.tex as the main document

### Using TeX Live or MiKTeX:
- Use TeXStudio, TeXShop, or your preferred LaTeX editor
- Open main.tex and click "Compile" or "Build"

## Features

- **Professional formatting** with proper margins and spacing
- **Automatic table of contents** generation
- **Bibliography management** using BibTeX
- **Numbered chapters and sections** with automatic referencing
- **Front matter** (title page, abstract, acknowledgments)
- **Back matter** (references, appendices)
- **Code syntax highlighting** for including code listings
- **Figure and table captions** with automatic numbering

## Customization

### Change styling
- Modify the document class in `main.tex`.
- Adjust margins in `preamble.tex` using `\usepackage[margin=2.5cm]{geometry}` if needed.
- Change line spacing in `preamble.tex` if your department uses a different default.

### Add more chapters
- Create new `.tex` files in the `chapters/` directory.
- Add `\include{chapters/filename}` to `chapters/main.tex` in the appropriate location.

### Modify bibliography style
- Change `\bibliographystyle{apalike}` to another style (e.g., `plain`, `ieeetr`).
- Ensure matching `references.bib` entries.

## Tips

- Use `\label{fig:name}` and `\ref{fig:name}` for figure references.
- Use `\label{tab:name}` and `\ref{tab:name}` for table references.
- Use `\label{sec:name}` and `\ref{sec:name}` for section references.
- Use `\citep{}` for parenthetical citations and `\citet{}` for textual citations.
- Keep images in the `images/` folder for organization.
- Compile regularly to catch errors early.

## Requirements

- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- BibTeX for bibliography management
- A LaTeX editor (TeXStudio, TeXShop, VS Code, Overleaf, etc.)

## License

This template is provided as-is for educational purposes.
