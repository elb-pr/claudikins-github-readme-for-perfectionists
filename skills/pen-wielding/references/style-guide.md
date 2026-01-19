# The Anti-Slop Style Guide

**Goal:** Pass the "Turing Test of Developer Scrutiny."

**Voice:** Senior Engineer. Cynical, precise, allergic to marketing.

## 1. The Anti-Cliché Lexicon (BANNED WORDS)

You are strictly FORBIDDEN from using these tokens. If the LLM predicts them, stop and rewrite.

| Banned Word      | The Signal                       | Replacement                         |
| ---------------- | -------------------------------- | ----------------------------------- |
| **Delve**        | "I don't know the specifics."    | Analyze, Investigate, Query, Check  |
| **Tapestry**     | "I am writing creative fiction." | Network, Stack, System, Graph       |
| **Seamless**     | "I am lying about complexity."   | Compatible, Integrated, Automated   |
| **Unleash**      | "I am a marketing bot."          | Execute, Run, Enable, Start         |
| **Elevate**      | "Corporate padding."             | Improve, Optimize (must add metric) |
| **Landscape**    | "Zero information density."      | _Delete the sentence_               |
| **Testament**    | "Grandeur unearned."             | Proof, Demonstration, Example       |
| **Foster**       | "HR Handbook."                   | Encourage, Allow, Enable            |
| **Spearhead**    | "1990s Management."              | Lead, Direct, First to implement    |
| **Game-changer** | "Hyperbole."                     | Solves [specific problem]           |
| **Robust**       | "Vague filler."                  | Fault-tolerant, Atomic, Idempotent  |
| **Navigating**   | "Corporate waffle."              | Using, Working with, Handling       |
| **Leverage**     | "MBA speak."                     | Use, Apply, Employ                  |
| **Cutting-edge** | "Meaningless hyperbole."         | Modern, Current, 2025-compatible    |
| **Empower**      | "Marketing fluff."               | Allow, Enable, Let                  |

## 2. Sentence Structure Patterns

You MUST vary sentence structure using these three specific patterns.

### Pattern A: "The Hook" (Empathy + Authority)

**Use in:** Description, Intro.

- **Structure:** [Short Sentence stating Pain]. [Short Sentence stating Solution].
- _Bad:_ "This library helps with JSON parsing issues."
- _Good:_ "JSON logs are unreadable. Kinesis parses them instantly."

### Pattern B: "The Hammer" (Fact + Metric)

**Use in:** Features, Performance.

- **Structure:** [Subject] + [Verb] + [Object] + [Metric]. (No adjectives).
- _Bad:_ "The system is designed to be incredibly fast."
- _Good:_ "Builds finish in under 200ms."

### Pattern C: "The Trust Builder" (Constraint + Fallback)

**Use in:** Usage, Technical Deep Dive.

- **Structure:** [Constraint] + [Fallback/Explanation].
- _Bad:_ "Works perfectly on all platforms."
- _Good:_ "Uses `epoll` on Linux; falls back to `kqueue` on macOS."

## 3. Spelling Consistency

Pick ONE and stick to it throughout:

| British    | American   |
| ---------- | ---------- |
| colour     | color      |
| optimise   | optimize   |
| analyse    | analyze    |
| behaviour  | behavior   |
| centre     | center     |
| finalising | finalizing |

## 4. Formatting Rules

- **No M-Dashes (—):** Use hyphens (-) or colons (:).
- **No Wall of Text:** Max 4 sentences per paragraph.
- **Visual Density:** Every 300 words MUST have a code block, diagram, or image

## 5. Quality Metrics

| Metric                 | Target          | Action if Violated     |
| ---------------------- | --------------- | ---------------------- |
| Flesch-Kincaid         | Grade 8-10      | Simplify sentences     |
| Time to Joy            | ≤3 commands     | Add Docker/Makefile    |
| Visual density         | 1 per 300 words | Add code block/diagram |
| Badge count            | 5-7             | Curate to essentials   |
| Quick start visibility | < 30 seconds    | Move above the fold    |

## 6. Humanisation Patterns

Write TO readers, not AT them. These patterns build trust and engagement.

### Tone & Voice

| Pattern                      | Description                                        | Example                                                   |
| ---------------------------- | -------------------------------------------------- | --------------------------------------------------------- |
| **Human-first address**      | Use "you" directly, speak TO the reader            | "This helps you..." not "This system enables users to..." |
| **Conversational warmth**    | Casual but professional, no corporate-speak        | "We love your creative voice!"                            |
| **Action-oriented language** | Active verbs, direct commands                      | "Design", "Create", "Plan" not "The system will..."       |
| **Empowering assumptions**   | Assume reader competence while providing structure | Tips not mandates                                         |

### Confidence Framing

| Pattern                        | Description                                   | Example                                         |
| ------------------------------ | --------------------------------------------- | ----------------------------------------------- | ----------------- |
| **Explicit confidence levels** | Use High/Med/Low ratings alongside claims     | `Claim: X                                       | Confidence: High` |
| **Tiered urgency**             | Must/Should/Nice-to-Have classifications      | "Must Fix" > "Should Fix" > "Nice to Have"      |
| **Assessment verdicts**        | End calculations with human-readable verdicts | "**Assessment**: Profitable"                    |
| **Caveat callouts**            | Flag limitations with warning symbols         | `Warning: Use for directional comparison only.` |

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

## 7. Reusable Phrase Templates

Pre-tested phrases for common documentation needs.

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

### Warning/Caveat Phrases

- "Use for directional comparison, not absolute measurement."
- "Things that would [cause damage/break this]:"
- "What NOT to do:"
