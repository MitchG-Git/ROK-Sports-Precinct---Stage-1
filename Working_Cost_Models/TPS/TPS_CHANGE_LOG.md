# TPS_CHANGE_LOG — ROK_TPS_CostModel_V2.xlsx
**Tender:** TEN16699 Rockhampton Sports Precinct Stage 1A & 1B · **Entity:** TriCore Plumbing Services (hydraulic)
**Source:** `TriCore Docs\Master Cost Sheets\MasterCostSheet_Hyd.V1.xlsx` (copied 26 Jul 2026 — **original never modified**)
**Working copy:** `Working_Cost_Models\TPS\ROK_TPS_CostModel_V2.xlsx`
**Work order:** `_Tender_Control\07_Commercial_Reconciliation\COST_MODEL_REBUILD_DECISION.md` §"Rebuild plan" item 4
**Architecture:** PRESERVED in full (10 original sheets untouched structurally; 2 sheets added). All pricing **EX GST**.

---

## Headline result

| | ex GST |
|---|---:|
| **STAGE 1A TOTAL** (lump sum + PC sums + provisional) | **$1,743,304.82** |
| **STAGE 1B TOTAL** (lump sum + PC sums + provisional) | **$266,489.36** |
| **TPS GRAND TOTAL** | **$2,009,794.18** |
| — of which base sell (`N64`) | $1,670,180.34 |
| — of which PC sums + provisionals (`N78`) | $339,613.84 |
| Total cost before markup (`R39`) | $1,159,948.87 |
| Effective markup (`R49/R39`) | **41.50%** (was 45.73%) |

*(Totals include the Rule 4 equipment-test adjustments of §12 below: +$2,011.86 net. Pre-equipment-test figures were 1A $1,741,527.08 / 1B $266,255.24 / total $2,007,782.32.)*

Held separately, **not** in the tendered sum: EBC add-prices $22,405.74; alternate deltas ALT-1 $36,891.78 / ALT-2 $1,169.23.

---

## Bridge: old $273,056.54 → new $2,009,794.18 ex GST

| Step | $ | Running |
|---|---:|---:|
| **OLD sub-total `N64`** (NBC $81,329.70 + PAM $17,272.79 + Siteworks $174,454.06) | | **273,056.54** |
| 1. Remove GST rows (`N66` $27,305.65 / `N68` $300,362.20) — model is now ex-GST throughout | 0.00 | 273,056.54 |
| 2. Re-base markup 45.73% → 41.50% (profit now on total cost, not on cost+prelims+O/H), applied to the **old** cost base | −7,263.76 | 265,792.78 |
| 3. **Big-ticket net movement** (detail below) | +6,043.97 | 271,836.75 |
| 4. **Cost growth × 1.415 markup** (detail below) | +1,398,343.59 | 1,670,180.34 |
| **= NEW base sell `N64` ex GST** | | **1,670,180.34** |
| 5. PC sums now separately identified (fixtures, drinking fountains, bubblers) + $20,000 provisional connection fees in **both** stages | +339,613.84 | **2,009,794.18** |
| **= NEW GRAND TOTAL ex GST `N87`** | | **2,009,794.18** |

Step 3 in detail — the big-ticket blocks moved from $22,808.73 to $28,852.70:

| Movement | $ |
|---:|---:|
| Orphaned NBC Rheem HWU block `AC17` wired into `N16` at the corrected qty 2 (it reached **no** total before) | +8,329.51 |
| PAM HWU rate corrected — `W25` $3,438.29 (315 L model) → $2,016.08 (50 L Rheem 613/050) | −1,635.54 |
| Three remaining `Installation_MH` tokens zeroed as Rule 4 duplicates (`W16` $250 + `Z16` $200 + `W30` $200) | −650.00 |
| **Net** | **+6,043.97** |

Step 4 in detail — total cost rose from **$171,720.18** to **$1,159,948.87** (**+$988,228.69**):

| Cost driver | at cost |
|---|---:|
| **Labour** — 166 base crew-days + 1,399.8 LH supervision hours at the ×1.08 FIFO rates (previously **$0 priced anywhere**) | +661,284.94 |
| **Plant** — Phase 7 plant roll-up (previously **$0**) | +39,539.01 |
| **Subbies / testing / CCTV / hydro tests / Form 72 / equipment storage** (was $2,085 of compaction testing only) | +31,675.00 |
| **Materials, net** — adopted quantities, new scope rows (DP stubs, vent risers, articulation, seismic, AS1851, temp water, HWU plinths), **less** the Ø200 copper→HDPE re-rate and the 316 SS re-rate | +12,031.22 |
| Contingency & deliveries on the above (×1.18 Siteworks/PAM, ×1.12 NBC) | +111,103.15 |
| **Accommodation** — Phase 7 Option A (14 apt-months + 225 LH nights) | +87,715.37 |
| **Flights** — 51 person-months × 2 returns × 2 legs × $220 | +44,880.00 |
| **Total cost growth** | **+988,228.69** |

Note within the materials line: the Ø200 main re-rate **reduced** cost by **$23,226.61** (old copper line $46,345.00 → new HDPE $23,118.39), which is why a large volume of quantity and scope additions nets to only +$12,031.22.

**The old $300,362.20 "incl GST" figure is withdrawn.** It was $273,056.54 + 10% GST on a materials-and-subbies-only sell that contained **no labour, no plant, no accommodation and no supervision**, and it silently omitted the NBC hot water units. It must not be reused or compared like-for-like.

**D6 director flag (carried from the audit):** the old model's pump-station block (`W37` $468,000 → `W43` $545,700) fed **no roll-up cell**. Any quote previously circulated off `N68` never included the pump station — its removal moves no headline number.

Cost composition of the new model (pre-contingency, across the three work areas): labour $661,284.94 · plant $39,539.01 · subbies $33,760.00 · materials $145,271.38 · = $879,855.33, plus contingency/deliveries $147,498.15, accommodation $87,715.37 and flights $44,880.00 = $1,159,948.87.

---

## Repair 1 — External links severed

All **4** external links removed; **252** externally-referenced cells replaced with their frozen cached values as literals, each tagged in a new **"Source"** note column (row 4 header) on the affected sheet.

| Ref | Source workbook | Cells frozen | Note column | Tag written |
|---|---|---:|---|---|
| [1] | SharePoint `CQU ROK_PROGRAM - MASTER.V1.xlsx` | 4 (`00_ TCS Prelim & OH` C9:C12, D45) | K | "frozen from [1] … re-based from Phase 7 TPS_Programme" |
| [2] | SharePoint `CQU ROK_Staff Costing.V1_Steph.xlsx` | 13 (all labour rates) | I | "frozen from [2] … re-based ×1.08 below" |
| [3] | `240614 - Pipe & Fittings - Price Comparison.xlsx` | 155 (`Material Rates_Master` D-col) | N | "frozen from [3] (Jun-2024 cache) … ≥2 yr old at 2027 start — Phase 5 re-source pending" |
| [4] | `240614 - Suppliers Subbies - Price Comparison.xlsx` | 80 (`Equip&HIRE` 35 + `Misc Subbie` 45) | G / H | "frozen from [4] (Jun-2024 cache) … Phase 5 re-source pending" |

Verified: `xl/externalLinks/*` parts **absent** from the package; no `externalLink` entry in `xl/_rels/workbook.xml.rels`; no `<externalReferences>` block in `workbook.xml`; **0** formulas containing `[n]`. The only `[n]` strings remaining anywhere are inside the human-readable Source note text.

Also removed: 14 orphaned workbook-level defined names, all resolving to `#REF!` (verified unreferenced by any formula before deletion).

---

## Repair 2 — Labour ×1.08 re-base, formula-derived cascade

`LabourProject Rates_Master`: monthly rates are now **literals**; hour/day/week cells remain **formula-derived** (`÷210`, `÷21`, `÷4`), so the cascade recalculates.

| Role | Old monthly | New monthly (×1.08) | $/hr | $/day | $/week |
|---|---:|---:|---:|---:|---:|
| Leading Hand (`E17`) | 25,854.00 | **27,922.32** | **132.9634** | 1,329.6343 | 6,980.58 |
| Tradesman/Plumber/Operator (`E24`) | 19,764.4593 | **21,345.6160** | **101.6458** | 1,016.4579 | 5,336.40 |
| T/A & Apprentice (`E31`) | 16,129.3667 | **17,419.7160** | **82.9510** | 829.5103 | 4,354.93 |

All three targets hit **to the cent** per §5.4. Crew #1/#2 day rate `E37` = $2,862.4261 (matches the Phase 7 indicative figure). Cascade verified: every dependent formula in `Siteworks`, `ClubHouse (NBC )`, `Public Amenities (PAM)` and `00_ TCS Prelim & OH` resolves through these cells — **no stale hardcoded labour rate remains anywhere**.

Escalation factors left untouched as verified correct: PE ×1.38, PVC ×1.38, Subby ×1.15, Delivery ×1.20 (block J14:M19 on each work-area sheet).

---

## Repair 3 — `TCS $ Sched` roll-up defects

**(a) Pump station block DELETED** — the whole `V34:W43` block (`W37` $468,000 → `W43` $545,700) removed, merged cells unmerged first. Note row written at `V34`:
> "Sewer pump station EXCLUDED — installed by Council per Addendum 2 (10 Jul 2026); interfaces per interface ledger L6; add-price held in EBC register (APS 14065 basis) — see EBC_Alternates."

**(b) NBC Rheem HWU block wired into the summary** — `AC14` qty **3 → 2** (per `QUANTITY_RECONCILIATION` TPS_NBC: take-off double-count across legend pages H+J removed; 2 drawn on H-NBC-200/202). `N16` rewritten `=S16+W17+Z17` → **`=S16+W17+Z17+AC17`**. `AC17` now contributes **$8,329.51** (after the Rule 4 token zeroing of repair 12; $8,929.51 before it); it previously reached no total at all.
Also corrected: the PAM HWU rate (`W25`) $3,438.29 → **$2,016.08** — the PAM unit is a Rheem 50 L 613/050 (H-PAM-200), not the 315 L model whose rate had been used.

**(c) `S39` dead formula removed** (`=SUM(S13:S26)` — mixed/mislabelled range, referenced by nothing).

**(d) GST removed** — `N66` (10% GST) and `N68` (grand total incl GST) cleared; `M64` relabelled **"TOTAL — TPS BASE SELL ex GST (excl PC Sums)"**; note written at `M66`. Everything downstream is ex GST.

**(e) Markups re-based to the §5.4 rule** — each of Prelims 5.5%, O/H 18%, Profit 18% now applied **to total cost**:

| Cell | Before | After |
|---|---|---|
| `R42` Prelims | `=R39*Q42` (already on cost) | unchanged |
| `R43` O/H | `=R39*Q43` (already on cost) | unchanged |
| `R47` Profit | `=R45*Q47` — profit on **cost + prelims + O/H** | **`=R39*Q47`** — profit on **cost** |

Effective markup `R49/R39`: **45.73% → 41.50%**, now agreeing with the label at `Q51`. The old chain compounded to cost × 1.235 × 1.18 = **×1.45730**; the new chain is cost × (1 + 0.055 + 0.18 + 0.18) = **×1.41500**. On the new cost base the re-base removes **$49,065.84** of compounded profit; on the old cost base (as shown in the bridge) it is **−$7,263.76**.

---

## Repair 4 — Adopted quantities (Denis's figures preserved, never overwritten)

A **"Denis qty"** column (**G**) and a **"Qty / rate source note"** column (**H**) were added to all three work-area sheets (headers at row 13). Every quantity change writes Denis's original figure into column G and the reason into column H — **no figure was deleted or silently changed**.

**Siteworks (10 lines):** Ø200 main 135 → **134.63 m** · fire main 218 → **217.73 m** · CW spine 237 → **236.88 m** · 32 PE 38 → **37.26 m** · 25 PE 75 → **74.25 m** (the Ø20→25 / Ø25→32 upsizing convention retained per Rule 1, Opens #11) · sewer Ø150 30 → **29.29 m** · sewer Ø100 179 → **178.24 m** · trade waste 17 → **16.28 m** · storm stubs 7 → **6.91 m** · meter assembly 0.5 → **1 EA** (the legend groups both assemblies as one item).

**NBC (25 lines):** sanitary Ø100 231 → **230.07 m** · Ø50 **12.68** · Ø40 **25.61** · trade waste 53 → **54.78 m** (52.80 TW layer + 1.98 vent-layer stub merged and **counted once**, Opens #25 — the three duplicate vent-layer rows were zeroed with a note, not deleted) · TW bends 8/24 · Geberit 50 **12.47 m** · PE 40/32/25 **27.78 / 21.31 / 15.45 m** · PEX black **157.82 m** / red **65.29 m** · hose taps 4 → **5** (drawn-but-uncounted symbol on NBC-201, adopt-higher per H002 n.15) · 20 mm RPZD 3 → **4** · 50 mm RPZD 1 → **2** · HWU **2**.

**PAM (12 lines):** sanitary Ø100 62 → **61.16 m** · Ø50 **6.93 m** · clean-outs 6 → **7** (+ covers) · FWG 3 → **4** · vent Ø65 **1.93 m** · PE 40 **3.27 m** · PEX **18.86 / 5.89 m**.

**Fixture recount adopted** (Fixtures sheet) — 21 WC pans, 14 basins, 10 showers + 10 mixers, 3 urinals, 4 hand-wash troughs, 4 wash troughs, 1 CSK, 22 floor wastes, PWD suite ≈ **93 NBC fixtures**, driving the fit-off labour (T5-01, 13 crew-days) and the fit-off consumable line (re-based from an $1,800 lump to 93 × $30). **PAM ≈ 15 fixtures** (8 s/s WC + in-wall cisterns, 1800 trough, PWD basin, CSK, 2 TR, timed taps) — never counted in the original take-off.
**DP stubs: NBC 19 EA, PAM 4 EA** (NewItems #5/#6, both carrying the count RFI).

---

## Repair 5 — Ø200 main re-rate (HDPE base, copper alternate)

**BASE OFFER:** Ø200 ID **HDPE PE100 SDR11 DN250** per locked §5.5 — inside the spec's own equivalence table (VOL38 §10.1, Cromford PN16 250 = Ø200 ID), so this is a **conforming** offer, not a departure.

No project quote exists for PE (Gap #5). Rate **benchmark-derived**:

> Reece Q-459014437 (NAS, current Jul-26) PE100 PN16 125 mm @ $186.65 / 6 m = **$31.1083/m**
> × (250/125)² weight ratio (wall ∝ OD at constant SDR) = **$124.4333/m**
> × **1.38** PE escalation-to-2027, applied **once** via `$M$16` (the source rate is pre-escalation per KeyRates)
> = **$171.72/m** → 134.63 m = **$23,118.39**

Cell `E349` carries the live formula `=124.4333*$M$16` and is tagged **"BENCHMARK-DERIVED PENDING RFQ (Gap #5)"** in the Source column.

**Copper retained as a clearly-labelled ALTERNATE, excluded from the base roll-up** — `EBC_Alternates` ALT-1: 134.63 m of Kembla Type B DN200 at the Tradelink 6595064 basis ($2,015 / 6 m) = $45,213.24, a **+$36,891.78 sell delta** if adopted. The copper tapping-cluster fittings (tees, bends, full-faced stubs, gasket kits, sluice valves) **stay in the base** at adopted counts — only the pipe run changes material.

---

## Repair 6 — Building water >DN22 (316 SS base, copper alternate)

**BASE:** 316 SS press-fit per WS2 for everything >DN22; PEX/copper ≤DN22 unchanged (conforming).

Tradelink refused a 316 SS rate (Gap #2); Reece Q-459014431 priced 22 / 28 / 35 mm — which **covers every size needed** (NBC and PAM carry nothing above 35 mm), so the **pipe** rate is a project quote:
- 32 Cu → **316 SS 35 mm** `=132.03/6`
- 25 Cu → **316 SS 28 mm** `=80.63/6`

**Fittings** have no quote at any size, so they are **benchmark-derived at copper-press × 1.5** (SS press fittings run 1.4–1.6× copper on supplier curves) — 15 fitting rows across NBC and PAM, every one tagged **"pending RFQ per gap list (Gap #2)"** in the Source column.

**Copper alternate** — `EBC_Alternates` ALT-2, outside the base roll-up: copper pipe $3,657.30 vs SS pipe $2,479.64, less the fitting uplift reversion ($439.89) = **+$737.77 material**, **+$1,169.23 sell** if adopted. Note recorded: SS pipe is *cheaper* than copper at these sizes; the uplift sits in the fittings. 316 SS long-lead 10–14 weeks flagged.

---

## Repair 7 — New scope rows

| Item | Where | Basis |
|---|---|---|
| Sewer rising main 110 m — **EBC** | `EBC_Alternates` EBC-1 | PE100 DN110 benchmark + fittings + 2 crew-days + plant; **add-price $15,717.29**, formula-ready for reinstatement; RFI CL C4 |
| **Articulation adder** (H1 "P" reactive site) | NBC r782 $2,500 · PAM r748 $750 | ~25 / ~7 joints at ~$100 (H-NBC-300 det. 1); **labour** is Phase 7 T5-05 (3 crew-days) inside the fit-off block; pending Storm Plastics RFQ (Gap #4) |
| **Seismic adder** (AS1170.4 EDC 2, subsoil Ce) | NBC r932 $3,500 · PAM r853 $500 | ~2.5% of rough-in material; **EWP** = scissor-lift days; **labour** T3-04 (3 cd) + T4-07 (2 cd); layout drafting only, no design liability (CL C7); RFQ nVent/Unistrut/Hilti pending (Gap #3) |
| **Testing / commissioning / CCTV share** | Siteworks r147 CCTV $5,000; r149 boost test $3,560; r150 3× hydro @ $1,945; r151 Form 72; NBC r150 test gear, r154 Form 72 | VOL38 §3.56 CCTV of TPS's own assets only (interface L15); Misc Subbie rates |
| **Temporary potable water for testing/flushing** | Siteworks r148 $1,500 (purchase) + water truck 30 hr @ $110 | ITT §17.3 — no site water; storage pods are in Prelim & OH (no overlap) |
| **AS1851 12-month fire maintenance** | NBC r309 $2,500 | VOL38 obligation; 6-monthly service visits piggybacked on site attendance |
| **Trade waste application — EBC** | `EBC_Alternates` EBC-2 | Excluded per locked §5.3 / X3; **add-price $4,147.67**; arrestor hardware stays in the NBC base |
| Fire extinguishers — EBC | `EBC_Alternates` EBC-3 | NBC ×8 + PAM ×1, no trade allocation (CL B8); **add-price $2,540.78** |
| FB fire blanket | NBC r308 | Matrix 4.11-d |
| Vertical vent risers | NBC r795 (13 EA) · PAM r761 (1 EA) | NewItems #7/#8 — plan take-off measured horizontals only |
| Roof-DP connection stubs | NBC r844 (19 EA) · PAM r767 (4 EA) | NewItems #5/#6; scope ends at "CONNECT TO CIVIL" (interface L2) |
| Basket traps (water layer) | NBC r718 (2 EA) | Distinct from the sewer basket traps — explicitly not merged |

---

## Repair 8 — PC Sums as separate identified lines (`TCS $ Sched` M70:N78, build-up R70:S78)

| Line | Cell | ex GST |
|---|---|---:|
| PC-1A Fixtures supply — Tradelink 1066143 adjusted + 15% | `N71` | 207,268.84 |
| PC-1A Drinking fountains — 2 × CF400 chilled (NBC) + 15% | `N72` | 25,415.00 |
| PC-1A Provisional connection fees — **as directed, no markup** | `N73` | 20,000.00 |
| PC-1B Fixtures supply — PAM adopted-count extension + 15% | `N74` | 17,250.00 |
| PC-1B Drinking fountains — 2 × CF400 non-chilled (PAM) + 15% | `N75` | 16,560.00 |
| PC-1B Water bubbler stations — 4 × site DF (H003) + 15% | `N76` | 33,120.00 |
| PC-1B Provisional connection fees — **as directed, no markup** | `N77` | 20,000.00 |
| **PC SUMS TOTAL** | `N78` | **339,613.84** |

**Fixture PC build-up and the adopted-count delta** (visible at `R70:S78`):

| | $ |
|---|---:|
| Tradelink 1066143 quote total | 252,694.77 |
| less 4 × CF400 chilled fountains (moved to the DF PC lines — no double count) | −44,200.00 |
| less 5 × Billi Quadra 4180 — **supplied by RCC** per FF&E VOL25 (install labour retained in Base) | −38,261.00 |
| **plus NBC adopted-count extension allowance** | +10,000.00 |
| **plus PAM adopted-count extension allowance** | +15,000.00 |
| **Adjusted PC base** | **180,233.77** → 1A $207,268.84 / 1B $17,250.00 after +15% |

**Stated delta = +$25,000.** The quote was assembled when only 25 of ~108 adopted fixtures had been counted (2 of 9 architectural sheets); the PAM set was never counted at all. Where adopted counts exceed the known quote lines they are extended at the quote-rate family. Phase 4 line-by-line reconciliation governs before award. Quote validity 13/08/26 vs a 2027 start and the "544 Yaamba Rd Parkhurst" header defect are qualified (CL F4).

**Drinking fountains — calculated PC:** chilled CF400 @ $11,050 (Tradelink 1066143, project quote). The **non-chilled** variant is unpriced by anyone (Gap #6) — benchmark **$7,200** adopted (chilled less ~35% chiller premium), stated on the build-up and carried for both the PAM units and the 4 site DF/BT positions on H003. Signage is explicitly extra on the quote. Chilled/non-chilled same-SKU confusion RFI'd (CL C10).

**$20,000 provisional connection fees carried in BOTH stages exactly as directed** (§5.4), at actual-cost reimbursement with **no markup** — 1A 5.0 and 1B 4.6.

---

## Repair 9 — Labour, plant and accommodation from Phase 7

**Crew-days** loaded into the work-area labour blocks as formula-driven `qty × day rate` (166 base crew-days, matching the Phase 7 roll-up exactly; the 2 EBC crew-days for the rising main are **excluded** from base and sit in EBC-1):

| Sheet | Crew 1 | Crew 2 | Crew 3 | Crew 4 | Crew 5 | LH supervision (hr) |
|---|---:|---:|---:|---:|---:|---:|
| Siteworks | 23 | 35 | — | — | — | 489.2 |
| NBC | 26 | — | 14 | 21 | 27 | 742.1 |
| PAM (1B) | 4 | 4 | 2 | 5 | 5 | 168.5 |
| **Total** | **53** | **39** | **16** | **26** | **32** | **1,399.8** |

166 crew-days · 1,399.8 LH hours = **140 LH days** exactly as the brief requires.

**Plant** loaded into the Equip blocks from the Phase 7 plant roll-up: 13–16 T 16 d · 8 T 6 d · 3–5 T 19 d · 1.8 T 24 d · trench roller 22 d · wacker 28 d · <6 T tipper 18 d · scissor lift 13 d · vac trailer 1 d · hydro-ex 20 hr · water truck 30 hr · crane/HIAB 25 hr. **PE butt welder + EF processor** (22 d total) is **not in any hire register** — carried as a stated ~$350/day allowance to be quoted at Phase 6. Scissor lift is on a weekly register rate converted to $30/day and **flagged** for Phase 6 confirmation.

**Accommodation** — Phase 7 **Option A** (recommended) as cost row `R32`: 14 apartment-months × $4,606.06 (a crew of 3 per apartment) + LH 225 individual nights × $103.2468 = **$87,715.37**. **Option B** (all-individual, 1,275 nights = $131,639.67) is documented in the same note as the not-taken alternative — a **$43,924.29** premium. No sharing with TCS (§5.2).
**Flights** — new cost row `R33`: 51 person-months × 2 returns × 2 legs × $220 = **$44,880.00** (assumption stated).

Bedding/pipe-surround import and spoil haulage are now **formula-linked to the take-off helper blocks** (`I902/M902`, `I971/M971`, `I892/M892`) so they follow the adopted pipe lengths automatically.

---

## Repair 10 — `00_ TCS Prelim & OH` populated bottom-up

Programme drivers re-based from Phase 7 (link [1] severed): 285 calendar days on site, 9.4 months, 40 work weeks, 197 work days.

| Bottom-up prelims | $ |
|---|---:|
| Supervisor ute 140 d @ $90 | 12,600.00 |
| Crew ute 166 crew-days @ $60 | 9,960.00 |
| Genset + fuel 285 d @ $45 (no site power, ITT §17.3) | 12,825.00 |
| Temporary potable water storage pods + distribution | 5,000.00 |
| Portable toilet / lunchroom / office 285 d each | 14,666.10 |
| 20 ft container (purchase) | 1,800.00 |
| Skip changeovers 9.4 | 2,254.12 |
| **Three-mobilisation allowance** (3 × 2 loads × 4 hr × $180 ex-ROK) | 4,320.00 |
| Project-specific insurances | 20,000.00 |
| **Total bottom-up prelims (`F89`)** | **83,425.22** |

**Cross-check vs the 5.5% allowance:** 5.5% × cost = **$63,670.40** → bottom-up is **+$19,754.82 (+31.0%)** over. This is a real exposure and is stated on the sheet: TPS must carry a standalone compound (§5.2, interface L5) with no shared prelims and no site power or water.

**Overheads:** 9.4 months × $40,000 = $376,000 full corporate rate, **less a 45% project allocation** (−$206,800) = **$169,200**. Against the 18% allowance of $208,375.86 that is **−$39,175.86 (−18.8%)** under.
**Combined:** bottom-up $252,625.22 vs allowance $272,046.26 = **−$19,421.04 (−7.1%)**.

> **STATED ASSUMPTION — Director to confirm:** charging 100% of corporate overhead to one project would over-recover, so a **45% allocation** is adopted for a project of this duration and value against expected concurrent workload.

Double-count control recorded on the sheet: the 140 LH supervision days and the accommodation are **memo-only here** (`D36`, `D53/D54` set to 0) because they are priced in the work-area labour blocks and at `R32` respectively. Crew remobilisation labour (T1-12) sits in Siteworks, not in the three-mobilisation plant-float line.

---

## Repair 11 — Stage split and `Sched3_Extract`

**Stage split** (`TCS $ Sched` M80:N88), on the `01_SCOPE_MATRIX` basis — mains-through-1B priced in 1A; PAM, bubblers and 1B's own connections in 1B:

| | Cell | ex GST |
|---|---|---:|
| 1A base sell (NBC + Siteworks + 146/166 of accommodation & flights) | `N81` | 1,490,620.98 |
| 1A PC sums | `N82` | 252,683.84 |
| **STAGE 1A TOTAL** | `N83` | **1,743,304.82** |
| 1B base sell (PAM sheet incl. the 1B site branches T2-09 + 20/166 share) | `N84` | 179,559.36 |
| 1B PC sums | `N85` | 86,930.00 |
| **STAGE 1B TOTAL** | `N86` | **266,489.36** |
| **GRAND TOTAL** | `N87` | **2,009,794.18** |
| Tie check `N64 + N78 − N87` | `N88` | **0.00** ✓ |

Accommodation and flights are split 146 / 20 crew-days per the Phase 7 stage allocation. The 1B site branch take-offs (T2-09, 4 crew-days) are carried on the PAM sheet, which acts as the 1B roll-up collector — the branch fitting is the 1A/1B line (interface L9).

**New sheet `Sched3_Extract`** maps our prices to the exact Paynters Schedule 3 line structure (D5): every TPS-allocated line of both stages, each showing Stage / Sch ref / schedule line / TPS treatment / amount / basis-and-qualification. Lump-sum lines are shown as carried inside the stage lump sums; PC Sums, provisional fees and schedule-of-rates lines are separately identified as the schedule requires. Excluded and Not-Ours lines are listed so **no schedule line is silent**.

It also carries a **schedule-of-rates build-up** for 1A 7.0 / 1B 5.0, so the tendered rates are derived rather than asserted — extra-over $/m³ = (crew + plant $/day) × (1/rock production − 1/normal production) + disposal/import:

| Rate line | $/m³ |
|---|---:|
| Soft rock — trench | 134.94 |
| Hard rock — trench | 421.99 |
| Soft rock — pit/structure | 225.94 |
| Hard rock — pit/structure | 683.19 |
| Unsuitable ground — removal & reinstatement | 189.72 |

Four rates per H002 n.24 (soft/hard × trench/pit), TPS excavations only, extra-over on Superintendent written direction. The three inconsistent rock regimes (ITT §18.2 vs H002 n.24 vs VOL38 §7.7) are stated and RFI'd (CL B5/A5) so H002 n.15 cannot bite.

**New sheet `EBC_Alternates`** holds the EBC register and both alternates. Nothing on it feeds the base roll-up; the markup factor is referenced live from `Q51`.

---

## Formula audit and forced recalculation

**Pre-recalc audit (openpyxl + package inspection):**

| Check | Result |
|---|---|
| `externalLink` parts in package / rels / `<externalReferences>` | **none** ✓ |
| Formulas containing `[n]` external indices | **0** ✓ |
| `#REF!` in any formula or value | **0** ✓ |
| Orphaned defined names (`#REF!`) | 14 found, all verified unreferenced, **removed** ✓ |
| References to non-existent sheets | **0** ✓ |
| Big-ticket totals reaching the summary (`W17`, `Z17`, `AC17`, `W31`) | **all 4** ✓ |
| New rows inside their sheet's `SUM` range | **all** ✓ |

**Native recalculation** — Excel COM (`New-Object -ComObject Excel.Application`), `ForceFullCalculation = true`, `CalculateFullRebuild()`, `CalculateUntilAsyncQueriesDone()`, `Save`, `Quit`, COM objects released via `Marshal::ReleaseComObject` + GC.

- `LinkSources(xlExcelLinks)` returned **null** — Excel confirms **no external links** remain.
- Formula-error census via `SpecialCells(xlCellTypeFormulas, xlErrors)` across all 12 sheets: **0 errors**.
- Re-read with `data_only=True`: **5,209** formulas, **0** with error values, **0** with no cached value.
- **14 computed-vs-expected checks, 0 divergent cells** — including `N64 = N16+N23+N29+N32+N33`, `R49/R39 = 1.4150` exactly, `R42/R43/R47` each = the correct percentage of `R39`, `N87 = N64 + N78 = N83 + N86`, tie check `N88 = 0.00`, and all three labour rates to the cent.

**Defect found and fixed during the audit:** two "Basis" note strings on `Sched3_Extract` began with `"= "`, so openpyxl wrote them into `<f>` elements as invalid formulas, which made Excel refuse to open the workbook. Both were rewritten as plain text and a workbook-wide sweep confirmed no other pseudo-formula strings. *(Diagnosis note: this presented as a generic COM open failure; it was isolated by a per-sheet bisect. A related trap was confirmed in passing — severing external links while `[n]` formulas remain anywhere also makes Excel reject the file. Our sever step replaces the formulas with literals, so the repaired model is clean.)*

---

## Repair 12 — Rule 4 fixture and equipment test (TENDER_PROMPT §2 Rule 4, third test)

Full test written to `_Tender_Control\07_Commercial_Reconciliation\EQUIPMENT_TEST_TPS.md`. **14 equipment items tested against all nine Rule 4 determinations** (supply · delivery · storage · installation · fixings/accessories · connection · testing/commissioning · controls · supply ownership): **12 complete on first pass, 2 fixings gaps + 1 cross-cutting storage gap closed, 4 duplicate installation tokens neutralised.** No item remains MISSING.

**The `Installation_MH` tokens were duplicates, not shortfalls.** The big-ticket blocks carried token *dollar* figures labelled `Installation_MH` — GIT $250, HW pump $200, NBC HWUs $600, PAM HWU $200 ($1,250 total). Testing each against Phase 7 showed installation labour is already fully loaded as crew-days:

| Token | Was | Now | Covering Phase 7 activity |
|---|---:|---:|---|
| `W16` GIT | 250 | **0** | **T1-08** — 8 crew-days Crew 1; rate basis explicitly *"GIT excavation/set"*; 3–5 T excavator 4 d + crane 1 d. Commissioning **T5-02** |
| `Z16` HW pump | 200 | **0** | **T4-03** — 3 crew-days Crew 4, *"2x Rheem 315L HWU + HW circulating pump + flow/return loop"* |
| `AC16` NBC HWUs | 600 | **0** | **T4-03** (same activity; crane truck 0.5 d for HWU set). Commissioning **T5-06** *"…HWU…"* |
| `W30` PAM HWU | 200 | **0** | **T4-06** — 1 crew-day Crew 4, *"PAM Rheem 50L HWU + TMV + Ø32 check-meter assembly"* |

Each token cell keeps an in-cell note naming the covering activity ID, so the labour is traceable rather than lost, and cannot be re-added later by someone reading a $0 as an omission.

> **Recorded so it is not re-litigated:** searching the Phase 7 `Activity` column for "hot water" returns nothing, which reads like a missing HWU/pump installation. It is a column artefact — "Hot water" is the value in the **`System`** column, while the **`Activity`** text names the Rheem units and the pump directly. Both activities were already loaded (NBC Crew 4 = 21 crew-days includes T4-03's 3; PAM Crew 4 = 5 includes T4-06's 1). Verified against `PROGRAMME_LABOUR_PLANT.xlsx`, not inferred.

**Genuine gaps found and closed:**

| Gap | Fix | Basis |
|---|---|---|
| HWU **SS plinth/stand + fixings** priced nowhere. H-NBC-301/H-PAM-301 call up safe tray + SS plinth + seismic strap; the tray was in the big-ticket block and the strap in the seismic allowance, but the plinth was in neither | NBC r933 2 EA @ $260 · PAM r854 1 EA @ $260 | Estimator basis — fabricated 316 SS plinth ~$220 + dynabolt/Unistrut fixings ~$40. Materials only; install labour already in T4-03/T4-06 |
| **Storage** — a distinct Rule 4 determination, costed for no item | SW r153 $1,200 long-lead equipment storage & double-handling allowance | Long leads per Phase 7: 316 SS 10–14 wks, booster + cabinet 10–12 wks, Rheem 4–6 wks, Stoddart specials 8–12 wks; supplier storage charges bite after 30 days (Humes Service Fees basis). Explicitly **not** a duplicate of the 20 ft site container (Prelim & OH `B80`) — that is the on-site store, this covers off-site holding and the extra handling movement |

**Net effect:** cost +$1,980 pre-contingency (+$2,305.20 after contingency) → +$3,261.86 of sell at the 41.5% chain, less $1,250 of removed tokens = **+$2,011.86**. Stage 1A +$1,777.74, Stage 1B +$234.12.

**Rule 4 wording controls captured for the submission** (full list in the test document): the Billi units are **Principal-supplied — install and connect only**, never "Billi units included"; fixture supply is a separate PC line, never a blanket "fixtures included"; fountains/bubblers are PC Sums with **slabs by others and signage excluded**; extinguishers are EBC with an add-price held; backflow **registration** rides with the excluded approval lodgement (X2); electrical isolators, panels and control cabling to the HWUs, pump and chilled fountains are by the electrical trade.

### Big-ticket markup quantum — for Director decision (structure left AS IS)

The four big-ticket blocks take purchase × 1.15 and add freight un-marked-up, sitting outside the normal cost→markup chain. **Unchanged**, but now quantified:

| Item | Cost (purchase + freight) | Current sell | Normal chain (cost × 1.415) | Delta |
|---|---:|---:|---:|---:|
| 1500 L Viking GIT + lids | 8,773.28 | 10,051.77 | 12,414.19 | +2,362.42 |
| HW circulating pump set | 6,925.83 | 7,942.20 | 9,800.05 | +1,857.84 |
| Rheem 315 L HWU × 2 + safe trays | 7,282.18 | 8,329.51 | 10,304.28 | +1,974.78 |
| Rheem 50 L HWU × 1 + safe tray | 2,218.88 | 2,529.21 | 3,139.72 | +610.50 |
| **TOTAL** | **25,200.17** | **28,852.70** | **35,658.24** | **+6,805.55** |

Current effective margin on this equipment is **14.49%** against the model's **41.50%**. Adopting the normal chain would add **$6,805.55** (1A +$6,195.05, 1B +$610.50), taking the grand total to **$2,016,599.73**. Note that **$850 of freight currently carries no margin at all**, and that — now that installation is proven to sit in the crew-day blocks — the ×1.15 is doing only a supply-margin job, not a disguised installation allowance.

---

## Open items — NOT closed by this repair

1. **Big-ticket equipment carries only ×1.15 + freight — no prelims/O/H/profit.** Pre-existing architecture (audit defect 7), **preserved** as instructed. Now precisely quantified above: **+$6,805.55** if run through the normal 41.5% chain. **Director decision.**
2. **Benchmark-derived rates pending RFQ:** Ø200 HDPE PE100 SDR11 DN250 (Gap #5); 316 SS press **fittings** (Gap #2); seismic hardware (Gap #3); articulation joints (Gap #4); non-chilled CF400 (Gap #6). All tagged in-cell.
3. **June-2024 cached rates** now frozen as literals in `Material Rates_Master`, `Equip&HIRE_Master` and `Misc Subbie Rates_Master` are ≥2 years old at a 2027 start — Phase 5 re-sourcing still outstanding; every affected row carries its Source tag.
4. **Fixture counts are LOW confidence** (Opens #18): 7 of 9 architectural sheets were never counted. The adopted 93 NBC / 15 PAM counts drive both the fit-off labour and the PC-sum extension. Phase 4 recount + line-by-line Tradelink reconciliation is **mandatory** before award.
5. **45% corporate overhead allocation** is a stated assumption awaiting Director confirmation.
6. **Bottom-up prelims exceed the 5.5% allowance by 31%** — lift the percentage or carry the delta as a priced line.
7. Quantity RFIs still open: DP counts (Opens #23), fire-service extent vs AS2419.1 (Opens #13), TMV count basis (Opens #28), grease arrestor size (Opens #24), PAM "TR" fixture type (Opens #22), rock regime (CL B5/A5).
8. Escalation is applied **once** (PE ×1.38 on the Ø200 main). Rates frozen from the 2024 comparisons have **not** been escalated to 2027 — doing so at Phase 5 must not double-count against the ×1.38/×1.18 factors already in the sheets.

---

*Repairs 1–11 executed 26 Jul 2026; repair 12 (Rule 4 equipment test) 27 Jul 2026. Original master workbook unmodified.*
*Outputs: `Working_Cost_Models\TPS\ROK_TPS_CostModel_V2.xlsx` · `Working_Cost_Models\TPS\TPS_CHANGE_LOG.md` · `_Tender_Control\07_Commercial_Reconciliation\EQUIPMENT_TEST_TPS.md`.*
