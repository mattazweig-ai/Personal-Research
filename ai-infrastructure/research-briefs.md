# AI Capex & Chip Demand — Research Briefs (Appendix)

Condensed findings from a 14-angle parallel agent sweep, 2026-06-02. Each brief = key facts +
consensus + where we diverge + sources. **[C]** confirmed / **[R]** rumored. Synthesis lives in
[`ai-capex-and-chip-demand-thesis.md`](./ai-capex-and-chip-demand-thesis.md).

---

## 1. AI capex trajectory (demand side)

**Verdict: still surprising to the upside.** Every major spender RAISED 2026 guidance in the
Apr–May '26 prints; the bottleneck flipped from "will they spend" to "can they power it."

- Microsoft ~$190B CY26 (beat ~$155B consensus by ~$35B) **[C]**; Amazon ~$200B **[C]**; Alphabet
  $175–185B (funded via $80B equity offering + >$85B debt) **[C]**; Meta $125–145B (raised) **[C]**;
  Oracle ~$50B FY26, RPO $523–553B, FCF ~−$24.7B **[C]**; CoreWeave $31–35B, backlog $99.4B **[C]**.
- Big-5 2026 ≈ $650–725B (Goldman ~$725B). Morgan Stanley: 2026 ~$805B, **2027 ~$1.1T** (both
  raised) **[C]**. Goldman 2025–27 cumulative ~$1.15T (>2× 2022–24) **[C]**.
- AI-lab commitments (envelopes, not bookings): OpenAI/Stargate ~$1.4T; Anthropic ~$600B 5-yr,
  paying xAI $1.25B/mo **[R]**.
- Counter-signals: MSFT ~200MW lease cancellations (early-25 vintage); 30–50% of 2026 US DC
  capacity delayed/cancelled — **for power/transformers, not demand** **[C]**.

Sources: CNBC/MSFT Q1; Global Datacenter Hub; Yahoo/Amazon; Constellation/Alphabet; SEC FWP;
Fortune/Meta; SEC 8-K; Investing.com/Oracle RPO; CoreWeave IR; Phemex & FXStreet/Morgan Stanley;
goldmansachs.com; CNBC/Stargate guide; TechCrunch/Anthropic-xAI; DCD/MSFT leases.

---

## 2. GPU / accelerator demand durability

**Verdict: total demand soars; Nvidia's *share* is what erodes.**

- Nvidia Q1 FY27 (ended Apr 26 '26): rev $81.6B, **Data Center $75.2B (+92% YoY)**; Q2 guide
  **$91B** (above consensus), ~75% GM, assumes **zero China**. **$500B Blackwell+Rubin visibility**,
  "gotten larger." Rubin HVM H2-26. **[C]**
- AMD DC $5.8B (+57%); MI350/355X volume; Meta up to **6 GW** AMD Instinct. **[C]**
- ASICs: TPU v7 Ironwood + Anthropic (up to 1M chips/5GW); Trainium3 shipped; Maia 200; OpenAI
  +Broadcom 10GW. **ASIC unit growth +44.6% vs GPU +16.1%** in 2026 (~3:1) **[C/R]**.
- Inference now ~⅔ of compute. Some bears: Nvidia inference share 90%→20–30% by 2028 (aggressive)
  **[R]**.

Sources: Nvidia 8-K/StockTitan; Futurum; AMD 8-K; TechTimes & TrendForce/ASIC; Tom's Hardware;
VentureBeat/Anthropic-Google; Deloitte.

---

## 3. Power & grid bottleneck

**Verdict: real ceiling, but backlogs/queues are inflated — bullish near-term, softer than priced.**

- Transformer lead times **128–144 wks, up to 4 yrs**; **Cleveland-Cliffs = only US GOES producer**
  (single point of failure) **[C]**.
- GE Vernova ~100 GW backlog+reservations Q1-26, "sold out through 2030" by YE26; Siemens Energy
  ~€136–146B backlog **[C]**.
- PJM capacity cleared **$329/MW-day vs $28.92** prior (~10×); data centers = 40% of 2027/28
  auction **[C]**.
- **EPA closed the behind-the-meter gas permitting loophole (Jan 16 '26)**; xAI sued over Colossus
  turbines **[C]** — raises cost of the 2026–28 bridge.
- Interconnection queue ~2,060 GW but ~80% withdraw; NERC 90 GW DC forecast contested as
  double-counted (Grid Strategies) **[C/R]**. Slot reservations ≠ firm orders.

Sources: industrialsage, pv-magazine-usa, powermag; utilitydive (GEV, PJM, NERC); enlit/Siemens;
power-eng; encinoenviron & federalregister & earthjustice/EPA; emp.lbl.gov; latitudemedia/TD Cowen.

---

## 4. HBM4 supply (swing factor)

**Verdict: real swing factor is *conventional* DRAM; TSMC now in the HBM critical path.**

- Each HBM wafer ≈ **3 commodity DRAM wafers**; HBM4 yields ~50–60% vs DDR5 ~70% **[R/physics]**.
  AI/HBM ~20% of global DRAM wafer capacity in 2026; conventional DRAM +55–110% QoQ **[C]**.
- SK Hynix HBM **sold out ~3 yrs**; Q1-26 op margin ~72% **[C]**. Micron contradiction: SemiAnalysis
  says out of year-1 Rubin **[R]** vs Micron's own "CY26 HBM sold out, ramps Q2-26" **[C]**.
- **Logic base die → foundry product:** SK Hynix outsources to TSMC (weighing 3nm for HBM4E);
  Samsung uses own 4nm (only fully vertical) **[C/R]**.
- **Nvidia relaxing Rubin HBM4 specs** (22→~20 TB/s, ~10.6 Gbps) — suppliers missing bins **[R]**.
- HBM4 12-Hi ~$500/stack (+60–70% vs HBM3E) **[C]**. HBM4 stays on **microbumps** (hybrid bonding
  slips to HBM4E/HBM5, ~2028+) — so HB-yield fears are a 2028 story **[C]**.

Sources: TrendForce (multiple); SK Hynix PR/Seoul Economic Daily; Micron FQ1-26; Digitimes;
semiengineering; siliconanalysts.

---

## 5. Advanced packaging / CoWoS

**Verdict: "wafers" is the wrong unit; bottleneck migrates CoWoS-S → CoWoS-L → SoIC.**

- TSMC CoWoS: ~35–40K/mo (24) → ~75–80K (25) → 120–130K (26) → 160–170K (27, MS) **[C-ish]**.
- Nvidia >60% of CoWoS, >70% of CoWoS-L; reportedly booked ~800–850K wafers for 2026 **[C/R]**.
- **Rubin ~5.5× reticle → only ~4–7 GPUs per carrier wafer** → wafer growth overstates unit growth
  **[C]**. The 2025 "60% utilization scare" was a CoWoS-S→L mix shift, not a downturn **[C]**.
- **SoIC is the real next ceiling** (~10K/mo vs CoWoS ~80K) **[C]**. ABF substrate shortfall
  10%→21%→42% (26→28) **[R]**. **N2 +10–20%, not feared +50%** **[C]**. US onshore packaging
  (Amkor AZ) not until ~2028 **[C]**.

Sources: TrendForce; FinancialContent/WRAL; Morgan Stanley via futunn; design-reuse/SoIC; Digitimes/ABF;
Tom's Hardware/Amkor.

---

## 6. Custom ASIC substitution

**Verdict: growth-rate inversion is real; share inversion is not (yet). Training breach under-rated.**

- TPU v7 Ironwood GA Apr-26 (inference-first); Anthropic up to 1M TPUs/5GW; **TPU gone merchant**
  (Meta rent-26/buy-27) **[C/R]**. Broadcom AI backlog **$73B**, Q1 FY26 AI rev $8.4B (+106%),
  "line of sight" >$100B AI rev 2027 **[C]**.
- Amazon Trainium3 shipped Dec-25; Anthropic trains on **>1M Trainium2** (training, not just
  inference) **[C]**. Maia 200 launched but delayed/laggard **[C]**. MTIA: 4 gens in 2 yrs **[C]**.
- Counterweight: Nvidia GB300 fastest ramp ever; Huang says ASICs "harder to deploy than expected";
  Nvidia ships its own inference ASIC (Rubin CPX) **[C]**.

Sources: DCD/Google-Anthropic; thenextweb; oplexa/Broadcom; Anthropic/AWS; MSFT blog; about.fb.com;
Futurum/Marvell; nvidianews.

---

## 7. Inference efficiency shocks

**Verdict: two price curves coexist; risk is value-elasticity, not token-elasticity.**

- Fixed-capability cost **−10×/yr** but **frontier cost +18×/yr** (Epoch) **[C]**.
- Google tokens 480T→**3.2 quadrillion/mo** YoY; OpenRouter ~100T/mo; **reasoning >50% of tokens**
  (10–100× per query) **[C]**. DeepSeek did *not* cut spend — capex accelerated **[C]**.
- Crack: Uber & Microsoft **blew 2026 token budgets in months**; JPMorgan "token costs eating
  internet profits" **[C/R]**. Open-weight Chinese models ~13% (peak 30%) of routed tokens cap the
  price floor **[C]**.

Sources: Epoch/arXiv; TECHi & TechStartups/tokens; a16z/OpenRouter; Tom's Hardware/Goldman; TechCrunch/DeepSeek.

---

## 8. Enterprise AI ROI reality

**Verdict: demand accelerating, but token growth ≠ revenue ≠ profit; cost-side reckoning emerging.**

- OpenAI ~$24–25B run-rate (Apr-26, ~$2B/mo); **Anthropic $47B run-rate (May-26)**, S-1 filed
  Jun-1 **[C]**. Microsoft AI **$37B run-rate (+123%)**, 20M+ Copilot seats (~3–4% penetration)
  **[C]**.
- Revenue gap: Bain ~$2T needed by 2030 (~$800B short); Sequoia gap → $500–600B **[C]**.
- OpenAI: ~$25B loss 2026, cash-positive not until 2029–30 **[C]**.
- **MIT "95% of pilots no ROI" is widely misread** — measures custom internal builds; Wharton shows
  ~75% positive returns on off-the-shelf tools. Value accrues to *vendors*, not most *buyers*.
- AI product gross margins ~52% vs 80% SaaS; agentic inference scales with usage (inverts cost
  curve) **[C/R]**.

Sources: Sacra/OpenAI; simonwillison/Anthropic; CNBC/S-1; GeekWire/MSFT; Bain; CNBC/capex; The
Information/Fortune/OpenAI losses; Fortune/MIT; BusinessWire/Wharton; SoftwareSeni/margins.

---

## 9. Circular / vendor financing web

**Verdict: not diversified — hub-and-spoke on OpenAI; marginal dollar is now debt.**

- Nvidia: up to **$100B + fresh $30B to OpenAI**; >$40B AI equity in 2026; **backstops CoreWeave
  unsold capacity to 2032 ($6.3B)** **[C]**.
- OpenAI ~$1.4T commitments vs ~$13–20B rev; ~$74B projected op-loss 2028 **[C]**. Oracle: ~$300B
  of RPO is OpenAI (~54%); FCF −$13.2B Q2 FY26; $18B bonds; CDS ~139bps **[C]**.
- Off-balance-sheet: Meta-Blue Owl Hyperion $27–30B (Meta owns 20%); ~$120B AI debt moved
  off-book **[C]**. Meta $30B bond (record $125B book) **[C]**. Morgan Stanley: ~$1.5T external
  financing gap, ~$800B private credit **[C]**.
- Risk transferred to retirement savers via Apollo/Athene, Blue Owl, PIMCO **[C]**.

Sources: TechCrunch/Nvidia equity; SEC 8-K/CoreWeave; TechCrunch & Fortune/OpenAI; SEC/Oracle;
Meta IR & Cryptopolitan; PitchBook & Janus Henderson; Morgan Stanley; Apollo.

---

## 10. GPU depreciation accounting

**Verdict: Amazon-shortens-while-Meta-lengthens is the real tell; dark GPUs ≠ dark fiber.**

- MSFT 4→6yr (2022, ~$3.7B FY23 benefit); Google →6yr (~$3.9B saved); **Meta →5.5yr (Jan-25,
  −$2.9B deprec) while Amazon SHORTENED 6→5yr citing AI pace** — opposite calls, identical
  hardware **[C]**.
- Burry: real life 2–3yr → **~$176B understated deprec 2026–28**; Oracle ~26.9%, Meta ~20.8% by
  2028 **[R, his model]**. Nvidia rebuttal (A100s "still at full tilt"); Burry: straw man **[C]**.
- H100 rental $7–8 → $1.70 low (Oct-25) → ~$2.35 (Mar-26) **[C]**. Used H100 SXM ~$40K→$6–15K;
  value decay accelerates after ~24 mo **[C]**. Llama-3 405B run: ~9% annualized GPU failure **[C]**.

Sources: Register & Computer Weekly/MSFT; DCD/Google; Yahoo & DeepQuarry/Meta-Amazon; CNBC &
Benzinga/Burry; American Bazaar/Nvidia memo; Silicon Data & Introl; hashrateindex; arXiv 2503.11901.

---

## 11. Neocloud unit economics

**Verdict: collateral, revenue, and borrowing base are the *same asset*; bond mkt ≠ equity mkt.**

- CoreWeave Q1-26: rev $2.08B (+112%), **net loss −$740M**, interest **$536M/qtr** (2× YoY); total
  debt ~**$24.9B** at ~11% blended; capex $31–35B **[C]**.
- Loans **GPU- and contract-collateralized** (novel); public bonds **9.25–9.75%** (junk) **[C]**.
- Concentration: MSFT ~67% of CoreWeave; Lambda ~62% MSFT; Nebius better diversified **[C/R]**.
- 6yr depreciation is the load-bearing assumption; H100 rental already crashed 64% once **[C]**.
- Nuance: Burry's 2–3yr too harsh (Azure ran V100s ~7.5yr) → ~4–5yr truer **[C]**.

Sources: CNBC & SEC 8-K/CoreWeave; Motley Fool; DCD/bonds; Sacra/Lambda; SEC 6-K/Nebius;
DeepQuarry; Axios/Crusoe (RUMORED valuations flagged).

---

## 12. Sovereign AI demand

**Verdict: real but grossly over-headlined; authorization ≠ delivery; partly double-counted.**

- Only audited proxy: Nvidia sovereign **>$20B FY25 (~10% of rev)** **[C]**.
- Korea **260K GPUs / $9.8B by 2030** (MOU, *not binding*); Saudi HUMAIN 18K GB300 confirmed,
  "several hundred thousand" RUMORED; UAE/G42 — US approved ~500K chips/yr but **G42 can buy only
  ~35K GB300-equiv now** vs 5GW "vision" **[C]**.
- Europe weakest vs rhetoric (€20B gigafactory call delayed twice); India tiny (~$1.25B) **[C]**.
- **OpenAI cut compute pledge $1.4T→$600B and abandoned Stargate UAE expansion** **[R]**. Biden AI
  Diffusion Rule rescinded (~May-26) **[C]**.

Sources: Motley Fool/Nvidia; KED Global & White House/Korea; DCD & PRNewswire/HUMAIN; Malay Mail &
The National/UAE; STL Partners & Nvidia/Europe; DD News/India; TechTimes/OpenAI cut; DCD/Diffusion.

---

## 13. Historical overbuild analogs

**Verdict: dark fiber held option value ~20yr; dark GPUs don't — *more* fragile than telecom.**

- Fiber: >$500B (96–01), **<5% ever lit, ~85% dark by 2005**; WorldCom/Global Crossing **[C]**.
  Rails: Panic of 1893, ~25% of US railroads failed **[C]**.
- Contradiction: CBRE vacancy **record-low 1.4%** + preleasing mid-70s **[C]** *and* 30–50% of 2026
  capacity delayed/cancelled (supply-side) **[C]**.
- H100 rental crash→rebound is the cleanest real-time gauge (not flashing red now) **[C]**.
- **Phantom load:** speculative interconnection 5–10× real builds; **ERCOT queue 63→226 GW** (~75%
  DC) **[C]**. Enterprise GPU idle ~95% ("$401B problem") **[C, enterprise-specific]**.

Sources: thebubblebubble; Wikipedia/telecoms-crash & dark-fibre & Panic-1893; mises.org; CBRE;
techspot; Silicon Data & Introl; utilitydive & latitudemedia/phantom load; VentureBeat; hashrateindex.

---

## 14. Analyst consensus map (the benchmark)

**Verdict: a tight cluster — bulls & bears use near-identical capex; the fight is downstream.**

- **2026 Big-5 capex ~$600–805B** (MS high $805B; →~$1.0–1.15T 2027) — most consensus number on the
  Street **[C]**.
- **NVDA targets cluster $275–320, all Buy** (~15% band): Bernstein $275, JPM/Morningstar $280,
  Citi/others $300, BofA $320 **[C]**.
- **Memory shortage to 2027–28** unanimous (Gartner, TrendForce, GS, BofA, SemiAnalysis); Micron
  $840 (Citi), SK Hynix PT +94% (GS) **[C]**.
- AI ~30% of a $1.3T semi market 2026 (Gartner/IDC) **[C]**.
- Bull tail: Ives (NVDA $6T '27), Wells Fargo ("buy the euphoric bubble"). Bear tail: Burry (short
  NVDA, $176B deprec), Chanos ("own the chip magic, short the landlords"), MIT (95% no ROI).
- **Shared blind spots (the contrarian ground):** (1) capex→merchant-chip revenue is linear;
  (2) backlog = durable (not circular) demand; (3) 5–6yr depreciation is real; (4) shortage =
  durable pricing (not a whipsaw); (5) power arrives on schedule; (6) Nvidia holds share+margin.

Sources: Morgan Stanley IM & FXStreet; goldmansachs.com & Benzinga; 247WallSt/BofA; Yahoo &
TradingKey/Citi; TheStreet/JPM; Fortune & 247WallSt/Wells Fargo; Benzinga/Bernstein;
Morningstar; DigitalToday & SemiAnalysis; TrendForce; Gartner; IDC; Yahoo/Ives; Yahoo & CNBC/Burry;
Acquirer's Multiple/Chanos; Fortune/MIT.

---

*Several primary trade sources (TrendForce, SemiAnalysis, Digitimes, Tom's Hardware) intermittently
returned 403 to direct fetch; figures from those were taken via search-engine summaries and should
be re-verified against the primary article before acting on any single number. Directional
conclusions are corroborated across ≥2 independent sources.*
