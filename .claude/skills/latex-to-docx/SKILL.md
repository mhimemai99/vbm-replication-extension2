# LaTeX to DOCX Conversion

Convert LaTeX manuscripts to Microsoft Word format (.docx) for collaborators who prefer Word editing.

## When to Use

- Collaborators need to edit in Word
- Journal requires Word submission
- User asks to "convert to Word" or "make a docx"
- Need track changes or commenting features

## Related Skills

- **markdown-to-latex**: Convert markdown first, then to docx
- **reference-management-apa**: Ensure citations work in Word

## Conversion Methods

### Method 1: Pandoc (Recommended)

Pandoc is the gold standard for document conversion.

**Basic conversion:**
```bash
pandoc manuscript.tex -o manuscript.docx
```

**With bibliography:**
```bash
pandoc manuscript.tex --bibliography=references.bib --citeproc -o manuscript.docx
```

**With reference document for styling:**
```bash
pandoc manuscript.tex --reference-doc=template.docx -o manuscript.docx
```

**Full command with all options:**
```bash
pandoc manuscript.tex \
  --bibliography=references.bib \
  --citeproc \
  --reference-doc=template.docx \
  -o manuscript.docx
```

### Method 2: Online Converters

If pandoc is not available:

1. **Overleaf** → Export as .docx (limited)
2. **latex2rtf** → Convert to RTF, open in Word
3. **Online tools**:
   - https://www.vertopal.com/
   - https://cloudconvert.com/tex-to-docx

### Method 3: Manual Conversion

For complex documents or when automated conversion fails:

1. Compile LaTeX to PDF
2. Copy text from PDF to Word
3. Manually reformat tables and equations
4. Re-insert citations using Word's citation manager

## Pandoc Installation

**macOS:**
```bash
brew install pandoc
```

**Ubuntu/Debian:**
```bash
sudo apt-get install pandoc
```

**Windows:**
```bash
choco install pandoc
# or download from https://pandoc.org/installing.html
```

## Formatting Preservation

### What Converts Well
- Sections and headings
- Bold, italic, underline
- Numbered and bulleted lists
- Basic tables
- In-text citations (with --citeproc)
- Footnotes

### What May Need Manual Fixing
- Complex tables (merged cells, multi-page)
- Equations (convert to Word equation editor)
- Cross-references (Table 1, Figure 2)
- Custom LaTeX commands
- Special characters

## Reference Document (Template)

Create a Word template for consistent styling:

1. Create a new Word document
2. Define styles:
   - Heading 1, 2, 3 (for sections)
   - Normal (body text)
   - Table style
   - Caption style
3. Save as `template.docx`
4. Use with `--reference-doc=template.docx`

## Citation Handling

### Option A: Convert citations to plain text
```bash
pandoc manuscript.tex --citeproc --bibliography=references.bib -o manuscript.docx
```
Citations become "(Author, Year)" text - not editable as Word citations.

### Option B: Keep as fields (for Zotero/Mendeley users)
After conversion, collaborators can:
1. Delete plain-text citations
2. Re-insert using Zotero/Mendeley Word plugin
3. This enables bibliography regeneration

### Option C: Use CSL for specific journal style
```bash
pandoc manuscript.tex \
  --citeproc \
  --bibliography=references.bib \
  --csl=apa.csl \
  -o manuscript.docx
```

Download CSL files from: https://www.zotero.org/styles

## Table Conversion

LaTeX tables often need manual adjustment in Word.

**Before conversion**, simplify tables:
- Remove complex column specifications
- Avoid \multicolumn, \multirow if possible
- Use simple `|l|c|r|` column types

**After conversion**:
1. Select table in Word
2. Table Design → Apply table style
3. Adjust column widths
4. Fix any merged cells manually

## Equations

LaTeX equations may not convert perfectly.

**Options:**
1. **Let pandoc try**: Often works for simple equations
2. **Convert to images**: Render in LaTeX, insert as images
3. **Use Word equation editor**: Re-type complex equations
4. **MathType**: Commercial plugin for better equation handling

## Conversion Process

### Step 1: Prepare LaTeX File

Ensure your .tex file:
- Compiles without errors
- Has all packages that pandoc supports
- Uses standard LaTeX commands

### Step 2: Run Pandoc

```bash
cd /path/to/latex/folder
pandoc manuscript.tex --bibliography=references.bib --citeproc -o manuscript.docx
```

### Step 3: Review in Word

Open the .docx and check:
- [ ] All sections present
- [ ] Tables formatted correctly
- [ ] Citations rendered
- [ ] Equations readable
- [ ] No missing text

### Step 4: Manual Fixes

Common fixes needed:
- Adjust table formatting
- Fix equation rendering
- Update cross-references
- Apply journal-specific styling

## Troubleshooting

### "Unknown LaTeX command"
Pandoc doesn't support all LaTeX packages. Remove or simplify custom commands.

### Tables look wrong
Simplify the LaTeX table structure before conversion.

### Citations not rendering
Ensure you use `--citeproc` and `--bibliography=file.bib`

### Special characters broken
Check encoding: use UTF-8 throughout.

### Missing sections
Check for LaTeX errors that cause pandoc to skip content.

## Output Quality Checklist

Before sending to collaborators:

- [ ] Document opens in Word without errors
- [ ] All text is present and readable
- [ ] Tables are properly formatted
- [ ] Citations appear correctly
- [ ] Page breaks are reasonable
- [ ] Fonts are standard (Times New Roman, Arial)
- [ ] Line spacing is appropriate (double for manuscripts)

## Example Workflow

```bash
# 1. Navigate to latex folder
cd ver1/scoping_review/latex_output

# 2. Convert with bibliography
pandoc manuscript.tex \
  --bibliography=references.bib \
  --citeproc \
  -o manuscript.docx

# 3. Check output
ls -la manuscript.docx
```

## Tips for Collaborators

Include these instructions when sharing:

1. **Track Changes**: Enable before editing
2. **Comments**: Use Word comments for feedback
3. **Don't reformat**: Keep styling minimal
4. **Save as .docx**: Don't save as .doc (old format)
5. **Version naming**: Use `manuscript_v2_initials.docx`
