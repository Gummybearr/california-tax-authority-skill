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
- General-reader-first formatting: short opening, 3-key-point summary, and action checklist before deep legal detail.

## 3A) Readability Standard (General User)

Default audience is a non-lawyer.

For ordinary user questions, the answer should be skimmable in under 30 seconds:

- `Bottom Line` in 1-2 sentences
- `Quick Read (3 Key Points)` with exactly 3 short bullets
- `What To Do Now` with 3-5 concrete actions

Then provide legal depth (`Why`, `Risk`, `Authorities`, `Sources`).

Avoid long dense paragraphs when bullets are clearer.

Default mode is compact:

- target 180-260 words before `Sources`
- hard cap about 300 words before `Sources`
- 3-4 source links max unless user asks for deep research

Only expand to full detail when the user asks for memo-level depth.

## 3B) Question-Type Router (General Quality)

Select one output route based on user intent:

- practical yes/no
- compare/rank options
- filing/process steps
- authority reliability check
- formal memo

Do not combine multiple full routes in one answer.

## 3C) Final Concision Gate

Before sending:

- answer in first 1-2 sentences
- remove repeated caveats
- keep assumptions to 3 or fewer
- keep actionable bullets to 3-5
- trim legal detail before expanding length
- use precise case-effect wording (`rejected/limited`) unless an opinion expressly says `overruled`
- remove process narration (`now I'll run...`, `I have enough to answer...`)
- keep only one disclaimer block in compact answers
- if a case is central to the conclusion, include at least one official court or OTA link
- avoid commentary-only support for dispositive points when official sources are available

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

## 6A) Time-Sensitive Question Rule

For wording like `still taxable`, `currently`, `latest`, or `has this changed`, require a date-stamped recent case-law sweep before finalizing.

Minimum sweep:

- California published/citable appellate opinions
- OTA current-year + precedential opinions
- FTB legal-ruling, notice, and tax-news update pages

For nonresident sole-proprietor sourcing, run targeted queries (for example `CCR 17951-4`, `RTC 25136`, `customer benefit`, `nonresident sole proprietor`).

Require current-year coverage:

- derive the query year from the answer's freshness/as-of date
- include at least one current-year query and one prior-year query
- do not use a year range ending before the current year
- check California Courts published/citable opinions directly before saying no appellate case exists
- include one query with the agency name (`Franchise Tax Board`) plus current year on California Courts published/citable opinions
- if uncertain, run `current-1/current/current+1` plus one non-year-bounded official court query

In the final `Sources` section, include:

- `freshness check date`
- short `query -> source checked -> result` log

If that sweep is incomplete, do not provide a high-confidence filing-position conclusion.

## 6B) Pinpoint Citation Rule

When citing subsection-level authority:

- verify the subsection text
- verify taxpayer-role fit
- avoid citing a partnership subsection as if it controls sole-proprietor facts

If pinpoint text is not verified from a reliable source, label it as a research lead and avoid presenting it as controlling support.

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
