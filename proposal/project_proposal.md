# Project Proposal: Deconstructing Klarna's $40M AI Claim

**Tanya Ojha | MS Analytics, Northeastern University**

---

## Background

In February 2024, Klarna announced that its AI customer service assistant had handled the equivalent of 700 full-time agents in its first month, generating $40M in annual profit improvement. The announcement received widespread coverage and became one of the most-cited examples of enterprise AI ROI.

The claim is specific enough to model but vague enough to warrant scrutiny. Klarna never disclosed ticket-level cost breakdowns, automation rates by ticket type, or a baseline counterfactual. Without those, the $40M figure is essentially unverifiable as stated.

This project builds an independent attribution model using only publicly available data.

---

## Problem Statement

When a company attributes a specific dollar figure to an AI investment, how should that attribution be evaluated? The Klarna case presents three interrelated challenges:

**Attribution ambiguity.** Klarna's 2022 workforce restructuring reduced customer service costs by $47M before the AI assistant launched. Any honest model must account for what costs would have looked like in 2024 without AI.

**Metric selection.** Aggregate cost reduction ($84M over two years) looks different from AI-isolated contribution when restructuring effects are stripped out.

**Projection risk.** The 67% automation rate achieved in month one reflects the easiest ticket types. Assuming that rate holds across years 2-5 overstates long-term value.

---

## Objectives

1. Build a bottom-up value driver model that decomposes Klarna's $40M claim into measurable components
2. Apply counterfactual analysis to isolate AI's contribution from parallel restructuring effects
3. Run a 5-year NPV and IRR model under multiple attribution scenarios
4. Validate model outputs against Klarna's actual disclosed financials where available
5. Quantify uncertainty using a Monte Carlo simulation across 1,000 scenarios

---

## Methodology

**Phase 1: Data Collection and Assumptions**
Compile all publicly available data from Klarna's F-1 SEC filing, annual reports, press releases, and third-party coverage. Document every assumption with source and confidence level.

**Phase 2: Value Driver Decomposition**
Break down the $40M figure into individual drivers: labor efficiency (automation rate x agent headcount x average salary), repeat inquiry reduction (25% confirmed by Klarna), capacity unlock (avoided hiring during 20% volume growth), and resolution speed efficiency.

**Phase 3: Counterfactual Construction**
Model two counterfactual scenarios. CF1: the 2023 cost reduction trend continues at $47M/year without AI. CF2: costs flatten at $240M without AI. Apply each to estimate AI's isolated contribution.

**Phase 4: Financial Modeling**
Build a 5-year discounted cash flow model with NPV, IRR, simple payback, and ROI. Run three attribution scenarios: skeptical ($15M AI contribution), base case ($25M), and Klarna's stated ($40M).

**Phase 5: Monte Carlo Simulation**
Identify the five key input variables (automation rate, labor cost, productivity gain, revenue uplift, implementation cost) and assign probability distributions. Run 1,000 simulations to generate expected NPV and probability that NPV exceeds zero.

**Phase 6: Reality Check**
Compare model predictions against Klarna's actual 2024 outcomes as reported in the F-1 filing and Q1 2025 earnings. Flag where the model was right, wrong, and directionally correct.

---

## Scope and Limitations

This model uses only publicly disclosed data. Klarna has never disclosed ticket-level cost breakdowns, automation rates by ticket type, or internal headcount data beyond what appears in annual reports. Estimates are directional, not precise.

The model explicitly acknowledges five data gaps and their impact on output confidence. The goal is not a definitive figure but a defensible range with transparent assumptions.

---

## Deliverable

A single Excel workbook with 13 sheets covering the full analysis, from raw assumptions through Monte Carlo output, with an executive memo summarizing findings for a non-technical reader.

---

## Tools

Microsoft Excel (financial modeling, Monte Carlo simulation, scenario analysis, waterfall chart)

---

## Timeline

Solo project, completed over approximately 3 weeks.
