---
name: writing-readmes
description: README writing methodology with structural templates, visual engineering, and quality metrics. Use when writing README content, drafting documentation sections, applying style preferences, or producing high-quality technical documentation. Covers section templates, badge guidelines, SEO best practices, and anti-patterns to avoid.
---

# README Writing Methodology

Produce high-quality README sections following proven structural patterns and quality metrics.

## Input Required

Before writing, ensure you have:
- **Approved structure:** Which sections to write
- **Codebase analysis:** Project details, value prop, dependencies
- **Research findings:** Patterns to use, anti-patterns to avoid
- **Style preferences:** Spelling (British/American), tone

## Writing Rules (Always Enforced)

### Style
- Clear and concise
- Active voice
- Important information first
- **No M dash (—) EVER** - use hyphens or restructure
- Technical only - no marketing fluff

### Spelling Consistency
- **British:** colour, optimise, analyse, behaviour, centre
- **American:** color, optimize, analyze, behavior, center

## Section Order

Write sections in this order:

1. **Hero Section** - Banner, badges (5-7 max), tagline
2. **Description** - Problem, solution, key features
3. **Table of Contents** - If README > 200 lines
4. **Installation** - Prerequisites, package manager, source, Docker
5. **Quick Start** - Minimum viable example with output
6. **Usage** - Basic and advanced (collapsible)
7. **Configuration** - Options table if applicable
8. **Contributing** - Link to CONTRIBUTING.md, dev setup
9. **License** - Link to LICENSE file

See `references/structural-templates.md` for complete templates.

## Quality Metrics

Check every section against:

| Metric | Target | Action if Violated |
|--------|--------|-------------------|
| Flesch-Kincaid | Grade 8-10 | Simplify sentences |
| Time to Joy | ≤3 commands | Add Docker/Makefile |
| Visual density | 1 per 300 words | Add code block/diagram |
| Badge count | 5-7 | Curate to essentials |

## Visual Engineering

### When to Use What

| Visual Type | Use Case | Tool |
|-------------|----------|------|
| Terminal GIF | CLI tools, workflows | VHS |
| Diagram | Architecture, data flow | Mermaid |
| Screenshot | UI apps, dashboards | With alt text |

See `references/visual-engineering.md` for detailed guidance.

## Anti-Patterns (Never Do)

| Anti-Pattern | Instead |
|--------------|---------|
| Wall of text | Headers, bullets, code blocks |
| Badge overload | Max 5-7, curate |
| Generic headers | Semantic, searchable |
| Missing prerequisites | Explicit versions |
| No output shown | Always show expected result |
| M dash (—) | Hyphens or restructure |

See `references/anti-patterns.md` for complete list.

## Output Process

1. Write ONE section at a time
2. Target 200-300 words per section
3. Present for review before next section
4. Incorporate feedback immediately
5. Return as Markdown text

## Additional Resources

- `references/structural-templates.md` - Complete section templates
- `references/visual-engineering.md` - GIF, diagram, screenshot guidance
- `references/anti-patterns.md` - Detailed patterns to avoid
