# California Tax Authority Framework

This reference defines the authority ranking system used by the `california-tax-authority` skill.

## 1) Global Authority Ladder (All Domains)

Apply `Rank 0` first, then rank by `1 -> 12`.

| Rank | Level | Type | Examples | Handling |
| --- | --- | --- | --- | --- |
| 0 | Applicability Filter | Jurisdiction, tax year, effective date, superseded/rescinded status | 2024 vs 2025 forms, rescinded guidance | Filter first. Exclude stale/revoked sources or label as caution. |
| 1 | Highest | Statutes / Codes | IRC, CA Revenue and Taxation Code, CUIC, municipal code | Primary controlling basis. |
| 2 | Highest | Final or temporary regulations | Treasury Regs, 26 CFR, CCR Title 18 | Next strongest controlling basis. |
| 3 | High | Binding court precedent | U.S. Supreme Court, Ninth Circuit, CA Supreme Court, published CA Court of Appeal | Strong if jurisdiction fits. |
| 4 | High | Tax-specialized precedential opinions | U.S. Tax Court regular opinions, OTA precedential, BOE precedential | Strong, but confirm precedential status. |
| 5 | High | Official administrative guidance | IRS Rev. Rul./Rev. Proc./Notice, FTB Legal Ruling/Notice | Strong practical authority, subordinate to statute/regulation/case law. |
| 6 | Medium | Agency rulings or fact-specific guidance | FTB Chief Counsel Ruling, IRS PLR/TAM/CCA, CDTFA opinion/annotation, EDD ruling | Usually nonprecedential. Label clearly. |
| 7 | Medium | Official practical guidance | Forms, instructions, publications, agency guides | Filing operations guidance, not primary legal authority. |
| 8 | Medium-Low | Internal procedural manuals | IRM, FTB/CDTFA manuals, BOE Assessors' Handbook | Operational context, weak for taxpayer legal position. |
| 9 | Low | Nonprecedential opinions | OTA nonprecedential, Tax Court summary opinions | Fact-pattern reference only. |
| 10 | Low | Legislative history / policy history | Committee reports, bill analyses | Interpretation support only when text is ambiguous. |
| 11 | Low | Commentary | Spidell, CalCPA, CCH, RIA, Bloomberg Tax, Tax Notes, internal brief | Secondary analysis only. |
| 12 | Lowest | Templates/checklists | Notice response templates, internal checklists | Format support only. Not legal authority. |

## 2) Federal Tax Ladder

| Rank | Authority |
| --- | --- |
| F1 | U.S. Constitution, Internal Revenue Code (26 U.S.C.) |
| F2 | Final/temporary Treasury Regulations, 26 CFR |
| F3 | U.S. Supreme Court opinions |
| F4 | Ninth Circuit published opinions (high relevance for CA taxpayers) |
| F5 | U.S. Tax Court regular opinions |
| F6 | Other circuit/district/CFC/bankruptcy decisions (jurisdiction-specific or persuasive) |
| F7 | IRS Revenue Rulings and Revenue Procedures |
| F8 | IRS Notices, Announcements, IRB items |
| F9 | IRS written determinations (PLR/TAM/CCA), nonprecedential |
| F10 | IRS forms/instructions/publications |
| F11 | IRS FAQs/Tax Tips/news releases |
| F12 | Internal Revenue Manual (IRM) |
| F13 | Commercial commentary |

## 3) California Income/Franchise (FTB) Ladder

| Rank | Authority |
| --- | --- |
| C1 | California Revenue and Taxation Code |
| C2 | CCR Title 18 / FTB regulations |
| C3 | California Supreme Court published opinions |
| C4 | California Court of Appeal published opinions |
| C5 | OTA precedential opinions |
| C6 | BOE precedential opinions still in force/relevance |
| C7 | FTB Legal Rulings |
| C8 | FTB Notices |
| C9 | FTB Chief Counsel Rulings, fact-specific and generally nonprecedential |
| C10 | FTB forms/instructions/publications, including 540NR Booklet, Schedule CA instructions, Schedule R instructions, Pub 1001, Pub 1004, Pub 1031, and Pub 1100 |
| C11 | OTA nonprecedential opinions |
| C12 | FTB webpages/FAQs/Tax News, including current practical examples |
| C13 | Commentary |

Important caution for C10-C12:

- These materials are generally not controlling legal authority.
- However, current FTB forms, instructions, publications, and webpages may be highly relevant practical guidance, especially when they directly address the taxpayer’s exact fact pattern.
- If current FTB practical guidance conflicts with a broad generalization derived from older or less-specific authority, state the tension and avoid an overconfident filing-position conclusion.

## 4) California Sales/Use (CDTFA) Ladder

| Rank | Authority |
| --- | --- |
| S1 | CA Revenue and Taxation Code (sales/use provisions) |
| S2 | CDTFA regulations / CCR Title 18 |
| S3 | CA Supreme Court / published Court of Appeal |
| S4 | OTA precedential business tax opinions |
| S5 | BOE precedential decisions (historical but valid where applicable) |
| S6 | CDTFA Business Taxes Law Guide materials |
| S7 | CDTFA annotations / legal opinion letters (generally nonbinding) |
| S8 | CDTFA publications/guides/rate tables |
| S9 | CDTFA webpages/FAQs/newsletters |
| S10 | Commentary |

Important caution for S7:
- Annotation/legal opinion material is a research lead.
- If conflict exists, statute/regulation/case law controls.

## 5) California Payroll (EDD) Ladder

| Rank | Authority |
| --- | --- |
| E1 | California Unemployment Insurance Code |
| E2 | CCR / EDD payroll tax regulations |
| E3 | CA Supreme Court / published Court of Appeal |
| E4 | EDD precedential or ruling materials (including DE 231 series as applicable) |
| E5 | EDD Employer's Guide (DE 44) |
| E6 | EDD forms/instructions/webpages |
| E7 | Commentary |

Required note for worker classification issues:
- `This is a payroll tax/compliance research draft. Worker classification may also require employment-law review.`

## 6) California Property Tax (BOE + County) Ladder

| Rank | Authority |
| --- | --- |
| P1 | California Constitution + property tax statutes in Revenue and Taxation Code |
| P2 | BOE property tax regulations / CCR |
| P3 | CA Supreme Court / published Court of Appeal |
| P4 | BOE precedential decisions |
| P5 | BOE Property Taxes Law Guide |
| P6 | BOE Property Tax Annotations (research lead) |
| P7 | BOE Assessors' Handbook |
| P8 | County assessor forms/pages |
| P9 | Commentary |

## 7) Local Business Tax Ladder

| Rank | Authority |
| --- | --- |
| L1 | Municipal code (city/county ordinance) |
| L2 | Local regulations/administrative rules |
| L3 | Published court opinions interpreting local tax |
| L4 | Official city/county finance or treasurer guidance/rulings |
| L5 | City/county forms and instructions |
| L6 | Local FAQs/webpages |
| L7 | Commentary |

Always track metadata for local sources:
- city/county name
- tax year
- effective date
- last updated date

## 8) Entity Compliance Ladder (SOS + FTB)

| Rank | Authority |
| --- | --- |
| B1 | California Corporations Code |
| B2 | California SOS regulations |
| B3 | California court opinions |
| B4 | SOS forms/instructions |
| B5 | FTB suspension/forfeiture compliance guidance |
| B6 | SOS webpages/FAQs |
| B7 | Commentary |

## 9) Professional Standards / Liability Layer

Use this for risk controls, not tax-law conclusions.

| Rank | Authority |
| --- | --- |
| G1 | Treasury Circular 230 |
| G2 | AICPA SSTS |
| G3 | California Board of Accountancy laws/rules |
| G4 | IRS due diligence / PTIN guidance |
| G5 | CTEC rules (if applicable) |
| G6 | Firm internal policy templates |

## 10) Commentary Layer Rules

| Rank | Type | Handling |
| --- | --- | --- |
| M1 | Licensed premium commentary | Useful secondary analysis; respect license boundaries. |
| M2 | Professional association articles | Cite date/author/source, still secondary. |
| M3 | Law/CPA firm public articles | Verify against primary authority. |
| M4 | Internal editorial brief | Show reviewer/date and base authorities. |
| M5 | Generic blog/SEO material | Avoid as legal support. |

Key rule:
- Use commentary to explain, not to establish controlling conclusions.

## 11) Scoring Model

### Base Score Table

| Score | Authority Type |
| --- | --- |
| 100 | Statute/code |
| 95 | Final/temporary regulation |
| 92 | U.S. Supreme Court / CA Supreme Court |
| 90 | Ninth Circuit / published CA Court of Appeal |
| 85 | Tax Court regular / OTA precedential / BOE precedential |
| 78 | IRS Rev. Rul./Rev. Proc. or FTB Legal Ruling |
| 72 | IRS Notice/Announcement or FTB Notice |
| 65 | FTB Chief Counsel / CDTFA legal opinion / EDD ruling |
| 55 | PLR/TAM/CCA or other written determination |
| 50 | Forms and instructions |
| 45 | Publications/agency guides |
| 35 | Internal manuals/handbooks |
| 30 | Nonprecedential opinions |
| 25 | FAQs/webpages/newsletters |
| 20 | Licensed commentary |
| 15 | Public commentary |
| 5 | Templates/checklists |

### Multipliers

| Multiplier | Condition |
| --- | --- |
| x1.25 | Same jurisdiction + same tax type + same tax year |
| x1.15 | Exact section/line/issue-tag match |
| x1.10 | Current and not superseded |
| x0.75 | Cross-jurisdiction persuasive authority |
| x0.60 | Older source, status uncertain |
| x0.40 | Potentially superseded/rescinded |
| x0.25 | Nonprecedential used for filing-position question |
| x0.10 | Commentary-only support |

Composite score guideline:
- `composite_score = base_score * all applicable multipliers`

## 12) Generation Rules (Hard Constraints)

1. Filing-position conclusions require at least one primary/strong authority:
- statute
- regulation
- binding/citable precedent
- precedential OTA/BOE opinion
- IRS Rev. Rul./Rev. Proc.
- FTB Legal Ruling

2. If no primary/strong authority is found:
- state limitation explicitly:
  - `Current materials are insufficient to lock a filing position. The items below are research leads.`

3. Nonprecedential content must be clearly marked:
- `Authority status: Nonprecedential`
- `Use: fact-pattern reference only`
- `Do not treat as controlling authority`

4. Match agency owner to question:
- Federal income -> IRS/Treasury/federal courts/Tax Court
- CA income/franchise -> FTB/OTA/CA courts
- Sales/use -> CDTFA/OTA/BOE
- Payroll -> EDD
- Property tax -> BOE/county assessor
- Entity compliance -> CA SOS/FTB
- Local business tax -> city/county finance/treasurer

5. Keep legal authority and practical guidance separate.

6. External links are required in final outputs:
- Every cited authority used in `Controlling Authorities`, `Practical Filing Guidance`, or `Nonprecedential / Research Leads` must have at least one clickable source URL in a dedicated `External Sources (Links)` section.
- If no verifiable public link can be found, the item cannot be treated as controlling support and must be labeled `Research lead only` or `Secondary commentary`.

## 13) Question-Type Search Order

### Federal vs California conformity questions
1. IRC
2. Treasury Regulations
3. FTB conformity source / RTC
4. CCR Title 18
5. FTB Pub 1001 / Schedule CA instructions
6. FTB Legal Ruling / Notice
7. OTA precedential opinions
8. Commentary

### California residency / sourcing

1. RTC residency and nonresident sourcing provisions.
2. CCR Title 18 regulations, especially rules applicable to nonresident income and business/apportionment.
3. Current FTB residency and nonresident guidance, including current “Leaving California” scenarios.
4. Current FTB form instructions and publications, including 540NR Booklet, Schedule R instructions, Pub 1004, Pub 1031, and Pub 1100 as applicable.
5. CA Supreme Court and published Court of Appeal cases.
6. OTA precedential opinions.
7. FTB Legal Rulings / Notices.
8. FTB Chief Counsel Rulings, labeled as fact-specific or nonprecedential where applicable.
9. OTA nonprecedential opinions, labeled as nonprecedential.
10. Commentary.

Special rule:

For independent contractor / sole proprietor / Schedule C service-income sourcing, current FTB practical guidance must be checked before finalizing the answer. If the fact pattern matches FTB’s independent contractor/sole proprietor customer-benefit scenario, the answer must address that guidance directly.

### FTB notice response
1. RTC
2. CCR Title 18
3. FTB Legal Ruling / Notice
4. OTA precedential opinions
5. FTB Chief Counsel Rulings
6. FTB forms/instructions/publications
7. OTA nonprecedential opinions
8. Client template

### CDTFA sales/use tax
1. RTC sales/use provisions
2. CDTFA regulations / CCR Title 18
3. CA published cases
4. OTA/BOE precedential business tax opinions
5. CDTFA Business Taxes Law Guide
6. CDTFA annotations
7. CDTFA publications / rate tables
8. Commentary

### EDD payroll / worker classification
1. CUIC
2. CCR / EDD regulations
3. CA published cases
4. EDD DE 231 series / ruling materials
5. EDD DE 44
6. EDD forms/webpages
7. Commentary

### Local business tax
1. Municipal code
2. Local regulations
3. Published cases
4. Local finance/treasurer official guidance
5. Forms/instructions
6. FAQs/webpages
7. Commentary

## 13A) California Residency / Sourcing Decision Tree

Use this decision tree for California nonresident and part-year resident questions.

### Step 1: Separate residency from sourcing

Always separate:

1. Residency/domicile:
   - Is the taxpayer a California resident, part-year resident, or nonresident?
   - California residents are generally taxed on worldwide income.
   - Part-year residents are generally taxed on worldwide income during the resident period and California-source income during the nonresident period.

2. Source income:
   - If the taxpayer is a nonresident, does the income have a California source?

3. Filing obligation:
   - If there is California-source income or part-year resident income, determine whether a California return is required.

4. Apportionment/allocation:
   - If income is from a business, trade, or profession conducted within and outside California, consider Schedule R and apportionment/allocation rules.

### Step 2: Classify the taxpayer role

Classify the income recipient before applying any service-income sourcing rule:

- W-2 employee
- Independent contractor
- Sole proprietor / Schedule C business
- Pass-through entity owner
- Corporation or other entity
- Investor receiving intangible income
- Real-property owner
- Deferred/equity compensation recipient

### Step 3: Apply the correct service-income rule

#### W-2 employee compensation

For a nonresident W-2 employee, California generally sources wage compensation to California to the extent the employee physically performs services in California.

If the employee performs all post-move services outside California, the wage income is generally not California-source, subject to special rules such as deferred or equity-based compensation.

#### Independent contractor / sole proprietor service income

For a nonresident independent contractor or sole proprietor, do not automatically apply the W-2 employee workday rule.

Current FTB guidance states that California-source income for independent contractors/sole proprietors is determined by where the customer receives the benefit of the service. The contractor’s work location is not a factor.

Therefore:

- California customer receives benefit in California -> possible or likely California-source income.
- Non-California customer receives benefit outside California -> generally weaker California-source position.
- Mixed customer benefit locations -> analyze apportionment/allocation and customer-level sourcing.
- Unclear benefit location -> ask for facts or state uncertainty.

#### Trade or business inside and outside California

For a nonresident individual operating a trade or business inside and outside California, check Schedule R instructions and CCR Title 18 section 17951-4.

If the activity is an apportioning trade or business, analyze whether California-source income is determined using apportionment and market-assignment rules.

### Step 4: Apply mandatory caveats

For California nonresident service-income questions, always check:

- whether the taxpayer actually changed domicile/residency
- whether the taxpayer was a part-year resident in the move year
- whether any workdays occurred in California
- whether the business has California property, payroll, employees, contractors, agents, or offices
- whether the income is pass-through income
- whether the income is tied to California real property
- whether the income is deferred compensation or equity-based compensation
- whether the taxpayer has California withholding or estimated tax obligations

## 13B) California Nonresident Sole Proprietor / Independent Contractor Guardrail

This is a hard guardrail.

If the question includes all or most of these facts:

- taxpayer moved out of California
- taxpayer claims nonresident status
- taxpayer is a sole proprietor, independent contractor, self-employed consultant, freelancer, or Schedule C business
- taxpayer performs services remotely from another state
- taxpayer has California customers or clients

Then do not answer:

> The income is not California-source because the services are performed outside California.

Instead, answer with this structure:

1. Start with a cautious conclusion:
   - “Possibly yes.”
   - “California may still treat the income as California-source.”
   - “Physical work location alone is not dispositive for a sole proprietor or independent contractor.”

2. Explain the FTB customer-benefit rule:
   - Current FTB guidance for independent contractors/sole proprietors looks to where the customer receives the benefit of the service.
   - The contractor’s work location is not a factor under that guidance.

3. Apply the facts:
   - If California clients receive the benefit in California, California-source income risk is significant.
   - If the benefit is received outside California, the California-source case is weaker.
   - If benefit location is mixed or unclear, recommend customer-by-customer or receipts-based analysis.

4. Separate residency:
   - If the taxpayer remains a California resident, California may tax worldwide income regardless of sourcing.
   - If the taxpayer is a bona fide nonresident, only California-source income is at issue.

5. Discuss filing:
   - Nonresident sole proprietors with California-source income may need Form 540NR.
   - If the business has income/loss inside and outside California, Schedule R may be required.

6. Risk conclusion:
   - “Low” only if no California customer benefit, no California workdays, no California business presence, and strong nonresident facts.
   - “Medium” if California customers receive benefit in California but facts are otherwise clean.
   - “High” if residency is weak, work occurs in California, or California business presence exists.
  
## 13C) Case-Law Caution: Do Not Overread Valentino

Do not cite Valentino v. Franchise Tax Board as controlling authority for the broad proposition that a nonresident sole proprietor’s service income is sourced only where the services are physically performed.

Use Valentino cautiously.

Valentino involved California taxation of income passed through from an S corporation to a nonresident shareholder. It may be relevant to pass-through entity sourcing issues, but it should not be the primary authority for a Schedule C sole proprietor remote-service fact pattern.

If Valentino is cited:

- identify the actual taxpayer structure
- explain the pass-through context
- do not use it to override current FTB guidance for independent contractors/sole proprietors
- do not present it as a clean “physical performance controls” rule for sole proprietors

## 14) Citation Label Set for UI/Output

Use one label per citation:
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

## 15) External Link Policy

### Link Quality Order

Use this order when selecting links for cited authorities:
1. Official statute/regulation source (for example `uscode.house.gov`, `ecfr.gov`, `leginfo.legislature.ca.gov`).
2. Official court source (for example `supremecourt.gov`, `courtinfo.ca.gov`, official appellate/tax court publication pages).
3. Official agency source (for example `irs.gov`, `ftb.ca.gov`, `cdtfa.ca.gov`, `edd.ca.gov`, `boe.ca.gov`, county/city official sites).
4. Reputable open legal publisher when official source is unavailable.
5. Commentary only as secondary support.

### Required Source Map Format

Final answers must include a dedicated `External Sources (Links)` section with one row/bullet per authority, including:
- citation name or short cite
- authority label
- source type (`official statute`, `official regulation`, `official court`, `official agency`, `secondary`)
- clickable URL
- short note explaining why the source supports the statement

### Link Failure Handling

- If an official link is inaccessible, add a backup link and mark the confidence impact.
- If no reliable link is found, explicitly state:
  - `No public verifiable link located for this item; treated as research lead only.`
- Do not present unlinked items as controlling legal authority.
