# Style Options Reference

Detailed examples of each tone option for README writing.

## Tone: Minimal

**Characteristics:**
- Bare essentials only
- No explanation of "why"
- Assumes technical competence
- Fastest time to usage

**Example Installation Section:**
```markdown
## Installation

```bash
npm install my-tool
```

## Usage

```bash
my-tool --input file.txt --output result.json
```
```

**Best for:** CLI utilities, developer tools, libraries with obvious purpose.

---

## Tone: Conversational

**Characteristics:**
- Friendly but professional
- Explains the "why" not just the "how"
- Anticipates questions
- Welcoming to newcomers

**Example Installation Section:**
```markdown
## Installation

Getting started is straightforward. Install via npm:

```bash
npm install my-tool
```

This adds `my-tool` to your project's dependencies. If you prefer a global install (available anywhere on your system), add the `-g` flag.

## Usage

The simplest way to use my-tool is with an input file:

```bash
my-tool --input file.txt --output result.json
```

This reads `file.txt`, processes it, and writes the result to `result.json`. If you omit `--output`, results print to stdout.
```

**Best for:** Projects targeting mixed skill levels, educational tools, community projects.

---

## Tone: Opinionated

**Characteristics:**
- Has personality and voice
- States positions clearly
- May include philosophy/rationale
- Your project, your voice

**Example Installation Section:**
```markdown
## Installation

```bash
npm install my-tool
```

We deliberately keep dependencies minimal. No bloat, no surprises.

## Usage

```bash
my-tool --input file.txt --output result.json
```

We chose explicit flags over positional arguments. Yes, it's more typing. But six months from now when you read your scripts, you'll thank us.

### Why Not YAML?

We use JSON. YAML's implicit typing has burned us too many times. `no` becoming `false`? Not in our house.
```

**Best for:** Projects with strong design philosophy, tools by experienced developers, projects that want to stand out.

---

## Tone: Reference

**Characteristics:**
- Comprehensive documentation
- Every flag, option, edge case
- Structured for searchability
- May include tables, detailed API docs

**Example Installation Section:**
```markdown
## Installation

### Requirements

| Dependency | Version | Notes |
|------------|---------|-------|
| Node.js | ≥18.0.0 | LTS recommended |
| npm | ≥9.0.0 | Comes with Node.js |

### Package Managers

**npm:**
```bash
npm install my-tool
```

**yarn:**
```bash
yarn add my-tool
```

**pnpm:**
```bash
pnpm add my-tool
```

### Global Installation

```bash
npm install -g my-tool
```

**Note:** Global installation requires appropriate permissions. On Unix systems, you may need `sudo` or configure npm's prefix.

## Usage

### Command Line Interface

```
my-tool [options] [command]
```

### Options

| Flag | Alias | Type | Default | Description |
|------|-------|------|---------|-------------|
| `--input` | `-i` | string | stdin | Input file path |
| `--output` | `-o` | string | stdout | Output file path |
| `--format` | `-f` | enum | json | Output format: json, yaml, csv |
| `--verbose` | `-v` | boolean | false | Enable verbose logging |
| `--quiet` | `-q` | boolean | false | Suppress all output except errors |
| `--version` | | boolean | | Print version and exit |
| `--help` | `-h` | boolean | | Print help and exit |

### Examples

**Basic usage:**
```bash
my-tool --input file.txt --output result.json
```

**Multiple input files:**
```bash
my-tool --input file1.txt --input file2.txt --output combined.json
```

**Pipe from stdin:**
```bash
cat file.txt | my-tool --output result.json
```

**Output to stdout:**
```bash
my-tool --input file.txt
```
```

**Best for:** Libraries, APIs, complex tools, enterprise software, projects with many options.

---

## Spelling Differences Quick Reference

| British | American |
|---------|----------|
| colour | color |
| optimise | optimize |
| analyse | analyze |
| behaviour | behavior |
| centre | center |
| licence (noun) | license |
| organisation | organization |
| recognise | recognize |
| summarise | summarize |
| customise | customize |

## The M Dash Rule

**NEVER use the M dash (—).**

Instead:
- Use hyphens for compound words: `real-time`, `open-source`
- Use parentheses for asides: `The tool (which is fast) works well`
- Restructure sentences: "The tool is fast. It works well."
- Use colons for elaboration: `One benefit: speed`

**Wrong:** `The tool—which is fast—works well`
**Right:** `The tool (which is fast) works well`
