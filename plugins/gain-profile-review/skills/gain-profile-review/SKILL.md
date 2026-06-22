---
name: gain-profile-review
description: Review analyst-drafted Gain.pro company profiles and asset IDs using Gain house standards, with emphasis on Polish Full profiles, Key Facts, Business, Market, Background, Assessment, Pros and Cons, financial consistency, ownership, and cross-section quality. Use when asked to review, approve, correct, rewrite, quality-check, or discuss a Gain asset/profile; compare a draft with Gain standards or live-platform precedent; or learn from expert reviewer feedback. Use the Gain connector or MCP when available and preserve acceptable analyst wording rather than rewriting for novelty.
---

# Gain Profile Review

Review Gain assets as a senior first or final reviewer. Find material factual, analytical, and consistency issues before polishing language. Preserve client-ready analyst work.

## Required references

Read `references/expert-calibration.md` fully for every review.

Use `references/model-context.md` as the authoritative handbook. It is large, so locate relevant sections before reading them:

```bash
rg -n "^## |^### " references/model-context.md
rg -n -i "customer base|sales channel|cash conversion|segmentation|pros and cons" references/model-context.md
```

For a complete Full-profile review, read the targeted sections covering:

- Key Facts and General Consistency.
- Business, Market, Background, and Assessment.
- Reviewing drafted assets and cross-section checks.
- Empirical validation, especially section 21.

Use these references when practical precedent or examples are needed:

- `references/key-facts-consistency-benchmark.md`: structured-field and cross-profile defects from 232 Polish Full profiles.
- `references/profile-benchmark-round-1.md`: initial 54-profile style baseline.
- `references/profile-benchmark-round-2.md`: expanded 103-profile calibration.
- `references/profile-benchmark-round-3.md`: difficult ownership, sector, and Assessment cases.

Treat live profiles as evidence of style and structure, not error-free authority.

## Review workflow

### 1. Retrieve the asset

Prefer lookup by Gain `assetId`. Request only the packages needed, normally:

`business`, `ownership`, `fte`, `deals`, `assessment`, `financials`, `financialRatios`, `growth`, `valuation`, and `competitors`.

State any material visibility limitation. In particular:

- Gain MCP may expose Total revenue while financial segmentations reconcile to Net revenue in Excel.
- Use the Excel `Cash conversion - Capex-based` metric when reviewing that rating. Do not substitute a self-calculated MCP proxy.
- Secondary URLs, parent links, current-investor flags, and some CMS fields may be unavailable.

Do not raise a contradiction solely because an inaccessible Excel/CMS field cannot be reconciled.

### 2. Build an internal consistency table

Compare before drafting findings:

| Topic | Compare |
|---|---|
| Identity | Official name, aliases, group perimeter, URLs, brands/subsidiaries |
| Classification | Short activity, sector/subsector, activity ticks, tags, Business |
| Customers | Direct payer, materiality, Further information, B2B/B2C/B2G ticks |
| Route to market | Revenue model and direct/indirect/online/brick-and-mortar channels |
| Location | Actual headquarters, exact address, Business city/country |
| People | Count, date, perimeter, employees/FTEs, average/period-end, financials |
| Ownership | Type, investors, parent, Background ending, deals, management |
| Origin | Founding year, predecessor/group logic, Background |
| Position | Market wording, sources, competitors, Leader rating |
| Assessment | Financial evidence, ratings, P&C logic, periods, character discipline |

Classify issues as direct contradiction, missing required field, perimeter/convention mismatch, stale field, verification candidate, or mechanical defect.

### 3. Verify material facts

Use the company website, filings, annual reports, reliable transaction sources, and current external research where needed. Verify high-impact claims first:

- Current ownership and TopCo.
- Market share, ranking, and leadership.
- Revenue/FTE datapoints and periods.
- Headquarters and founding year.
- Material P&C statistics.

Attribute company-sourced leadership wording with `claims to be`. Attribution does not rescue an artificially narrow market definition.

### 3A. Escalate consequential gaps with targeted research

Do not repeat the analyst's full research process, but do not treat the drafted profile as a closed evidence set. Run focused external research when an unresolved fact could materially change a required field, profile conclusion, or rating. Typical triggers include:

- The stated revenue model implies a missing B2B, B2C, or B2G payer category.
- The end-user is clear but the direct payer is not, especially in healthcare, education, utilities, infrastructure, defence, and other reimbursed or publicly funded sectors.
- Key Facts and Business are internally consistent but may share the same unsupported assumption.
- A star rating depends on an unverified feature such as contract length, backlog, reimbursement, subscriptions, recurring demand, or regulatory pricing.
- A vague or apparently generic statement could be resolved with a high-value, low-effort source check.

Use a bounded research ladder:

1. Check official company pricing, reimbursement, tender, contract, FAQ, service, and investor pages.
2. Check official government, payer, regulator, insurer, filing, or transaction sources.
3. Use one or two credible secondary sources only when primary evidence is unavailable.
4. Stop once the classification is supportable, the available evidence is exhausted, or further work is unlikely to change the review.

Keep three questions separate: does the route exist, is it likely material, and does it make revenue predictable? A framework agreement, insurer relationship, reimbursement eligibility, or public tariff does not by itself prove guaranteed volumes, contracted revenue, or four-star visibility.

If materiality remains uncertain, report the evidence and uncertainty rather than inventing a payer split. Treat a plausible but unresolved segment as a verification candidate or reviewer-discretion point; make it a critical fix only when evidence shows it is likely material or the existing profile is materially misleading. Ask the expert reviewer a concise question only when targeted research cannot resolve a consequential judgment call.

### 3B. Cite every externally researched finding in place

Every review finding that introduces or relies on information obtained outside the retrieved Gain profile must have a clickable source link directly beneath that finding. This is mandatory for factual corrections, ownership events, portfolio changes, customer shares, market evidence, financial datapoints, calculations, rating challenges, interpretations and proposed replacement text.

Use this format:

```text
- Critical fix: Public-sector customers represent approximately 30% of the customer base.
  Source: [Tången IPO prospectus, p. 18](direct URL)
```

Do not rely on a source list only at the end of the review. Repeat the relevant link beneath each externally researched finding, even when one source supports several findings. Source links belong in the review feedback, not in the proposed Gain profile prose.

Clearly distinguish:

- `Source states`: a fact explicitly reported by the source.
- `Calculation`: a result calculated from sourced figures; show the inputs or short formula.
- `Inference` or `Reviewer judgment`: a conclusion drawn from evidence rather than directly stated.

Do not present an inference as a sourced fact. If the source establishes that some contracts, recurring services, or public frameworks exist but does not quantify their group-wide share, state that limitation and do not claim the current revenue wording or rating is wrong solely on that basis.

### 4. Review Key Facts

Check every observable structured field against the whole profile.

Important distinctions:

- Treat missing useful aliases as reviewer-discretion by default. Escalate only when an alias is factually wrong, points to another business, or creates a material identity/perimeter contradiction.
- Customer type follows the direct payer and approximately 10% materiality threshold.
- A manufacturer selling directly to a distributor or retailer normally uses Direct sales. The reseller is the company's customer.
- Use Indirect sales when an intermediary facilitates the transaction without purchasing the product, such as Steam for game publishers.
- Online requires a material online sales channel, not merely a website.
- Manufacturing requires meaningful in-house production; outsourced production alone does not qualify.
- Include the selected subsector as a tag. Treat other tag additions or cleanup as reviewer-discretion unless a tag is factually wrong, the selected subsector is missing, or the tag set materially misrepresents the business.
- The platform has a limited tag taxonomy. Do not prescribe an exact tag unless its availability is known; otherwise suggest the nearest available concept softly.
- Populate last deal date only for current VC-, PE-majority-, or PE-minority-backed assets, and only from a qualifying deal in which the PE/VC investor itself enters, exits, funds, or changes its ownership stake. Do not update it for an operating-company acquisition, merger, or new management/physician minority shareholders merely because the asset is PE-backed.

### 5. Review prose sections

#### Business

Determine the profile perimeter before reviewing sentence-subject rhythm:

1. A profile containing subsidiaries and/or brands is a Group profile.
2. In a Group profile, alternate the asset name with `the Group` where practical and do not use `the Company` anywhere in the Business text.
3. In a standalone-company profile, alternate the asset name with `the Company` where practical and do not use `the Group`.
4. Do not introduce `it` or `its` merely for variety.

Keep accurate, conventional Gain wording. Rewrite only when inaccurate, inconsistent, incomplete, unsupported, unclear, or materially weaker than an available formulation.

Check identity, group composition, business model, offering, revenue generation, scale KPI, headquarters/FTE, customer exposure, and Market position.

#### Market

Prioritize position, correct market scope, recent evidence, and credible competitors. A company claim may remain attributed. Remove marketing language and feature-only differentiation. Do not add phrases such as `award-winning design` unless the award itself is analytically relevant and the wording remains factual.

#### Background

Confirm founding logic, only necessary ownership events, and a dated current-status sentence naming the actual owners/controller. Do not duplicate structured deals.

Use `remained` when the named ownership has demonstrably continued unchanged since founding or the preceding ownership event, e.g. `As of June 2026, the Company remained solely owned by the Żuk family.` Use `was` for a dated ownership snapshot when continuity is not established or not relevant. Do not mistake a precise `remained [named owner]` statement for the vague and insufficient phrase `remained privately owned`.

#### Assessment

Check ratings one by one against the prescribed periods and Excel metrics. Give recent performance meaningful weight without mechanically replacing the canonical period.

For Pros and Cons:

- Audit every existing point individually before drafting any new arguments. Label them `P1`, `P2`, `P3`, `C1`, `C2`, and `C3` in their submitted order.
- For each existing point, give a verdict: `Keep`, `Improve`, `Replace`, or `Remove`.
- Explain briefly what works and what needs improvement, including factual support, investor relevance, causal logic, specificity, ranking, timeframe, metric identification, and character discipline where applicable.
- When a point is salvageable, propose the smallest necessary edit and preserve its underlying idea. Do not replace it merely because another argument is available.
- Introduce a completely new point only when an existing point is unusable, a slot is blank, or a materially stronger argument should replace a weak lower-ranked point. State clearly which submitted point it replaces and why.
- If no Pros or Cons are populated, state `No existing Pros/Cons to audit` before proposing draft points.
- Preserve a correct, specific, well-ranked original argument.
- Prefer the standard parenthetical evidence style, e.g. `Solid top-line growth (+8% CAGR 2019-2024)`.
- Retain the year or period for every statistic.
- Do not invent causality between two valid facts.
- Use approximately 90-103 characters as the practical target and 90-120 as the outer range when clarity survives.
- Three per side is the default; two strong points may be approved instead of a weak third.

### 6. Deliver the review

Lead with the status and severity definitions, then organize all feedback by profile section. Within each section, present critical fixes before reviewer-discretion points. Use:

Set `Publishable` when no critical fixes remain, even if discretionary suggestions are noted. Set `Publishable after changes` when one or more critical fixes remain but can reasonably be completed in review. Reserve `Return to analyst` for exceptional extensive or unresolvable work.

```text
REVIEW STATUS
- Publishable / Publishable after changes / Return to analyst
- Highest-priority issue
- Critical fix: required before publication because it affects factual accuracy, required completeness, financial logic, ownership, or cross-section consistency.
- Reviewer discretion: optional improvement, interpretive judgment, or stylistic/tag suggestion that does not independently block publication.

KEY FACTS
- Critical fixes
- Reviewer discretion
- State `Pass` when no findings arise.

FINANCIALS
- Critical fixes
- Reviewer discretion
- State visibility limitations for Excel-only fields.

BUSINESS
- Business model text
- Customer base text
- Competitive position text
- Put exact replacement text directly under the relevant finding when warranted.

OWNERSHIP
- Background, current ownership, investors, parent/TopCo, ownership deals and management consistency.

ASSESSMENT
- Pros and Cons: audit every existing P1/P2/P3 and C1/C2/C3 first, with `Keep`, `Improve`, `Replace`, or `Remove`, reasoning and minimal revised wording where needed.
- New candidate arguments only after the existing-point audit, clearly identifying the point or blank slot they replace.
- Rating-by-rating issues

CROSS-SECTION CONSISTENCY
- Include only when contradictions or perimeter/convention issues span sections.

ANALYST FEEDBACK
- Reusable lessons only.
```

Do not create a separate catch-all rewrite section. Do not overwhelm the reviewer with cosmetic alternatives. Clearly label every finding as `Critical fix` or `Reviewer discretion`; tag suggestions are normally discretionary.
Missing aliases and Oxford-comma cleanup are also normally reviewer-discretion. Escalate only when the alias is wrong or materially confuses the profile perimeter, or when punctuation changes meaning.
For every externally researched finding, place its source link immediately below it. A consolidated source list at the end is optional and never substitutes for finding-level sourcing.

## Learning loop

When an expert reviewer corrects the model:

1. Identify whether the error came from missing guidance, contradictory guidance, or failure to apply existing guidance.
2. Update `references/expert-calibration.md` with the concise rule and example.
3. Update `references/model-context.md` only when the handbook itself needs clarification.
4. Preserve the expert's distinction instead of generalizing beyond the case.
5. Re-test on a different asset before treating the rule as stable.

For a shared installation, treat this skill folder as the canonical package. Keep `SKILL.md` and all files under `references/` together when exporting, uploading, copying, or versioning the skill.
