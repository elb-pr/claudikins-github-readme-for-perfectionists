# Influencer Marketing Skills - Pattern Synthesis

> **ARCHIVED:** Patterns from this file have been integrated into the GRFP pipeline reference files:
>
> - Sections 1, 4 → `pen-wielding/references/style-guide.md` (Humanisation Patterns, Reusable Phrases)
> - Section 2 (tables) → `pen-wielding/references/structural-templates.md` (Results/Metrics Tables)
> - Section 2 (visuals) → `pen-wielding/references/visual-engineering.md` (ASCII Visualisations)
> - Section 3 → `think-tank/SKILL.md` + `deep-dive/references/what-to-extract.md` (Validation Methodology)
> - Section 5 → `pen-wielding/references/anti-patterns.md` (Writing/Research Anti-Patterns)
>
> This file is preserved as a reference for the original source material.
> **Integration Date:** 2026-01-19

---

Extracted from 18 SKILL.md files in the influencer-marketing-claude-skills repository. These patterns improve documentation quality, humanise technical writing, and provide actionable structural templates.

---

## 1. Writing Style Patterns

### Tone & Voice

| Pattern                      | Description                                          | Example                                                         |
| ---------------------------- | ---------------------------------------------------- | --------------------------------------------------------------- |
| **Human-first address**      | Use "you" directly, speak TO the reader, not AT them | "This skill helps you..." not "This system enables users to..." |
| **Conversational warmth**    | Casual but professional, no corporate-speak          | "We love your creative voice!"                                  |
| **Action-oriented language** | Active verbs, direct commands                        | "Design", "Create", "Plan" not "The system will..."             |
| **Empowering assumptions**   | Assume reader competence while providing structure   | Tips not mandates                                               |

### Confidence Framing

| Pattern                        | Description                                   | Example                                                              |
| ------------------------------ | --------------------------------------------- | -------------------------------------------------------------------- | ----- | ---------- | --- |
| **Explicit confidence levels** | Use High/Med/Low ratings alongside claims     | `                                                                    | Claim | Confidence | `   |
| **Tiered urgency**             | Must/Should/Nice-to-Have classifications      | "Must Fix" > "Should Fix" > "Nice to Have"                           |
| **Assessment verdicts**        | End calculations with human-readable verdicts | "**Assessment**: Profitable"                                         |
| **Caveat callouts**            | Flag limitations with warning symbols         | `Warning: Use for directional comparison, not absolute measurement.` |

### Narrative Techniques

| Technique                    | Description                                   | Application                                  |
| ---------------------------- | --------------------------------------------- | -------------------------------------------- |
| **Progressive disclosure**   | Overview -> Details -> Examples -> Variations | TL;DR -> Features -> Full Docs               |
| **Problem-solution pairing** | Every issue immediately paired with solution  | "What we see -> What we need -> Why"         |
| **Value before ask**         | State benefits BEFORE requirements            | Show what they get before installation steps |
| **Lead with outcomes**       | Results first, methodology in appendix        | "Bottom Line: Campaign exceeded targets"     |

### Instead of X, Write Y

| Weak                                | Strong                                     | Why                              |
| ----------------------------------- | ------------------------------------------ | -------------------------------- |
| "We achieved 2.4M reach"            | "We reached 2.4M people, 20% above target" | Context makes numbers meaningful |
| "Fix disclosure"                    | "Add #ad to caption"                       | Specific beats vague             |
| "Users can optionally configure..." | "Configure your preferences in..."         | Direct address over passive      |
| "The system enables..."             | "This helps you..."                        | Human over system                |
| "Consider implementing..."          | "Implement..."                             | Commands over suggestions        |

---

## 2. Structural Patterns

### Table Formats

**Comparison Table** - For options/features:

```markdown
| Feature     | What It Does  | When to Use |
| ----------- | ------------- | ----------- |
| [Feature 1] | [Description] | [Use case]  |
```

**Results Table** - For metrics:

```markdown
| Metric   | Result  | Target   | vs. Target | vs. Benchmark | Status      |
| -------- | ------- | -------- | ---------- | ------------- | ----------- |
| [Metric] | [Value] | [Target] | [+/-X%]    | [+/-X%]       | check/cross |
```

**Timeline Table** - For processes:

```markdown
| Step | When | Action | Owner | Notes |
| ---- | ---- | ------ | ----- | ----- |
```

**Risk Table** - For known issues:

```markdown
| Risk | Likelihood | Impact | Mitigation |
| ---- | ---------- | ------ | ---------- |
```

**Feature-Benefit-HowTo** - For feature docs:

```markdown
| Feature | Benefit | How to Show |
| ------- | ------- | ----------- |
```

### Section Templates

**Standard Opener** (applies to any documentation):

```markdown
# [Title]

[Single sentence value proposition]

## When to Use

- [Trigger condition 1]
- [Trigger condition 2]

## What This Does

1. **[Capability]**: [Description]
2. **[Capability]**: [Description]

## How to Use

[Quick start instructions]
```

**Executive Summary Block**:

```markdown
## Summary

**Bottom Line**: [One-line verdict]

| Metric | Result | Status |
| ------ | ------ | ------ |

**Key Takeaway**: [Most important insight]
**Recommendation**: [Clear next action]
```

**Learnings Section**:

```markdown
## Learnings

| Learning          | Evidence             | Implication           |
| ----------------- | -------------------- | --------------------- |
| [What we learned] | [Data supporting it] | [What to do about it] |
```

**Do/Don't Parallel Lists**:

```markdown
### Best Practices

**Do:**

- [Good practice 1]
- [Good practice 2]

**Don't:**

- [Bad practice 1]
- [Bad practice 2]
```

### Progressive Elaboration Flow

```
1. Overview (what/why) - single paragraph
2. When to Use (triggers) - bullet list
3. Features (capabilities) - numbered with bold keywords
4. Quick Start (how) - code blocks
5. Detailed Config (specifics) - tables
6. Examples (concrete) - full worked example
7. Tips (wisdom) - numbered list
8. Related (ecosystem) - links
```

### Visual Elements

**Status Indicators**:

- `check` Pass / `cross` Fail
- `warning` Warning/Minor Issue
- Green/Yellow/Red priority system

**ASCII Visualisations**:

```
Metric  [================    ] 80%
Metric  [========            ] 40%
```

**Progress Funnel**:

```
Stage 1  [XXXXXXXXXX] 1,000  (100%)
              |
Stage 2  [XXXXXXX   ]   700  (70%)
              |
Stage 3  [XXXX      ]   400  (40%)
```

---

## 3. Research Methodology Patterns

### Pre-Writing Research

| Phase                          | Activities                           | Output            |
| ------------------------------ | ------------------------------------ | ----------------- |
| **Define Scope**               | Establish parameters before research | Parameter block   |
| **Gather Context**             | Structured information capture       | Context template  |
| **Multi-Source Triangulation** | Check multiple sources               | Source comparison |
| **Validation**                 | Test claims, run examples            | Evidence notes    |

### Context Gathering Template

```markdown
### Research Parameters

**Subject**: [What we're documenting]
**Target Audience**: [Primary readers]
**Goal**: [What success looks like]
**Constraints**: [Limitations, must-haves, must-avoids]
**Sources**: [Where information came from]
```

### Insight-to-Action Linking

Every insight should connect to an actionable output:

| Research Finding                | Section It Informs             |
| ------------------------------- | ------------------------------ |
| Target audience characteristics | "Who This Is For" section      |
| Common user problems            | "Features" framing             |
| Competitor gaps                 | "Why This Project" positioning |
| User language patterns          | Terminology choices            |

### Validation Patterns

1. **SMART Check**: Is the claim Specific, Measurable, Achievable, Relevant, Time-bound?
2. **Benchmark Comparison**: Compare against industry/competitor/historical data
3. **Evidence Requirement**: Every claim needs supporting evidence
4. **Run The Code**: Test installation instructions, run examples

---

## 4. Reusable Phrases

### Introductions

- "This helps you [action] by [method] resulting in [outcome]."
- "Bottom Line: [One-line verdict]"
- "For every $1 spent, generated $[X] in return."

### Transitions

- "Detailed analysis available in appendix"
- "Full documentation upon request"
- "See also: [Related Topic]"

### Metric Presentation

- "We achieved [X], [Y%] above/below target, indicating [interpretation]"
- "Our [X] outperformed the industry average of [Y], suggesting [conclusion]"
- "For directional comparison, not absolute measurement"

### Conclusions

- "**Assessment**: [Verdict]"
- "**Recommendation**: [Specific action]"
- "Thank you for [partnership/reading]. Questions? [Contact method]"

### Humanising Phrases

- "We love your [positive attribute]! These are guidelines, not scripts."
- "If this isn't for you, check out [alternative] instead."
- "Don't hesitate to reach out with questions."
- "My door is always open."

### Warning/Caveat Phrases

- "Use for directional comparison, not absolute measurement."
- "Things that would [cause damage/break this]:"
- "What NOT to do:"

---

## 5. Anti-Patterns to Avoid

### Writing Anti-Patterns

| Don't                         | Why                   | Do Instead                              |
| ----------------------------- | --------------------- | --------------------------------------- |
| Wall of text                  | Readers skim          | Use headers, bullets, tables            |
| Passive voice                 | Distances reader      | Direct address with "you"               |
| Hedging language              | Undermines confidence | State with appropriate confidence level |
| Corporate-speak               | Feels inhuman         | Conversational but professional         |
| Features without benefits     | No motivation         | Feature + why it matters                |
| Requirements without examples | Hard to understand    | Show, don't just tell                   |
| Overclaiming                  | Destroys trust        | Be honest, flag limitations             |

### Structural Anti-Patterns

| Don't                   | Why                     | Do Instead                           |
| ----------------------- | ----------------------- | ------------------------------------ |
| Overuse of emoji        | Looks unprofessional    | Sparingly, with consistent meaning   |
| Missing contact/support | Users get stuck         | Always include support path          |
| No worked example       | Abstract stays abstract | At least one complete example        |
| Buried important info   | Readers miss it         | Lead with the lede                   |
| Single methodology bias | Incomplete picture      | Multiple approaches where applicable |

### Research Anti-Patterns

| Don't                | Why                       | Do Instead                       |
| -------------------- | ------------------------- | -------------------------------- |
| Assuming user needs  | Often wrong               | Validate with research           |
| Skipping testing     | Instructions may not work | Run the code yourself            |
| Generic descriptions | Don't resonate            | Specific, concrete examples      |
| Ignoring failures    | Misses learning           | Analyse both success and failure |

---

## 6. Quick Reference Checklist

Before finalising any documentation:

- [ ] Single sentence value proposition at top
- [ ] "When to Use" section with specific triggers
- [ ] Features have benefits, not just descriptions
- [ ] At least one complete worked example
- [ ] Tables for any multi-dimensional data
- [ ] Do's paired with Don'ts
- [ ] Metrics have context (target, benchmark)
- [ ] Clear next steps / call to action
- [ ] Support/contact information included
- [ ] Related resources linked
- [ ] Tested: installation works, examples run

---

## Attribution

Synthesised from 18 SKILL.md files:

- Insight: audience-analyzer, trend-spotter, niche-researcher
- Map: influencer-discovery, fit-scorer, competitor-tracker
- Plan: campaign-planner, brief-generator, budget-optimizer
- Activate: outreach-manager, content-reviewer, contract-helper
- Convert: content-amplifier, ugc-repurposer, landing-optimizer
- Track: performance-analyzer, roi-calculator, report-generator

Source: [influencer-marketing-claude-skills](https://github.com/anthropics/influencer-marketing-claude-skills)
