---
name: california-tax-authority
description: Authority-weighted tax research framework for California-focused work. Use when answering federal or California tax/compliance questions that require citation quality control, legal-authority ranking, and jurisdiction-aware reasoning (for example CA income/franchise tax, CDTFA sales/use, EDD payroll, BOE property tax, local business tax, and entity compliance).
---

# California Tax Authority

## Purpose

Produce tax research answers that prioritize legal authority over retrieval similarity.
Always separate controlling authority from practical guidance and commentary.

## Required Workflow

1. Classify the question first:
- Domain: `federal income`, `CA income/franchise (FTB)`, `sales/use (CDTFA)`, `payroll (EDD)`, `property tax (BOE/county)`, `local business tax`, or `entity compliance`.
- Jurisdiction and agency owner.
- Tax year and effective date window.

2. Apply applicability filters before ranking:
- Confirm `jurisdiction`, `tax type`, `tax year`, and `effective date`.
- Check `superseded/rescinded` status.
- Exclude stale or revoked authority from final support unless explicitly used as historical context.

3. Build an authority stack:
- Use `references/authority-framework.md` as the source of truth.
- Prefer statutes, regulations, and binding/citable precedent.
- Treat forms, instructions, manuals, and commentary as lower-level support.

4. Enforce nonprecedential guardrails:
- Mark PLR/TAM/CCA, OTA nonprecedential opinions, summary opinions, annotations, and similar items as `Nonprecedential`.
- Never present nonprecedential material as controlling law.

5. Confirm minimum authority quality:
- A filing-position answer must include at least one primary or strong authority.
- If only low-authority or commentary material is available, explicitly limit confidence and ask for additional primary authority.

## Answer Contract

Always produce the following sections in order:

1. `Issue`
- One sentence framing the tax question and scope.

2. `Controlling Authorities`
- Cite highest-ranked applicable authorities first.
- Include short labels such as `Binding law`, `Binding regulation`, `Binding precedent`, `Administrative authority`.

3. `Analysis`
- Apply facts to controlling authorities.
- Resolve conflicts by authority rank, then by jurisdiction fit, then by recency/effective date.

4. `Practical Filing Guidance`
- Put forms, instructions, publications, and agency guides here.
- Keep this separate from legal authority.

5. `Nonprecedential / Research Leads`
- Include nonbinding items with explicit caution labels.

6. `Risk and Review`
- Provide a brief risk level (`low`, `medium`, `high`) and why.
- If scope crosses tax + employment/entity law boundaries, require professional review note.

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
- When authority support is weak, say so directly and request missing facts or primary sources.

## Required Disclaimer Snippets

Use these snippets when conditions are met:

- If only nonbinding guidance is available:
  - `Current support is nonprecedential or practical guidance only; this is a research lead, not controlling authority for a filing position.`
- If payroll classification issues appear:
  - `This is a payroll tax/compliance research draft. Worker classification may also require employment-law review.`

## Resource Usage

Read this file for details before finalizing answers:
- `references/authority-framework.md`

When the user asks for a strict ranking table, scoring formula, domain-specific ladder, or search order, quote from that reference and apply it directly.

Do not invent authorities.
