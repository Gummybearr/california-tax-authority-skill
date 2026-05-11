# California Tax Authority Skill

Turn Claude into a **California tax research copilot** that is concise, current-authority-first, and source-backed.

## Before vs After

Prompt example:

- `After moving from California to Nevada, if I’m a sole proprietor who performs 100% of services from Nevada for California clients, is that income still California-source taxable?`

Visual comparison:

| Before (no skill) | After (with skill) |
|---|---|
| <img src="without_claude_skill.png" alt="Without skill response screenshot" width="460" /> | <img src="with_claude_skill.png" alt="With skill response screenshot" width="460" /> |

| Before (no skill) | After (with skill) |
|---|---|
| Hard yes/no first | Risk-aware `Bottom Line` first |
| Can miss latest authority | Forces fresh sweep for `still/latest/current` |
| Long legal blocks | `3 key points + what to do now` first |
| Repeated disclaimers | One concise disclaimer block |
| Mixed source quality | Court/reg/statute first, commentary labeled |

<details>
<summary><strong>Open Before Raw Sample</strong></summary>

```text
This is a nuanced area of California tax law, and the answer is generally no - but with important caveats.

The Core Rule: Where You Perform the Work
California taxes income based on where the services are physically performed, not where the client is located. If you are a bona fide Nevada resident and perform 100% of your work from Nevada, that income is generally not California-source income and is not subject to California income tax.

What Makes This Tricky
1. You Must Be a True Nevada Resident
California's FTB is aggressive about residency audits. They look at day count, closest connections, and domicile facts.

2. Any Work Performed in California Is Taxable
If you physically work in California (meetings, client visits), those days can create CA-source income.

3. Market-Based vs Cost-of-Performance Confusion
Service sourcing and other income categories can follow different rules.

4. Pass-Through Entity Income
K-1 income from CA entities may still be California-source.

Practical Steps
- Establish Nevada domicile evidence
- Keep daily work-location records
- Avoid performing services while physically in California
- File Form 540NR when needed
```

</details>

<details>
<summary><strong>Open After Raw Sample</strong></summary>

```text
Now let me do the required current-authority sweep before answering. This answer involves a very recent published appellate court decision - Garcia-Rojas v. FTB, decided May 1, 2026 - that directly changes the landscape.

Bottom Line
Probably not under the theory California previously relied on - but the issue is not fully settled.

A California Court of Appeal decision issued just 10 days ago (Garcia-Rojas v. FTB, May 1, 2026) rejected the administrative rule the FTB and OTA had used since 2019 to tax nonresident sole proprietors on income from California clients. Under that ruling, Nevada-only physical performance is a strong argument against California tax. However, the court left open whether FTB can tax under a different legal theory.

Quick Read (3 Key Points)
- FTB previously relied on Bindley (OTA precedential) unitary-business framing.
- The Court of Appeal found that reasoning unconvincing on these facts.
- The opinion left room for alternate FTB theories.

What To Do Now
- Confirm Nevada residency break
- Track Garcia-Rojas status and FTB response
- Keep records showing 100% Nevada performance
- Consider protective filing posture with a CA tax professional

Risk
- Medium, improving but not low.
- Outcome can shift if review/depublication occurs or alternative theory is adopted.
```

</details>

## What You Get

- Clear first-screen format: `Bottom Line -> 3 key points -> What To Do Now`
- Better freshness control for time-sensitive questions
- Stronger source discipline (official sources first)
- Cleaner tone (less process narration, less repetition)

## Quick Setup

### Claude App
1. Enable code/file capability.
2. Customize -> Skills -> Upload skill zip.
3. Enable skill and ask questions normally.

### Claude Code
1. Put this folder at `.claude/skills/california-tax-authority/` (project) or `~/.claude/skills/california-tax-authority/` (global).
2. Ask normally or invoke `/california-tax-authority`.

## Skill Files

- `.claude/skills/california-tax-authority/SKILL.md`
- `.claude/skills/california-tax-authority/GUIDELINES.md`
- `.claude/skills/california-tax-authority/references/authority-framework.md`
- `.claude/skills/california-tax-authority/examples/prompt-examples.md`

## Closing Note
Do you want a SOC2-compliant, BlueJ-level California + Federal tax research engine? Reach out to `support@wesley-ai.co`
