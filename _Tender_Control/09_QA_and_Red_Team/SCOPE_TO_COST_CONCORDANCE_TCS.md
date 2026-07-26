# SCOPE_TO_COST_CONCORDANCE_TCS — Rule 4 Scope-to-Cost Concordance Pass

**Tender:** TEN16699 Rockhampton Sports Precinct Stage 1A & 1B — **TCS (civil stormwater) submission only.** TPS is out of scope for this pass and was not opened, analysed or written to; its own pass is complete and committed separately.

**Submission tested:** `Working_Proposals\TCS\TCS_ROK_Tender_Submission.docx` (a `.pdf` of the same timestamp sits beside it — **not analysed**; it will be stale the moment the draft changes, and this must be regenerated before issue).
**Cost model tested:** `Working_Cost_Models\TCS\ROK_TCS_CostModel_V2.xlsx` — 11 sheets, loaded both `data_only=True` (cached, Excel-COM-recalculated per `TCS_CHANGE_LOG.md`) and `data_only=False` (formulas).
**Rebuild history:** `Working_Cost_Models\TCS\TCS_CHANGE_LOG.md` and `MIGRATION_RECONCILIATION.xlsx` (Summary/Bridge/Register/CellIndex, 432 rows) — TCS was a full REBUILD (TPS was a repair), so migration evidence was read in full as the reverse-test instrument.
**Companion deliverable:** `SCOPE_TO_COST_CONCORDANCE_TCS.xlsx` (4 sheets: `Forward_Test` 46 rows, `Reverse_Test` 15 rows, `Equipment_Test` 4 rows, `Findings_Summary` 12 ranked findings).
**Method:** every sentence in the submission asserting, implying or capable of being read as asserting inclusion of scope was enumerated (not sampled) across §2 Tender Value, §3 Basis of this Tender, §4 Description of Proposed Services, §7 Civil Basis, §8 Noted Inclusions (8.1–8.4), §9 Provisional/Prime Cost Sums, §10 Schedule of Rates, §11 Access and Attendance, and §12 Exclusions/Qualifications/Departures. Each was traced against the workbook (row/cell level), `01_SCOPE_MATRIX.md`, `CONFLICT_LOG.md`, `QUANTITY_RECONCILIATION.xlsx`, `MATERIAL_QUOTE_REGISTER.xlsx` + `QUOTE_REGISTER_NOTES.md`, `RFI_SCHEDULE.md`, `06_ASSUMPTION_GAP_RISK_REGISTER.md` and `SUBMISSION_TEMPLATE_ANALYSIS.md`. **Read-only** — nothing in the submission, cost model or any register was edited.

**Note on the equipment-test exemplar.** The task instructed reading `EQUIPMENT_TEST_TPS.md` as the worked methodology exemplar before running TCS's own test. That file **does not exist anywhere in the repository** — `_Tender_Control\09_QA_and_Red_Team\` holds only `SCOPE_TO_COST_CONCORDANCE_TPS.md`/`.xlsx`, `SUBMISSION_TEMPLATE_ANALYSIS.md` and `ENTITY_IDENTIFIER_VERIFICATION.md`. The TPS concordance's own `Equipment_Test_Reconciliation` sheet was used as the closest available methodology reference instead (it is referenced *inside* that file as the source of TPS's equipment determinations), and the TCS equipment test below was built from scratch against the nine determinations the task specifies, applied to TCS's own drainage-product population (StormFilter manhole, precast pits/RCP/RCBC/headwalls, Hauraton GT channel system) rather than TPS's tapware/fixtures.

---

## 1. Headline: is the draft fit to proceed to red-team?

**Not yet — proceed only after two fixes, both directly traceable and both real.** The submission is, on the whole, a well-disciplined piece of Rule 4 drafting: headline figures tie to the cent against both the docx tables and the workbook's cached values ($2,761,814.98 + $111,787.74 = $2,873,602.72 for Stage 1A; $113,131.26 for Stage 1B; $2,986,733.98 total ex GST), the ABN is correct (89 195 291 365, confirmed against the Australian Business Register in `ENTITY_IDENTIFIER_VERIFICATION.md`), no prohibited blanket wording was found anywhere in the document, the WSUD PC-Sum/base-lump-sum boundary is drawn exactly where Rule 4's fixture/equipment test demands, the kerb-chute and basin/spillway exclusions both carry genuine, quantified add-prices on the EBC sheet (a model example of Rule 5 "no silent zero"), and RPEQ certification — which failed on the TPS side of this same tender — **does** have a real cost line here. But two defects would fail a red-team pass, and one of them is the exact same failure mode already found in the TPS submission, which raises it from an isolated slip to a systemic drafting habit:

1. **Shop drawings "add-price held" is unbacked** (§12.3) — no cost line exists anywhere in the model for shop-drawing production, despite the submission stating one is held and available on request. This is the identical defect independently found at TPS FT-39.
2. **"Excavation and quarry material" for the grated trench drains (§8.3/§8.4) is claimed but only the excavation half is costed.** This is not a minor drafting slip — it is a direct, named locked-decision reinstatement instruction at TENDER_PROMPT §5.3 ("Note Denis also set aside the excavation and quarry for these — reinstate that too"), and the quarry/bedding-material half of that instruction is not demonstrably implemented anywhere in the rebuilt model.

Three further HIGH-severity items (the WSUD PC-sum base-rate benchmark gap, the road-gully-inlet sourcing gap, and the Stage 1B standalone-viability structural risk) do not block red-team on their own but should be on the Director's list before award. See §4–§5 below for full detail and §7 for the ranked action list.

---

## 2. Verdict counts

**Forward test (46 rows — one row per inclusion assertion or closely related group of assertions):**

| Verdict | Count |
|---|---|
| PASS | 37 |
| PASS (rate flag — cost exists, underlying rate/allowance unconfirmed) | 3 |
| PARTIAL | 4 |
| FAIL | 2 |
| UNTRACEABLE | 0 (folded into the two FAIL rows, FT-37/FT-44, where the defect is a total absence of cost — flagged per Rule 2, not invented) |

**Reverse test (15 rows — one row per major cost-model cluster, hunting for cost with no external home):**

| Verdict | Count |
|---|---|
| PASS (clean) | 13 |
| PASS with a caveat (rate/allowance flag, not a homing gap) | 2 |

**No orphaned or unhomed cost was found anywhere in the rebuilt model** — a clean result on the specific question the reverse test exists to answer, and a genuine improvement over the superseded V1 model, which had two orphaned formula blocks feeding no roll-up at all (the $164,860.30 grated-trench package and the $10,865 subsoil-pipe package — `TCS_CHANGE_LOG.md` D3/D4). See RT-12.

**Equipment test (4 product groups — StormFilter manhole, RCP/RCBC/headwalls, precast pits/RGU inlets, Hauraton GT system), run from scratch per the task instruction since no TCS-specific equipment test pre-existed:**

| Item | Verdict | Confidence |
|---|---|---|
| WSUD StormFilter 22-cartridge DN3300 manhole | PASS | Medium |
| RCP/RCBC pipes, box culverts, headwalls | PASS | Medium |
| Precast pits, chambers, road gully inlets | PASS | Low-Medium |
| Hauraton Recyfix GT trench drain system + trash boxes | **FAIL (quarry material)** | Medium |

**Prohibited wording (§2 Rule 4) — zero hits.** The full document text (215 paragraphs, 9 tables) was searched for "all civil services", "complete system", "comprehensive", "fully compliant", "entire scope", "guarantee/warrant" and self-referential "in full"/"priced in full" claims. The only "in full" occurrence ("every structure scheduled on F1310 and every line drawn on the civil sheets — including lines 81, 83 and 87 **in full** — is priced in this submission") is a correctly bounded statement: it names the exact three lines and the exact boundary artefact (the F1303 point-of-discharge pit note), which is precisely the drafting discipline Rule 4 wants, not a blanket overclaim. No broad introductory language was found that could override the detailed exclusions.

---

## 3. Figures — tie-out against the locked numbers

| Figure | Locked | Draft / model | Status |
|---|---|---|---|
| Stage 1A lump sum (excl PC) | $2,761,814.98 | `TCS $ Sched` D24 → 2761814.975660199 → Table 2/3 $2,761,814.98 | **Ties exactly** |
| Stage 1A WSUD PC sum | $111,787.74 | `TCS $ Sched` D31 → 111787.7395 → Table 2/3/4/9 $111,787.74 | **Ties exactly** |
| Stage 1A total incl PC | $2,873,602.72 | `TCS $ Sched` D32 → 2873602.71516 → Table 2/3 $2,873,602.72 | **Ties exactly** |
| Stage 1B lump sum | $113,131.26 | `TCS $ Sched` D44 → 113131.262566 → Table 2/3 $113,131.26 | **Ties exactly** |
| Grand total ex GST | $2,986,733.98 | `TCS $ Sched` D46 → 2986733.977726 → Table 2/3 $2,986,733.98 | **Ties exactly** |
| TCS ABN | 89 195 291 365 | Cover table, entity table, signature block, `Cover_Control` C5 — all identical | **Correct** — independently ABR-verified in `ENTITY_IDENTIFIER_VERIFICATION.md` (Finding 2: "checksum valid; matches the master prompt exactly") |
| LH supervision treatment | Direct labour, not a preliminary (SW Zone Sumry B13 evidence) | `Stage1A_Drainage` A-14 / `Stage1B_Drainage` A-14 — priced as direct labour; `Prelim_OH` row 6 retained at $0 for traceability with the correction narrative | **Correct**, and unusually well-evidenced — `TCS_CHANGE_LOG.md` §9 documents the departure that was found, the primary evidence cited, and the $225,771.90 net commercial effect of the correction |
| Prelims cross-check | Bottom-up vs 5.5% allowance | $62,561.25 bottom-up vs $111,747.03 allowance → **+$49,185.78 SURPLUS** (44.0% below the allowance) | **Confirmed and tested** — see §5 RT-07; opposite direction to the TPS package's $19,628 shortfall, not comparable across entities |
| Markup sequence | Contingency → Prelims 5.5% → OH 18% → Profit 18%, each on cost, no compounding | `TCS $ Sched` C11 = 0.415 exactly; `TCS_CHANGE_LOG.md` §3 documents the correction from the old model's compounded 45.73% effective rate | **Correct** — resolves the Phase 3 audit finding exactly as directed |
| Margin structure disclosure | Never externally disclosed | No percentage, rate, or dollar overhead/profit/contingency/accommodation figure appears anywhere in the docx text or tables | **Correct** |
| Formula audit | Clean, no external links, no errors | `TCS_CHANGE_LOG.md` §4: 0 external references, 0 error values, 0 unresolved formulas after native Excel recalculation | **Confirmed** |

**No figure in the submission fails to tie to the locked set.**

---

## 4. The two FAIL findings, in full, with dollar exposure

### FAIL 1 — Shop drawings "add-price held" is unbacked (FT-44)
> §12.3 Departures from the tender documents: *"Shop drawings. Drawing H002 note 2 requires shop drawings. Shop drawings are excluded from this submission. This is a declared departure from the tender documents; an add-price is held and can be provided on request."*

Searched all 11 workbook sheets (`Cover_Control`, `TCS $ Sched`, `Stage1A_Drainage`, `Stage1B_Drainage`, `LabourRates_Master`, `Materials_Master`, `Equip_Master`, `Accommodation`, `Prelim_OH`, `EBC`, `Sched3_Extract`) for "shop drawing" — **no cost line exists.** The `EBC` sheet contains exactly three sections (E1 kerb chutes, E2 detention basin/spillway, E3 records of superseded/excluded items) and none of them is a shop-drawing line. This is the identical failure mode independently found on the TPS side of this same tender (TPS FT-39, same wording pattern: "an add-price is held and can be provided on request").
**Dollar exposure:** unquantified — not to be assumed equal to either kerb-chute EBC figure, which cover a completely different, unrelated scope. Director must build a fresh cost estimate for shop-drawing production, or the wording must be softened until one exists.

### FAIL 2 — GT trench "quarry material" is claimed but not costed (FT-03 / FT-37 / FT-38 / Equipment_Test row 4)
> §4 (Description): *"Runs GT1 to GT4 and GT7 to GT9 with their trash boxes, end caps and connection pits, including their excavation and quarry material (Schedule 3 item 3.5)"* — repeated at §8.3 (*"Excavation, bedding, quarry material and backfill and compaction for the grated trench runs and their pits"*) and §8.4 (Stage 1B, same wording for GT5/GT6).

This claim traces directly to a locked Director instruction at TENDER_PROMPT §5.3: *"Grated trench drains + trash boxes (Denis excluded these — reinstate and price…). Note Denis also set aside the excavation and quarry for these — reinstate that too."* The reinstatement of channel supply, trash boxes, end caps and installation labour is complete and correctly evidenced (`TCS_CHANGE_LOG.md` D3: the old model's orphaned $164,860.30 formula is now fully reinstated). But the **quarry/bedding-material** half of the same instruction has no traceable cost: `Stage1A_Drainage`'s only bedding-stone formula (Q1, row 62: `=ROUND(0.203*(C6+C8+C10+C11+C12+C13+C14+C16+C17+C18),0)`) sums only the mainline/collector/DWV pipe rows (P1, P3, P5–P9, P11–P13) — it deliberately excludes the GT channel rows (G1/G2, rows 54–55). No other material row anywhere in `Stage1A_Drainage`, `Stage1B_Drainage` or `Materials_Master` represents bedding or quarry stone for the 608.5 m of grated trench drain across both stages.
**Dollar exposure:** unquantified — no cost line exists to measure a variance against. Per Rule 2, this is flagged rather than estimated by inference from the (structurally different) pipe-trench bedding rate; a purpose-built estimate for the GT trench profile is required.

---

## 5. PARTIAL and rate-flag findings (not FAIL, but material enough to name)

- **FT-40 — Stage 1B standalone-viability structural risk.** Stage 1B carries dedicated, separately-quantified establishment/testing/CCTV crew-day activities (a genuinely stronger position than a bare percentage split), but its Leading Hand supervision (5.9 days) and its accommodation/FIFO travel share ($5,493.38) are both derived by a pro-rata crew-day ratio against the COMBINED 1A+1B base rather than independently costed for a stand-alone 1B mobilisation. Independently derived from TCS's own model — the same structural pattern as the TPS package's FT-01 finding, but arrived at separately by checking TCS's actual formulas. **HIGH severity**, no dollar figure assigned (no independent stand-alone-1B scenario exists in the model to compare against).
- **FT-04 / FT-41 — WSUD PC-sum base rate not reconciled to a like-for-like benchmark.** The only project-specific price ($90,064.63, Reece Q-459014431) sits roughly 16% above an Ocean-Protect-derived internal benchmark (≈$77.7k pre-freight, derived from the 18-cart/13-cart comparable-project pricing at Ocean Protect 19901). **HIGH severity**, ≈$12k rate-verification gap, not yet a confirmed number.
- **FT-26 — Road gully inlet (RGU) supply rate is a sourcing gap.** $1,350/ea × 33 = $44,550 materials value resting on an old-Civ-workbook benchmark with an explicit internal note that no current RGU/lintel package quote exists. **HIGH severity** given the dollar value of a single unquoted line.
- **FT-29 / FT-30 — Heavy plant (crane/franna/trench shields) is an unconfirmed hire-register allowance.** $69,480 combined pre-markup, all three lines explicitly flagged "not in hire registers" on `Equip_Master`. **MEDIUM severity.**
- **FT-07 / FT-17 — Compaction standard borrows a hydraulic-spec table because the governing civil spec is missing.** §7.3 prices to "the specification tables" without naming one; the only compaction table on file is VOL 38 §3.62 (the hydraulic spec, present), while VOL 35 (the governing civil spec) is absent. Per the document-wide confidence ceiling this cannot be rated High. **MEDIUM severity**, compliance-basis risk not a missing cost.
- **RT-07 — Prelims cross-check surplus, tested per instruction.** The $49,185.78 surplus (44.0% headroom against the 5.5% allowance) was specifically tested for whether it conceals a cost with no external home. It does not: every one of the 17 bottom-up `Prelim_OH` line items traces individually to a Noted-Inclusions §8.1 sentence (checked line-by-line — see FT-12/FT-13/FT-15/FT-17/FT-18/FT-19). The surplus is unconsumed headroom functioning as additional undisclosed margin under the "prelims" label rather than a masked cost — the opposite finding to TPS's genuine $19,628 shortfall, and not directly comparable across entities. **MEDIUM severity**, governance/labelling observation only, no external wording change required.
- **FT-38 — GT6 grate substitution unconfirmed.** Reece offered PRO200 G-tec against the F1320-scheduled PRO100 D400 code 47245 (Register Gap #7). **MEDIUM severity**, $12,171.53 line value at risk if rejected.

---

## 6. Prohibited-wording scan — result and why nothing needed replacing

Every phrase in §2 Rule 4's prohibited list, plus close paraphrases, was searched for verbatim across the full document text: "all civil services," "complete system," "comprehensive," "fully compliant," "entire scope," "guarantee/warrant," and any unqualified claim of "supplied and installed." **None were found in a form that oversells the priced scope.** The nearest candidates and why each is compliant:

- §37 closing scope statement — *"…necessary to deliver the included civil stormwater scope **only**"* — correctly self-limiting, mirrors the CQU master's own compliant formula.
- §61 (§7.5) — *"including lines 81, 83 and 87 **in full**"* — bounded to three named lines and one named boundary artefact (the F1303 POD pit note), not a blanket claim.
- §100 (§8.2 bullet 18) and §111 (§9) — the WSUD supply-vs-install split is stated twice, in both directions, with neither sentence claiming more than its own half. This is the correct pattern the fixture/equipment test requires, and it is the strongest positive example in the document.
- §69 (§8, opening line) — *"Each item below is a priced item. Nothing outside this list and the pricing summary at Section 6 is included"* — an explicit narrowing clause, the same drafting device Rule 4 wants everywhere.

No suggested replacement wording is required for any prohibited-wording hit, because none was found. The wording work required by this pass is confined to the two FAIL items in §4 (either cost the claim or soften the wording to match what is actually costed) and the five items in §5.

---

## 7. What must change before the draft goes to red-team (ranked)

1. **Cost or remove the shop-drawing "add-price held" claim** (§12.3) — build a real EBC line, or soften the wording until one exists.
2. **Close the GT trench quarry/bedding-material gap** (§8.3/§8.4) — add a GT-specific bedding/quarry material line to `Stage1A_Drainage` and `Stage1B_Drainage`, consistent with the explicit TENDER_PROMPT §5.3 reinstatement instruction, before treating that instruction as fully implemented.
3. **Obtain the direct Ocean Protect re-quote** for the 22-cartridge StormFilter manhole on the actual MUSIC model (Gap #1/Opens #10) before the $111,787.74 PC sum is locked for issue — it is a material, externally-visible figure resting on an unreconciled ≈16% rate gap.
4. **Obtain a current RGU/lintel package quote** — $44,550 of materials value has no live 2026 pricing.
5. **Test the Stage 1B standalone-viability claim against an independent stand-alone cost scenario**, or soften §2/§4/Table 2's "viable if awarded alone" wording to acknowledge the pro-rata apportionment method used for LH supervision and accommodation until that scenario exists.
6. **Firm up the 50t crane, franna and trench-shield hire rates** ($69,480 combined) against an actual hire-house quote before award.
7. **Name the compaction-standard basis explicitly** in §7.3 (VOL 38 §3.62 borrowed by analogy, pending VOL 35) rather than the unattributed "specification tables."
8. **Confirm the GT6 grate substitution** (PRO200 G-tec vs the scheduled PRO100 D400) with Reece before order.
9. **Confirm the Hauraton Fibretec $198/m vs $232.94/m rate** with Reece — favourable direction only, not a submission blocker.
10. **Director governance note (not a wording change):** the $49,185.78 prelims surplus is confirmed clean of any hidden unpriced obligation; decide whether to retain it as a VOL-35 risk buffer or address the labelling internally.
11. Carry forward (already logged, not new): the C09A/B non-standard-structure risk (Query B1, $1,177.60 low materiality) and the WSUD unit-specific testing/commissioning granularity (low priority) remain open for the Director's awareness.

---

## 8. What did NOT need fixing — confirming the draft's strengths

- Every headline dollar figure ties exactly across the docx tables, the cached workbook values and the `Sched3_Extract` Paynters-format transfer sheet — no arithmetic drift anywhere.
- The TCS ABN (89 195 291 365) is independently ABR-verified as correct — unlike TPS's template ABN, which failed the ABN check-digit algorithm in every prior source held.
- The WSUD supply-vs-installation boundary (§9, §8.2 bullet 18) is the cleanest example in the whole document of the exact discipline Rule 4's fixture/equipment test demands — supply/delivery (PC Sum +15%) and installation (base lump sum, 41.5% chain) are never conflated, in either direction, anywhere in the wording or the model.
- Both declared "excluded but add-price held" items that DO have real cost backing — the kerb chutes ($55,429.90, EBC E1) and the detention basin/spillway ($52,523.57, EBC E2) — are correctly built up from materials, labour and plant and marked for Director decision, which sharpens rather than excuses the shop-drawings gap (Finding 1): the model shows the discipline can be done correctly, and was, twice.
- RPEQ certification, as-constructed drafting and ADAC XML preparation all carry real, named costs (`Prelim_OH` rows 24–26) — the same class of claim that failed on the TPS side of this tender (zero RPEQ cost found anywhere in that model) is correctly backed here.
- Compaction testing is quantified on BOTH stage sheets (40 tests 1A, 4 tests 1B) — again the same claim type that failed on the TPS side (package-wide wording, single-work-area cost) is handled correctly here.
- No orphaned or unhomed cost was found anywhere in the rebuilt model (Reverse Test, §2) — a material improvement over the superseded V1 model's two orphaned formula blocks.
- The markup sequence (contingency → 5.5% prelims → 18% OH → 18% profit, each on cost) is exactly as directed, with the old model's compounding defect (45.73% effective vs 41.5% labelled) corrected and disclosed in the change log, not silently fixed.
- No prohibited blanket wording exists anywhere in the document.
- The LH-supervision-as-direct-labour correction is exceptionally well evidenced end to end (primary-source cell reference, the departure that was found, and the exact dollar effect of the fix).

---

## 9. Files produced

- `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TCS.xlsx` — 4 sheets: `Forward_Test` (46 rows), `Reverse_Test` (15 rows), `Equipment_Test` (4 rows, run from scratch per the task instruction — no pre-existing TCS equipment test was found), `Findings_Summary` (12 ranked findings, most severe first).
- `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TCS.md` — this file.

Nothing else was created, edited or touched. The TPS submission, cost model and registers were not opened. The `.pdf` sibling of the TCS submission was not analysed and will be stale relative to this pass's findings until the draft is corrected and reissued.
