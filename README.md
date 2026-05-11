# California Tax Authority Skill (Claude App + Claude Code + Claude Cowork)

This repository contains a reusable skill for authority-weighted California tax research.

## Skill Path

- `.claude/skills/california-tax-authority/SKILL.md`

## What It Does

- Enforces legal authority ranking (statute -> regulation -> precedent -> admin guidance -> practical guidance -> commentary)
- Separates controlling authority from practical filing guidance
- Forces nonprecedential labeling and confidence guardrails
- Forces a date-stamped recent case-law sweep for time-sensitive questions (e.g., "still taxable?", "latest/current")
- Forces subsection-level pinpoint verification (text + taxpayer-role fit) before using detailed citation claims
- Requires an `External Sources (Links)` section in final answers
- Supports Federal + California domains (FTB, CDTFA, EDD, BOE, local tax, entity compliance)

## Included Files

- `.claude/skills/california-tax-authority/SKILL.md`
- `.claude/skills/california-tax-authority/references/authority-framework.md`
- `.claude/skills/california-tax-authority/GUIDELINES.md`
- `.claude/skills/california-tax-authority/examples/prompt-examples.md`

## Output Contract Highlights

- Final answers must include:
  - `Issue`
  - `Controlling Authorities`
  - `Analysis`
  - `Practical Filing Guidance`
  - `Nonprecedential / Research Leads`
  - `Risk and Review`
  - `External Sources (Links)`
- Every cited authority used for conclusions should map to at least one clickable link.
- Official sources are preferred whenever available.

## Setup Guide

### A) Claude App (Web/Desktop)

1. Enable `Code execution and file creation` in Settings > Capabilities.
2. Go to Customize > Skills.
3. Click `+` > `Create skill` > `Upload a skill`.
4. Upload a zip containing the `california-tax-authority` folder (with `SKILL.md` inside).
5. Turn the skill on.
6. Ask naturally, or explicitly request use of `california-tax-authority`.

### B) Claude Code

Project skill option:
1. Place this directory under your repo at `.claude/skills/california-tax-authority/`.
2. Start Claude Code in that project.
3. Ask tax research questions naturally (auto trigger), or invoke directly with `/california-tax-authority`.

Personal skill option:
1. Place the directory under `~/.claude/skills/california-tax-authority/`.
2. Use it across projects in Claude Code.

### C) Claude Cowork

1. Zip the `california-tax-authority` folder.
2. In Cowork, open Customize > Skills.
3. Upload and enable the skill.
4. For org-shared workflows, use org skill sharing/install paths as configured by your workspace owner.

## Notes

This skill incorporates workflow discipline inspired by gstack-style skills:
- explicit procedural steps
- hard output contract
- deterministic labeling and risk signaling
