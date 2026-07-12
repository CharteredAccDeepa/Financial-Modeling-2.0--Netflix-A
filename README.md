# Netflix, Inc. — Three-Statement Financial Model & DCF Valuation

An independent, equity-research-style financial model for Netflix (NASDAQ: NFLX), built from the FY2025 10-K as a self-paced project to move from Controllership/accounting into FP&A/financial analysis.

**[Download the model](./Netflix_Financial_Model_v2.xlsx)**

---

## Why I built this

I'm a Chartered Accountant working in financial accounting/controllership, transitioning toward FP&A and financial analyst roles. Reconciling historical numbers and forecasting a business forward are genuinely different skills, and I wanted a project that would force me to build the second one — not just read about it.

This is that project. It's a full three-statement model with a live scenario engine, a sourced set of assumptions, and a documented audit trail of my own mistakes and how I found them.

**On AI use:** I built this with Claude (Anthropic) as a modeling partner — for structure, formula design, and catching my own errors — because I was learning the mechanics of financial modeling as I went, not because I already knew them. I can walk through every assumption, every formula, and every fix in this model, and I'd rather say that upfront than have it come up in an interview. My next project is building a reusable modeling template from what I learned here.

---

## What's in the model

- **Live scenario engine** — a single dropdown (Worst / Neutral / Best) drives every tab: revenue by region, cost ratios, working capital, debt, and the DCF. Changing it recalculates the entire model.
- **Fully linked three-statement output** — Income Statement, Balance Sheet, and Cash Flow Statement, FY2026E–FY2030E, built up from FY2023A–FY2025A actuals.
- **Sourced assumptions** — every driver (regional revenue growth, cost of revenue, opex ratios, tax rate, working capital) is tied to language in the 10-K MD&A where Netflix discloses it, or explicitly flagged as an analyst estimate where it isn't.
- **DCF valuation** — CAPM-based WACC, unlevered free cash flow, Gordon Growth terminal value, and an implied share price compared to the market.
- **Native Excel charts** — Revenue, Cost of Revenue, Operating Expenses, Operating Income, Net Profit, and Operating Margin, each plotted across all three scenarios at once.
- **A self-audit log** — I ran a structured integrity check on my own model and found real errors: a 2.5-point mismatch between my stated and actual 2025 Cost of Revenue ratio, a depreciation assumption that was off by 3x, and an interest rate that didn't match my own debt schedule. All are documented and fixed in the `Checks` tab, including what the fix changed in the output (net income moved ~9% once corrected).

## Methodology note: why this is revenue-driven, not subscriber-driven

Netflix stopped disclosing subscriber/membership counts starting with the FY2025 10-K, stating that revenue and operating margin are now its primary reported performance metrics. This model follows that same approach — regional revenue growth rather than subscriber count × ARPU — consistent with how Netflix itself now reports.

## Tab guide

| Tab | Purpose |
|---|---|
| `Cover` | Summary, methodology, and how-to-use guide |
| `Model Control` | Master scenario switch + single-point operating drivers |
| `Assumptions` | Every scenario-driven driver, with sourced rationale (Worst/Neutral/Best) |
| `P&L Input` / `Balance Sheet Input` / `CFS Input` / `Revenue Modelling` / `Other Items` | FY2023A–FY2025A historicals, sourced to the 10-K |
| `Schedules` / `Debt` | Supporting historical reconciliations |
| `Proj Drivers` / `Proj Schedules` | Scenario-resolved drivers and forward rollforwards |
| `Projected PnL` / `Projected BS` / `Projected CFS` | The linked three-statement forecast |
| `Checks` | Balance sheet, cash, and cross-tab integrity checks, plus the audit log |
| `Chart Data` / `Charts` | All three scenarios computed in parallel, and the charts built from them |
| `WACC` / `DCF` | Cost of capital and valuation |

## Skills this demonstrates

Three-statement modeling · scenario/sensitivity analysis · DCF valuation · working-capital modeling · data integrity auditing · Excel formula architecture (dynamic scenario switching via `CHOOSE`/`MATCH`) · financial statement analysis from 10-K filings

## Limitations (stated honestly)

- Market inputs (share price, beta) are point-in-time as of July 2026 and would need refreshing for live use.
- Share buybacks are held flat in dollar terms across scenarios — a simplification, not a scenario-sensitive forecast.
- Diluted share count in the DCF is static and doesn't reflect share count reduction from ongoing buybacks.
- This is an educational/portfolio exercise, not investment advice.

**Source:** Netflix, Inc. Form 10-K for fiscal year ended December 31, 2025 (SEC accession 0001065280-26-000034, filed January 23, 2026).

---

*Built by CADeepa — [LinkedIn](https://www.linkedin.com/in/deepa-rani-675334339/)*
