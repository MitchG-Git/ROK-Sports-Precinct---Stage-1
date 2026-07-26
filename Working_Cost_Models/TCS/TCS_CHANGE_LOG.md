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
| **Total ex GST** | **$890,849.95** | **$2,986,733.98** |
| What it contained | Materials + quarry only, marked up | Materials + **labour incl. LH supervision + plant + subbies + accommodation**, marked up |
| Crew labour | **$0** | $638,321.02 (223 crew-days) |
| Leading Hand supervision | **$0** | $159,556.11 (120 LH-days, **direct labour**) |
| Plant | **$0** | $168,088.85 |
| Accommodation / FIFO travel | **$0 (no logic existed)** | $111,365.80 |
| Grated trench drains | **$0 — orphaned out of the total** | Reinstated in full |
| Effective markup on cost | 45.73% (labelled 41.5%) | **41.5% (as directed)** |
| GST | 10% line present on the Hyd sibling; Civ V1 ex-GST | Ex-GST throughout, stated on every summary |

**Movement: +$2,095,884.03 (+235.3%).** The movement is not a price increase — it is the cost of work the old model never priced. The old figure was never a complete offer.

**Stage split:** Stage 1A lump sum $2,761,814.98 + WSUD PC sum $111,787.74 = **$2,873,602.72**; Stage 1B lump sum **$113,131.26**.

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
| **Prelim cross-check** | ~~Shortfall~~ **RESOLVED at §9.** Bottom-up true preliminaries **$62,561.25** vs the 5.5% allowance **$111,747.03** → allowance covers with a **$49,185.78 surplus** (bottom-up is **44.0% below** the allowance). |
| **Gap #1 / Opens #10** | Ocean Protect direct re-quote for the 22-cartridge DN3300 StormFilter (MUSIC model required). |
| **Gap #7** | GT6 grate substitution (PRO100 D400 47245 vs PRO200 G-tec offered). |
| **Reece anomaly** | $198.00/m vs $232.94/m on the 550 m Fibretec line — $19,217 delta. |
| **Opens #2/#3** | RCP375 CL4 extent and chainage re-sum. |
| **Opens #4/#7/#8/#9** | 1200AC/P2P counts; GT2 "4 pits"; C09A/B details missing; F1310 schedule defects. |
| **Plant registers** | 50 t crane, franna and trench shields are **allowances** — absent from every hire register; quote at award (`Equip_Master`, flagged). |
| **Validity cliff** | Every quote on file expires Aug-2026 against a 2027 commencement. Escalation carried once; re-quote at award. |

---

## 8. PRELIMS CROSS-CHECK — RESULT

The bottom-up prelims cross-check that the old model could never perform (because both sides read zero) now passes:

| | Amount |
|---|---|
| Bottom-up TRUE preliminaries | **$62,561.25** |
| 5.5% allowance (5.5% × $2,031,764.12 total cost) | **$111,747.03** |
| **Variance (surplus)** | **+$49,185.78** |
| **Variance %** | **−44.0%** (bottom-up sits 44% below the allowance) |

The 5.5% allowance comfortably covers establishment non-labour, temporary services (incl. temp water cartage), the EDQ remobilisation line and the ADAC/CCTV/as-constructed deliverables. **No Director decision is required** — see §9 for how this was resolved.

---

## 9. CORRECTION — LEADING HAND SUPERVISION RETURNED TO DIRECT LABOUR

### The departure found

An earlier build of V2 placed the 120 Leading Hand supervision days in the **`Prelim_OH` pool**, funded from the 5.5% prelims allowance. That was a **departure from TriCore's existing commercial methodology** and it produced a false $119,146 prelims shortfall.

### The evidence

`MasterCostSheet_Civ.V1.xlsx`, sheet **`SW Zone Sumry`**, section **B "Labour"** (total at H9, formula `H11 =SUM(F13:F19)`):

```
A8  = B                              <- section B
B8  = Labour                         <- section heading
B13 = TRADESMAN_LEADING HAND         <- the Leading Hand
C13 = Day                            <- priced by the day
E13 = ='Staff Rates'!E17  ($822.50)  <- linked to the LH day rate
F13 = =E13*D13                       <- extends into the labour total
```

The Leading Hand is **row 13 of the work-area labour block**, extending straight into `TOTAL Labour`. TriCore prices supervision as **direct cost of the work**, not as a preliminary. `MasterCostSheet_Hyd.V1` follows the identical pattern. TENDER_PROMPT §5.4 directs that the existing TriCore commercial structure and methodology be preserved; §8-PHASE 6 directs that a defect found be corrected and shown here.

### The correction

1. The 120 LH-days moved **out of `Prelim_OH` and into the direct labour blocks** of both stage sheets as their own line **A-14 "Leading Hand supervision — site-wide"**, at the LH day rate from `LabourRates_Master` ($1,329.6343/day).
2. **Allocated pro-rata to crew-days**, consistent with the accommodation allocation: **1A 114.1 days = $151,711.27** · **1B 5.9 days = $7,844.84** · total 120.0 days = $159,556.11.
3. The labour block was restructured so the allocation cannot become circular: **`B1 — Crew labour subtotal`** (the `SUM` over activity rows, which still carries the crew-day count used by the accommodation and LH pro-rata formulas), then the **A-14 LH row**, then **`B — LABOUR TOTAL` = crew + LH**. Accommodation and the `Sched3_Extract` GT allocation continue to divide by **crew-days**, excluding LH days.
4. `Prelim_OH` **retains the LH row at $0 for traceability**, with the note *"reallocated to direct labour per TriCore methodology (old Civ SW Zone Sumry B13) — see change log"*, and the rate still shown for reference.
5. The `Sched3_Extract` grated-trench component now carries its share of LH supervision (36 crew-days pro-rata), so the Schedule 3 transfer lines remain a true cost split.
6. `Cover_Control` assumption #4 rewritten; `MIGRATION_RECONCILIATION.xlsx` carries a dedicated register row against `SW Zone Sumry` B13/C13/E13/F13 recording the evidence, the departure and the correction.

### Price movement caused by this correction

| | Before | After | Movement |
|---|---|---|---|
| Stage 1A lump sum | $2,547,143.53 | **$2,761,814.98** | **+$214,671.45** |
| Stage 1B lump sum | $102,030.81 | **$113,131.26** | **+$11,100.45** |
| WSUD PC sum | $111,787.74 | $111,787.74 | unchanged |
| **Grand total ex GST** | $2,760,962.08 | **$2,986,733.98** | **+$225,771.90** |

The movement is exactly **$159,556.11 × 1.415 = $225,771.90** — the LH supervision cost now correctly attracting prelims, overhead and profit as direct cost does, instead of being absorbed inside a fixed 5.5% pool that could not fund it.

**Net commercial effect:** the offer rises $225,772, and the prelims pool swings from a $119,146 shortfall to a $49,186 surplus. Supervision is recovered properly rather than eroding overhead and profit.

---

## 10. PHASE A REMEDIATION — 27 JULY 2026 (Director-authorised)

Three surgical edits executed on `ROK_TCS_CostModel_V2.xlsx` under the "cell before sentence, both directions" standard. Native Excel recalculation forced via COM after editing: **600 formulas · 0 errors · 0 `#REF!`/`#VALUE!`/`#DIV/0!` · 0 external references · 0 formulas without a computed result.**

### 10.1 Headline movement

| | Before | After | Movement |
|---|---:|---:|---:|
| Stage 1A lump sum | $2,761,814.98 | **$2,815,365.59** | +$53,550.62 |
| WSUD PC sum | $111,787.74 | $111,787.74 | unchanged |
| Stage 1A incl PC | $2,873,602.72 | **$2,927,153.33** | +$53,550.62 |
| Stage 1B lump sum | $113,131.26 | **$117,646.13** | +$4,514.87 |
| **GRAND TOTAL ex GST (`TCS $ Sched`!D46)** | **$2,986,733.98** | **$3,044,799.46** | **+$58,065.49 (+1.944%)** |

**Tolerance band check: PASS, but at the margin.** Locked baseline $2,986,733.98, 2% band $2,926,999.30 – $3,046,468.66. The new total sits **$1,669.20 below the upper limit (1.944% of a permitted 2%)**. Any further base addition of more than about $1,180 of pre-contingency material cost will breach the band.

**Component split reconciles:** $2,815,365.59 (1A lump sum) + $111,787.74 (WSUD PC) + $117,646.13 (1B lump sum) = **$3,044,799.46** = `TCS $ Sched`!D46. Verified.

### 10.2 Edit 1 — RPEQ certification EXCLUDED (Director decision, both entities)

| Cell | Before | After |
|---|---|---|
| `Prelim_OH`!C26 | `1` (lot) | **`0`** |
| `Prelim_OH`!F26 (`=C26*E26`) | `$3,500.00` | **`$0.00`** |
| `Prelim_OH`!E26 | `3500` | `3500` — **rate retained for reference** |
| `Prelim_OH`!G26 | "Estimator allowance; surveyor pickup attendance already in Stage subbies." | Rewritten — records the Director decision, the date, and the as-constructed consequence below |

Row **not deleted**; quantity zeroed and annotated so the audit trail survives — the same convention already used for the Leading Hand row at `Prelim_OH`!B6.

**Cascade chain (verified cell by cell):**
`Prelim_OH`!F26 → `Prelim_OH`!F29 (`=SUM(F5:F27)`) **$62,561.25 → $59,061.25** → `Prelim_OH`!F32 variance and F33 variance %. **The chain stops there.** `Prelim_OH` is a bottom-up cross-check sheet only — its own header (`Prelim_OH`!B2) states *"Items here are NOT added to the sell — they are funded from the 5.5% pool"*, and the sell computes prelims independently at `TCS $ Sched`!D21 (`=D20*$C$8`) and D41 (`=D40*$C$8`). **Removing the $3,500 therefore has ZERO effect on the grand total.** The entire +$58,065.49 movement above comes from Edit 2.

Post-edit prelims cross-check: allowance `Prelim_OH`!F31 **$114,003.99** (risen with the Edit 2 cost base) vs bottom-up F29 **$59,061.25** → surplus **$54,942.74**, bottom-up **48.2% below** the allowance (was 44.0%).

> **FLAGGED FOR THE DIRECTOR — NOT ACTED ON.** The removed line read *"RPEQ certification **+ as-constructed drawing preparation**"*. Removing $3,500 removes **both**. As-constructeds are now **partially but not wholly covered**: ADAC XML preparation + validation remains separately priced at `Prelim_OH`!B25/F25 (**$4,500**), and as-constructed survey / ADAC attendance labour remains at `Stage1A_Drainage` A-10 (3 crew-days) and `Stage1B_Drainage` A-13, with surveyor as-con pickup at `Stage1A_Drainage`!C126 (5 days). What is now unpriced is the **RPEQ certification itself and the drafting of the as-constructed drawing sheets**. **No compensating adjustment has been made.** Stated here as a factual consequence for decision.

### 10.3 Edit 2 — Grated-trench bedding/surround priced into base (locked §5.3)

**Basis adopted: CONCRETE SURROUND + CRUSHED ROCK BASE, measured off the dimensioned drawing detail — not the pipe-trench quarry factor.**

The prior audit (`EQUIPMENT_TEST_TCS.md` §5, `UNBACKED_CLAIMS_AUDIT.md` UC-03) recorded that *"no Hauraton install guide, manufacturer detail or drawing note exists anywhere in the repository"* and treated the basis as a Rule 2 "cannot determine". **That finding is superseded.** The detail does exist and is dimensioned, on the tendered drawing set:

**Source: VOL 15 `SE_12306_F1320-T1` STORMWATER DRAINAGE DETAILS SHEET 1** — three typical sections, read directly off the PDF and cross-checked against the register transcription at `_Tender_Control\01_Document_Register\notes\vol15_layouts_pits_details.md` line 80 (*"Pro 200 Type 010 trench (concrete surround, crushed rock base)"*):

| Detail | Concrete surround | Channel body | Crushed rock base |
|---|---|---|---|
| HAURATON RECYFIX PRO 200 TYPE 10 / TYPE 010 TRENCH | **500 wide** (119 + 262 + 119) x **350 deep** (200 channel + 150 under) | 262 x 200 | **100 thick**, 150 beyond concrete each side = **800 wide** |
| HAURATON RECYFIX PRO 100 TYPE 010 TRENCH | **450 wide** (145 + 160 + 145) x **350 deep** | 160 x 200 | **100 thick**, 150 each side = **750 wide** |

Channel depth 200 mm is confirmed independently by F1320 note 1 (*"all grated trench depths are 200 mm"*).

Derived unit volumes: concrete **PRO200 = 0.500 x 0.350 − 0.262 x 0.200 = 0.1226 m3/m**; **PRO100 = 0.450 x 0.350 − 0.160 x 0.200 = 0.1255 m3/m**. Crushed rock **PRO200 = 0.080 m3/m**; **PRO100 = 0.075 m3/m**.

**Rows added** (inserted via Excel COM so every downstream reference re-pointed natively; new IDs Q4/Q5 in 1A and Q2/Q3 in 1B do not collide with existing IDs, which retain their meaning in all existing registers):

| Cell | Item | Formula | Qty | Rate | Total |
|---|---|---|---:|---:|---:|
| `Stage1A_Drainage`!A64:G64 (**Q4**) | Concrete surround, GT1–GT4 + GT7–GT9 | `=ROUND(C54*0.1226+C55*0.1255,1)` | **68.9 m3** | `=Materials_Master!$H$75` $400/m3 | **$27,560.00** |
| `Stage1A_Drainage`!A65:G65 (**Q5**) | Crushed rock base, GT1–GT4 + GT7–GT9 | `=ROUND((C54*0.08+C55*0.075)*2.1,0)` | **94 T** | `=Materials_Master!$H$77` $48/T | **$4,512.00** |
| `Stage1B_Drainage`!A12:G12 (**Q2**) | Concrete surround, GT5 + GT6 | `=ROUND(C8*0.1226+C7*0.1255,1)` | **5.8 m3** | `=Materials_Master!$H$75` $400/m3 | **$2,320.00** |
| `Stage1B_Drainage`!A13:G13 (**Q3**) | Crushed rock base, GT5 + GT6 | `=ROUND((C8*0.08+C7*0.075)*2.1,0)` | **8 T** | `=Materials_Master!$H$77` $48/T | **$384.00** |

Quantities are **live formulas driven off the GT length cells themselves** — `Stage1A_Drainage`!C54 (GT1–GT4, 548.8 m) and C55 (GT7–GT9, 13.1 m) = 561.9 m, matching the C-06 labour note; `Stage1B_Drainage`!C8 (GT6, 31.4 m) and C7 (GT5, 15.2 m) = 46.6 m. Total 608.5 m = the F1320 schedule sum.

**Rate selection.** Concrete = `Materials_Master` **M65** (`H75`, $400/m3) — the model's own concrete rate, whose description already reads *"Concrete 32 MPa (spillway/**surrounds**)"* (source: old Civ rate table `SW_Mataterial`!E362). Crushed rock base = `Materials_Master` **M67** (`H77`, $48/T, Type 2.3 sub-base, ex old Civ CBR15 rate `SW_Mataterial`!E359) — a compacted crushed-rock base course, which is what the drawing calls up, **not** the 5–7 mm single-sized drainage bedding stone of M62. Both carry factor 1 (no directed category escalation; 2027 risk sits inside the x1.18 contingency), consistent with every other concrete/quarry rate in the model.

**m3 to tonne conversion 2.10 T/m3** is the model's own implied Type 2.3 density, not an imported assumption: `EBC`!C20 carries 13 T of Type 2.3 sub-base against the `EBC`!C18 spillway geometry of 50 x 1.65 = 82.5 m2 x 0.075 m = 6.19 m3, giving 13 / 6.19 = 2.10.

**Contingency and markup follow the destination sheets exactly** — the new rows sit inside `Stage1A_Drainage`!F74 (`=SUM(F6:F73)`, materials subtotal) which carries x1.18 at F75/F76, and inside `Stage1B_Drainage`!F16 with x1.18 at F17/F18; both then flow to the 41.5% chain unchanged.

**Effect:** materials +$32,072.00 pre-contingency in 1A and +$2,704.00 in 1B (**+$34,776.00 total**) → +$41,035.68 after x1.18 → **+$58,065.49 of sell**.

> **Recorded against the prior estimate.** The indicative figure carried in `EQUIPMENT_TEST_TCS.md` and `UNBACKED_CLAIMS_AUDIT.md` was about $7,626 pre-contingency, computed by applying the pipe-trench factor 0.203 T/m x $62/T to the 608.5 m run. That proxy is **4.6x too low** because it priced loose bedding stone only and no concrete. The audit itself flagged the proxy as unvalidated and warned that *"concrete haunching is at least as plausible a requirement and would carry a different, likely higher, cost"* — the drawing confirms it, and it does. The $7,626 sanity check is therefore **not met, correctly**: the measured detail governs (Rule 2).

**Labour not adjusted.** `Stage1A_Drainage` C-06 (23 crew-days, 561.9 m) and `Stage1B_Drainage` C-08 (3 crew-days, 46.6 m) already state *"REINSTATED incl excavation & quarry"*. **FLAG:** those crew-day rates were built at 25 m/day with no benchmark and with the concrete-surround detail expressly *"not re-verified"* (`LABOUR_REVIEW_PACK.md` line 85). Placing, screeding and curing 74.7 m3 of surround concrete to a channel line may not sit inside 26 crew-days. **Not adjusted here — outside the authorised scope of this edit, and any addition would breach the 2% band.** Raised for Phase B.

Cross-checked against the old workbook: `MasterCostSheet_Civ.V1.xlsx`!`SW_Mataterial` B243:I257 (the $164,860.30 set-aside at K258) contains **channel, end caps, trash boxes and transport only** — no quarry, no concrete. Its quarry table at B340:N351 is driven off `C310`/`C314` = **1,883 m of pipe trench only**. **GT bedding/surround was never priced in the old model either**, so no corroborating quantity existed and none was assumed.

### 10.4 Edit 3 — E2 detention basin / concrete spillway: EXCLUDED, add-price retained

**Decision recorded: EXCLUDE. Base stays $0. NOT converted to a Provisional Sum. NOT added to any total.**

| Cell | Before | After |
|---|---|---|
| `EBC`!G24 | "Reinstatement: set Stage1A_Drainage labour B-07 = 10 cd; enter spillway material rows at X1; add 5 plant-days 3-5T." | Rewritten — records the Director disposition, the sub-component verification and the no-double-count confirmation |

The `EBC` E2 add-price **$52,523.57** (`EBC`!F24) is **unchanged and intact** as a Rule 5 internal reinstatement price. `EBC`!B18:F23 untouched.

**Sub-component verification (required before accepting the exclusion) — RESULT: NO pipe, pit or scour-pad element is bundled into E2.** Every component opened and tested against the Director's three limbs, against `SE_12306_F1323-T1` (spillway sections) and `SE_12306_F1305-T1` (basin layout):

| `EBC` cell | Component | Pipe? | Pit? | Scour pad off a headwall? | Verdict |
|---|---|---|---|---|---|
| B18 | Spillway concrete 25 MPa, 125 thk x 50 m weir + 1.5 m aprons, 10.3 m3 | No | No | No — an overflow weir slab on the embankment crest at RL 29.700, not energy dissipation at a structure outlet | Excluded |
| B19 | SL72 mesh central, 12 sheets | No | No | No | Excluded |
| B20 | Type 2.3 sub-base 75 mm, 13 T | No | No | No | Excluded |
| B22 | Labour B-07, 10 crew-days | — | — | — | Excluded |
| B23 | Plant, 5 days 3–5 T + concrete gear | — | — | — | Excluded |

**The basin's genuine pipe / pit / scour-pad elements are separate line items and are ALREADY IN BASE** — they were never part of E2 and are not affected by this exclusion:

- `Stage1A_Drainage`!A61 **R3** — Basin rock D50 = 500 x 900 deep, C10 inlet/outlet, 236.997 m3 @ $110 = **$26,069.67** (this *is* the scour protection off the basin headwalls, per F1305/F1321)
- `Stage1A_Drainage`!A32 **C6** — LBC 2700x1200 crowns, C10 basin outlet, 8 ea = **$47,135.60**
- `Stage1A_Drainage`!A43 **H11** — BCC headwalls 2700x1200 (C10A/B), 2 ea = **$10,482.90**
- `Stage1A_Drainage`!C96 **C-01** labour — C10 RCBC basin outlet, 6 crew-days

**No sub-component requires promotion into base.**

**No-double-count confirmed by direct cell read after recalculation:** `Stage1A_Drainage`!C67 (row X1, *"DETENTION BASIN EARTHWORKS / CONCRETE SPILLWAY — NOT PRICED"*) = **0**, F67 = **$0.00**; `Stage1A_Drainage`!C96 (labour **B-07**, *"Concrete spillway weir 50 m — HELD AT 0"*) = **0** crew-days, F96 = **$0.00**. (Both rows moved down two by the Edit 2 insertion — previously rows 65 and 94.)

Basin **bulk earthworks** remain unpriceable in any form: never quantified in any drawing (F1305 annotation only), per `EBC`!B17 — unchanged.

**Phase B action carried:** client-facing exclusion sentence still required in the submission. Its sibling exclusion (kerb chutes, `EBC` E1) is disclosed; this one is not. That is the whole of UC-07 and it is **not closed by this edit** — only the model side is.

### 10.5 Cells changed — complete list

`Prelim_OH`!C26 · `Prelim_OH`!G26 · `Stage1A_Drainage`!A64:G64 (inserted) · `Stage1A_Drainage`!A65:G65 (inserted) · `Stage1B_Drainage`!A12:G12 (inserted) · `Stage1B_Drainage`!A13:G13 (inserted) · `EBC`!G24. Nothing else was edited. Row insertions were performed natively in Excel so all downstream references re-pointed automatically — verified: `TCS $ Sched`!D15 now `=Stage1A_Drainage!$F$76`, D35 now `=Stage1B_Drainage!$F$18`, `Prelim_OH`!F31 now `=0.055*(Stage1A_Drainage!$F$138+Stage1B_Drainage!$F$44)`.

**Authority:** Director decisions of 27 July 2026 — RPEQ excluded (both entities); GT quarry/bedding priced into base per locked §5.3; E2 detention basin / spillway excluded on the pipe-pit-scour-pad test with the add-price retained internally.
