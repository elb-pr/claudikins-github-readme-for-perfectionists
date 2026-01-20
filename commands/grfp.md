---
name: claudikins-github-readme-for-perfectionists:grfp
description: Begin README creation workflow or check current progress and missed areas
argument-hint: [--status | --resume]
allowed-tools:
  - Read
  - Glob
  - Grep
  - Task
  - WebFetch
  - WebSearch
  - AskUserQuestion
  - Skill
skills:
  - grfp
---

# claudikins-github-readme-for-perfectionists:grfp Command

You are orchestrating the GitHub README For Perfectionists workflow.

## Arguments

- `--status` → Show current progress through the 5-stage workflow
- `--resume` → Continue from last completed stage
- No argument → Start fresh or show overview

## Workflow

1. Load the grfp skill for methodology
2. Guide user through the 5-stage README creation process
3. Track progress and ensure quality at each stage

## The 5 Stages

| # | Stage | Command | Purpose |
|---|-------|---------|---------|
| 1 | Deep Dive | `/claudikins-github-readme-for-perfectionists:deep-dive` | Understand what the project IS |
| 2 | Crystal Ball | `/claudikins-github-readme-for-perfectionists:crystal-ball` | Envision what it COULD become |
| 3 | Think Tank | `/claudikins-github-readme-for-perfectionists:think-tank` | Research exemplar READMEs |
| 4 | Brain Jam | `/claudikins-github-readme-for-perfectionists:brain-jam` | Collaborate with Gemini on angle |
| 5 | Pen Wielding | `/claudikins-github-readme-for-perfectionists:pen-wielding` | Write the final README |

## Philosophy

> "A README is your project's first impression. Make it count."

- Dual-AI collaboration (Claude + Gemini)
- Research-driven, not template-driven
- Quality over speed
