# California Tax Authority Skill Guidelines

This folder is a Claude/Claude Cowork-compatible project skill.

## 1) Compatibility

- Location for project skill: `.claude/skills/california-tax-authority/`
- Required file: `SKILL.md`
- Optional support files: `references/*.md`, `examples/*.md`

This structure works for:
- Claude Code project skills
- Claude Cowork custom skills (upload as zip if needed)

## 2) What This Skill Enforces

- Authority-first tax research for California-focused work.
- Jurisdiction and tax-year applicability filtering before ranking.
- Hard separation between:
  - controlling legal authority
  - practical filing guidance
  - nonprecedential research leads
  - commentary
- Mandatory nonprecedential labeling.
- No filing-position conclusion without at least one primary/strong authority.

## 3) Sources and Ranking

Use `references/authority-framework.md` as the single source of truth for:
- global authority ladder
- federal/FTB/CDTFA/EDD/BOE/local ladders
- score and multiplier model
- question-type search order
- citation labels for UI/output

## 4) gstack-Inspired Practices Applied

The skill design borrows gstack's strengths:
- explicit workflow instead of vague advice
- hard output contract and checklist-style enforcement
- clear escalation when authority support is weak
- deterministic labeling rules for downstream review

## 5) How to Use

Natural-language trigger examples:
- "캘리포니아 거주지 판정 authority 순서로 정리해줘"
- "FTB notice 답변 초안인데 controlling authority 먼저 보여줘"
- "CDTFA annotation밖에 없을 때 리스크 문구 포함해서 써줘"

Direct trigger (if slash commands are enabled):
- `/california-tax-authority`

## 6) Sharing in Claude Cowork

If you need to import manually in Cowork:
1. Zip the `california-tax-authority` folder.
2. Open Claude > Customize > Skills.
3. Upload the zip file.
4. Enable the skill for your workspace.

