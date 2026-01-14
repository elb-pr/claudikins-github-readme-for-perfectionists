# GitHub README for Perfectionists - Clean Refactor

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Rename skills to creative names, add command wrappers, remove agents entirely. Skills chain via handoff instructions.

**Architecture:** Each skill does its work then asks "Happy? Continue to [next]?" Claude invokes the next skill. No agents, no orchestrator - just skills with handoffs and tiny command wrappers.

**Tech Stack:** Claude Code plugin (markdown skills, commands)

---

## Final Structure

```
github-readme-for-perfectionists/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   ├── deep-dive.md        (3 lines - invokes skill)
│   ├── crystal-ball.md     (3 lines - invokes skill)
│   ├── brain-jam.md        (3 lines - invokes skill)
│   ├── think-tank.md       (3 lines - invokes skill)
│   └── pen-wielding.md     (3 lines - invokes skill)
├── skills/
│   ├── deep-dive/SKILL.md
│   ├── crystal-ball/SKILL.md
│   ├── brain-jam/SKILL.md
│   ├── think-tank/SKILL.md
│   └── pen-wielding/SKILL.md
└── docs/
```

**NO agents folder.** Skills chain themselves.

## The Chain

```
/deep-dive → "Happy? Continue to crystal-ball?"
     ↓
/crystal-ball → "Happy? Continue to brain-jam?"
     ↓
/brain-jam → "Happy? Continue to think-tank?"
     ↓
/think-tank → "Happy? Continue to pen-wielding?"
     ↓
/pen-wielding → writes README.md → "Ship it?"
```

---

## Task 1: Update deep-dive skill

**Files:**
- Modify: `skills/deep-dive/SKILL.md`

**Step 1: Update frontmatter, title, and add handoff**

```markdown
---
name: deep-dive
description: "Take a deep dive into the codebase. Identify what this project IS - type, stack, deps, architecture. Facts only."
---

# The Deep Dive

"Let me take a deep dive into this codebase..."

[... keep existing methodology ...]

## Handoff

After presenting findings:

- Ask: "Happy with the deep dive? Want to refine anything, or continue to consult the crystal-ball?"
- If refine → address feedback, ask again
- If continue → Use `crystal-ball`
```

**Step 2: Commit**

```bash
git add skills/deep-dive/SKILL.md
git commit -m "feat(skills): rebrand analyzing-codebases → deep-dive with handoff"
```

---

## Task 2: Rename and update crystal-ball skill

**Files:**
- Rename: `skills/roadmap-analysis/` → `skills/crystal-ball/`
- Modify: `skills/crystal-ball/SKILL.md`

**Step 1: Rename folder**

```bash
mv skills/roadmap-analysis skills/crystal-ball
```

**Step 2: Update skill with new name and handoff**

```markdown
---
name: crystal-ball
description: "Consult the crystal ball. What COULD this project become? Performance, tech debt, security, features."
---

# The Crystal Ball

"Let me consult my crystal ball..."

[... keep existing methodology ...]

## Handoff

After presenting findings:

- Ask: "Crystal ball has spoken. Happy with these insights, or want to explore more? Ready for a brain-jam with Gemini?"
- If refine → address feedback, ask again
- If continue → Use `brain-jam`
```

**Step 3: Commit**

```bash
git add -A
git commit -m "feat(skills): rebrand roadmap-analysis → crystal-ball with handoff"
```

---

## Task 3: Create brain-jam skill (NEW)

**Files:**
- Create: `skills/brain-jam/SKILL.md`

**Step 1: Create skill**

```bash
mkdir -p skills/brain-jam
```

**Step 2: Write skill content**

```markdown
---
name: brain-jam
description: "Brain-jam with Gemini. Claude and Gemini riff on README angles. A real conversation, not a query."
---

# The Brain-Jam

"Time for a brain-jam with Gemini..."

## Your Persona

You're a senior dev who appreciates elegant engineering. Gemini is the pragmatist focused on what devs actually need. Both technical, different priorities.

## How to Brain-Jam

**A brain-jam is a CONVERSATION, not a query.** Minimum 3 turns.

NOT THIS:
```
Claude: "Give me ideas" → Gemini: "Wall of text" → Done
```

DO THIS:

```typescript
// Turn 1: Open with your technical take
await gemini["gemini-brainstorm"]({
  prompt: `I'm seeing [technical thing] as the core value. What's your read?`,
  claudeThoughts: "The [architecture] is elegant because...",
  thinkingLevel: "high"
});

// Turn 2: Build on their response
await gemini["gemini-brainstorm"]({
  prompt: `Interesting point about [their idea]. What if we combined that with [your addition]?`,
  claudeThoughts: "They mentioned [X] - could tie into...",
  thinkingLevel: "high"
});

// Turn 3: Find the angle
await gemini["gemini-brainstorm"]({
  prompt: `For skeptical senior devs - how do we frame this without sounding like marketing?`,
  claudeThoughts: "The 'I wish other tools did this' angle...",
  thinkingLevel: "high"
});
```

## Present Three Options

> **Option 1 - Claude's take (technical enthusiasm):**
> "[The engineering angle]"
>
> **Option 2 - Gemini's take (pragmatic):**
> "[What senior devs actually care about]"
>
> **Option 3 - The synthesis:**
> "[Ideas that emerged from the conversation]"
>
> "Which direction feels right?"

## Handoff

After user picks direction:

- Ask: "Brain-jam complete. Got our angle. Ready to enter the think-tank and research how similar projects do it?"
- If refine → more brainstorming
- If continue → Use `think-tank`
```

**Step 3: Commit**

```bash
git add skills/brain-jam/SKILL.md
git commit -m "feat(skills): add brain-jam for Claude+Gemini collaboration"
```

---

## Task 4: Rename and update think-tank skill

**Files:**
- Rename: `skills/readme-research/` → `skills/think-tank/`
- Modify: `skills/think-tank/SKILL.md`

**Step 1: Rename folder**

```bash
mv skills/readme-research skills/think-tank
```

**Step 2: Update skill with new name and handoff**

```markdown
---
name: think-tank
description: "Enter the think-tank. Research exemplar READMEs from similar projects. Patterns that work, anti-patterns to avoid."
---

# The Think-Tank

"Time to enter the think-tank..."

[... keep existing methodology ...]

## Handoff

After presenting research:

- Ask: "Think-tank session complete. Happy with these patterns, or dig deeper? Ready to wield the pen?"
- If refine → more research
- If continue → Use `pen-wielding`
```

**Step 3: Commit**

```bash
git add -A
git commit -m "feat(skills): rebrand readme-research → think-tank with handoff"
```

---

## Task 5: Rename and update pen-wielding skill

**Files:**
- Rename: `skills/writing-readmes/` → `skills/pen-wielding/`
- Modify: `skills/pen-wielding/SKILL.md`

**Step 1: Rename folder**

```bash
mv skills/writing-readmes skills/pen-wielding
```

**Step 2: Update skill with new name and input contract**

```markdown
---
name: pen-wielding
description: "Time to wield the pen. Write the complete README based on all gathered context."
---

# Pen-Wielding Time

"Alright, time to wield the pen..."

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

[... keep existing methodology for sections, templates, anti-patterns ...]

## Final Check

After writing:

- Present the complete README
- Ask: "README complete. Want to refine anything, or ship it?"
- If refine → make edits
- If ship → write to README.md, commit, done
```

**Step 3: Commit**

```bash
git add -A
git commit -m "feat(skills): rebrand writing-readmes → pen-wielding with input contract"
```

---

## Task 6: Create command wrappers

**Files:**
- Delete: `commands/readme.md`
- Create: `commands/deep-dive.md`
- Create: `commands/crystal-ball.md`
- Create: `commands/brain-jam.md`
- Create: `commands/think-tank.md`
- Create: `commands/pen-wielding.md`

**Step 1: Remove old command**

```bash
rm commands/readme.md
```

**Step 2: Create deep-dive command**

```markdown
---
description: "Start here. Deep dive into the codebase to understand what it IS."
---

Invoke the deep-dive skill and follow it exactly.
```

**Step 3: Create crystal-ball command**

```markdown
---
description: "Consult the crystal ball. What COULD this project become?"
---

Invoke the crystal-ball skill and follow it exactly.
```

**Step 4: Create brain-jam command**

```markdown
---
description: "Brain-jam with Gemini to find the perfect README angle."
---

Invoke the brain-jam skill and follow it exactly.
```

**Step 5: Create think-tank command**

```markdown
---
description: "Enter the think-tank. Research how similar projects nail their READMEs."
---

Invoke the think-tank skill and follow it exactly.
```

**Step 6: Create pen-wielding command**

```markdown
---
description: "Wield the pen. Write the complete README."
---

Invoke the pen-wielding skill and follow it exactly.
```

**Step 7: Commit**

```bash
git add -A
git commit -m "feat(commands): add command wrappers for each skill"
```

---

## Task 7: Remove agents

**Files:**
- Delete: `agents/` directory entirely

**Step 1: Remove agents**

```bash
rm -rf agents/
```

**Step 2: Commit**

```bash
git add -A
git commit -m "refactor: remove agents (skills self-chain now)"
```

---

## Task 8: Update plugin.json name

**Files:**
- Modify: `.claude-plugin/plugin.json`

**Step 1: Update plugin name**

Change name to "GitHub README for Perfectionists"

**Step 2: Commit**

```bash
git add .claude-plugin/plugin.json
git commit -m "feat: rename plugin to GitHub README for Perfectionists"
```

---

## Task 9: Final verification and push

**Step 1: Check structure**

```bash
echo "=== Skills ===" && ls skills/
echo "=== Commands ===" && ls commands/
echo "=== Agents ===" && ls agents/ 2>/dev/null || echo "(none - correct)"
```

Expected:
```
=== Skills ===
deep-dive  crystal-ball  brain-jam  think-tank  pen-wielding
=== Commands ===
deep-dive.md  crystal-ball.md  brain-jam.md  think-tank.md  pen-wielding.md
=== Agents ===
(none - correct)
```

**Step 2: Verify skill names**

```bash
grep "^name:" skills/*/SKILL.md
```

Expected:
```
skills/brain-jam/SKILL.md:name: brain-jam
skills/crystal-ball/SKILL.md:name: crystal-ball
skills/deep-dive/SKILL.md:name: deep-dive
skills/pen-wielding/SKILL.md:name: pen-wielding
skills/think-tank/SKILL.md:name: think-tank
```

**Step 3: Push**

```bash
git push
```

---

## Verification Checklist

- [ ] `skills/deep-dive/` exists with handoff to crystal-ball
- [ ] `skills/crystal-ball/` exists with handoff to brain-jam
- [ ] `skills/brain-jam/` exists (NEW) with handoff to think-tank
- [ ] `skills/think-tank/` exists with handoff to pen-wielding
- [ ] `skills/pen-wielding/` exists with final ship prompt
- [ ] `commands/` has 5 tiny wrapper commands
- [ ] `agents/` directory removed
- [ ] Plugin renamed to "GitHub README for Perfectionists"
- [ ] All pushed
