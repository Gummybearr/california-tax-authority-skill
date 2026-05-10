# California Tax Authority Skill (Claude + Claude Cowork)

This repository contains a reusable skill for authority-weighted California tax research.

## Skill Path

- `.claude/skills/california-tax-authority/SKILL.md`

## What It Does

- Enforces legal authority ranking (statute -> regulation -> precedent -> admin guidance -> practical guidance -> commentary)
- Separates controlling authority from practical filing guidance
- Forces nonprecedential labeling and confidence guardrails
- Supports Federal + California domains (FTB, CDTFA, EDD, BOE, local tax, entity compliance)

## Included Files

- `.claude/skills/california-tax-authority/SKILL.md`
- `.claude/skills/california-tax-authority/references/authority-framework.md`
- `.claude/skills/california-tax-authority/GUIDELINES.md`
- `.claude/skills/california-tax-authority/examples/prompt-examples.md`

## Use in Claude Code

1. Keep this folder in your project.
2. Ask Claude tax research questions naturally.
3. Claude will auto-load the skill when relevant.

## Use in Claude Cowork

1. Zip `california-tax-authority` folder.
2. Open Claude > Customize > Skills.
3. Upload and enable the skill.

## Notes

This skill incorporates workflow discipline inspired by gstack-style skills:
- explicit procedural steps
- output contract
- deterministic labeling and risk signaling
