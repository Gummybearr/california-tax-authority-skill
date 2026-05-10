---
name: california-tax-authority
description: Authority-weighted tax research framework for California-focused work. Use when answering federal or California tax/compliance questions that require citation quality control, legal-authority ranking, jurisdiction-aware reasoning, taxpayer-role classification, or California sourcing/residency analysis. Covers CA income/franchise tax, nonresident sourcing, sole proprietor and independent contractor sourcing, CDTFA sales/use, EDD payroll, BOE property tax, local business tax, and entity compliance.
---

# California Tax Authority

## Purpose

Produce tax research answers that prioritize legal authority, taxpayer-role classification, jurisdiction fit, tax-year applicability, and current agency guidance over retrieval similarity or generic tax intuition.

Always separate:

- controlling authority
- administrative authority
- practical filing guidance
- nonprecedential research leads
- commentary

Do not give a filing-position conclusion unless the answer is supported by at least one primary or strong authority, or unless the answer clearly states that the support is practical guidance only and not enough to lock a filing position.

## Answer Style: Bottom Line First

For user-facing answers, start with the direct answer before the authority stack.

The first paragraph must answer the user’s question in plain English using one of:

- `Yes`
- `No`
- `Probably`
- `Possibly`
- `It depends`

Then give the one-sentence reason.

Do not begin a direct user-facing answer with `Issue` unless the user specifically asks for a formal research memo.

For direct practical questions, use this order:

1. `Bottom Line`
2. `Why`
3. `Authorities`
4. `Application`
5. `Filing Guidance`
6. `Risk`
7. `Sources`

For formal research memos, the full authority-first format may be used, but still include a short `Bottom Line` before the `Issue` section.

## Required Workflow

### 1. Classify the question first

Identify:

- Domain:
  - `federal income`
  - `CA income/franchise (FTB)`
  - `CA residency/sourcing`
  - `sales/use (CDTFA)`
  - `payroll (EDD)`
  - `property tax (BOE/county)`
  - `local business tax`
  - `entity compliance`
- Jurisdiction and agency owner.
- Tax year and effective date window.
- Taxpayer role:
  - W-2 employee
  - independent contractor
  - sole proprietor / Schedule C business
  - partner / S corporation shareholder / LLC member
  - corporation
  - trust/estate
  - other

### 2. Apply applicability filters before ranking

Confirm:

- jurisdiction
- tax type
- tax year
- effective date
- taxpayer role
- residency status
- source of income
- superseded, rescinded, obsolete, or amended status

Exclude stale or revoked authority from final support unless explicitly used as historical context.

### 3. Apply issue-specific guardrails

Before building the authority stack, check whether the question matches one of the recurring issue-specific guardrails in `references/authority-framework.md`, especially:

- California nonresident service-income sourcing
- W-2 employee vs independent contractor vs sole proprietor sourcing
- pass-through entity owner sourcing
- residency/domicile vs source-income distinction
- nonprecedential OTA or agency-ruling limitations

### 4. Build an authority stack

Use `references/authority-framework.md` as the source of truth.

Prefer:

1. statutes
2. regulations
3. binding/citable precedent
4. precedential OTA/BOE opinions where applicable
5. FTB/IRS/CDTFA/EDD/BOE formal administrative guidance
6. official forms, instructions, and publications
7. agency webpages and FAQs
8. nonprecedential materials
9. commentary

Do not invent authorities.

### 5. Run a current-agency-guidance conflict check

Before finalizing the answer, check whether current official agency guidance directly addresses the fact pattern.

If current official guidance gives a specific example that matches the facts, mention it and do not ignore it merely because an older general rule or a loosely related case appears to point elsewhere.

If authorities are in tension, state the tension clearly.

Example wording:

> The general rule for some service compensation looks to where services are physically performed. However, current FTB guidance gives a separate rule for independent contractors and sole proprietors, focusing on where the customer receives the benefit of the service.

### 6. Enforce nonprecedential guardrails

Mark these as `Nonprecedential` or `Research lead only` unless a specific rule says otherwise:

- IRS PLR/TAM/CCA
- FTB Chief Counsel Rulings
- CDTFA annotations or opinion letters
- OTA nonprecedential opinions
- Tax Court summary opinions
- informal agency FAQs
- commentary

Never present nonprecedential material as controlling law.

### 7. Confirm minimum authority quality

A filing-position answer must include at least one of:

- statute
- regulation
- binding/citable precedent
- precedential OTA/BOE opinion
- IRS Revenue Ruling / Revenue Procedure
- FTB Legal Ruling or other strong formal guidance

If only low-authority, nonprecedential, practical, or commentary material is available, explicitly limit confidence.

Use:

> Current materials are insufficient to lock a filing position. The items below are research leads or practical guidance only.

### 8. Collect external source links

For each authority cited in the final answer, capture at least one clickable source URL.

Prefer links in this order:

1. official statute/regulation source
2. official court source
3. official agency guidance
4. reputable open legal publisher
5. commentary

If no official public URL is available, say so explicitly and downgrade the item to `Research lead only` or `Secondary commentary`.

## California Nonresident Service-Income Guardrail

This guardrail is mandatory for California residency and sourcing questions.

### Do not use one generic service-income rule for all taxpayers

First classify the taxpayer role.

#### W-2 employee

For a nonresident W-2 employee, California generally sources wage income by where the employee physically performs services during the nonresident period.

California workdays may create California-source wages.

If all post-move services are performed outside California, wage income is generally not California-source, subject to special rules such as deferred compensation or equity-based compensation.

#### Independent contractor / sole proprietor / Schedule C business

For a nonresident independent contractor, sole proprietor, or Schedule C service business, do not default to the W-2 physical-work-location rule.

Current FTB practical guidance states that, for independent contractors and sole proprietors, California-source income is determined by where the customer receives the benefit of the service. Under that FTB guidance, the contractor’s work location is not treated as the controlling factor.

Label this as `Practical guidance` or `Administrative guidance`, not as binding law, unless a binding statute, regulation, or case directly supports the same proposition.

Do not overstate FTB webpages as controlling authority. They are important evidence of FTB’s administrative position and filing expectations, especially when directly on point, but they should be labeled separately from statutes, regulations, and binding precedent.

Therefore, if a nonresident sole proprietor performs services from Nevada for California customers who receive the benefit of those services in California, the answer should be:

- not “definitely non-California-source,” and
- instead “potentially or likely California-source under FTB’s customer-benefit approach, depending on the facts and apportionment.”

#### Pass-through entity owner

If the taxpayer owns an interest in a partnership, S corporation, or LLC, analyze entity-level California-source income and owner-level reporting separately.

Do not apply sole proprietor sourcing rules automatically to pass-through K-1 income.

#### Entity or apportioning business

If the taxpayer operates a trade or business with income inside and outside California, evaluate California apportionment and allocation rules, including Schedule R and market-assignment rules where applicable.

### Required answer framing for Nevada move + California clients + sole proprietor

For facts like:

> Moved from California to Nevada; now a Nevada resident; sole proprietor; performs 100% of services from Nevada; all or some clients are in California.

Use this bottom-line framing:

> Possibly yes. Even if you perform 100% of the services from Nevada, California may still treat the income as California-source if you are a sole proprietor or independent contractor and your California clients receive the benefit of the services in California.

Then explain:

> The key distinction is taxpayer role. A W-2 employee’s nonresident wage sourcing generally turns on where the employee physically performs services. But current FTB practical guidance for independent contractors and sole proprietors looks to where the customer receives the benefit of the service, not merely where the contractor performs the work.

Also separately analyze:

- whether the taxpayer is truly a California nonresident
- whether the taxpayer was a part-year resident during the move year
- whether any services were physically performed in California
- whether the business has California property, payroll, contractors, employees, offices, or agents
- whether Schedule R or market assignment applies
- whether any income is deferred, equity-based, pass-through, or tied to California real property

## Answer Contract

Use a bottom-line-first structure unless the user specifically requests a formal research memo.

### For direct user questions

Use these sections in order:

### 1. Bottom Line

Answer the question directly in 1-3 sentences.

Use plain English first. Do not start with citations or an issue statement.

For example:

> Possibly yes. If you are a nonresident sole proprietor or independent contractor, California may still treat the income as California-source if your California clients receive the benefit of your services in California. Physical work location alone is not dispositive for this taxpayer type.

### 2. Why

Explain the key rule in plain English.

For California nonresident service-income questions, distinguish:

- W-2 employee physical-work-location rule
- independent contractor / sole proprietor customer-benefit rule
- residency/domicile issue
- source-income issue

### 3. Authorities

Cite highest-ranked applicable authorities first.

Use labels such as:

- `Binding law`
- `Binding regulation`
- `Binding precedent`
- `Citable precedent`
- `Administrative authority`
- `Practical guidance`

Do not present forms, instructions, webpages, FAQs, or commentary as controlling law.

### 4. Application

Apply the facts to the rule.

Resolve conflicts by:

1. specific applicability to the taxpayer role and fact pattern
2. authority rank
3. jurisdiction fit
4. recency/effective date
5. precedential status

### 5. Filing Guidance

Include:

- form names
- schedule names
- recordkeeping suggestions
- filing threshold notes
- withholding or estimated tax considerations

Keep filing mechanics separate from legal authority.

### 6. Nonprecedential / Research Leads

Include nonbinding items only if useful.

Required labels:

- `Authority status: Nonprecedential`
- `Use: fact-pattern reference only`
- `Do not treat as controlling authority`

### 7. Risk and Review

Provide a brief risk level:

- `low`
- `medium`
- `high`

Explain why.

If scope crosses tax, employment, entity, residency, or legal-domicile issues, include professional review language.

### 8. Sources

Include a source map tying each major citation to at least one URL.

For each link, include:

- citation name or short cite
- authority label
- source type
- clickable URL
- why this source supports the point

### For formal research memos

If the user specifically asks for a formal memo, use this order:

1. `Bottom Line`
2. `Issue`
3. `Controlling Authorities`
4. `Administrative / Practical Guidance`
5. `Analysis`
6. `Practical Filing Guidance`
7. `Nonprecedential / Research Leads`
8. `Risk and Review`
9. `External Sources (Links)`

## Output Rules

- Never rely on commentary alone for a final filing-position conclusion.
- Do not claim binding status unless the authority is actually binding in that jurisdiction.
- Clearly label each citation with authority status:
  - `Binding law`
  - `Binding regulation`
  - `Binding precedent`
  - `Citable precedent`
  - `Administrative authority`
  - `Practical guidance`
  - `Nonprecedential`
  - `Research lead only`
  - `Secondary commentary`
  - `Superseded / caution`
- Every legal or practical citation in sections 2-6 must be traceable to at least one link in section 8.
- Prefer source links in this order:
  1. official statute/regulation source
  2. official court source
  3. official agency guidance
  4. reputable open legal publisher
  5. commentary
- If a citation has no verifiable link, mark it as `Research lead only` and do not use it as controlling support.
- Do not overread cases. State what the case actually held and explain any factual mismatch.
- Do not use W-2 sourcing rules to answer independent contractor or sole proprietor questions unless clearly explaining the distinction.

## Required Disclaimer Snippets

Use these snippets when conditions are met.

If only nonbinding guidance is available:

> Current support is nonprecedential or practical guidance only; this is a research lead, not controlling authority for a filing position.

If payroll classification issues appear:

> This is a payroll tax/compliance research draft. Worker classification may also require employment-law review.

If California residency/domicile is material:

> Residency and domicile are separate from source-income analysis. A taxpayer who remains a California resident may be taxed on worldwide income regardless of the source-income result.

If a sole proprietor/independent contractor California sourcing issue appears:

> For independent contractors and sole proprietors, current FTB guidance focuses on where the customer receives the benefit of the service, not merely where the contractor physically performs the work.

## Resource Usage

Read this file before finalizing answers:

- `references/authority-framework.md`

When the user asks for a strict ranking table, scoring formula, domain-specific ladder, sourcing analysis, or search order, quote from that reference and apply it directly.

Do not invent authorities.
