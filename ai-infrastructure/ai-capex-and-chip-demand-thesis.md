# AI Capex & Chip Demand — A Differentiated Thesis

**Question:** Will demand for GPUs and memory chips keep *soaring beyond expectations*, given the
trillion-dollar AI capex wave?

**Built:** 2026-06-02, from a 14-angle parallel research sweep (briefs + sources in
[`research-briefs.md`](./research-briefs.md)).
**Method note:** facts tagged **[C]** confirmed (filings / multi-source) vs **[R]** rumored
(single-source, channel-check, or model estimate). Treat every multi-year "commitment" dollar
figure as a marketing envelope until it shows up as a booked order.

---

## 1. The one-paragraph call

**Yes — demand keeps soaring *through 2026*, but the consensus is right for reasons that
contain its own undoing, and it is mispricing three things.** (1) The binding constraint has
already flipped from *capital* to *physical* — power, transformers, HBM, advanced packaging —
so the "soaring" now shows up in **price and backlog, not deployed units**. That rationing is
*bullish near-term* (it sustains pricing power) and *bearish medium-term* (it defers a supply
wave into 2027–28 exactly as the monetization and depreciation reckonings arrive). (2) The
cleanest "beyond expectations" leg is **memory, not GPUs** — and within memory, the *conventional
DRAM* cannibalization is the under-priced move, while *Nvidia's share* of accelerators is the
quietly *eroding* one. (3) The whole edifice is not a diversified web but a **hub-and-spoke bet on
OpenAI**; the thing that breaks the cycle is not a demand cliff but a *financing/ROI event at the
hub*, transmitted through circular financing and a depreciation re-rating. **Net positioning
instinct: long the rationed physical bottleneck, skeptical of the financially-engineered demand
layer.**

---

## 2. Where we agree with the Street — and where we depart

The consensus is a **tight cluster**, which is itself the opportunity:

| Dimension | Crowded consensus | Our stance |
|---|---|---|
| 2026 hyperscaler capex | ~$600–805B (+36–83% YoY) **[C]** | **Agree.** Every spender raised guidance in the Apr–May '26 prints; no major cut. |
| 2027 capex | ~$1.0–1.15T **[C]** | Agree on the number, **disagree it's "safe"** — it's increasingly *debt*-funded. |
| Nvidia | PT $275–320, all Buy (tight ~15% band) **[C]** | **Long the demand, question the monopoly.** Share erosion is the unpriced risk. |
| Memory | Structural shortage to 2027–28 **[C]** | **Agree, and it's the highest-conviction "beyond expectations" leg** — plus a sleeper in commodity DRAM. |
| The real debate | Bulls = durable secular buildout; bears = accounting/financing mirage | **Both are arguing the wrong axis.** See §3. |

**The key meta-finding:** bulls and bears use *nearly identical capex inputs*. The entire fight is
*downstream interpretation*. So the contrarian edge is **not** "capex will be lower" — it's the
**bridges everyone assumes hold**.

---

## 3. The four unpriced bridges (this is the differentiated core)

Consensus prices AI capex as if four conversions are frictionless. Each is leakier than modeled.

### Bridge 1 — capex → *merchant GPU/HBM* revenue mix
The Street reads "$700B capex" straight through to Nvidia + the HBM big-3. But the *mix* is
shifting under the headline:
- **ASIC growth is inverting GPU growth:** custom-silicon unit growth **+44.6% vs merchant GPU
  +16.1%** in 2026 (~3:1) — first year ASICs out-grow GPUs **[C, TrendForce]**. *But* installed
  base is still ~70% GPU / ~28% ASIC → **growth-rate inversion ≠ share inversion** (the headline
  most people get wrong, in *both* directions).
- TPU has gone **merchant** (Meta to rent in '26, buy in '27; Anthropic up to 1M TPUs) — breaking
  the "ASICs are captive, not a real Nvidia competitor" axiom **[C/R]**.
- Anthropic is **training frontier models on >1M Trainium2** — the training socket, not just
  inference — undercutting the "GPUs keep training, ASICs only nibble inference" comfort **[C]**.
- Nvidia is **relaxing Rubin HBM4 specs** (22→~20 TB/s, accepting lower pin-speed bins) because
  suppliers can't hit target — ASP/margin risk hiding under "sold out" **[R]**.

→ **Even in a high-capex world, Nvidia's revenue read-through can disappoint if mix rotates to
ASICs / networking / inference-optimized faster than priced.** Almost nobody models this scenario.

### Bridge 2 — committed backlog → *durable end demand*
The "many independent deals" web is really a **single concentrated bet wearing six costumes**:
- ~$300B of Oracle's ~$523–553B RPO is **OpenAI (~54%)** **[C]**; CoreWeave anchored by
  MSFT (~67%) + OpenAI **[C/R]**; Nvidia committed **up to $100B + a fresh $30B to OpenAI** and
  **backstops CoreWeave's unsold capacity to 2032 ($6.3B)** **[C]**.
- Nvidia is **funding its own demand**: >$40B of equity into AI customers in 2026 alone **[C]** —
  the Lucent/Nortel vendor-financing pattern that amplified the 2000 telecom bust.
- The hub burns: OpenAI ~$1.4T commitments vs ~$13–20B revenue, ~$74B projected operating loss in
  2028; it **already cut its own compute pledge $1.4T→$600B** and abandoned a Stargate UAE
  expansion **[C/R]**.

→ **Counterparty risk is not diversified — it's hub-and-spoke on one pre-profit entity.** Watch
OpenAI funding above all else.

### Bridge 3 — booked depreciation → *true economics*
- Hyperscalers/neoclouds depreciate GPUs over **5–6 yrs**; Burry argues 2–3 yrs → **~$176B
  understated depreciation 2026–28**, Oracle/Meta op-income >20% inflated **[R, his model]**.
- The most damning evidence isn't Burry — it's **Amazon already *shortened* to 5yr (citing AI
  pace) in the very quarter Meta *lengthened* to 5.5yr** **[C]**. Two sophisticated operators,
  identical hardware, opposite calls → the estimate is a **management lever, not an engineering
  fact.**
- The killer analogy: **dark fiber held option value for ~20 years; dark GPUs do not** (2–3yr
  obsolescence). So the AI build is *more* fragile to a demand pause than telecom — the opposite
  of the "better collateral" comfort.
- Nuance (where the bears overreach): Azure ran V100s ~7.5yrs; true economic life is probably
  **~4–5yr, not 2–3** — bad for reported EPS, *not* zero-recovery collateral.

→ **The same companies issuing record debt are likely reporting inflated operating income that
services it.** A single hyperscaler shortening useful-life in a 10-Q re-rates the group.

### Bridge 4 — shortage → *durable pricing*
- Memory is genuinely sold out (SK Hynix HBM **sold out ~3 yrs**; HBM4 12-Hi ~$500/stack,
  +60–70% vs HBM3E) **[C]**, and capex is **disciplined** (+11–23%), not a 2018-style blowout
  **[C]** — the bullish tell.
- **But** the same dynamic creates a *bifurcated* market: an AI/HBM **shortage** coexisting with a
  China/CXMT-driven **commodity DRAM/NAND glut** (DDR5 undercut ~10%, DDR4 ~50%) **[C/R]**. A
  single "memory cycle" thesis is wrong.
- "Memflation" (DRAM ASPs +125%) is **demand-destroying** for phones/PCs, and one quarter of HBM
  allocation cancellation flips "shortage" → "glut" — the classic memory whipsaw nobody models.

→ **Memory soars hardest *and* is the most cyclically fragile.** It's the best "beyond
expectations" trade *and* the one most likely to crack first.

---

## 4. The physical bottleneck stack (why "soar" means price, not units)

Demand can't soar *in deployed terms* because deployment is physically gated. The chokepoints,
deepest-to-shallowest:

1. **Transformers / GOES steel** — large-transformer lead times **128–144 wks, up to 4 yrs**;
   **Cleveland-Cliffs is the *only* US producer of grain-oriented electrical steel** → single
   point of failure, no clean pure-play. *The most under-appreciated bottleneck.* **[C]**
2. **Power / grid** — gas turbines (GE Vernova, Siemens Energy) **sold out into 2029–30**; PJM
   capacity prices **~10×** YoY; first AI nuclear electrons not until 2027, SMRs 2030+. EPA's
   **Jan-2026 closure of the behind-the-meter gas permitting loophole** just made the favored
   bridge pricier. **[C]**
3. **HBM4 + conventional DRAM** — each HBM wafer eats **~3 commodity DRAM wafers**; the logic
   base die is now a **TSMC foundry product** (TSMC is *in the HBM critical path*). **[C/R]**
4. **Advanced packaging (CoWoS → SoIC)** — "wafers" is the wrong unit: Rubin's ~5.5× reticle
   yields only **4–7 GPUs per carrier wafer**; **SoIC is the real next ceiling** at ~10× smaller
   than CoWoS. N2 pricing came in **+10–20%, not the feared +50%**. **[C/R]**
5. **ABF substrate** — projected shortfall 10%→21%→42% (2026→28); choke runs up to glass-cloth /
   copper foil. **[R]**
6. **EML lasers / optics** — Nvidia locked up **$4B (Coherent + Lumentum)**, pushing rivals'
   lead times past 2027; contrarian read: **CPO *deepens* the EML moat, doesn't kill it.** **[C/R]**

→ **The "soaring" is real but it manifests as pricing power and multi-year backlog at the
bottlenecks, not as a units-deployed melt-up.** And every one of these chokepoints implies a
**deferred supply wave in 2027–28**.

---

## 5. The efficiency question (does cheaper compute kill demand?)

The decisive, non-obvious finding: **two price curves coexist.** Per-token cost for a *fixed
capability* falls ~10×/yr, **but the cost to run the *frontier* rises ~18×/yr** (Epoch) **[C]**.
Token volume is going vertical (Google: ~480T → **3.2 quadrillion** tokens/mo YoY; OpenRouter
~100T/mo) **[C]**, with **reasoning/agentic workloads now >50% of tokens** (10–100× tokens/query).
DeepSeek did *not* cut spend — capex *accelerated* after it **[C]**.

- **Jevons holds for now** — but on *token* elasticity, which is enormous, not *value* elasticity,
  which is unproven.
- **The crack (this quarter):** Uber and Microsoft **blew through 2026 token budgets in months**;
  JPMorgan: "token costs are eating internet profits alive." **[C/R]** → a *willingness-to-pay
  ceiling* the token-volume charts hide.

→ **Token growth ≠ revenue growth ≠ profit growth.** The frontier curve (rising 18×/yr) sustains
high-end hardware intensity; the risk is the value ceiling, not a demand cliff.

---

## 6. Memory vs GPUs — the differentiated read

- **Memory = highest-conviction "soar beyond expectations."** Supply discipline is real, HBM is
  sold out multi-year, *and* the second-order commodity-DRAM cannibalization is under-priced.
  Cleanest beneficiaries: SK Hynix, Micron, Samsung (turnkey HBM4 edge under-credited). *Caveat:*
  most cyclically fragile — soars then whipsaws.
- **GPUs / accelerators = total demand soars, Nvidia's *share* is the question.** "Long the
  demand, question the monopoly." Total accelerator TAM is durable (backlog, GW commitments,
  inference scaling); Nvidia's near-monopoly is the eroding part (ASIC inference substitution,
  customer concentration ~64% of receivables in 3 names, spec relaxation).
- **The picks-and-shovels nobody crowds:** transformers/GOES, EML lasers, power gear — rationed
  pricing power with *real cash flow*, vs the debt-funded demand layer.

---

## 7. Time-phased view: soar, then whipsaw

- **2026 — Soar (high confidence).** Capex up, memory sold out, bottlenecks rationing supply →
  pricing power intact, "beyond expectations" mostly in *price/revenue*. The bottleneck is
  electrons and HBM, not willingness to spend.
- **2027–28 — Whipsaw risk (medium).** The deferred supply wave (transformers, turbines, new HBM
  fabs, CoWoS/SoIC) arrives *just as* (a) the monetization gap (~$800B–$2T revenue needed) bites,
  (b) depreciation re-rates, (c) circular-financing fragility is tested, and (d) commodity-memory
  glut leaks upward. **GPUs don't hold option value like fiber did** → a sharper down-leg if a
  demand pause hits.

---

## 8. Scenarios (subjective)

| Scenario | Prob | What it looks like |
|---|---|---|
| **Rationed melt-up** (base) | ~50% | Demand soars through 2026 in price/backlog; supply gates units; memory leads; mix quietly rotates toward ASICs. |
| **Hub event** | ~25% | OpenAI funding/ROI stumble cascades: Oracle RPO markdown → CDS → SPV lenders → CoreWeave covenants → Nvidia backstop drawdown. Demand "disappears" via financing, not end-users. |
| **Clean secular bull** | ~15% | Value-elasticity holds, monetization catches capex, Nvidia defends share — consensus is simply right, no whipsaw. |
| **2027–28 overbuild bust** | ~10% | Deferred supply + glut + depreciation reckoning = telecom-style down-leg, worsened by GPU obsolescence. |

---

## 9. What we'd actually do (value-capture, repo-style)

Not advice — research positioning angles to pressure-test next:
- **Prefer the rationed physical chokepoints with real cash** (memory oligopoly; power /
  transformer / GOES; EML / optics) **over** the financially-engineered demand layer (neoclouds,
  OpenAI-dependent backlog).
- **"Long the demand, question the monopoly":** own accelerator-TAM growth without assuming Nvidia
  holds 70%+ share — pair vs. ASIC enablers (Broadcom/Marvell) and watch the share line.
- **Memory: ride it, but keep a hand on the exit** — it's the best beyond-expectations leg and the
  first to whipsaw. The conventional-DRAM cannibalization is the sleeper.
- **Hedge the hub:** the cheapest tail risk to track is anything keyed to OpenAI funding /
  circular-financing stress (Oracle CDS, CoreWeave spreads).
- **Avoid mistaking backlog for demand and EBITDA for cash** in the neocloud complex.

---

## 10. Dated watchlist / tripwires

Theses live or die on catalysts. Watch:

- **OpenAI funding / ROI** — any down-round, the floated govt backstop, or further pledge cuts =
  hub crack. *(The single most important variable.)*
- **GPU useful-life** — a *second* hyperscaler following Amazon to shorten depreciation in a 10-Q
  → validates Burry, re-rates the group.
- **GPU rental rate** — H100 1-yr back below ~$1.70/hr (the Oct-25 low) = oversupply re-asserting.
  (Rebounded to ~$2.35 in Mar-26.)
- **Mix rotation** — Nvidia DC share slipping below ~75% faster than guided; Meta's 2027 TPU
  *purchase* (vs rent) converting; Broadcom backlog >$73B and a 7th custom customer.
- **Memory whipsaw** — conventional DRAM contract prices: still doubling QoQ = cannibalization
  confirmed; a roll-over = pull-forward. CXMT HBM3 mass-production order placed (or slips to 2027).
- **HBM specs** — further Nvidia Rubin down-binning = ASP pressure under "sold out."
- **Physical supply** — GE Vernova / Siemens slot-reservation *conversion* rate (first place an
  AI-capex slowdown shows); transformer lead times; EPA NSPS (xAI) litigation.
- **Circular financing** — Oracle FCF/CDS (>150bps sustained); a failed neocloud SPV syndication;
  Nvidia disclosing rising revenue to equity-investee customers.
- **Demand-at-a-price** — more enterprises capping token budgets (after Uber/Microsoft); Anthropic
  S-1 (filed 2026-06-01) net-revenue-retention — first audited look at enterprise AI stickiness.

---

## 11. Confidence & what would change our mind

- **High:** capex still surprising up through mid-2026; bottleneck has flipped capital→physical;
  memory is the strongest beyond-expectations leg; ASIC growth-rate inversion is real.
- **Medium:** the hub-fragility / 2027–28 whipsaw call (well-supported but a forward, timing-
  dependent judgment); Nvidia-share erosion magnitude.
- **Would flip us more bullish:** value-elasticity proven (token budgets stop binding; AI product
  gross margins turn durably positive), Nvidia defends share, OpenAI reaches a credible funding /
  profitability path.
- **Would flip us bearish *now*:** a hyperscaler cuts capex guidance or uses "digestion" language;
  an OpenAI funding wobble; a second useful-life shortening; conventional-DRAM prices roll over.

---

### Sources
Full per-angle findings with inline citations are in
[`research-briefs.md`](./research-briefs.md). Headline corroboration spans company filings/8-Ks
(Nvidia, AMD, Microsoft, Meta, Alphabet, Oracle, CoreWeave, SK Hynix, Micron), Morgan Stanley,
Goldman Sachs, BofA, Citi, JPMorgan, Bernstein, SemiAnalysis, TrendForce, Gartner/IDC, Epoch AI,
CBRE, CSIS, and primary trade press. Facts are dated to the Q1-2026 (calendar) earnings cycle
(late Apr–May 2026), the most recent available as of 2026-06-02.

*Built from a 14-agent parallel research sweep. Separate confirmed from rumored; this is a
thesis to attack, not a conclusion to trust.*
