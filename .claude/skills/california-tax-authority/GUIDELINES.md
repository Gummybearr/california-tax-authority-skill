# California Tax Authority Skill Guidelines

This folder is a Claude/Claude Cowork-compatible project skill.

## 1) Compatibility

- Project skill location: `.claude/skills/california-tax-authority/`
- Required entrypoint: `SKILL.md`
- Optional support files:
  - `references/*.md`
  - `examples/*.md`

This structure works for:
- Claude Code project skills
- Claude Cowork custom skills, uploaded as a zip if needed

## 2) What This Skill Enforces

This skill enforces authority-first California tax research. It is designed to prevent answers that sound legally precise but rely on the wrong authority, stale authority, nonprecedential material, or an overbroad general rule.

The skill specifically enforces:

- Authority-weighted tax research for California-focused work.
- Jurisdiction, tax type, taxpayer type, and tax-year filtering before ranking.
- Separate treatment of:
  - controlling legal authority
  - administrative guidance
  - practical filing guidance
  - nonprecedential research leads
  - commentary
- Mandatory nonprecedential labeling.
- No filing-position conclusion without at least one primary or strong authority.
- Mandatory external source links for cited authorities.
- Official-source-first link policy for every citation.
- Current-agency-guidance conflict checks before final conclusions.
- Taxpayer-role distinction, especially for:
  - W-2 employees
  - independent contractors
  - sole proprietors / Schedule C businesses
  - pass-through entity owners
  - corporations and other entities

## 3) Critical California Nonresident Sourcing Guardrail

For California nonresident sourcing questions, the skill must not collapse all service income into a single “where services are physically performed” rule.

The skill must first identify the taxpayer role:

- W-2 employee
- Independent contractor
- Sole proprietor / Schedule C business
- Partner, S corporation shareholder, or LLC member
- Corporation or other entity

For W-2 employees, California generally sources nonresident wage income by where the employee physically performs services, subject to special rules such as deferred or equity-based compensation.

For independent contractors and sole proprietors, do not default to the W-2 workday rule. Current FTB guidance states that California-source income for independent contractors/sole proprietors is determined by where the customer receives the benefit of the service, and that the contractor’s work location is not a factor.

Therefore, for a fact pattern such as:

> A taxpayer moved from California to Nevada, is a sole proprietor, performs 100% of services from Nevada, and serves California clients.

The skill should not conclude that the income is automatically non-California-source merely because the work is physically performed in Nevada. The skill must analyze whether California customers receive the benefit of the services in California.

## 4) Sources and Ranking

Use `references/authority-framework.md` as the single source of truth for:

- global authority ladder
- federal, FTB, CDTFA, EDD, BOE, local, and entity-compliance ladders
- score and multiplier model
- question-type search order
- citation labels for output
- external link quality and fallback rules
- California nonresident service-income decision tree
- current-agency-guidance conflict check

## 5) gstack-Inspired Practices Applied

The skill design borrows gstack's strengths:

- explicit workflow instead of vague advice
- hard output contract and checklist-style enforcement
- clear escalation when authority support is weak
- deterministic labeling rules for downstream review
- issue-specific guardrails for recurring failure modes
- no unsupported filing-position conclusions

## 6) How to Use

Natural-language trigger examples:

- "Analyze California residency sourcing with authority ranking."
- "Prepare a California FTB notice response draft and label any nonprecedential support."
- "Can a nonresident sole proprietor working outside California still have California-source income from California customers?"
- "For a California sourcing issue, separate controlling authority from practical FTB guidance."
- "Rank the authority for this CDTFA sales tax position."
- "Explain whether this OTA opinion is precedential or only a research lead."

Direct trigger, if slash commands are enabled:

- `/california-tax-authority`

## 7) Sharing in Claude Cowork

If manual import is needed in Cowork:

1. Zip the `california-tax-authority` folder.
2. Open Claude > Customize > Skills.
3. Upload the zip file.
4. Enable the skill for the workspace.

## 8) Maintenance Notes

When the skill gives an incorrect or overconfident answer, update the relevant guardrail rather than only adding another example.

Common failure modes to guard against:

- Treating FTB webpages as controlling law without labeling them as practical or administrative guidance.
- Treating nonprecedential OTA opinions as controlling.
- Using a general rule when a more specific taxpayer-type rule applies.
- Applying W-2 employee sourcing rules to independent contractors or sole proprietors.
- Citing a case for a proposition that is broader than the case actually supports.
- Ignoring current FTB examples that directly match the facts.
