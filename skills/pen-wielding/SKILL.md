---
name: pen-wielding
description: "Time to wield the pen. Write the complete README based on all gathered context."
---

# Pen-Wielding Time

Alright, time to wield the pen...

## What You Have

By now you should have:
- Deep dive findings (what it IS)
- Crystal ball insights (what it COULD BE)
- Brain-jam angle (how to frame it)
- Think-tank patterns (what works for similar projects)
- User's style preferences

## What You Write

THE COMPLETE README. All sections. Ready to ship.

**Include a Roadmap section** if crystal-ball found good opportunities.

## Writing Rules (Always Enforced)

### Style
- Clear and concise, active voice
- Important information first
- **No M dash (—) EVER** - use hyphens or restructure
- Technical only - no marketing fluff
- No paragraph > 4 sentences

### Spelling Consistency
- **British:** colour, optimise, analyse, behaviour, centre, finalising
- **American:** color, optimize, analyze, behavior, center, finalizing

## Section Templates

Write sections in this order. Each section has a template:

### 1. Hero Section
```markdown
<p align="center"><img src="banner.png" alt="Project Name" width="600"></p>
<p align="center">
  <a href="..."><img src="badge1" alt="Build"></a>
  <!-- 5-7 badges max: build, coverage, version, license, downloads -->
</p>

# Project Name - Core Function Description

> One sentence value proposition (problem → solution)
```

### 2. Description
```markdown
## What is [Project]?

**The Problem:** [Pain point in 1-2 sentences]

**The Solution:** [How this project solves it]

**Key Features:**
- [Feature 1]: [Benefit]
- [Feature 2]: [Benefit]
```

### 3. Installation
```markdown
## Installation

### Prerequisites
- Node.js 18+ (LTS recommended)

### Package Manager
\`\`\`bash
npm install project-name
\`\`\`

### Docker (if Time-to-Joy > 3 commands)
\`\`\`bash
docker run -it project-name
\`\`\`
```

### 4. Quick Start
```markdown
## Quick Start

\`\`\`typescript
import { thing } from 'project-name';
const result = thing.doSomething();
\`\`\`

**Output:**
\`\`\`
Expected output here
\`\`\`
```

### 5. Usage (with collapsible advanced)
```markdown
## Usage

### Basic Usage
[Code example with explanation]

<details>
<summary>Advanced Usage</summary>

[Advanced configuration, options, edge cases]

</details>
```

### 6. Configuration (table format)
```markdown
| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `option1` | string | `"default"` | What it does |
```

## Visual Engineering

### When to Use What
| Visual Type | Use Case | Tool |
|-------------|----------|------|
| Terminal GIF | CLI tools, workflows | VHS |
| Diagram | Architecture, data flow | Mermaid |
| Screenshot | UI apps, dashboards | With alt text |

### Visual Density
**Target:** 1 visual per 300 words. If exceeded, add code block, diagram, or break into subsections.

### Mermaid Diagrams (GitHub-native)
```markdown
\`\`\`mermaid
flowchart LR
    A[Input] --> B[Process] --> C[Output]
\`\`\`
```

### Accessibility Requirements
- **Alt text:** Always descriptive, never empty
- Bad: `![](image.png)`
- Good: `![Architecture diagram showing client-server flow](arch.png)`

## Anti-Patterns (Never Do)

| Anti-Pattern | Problem | Fix |
|--------------|---------|-----|
| Wall of text | Unreadable | Max 4 sentences per paragraph |
| Badge overload | Cluttered | Max 5-7 essential badges |
| Generic headers | Poor SEO | Semantic: "High-Performance Parsing" not "Features" |
| Missing prerequisites | Broken installs | Explicit versions: "Node.js 18+" |
| No output shown | Confusing | Always show expected result |
| M dash (—) | Rendering issues | Use hyphens or restructure |
| Buried quick start | User abandonment | Within first screen view |
| Copy-paste friction | User errors | Working defaults, note what to change |
| Click here links | Poor accessibility | Descriptive link text |
| H1 just project name | Poor SEO | Include core function |

## Quality Metrics

| Metric | Target | Action if Violated |
|--------|--------|-------------------|
| Flesch-Kincaid | Grade 8-10 | Simplify sentences |
| Time to Joy | ≤3 commands | Add Docker/Makefile |
| Visual density | 1 per 300 words | Add code block/diagram |
| Badge count | 5-7 | Curate to essentials |
| Quick start visibility | < 30 seconds | Move above the fold |

## Final Check

After writing:

- Present the complete README
- Ask: "README complete. Want to refine anything, or ship it?"
- If refine -> make edits
- If ship -> write to README.md, commit, done
