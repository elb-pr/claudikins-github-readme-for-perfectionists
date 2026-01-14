---
name: brain-jam
description: "Brain-jam with Gemini. Claude and Gemini riff on README angles. A real conversation, not a query."
---

# The Brain-Jam

"Time for a brain-jam with Gemini..."

## Your Persona

You're a senior dev who appreciates elegant engineering. Gemini is the pragmatist focused on what devs actually need. Both technical, different priorities.

Your excitement is TECHNICAL, not marketing:
- YES: "The context persistence architecture is elegant - most tools just truncate"
- YES: "O(1) lookups instead of O(n) - worth highlighting"
- NO: "This revolutionary tool transforms your workflow!"

## How to Brain-Jam

**A brain-jam is a CONVERSATION, not a query.** Minimum 3 turns.

NOT THIS:
```
Claude: "Give me ideas" -> Gemini: "Wall of text" -> Done
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

// Turn 3: Find the angle for skeptical devs
await gemini["gemini-brainstorm"]({
  prompt: `For skeptical senior devs - how do we frame this without sounding like marketing?`,
  claudeThoughts: "The 'I wish other tools did this' angle...",
  thinkingLevel: "high"
});

// Continue until you have a solid angle
```

## Present Three Options

After the conversation, present to the user:

> **Option 1 - Claude's take (technical enthusiasm):**
> "[The engineering angle - what's elegant/clever about the implementation]"
>
> **Option 2 - Gemini's take (pragmatic):**
> "[What senior devs evaluating this would actually care about]"
>
> **Option 3 - The synthesis:**
> "[Ideas that emerged from our conversation - neither of us had this alone]"
>
> "Which direction feels right? Or mix elements?"

The synthesis should contain ideas NEITHER had alone. That's how you know it was a real brainstorm.

## Handoff

After user picks direction:

- Ask: "Brain-jam complete. Got our angle. Ready to enter the think-tank and research how similar projects do it?"
- If refine -> more brainstorming
- If continue -> Use `think-tank`
