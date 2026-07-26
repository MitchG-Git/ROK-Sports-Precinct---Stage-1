# COST_MODEL_REBUILD_DECISION — tender-run-01, 26 Jul 2026
Basis: full openpyxl audit of all 4 workbooks (every sheet incl. hidden; formulas vs cached values; external links; named ranges). Raw audit: `workbook_audit_raw.json`; full cell dumps (formula + cached value): `dumps/*.csv` (30 sheets).

## Decision

| Workbook | Decision | Why |
|---|---|---|
| `MasterCostSheet_Hyd.V1.xlsx` | **REPAIR IN PLACE** (architecture preserved per §5.4/§8-P3) | Correct CQU architecture; correct FIFO roster basis; defects are enumerable and local (below) |
| `MasterCostSheet_Civ.V1.xlsx` | **REBUILD on the CQU/Hyd architecture** (per Phase 6 instruction) with line-by-line migration reconciliation | Different structure, local (non-FIFO) rates, no accommodation logic, zero labour/plant, inherited external link to an unrelated 2018-era project file |
| `CQU_TAFE- HYD Example.xlsx` | Reference only — the structural template (work-area tabs + 5 master rate tabs + TCS $ Sched + Prelim & OH) | 7 work-area tabs prove the architecture scales; carries same external-link disease (don't copy links) |
| `CQU_TAFE- Civil Example.xlsx` | NOT a structural reference | 2 tabs only, no labour template — confirmed |

## Verified current state — MasterCostSheet_Hyd.V1 (TPS)

**Architecture (10 sheets, matches prompt):** `TCS $ Sched`, `00_ TCS Prelim & OH`, `ClubHouse (NBC )`, `Public Amenities (PAM)`, `Siteworks `, `LabourProject Rates_Master`, `Material Rates_Master`, `Equip&HIRE_Master`, `Misc Subbie Rates_Master`, `Accomodation_Master` (223 hidden rows).

**Labour rates verified to the cent (LabourProject Rates_Master):** roster text "Work ROSTER Example #3 – 6-Day Week, 10Hr Days, Stay @ Rocky for W/E, Return Every 2nd W/E. (FLY)"; 21 work-days/210 hrs per month. Leading Hand $25,854/mo → **$123.1143/hr** (E14) ✓; Tradesman/Plumber/Operator **$94.1165/hr** (E21) ✓; T/A & Apprentice at E52-block (Civ cross-ref $76.8065 to be re-verified in rebuild). ×1.08 targets: **$132.9634 / $101.6458 / $82.9510** per §5.4.

**Escalation factors verified (all three work-area sheets, block J14:M19):** "april 2026 direct impact Increase % (not contigency)" — PE Pipe & Fitting **×1.38**, PVC Pipe & Fittings **×1.38**, Subby Rates **×1.15**, Delivey [sic] Rate **×1.20** ✓.

**Roll-up defects verified with formulas (TCS $ Sched):**
1. `N64 SUB-TOTAL = SUM(N16:N63) = $273,056.54` = CLUBHOUSE $81,329.70 + PUBLIC AMENITIES $17,272.79 + SITEWORKS $174,454.06 ✓ (prompt figure confirmed).
2. **Pump station orphaned:** big-ticket block W37=$468,000 → `W43 = 468,000×1.15 + 2,500 freight + 5,000 install = $545,700` — **W43 feeds NO roll-up cell**. The prompt says "carries this at $545,700 sell — remove it"; true state: computed but already outside the total. Removal per §5.3 = delete block + document; no headline movement from removal itself. **D6 flag: any prior quote circulated from N68 never included the pump station.**
3. **NEW DEFECT FOUND — NBC hot water units orphaned:** `AC17 = (3,438.29+52.80)×1.15×3 + 300 + 600 = $12,944.26` (3× Rheem HWU + safe trays, NBC block) — **not referenced by N16 or any total** (N16 = S16+W17+Z17 only picks up grease trap $10,301.77 + HW pump set $8,142.20). PAM's HWU (W31=$4,364.75) IS included in N23. → NBC HWUs are silently missing from the current sell.
4. **GST:** `N66 = N64×10%` → GRAND TOTAL N68 $300,362.20 incl GST. Remove; ex-GST throughout (§5.4).
5. **Markup compounding vs §5.4:** current chain R42=5.5%×cost, R43=18%×cost, R45=cost+P+OH, **R47 = 18%×R45** (profit on cost+prelim+OH) → effective markup R49/R39 = 45.73% while label Q51 shows 41.5%. §5.4 orders Prelims/OH/Profit each **on cost** → 41.5%. Rebuild applies §5.4; movement (~4.2% of cost) recorded in change log. **Director visibility flag in D6.**
6. `S39 = SUM(S13:S26)` mixed/mislabelled range (captures NBC+PAM, not Siteworks; unused by N-column) — dead formula, remove in repair.
7. Big-ticket items carry only 1.15 margin + freight + install — no prelims/OH/profit and no labour beyond "Installation_MH" token cells (250/200/600 etc. are *dollar* cells, not hours). Rebuild treats equipment properly (PC-sum lines where §5.4 nominates, else full-cost build-up).

**External links (must be severed in repair — values frozen then re-sourced):** [1] SharePoint `CQU ROK_PROGRAM - MASTER.V1.xlsx` (feeds `00_ TCS Prelim & OH` C9:C12, D45); [2] SharePoint `CQU ROK_Staff Costing.V1_Steph.xlsx` (feeds ALL labour rates); [3] `240614 - Pipe & Fittings - Price Comparison.xlsx` (feeds Material Rates_Master D-column); [4] `240614 - Suppliers Subbies - Price Comparison.xlsx` (feeds Equip&HIRE + Misc Subbie masters). Note refs [3]/[4] are **June 2024 (CQU Hydrant era) price comparisons** — cached rates are ≥2 years old at 2027 commencement; Phase 5 re-sources every adopted rate.

**Labour/plant population state:** work-area sheets carry the six-crew convention (Crew #1 InGround Drainage … Crew #6 DEMO) with day-quantity cells empty/zero — **no labour or plant priced anywhere in the sell**. `00_ TCS Prelim & OH` external-linked and effectively unpopulated.

## Verified current state — MasterCostSheet_Civ.V1 (TCS)

**Structure (8 sheets):** `V1` (summary), `Prelim_OH-Check`, `SW Zone Sumry`, `SW_Mataterial` [sic], `SW_Pit Takeoff`, `SW_insitu Takeoff`, `Staff Rates`, `Equip&HIRE`.

- Summary V1: TCS Quote **#2372**, dated 16-07-2026. Part A Stormwater cost R13 = `SW Zone Sumry'!F70` = **$535,364.20** → marked-up S13 $780,186.25 (same §5.4-inconsistent profit compounding) + WSUD block W12 = 88,838×1.15 + 6,000 install est + 2,500 fuel levy = **$110,663.70** → **K26 TOTAL ex GST $890,849.95**.
- **WSUD basis is superseded:** $88,838 is the Atlan estimate; Design Report RPT006_B §7.4 (Add 8) nominates 22× Ocean Protect Tall (690) PSorb in DN3300 manhole → reprice in Phase 5/6; §5.3 PC-sum treatment (supply+delivery PC +15%; install in lump sum, not exposed).
- **Labour = $0, Plant = $0:** zone labour blocks reference `Staff Rates` day rates (LOCAL: leading hand $822.50/day ≈ $82.25/hr — no FIFO, no accommodation logic) but ALL quantity cells are empty → `TOTAL Labour = 0`, `TOTAL Equip = 0`. **The $890,849.95 is materials/subbies-only marked up.** Biggest single commercial risk in the current models.
- `Prelim_OH-Check` cross-check cells F42/F47 = **0** (empty), referenced by V1 T29/T30 as "Manual Calc" — the check the prompt requires populated.
- External link: `\\SBSERVER\Users\tony.rieck\My Documents\60 Richards St Loganlea Costings V2.xls` — inherited from an unrelated Loganlea project via template lineage; sever.
- 15 named ranges (several likely orphaned — resolve at rebuild).
- **Migration inventory (nothing may be lost):** SW_Mataterial 370 rows (337 formulas) material take-off; SW_Pit Takeoff 120×54 grid (pit-by-pit); SW_insitu Takeoff 28 rows; SW Zone Sumry zone logic (7 zones, F70 roll-up); Staff Rates local rate build; Equip&HIRE 247 hard-coded rates. Each carried line-by-line into the rebuild with a reconciliation register.

## CQU_TAFE- HYD Example — the target architecture
`TCS $ Sched` + `00_ TCS Prelim & OH` + 8 work-area tabs (MISC & SITEWIDE, ROK092, ROK21A, ROK019, ROK033, ROK034, ROK036, ROK076) + the same 5 master rate tabs. Cached #DIV/0! errors in MISC & SITEWIDE (E936-938, O962, P966/Q966) and 749 hidden rows — copy the *structure*, not the content. Same external links — do not carry.

## Rebuild plan (Phase 6 execution order)
1. Freeze current cached values of every external-linked cell (done — dumps/*.csv are the frozen record); sever links.
2. New TCS workbook on CQU/Hyd architecture: work-area tabs = Stage 1A zones / Stage 1B zones mirroring Paynters Schedule 3 structure; masters = FIFO labour (ROK rates ×1.08), materials (Phase 5 sourced), equip, subbies, accommodation.
3. Migrate Civil content line-by-line → `MIGRATION_RECONCILIATION.xlsx` (old cell → new cell → value → variance → reason).
4. Repair TPS workbook: sever links, fix N16 (+AC17), remove pump-station block per §5.3 with interface ledger, remove GST, re-base profit per §5.4, apply ×1.08 cascade, populate crew-days from Phase 7 programme, populate Prelim & OH tab and reconcile vs 5.5%/18%.
5. Forced recalculation via LibreOffice headless before trusting any total; reconcile computed vs cached; report every divergent cell.
