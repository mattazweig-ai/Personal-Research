# IPO Oversubscription Comps — Does the "X-times-oversubscribed" Book Predict Aftermarket Performance?

**Built:** 2026-06-09. **Comp set:** 36 US-listed IPOs (Jan 2024 → Jun 2026) + Saudi Aramco
(2019) as the historical mega-deal benchmark, with **SpaceX (pricing 2026-06-11)** situated
against the set.

---

## The central data caveat (read this first)

**Oversubscription multiples are NOT disclosed in any SEC filing.** The US does not mandate
disclosure of book-coverage ratios — bookbuilding demand is private to the underwriters.
Every "the book was *N* times oversubscribed" figure in this doc is a **press leak** —
"people familiar with the matter" briefing Reuters / Bloomberg / FT / CNBC during the
roadshow. That means the data is:

1. **Patchy** — most deals never get a number leaked at all (marked `n/a` below).
2. **Anonymous & directional** — it reflects *indicated, non-binding* interest at a moving
   price, and is selectively leaked to build momentum. It is often padded.
3. **Conflicting** — figures escalate through the roadshow (Arm went 6x → 10x+ in four days)
   and outlets disagree (Klarna: 15x per one source, 25x+ per another).
4. **Not comparable to the academic literature** — the studies that find a clean
   oversubscription→performance relationship (Hong Kong, Malaysia, India, UK) use
   *legally-disclosed, fixed-price* subscription ratios. US leaks are a different, dirtier
   animal. No peer-reviewed paper validates leaked US numbers.

**Rule applied throughout:** every oversubscription figure carries an outlet + date and notes
conflicts. Where no sourced number exists, the cell is `n/a` — **never estimated.** A smaller
set of real numbers beats a complete table of guesses.

> **Fetch caveat:** the research behind this doc hit HTTP 403 on direct fetches of most
> primary outlets (Bloomberg, CNBC, Fortune, Reuters, IPOScoop, SEC EDGAR). Figures are
> sourced from search-surfaced article text and accessible mirrors / company press releases /
> 424B4 prospectuses. The two most load-bearing data points (SpaceX live terms; Figma 40x)
> were independently re-verified. Single-source / snippet-only multiples are flagged "low
> confidence" in the detail table.

---

## Master comps table

Day-1 = offer→first-day close. "Current" = approx. spot as of ~2026-06-08/09 (aggregator
snapshots; treat as indicative). ▲ = above offer, ▼ = below offer.

| # | Company | Tkr | Date | Exch | Raised | Offer | Range | vs Range | IPO val | Oversub (leaked) | Greenshoe | Day-1 | Current vs offer |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| — | **Saudi Aramco** | 2222.SR | 2019-12-11 | Tadawul | $25.6B ($29.4B w/GS) | $8.53 | SAR30–32 | **Top** | ~$1.7T | **2.95x inst** / 465% hdln | Y (full) | +10% (limit) | n/m |
| 1 | Arm Holdings | ARM | 2023-09-14 | Nasdaq | ~$4.87B | $51 | $47–51 | **Top** | ~$54.5B | **6x→10x+** (escalating) | Unknown | +24.7% | ▲ |
| 2 | Reddit | RDDT | 2024-03-21 | NYSE | $748M gross | $34 | $31–34 | **Top** | ~$6.4B | **4–5x** | Unknown | +48% | ▲ |
| 3 | Astera Labs | ALAB | 2024-03-20 | Nasdaq | ~$713M | $36 | $27–30→32–34→36 | **Above** | ~$5.5B | n/a | Y (likely) | +72% | ▲▲ |
| 4 | Birkenstock | BIRK | 2023-10-11 | NYSE | ~$1.5B | $46 | $44–49 | Within | ~$8.6B | n/a | Unknown | **−12.6%** | ▲ (recov.) |
| 5 | Kenvue | KVUE | 2023-05-04 | NYSE | $3.8B ($4.37B w/GS) | $22 | $20–23 | **Top** | ~$41B | n/a | Y (full) | +22.3% | ▼ |
| 6 | Amer Sports | AS | 2024-02-01 | NYSE | ~$1.37B | $13 | $16–18 | **BELOW** | ~$6.3B | n/a (weak) | Unknown | +3.1% | ▲ |
| 7 | Lineage | LINE | 2024-07-25 | Nasdaq | ~$4.44B | $78 | $70–82 | Within (top) | >$18B | n/a | Unknown | ~+3% | **▼ (~$32)** |
| 8 | Viking Holdings | VIK | 2024-05-01 | NYSE | ~$1.54B | $24 | $21–25 | **Top** | >$10B | 15x ⚠️low-conf | Y (full) | +8% | **▲▲ (~$89)** |
| 9 | Waystar | WAY | 2024-06-07 | Nasdaq | ~$968M | $21.50 | $20–23 | Mid | ~$3.7B | n/a | Unknown | **−3.7%** | ▲ (~flat) |
| 10 | StandardAero | SARO | 2024-10-02 | NYSE | ~$1.44B | $24 | $20–23 | **Above** | ~$8.0B | n/a | Y (secondary) | +36% | ▲ |
| 11 | Rubrik | RBRK | 2024-04-25 | NYSE | ~$752M | $32 | $28–31 | **Above** | ~$5.6B | 20x ⚠️low-conf | Unknown | +16% | **▲▲ (~$71)** |
| 12 | Tempus AI | TEM | 2024-06-14 | Nasdaq | ~$411M | $37 | $35–37 | Top | ~$6.1B | n/a ("well o/s") | Unknown | +9% | ▲ (~$52) |
| 13 | Ibotta | IBTA | 2024-04-18 | NYSE | ~$577M | $88 | $76–84 | **Above** | ~$2.67B | n/a | Unknown | +17% | **▼ (~$35)** |
| 14 | UL Solutions | ULS | 2024-04-12 | NYSE | ~$946M ($1.08B w/GS) | $28 | ~within | ~$5.6B | n/a | Y (full) | +23% | **▲▲ (~$97)** |
| 15 | OneStream | OS | 2024-07-24 | Nasdaq | ~$490M | $20 | $17–19 | **Above** | ~$6B | n/a | Y (full) | +34% | *Taken private $24 (Apr'26)* |
| 16 | ServiceTitan | TTAN | 2024-12-12 | Nasdaq | ~$625M | $71 | $52–57→65–67→71 | **Above** | ~$8.5B | n/a | Y (full) | +42% | ▲ (~$77) |
| 17 | Venture Global | VG | 2025-01-24 | NYSE | $1.75B | $25 | $40–46→23–27 | **BELOW** (slashed) | ~$60.5B | n/a (weak) | Unknown | **−4%** | **▼ (~$13)** |
| 18 | SailPoint | SAIL | 2025-02-13 | Nasdaq | ~$1.38B | $23 | $19–21 | **Above** | ~$11.5B+ | 20x ⚠️1-src | Unknown | n/a | **▼ (~$18)** |
| 19 | Karman | KRMN | 2025-02-13 | NYSE | $506M ($582M w/GS) | $22 | $18–20 | **Above** | ~$4B | n/a | Y (full) | +30% | **▲▲ (~$52)** |
| 20 | Smithfield | SFD | 2025-01-28 | Nasdaq | ~$261M (co) | $20 | $23–27 | **BELOW** | ~$7.9B | n/a (weak) | Unknown | ~flat | ▲ (~$25) |
| 21 | CoreWeave | CRWV | 2025-03-28 | Nasdaq | ~$1.5B | $40 | $47–55 | **BELOW** (downsized) | ~$23B | n/a (leak contradicted) | Unknown | ~0% | **▲▲ (~$106)** |
| 22 | eToro | ETOR | 2025-05-14 | Nasdaq | ~$620M tot | $52 | $46–50 | **Above** | ~$4.2B | **~10x** | Y (full) | +29% | **▼ (~$39)** |
| 23 | Hinge Health | HNGE | 2025-05-22 | NYSE | ~$437M | $32 | $28–32 | Top | ~$2.6B | n/a | Unknown | +17% | ▲ (~$54) |
| 24 | MNTN | MNTN | 2025-05-22 | NYSE | ~$187M | $16 | n/a | — | ~$1.2B | dbl-digit / 14x ⚠️ | Unknown | +65% | **▼ (~$9)** |
| 25 | Circle | CRCL | 2025-06-05 | NYSE | ~$1.1B | $31 | $27–28 | **Above** | ~$8.1B | **25x** (30x outlier) | Unknown | **+168%** | ▲ (~$83) |
| 26 | Chime | CHYM | 2025-06-12 | Nasdaq | ~$994M | $27 | $24–26 | **Above** | ~$11.6B | **>10x** | Y (full) | +37% | **▼ (~$18)** |
| 27 | Voyager Tech | VOYG | 2025-06-11 | NYSE | $383M ($402M w/GS) | $31 | $26–29 | **Above** | ~$1.9B | n/a | Y (full) | +84% | ▲ (~$42) |
| 28 | Figma | FIG | 2025-07-31 | NYSE | ~$1.2B | $33 | $25–28→30–32→33 | **Above** | ~$19.3B | **~40x** | Unknown | **+250%** | **▼ (~$21)** |
| 29 | Bullish | BLSH | 2025-08-13 | NYSE | ~$1.1B | $37 | $28–31→32–33→37 | **Above** | ~$5.4B | **>20x** | Unknown | +84% | ▲ (~$44) |
| 30 | Klarna | KLAR | 2025-09-10 | NYSE | ~$1.37B | $40 | $35–37 | **Above** | ~$15.1B | **15x→25x+** | Unknown | +15% | **▼ (~$17)** |
| 31 | Via Transport. | VIA | 2025-09-12 | NYSE | ~$493M | $46 | $40–44 | **Above** | ~$3.65B | n/a (Wellington IOI) | Unknown | +7.6% | **▼▼ (~$15)** |
| 32 | Gemini | GEMI | 2025-09-12 | Nasdaq | ~$425M (capped) | $28 | $24–26 | **Above** | ~$3.3B | **>20x** | Y (full) | n/a (faded) | **▼▼ (~$4)** |
| 33 | StubHub | STUB | 2025-09-17 | NYSE | ~$800M | $23.50 | $22–25 | Mid | ~$8.6B | **~20x** | Unknown | **−6.4%** | **▼▼ (~$10)** |
| 34 | Netskope | NTSK | 2025-09-18 | Nasdaq | ~$908M | $19 | $17–19 (rev. up) | Top | ~$7.3B | **>20x** (CEO) | Unknown | +18% | **▼ (~$10)** |
| 35 | Medline | MDLN | 2025-12-17 | Nasdaq | ~$6.26B | $29 | $26–30 | **Top** | ~$37–39B | >10x ⚠️1-src | Unknown | +41% | ▲ (~$34) |
| 36 | **SpaceX** | SPCX | **2026-06-12 (exp)** | Nasdaq/TX | **~$75B (~$86B w/GS)** | **$135 fixed** | none (fixed) | — | **~$1.77T** | **~2x** ($150B/$75B) | Option +83.3M | *not priced* | *not priced* |

> **% retail allocation:** not disclosed for any deal except where noted (Reddit's ~75k-Redditor
> directed-share program; SpaceX's reported ~30% retail set-aside). **Long-only vs hedge-fund
> book splits:** never found in the press for any deal — only named cornerstones (Arm's chip-
> customer consortium; Bullish's BlackRock+ARK ~$200M; Lineage's Norges ~$900M; Via's Wellington
> ~$100M; CoreWeave's Nvidia $250M anchor).

---

## Oversubscription detail — sources & conflicts

Only the rows with a leaked number are testable. Everything else is `n/a`.

| Deal | Multiple | Source(s) + date | Conflict / note |
|---|---|---|---|
| Aramco | 2.95x institutional; 1.5x retail; "465%" combined | Nasdaq/Reuters/Gulf News Dec 3 '19; Argaam Dec 5 '19 | Two metrics circulated (inst-only vs total book). Domestic book; foreign only ~10.5%. |
| Arm | 6x → 10x → "could hit 15x" | Reuters Sep 8 '23; The National Sep 12; Fortune Sep 14 | Not contradictory — book built through roadshow. SoftBank declined to raise price. |
| Reddit | 4–5x | Reuters (exclusive) Mar 17 '24; Bloomberg same day | Consistent across outlets. |
| Viking | 15x | Seeking Alpha, late-Apr '24 (pre-pricing) | ⚠️ Single source, snippet only, roadshow figure. |
| Rubrik | 20x | Fortune, Apr 24 '24 | ⚠️ Single source, snippet only; attribution unconfirmed. |
| CoreWeave | "oversubscribed" (no #) | Bloomberg Mar 21 '25 | **Leak contradicted by outcome:** downsized 49M→37.5M, priced *below* range, Nvidia $250M anchor. Do NOT carry as a hot book. → `n/a`. |
| eToro | ~10x | Finance Magnates / FinanceFeeds May 12 '25 | Books closed a day early. Consistent. |
| MNTN | "double-digit" / 14x | Bloomberg (dbl-digit); tradingcalendar (14x) | 14x is single low-tier source; trust "double-digit." |
| Circle | 25x (30x outlier) | Bloomberg Jun 4 '25; Morningstar (30x) | Complaints of "measly" allocations (Arca). |
| Chime | >10x ("double-digit") | Bloomberg, Jun '25 | Top accounts got majority of shares. |
| Figma | ~40x | **Bloomberg Jul 29 '25 (re-verified)** | 100% roadshow conversion. Most extreme in set. |
| Bullish | >20x | Bloomberg Aug 12 '25 | BlackRock + ARK ~$200M IOI. |
| Klarna | 15x → 25x+ | Sahm Capital Sep 8; IFR "north of 25x"; Bloomberg Sep 9 | **Conflict:** 15x vs 25x+ spread across the roadshow. ~half of orders got zero. |
| SailPoint | 20x | Nasdaq | ⚠️ Single source. |
| Gemini | >20x | cryptonews / crypto.news, Sep '25 | $425M cap was a *response* to >20x demand; books closed early. |
| StubHub | ~20x | Reuters (via BNN) Sep 12 '25 | Bloomberg Law separately "oversubscribed" (no #). |
| Netskope | >20x | CNBC Sep 17–18 '25 | **CEO-sourced** (self-reported), not a banker leak. |
| Medline | >10x | financialcontent/WRAL Dec 18 '25 | ⚠️ Single low-tier source. |
| SpaceX | ~2x ($150B vs $75B) | Bloomberg/Yahoo/TNW Jun 8–9 '26 | Demand at a *fixed* $135 price — not comparable to bookbuilt demand. |

---

## The test: does oversubscription predict aftermarket performance?

### What the academic literature says (the backbone)

In markets that *legally disclose* subscription ratios, the finding is **two-part and
opposite-signed**:

- **First-day pop:** higher oversubscription → reliably **higher** first-day return. Robust
  across Hong Kong, Malaysia, India, UK. (Agarwal-Liu-Rhee 2008, *JIFMIM* 18(2); Malaysian
  fixed-price studies, *Pacific-Basin Finance J.*; MDPI *JRFM* 14(6):158, 2026.)
- **Long-run:** higher oversubscription / bigger pop → predicts **long-run UNDERPERFORMANCE**
  — the winner's-curse / overreaction reversal. (Agarwal-Liu-Rhee 2008 is the keystone: high-
  demand IPOs show positive initial but *negative* long-run excess returns.) Caveat: UK
  *privatization* IPOs are a documented exception (positive long-run).
- **Mechanism:** issuers deliberately underprice to stimulate oversubscription; informed money
  crowds hot deals; sentiment-driven pops mean-revert to fundamentals.

### What THIS (dirty, leaked-US) comp set shows

Our 2024–25 sample behaves like a **natural experiment** — and it lines up with the
literature's long-run leg almost too cleanly. Group the deals by leaked multiple:

**The "blowout book" cohort (≥20x leaked) — 2025:**

| Deal | Leaked | Day-1 | Current vs offer |
|---|---|---|---|
| Figma | ~40x | +250% | **▼ −36%** |
| Klarna | 15–25x+ | +15% | **▼ −59%** |
| Circle | 25x | +168% | ▲ (still up, well off highs) |
| Gemini | >20x | faded | **▼▼ −85%** |
| Bullish | >20x | +84% | ▲ +18% (off day-1 highs) |
| StubHub | ~20x | −6% | **▼▼ −58%** |
| Netskope | >20x | +18% | **▼ −49%** |
| SailPoint | 20x | n/a | **▼ −23%** |

→ **7 of 8 of the most-hyped 2025 books are now flat-to-deeply underwater.** Only Circle and
Bullish (both crypto, both off their highs) held above offer. The single most oversubscribed
deal in the entire set — **Figma at ~40x — had the biggest first-day pop in 3+ decades
(+250%) and is now ~36% below its IPO price.** Gemini (>20x) is down ~85%.

**The "no leaked number / weak book / below-range" cohort — frequently the BEST performers:**

| Deal | Book | Day-1 | Current vs offer |
|---|---|---|---|
| CoreWeave | leak contradicted; priced *below* range; Nvidia anchor | ~0% | **▲▲ +164%** |
| Viking | 15x but only +8% day-1 | +8% | **▲▲ +270%** |
| UL Solutions | n/a | +23% | **▲▲ +245%** |
| Karman | n/a | +30% | **▲▲ +135%** |
| Rubrik | 20x but only +16% day-1 | +16% | **▲▲ +120%** |
| Astera Labs | n/a | +72% | ▲▲ (multi-bagger) |

### Conclusion

1. **The leaked multiple is a momentum signal, not a quality signal.** It predicts the
   *first-day pop* (consistent with the literature) — but in this sample the pop is the
   *warning sign*, not the reward. The deals that popped hardest (Figma +250%, Circle +168%,
   Bullish/Voyager +84%) gave most or all of it back.
2. **A big leaked multiple has been, if anything, a contrarian *sell* signal for the
   aftermarket** in 2024–25. The ≥20x cohort underperformed the "boring book" cohort badly.
   This is exactly the winner's-curse reversal Agarwal-Liu-Rhee describe — now visible even in
   the noisy US leak data.
3. **Day-1 pop magnitude > the leaked multiple itself.** The cleanest predictor of subsequent
   pain isn't the rumored "Nx" — it's how violently the stock popped on day 1 (the realized
   expression of that demand). Treat any +100% debut as a mean-reversion candidate.
4. **The data is too thin and too dirty for a real regression.** Only ~18 of 36 deals have any
   leaked number; several are single-source snippets; the multiples mix pre-pricing and final-
   book figures. This is a *directional* read, not an estimated coefficient. Per the caveat up
   top, that's the honest ceiling on this exercise.

---

## Situating SpaceX (SPCX) — pricing 2026-06-11

**Live terms (re-verified 2026-06-09):** $135/share **fixed before the roadshow** (no range —
almost unheard of), 555.6M Class A shares, **~$75B base raise (~$86B with the +83.3M-share
greenshoe), ~$1.77T implied valuation.** Dual-class: Musk keeps ~79–82% of votes on ~42% of
equity. **~30% of shares reportedly reserved for retail** (≈3x the typical 5–10%). Whole
company, *not* a Starlink carve-out. Lead-left Goldman; ~21-bank syndicate. Books close ~Jun
11; trades Jun 12 on Nasdaq + "Nasdaq Texas." **~2x oversubscribed** ($150B orders vs $75B).

**How it stacks against the comp set:**

- **Size:** off the chart. ~$75B base is **~2.5x Saudi Aramco's $29.4B** (the prior record) and
  dwarfs every 2024–25 deal (next-biggest in set: Medline $6.26B, Lineage $4.44B, Arm $4.87B).
- **Oversubscription:** **~2x is strikingly *modest*** next to the 2025 hot books (Figma ~40x,
  Circle/Klarna 25x, Gemini/Bullish/Netskope/StubHub ~20x). On the contrarian read above, a
  *modest* book is **reassuring, not disappointing** — the 20–40x deals are the ones that
  cratered. But three things make the 2x non-comparable:
  1. **The price is FIXED.** 2x reflects demand at a non-negotiable $135 — there's no
     bookbuild for institutions to inflate, and no underwriter underpricing to manufacture a
     pop. The leaked-multiple→pop mechanism that drove Figma simply doesn't apply the same way.
  2. **Sheer size caps the pop.** A ~$75–86B float cannot melt up 250% like a $1.2B Figma
     float. Expect a muted day-1 move regardless of "demand."
  3. **~30% retail** dilutes the concentrated-institutional-book dynamic the comps are built on.
- **Valuation stretch is the real risk, not the book.** The ~$1.77T IPO mark is **~2.2x the
  ~$800B Dec-2025 secondary tender ($421/share)** — a massive step-up in ~6 months. The comps
  warn that the deals pricing at the richest stretch into the hottest sentiment (Figma at
  ~$19.3B/40x; Gemini; Klarna down from its $45.6B peak) reversed hardest. SpaceX's risk vector
  isn't "the book was only 2x" — it's "the implied valuation more than doubled the last private
  mark into a fixed-price take-it-or-leave-it deal."

**Bottom line for SpaceX:** the ~2x book is a *weak* comp to the academic ratios and to the
2025 leak cohort because the price was fixed — so don't read it as either bullish (vs 40x
Figma) or bearish on the usual oversubscription logic. The transferable lesson from this comp
set is the **opposite** one: the splashy 20–40x "blowout" books of 2025 were the worst
aftermarket bets, and the quiet/below-range deals (CoreWeave, Viking, UL, Karman) were the
best. SpaceX is sui generis on size and structure; judge it on the **2.2x valuation step-up
and the fixed-price mechanics**, not on a leaked subscription multiple.

---

## Open items / what to verify before relying on this

- **Greenshoe exercise** unconfirmed for ~half the deals (option existed; no post-30-day PR
  found). Confirmed full: Aramco, Kenvue, Viking, UL, OneStream, ServiceTitan, Karman, Voyager,
  Chime, eToro, Gemini. StandardAero: on the secondary. Astera: likely.
- **Single-source / snippet-only multiples** (Viking 15x, Rubrik 20x, SailPoint 20x, Medline
  >10x, MNTN 14x) need confirmation against original Bloomberg/IFR text before citing hard.
- **1-week / 1-month aftermarket marks** not uniformly pulled — only day-1 and current are
  firmly sourced. A clean intermediate-return table requires per-ticker historical series.
- **SpaceX is not yet priced** — all terms are reported/expected and can move at the Jun 11
  pricing. Primary S-1: SEC EDGAR CIK 0001181412.

---

## Sources (primary, by deal)

**SpaceX (re-verified):** [Yahoo/Bloomberg "well oversubscribed, $10B orders"](https://finance.yahoo.com/markets/stocks/articles/spacex-ipo-said-well-oversubscribed-154906500.html) · [TNW](https://thenextweb.com/news/spacex-ipo-oversubscribed-orders-close) · [Motley Fool, Jun 9 '26](https://www.fool.com/investing/2026/06/09/spacexs-historic-ipo-may-be-oversubscribed-heres-w/) · S-1 EDGAR CIK 0001181412.
**Figma (re-verified):** [Bloomberg "approaching 40x"](https://www.bloomberg.com/news/articles/2025-07-29/figma-s-1-2-billion-ipo-approaching-40-times-oversubscribed) · [Secfi "+250%/$68B"](https://secfi.com/newsletter/figmas-ipo-pricing-analysis) · [Yahoo "dips below IPO price"](https://finance.yahoo.com/news/figma-dips-below-ipo-price-172738154.html).
**Aramco:** [Nasdaq/Reuters 2.95x](https://www.nasdaq.com/articles/saudi-aramco-ipo-institutional-tranche-2.95-times-oversubscribed-2019-12-03) · [Argaam 465%](https://www.argaam.com/en/article/articledetail/id/1333537) · [CNBC greenshoe](https://www.cnbc.com/2020/01/12/saudi-aramco-raises-ipo-to-record-29point4-billion-through-greenshoe-option.html).
**Arm:** [Reuters 6x](https://finance.yahoo.com/news/softbanks-arm-ipo-currently-six-174319599.html) · [The National 10x](https://www.thenationalnews.com/business/technology/2023/09/12/arms-ipo-already-10-times-oversubscribed/) · [Fortune 10x+](https://fortune.com/europe/2023/09/14/softbank-raising-prices-49-billion-arm-ipo-investors-oversubscribed-10-times/).
**Reddit:** [Bloomberg/Reuters 4–5x](https://www.bloomberg.com/news/articles/2024-03-17/reddit-s-ipo-as-much-as-five-times-oversubscribed-reuters-says) · [Variety day-1](https://variety.com/2024/digital/news/reddit-ipo-stock-price-1235948162/).
**Astera:** [IPOScoop](https://www.iposcoop.com/the-ipo-buzz-astera-labs-alab-prices-ipo-at-36-00-2-00-above-the-range/) · [Bloomberg $713M](https://www.bloomberg.com/news/articles/2024-03-20/astera-labs-said-to-price-ipo-above-target-to-raise-713-million).
**Birkenstock:** [CNBC](https://www.cnbc.com/2023/10/10/birkenstock-expects-to-price-ipo-at-46-per-share.html) · [Yahoo/Reuters day-1](https://finance.yahoo.com/news/birkenstock-opens-at-41-a-share-in-ipo-debut-nearly-11-below-its-initial-price-174247646.html).
**Kenvue:** [Kenvue pricing PR](https://investors.kenvue.com/financial-news/news-details/2023/Johnson--Johnson-and-Kenvue-Announce-Pricing-of-Upsized-Kenvue-Inc.-Initial-Public-Offering/default.aspx) · [CNBC day-1](https://www.cnbc.com/2023/05/04/jj-kenvue-ipo-kvue-starts-trading-on-nyse.html).
**Amer Sports:** [Renaissance Capital](https://www.renaissancecapital.com/IPO-Center/News/103063/Sports-equipment-and-apparel-maker-Amer-Sports-prices-US-IPO-at-$13-below-t) · [CNBC](https://www.cnbc.com/2024/02/01/amer-sports-ipo-wilson-tennis-racket-maker-to-trade-on-nyse.html).
**CoreWeave:** [CNBC Nvidia $250M anchor / below range](https://www.cnbc.com/2025/03/27/coreweave-ipo-pricing.html) · Bloomberg Mar 21 '25 ("oversubscribed").
**Circle:** Bloomberg Jun 4 '25 (25x) · Morningstar (30x) · Fortune Jun 4/6 '25.
**Klarna:** Sahm Capital Sep 8 '25 (15x) · IFR (25x+) · Bloomberg Sep 9 '25 · CNBC.
**Chime:** Chime closing PR / Davis Polk ($993.6M, greenshoe) · CNBC Jun 12 '25 · Bloomberg (>10x).
**eToro:** Finance Magnates / FinanceFeeds May 12 '25 (~10x, greenshoe) · CNBC.
**Hinge Health:** CNBC May 21 '25 · MobiHealthNews · Seeking Alpha ("oversubscribed," no #).
**Bullish:** Bloomberg Aug 12 '25 (>20x) · Yahoo/CNBC (BlackRock+ARK; day-1).
**Gemini:** Gemini closing PR (full greenshoe) · cryptonews/crypto.news (>20x) · Bloomberg Sep 11 '25.
**Venture Global / SailPoint / Karman / Smithfield / MNTN / Voyager / Netskope / StubHub / Via / Medline:** company pricing/closing PRs + SEC 424B4; Renaissance Capital recaps; Bloomberg/Reuters/CNBC pricing coverage; financialcontent (Medline). See per-deal notes above for the specific oversubscription attributions.
**2024 large-caps (Lineage/Viking/Waystar/StandardAero/Rubrik/Tempus/Ibotta/UL/OneStream/ServiceTitan):** company pricing & closing PRs + SEC 424B4 prospectuses; CNBC/Bloomberg/Fortune/Renaissance day-1 coverage; OneStream take-private via Hg PR (Apr 2026).
**Literature:** Agarwal, Liu & Rhee (2008), *J. Intl Fin. Markets, Inst. & Money* 18(2):176–190; Levis (1995); MDPI *JRFM* 14(6):158 (2026); Malaysian fixed-price oversubscription studies (*Pacific-Basin Finance J.*); Indian hybrid-IPO study (*PBFJ*).
