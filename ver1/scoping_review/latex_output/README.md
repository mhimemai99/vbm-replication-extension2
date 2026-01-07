# LaTeX Output

This folder contains the LaTeX version of the scoping review manuscript.

## Files

- `manuscript.tex` - Main LaTeX document
- `references.bib` - BibTeX reference file
- `manuscript_for_word.md` - Markdown version optimized for Word conversion

---

## Converting to Word (.docx)

### Option 1: Using the Markdown File (Easiest)

1. Go to [pandoc.org/try](https://pandoc.org/try/) or [cloudconvert.com](https://cloudconvert.com/md-to-docx)
2. Upload `manuscript_for_word.md`
3. Convert to .docx
4. Download

### Option 2: Direct in Word

1. Open Word
2. File → Open → Select `manuscript_for_word.md`
3. Word will convert it automatically
4. Save as .docx

### Option 3: Using Pandoc (if installed)

```bash
# From markdown (simpler, recommended)
pandoc manuscript_for_word.md -o manuscript.docx

# From LaTeX (more complex)
pandoc manuscript.tex --bibliography=references.bib --citeproc -o manuscript.docx
```

### Option 4: Google Docs

1. Upload `manuscript_for_word.md` to Google Drive
2. Open with Google Docs
3. File → Download → Microsoft Word (.docx)

---

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
