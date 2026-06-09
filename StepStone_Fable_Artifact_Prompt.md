# BUILD PROMPT — StepStone SPW Buyout & Fee-Stream Refinancing (interactive artifact)

> **Paste this whole file into a Claude (Fable) chat.** It is a build instruction + embedded data. Claude: build the artifact described in "WHAT TO BUILD" using ONLY the data in "DATA" below. Do not fetch anything external. All figures are from StepStone Group (NASDAQ: STEP) primary SEC filings FY2022–FY2026, the Nov-2022 Option Agreement (Exhibit 10.1), earnings releases/calls, and fund prospectuses. Treat estimates as labeled.

---

## WHAT TO BUILD
A single-file, self-contained **interactive React artifact** — a clean, professional "deal dashboard" (institutional/finance aesthetic, neutral palette, no external assets) titled **"StepStone Private Wealth — Buyout Liability & Fee-Stream Refinancing Model."** Use 4 tabs:

**Tab 1 — The Liability Over Time.**
- A line/area chart of the contingent liability carrying value by quarter (Dec-2022 → Mar-2026), with a secondary line for SPW AUM and a labeled marker where the disclosed max-settlement series sits.
- Toggle to overlay the discount rate and adjusted trading multiple per period.
- Callout: "Immaterial through FY2024 → inflected Dec-2024 → $2.27B by FY2026."

**Tab 2 — Buyout Price Calculator (the formula).**
- Sliders: (a) SPW pre-tax earnings base $ (range $40M–$220M, default $198M), (b) StepStone trading multiple "P/ANI" (range 12x–32x, default 21x), (c) Applicable Sale % (50–100%, default 100%), (d) blended tax rate (default 22.6%).
- Compute and display: Purchase Multiple = min(20, 0.70 × P/ANI); Gross Purchase Price = base × (1−tax) × Sale% × Purchase Multiple; subtract ~$18.6M seed → Net.
- Show two reference markers: **Floor ≈ $564M** (recurring-fee base ~$50M) and **Ceiling ≈ $2,258M** (with-performance base ~$198M). Headline: "The carried $2,266M sits at the performance-PEAK; normalized base → ~$564M floor."
- A small stacked bar showing the earnings base split: ~$50M recurring fees vs ~$83M one-time SPRING incentive fee vs the rest.

**Tab 3 — The Fee-Stream Refinancing (the proposed solution) + sizing.**
- A simple flow diagram (boxes/arrows, drawn with divs/SVG): Investor (us) → SPV "the box" (rated notes) → cash → StepStone → pays Founders (CH) cash → CH exits; StepStone remits a 20-yr SPW management-fee slice → SPV → debt service.
- Sizing model with sliders: SPW AUM now ($B, default 15), annual AUM growth/runoff % (−10% to +25%, default +8%), pledged management-fee rate (bps on AUM, default 70bps = ~half of ~1.36% to reflect the sub-advisory split / pledged slice), term (default 20 yrs), PV discount rate (default 9%), advance rate (default 70%).
- Compute: projected annual pledged fees = AUM(t)×rate; PV over term; **Notes raised = PV × advance rate**; show whether Notes ≥ target buyout amount (default target = the Tab-2 Net), the DSCR (pledged fees ÷ level debt service), and residual fees retained by StepStone.
- Output card: "Fundable? ✔/✖", sources & uses, and a sensitivity note.

**Tab 4 — Accounting: Before vs After (StepStone).**
- Two side-by-side columns (Before / After) from the table in DATA. Emphasize: liability-classified $2.27B comp award → GONE; replaced by non-recourse, rated SPV debt (consolidated gross under ASC 810, like their existing $3.1B CFO); IG/3.5x covenant preserved; no equity dilution.
- A short "accounting characterization" note: monetizing FUTURE fees = secured borrowing (ASC 470-10 sale-of-future-revenue), NOT a true sale; SPV likely consolidated (StepStone = VIE primary beneficiary).

UX: tasteful, dense-but-readable, tooltips citing the source line, a persistent footer with the three caveats. No login, no backend, everything client-side.

---

## DATA (use these exact values)

```json
{
  "liabilityOverTime": [
    {"date":"2022-12","label":"Q3 FY23","carryingUSDm":3.8,"discountRate":null,"multiple":null,"maxSettlementUSDm":null,"spwAUM_USDb":1.0},
    {"date":"2024-03","label":"FY24 end","carryingUSDm":28.3,"discountRate":null,"multiple":null,"maxSettlementUSDm":null,"spwAUM_USDb":3.4},
    {"date":"2024-09","label":"Q2 FY25","carryingUSDm":70.8,"discountRate":null,"multiple":null,"maxSettlementUSDm":70.8,"spwAUM_USDb":5.0},
    {"date":"2024-12","label":"Q3 FY25","carryingUSDm":554.3,"discountRate":0.38,"multiple":null,"maxSettlementUSDm":544.2,"spwAUM_USDb":6.3},
    {"date":"2025-03","label":"FY25 end","carryingUSDm":663.9,"discountRate":0.34,"multiple":20.0,"maxSettlementUSDm":661.1,"spwAUM_USDb":8.2},
    {"date":"2025-06","label":"Q1 FY26","carryingUSDm":841.7,"discountRate":0.30,"multiple":18.6,"maxSettlementUSDm":838.1,"spwAUM_USDb":10.0},
    {"date":"2025-09","label":"Q2 FY26","carryingUSDm":1712.9,"discountRate":0.30,"multiple":20.0,"maxSettlementUSDm":1708.8,"spwAUM_USDb":12.0},
    {"date":"2025-12","label":"Q3 FY26","carryingUSDm":2165.6,"discountRate":0.31,"multiple":20.0,"maxSettlementUSDm":2084.1,"spwAUM_USDb":13.0},
    {"date":"2026-03","label":"FY26 end","carryingUSDm":2265.8,"discountRate":0.27,"multiple":14.7,"maxSettlementUSDm":2257.6,"spwAUM_USDb":16.0}
  ],
  "annualExpenseUSDm": {"FY23":8.6,"FY24":22.9,"FY25":651.8,"FY26":1720.9},
  "cashSettledUSDm":   {"FY24":3.1,"FY25":16.2,"FY26":118.8},
  "settlementRangeFY26USDm": {"min":564.4,"max":2257.6,"carrying":2265.8},
  "buyoutFormula": {
    "grossPurchasePrice":"[ (2 x AdjustedAdviserANI_6mo) + (0.60*CurrentYrIncentiveFees + 0.40*PriorYrAnnual + 1.00*PriorYrQuarterly) - tax ] x ApplicableSalePct x PurchaseMultiple",
    "purchaseMultiple":"min(20, PercentageFactor * SSG_Multiple); PercentageFactor=0.70 if SSG>=20x",
    "SSG_Multiple":"StepStone P/ANI = 10-day VWAP / LTM ANI",
    "taxRateFY26":0.226,
    "referenceSeedUSDm":18.638,
    "fy26_inputs":{"adjTradingMultiple":14.7,"discountRate":0.27,"impliedPretaxBase_max_USDm":198.0,"impliedPretaxBase_min_USDm":49.6}
  },
  "profitInterestAttributableUSDm": {"FY24":3.1,"FY25":23.2,"FY26":136.2},
  "fy26_PI_split_USDm": {"recurringFRE":53,"oneTime_SPRING_incentive":83},
  "note_on_51pct":"'51%' = 136.2 / 264.6 after-tax ANI = 51.5% ARTIFACT, not CH ownership. CH's actual % is undisclosed (unfiled LLC agreement).",
  "spwFundFees": [
    {"fund":"SPRIM","mgmtFeePct":1.40,"incentive":"none","netAssetsUSDb":5.27},
    {"fund":"SPRING","mgmtFeePct":1.50,"incentive":"15% of net profits","netAssetsUSDb":3.34},
    {"fund":"STRUCTURE","mgmtFeePct":1.60,"incentive":"none","netAssetsUSDb":0.76},
    {"fund":"STPEX","mgmtFeePct":1.60,"incentive":"none","netAssetsUSDb":0.78},
    {"fund":"SCRED","mgmtFeePct":1.15,"incentive":"10% of NII","netAssetsUSDb":1.02},
    {"fund":"PrivateCreditLLC","mgmtFeePct":1.00,"incentive":"partly waived","netAssetsUSDb":1.86}
  ],
  "spwBlendedMgmtFeePct":1.36,
  "spwRecurringFRE_estUSDm":{"low":57,"mid":75,"high":100},
  "subAdvisorySplitNote":"Flagship funds (SPRIM/SPRING/STRUCTURE) mgmt fee shared ~50/50 with a sub-adviser; StepStone-retained could be ~half.",
  "valuationMultiples": [
    {"date":"2024-03","priceUSD":35.74,"econShares_m":112.5,"mktCapUSDm":4021,"ttmFRE_USDm":189.8,"P_FRE":21.2,"ttmANI_USDm":139.4,"P_ANI":28.8},
    {"date":"2025-03","priceUSD":52.23,"econShares_m":118.7,"mktCapUSDm":6202,"ttmFRE_USDm":312.2,"P_FRE":19.9,"ttmANI_USDm":244.1,"P_ANI":25.4},
    {"date":"2025-09","priceUSD":65.31,"econShares_m":122.0,"mktCapUSDm":7968,"ttmFRE_USDm":328,"P_FRE":24.3,"ttmANI_USDm":248,"P_ANI":32.1},
    {"date":"2026-03","priceUSD":47.72,"econShares_m":122.2,"mktCapUSDm":5831,"ttmFRE_USDm":354.4,"P_FRE":16.5,"ttmANI_USDm":264.6,"P_ANI":22.0},
    {"date":"2026-06-02","priceUSD":46.07,"econShares_m":122.2,"mktCapUSDm":5629,"ttmFRE_USDm":354.4,"P_FRE":15.9,"ttmANI_USDm":264.6,"P_ANI":21.3}
  ],
  "balanceSheetFY26": {
    "recourseDebtUSDm":270.6, "cashUSDm":213.1, "netRecourseDebtUSDm":57.5, "netLeverageX":0.16,
    "covenantMaxNetLeverageX":3.5, "seniorNotes":"$175M 5.52% due Oct-22-2029","revolver":"$300M due May-16-2029",
    "nonRecourseConsolidatedFundDebtUSDm":931.2, "rating":"Moody's-rated, low-IG (exact notch not public)"
  },
  "existingCFO": {
    "name":"Structured Solutions Vehicle for Private Market Secondaries (a CFO/CFE)","closed":"2026-03-31",
    "commitmentsUSDb":3.1,"notesUSDm":931.2,"seniorUSDm":736.9,"seniorRatePct":7.59,"seniorMaturity":"April 2041",
    "subUSDm":194.3,"addlCapacityUSDm":1396.8,"liquidityFacilityUSDm":408.4,
    "parties":"Ares (primary capital), Barings Portfolio Finance (anchored rated debt), Citi (structuring/placement), Alter Domus (admin agent)",
    "rated":"privately rated (no public grade)","recourse":"non-recourse; consolidated as VIE"
  },
  "accountingBeforeAfter": {
    "Profits-interest liability":["$2,266M, marked-to-market through P&L","Settled & derecognized — gone"],
    "GAAP volatility":["~$1.7B/yr comp swings; -$6.78 EPS FY26","Eliminated"],
    "Equity dilution":["up to 75% stock to CH","None — founders paid cash"],
    "Balance sheet":["accrued compensation","Non-recourse rated SPV debt (consolidated, gross)"],
    "Recourse leverage / IG":["<0.2x; IG","Preserved (notes non-recourse, outside 3.5x covenant)"],
    "Fee income":["100% retained","Gross fees minus 20-yr debt service; residual retained"]
  }
}
```

---

## SIZING MODEL (implement this logic in Tab 3)
1. `AUM(t) = AUM0 * (1+growth)^t` for t = 1..term.
2. `pledgedFees(t) = AUM(t) * pledgedFeeRate` (rate as decimal, e.g. 0.0070 for 70 bps).
3. `PV = Σ pledgedFees(t) / (1+discountRate)^t`.
4. `notesRaised = PV * advanceRate`.
5. `fundable = notesRaised >= targetBuyout` (default targetBuyout = Tab-2 Net Purchase Price).
6. `levelDebtService = notesRaised * (discountRate)/(1-(1+discountRate)^-term)` (annuity); `DSCR = pledgedFees(1) / levelDebtService`.
7. Show sources & uses: Uses = buyout + reserves(default 3%) + fees(default 1.5%); Sources = notesRaised (+ any StepStone cash plug).
Default target buyout: let the user pick between **Floor ($564M)**, **Carried ($2,266M)**, or the Tab-2 computed Net.

---

## CAVEATS (show in footer)
1. The **~$2.27B is a performance-PEAK ceiling**; on a recurring-fee base the obligation maps toward the **~$564M floor** (FY26's $136.2M "profit share" was ~$83M one-time SPRING incentive fee + ~$53M recurring).
2. **CH's actual ownership % and SPW standalone ANI are NOT disclosed** (in the unfiled Adviser LLC Agreement). The "51%" cited in press = $136.2M ÷ firm ANI artifact, not an ownership stake.
3. Accounting reality: monetizing future fees is a **secured borrowing (ASC 470-10), not a true sale**, and the SPV is **likely consolidated (ASC 810 VIE)** — so it's non-recourse rated debt on-balance-sheet, not off-balance-sheet. Two press traps to ignore: the wrong "$722.8M Q2 net loss" (actual –$575.5M / –$366.1M) and the German "The Stepstone Group" B2/B credit ratings (different company).

*All values are point-in-time and partly estimated where labeled; this is an analytical model, not investment advice.*
