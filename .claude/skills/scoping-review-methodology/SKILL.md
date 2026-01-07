---
name: scoping-review-methodology
description: Conducting scoping reviews following JBI methodology and PRISMA-ScR reporting guidelines. Use when user needs to map literature, identify gaps, or conduct systematic evidence synthesis without meta-analysis.
---

# Scoping Review Methodology

Guide the conduct and reporting of scoping reviews following Joanna Briggs Institute (JBI) methodology and PRISMA-ScR guidelines.

## When to Use

- User wants to map available literature on a topic
- User needs to identify gaps in research
- User wants to clarify concepts or definitions
- User needs to examine how research is conducted in a field
- User explicitly asks for a scoping review

## Scoping vs Systematic Review

| Aspect | Scoping Review | Systematic Review |
|--------|---------------|-------------------|
| Question | Broad, exploratory | Focused, specific |
| Quality appraisal | Optional | Required |
| Synthesis | Narrative, mapping | Often meta-analysis |
| Purpose | Map literature, identify gaps | Answer specific question |

## Framework: PCC (Population, Concept, Context)

Unlike systematic reviews (PICO), scoping reviews use PCC:

- **Population**: Who is being studied?
- **Concept**: What is being examined?
- **Context**: What settings, conditions, or circumstances?

## Required Sections (PRISMA-ScR)

### 1. Title
Include "scoping review" in title.

### 2. Abstract
Structured abstract with: Background, Objectives, Methods, Results, Conclusions.

### 3. Introduction
- Rationale for the review
- Objectives stated as questions or aims

### 4. Methods
- Protocol registration/availability
- Eligibility criteria (PCC framework)
- Information sources (databases, dates)
- Search strategy (full strategy in supplement)
- Selection process
- Data extraction items
- Synthesis methods

### 5. Results
- Study selection (PRISMA flow)
- Characteristics of included studies
- Results of individual studies
- Synthesis of results

### 6. Discussion
- Summary of evidence
- Limitations
- Conclusions

## Search Strategy Template

```
Database: [Name]
Date searched: [Date]
Search string:
([Population terms])
AND
([Concept terms])
AND
([Context terms])

Filters applied: [Language, date range, etc.]
Records identified: [N]
```

## Study Selection Flow

```
Records identified (n = X)
    ↓
Duplicates removed (n = X)
    ↓
Records screened (n = X)
    ↓
Records excluded (n = X)
    ↓
Full-text assessed (n = X)
    ↓
Full-text excluded with reasons (n = X)
    ↓
Studies included (n = X)
```

## Data Extraction Template

For each included study, extract:
- Citation (authors, year, title, journal)
- Study design
- Population characteristics
- Sample size
- Key concept measured
- Context/setting
- Main findings
- Relevant to review question because...

## Charting Table Format

| Author (Year) | Country | Population | N | Method | Key Findings |
|---------------|---------|------------|---|--------|--------------|
| Smith (2020) | USA | Adults | 100 | Survey | Finding 1, 2 |

## Table Quality Standards (Critical)

Tables are the core deliverable of scoping reviews. Poor tables undermine the entire review. Follow these standards:

### 1. Sample Size Specificity

**Bad:** "N = 64" or "Multi-site"
**Good:** "32 intervention, 32 control" or "Multi-site: 1,262 total (breakdown: 600 site A, 400 site B, 262 site C)"

Always break down by relevant groups (treatment/control, smoker/non-smoker, patient/healthy).

### 2. Direction Indicators (Required)

Every quantitative finding MUST include direction:
- Use ↑ (increased) and ↓ (decreased/reduced)
- Apply consistently across ALL rows
- If no direction applies, explain why (e.g., "interaction effect only")

**Bad:** "Hippocampus" or "ACC, insula"
**Good:** "Smaller hippocampus (↓ 2.2%)" or "Thinner ACC (↓), thinner insula (↓)"

### 3. Valid Findings Only

The "Findings" column must contain ACTUAL RESULTS, not:
- Statistical categories ("Diagnosis × smoking interaction" is not a brain region)
- Vague descriptions ("Progressive loss" - loss of what? where?)
- Method descriptions ("Whole brain analysis")
- Missing data ("—" without explanation)

**Bad:** "Diagnosis × smoking interaction for subcortical"
**Good:** "No main effect of smoking; diagnosis × smoking interaction for thalamus (↓ in patients who smoke) and pallidum (↑)"

### 4. Consistency Across Rows

- Same column structure for all rows
- Same level of detail for all studies
- Same abbreviation style throughout
- If one study has direction indicators, ALL must have them

### 5. Table Abbreviations

Always include abbreviation legend below table:
```
*Abbreviations: [Abbrev1], full term; [Abbrev2], full term. Direction: ↑ increased, ↓ decreased.*
```

### 6. Self-Check Questions

Before finalizing any table, verify:
- [ ] Can a reader understand each cell without reading the paper?
- [ ] Are sample sizes broken down by relevant groups?
- [ ] Does every finding have a direction indicator?
- [ ] Are all entries actual findings (not statistical categories)?
- [ ] Is the level of detail consistent across rows?
- [ ] Are abbreviations defined?

## Quality Appraisal

Per JBI methodology, quality appraisal is **optional** for scoping reviews. If not conducted, state:
> "Consistent with scoping review methodology, formal quality assessment of included studies was not conducted."

## Synthesis Approaches

Scoping reviews typically use:

1. **Narrative synthesis**: Describe findings in prose
2. **Tabular presentation**: Summarize study characteristics
3. **Mapping**: Visualize gaps and coverage
4. **Frequency counts**: How many studies address X?

NOT typically used:
- Meta-analysis
- Effect size pooling
- Forest plots

## Common Pitfalls

### Avoid:
- Overclaiming (scoping reviews identify gaps, not answer questions)
- Treating as systematic review (no meta-analysis needed)
- Ignoring heterogeneity (describe, don't resolve)
- Missing gaps analysis (the main purpose!)

### Include:
- Clear statement that this is a scoping review
- PCC framework for eligibility
- Acknowledgment of limitations
- Explicit gaps identification
- Directions for future research

## Key Citations

Always cite:
- JBI methodology: Peters et al. (2020)
- PRISMA-ScR: Tricco et al. (2018)

## Output: Gaps Analysis

The key output of a scoping review is identifying what's missing:

```markdown
## Gaps Identified

1. **Population gap**: No studies in [population X]
2. **Methodological gap**: No studies using [method Y]
3. **Conceptual gap**: [Concept Z] not examined
4. **Geographic gap**: Limited to [regions]

## Implications for Future Research

These gaps suggest priority areas for future research:
- Study [concept] in [population]
- Use [method] to examine [question]
```

## Guidelines

- Be transparent about search limitations
- Document everything for reproducibility
- Focus on mapping, not judging quality
- Identify gaps explicitly - this is the main contribution
- Use tables to support narrative, not replace it
