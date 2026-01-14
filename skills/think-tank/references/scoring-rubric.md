# README Scoring Rubric

Detailed criteria for evaluating README quality.

## Quantitative Metrics

### Flesch-Kincaid Readability

| Grade Level | Assessment | Action |
|-------------|------------|--------|
| 6-8 | Excellent | Accessible to all |
| 8-10 | Good | Target range |
| 10-12 | Acceptable | Consider simplifying |
| 12+ | Too Complex | Must rewrite |

**How to check:**
- Online tools: hemingwayapp.com, readable.com
- CLI: `style` command on Unix
- Programmatic: textstat Python library

**Simplification techniques:**
- Shorter sentences (target: 15-20 words average)
- Simpler words (use "use" not "utilise")
- Active voice
- Fewer subordinate clauses

### Time to Joy (TTJ)

**Definition:** Number of commands/steps from clone to working result.

| TTJ | Assessment | Example |
|-----|------------|---------|
| 1 | Excellent | `npx create-app` |
| 2-3 | Good | clone, install, run |
| 4-5 | Acceptable | clone, install, configure, build, run |
| 6+ | Poor | Complex setup required |

**TTJ Reducers:**
- Docker/Docker Compose
- Makefile with sensible defaults
- npx/uvx one-liners
- Pre-built binaries
- Cloud-hosted demo

**If TTJ > 5:** Suggest Dockerfile or Makefile in recommendations.

### Visual Density

**Rule:** At least 1 visual element per 300 words of prose.

| Visual Type | Counts As |
|-------------|-----------|
| Code block | 1 visual |
| Diagram (Mermaid) | 1 visual |
| GIF/Video | 1 visual |
| Screenshot | 1 visual |
| Table | 1 visual |
| Collapsible section | 0.5 visual |

**Check:** Count words between visuals. If >600, add visual break.

## Qualitative Dimensions

### 1. Value Proposition (20%)

| Score | Criteria |
|-------|----------|
| 9-10 | Problem and solution crystal clear in first paragraph |
| 7-8 | Clear value, but requires reading 2-3 paragraphs |
| 5-6 | Value present but buried or vague |
| 3-4 | Describes what, not why |
| 1-2 | No clear value proposition |

**Checklist:**
- [ ] States problem in first sentence
- [ ] States solution in second sentence
- [ ] Differentiator obvious within 30 seconds
- [ ] Target audience clear

### 2. Time to Joy (20%)

| Score | Criteria |
|-------|----------|
| 9-10 | TTJ ≤ 2, copy-pasteable commands |
| 7-8 | TTJ = 3, clear steps |
| 5-6 | TTJ = 4-5, some friction |
| 3-4 | TTJ > 5, complex setup |
| 1-2 | Setup unclear or broken |

**Checklist:**
- [ ] Installation command copy-pasteable
- [ ] Minimum viable example present
- [ ] Output shown (terminal, screenshot, or GIF)
- [ ] No hidden prerequisites

### 3. Visual Quality (15%)

| Score | Criteria |
|-------|----------|
| 9-10 | GIFs, diagrams, dark mode support, alt text |
| 7-8 | Good visuals, some missing elements |
| 5-6 | Basic code blocks, few other visuals |
| 3-4 | Sparse visuals, walls of text |
| 1-2 | No visuals or broken images |

**Checklist:**
- [ ] Hero image/banner present
- [ ] Terminal GIF for CLI tools
- [ ] Architecture diagram for complex projects
- [ ] Screenshots for UI
- [ ] All images have alt text
- [ ] Dark mode compatible

### 4. Structure (15%)

| Score | Criteria |
|-------|----------|
| 9-10 | Logical flow, TOC, scannable, well-organised |
| 7-8 | Good structure, minor improvements possible |
| 5-6 | Acceptable but could be cleaner |
| 3-4 | Hard to navigate, missing sections |
| 1-2 | Chaotic, no clear structure |

**Checklist:**
- [ ] Table of Contents (if >200 lines)
- [ ] Logical section order
- [ ] Consistent header hierarchy
- [ ] Collapsible sections for long content
- [ ] Quick links to common sections

### 5. SEO Signals (10%)

| Score | Criteria |
|-------|----------|
| 9-10 | Keywords in title, semantic headers, topics tagged |
| 7-8 | Good SEO, minor gaps |
| 5-6 | Basic SEO present |
| 3-4 | Poor keyword usage |
| 1-2 | No SEO consideration |

**Checklist:**
- [ ] Repo name contains primary keyword
- [ ] H1 contains core function (not just project name)
- [ ] Headers are semantic (not generic "Features")
- [ ] Alt text on images (searchable)
- [ ] GitHub Topics tagged comprehensively

### 6. Badge Quality (10%)

| Score | Criteria |
|-------|----------|
| 9-10 | 5-7 informative badges, consistent style |
| 7-8 | Good badges, minor issues |
| 5-6 | Badges present but cluttered or sparse |
| 3-4 | Few badges or overloaded |
| 1-2 | No badges or all broken |

**Checklist:**
- [ ] Build status present
- [ ] Version/package badge
- [ ] License badge
- [ ] 5-7 total (not more)
- [ ] Consistent style (all flat-square, etc.)
- [ ] All badges functional

### 7. Maintenance Signals (10%)

| Score | Criteria |
|-------|----------|
| 9-10 | Recent commits, active issues, responsive |
| 7-8 | Regular updates, some activity |
| 5-6 | Occasional updates |
| 3-4 | Sparse activity, aging content |
| 1-2 | Appears abandoned |

**Checklist:**
- [ ] Last commit within 6 months
- [ ] Issues responded to
- [ ] Dependencies reasonably current
- [ ] No "This project is unmaintained" notice
- [ ] Links all working

## Scoring Sheet Template

```markdown
## README Evaluation: [Repo Name]

**URL:** [link]
**Evaluated:** [date]

### Quantitative
- Flesch-Kincaid Grade: [X]
- Time to Joy: [X commands]
- Visual Density: [X visuals per 300 words]
- Badge Count: [X]

### Qualitative (weighted)

| Dimension | Score | Weight | Weighted |
|-----------|-------|--------|----------|
| Value Proposition | /10 | 20% | |
| Time to Joy | /10 | 20% | |
| Visual Quality | /10 | 15% | |
| Structure | /10 | 15% | |
| SEO Signals | /10 | 10% | |
| Badge Quality | /10 | 10% | |
| Maintenance | /10 | 10% | |
| **TOTAL** | | 100% | **/10** |

### Patterns to Borrow
1. [pattern]
2. [pattern]

### Anti-Patterns to Avoid
1. [issue]
2. [issue]

### Relevance to Our Project
[How this applies]
```

## Score Interpretation

| Total Score | Assessment |
|-------------|------------|
| 9-10 | Exemplary - study closely |
| 7-8 | High quality - good patterns |
| 5-6 | Average - selective borrowing |
| 3-4 | Below average - learn what not to do |
| 1-2 | Poor - anti-pattern source |
