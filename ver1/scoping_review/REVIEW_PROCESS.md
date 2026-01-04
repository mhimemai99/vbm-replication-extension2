# Manuscript Review and Revision Process

## Overview

This document describes the iterative review process used to improve manuscript quality. The process involves self-review acting as a peer reviewer, followed by systematic revisions.

## Process Steps

1. **Draft Completion**: Complete initial manuscript draft
2. **Self-Review**: Act as peer reviewer - identify major and minor issues
3. **Prioritized Revision**: Address issues by priority (major before minor)
4. **Document Changes**: Log all changes made in each iteration
5. **Re-Review Check**: Evaluate if further revision needed (see decision function below)
6. **Iterate or Finalize**: If re-review needed → repeat from step 2; if not → finalize

---

## Re-Review Decision Function

After each iteration, evaluate the manuscript against these criteria:

### Decision Criteria

| Category | Question | Weight |
|----------|----------|--------|
| Major Issues | Are there any remaining major methodological flaws? | Critical |
| Major Issues | Are claims still overclaimed or unsupported? | Critical |
| Major Issues | Are there factual errors or citation problems? | Critical |
| Minor Issues | Is writing style consistently academic? | Important |
| Minor Issues | Are there redundant sections/tables? | Low |
| Minor Issues | Could language be more precise? | Low |

### Decision Rules

```
IF any Critical issue = YES:
    → RE-REVIEW NEEDED (next iteration)

ELSE IF multiple Important issues = YES:
    → RE-REVIEW NEEDED (next iteration)

ELSE IF only Low issues remain:
    → FINALIZE (acceptable for submission)

ELSE:
    → FINALIZE
```

### Re-Review Output Format

```
## Re-Review Check: Iteration [N]

Critical Issues:
- [ ] Major methodological flaws: [YES/NO] - [details if YES]
- [ ] Overclaimed/unsupported claims: [YES/NO] - [details if YES]
- [ ] Factual/citation errors: [YES/NO] - [details if YES]

Important Issues:
- [ ] Academic writing style: [YES/NO] - [details if YES]

Low Priority Issues:
- [ ] Redundancies: [YES/NO] - [details if YES]
- [ ] Language precision: [YES/NO] - [details if YES]

DECISION: [RE-REVIEW NEEDED / FINALIZE]
```

---

## Review Criteria

### Major Issues (Must Address)
- Title-content alignment
- Methodological transparency (PRISMA, search strategies)
- Logical validity of claims (e.g., "convergence" claims)
- Contradictions in findings
- Citation accuracy

### Minor Issues (Address if Possible)
- Redundant tables/figures
- Speculative language
- Missing effect sizes
- Structural redundancy

---

## Revision Log

### Iteration 1 (2026-01-04)

**Reviewer Comments Addressed:**

| Issue | Category | Action Taken |
|-------|----------|--------------|
| Title-Content Mismatch | Major | Revised title to reflect gap identification rather than structural evidence |
| Base-rate convergence problem | Major | Added acknowledgment that ACC/insula/prefrontal are commonly reported regions |
| fMRI heterogeneity/contradictions | Major | Explicitly addressed decreased vs. increased insula findings |
| Missing PRISMA flow | Major | Added study selection numbers and flow description |
| Musket 2026 status | Minor | Confirmed as published, removed "[In press]" |
| Table 3 redundancy | Minor | Condensed to prose statement |
| Introduction aim redundancy | Minor | Restructured aims to avoid circularity |

**Files Modified:**
- 01_Introduction.md
- 03_Results.md
- 04_Discussion.md
- 05_References.md

**Re-Review Check: Iteration 1**

Critical Issues:
- [x] Major methodological flaws: NO
- [x] Overclaimed/unsupported claims: NO - cautious language added throughout
- [x] Factual/citation errors: NO - Musket 2026 fixed

Important Issues:
- [x] Academic writing style: NO - prose style maintained

Low Priority Issues:
- [ ] Redundancies: MINOR - Methods section could be streamlined
- [ ] Language precision: MINOR - some phrases could be tightened

**DECISION: FINALIZE** - No critical or important issues remain. Low priority issues are acceptable for submission.

---

### Iteration 2 (2026-01-04)

**Reviewer Comments Addressed:**

| Issue | Category | Action Taken |
|-------|----------|--------------|
| Methods section unprofessional | Major | Complete rewrite removing bullet points, numbered lists, bold labels, horizontal rules |
| Fragmented structure | Major | Consolidated into flowing academic paragraphs |
| AI-like formatting | Major | Removed all stylistic markers (---, ###, **bold**) |

**Files Modified:**
- 02_Methods.md

**Re-Review Check: Iteration 2**

Critical Issues:
- [x] Major methodological flaws: NO
- [x] Overclaimed/unsupported claims: NO
- [x] Factual/citation errors: NO

Important Issues:
- [x] Academic writing style: NO - Methods now in proper prose

Low Priority Issues:
- [x] Redundancies: NO
- [x] Language precision: NO

**DECISION: FINALIZE** - All sections now in proper academic prose

---

## Quality Checklist (Final Verification)

- [x] Title accurately reflects content
- [x] All claims are appropriately hedged
- [x] Contradictory findings acknowledged
- [x] Limitations section comprehensive
- [x] PRISMA-ScR requirements met (study selection flow added)
- [x] All citations verified
- [x] No redundant tables/figures
- [x] Academic prose throughout

---

## Final Status

**MANUSCRIPT FINALIZED**: 2026-01-04 (Iteration 2)

All sections revised to proper academic prose. Manuscript ready for submission.
