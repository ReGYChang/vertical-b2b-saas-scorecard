---
name: vertical-b2b-saas-scorecard
description: >
  Evaluate vertical B2B SaaS project ideas and companies from a VC investment perspective,
  covering macro-to-micro PMF validation across 6 dimensions: market structure, vertical moat,
  PMF signals, SaaS unit economics (ARR multiples, CAC/LTV, NRR, Logo retention), team-market fit,
  and capital efficiency. Use this skill whenever someone wants to validate a B2B SaaS idea,
  assess product-market fit for a vertical SaaS product, score a SaaS startup for investment,
  analyze SaaS metrics like ARR/NRR/CAC/LTV, evaluate whether a vertical software idea is
  fundable, or run a due-diligence-style assessment on a SaaS company. Also trigger when
  users mention "PMF validation", "vertical SaaS", "SaaS investment thesis", "SaaS scorecard",
  "is my SaaS idea viable", or "evaluate my startup idea".
---

# Vertical B2B SaaS Investment Scorecard

A structured, weighted scoring framework for evaluating vertical B2B SaaS projects — from
early-stage idea validation through growth-stage investment assessment. Designed to work as
both a founder's PMF self-check and a VC-grade due diligence tool.

The framework moves **macro → micro**: market structure first, unit economics last. This
ordering is intentional — a perfect NRR means nothing if the market ceiling is $200M.

## When to Use This Skill

1. **Idea validation**: Founder says "I want to build X for Y industry" — run the full
   scorecard to surface structural risks before writing code.
2. **PMF assessment**: Product exists but unclear if PMF is real — focus on Dimensions C & D
   to diagnose.
3. **Investment screening**: Evaluating a vertical SaaS company — run all 6 dimensions for
   a comprehensive score.
4. **Self-audit**: Existing SaaS company wants to benchmark itself — compare against the
   stage-appropriate benchmarks in `references/benchmarks.md`.

---

## Evaluation Workflow

### Step 1: Gather Context

Before scoring, collect the following. Ask the user for what they have; infer or flag gaps.

**Required inputs:**
- What vertical/industry does the product serve?
- What specific workflow or pain point does it address?
- Who is the buyer (title, department, budget authority)?
- Current stage (idea / pre-revenue / post-revenue / scaling)?
- Any existing metrics (ARR, customer count, churn, NRR, CAC)?

**Nice-to-have:**
- Competitive landscape (who else serves this vertical?)
- Regulatory or compliance context
- Pricing model and ACV
- Founding team background

If the user only has an idea (no metrics), score Dimensions A-C fully and provide
directional guidance on D-F with benchmark targets they should aim for.

### Step 2: Score Each Dimension

Score each dimension 1-10 using the rubrics in `references/scoring-rubrics.md`.
Read that file before scoring — it contains the detailed criteria for each score level.

### Step 3: Calculate Weighted Score

| Dimension | Weight | What It Measures |
|-----------|--------|------------------|
| **A. Market Structure & TAM** | 20% | Addressable market size, growth, vertical concentration |
| **B. Vertical Moat & Defensibility** | 20% | Switching costs, data network effects, regulatory barriers |
| **C. PMF Signals & Demand** | 20% | Evidence of pull vs push, adoption velocity, retention shape |
| **D. SaaS Unit Economics** | 20% | ARR, NRR, Logo retention, CAC/LTV, payback, Rule of 40 |
| **E. Team–Market Fit** | 10% | Domain expertise, GTM capability, technical depth |
| **F. Capital Efficiency & Exit Path** | 10% | Burn multiple, path to profitability, exit comparables |

**Weighted Score = Σ (Dimension Score × Weight)**

### Step 4: Apply Verdict Thresholds

| Score | Verdict | Interpretation |
|-------|---------|----------------|
| 8.5–10.0 | 🟢 **Strong PMF / Strongly Investable** | Structural advantages across all dimensions |
| 7.0–8.4 | 🟡 **Emerging PMF / Investable with Conditions** | Core thesis is sound; specific risks to mitigate |
| 5.5–6.9 | 🟠 **Pre-PMF / Watch** | Promising elements but critical gaps; revisit in 6 months |
| < 5.5 | 🔴 **No PMF / Pass** | Structural issues unlikely to resolve with iteration alone |

### Step 5: Check One-Vote Vetoes

These conditions trigger an automatic 🔴 **Pass** regardless of total score:

1. **TAM ceiling < $1B** in serviceable market (too small for venture-scale returns)
2. **NRR < 85%** for 2+ consecutive quarters (leaky bucket — value destruction)
3. **Logo retention < 70%** annually (product is not sticky; churn is structural)
4. **Single-customer concentration > 40%** of revenue (existential dependency)
5. **No identifiable buyer** with budget authority (vitamin, not painkiller)
6. **Regulatory prohibition or imminent disruption** that eliminates the category

If a veto triggers, note it prominently and explain why it overrides the score.

### Step 6: Generate the Report

ALWAYS use this output structure:

```
# [Company/Idea Name] — Vertical B2B SaaS Scorecard

## Executive Summary
One paragraph: verdict, score, top strength, top risk, and recommended action.

## Scoring Breakdown

### A. Market Structure & TAM — [X/10] (20%)
[Assessment with evidence]

### B. Vertical Moat & Defensibility — [X/10] (20%)
[Assessment with evidence]

### C. PMF Signals & Demand — [X/10] (20%)
[Assessment with evidence]

### D. SaaS Unit Economics — [X/10] (20%)
[Assessment with evidence or benchmark targets if pre-revenue]

### E. Team–Market Fit — [X/10] (10%)
[Assessment with evidence]

### F. Capital Efficiency & Exit Path — [X/10] (10%)
[Assessment with evidence or directional analysis]

## Weighted Score: [X.X / 10] — [Verdict Emoji + Label]

## Veto Check
[Pass / which vetoes triggered, if any]

## PMF Stage Assessment
[Current stage + what evidence would advance to next stage]
See references/pmf-stages.md for the full stage framework.

## Key Risks & Mitigations
Top 3 risks ranked by severity, each with a concrete mitigation path.

## Recommended Next Steps
3-5 actionable items prioritized by impact, tailored to the current stage.
```

---

## Dimension Summaries

Below are condensed guides for each dimension. For full scoring rubrics with per-level
criteria (1-2, 3-4, 5-6, 7-8, 9-10), read `references/scoring-rubrics.md`.

### A. Market Structure & TAM (20%)

Evaluates whether the vertical is large enough, growing fast enough, and structured
favorably for a SaaS entrant.

Key factors:
- **TAM/SAM/SOM reality check** — Bottom-up calculation preferred over top-down.
  Vertical SaaS TAMs are often smaller than horizontal; $1-5B is a healthy range.
  Below $1B triggers the veto unless the vertical is a wedge into adjacencies.
- **Market growth rate** — Is the vertical itself growing (secular tailwind) or
  static? Regulatory mandates that force digitization are strong tailwinds.
- **Fragmentation vs concentration** — Highly fragmented buyers (many SMBs) favor
  PLG/self-serve; concentrated buyers (few enterprises) favor outbound sales.
- **Spend migration** — Is budget currently locked in legacy systems, manual
  processes, or spreadsheets? Greenfield is better than displacement.

### B. Vertical Moat & Defensibility (20%)

Vertical SaaS lives or dies by switching costs. Unlike horizontal tools, vertical
products embed themselves in industry-specific workflows that are painful to replace.

Key factors:
- **Workflow integration depth** — Does the product become the system of record?
  Deeper embedding = higher switching costs.
- **Data network effects** — Does the product accumulate proprietary data that
  improves with usage? Industry benchmarks, compliance records, pricing data.
- **Regulatory/compliance moat** — Does operating in this vertical require
  certifications, audits, or regulatory approvals that raise barriers?
- **Ecosystem lock-in** — Integrations with vertical-specific hardware, ERPs,
  or industry platforms that create multi-product dependency.
- **Horizontal competitor insulation** — How hard is it for Salesforce, HubSpot,
  or a general-purpose tool to replicate vertical-specific features?

### C. PMF Signals & Demand (20%)

The most judgment-intensive dimension. Distinguishes real pull from manufactured push.
Read `references/pmf-stages.md` for the full PMF stage framework.

Key signals of real PMF:
- **Organic inbound** — Customers finding you without paid acquisition
- **Short sales cycles** — Relative to the vertical's norm
- **Expansion without prompting** — Users adding seats/modules on their own
- **High NPS / active referrals** — Customers recruiting other customers
- **Retention shape** — Flat or smiling curve after initial onboarding period

Red flags (fake PMF):
- Growth driven entirely by founder's personal network
- Deep discounting to close deals
- Heavy customization per customer (consulting disguised as SaaS)
- High logo acquisition but immediate churn after onboarding

### D. SaaS Unit Economics (20%)

The quantitative core. For pre-revenue companies, this section becomes a benchmark
target map. For post-revenue, it's a health check.

Read `references/benchmarks.md` for stage-specific benchmark tables.

Key metrics and what "good" looks like for vertical B2B SaaS:

| Metric | Good | Great | Veto Trigger |
|--------|------|-------|--------------|
| NRR (Net Revenue Retention) | >100% | >115% | <85% |
| GRR (Gross Revenue Retention) | >85% | >92% | <75% |
| Logo Retention (annual) | >85% | >90% | <70% |
| LTV:CAC Ratio | >3:1 | >5:1 | <1.5:1 |
| CAC Payback (months) | <18 | <12 | >30 |
| Gross Margin | >70% | >80% | <50% |
| Rule of 40 | >40% | >60% | — |
| ARR Growth (YoY) | >50% | >100% | — |

**ARR multiples context** (for valuation sanity-check):
- Early-stage vertical SaaS: 10-20x ARR (high growth, pre-profit)
- Growth-stage: 8-15x ARR (proven PMF, path to efficiency)
- Mature: 5-10x ARR (stable growth, profitable)
- Distressed/declining: 2-4x ARR

These multiples compress significantly in risk-off markets. Always compare to
public vertical SaaS comps (Veeva, Toast, Procore, ServiceTitan, Clio).

### E. Team–Market Fit (10%)

For vertical SaaS, domain expertise is disproportionately important. The best
vertical SaaS founders have "lived the pain" — they come from the industry they serve.

Key factors:
- **Domain credibility** — Has the founder worked in the vertical? Do they have
  a network of potential early customers who trust them?
- **Technical capability** — Can the team build the product, or are they dependent
  on outsourced development?
- **GTM understanding** — Do they know how this vertical buys software? Trade
  shows, associations, referral networks, channel partners?
- **Regulatory literacy** — If the vertical is regulated, does the team understand
  compliance requirements firsthand?

### F. Capital Efficiency & Exit Path (10%)

Vertical SaaS companies can be capital-efficient because they serve concentrated
markets with high willingness-to-pay. But the exit universe is different from
horizontal SaaS.

Key factors:
- **Burn multiple** — Net burn / net new ARR. <2x is efficient; >3x is concerning.
- **Path to profitability** — Vertical SaaS should reach profitability earlier than
  horizontal because of lower CAC and higher retention.
- **Exit comparables** — Strategic acquirers (PE, industry incumbents, platform
  companies) vs IPO. Vertical SaaS is a natural PE target due to predictable cash flows.
- **Platform expansion potential** — Can the wedge product expand into adjacent
  workflows to grow TAM? (e.g., Toast: POS → payments → lending → payroll)

---

## Adapting to User Context

**If the user has only an idea (no product/metrics):**
- Score A, B, C, E fully based on market research and team background.
- For D, provide benchmark targets per stage instead of actual scores.
- For F, provide directional analysis based on comparable exits.
- Frame the output as "validation scorecard" — what must be true for this to work.

**If the user has early traction (some customers, partial metrics):**
- Score all dimensions but flag where data is insufficient.
- Compare available metrics against stage-appropriate benchmarks.
- Emphasize the PMF stage assessment and what evidence would level-up confidence.

**If the user has mature metrics (post-Series A):**
- Full quantitative scoring across all dimensions.
- Include valuation context (ARR multiples, comparable transactions).
- Provide growth vs efficiency trade-off analysis.

**Language preference:**
- If the user writes in Chinese, respond in Traditional Chinese (繁體中文).
- If the user writes in English, respond in English.
- Always keep metric names in English (ARR, NRR, CAC, LTV) for precision.

---

## Reference Files

Read these files for detailed scoring criteria and benchmarks:

- `references/scoring-rubrics.md` — Detailed per-dimension scoring rubrics with
  criteria for each score level (1-2, 3-4, 5-6, 7-8, 9-10). **Read before scoring.**
- `references/benchmarks.md` — Stage-specific benchmark tables for vertical B2B SaaS
  metrics, ARR multiple ranges, and public comp data.
- `references/pmf-stages.md` — PMF stage definitions (Pre-PMF → Emerging → Strong →
  Scaling) with signal checklists and advancement criteria.
