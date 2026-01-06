---
name: citation-needed-check
description: Reviewing text to identify claims that need academic citations, finding appropriate sources, and adding properly formatted references. Use when reviewing manuscript for missing citations or when writing claims that need grounding. Works with due-diligence-research to find sources and reference-management-apa to format them.
---

# Citation Needed Check

Review academic text to identify claims requiring citations, find appropriate sources, and integrate references properly.

## When to Use

- Reviewing manuscript draft for missing citations
- Writing claims that need academic grounding
- User asks to "check if references are needed"
- Adding citations to existing text
- Verifying all claims are properly supported

## Related Skills (Use Together)

- **due-diligence-research**: Find sources for claims
- **reference-management-apa**: Format citations properly
- **contradiction-acknowledgment**: When sources conflict
- **data-honesty-check**: Verify sources are real

## What Needs Citation

### ALWAYS Cite

| Claim Type | Example | Needs Citation? |
|------------|---------|-----------------|
| Statistics/numbers | "Rates are 2-3x higher" | ✓ Yes |
| Prevalence data | "affects 50% of patients" | ✓ Yes |
| Effect sizes | "d = 0.8" | ✓ Yes |
| Mechanisms | "caused by dopamine dysfunction" | ✓ Yes |
| Previous findings | "studies have shown..." | ✓ Yes |
| Methodological claims | "fMRI measures blood oxygenation" | ✓ Yes |
| Definitions | "Psychological flexibility is defined as..." | ✓ Yes |
| Historical claims | "First described in 1950" | ✓ Yes |

### MAY NOT Need Citation

| Claim Type | Example | Citation Needed? |
|------------|---------|-----------------|
| Common knowledge | "The brain has two hemispheres" | Usually no |
| Your own study's findings | "We found that..." | No (it's your data) |
| Logical inferences | "Therefore, X suggests Y" | No (if premises cited) |
| Author's interpretation | "This may indicate..." | No (it's your analysis) |

### GREY AREA (Cite If Uncertain)

When in doubt, cite. Better to over-cite than under-cite.

## Citation Checking Process

### Step 1: Scan for Claim Types

Read each sentence and identify:
- Factual claims (need citation)
- Interpretations (may not need)
- Your own findings (don't need)

Mark suspected uncited claims:
```markdown
"BOLD signal is generated predominantly in gray matter [CITATION NEEDED]"
```

### Step 2: Categorize Claims

```markdown
## Citation Audit

### Claims Needing Citations
1. "Rates are 2-3x higher" - needs prevalence source
2. "BOLD signal is generated in gray matter" - needs neuroscience source
3. "ACT is effective for smoking cessation" - needs meta-analysis

### Claims Already Cited
1. "...associated with gray matter reductions (Koster et al., 2025)"

### Claims Not Needing Citations
1. "We focused on gray matter outcomes" - methodological choice
2. "This suggests..." - author interpretation
```

### Step 3: Find Sources

For each uncited claim:

1. **Search for evidence** (use due-diligence-research skill)
   - Academic databases (PubMed, PsycINFO, etc.)
   - Prefer: reviews, meta-analyses, seminal papers
   - Avoid: non-peer-reviewed sources

2. **Verify source exists and is accessible**
   - Check DOI works
   - Confirm authors and year correct
   - Read abstract to confirm relevance

3. **Assess source quality**
   - Peer-reviewed? ✓
   - Recent? (note if dated)
   - Reputable journal? ✓
   - Relevant to claim? ✓

### Step 4: Add In-Text Citations

Format per APA 7th:

**Single author:**
> "...higher rates (Smith, 2020)."
> "Smith (2020) found that..."

**Two authors:**
> "...higher rates (Smith & Jones, 2020)."

**Three+ authors:**
> "...higher rates (Smith et al., 2020)."

**Multiple sources:**
> "...higher rates (Jones, 2019; Smith, 2020)."

**Direct quote:**
> "...described as 'highly prevalent' (Smith, 2020, p. 15)."

### Step 5: Update Reference List

For each new citation:
1. Create full APA reference
2. Add to reference list alphabetically
3. Verify no duplicates
4. Check DOI/URL works

## Output Format

```markdown
## Citation Check Report

### Document Reviewed
[Document name/section]

### Claims Requiring Citations

| # | Claim | Type | Suggested Source | Status |
|---|-------|------|------------------|--------|
| 1 | "Rates are 2-3x higher" | Prevalence | de Leon & Diaz (2005) | Added |
| 2 | "BOLD in gray matter" | Mechanism | Logothetis (2001) | Added |
| 3 | "No studies examined X" | Gap claim | Our search | Verified |

### Suggested Text Revisions

**Original:**
> Tobacco smoking rates are 2-3x higher in schizophrenia.

**Revised:**
> Tobacco smoking rates are two to three times higher among individuals with schizophrenia compared to the general population (de Leon & Diaz, 2005).

### New References Added

de Leon, J., & Diaz, F. J. (2005). A meta-analysis of worldwide studies demonstrates an association between schizophrenia and tobacco smoking behaviors. *Schizophrenia Research*, *76*(2–3), 135–157. https://doi.org/10.1016/j.schres.2005.02.010

### Verification Checklist
- [ ] All factual claims cited
- [ ] All citations have references
- [ ] All references cited in text
- [ ] DOIs verified working
- [ ] Sources are peer-reviewed
```

## Common Patterns Needing Citations

### Introduction
- Prevalence/incidence statistics
- Background on condition/phenomenon
- Previous research findings
- Theoretical frameworks

### Methods
- Methodological guidelines followed (e.g., JBI, PRISMA)
- Validated instruments used
- Statistical approaches

### Results
- Usually fewer citations needed (your data)
- May cite if comparing to benchmarks

### Discussion
- When comparing to prior literature
- When explaining mechanisms
- When citing limitations noted by others

## Quality Checks

### Before Finalizing

- [ ] Every factual claim has citation
- [ ] Citation format consistent (APA 7th)
- [ ] All in-text citations in reference list
- [ ] All references cited somewhere in text
- [ ] No fabricated sources
- [ ] DOIs/URLs verified
- [ ] Page numbers for direct quotes

### Red Flags

Watch for:
- Vague citations: "studies show..." (which studies?)
- Missing citations after statistics
- Uncited mechanism claims
- Unsupported "evidence suggests..."

## Integration with Other Skills

This skill works as part of a workflow:

```
1. Write draft text
   ↓
2. CITATION-NEEDED-CHECK: Identify uncited claims
   ↓
3. DUE-DILIGENCE-RESEARCH: Find sources
   ↓
4. REFERENCE-MANAGEMENT-APA: Format citations
   ↓
5. DATA-HONESTY-CHECK: Verify sources are real
   ↓
6. Final verified text with citations
```

## Guidelines

- When in doubt, cite
- Use primary sources when possible
- Cite most recent AND seminal works
- Don't over-cite common knowledge
- Verify every source is real
- Keep reference list updated
- Match citation style to target journal
