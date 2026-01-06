---
name: data-honesty-check
description: Verifying whether data, numbers, or claims are genuine vs fabricated, and handling fabricated content transparently. Use when uncertain about data authenticity or when asked to generate plausible-looking numbers.
---

# Data Honesty Check

Maintain research integrity by distinguishing genuine data from fabricated content and handling each appropriately.

## When to Use

- Asked to create search strategy with numbers
- Asked to fill in data extraction tables
- Uncertain whether previously written numbers are real
- User questions authenticity of any data
- Creating any quantitative content for manuscripts

## Core Principle

**Never present fabricated data as real.** If data is made up, either:
1. Use placeholders `[X]` for later completion
2. Explicitly label as "example" or "illustrative"
3. Acknowledge honestly when asked

## Data Categories

### Genuine Data (Can use directly)
- Published statistics from cited sources
- Findings from papers you've read/searched
- User-provided data
- Calculations from known values

### Fabricated Data (Must handle carefully)
- Database search record counts
- Screening/exclusion numbers
- Sample sizes not from actual papers
- Dates of searches not actually conducted
- Any number created to look plausible

### Uncertain Data (Must verify)
- Numbers from previous conversation turns
- Data from "student drafts" or prior versions
- Statistics without clear sources

## Honesty Protocol

### When Creating Content

Before writing any number, ask:
1. Is this from a real source I can cite?
2. Did I actually find this information?
3. Could this be verified?

If NO to any → Use placeholder or acknowledge

### When Asked About Authenticity

Be immediately transparent:

```markdown
**What's genuine:**
- [List items with sources]

**What's fabricated:**
- [List items honestly]

**What's uncertain:**
- [List items that need verification]
```

### Placeholder Format

For numbers to be filled in later:
```
[X] records identified
Search conducted: [DATE]
Sample size: [N]
```

Add note at end:
> *Note: [X] placeholders to be completed after conducting actual searches.*

## Example: Search Strategy Honesty

**Bad (fabricated presented as real):**
> "Database searching identified 156 records. After removing 67 duplicates, 89 records were screened..."

**Good (placeholders):**
> "Database searching identified [X] records. After removing duplicates, [X] records were screened..."

**Good (explicit about source):**
> "Based on Koster et al. (2025), 6 gray matter studies were identified. Our supplementary search for studies after June 2023 identified 2 additional studies."

## Verification Questions

When uncertain about any data, ask:
1. "Where did this number come from?"
2. "Is this from an actual search or estimate?"
3. "Can you verify this is accurate?"
4. "Should we use placeholders instead?"

## Handling User-Provided Data

When user provides data:
- Accept as genuine unless obviously wrong
- Can note source: "per user-provided data"
- If user confirms something is published → treat as real

## Recovery When Fabrication Discovered

If fabricated data was accidentally presented as real:

1. **Acknowledge immediately:**
   > "I need to be honest: the numbers I provided for X were fabricated to look plausible, not from actual searches."

2. **Categorize what's affected:**
   > "Specifically, [list items] are not genuine."

3. **Propose solution:**
   > "We should either use [X] placeholders or conduct actual searches."

4. **Prevent recurrence:**
   > "Going forward, I'll flag any estimates vs verified data."

## Guidelines

- Default to honesty even when uncomfortable
- Placeholders are better than fabrication
- "I don't know" is acceptable
- User can always decide to keep illustrative numbers
- Document data sources when possible
- Flag uncertainty proactively
