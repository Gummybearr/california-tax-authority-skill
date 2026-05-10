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
| C9 | FTB Chief Counsel Rulings (fact-specific) |
| C10 | FTB forms/instructions/publications (including Pub 1001, Schedule CA instructions) |
| C11 | OTA nonprecedential opinions |
| C12 | FTB webpages/FAQs/Tax News |
| C13 | Commentary |

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
1. RTC
2. CCR Title 18
3. CA published cases
4. OTA precedential opinions
5. FTB Legal Ruling / Notice
6. FTB publications / 540NR instructions
7. OTA nonprecedential opinions
8. Commentary

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
