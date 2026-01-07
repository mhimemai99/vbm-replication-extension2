# Markdown to LaTeX Conversion

Convert academic manuscript markdown files to LaTeX format for submission to journals with different templates.

## When to Use

- User wants to convert markdown manuscript to LaTeX
- User needs to submit to a journal requiring LaTeX format
- User asks to "convert to LaTeX" or "make this LaTeX"
- User wants output compatible with journal templates (Elsevier, Springer, APA, etc.)

## Related Skills

- **reference-management-apa**: Ensure citations are properly formatted before conversion
- **academic-prose-writing**: Clean up text before conversion

## LaTeX Basics for Non-LaTeX Users

LaTeX is a typesetting system used by academic journals. Key concepts:
- Commands start with backslash: `\section{Title}`
- Special characters must be escaped: `%`, `&`, `$`, `#`, `_`, `{`, `}`
- Comments use `%`
- Environments wrap content: `\begin{table}...\end{table}`

## Conversion Reference Table

### Document Structure

| Markdown | LaTeX |
|----------|-------|
| `# Title` | `\title{Title}` |
| `## Section` | `\section{Section}` |
| `### Subsection` | `\subsection{Subsection}` |
| `#### Subsubsection` | `\subsubsection{Subsubsection}` |

### Text Formatting

| Markdown | LaTeX |
|----------|-------|
| `**bold**` | `\textbf{bold}` |
| `*italic*` | `\textit{italic}` |
| `***bold italic***` | `\textbf{\textit{bold italic}}` |
| `` `code` `` | `\texttt{code}` |
| `> blockquote` | `\begin{quote}...\end{quote}` |

### Lists

**Bulleted list:**
```markdown
- Item 1
- Item 2
```
→
```latex
\begin{itemize}
  \item Item 1
  \item Item 2
\end{itemize}
```

**Numbered list:**
```markdown
1. First
2. Second
```
→
```latex
\begin{enumerate}
  \item First
  \item Second
\end{enumerate}
```

### Citations

| Markdown | LaTeX (natbib) | LaTeX (biblatex) |
|----------|----------------|------------------|
| `(Smith, 2020)` | `\citep{smith2020}` | `\parencite{smith2020}` |
| `Smith (2020)` | `\citet{smith2020}` | `\textcite{smith2020}` |
| `(Smith, 2020; Jones, 2021)` | `\citep{smith2020,jones2021}` | `\parencite{smith2020,jones2021}` |

### Tables

**Markdown:**
```markdown
| Study | N | Finding |
|-------|---|---------|
| Smith (2020) | 50 | Significant |
| Jones (2021) | 100 | Not significant |
```

**LaTeX:**
```latex
\begin{table}[htbp]
\centering
\caption{Study characteristics}
\label{tab:studies}
\begin{tabular}{lrl}
\hline
Study & N & Finding \\
\hline
Smith (2020) & 50 & Significant \\
Jones (2021) & 100 & Not significant \\
\hline
\end{tabular}
\end{table}
```

### Special Characters

These must be escaped in LaTeX:

| Character | LaTeX |
|-----------|-------|
| `%` | `\%` |
| `&` | `\&` |
| `$` | `\$` |
| `#` | `\#` |
| `_` | `\_` |
| `{` | `\{` |
| `}` | `\}` |
| `~` | `\textasciitilde{}` |
| `^` | `\textasciicircum{}` |
| `\` | `\textbackslash{}` |
| `<` | `\textless{}` |
| `>` | `\textgreater{}` |

### Greek Letters and Symbols

| Symbol | LaTeX |
|--------|-------|
| α | `$\alpha$` |
| β | `$\beta$` |
| ≈ | `$\approx$` |
| ± | `$\pm$` |
| × | `$\times$` |
| ≤ | `$\leq$` |
| ≥ | `$\geq$` |

### URLs and DOIs

```latex
\url{https://doi.org/10.1000/example}
% or with hyperref package:
\href{https://doi.org/10.1000/example}{Link text}
```

## Conversion Process

### Step 1: Create Document Preamble

Generate a basic preamble (user can swap for journal template later):

```latex
\documentclass[12pt]{article}

% Essential packages
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage{booktabs}  % Better tables
\usepackage{natbib}    % Citations
\usepackage{hyperref}  % Clickable links
\usepackage{setspace}  % Line spacing

% Document settings
\doublespacing
\usepackage[margin=1in]{geometry}

\begin{document}
```

### Step 2: Convert Title and Abstract

```latex
\title{Your Title Here}
\author{Author One\textsuperscript{1} \and Author Two\textsuperscript{2}}
\date{}
\maketitle

\begin{abstract}
Your abstract text here...
\end{abstract}

\textbf{Keywords:} keyword1, keyword2, keyword3
```

### Step 3: Convert Body Sections

Process each markdown section:
1. Convert headers to `\section{}`, `\subsection{}`, etc.
2. Escape special characters
3. Convert formatting (bold, italic)
4. Convert lists
5. Convert tables
6. Convert citations

### Step 4: Convert References

**Option A: Inline references (simple)**
```latex
\begin{thebibliography}{99}

\bibitem{deleon2005}
de Leon, J., \& Diaz, F. J. (2005). A meta-analysis of worldwide studies...

\bibitem{hayes2006}
Hayes, S. C., Luoma, J. B., Bond, F. W., Masuda, A., \& Lillis, J. (2006)...

\end{thebibliography}
```

**Option B: BibTeX file (recommended)**

Create a `.bib` file:
```bibtex
@article{deleon2005,
  author = {de Leon, Jose and Diaz, Francisco J.},
  title = {A meta-analysis of worldwide studies...},
  journal = {Schizophrenia Research},
  year = {2005},
  volume = {76},
  number = {2--3},
  pages = {135--157},
  doi = {10.1016/j.schres.2005.02.010}
}
```

Then in main document:
```latex
\bibliographystyle{apalike}  % or other style
\bibliography{references}     % references.bib file
```

### Step 5: Close Document

```latex
\end{document}
```

## Output Format

When converting, produce TWO files:

1. **main.tex** - The main document
2. **references.bib** - BibTeX references (if using Option B)

## Journal Template Compatibility

The converted LaTeX is designed to be modular. To use with a journal template:

1. **Elsevier**: Replace `\documentclass{article}` with `\documentclass{elsarticle}`
2. **Springer**: Use `\documentclass{svjour3}`
3. **APA**: Use `\documentclass{apa7}`
4. **Nature**: Use their specific template

Most templates only need you to:
- Change the `\documentclass` line
- Add journal-specific packages
- Keep your content between `\begin{document}` and `\end{document}`

## Common Conversion Pitfalls

1. **Unescaped special characters** - Always escape `%`, `&`, `$`, `#`, `_`
2. **Tables with merged cells** - LaTeX tables are more complex; may need `\multicolumn{}`
3. **Figure paths** - Use forward slashes, relative paths
4. **Citation keys** - Must be valid identifiers (no spaces, start with letter)
5. **Math mode** - Statistics like `r = 0.34` should be `$r = 0.34$`

## Quality Checklist

Before delivering converted LaTeX:

- [ ] All special characters escaped
- [ ] All sections converted to proper commands
- [ ] Tables use `booktabs` style (`\toprule`, `\midrule`, `\bottomrule`)
- [ ] Citations use consistent style
- [ ] References in proper BibTeX format
- [ ] Document compiles without errors
- [ ] Statistics in math mode where appropriate

## Example: Full Conversion

**Input (Markdown):**
```markdown
# Introduction

Tobacco smoking is **significantly** more prevalent among individuals
with schizophrenia, with rates 2-3× higher (de Leon & Diaz, 2005).

| Study | N | Effect |
|-------|---|--------|
| Smith | 50 | d = 0.8 |
```

**Output (LaTeX):**
```latex
\section{Introduction}

Tobacco smoking is \textbf{significantly} more prevalent among individuals
with schizophrenia, with rates 2--3$\times$ higher \citep{deleon2005}.

\begin{table}[htbp]
\centering
\caption{Study characteristics}
\begin{tabular}{lrl}
\toprule
Study & N & Effect \\
\midrule
Smith & 50 & $d = 0.8$ \\
\bottomrule
\end{tabular}
\end{table}
```
