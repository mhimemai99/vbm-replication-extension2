---
name: manuscript-review-iteration
description: Self-review as peer reviewer with iterative improvement cycles. Use when user wants to improve manuscript quality through systematic review and revision.
---

# Manuscript Review Iteration

Systematically improve manuscript quality by acting as a peer reviewer, identifying issues, prioritizing revisions, and iterating until quality standards are met.

## When to Use

- User asks to review or improve a manuscript
- User asks to "act as reviewer"
- User wants feedback on writing quality
- User needs to prepare manuscript for submission
- After completing a draft that needs quality checking

## Process

### Step 1: Initial Review (Act as Peer Reviewer)

Read the manuscript and identify issues in these categories:

**Critical Issues** (must address):
- Major methodological flaws
- Overclaimed or unsupported claims
- Factual errors or citation problems
- Title-content mismatch
- Logical inconsistencies

**Important Issues** (should address):
- Academic writing style problems
- Missing PRISMA/reporting requirements
- Insufficient limitations discussion
- Contradictions not acknowledged

**Low Priority Issues** (address if time permits):
- Redundant tables/figures
- Language precision
- Minor formatting

### Step 2: Provide Reviewer Report

Format feedback as a structured review:

```markdown
## Peer Review: [Manuscript Title]

### Overall Assessment
[Brief summary of strengths and main concerns]

### Major Issues
1. [Issue]: [Details and suggestion]
2. [Issue]: [Details and suggestion]

### Minor Issues
1. [Issue]: [Details]

### Suggestions for Improvement
- [Suggestion 1]
- [Suggestion 2]

### Recommendation
[Major revision / Minor revision / Accept]
```

### Step 3: Prioritized Revision

Address issues in order:
1. Critical issues first
2. Important issues second
3. Low priority if time permits

For each revision:
- Make the change
- Document what was changed
- Note the rationale

### Step 4: Re-Review Decision Function

After each iteration, evaluate:

```
IF any Critical issue remains = YES:
    → RE-REVIEW NEEDED (next iteration)

ELSE IF multiple Important issues remain = YES:
    → RE-REVIEW NEEDED (next iteration)

ELSE IF only Low priority issues remain:
    → FINALIZE (acceptable for submission)

ELSE:
    → FINALIZE
```

### Step 5: Document Changes

Maintain a revision log:

```markdown
### Iteration [N] ([Date])

**Issues Addressed:**
| Issue | Category | Action Taken |
|-------|----------|--------------|
| [Issue] | Major/Minor | [What was done] |

**Files Modified:**
- file1.md
- file2.md

**Re-Review Check:**
- Critical issues remaining: [YES/NO]
- Important issues remaining: [YES/NO]
- Decision: [RE-REVIEW / FINALIZE]
```

## Quality Checklist

Before finalizing, verify:
- [ ] Title accurately reflects content
- [ ] All claims appropriately hedged
- [ ] Contradictory findings acknowledged
- [ ] Limitations comprehensive
- [ ] Reporting requirements met (PRISMA, etc.)
- [ ] All citations verified
- [ ] No redundant content
- [ ] Academic prose throughout

## Common Issues to Check

### Writing Style
- Bullet points instead of prose
- Numbered lists where paragraphs needed
- Bold/italic overuse
- AI-like patterns (e.g., "Here's", "Let me")
- Overly promotional language

### Logic and Claims
- Overclaiming (e.g., "demonstrates" when "suggests")
- Missing hedging language
- Unsupported causal claims
- Circular reasoning

### Structure
- Redundant sections
- Missing transitions
- Title-content mismatch
- Aims not addressed in results

## Guidelines

- Be critical but constructive
- Prioritize ruthlessly - not all issues equal
- Document everything for transparency
- Multiple iterations are normal
- Stop when diminishing returns
