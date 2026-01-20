---
name: think-tank
description: "Use when researching documentation patterns after brain-jam phase. Analyses exemplar READMEs from similar high-star repositories, scores against rubric, extracts patterns."
---

# The Think-Tank

**Goal:** Extract high-converting patterns from similar tools and identify "Anti-Patterns" to avoid.

## Step 1: Load Research Standards

Read the governance files:

1. `references/scoring-rubric.md` (How to grade quality).
2. `references/badge-ecosystem.md` (Which badges signal what).
3. `references/gemini-deep-research.md` (How to execute Gemini deep research).

---

## Step 2: Define Search Criteria

Based on project context from codebase analysis, match on:

| Criterion  | How to Match                                           |
| ---------- | ------------------------------------------------------ |
| Category   | Same project type (CLI, library, framework, API, etc.) |
| Tech Stack | Same or similar languages/frameworks                   |
| Ecosystem  | Same package manager (npm, PyPI, Cargo)                |
| Complexity | Similar scope (simple util vs enterprise tool)         |
| Maturity   | Established projects with proven documentation         |

**Search queries:**

```
"best [project-type] [tech-stack] github"
"awesome [technology] list"
"[similar-tool] alternatives github"
```

Find 10-15 candidates, then narrow to top 5-7 based on stars and initial quality scan.

---

## Step 2.5: Validation Methodology

Before accepting research findings, validate them.

### Pre-Writing Research Phases

| Phase                          | Activities                           | Output            |
| ------------------------------ | ------------------------------------ | ----------------- |
| **Define Scope**               | Establish parameters before research | Parameter block   |
| **Gather Context**             | Structured information capture       | Context template  |
| **Multi-Source Triangulation** | Check multiple sources               | Source comparison |
| **Validation**                 | Test claims, run examples            | Evidence notes    |

### Validation Patterns

1. **SMART Check:** Is the claim Specific, Measurable, Achievable, Relevant, Time-bound?
2. **Benchmark Comparison:** Compare against industry/competitor/historical data
3. **Evidence Requirement:** Every claim needs supporting evidence
4. **Run The Code:** Test installation instructions, run examples yourself

### Insight-to-Action Linking

Every research finding should connect to a README section:

| Research Finding                | Section It Informs             |
| ------------------------------- | ------------------------------ |
| Target audience characteristics | "Who This Is For" section      |
| Common user problems            | "Features" framing             |
| Competitor gaps                 | "Why This Project" positioning |
| User language patterns          | Terminology choices            |
| Installation friction points    | Quick Start optimisation       |

---

## Step 3: Score Each README

Rate each README 1-10 on these dimensions:

| Dimension           | Weight | What to Look For                                      |
| ------------------- | ------ | ----------------------------------------------------- |
| Value Proposition   | 20%    | Problem and solution crystal clear in first paragraph |
| Time to Joy (TTJ)   | 20%    | Commands to first working result (target: 2-3)        |
| Visual Quality      | 15%    | GIFs, diagrams, code blocks, dark mode support        |
| Structure           | 15%    | Logical flow, scannable, TOC if >200 lines            |
| SEO Signals         | 10%    | Keywords in title, semantic headers, topics tagged    |
| Badge Quality       | 10%    | Informative badges, 5-7 max, consistent style         |
| Maintenance Signals | 10%    | Recent commits, active issues, working links          |

### Quantitative Targets

| Metric                   | Good            | Red Flag                  |
| ------------------------ | --------------- | ------------------------- |
| Flesch-Kincaid Grade     | 8-10            | >12 (too complex)         |
| TTJ (commands to result) | 2-3             | >5                        |
| Visual Density           | 1 per 300 words | >600 words without visual |
| Badge Count              | 5-7             | >10 or 0                  |

### The "Slop" Penalty

**CRITICAL:** Scan the text for the "Delve Index" (Delve, Seamless, Tapestry, Unleash, Landscape).

- **Action:** If _any_ appear in the Description/Intro, **DEDUCT 2 POINTS**.
- _Rationale:_ We do not want to mimic popular-but-lazy documentation.

### Score Interpretation

| Score | Assessment                           |
| ----- | ------------------------------------ |
| 9-10  | Exemplary - study closely            |
| 7-8   | High quality - good patterns         |
| 5-6   | Average - selective borrowing        |
| 3-4   | Below average - learn what not to do |

---

## Step 4: Pattern Extraction

For each high-scoring exemplar, extract:

**Hero Section:**

- Banner/logo style
- Tagline approach
- Badge selection and arrangement

**Structure:**

- Section order and naming conventions
- Use of collapsible sections
- Table of Contents style

**Visuals:**

- GIF usage (terminal recordings, UI demos)
- Diagram types (architecture, flow)
- Screenshot placement

**Writing Style:**

- Tone (minimal, conversational, opinionated, reference)
- Code example density
- Explanation depth

---

## Step 5: Badge Recommendations

### Badge Categories by Signal

| Category      | Signal                           | When to Use                           |
| ------------- | -------------------------------- | ------------------------------------- |
| Build Status  | "Code compiles and tests pass"   | Always                                |
| Code Coverage | "Maintainers care about testing" | If coverage >60%                      |
| Version       | "This is a releasable product"   | If published to registry              |
| Social Proof  | "Crowd has vetted this"          | Only if numbers impress (5000+ stars) |
| License       | "Legal to use in my project"     | Always                                |
| Activity      | "Project is alive"               | Only if actively maintained           |

### Badge Styles

Pick ONE style across all badges:

- `flat` - Modern, clean (most projects)
- `flat-square` - Sharp edges (technical projects)
- `for-the-badge` - Large, bold (hero sections only)

### Recommended Badge Sets

**Minimal (3-4):** Build Status, Version, License

**Standard (5-6):** Build Status, Coverage, Version, Downloads, License

**Comprehensive (7 max):** Build Status, Coverage, Quality, Version, Downloads, License, Last Commit

### Badge Anti-Patterns

- **Overload:** 15+ badges creating visual chaos
- **Inconsistent styling:** Mix of flat, plastic, for-the-badge
- **Vanity badges:** "Made with JavaScript" adds no value
- **Stale badges:** Coverage showing 0% from broken CI
- **Meaningless numbers:** Badging 3 stars, 12 downloads

---

## Step 6: Section Recommendations

| Section         | When to Include                            |
| --------------- | ------------------------------------------ |
| Quick Start     | Always - first thing after hero            |
| Installation    | Always - multiple methods if applicable    |
| Usage/Examples  | Always - show, don't just tell             |
| API Reference   | Libraries and frameworks                   |
| Configuration   | If configurable                            |
| Architecture    | Complex projects with multiple components  |
| Contributing    | Open source projects seeking contributions |
| FAQ             | If common questions exist                  |
| Troubleshooting | If known gotchas exist                     |

---

## Output Format

```markdown
# Think-Tank Research Results

## Summary

- **Repos Analysed:** [X]
- **High Quality (8-10):** [X]
- **Key Patterns Identified:** [X]

## Top Exemplar: [Repo Name]

- **Score:** [X]/10 (Slop Penalty: [Yes/No])
- **Why it wins:** [specific reason]
- **Steal this:** [specific pattern]

## The Blueprint (Our Plan)

### 1. Visual Strategy

- **Hero:** [e.g., Terminal GIF using VHS]
- **Architecture:** [e.g., Mermaid Graph LR]
- **Density Target:** One visual every [X] words.

### 2. Badge Selection

_(Selected from references/badge-ecosystem.md)_

- [Badge 1]: [what it signals]
- [Badge 2]: [what it signals]
- [Badge 3]: [what it signals]

### 3. Structural Flow

1. Hero & Badges
2. Description (The Hook)
3. Quick Start (Time-to-Joy)
4. ...

### 4. Anti-Patterns to Avoid

- [Thing]: Common mistake seen in lower-rated READMEs
```

## Handoff

**Ask:** "Research complete. We have the Badge list, Visual strategy, and Structural plan. Ready to wield the pen?"

- If refine -> more research
- If continue -> Use `pen-wielding`
