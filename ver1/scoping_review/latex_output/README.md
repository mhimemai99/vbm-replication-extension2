# LaTeX Output

This folder contains the LaTeX version of the scoping review manuscript.

## Files

- `manuscript.tex` - Main LaTeX document
- `references.bib` - BibTeX reference file

## How to Compile

### Option 1: Overleaf (Easiest - No Installation)

1. Go to [overleaf.com](https://www.overleaf.com)
2. Create a new project
3. Upload both `manuscript.tex` and `references.bib`
4. Click "Recompile"

### Option 2: Local Compilation

Run these commands in order:

```bash
pdflatex manuscript.tex
bibtex manuscript
pdflatex manuscript.tex
pdflatex manuscript.tex
```

(Yes, you need to run pdflatex multiple times for references to resolve)

## Adapting to Journal Templates

### Elsevier Journals
Replace the first line with:
```latex
\documentclass[review]{elsarticle}
```

### Springer Journals
Replace the first line with:
```latex
\documentclass{svjour3}
```

### APA Style
Replace the first line with:
```latex
\documentclass[jou]{apa7}
```

### Nature/Science
Download the journal's template and copy the content between `\begin{document}` and `\end{document}` into their template.

## Common Issues

1. **Missing packages**: Install via your LaTeX distribution (TeX Live, MiKTeX)
2. **Special characters**: Already escaped (ø, ö, etc.)
3. **[X] placeholders**: Replace with actual numbers from your search

## What the Skill Did

The markdown-to-latex skill converted:
- `#` headers → `\section{}`, `\subsection{}`
- `**bold**` → `\textbf{}`
- `*italic*` → `\textit{}`
- `(Author, Year)` → `\citep{author2020}`
- Markdown tables → LaTeX `tabular` environments
- Special characters → Escaped versions
- References → BibTeX format
