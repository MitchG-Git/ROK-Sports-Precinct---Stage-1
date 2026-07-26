# TCS_CHANGE_LOG — MasterCostSheet_Civ.V1 → ROK_TCS_CostModel_V2

**Entity:** TriCore Civil Services Pty Ltd (TCS) — ABN 89 195 291 365 · civil stormwater
**Tender:** TEN16699 ROK Sports Precinct Stage 1A & 1B · 554-700 Yaamba Rd, Norman Gardens QLD
**Old:** `TriCore Docs\...\MasterCostSheet_Civ.V1.xlsx` — TCS Quote #2372, 16-07-2026 (READ ONLY; never modified)
**New:** `Working_Cost_Models\TCS\ROK_TCS_CostModel_V2.xlsx` — TCS Quote #2372-V2, 26-07-2026
**Companion:** `MIGRATION_RECONCILIATION.xlsx` (Summary / Bridge / Register 431 rows / CellIndex 2,805 cells)
**All sums ex GST.**

---

## 1. HEADLINE

| | Old (V1) | New (V2) |
|---|---|---|
| **Total ex GST** | **$890,849.95** | **$2,760,962.08** |
| What it contained | Materials + quarry only, marked up | Materials + **labour + plant + subbies + accommodation**, marked up |
| Labour | **$0** | $638,321.02 (223 crew-days) |
| Plant | **$0** | $168,088.85 |
| Accommodation / FIFO travel | **$0 (no logic existed)** | $111,365.80 |
| Grated trench drains | **$0 — orphaned out of the total** | Reinstated in full |
| Effective markup on cost | 45.73% (labelled 41.5%) | **41.5% (as directed)** |
| GST | 10% line present on the Hyd sibling; Civ V1 ex-GST | Ex-GST throughout, stated on every summary |

**Movement: +$1,870,112.13 (+209.9%).** The movement is not a price increase — it is the cost of work the old model never priced. The old figure was never a complete offer.

---

## 2. FORMULA DEFECTS FIXED

| # | Old cell(s) | Defect | Fix in V2 |
|---|---|---|---|
| D1 | `SW Zone Sumry` H11 `=SUM(F13:F19)` | **Labour = $0.** Rate cells were live (LH $822.50/day, crew $2,152.50/day) but every day-quantity cell D13:D19 was empty. The sheet *looked* priced. | Labour rebuilt from Phase 7 crew-days × FIFO crew-day rate. 212 cd (1A) + 11 cd (1B). Every day-quantity is a visible blue input. |
| D2 | `SW Zone Sumry` H30 `=SUM(F30:F39)` | **Plant = $0.** Same defect — 10 plant rows with rates, all quantities empty. | Plant blocks on both stage sheets, days from the Phase 7 plant roll-up, rates from `Equip_Master`. |
| D3 | `SW_Mataterial` K258 `=SUM(I243:I257)` = **$164,860.30** | **Orphaned formula.** The whole grated-trench/Hauraton package computed correctly in columns H/I/K but **K258 fed no roll-up cell** — F294's `=SUM(F7:F293)` only sums column F. The old $890,849.95 contained **zero dollars of trench drains**. | Package reinstated across `Stage1A_Drainage` G1–G5 and `Stage1B_Drainage` G1–G4, on the Reece/Hauraton quote basis (≈$162,349, which verifies the old $164,860 figure), **including excavation and quarry** per the reinstatement direction. |
| D4 | `SW_Mataterial` G269/I269/**J269** = $10,865 | Second orphan: 2,173 m of 100 mm socked ag pipe priced in columns outside the F-sum. | Not reinstated — subsoil / type-2 strip filter is **excluded scope** ("by others", SCOPE_MATRIX 2.3-x2 / 2.5-x3). Recorded on the `EBC` sheet so the exclusion is a stated position, not a silent gap. |
| D5 | `Prelim_OH-Check` F42, F47 | Both totals `=SUM(...)` over rows whose REQ quantities were all zero → **$0**, yet `V1` T29/T30 displayed them as the "Manual Calc" cross-check. A cross-check that always passed because both sides were empty. | New `Prelim_OH` sheet: bottom-up build (LH supervision, establishment, temp services incl. temp water cartage, EDQ remob, ADAC/CCTV/as-cons) with a live **variance row and variance %** against the 5.5% allowance. |
| D6 | `V1` R32/R35 | **Markup compounding** — see §3. | Re-based; both effective percentages disclosed. |
| D7 | `SW_Mataterial` F16 | 375 rubber rings priced as **qty 1 @ $1,435.20** — a unit error (that is a lot rate sitting in an "each" cell). | Formula-driven: `=ROUNDUP(pipe metres / 2.44, 0)` = 293 rings @ $4.80 (Humes). |
| D8 | `V1` W10/W11 | WSUD "install estimate $6,000" and "fuel levy estimate $2,500" buried inside the WSUD supply block — installation money hidden inside a supply line. | Installation is now an 8 crew-day Phase 7 activity (C-05) with excavator, 50 t crane, shields and dewatering, priced in the **base lump sum, not the PC** (locked §5.3). Fuel levy carried as a qualification, not a guess. |
| D9 | `V1` S13 `=((R13/$R$26)*($R$36-$R$26))+R13` | Opaque ratio-scaling markup formula — unauditable. | Replaced by an explicit chain: `cost × (1 + 5.5% + 18% + 18%)`, each percentage its own visible input cell. |
| D10 | `SW_Pit Takeoff` (498 cells) | Three parallel "manual calc" versions of the same pit grid, producing **negative riser heights** (e.g. −0.98 m, −1.455 m) — internally inconsistent working. | Not carried. Superseded by the ADOPTED structure schedule (F1310's 121 unique pits + 20 C-series end structures = 141, Rule 3), priced as complete precast assemblies. |
| D11 | `SW_insitu Takeoff` J27 | In-situ chamber concrete computed **$0** (no volumes entered) while presenting as a priced block. | Dropped with reason — no cast-in-situ chambers in the adopted take-off. 32 MPa rate preserved (`Materials_Master` M65) for the spillway build-up held on `EBC`. |
| D12 | `SW_Mataterial` F295 | Materials contingency **0.10**. | Re-based to the directed **×1.18**, materials only. |
| D13 | `SW_Mataterial` C314 | Trench-metre driver summed pipe **and culvert** metres (1,883 m) into one bedding/spoil calculation. | Bedding stone and spoil haulage now derive from an explicit pipe-metre sum (1,637.22 m) with culvert extra-over priced separately (`Q2`, NewItems #2). |

---

## 3. MARKUP RE-BASING (the commercial correction)

**Old chain — `V1`:**
```
R29  Prelim  = R26 × 5.5%          (on cost)          $29,445.03
R30  O/H     = R26 × 18%           (on cost)          $96,365.56
R32  SubTot  = cost + Prelim + O/H                   $661,174.78
R35  Profit  = R32 × 18%   ← PROFIT ON COST+P+OH     $119,011.46
R36  Total   = R32 + R35                             $780,186.25
Q38  Label   = SUM(Q29:Q37) = 0.415  ("41.5%")
```
Effective markup actually applied: **$780,186.25 / $535,364.20 − 1 = 45.73%** against a displayed label of **41.5%** — a **4.23 percentage-point** overstatement baked into every price the old model produced.

**New chain — `TCS $ Sched`:** Prelims 5.5% + O/H 18% + Profit 18%, **each calculated on total cost, none compounded on another**:
```
Lump sum = Cost × (1 + 5.5% + 18% + 18%) = Cost × 1.415   →  41.5% exactly, as directed
```
where `Cost` = escalated-and-contingent materials + labour + plant + subbies + accommodation.

Precisely: old factor = (1 + 0.055 + 0.18) × 1.18 = **1.45730**; new factor = **1.41500**; difference **4.2300 percentage points**. On the new total cost of $1,872,208.01 the re-basing is worth **−$79,194.40** — a real reduction in the offer, not a presentational change. Both figures are disclosed on `TCS $ Sched` (cell H8) and on `Cover_Control`.

**Intermediate removed:** old `R32` existed *only* to compound profit onto prelims and O/H. It has no counterpart in V2.

---

## 4. EXTERNAL LINK SEVERANCE RECORD

| Link | Where it fed | Disposition |
|---|---|---|
| `\\SBSERVER\Users\tony.rieck\My Documents\60 Richards St Loganlea Costings V2.xls` | Inherited into `MasterCostSheet_Civ.V1` through template lineage from an **unrelated 2018-era Loganlea project** | **SEVERED.** Not carried into V2 in any form. |
| `[2] CQU ROK_Staff Costing.V1_Steph.xlsx` (SharePoint) | All labour rates in the Hyd sibling workbook | Cached monthly bases **frozen** from `dumps/CQUHyd__LabourProject Rates_Master.csv` and re-entered as stated blue inputs on `LabourRates_Master` (D11:D13) with the source named in column I. No link. |
| `[1] CQU ROK_PROGRAM - MASTER.V1.xlsx` (SharePoint) | Hyd `00_ TCS Prelim & OH` C9:C12, D45 | Not carried. Prelims rebuilt bottom-up from Phase 7. |
| `[3] 240614 - Pipe & Fittings - Price Comparison.xlsx` | Material rates (June 2024, CQU-Hydrant era) | Not carried — **every adopted rate re-sourced** at Phase 5 against current quotes; ≥2-year-old cached rates rejected. |
| `[4] 240614 - Suppliers Subbies - Price Comparison.xlsx` | Equip & subbie masters | Not carried; `Equip_Master` rates re-sourced, old Civ register preserved as a reference block. |
| 15 named ranges (several orphaned) | `MasterCostSheet_Civ.V1` | Not carried — V2 uses explicit `Sheet!Cell` references throughout. |

**Verified:** a formula audit of V2 found **0 external references**, **0 `#REF!`/`#VALUE!`/any error values**, and **0 formulas without a computed result** after native Excel recalculation.

---

## 5. BASIS CHANGES (beyond defect repair)

1. **Quantities** — pricing basis is now the ADOPTED column of `QUANTITY_RECONCILIATION.xlsx` (TCS_Civil + NewItems). Largest: 225 PVC DWV line 81 **180.93 → 115.45 m** (printed long-section chainage governs; continuation double-measure removed, Opens #1); RCP375 combined **725.47 → 714.9 m** with CL4 30.40 → 12.0 m re-split; GT total **622.09 → 608.5 m**; structures **131 → 141**.
2. **Labour** — local non-FIFO rates ($94.00/hr LH, $88.00/hr trades, $70.00/hr T/A on a 24-day/8.75-hr month) **superseded** by ROK FIFO Roster Example #3 (21 work-days, 10-hr days, 210 hrs/month) × the directed 1.08 uplift: **LH $132.9634/hr · Trades $101.6458/hr · T/A $82.9510/hr**, crew (2 Trades + 1 T/A) **$2,862.43/crew-day**. Whole cascade (month → hour/day/week) is formula-driven from three monthly-base inputs.
3. **Escalation to 2027** — applied **once**, only where `MATERIAL_QUOTE_REGISTER` KeyRates confirms the rate is not already loaded: ×1.38 PE/PVC (incl. PP Stormpro and Hauraton Recyfix PE-PP channel), ×1.15 subbies, ×1.20 delivery. Concrete/precast/quarry carry **no** directed category factor — that escalation risk sits inside the ×1.18 contingency plus a re-quote condition at award. **The per-rate decision is recorded against every rate** in `Materials_Master` column I.
4. **Supplier selection** — cheaper compliant rate per item: Humes REV2 (RCP, all RCBC crowns, all BCC headwalls, twin-375 headwall), Reece (winged 375 headwall $317.05, PP Stormpro, full Hauraton package, 100 PVC), Tradelink 1065005 R1 (225/150 PVC, 600 pits/grates), Jaybro (150/225/300 headwalls + a required freight adder — their rates exclude freight). **Humes REV1 → REV2** adopted (net $4,883.79 lower). The Humes-vs-Reece take-off discrepancy (**RCP375 299 vs 262 lengths**; LBC1500×600 13 vs 8) is noted at `Materials_Master` M01/M26 — **our adopted 714.9 m governs**, and both offers are schedule-of-rates so the quantity risk is ours.
5. **WSUD** — Atlan $88,838 (a same-day-validity "high level estimate only") **superseded** by the only project-specific price for the nominated system: Reece Q-459014431 **$90,064.63 + $7,142.10 freight**, carried as a **PC Sum +15% = $111,787.74**, shown separately from the lump sum. **Installation is in the base lump sum, not the PC** (locked §5.3). A direct Ocean Protect re-quote on the MUSIC model is still required (Gap #1 / Opens #10).
6. **Trench drains REINSTATED** — see D3. GT6 grate substitution (PRO100 D400 code 47245 vs the PRO200 G-tec offered) flagged for verification (Gap #7); the Reece `$198.00/m` annotation against the 550 m Fibretec line vs the extended $232.94/m is flagged — **a $19,217 delta to confirm with Reece**.
7. **Kerb chutes** — base **excludes** them per Denis 24-Jul; the full add-price (9 chutes + rock + matting + 9 crew-days) is costed on the `EBC` sheet and marked **"Director decision D6-F1"**. Both positions live; neither closed.
8. **Rock** — base allows only the geotech-anticipated band (NQL2024-0320: refusal at 25/36 locations, XW rock 0.2–2.2 m at 6 pits; ~15% of trench metres at reduced production = activity A-08, 10 crew-days). Extra-over rates are tendered separately as **four rates — soft and hard rock × trenches and pits** (H002 n.24) plus unsuitable ground, built up from crew + plant + production and sold at ×1.415.
9. **Detention basin earthworks / concrete spillway — NOT PRICED.** Carried as a **$0 flagged row** (`Stage1A_Drainage` X1, labour B-07 = 0 crew-days) with "allocation RFI pending" (Opens #26 + Director). The full spillway build-up is held on `EBC` with reinstatement instructions. Basin bulk shaping was never quantified in any drawing set (F1305 annotation only) and cannot be priced.
10. **Accommodation** — Option A (apartments housing 3, LH on nightly individual) **adopted at $75,365.80**; Option B (all individual nightly) shown at $116,152.65 for comparison. FIFO return flights add $36,000 (45 person-months × 2 returns × 2 legs × $200 ex GST). Total $111,365.80, allocated 1A/1B pro-rata crew-days.
11. **Not TCS** — the Ø100 sewer rising main (110 m allowance), the QMax pump station (excluded per Addendum 2), and the **$20,000 provisional connection fees** are all TPS-side and appear nowhere in this model. Recorded on `EBC` so their absence is deliberate and evidenced.

---

## 6. ARCHITECTURE (CQU/Hyd pattern)

`Cover_Control` · `TCS $ Sched` · `Stage1A_Drainage` · `Stage1B_Drainage` · `LabourRates_Master` · `Materials_Master` · `Equip_Master` · `Accommodation` · `Prelim_OH` · `EBC` · `Sched3_Extract`

Every derived cell is a formula. Blue = hardcoded input, green = cross-sheet link, yellow = key assumption, pink = flagged/pending item.

---

## 7. OPEN ITEMS CARRIED INTO V2

| Ref | Item |
|---|---|
| **D6-F1** | Kerb chutes — Director decision. Both positions costed (`EBC` E1). |
| **Opens #26** | Detention basin earthworks + spillway allocation — RFI + Director. $0 in base (`EBC` E2). |
| **Prelim cross-check** | Bottom-up prelims **$222,117.36** vs the 5.5% allowance **$102,971.44** → allowance short by **$119,145.92 (bottom-up is 115.7% above it)**. Driven mainly by LH supervision (120 days = $159,556). **This needs a Director decision before submission** — see §8. |
| **Gap #1 / Opens #10** | Ocean Protect direct re-quote for the 22-cartridge DN3300 StormFilter (MUSIC model required). |
| **Gap #7** | GT6 grate substitution (PRO100 D400 47245 vs PRO200 G-tec offered). |
| **Reece anomaly** | $198.00/m vs $232.94/m on the 550 m Fibretec line — $19,217 delta. |
| **Opens #2/#3** | RCP375 CL4 extent and chainage re-sum. |
| **Opens #4/#7/#8/#9** | 1200AC/P2P counts; GT2 "4 pits"; C09A/B details missing; F1310 schedule defects. |
| **Plant registers** | 50 t crane, franna and trench shields are **allowances** — absent from every hire register; quote at award (`Equip_Master`, flagged). |
| **Validity cliff** | Every quote on file expires Aug-2026 against a 2027 commencement. Escalation carried once; re-quote at award. |

---

## 8. THE ONE THING THAT NEEDS A DECISION

The bottom-up prelims cross-check that the old model could never perform (because both sides were zero) now shows the **5.5% prelims allowance does not cover TCS's actual preliminaries** on this job: **$102,971 allowed vs $222,117 built up**, a **$119,146 shortfall**.

The dominant cause is Leading Hand supervision — 120 days × $1,329.63 = **$159,556** on the FIFO basis, which by itself exceeds the entire 5.5% pool. The directed markup structure has been applied exactly as instructed and the shortfall left visible rather than absorbed by quietly moving supervision into direct cost.

**Three options, none taken unilaterally:**
1. Move LH supervision into direct cost (it then attracts prelims + O/H + profit like any other cost) — raises the offer by roughly $226k and is the most defensible commercially.
2. Raise the prelims percentage from 5.5% to about 12% on this job.
3. Accept the shortfall against O/H and profit — a real margin reduction of $119k.

Flagged for Mitch/Director before the tender is submitted.
