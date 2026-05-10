# California Tax Authority Skill Guidelines

This folder is a Claude/Claude Cowork-compatible project skill.

## 1) Compatibility

- Project skill location: `.claude/skills/california-tax-authority/`
- Required entrypoint: `SKILL.md`
- Optional support files:
  - `references/*.md`
  - `examples/*.md`

Works with:
- Claude Code project skills
- Claude Cowork custom skills, uploaded as a zip if needed

## 2) Purpose

This skill produces concise, authority-weighted California tax research answers.

It is designed to prevent:

- answering from intuition instead of authority
- applying the wrong taxpayer rule
- treating agency webpages as binding law
- relying on stale or superseded authority
- overstating cases beyond their holdings
- giving filing-position conclusions without adequate support

## 3) Core Standards

The skill enforces:

- Bottom-line-first answers.
- Jurisdiction, tax type, tax year, and taxpayer-role classification.
- Authority ranking before conclusion.
- Freshness and current-status checks for directly relevant authority.
- Clear separation of:
  - binding law
  - binding regulation
  - binding/citable precedent
  - formal administrative authority
  - practical guidance
  - nonprecedential research leads
  - commentary
- Official-source-first citation links.
- Narrow case reading: state what the authority actually holds and what it leaves open.

## 4) High-Risk California Issues

Apply extra care to:

- residency and domicile
- nonresident sourcing
- sole proprietor / independent contractor service income
- W-2 remote work
- pass-through entity income
- CDTFA annotations
- EDD worker classification
- local business taxes
- FTB/CDTFA/EDD webpages or publications that are practical guidance, not law

## 5) Nonresident Service-Income Principle

Do not use one generic service-income sourcing rule for all taxpayers.

Always classify the taxpayer first:

- W-2 employee
- independent contractor
- sole proprietor / Schedule C business
- pass-through owner
- corporation or other entity

For W-2 employees, physical work location is often central.

For independent contractors and sole proprietors, current FTB practical guidance may focus on where the customer receives the benefit of the service. But do not stop there. Check statutes, regulations, current cases, precedential administrative decisions, and whether recent authority limits or conflicts with the agency position.

## 6) Current Authority Rule

Do not rely only on static rules in this skill.

Before finalizing a filing-position answer, check whether there is current, directly relevant authority:

- published California appellate decisions
- California Supreme Court decisions
- OTA precedential opinions
- amended statutes or regulations
- current FTB/CDTFA/EDD/BOE guidance
- review granted, depublished, modified, superseded, withdrawn, or rescinded authority

If agency guidance and higher authority conflict, explain the conflict and risk. Do not treat either side as automatically dispositive unless the authority supports that.

## 7) How to Use

Example triggers:

- "Analyze this California sourcing issue with authority ranking."
- "Can a nonresident sole proprietor have California-source income?"
- "Draft an FTB notice response and label nonprecedential support."
- "Rank the CDTFA authority for this sales tax position."
- "Is this OTA opinion precedential?"
- "Separate California residency from source-income analysis."

Direct trigger, if slash commands are enabled:

- `/california-tax-authority`

## 8) Maintenance Notes

When the skill performs poorly, improve the general rule instead of hardcoding one-off answers.

Prefer durable rules like:

- classify taxpayer role first
- verify current status
- read cases narrowly
- separate agency position from binding law
- state uncertainty when authority is mixed

Avoid turning examples into categorical rules.
