
# UNBACKED CLAIMS AUDIT — TEN16699 Rockhampton Sports Precinct Stage 1A & 1B
TriCore Plumbing Services (TPS) · TriCore Civil Services (TCS) · tender-run-01 · full sweep, both entities, every register

**Scope of this pass:** every document listed in the task brief was opened and searched for the claim vocabulary (add-price held / price held / held not offered / reinstatable in minutes / reinstated / now in base / rolled up / wired into / cost carried / allowed / included / provision made / allowance exists / priced elsewhere / covered under / included in item / excluded but costed / verified / ties to / reconciles with), plus the converse direction (EBC/alternate entries with no external reference). Both cost models were loaded twice (`data_only=True` and `False`) with the venv Python 3.11.15 / openpyxl 3.1.5 interpreter at `C:\Users\Mitch-TPS\AppData\Local\hermes\hermes-agent\venv\Scripts\python.exe`, every populated cell and note/comment column read on `EBC_Alternates` (TPS) and `EBC` (TCS) in full, both `Stage1A_Drainage`/`Stage1B_Drainage` bedding-stone formulas resolved cell-by-cell, and `MIGRATION_RECONCILIATION.xlsx` (`Bridge` + `Register`, 436 rows) read for every "REINSTATED"/"STRUCTURE-MOVE" row touching drainage or quarry material. Both submission `.docx` files were extracted in full (paragraphs + every table cell) via python-docx. **Read-only** — nothing outside this one file was modified.

---

## 1. Summary

**Claims tested:** every claim-family hit returned by the vocabulary sweep was triaged — approximately 130 raw hits across all `.md` registers and both `.docx` submissions, collapsing (after merging repeated quotations of the same sentence across a submission/RFI/register/model chain) to **34 distinct claim-bearing assertions**, of which **11 were resolved as genuinely material** (i.e. a specific, checkable "a price/line/register-entry exists" statement) and individually traced to a model cell, formula, or EBC row.

**Verdict distribution (11 material assertions):**

| Verdict | Count | IDs |
|---|---|---|
| **UNBACKED** | 4 | UC-01, UC-02, UC-03, UC-04 |
| **PARTIAL** | 2 | UC-05, UC-06 |
| **ORPHANED** (converse — backed internally, silent externally) | 1 | UC-07 |
| **BACKED** (confirmed correct — logged as comparators, not defects) | 4 | UC-08, UC-09, UC-10, UC-11 |

**Distinct defects vs. total locations:** the sweep confirms **4 distinct defects** (not 4+more as separate items — the task's "four known instances" collapse to **three** distinct defects plus the GT quarry gap, because TPS §116 and TCS §12.3 are the *same* defect independently expressed in two entities from one shared drafting instruction) **plus 3 new defects not among the four originally known** (UC-04 RPEQ, UC-05 compaction testing, UC-07 the converse/spillway finding), for **6 distinct defects total**, propagated across **31 separate document/cell locations**. UC-06 is a seventh, minor/immaterial finding logged for completeness.

**New beyond the four known:** UC-04 (TPS RPEQ certification — zero cost, claimed 3× in the submission itself), UC-05 (TPS compaction testing — claimed package-wide, priced NBC-only, confirmed directly against the model), UC-07 (the converse case — TCS EBC E2 detention-basin/spillway add-price, $52,523.57, fully computed and internally documented but never disclosed to the client in the submission or the RFI schedule, unlike its sibling exclusion, kerb chutes, which is disclosed).

**Total quantified exposure:** **no net exposure sits inside either grand total** — every UNBACKED/PARTIAL claim by definition describes money that is *not* in the tendered sums (that is what "excluded" means), so there is no arithmetic error in the $2,009,794.18 (TPS) or $2,986,733.98 (TCS) headline figures. The exposure is asymmetric downside risk if the claims are ever tested: (a) **≈$7,626 pre-contingency / ≈$12,736 sell, indicative only** (UC-03, GT quarry/bedding — see §2 for the factor used and its limits); (b) **unquantifiable** for UC-01/UC-02/UC-04 — per Rule 2, no comparator exists in either model to anchor an estimate, so none is invented; (c) **$52,523.57 of already-computed reinstatement value that is currently invisible to the client** (UC-07) and at risk of being forfeited by omission if detention-basin/spillway scope is later assigned to TCS.

**Converse-check result:** one finding (UC-07). All other EBC/alternate entries in both models (TPS EBC-1/2/3/4, ALT-1, ALT-2; TCS EBC-1 kerb chutes) are correctly referenced externally with matching dollar figures — see §3.

---

## 2. The register

### UC-01 — Shop drawing production "add-price held" — cross-entity — **UNBACKED**
**Entity:** both (single shared defect, two independent implementations) · **Claim family:** "excluded but costed" / "add-price held"

> TPS §116: *"Shop drawing production is excluded — a stated departure from H002 note 2, with an add-price held and available on request."*
> TCS §12.3: *"Shop drawings. Drawing H002 note 2 requires shop drawings. Shop drawings are excluded from this submission. This is a declared departure from the tender documents; an add-price is held and can be provided on request."*

**Propagation chain (8 locations, both entities):**
1. `Working_Proposals\TPS\TPS_ROK_Tender_Submission.docx` paragraph 116
2. `Working_Proposals\TCS\TCS_ROK_Tender_Submission.docx` paragraph 171
3. `_Tender_Control\03_Scope_and_Interfaces\01_SCOPE_MATRIX.md` row X1 ("TPS/TCS (excl.) … add-price carried")
4. `_Tender_Control\09_QA_and_Red_Team\SUBMISSION_TEMPLATE_ANALYSIS.md` row N11 (the pre-drafting recommendation that generated the wording in the first place — "Shop drawings excluded — flagged departure … add-price carried")
5. `Working_Cost_Models\TPS\ROK_TPS_CostModel_V2.xlsx` sheet `Sched3_Extract` cell A51 — *inside the model itself*: *"shop drawings (X1 - EBC in the tender control register)"* — a citation to a register entry that does not exist anywhere in `_Tender_Control`
6. `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.md` FAIL 2 (FT-39) — prior audit finding
7. `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TCS.md` FAIL 1 (FT-44) — prior audit finding, explicitly cross-referencing FT-39 as "the identical defect"
8. TCS `EBC` sheet — searched in full; contains exactly E1 (kerb chutes), E2 (spillway), E3 (records) — no shop-drawing section. TPS `EBC_Alternates` — searched in full; contains exactly EBC-1 through EBC-4 plus ALT-1/ALT-2 — no shop-drawing line.

**Model line asserted:** none. Zero hits for "shop drawing" anywhere in either 12-sheet/11-sheet workbook outside the one self-referential citation at location 5.
**Dollar value:** no cost exists to measure (Rule 2 — not estimated).
**Severity:** HIGH — a stated contractual departure from a named spec clause (H002 n.2), in the client-facing submission of *both* entities, backed by nothing.
**Remedy:** Director call — either build a genuine EBC line in both `EBC_Alternates` and `EBC` for shop-drawing production (drafting labour, print/issue, coordination time), or soften both submissions' wording to "excluded; no add-price is held" until a real figure exists. Whichever is chosen, correct location 5 (the model's own internal citation to a non-existent register entry) as part of the same fix — it is not cosmetic, it is the one place the false claim lives *inside* the cost model rather than only in prose.

---

### UC-02 — TPS plumbing approval lodgement "add-price held" (§114 / Appendix B query C8) — **UNBACKED**
**Entity:** TPS only · **Claim family:** "add-price held" / "held internally"

> §114: *"Plumbing approval lodgement, application documentation and attendance at approval inspections are excluded — a stated departure from the Plumbing Subcontractor provisions of ITT Part 2 §16, with an add-price held (Appendix B query C8)."*

**Propagation chain (5 locations):**
1. `Working_Proposals\TPS\TPS_ROK_Tender_Submission.docx` paragraph 114
2. Same docx, Table 10 (Appendix B), row C8, column 4: *"If lodgement is required of us, an add-price applies (held)."*
3. `_Tender_Control\08_Risks_Assumptions_Qualifications\RFI_SCHEDULE.md` query C8: *"an add-price applies (held internally)"*
4. `_Tender_Control\08_Risks_Assumptions_Qualifications\06_ASSUMPTION_GAP_RISK_REGISTER.md` D6-F6: *"add-price held on EBC"*
5. `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.md` FAIL 1 (FT-38) — prior audit finding

**Model line asserted:** none. `EBC_Alternates` was searched in full for "lodge/lodgement/approval application" — no line exists. This is distinct from EBC-2 (Trade Waste application specifically, $4,147.67, correctly costed and confirmed live at `EBC_Alternates!F19`) — the broader ITT §16 lodgement obligation across *all* plumbing approvals has never had a line built, only the narrower trade-waste-specific one.
**Dollar value:** no cost exists to measure.
**Severity:** HIGH — a named departure from ITT Pt 2 §16 in the client-facing submission, repeated three times in TPS's own documents, with zero backing.
**Remedy:** Director call — build EBC-5 (plumbing approval lodgement) with a genuine estimate (admin time + RRC fees exposure), or remove "add-price held" from §114, the Appendix B table, the RFI Schedule and D6-F6 simultaneously — a partial fix (e.g. softening only the submission) would leave the internal registers asserting a backing that still doesn't exist.

---

### UC-03 — GT trench "quarry material" claimed "REINSTATED into base" — structurally excluded — **UNBACKED** (partial: excavation backed, material not)
**Entity:** TCS · **Claim family:** "reinstated into base" / "priced elsewhere"

> §4 (Description): *"Runs GT1 to GT4 and GT7 to GT9 with their trash boxes, end caps and connection pits, including their excavation and quarry material (Schedule 3 item 3.5)."*
> §8.3: *"Excavation, bedding, quarry material and backfill and compaction for the grated trench runs and their pits."*
> §8.4 (Stage 1B, GT5/GT6): same wording.

**Propagation chain (9 locations):**
1. `Working_Proposals\TCS\TCS_ROK_Tender_Submission.docx` paragraph 34 (§4)
2. Same docx, paragraph 104 (§8.3)
3. Same docx, paragraph 106 (§8.4)
4. Same docx, Table 3, row 5, column 3 (Tender Value table): *"…including excavation and quarry material."*
5. `Working_Cost_Models\TCS\ROK_TCS_CostModel_V2.xlsx` sheet `EBC`, cell B27: *"Grated trench drains (GT1-9, trash boxes, excavation & quarry) — REINSTATED into base"*
6. `_Tender_Control\03_Scope_and_Interfaces\01_SCOPE_MATRIX.md` row L1: *"TCS prices Sch 1A 3.5 in full (GT1–GT4, GT7–GT9, trash boxes, connection pits, excavation and quarry)"*
7. `Working_Cost_Models\TCS\TCS_CHANGE_LOG.md` §5 item 6 ("Trench drains REINSTATED") and D3 ("…including excavation and quarry per the reinstatement direction")
8. `Working_Cost_Models\TCS\MIGRATION_RECONCILIATION.xlsx`, `Bridge` sheet: *"ADD grated trench drain package — REINSTATED … Now priced in full (Reece/Hauraton basis $162,349) incl excavation & quarry."* and `Register` row for cell `K330`: the old workbook's single combined "excavation/quarry" block is mapped (`STRUCTURE-MOVE`) onto `Stage1A_Drainage!F62` — the ordinary pipe-bedding formula — with no corresponding GT-specific row created.
9. Traces to the locked Director instruction at `TENDER_PROMPT.md` §5.3: *"Note Denis also set aside the excavation and quarry for these — reinstate that too."* (the instruction itself is fine; execution is incomplete)

**Model line asserted and independently verified:** `Stage1A_Drainage!C62` formula = `=ROUND(0.203*(C6+C8+C10+C11+C12+C13+C14+C16+C17+C18),0)` — sums only the mainline/collector/DWV pipe-trench rows; `C54` (GT1–GT4) and `C55` (GT7–GT9) are not arguments to this formula. `Stage1B_Drainage!C11` formula = `=ROUND(0.203*C6,1)` — sums only the 150 PVC DWV row (`C6`); `C7`/`C8` (GT5/GT6) are not arguments. Both formulas confirmed by direct cell read (`data_only=False`) — not inferred from documentation. **Excavation is backed** (crew-day labour for GT installation is present and reaches the roll-up per `EQUIPMENT_TEST_TCS.md` §2.19/2.20 — installation/excavation confirmed live). **Quarry/bedding material is not** — no material row anywhere in `Stage1A_Drainage`, `Stage1B_Drainage` or `Materials_Master` represents bedding stone for the 608.5 m of GT trench across both stages.
**Dollar value: INDICATIVE ONLY, ≈$7,626 pre-contingency / ≈$12,736 sell** — computed by applying the *pipe-trench* bedding factor (0.203 t/m × $62/t) to the 608.5 m combined GT run (F1320 schedule total, GT1–GT9) purely as an order-of-magnitude proxy: 608.5 × 0.203 = 123.5 t × $62 = $7,658, ×1.18 material contingency = $9,036, ×1.415 markup ≈ $12,786 — consistent with the task brief's stated figures within rounding. **This factor is not validated for the GT channel-trench profile**, which is structurally different from a pipe trench (shallower, wider, different bedding depth) — a purpose-built rate is required before this number is relied on for anything beyond a rough sense of scale. Do not carry it into any register as a firm figure.
**Severity:** HIGH — this is not a drafting slip but a direct, named locked-decision instruction that has not been fully executed, and it is asserted as complete ("REINSTATED", "priced in full") in five separate places including inside the cost model's own migration audit trail.
**Remedy:** add a GT-specific bedding/quarry material line to both `Stage1A_Drainage` and `Stage1B_Drainage` (a purpose-built rate, not the pipe-trench factor), consistent with the TENDER_PROMPT §5.3 instruction, before the "reinstated in full" / "REINSTATED into base" language is retained anywhere.

---

### UC-04 — TPS RPEQ certification claimed "included" — zero cost anywhere in the model — **UNBACKED** *(not among the four known)*
**Entity:** TPS only · **Claim family:** "cost carried" / "included"

> §79 (Noted Inclusions): *"As-constructed documentation, RPEQ certification and ADAC-compliant XML deliverables for the hydraulic package's own water, sewer and fire assets…"*
> §116 (repeated): *"As-constructed documentation, RPEQ certification and ADAC drafting for our own assets remain included and are distinguished from shop-drawing production."*
> §145 (repeated again, Construct-Only Basis): *"…as-constructed documentation, RPEQ certification, ADAC XML and CCTV for our own assets, and Form 72 fire certification."*

**Propagation chain (5 locations):**
1. `Working_Proposals\TPS\TPS_ROK_Tender_Submission.docx` paragraph 79
2. Same docx, paragraph 116 (same sentence that also carries UC-01's shop-drawing defect — both faults sit in one paragraph)
3. Same docx, paragraph 145
4. Same docx, Table 9, row 6, column 2 (RFI Appendix, query A6, which quotes the ITT §19/VOL 38 §3.56 requirement)
5. `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.md` FAIL 4 (FT-32/RT-14) — prior audit finding

**Model line asserted:** none. Confirmed directly — every sheet of `ROK_TPS_CostModel_V2.xlsx` was searched for "RPEQ" (case-insensitive, all 12 sheets, `data_only=True`): **zero matches.** RPEQ sign-off is normally a discrete paid consultant engagement; unlike the seismic/articulation adders (which carry a stated round-number allowance even where a firm quote is pending), nothing represents RPEQ at all — not even a placeholder.
**Contrast (why this is not a template-wide problem):** the identical claim is made in the **TCS** submission (paragraphs 67, 76, 142, 174: *"RPEQ-certified as-constructed drawings … are included"*) and **is correctly backed** — `Prelim_OH!B26` = *"RPEQ certification + as-constructed drawing preparation"* with a live, non-zero cost that reaches the TCS total. This proves the claim type can be, and was, done correctly on the sibling entity — see §3/§4 comparators.
**Dollar value:** no cost exists to measure; no comparator anywhere in the TPS model to anchor an estimate (unlike UC-05 below, where a same-scope NBC figure exists as a floor).
**Severity:** HIGH — a real, external, professional-fee deliverable claimed as included three separate times in the client-facing submission text itself (not just in an internal register), with $0 anywhere behind it.
**Remedy:** Director call — obtain an RPEQ quote and add a line (mirroring TCS's `Prelim_OH!B26` treatment), or reword §79/§116/§145 to state RPEQ certification is provided by a named/TBC sub-consultant at cost, not a bundled inclusion.

---

### UC-05 — TPS compaction testing claimed package-wide, priced NBC-only — **PARTIAL / UNBACKED for 2 of 3 work areas** *(not among the four known)*
**Entity:** TPS only · **Claim family:** "allowance carried" / "cost carried"

> §77 (Noted Inclusions, no work-area qualifier): *"Compaction testing of our own trench backfill at the allowance carried, to the adopted standard stated at Appendix B query C13."*

**Propagation chain (2 locations):**
1. `Working_Proposals\TPS\TPS_ROK_Tender_Submission.docx` paragraph 77
2. `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.md` FAIL 3 (FT-30) — prior audit finding

**Model line asserted and independently verified:** the same two rate rows ("Compaction Testing - TEST" $115/ea and "Compaction Testing - Site Establishment" $90/ea) exist identically on all three work-area sheets, confirmed by direct cell read:
- `ClubHouse (NBC )` row 147/148: qty **15** / **4** → **$1,725 + $360 = $2,085**
- `Public Amenities (PAM)` row 145/146: qty **blank (0)** / **blank (0)** → **$0**
- `Siteworks ` row 145/146: qty **blank (0)** / **blank (0)** → **$0**

Siteworks carries the Ø200 main, the 236.88 m CW spine, the 217.73 m fire main and the 207.53 m gravity sewer — the majority of trench length in the entire package — at zero compaction-testing quantity, while the unqualified §77 sentence claims the allowance applies to "our own trench backfill" without restriction.
**Dollar value:** not currently priced for Siteworks/PAM (effectively $0 against the words used); the NBC comparator ($2,085 for a materially shorter trench run) indicates the true gap is a multiple of that figure, but per Rule 2 a precise number must be estimated fresh, not inferred from the NBC ratio.
**Severity:** HIGH — compaction testing is a genuine compliance/quality deliverable (VOL 38 §3.62), not a cosmetic clause, and Siteworks holds the longest runs in the package.
**Remedy:** add Siteworks and PAM compaction-testing quantities, or explicitly narrow §77's wording to "…of our own trench backfill within ClubHouse (NBC) works; Siteworks and PAM compaction testing is [priced/excluded] as follows…" until quantities exist.

---

### UC-06 — TPS fire "blankets" add-price held beyond the drawn kitchen unit — **PARTIAL** (minor/immaterial)
**Entity:** TPS only · **Claim family:** "add-price held"

> Appendix B query C10 (docx Table 10, row C10, column 4): *"Confirm fire equipment supply responsibility… Portable fire equipment (extinguishers, blankets other than the drawn kitchen fire [blanket])… Add-price held."*

**What is and isn't backed:** `EBC_Alternates` EBC-3 (`F26` = $2,540.78) backs the **extinguisher supply** (NBC ×8 + PAM ×1) exactly, and the base model separately carries one kitchen fire blanket (`NBC r308`, per `TPS_CHANGE_LOG.md` Repair 7). The Appendix B sentence additionally claims an add-price is "held" for **fire blankets beyond the one drawn unit** — no such line exists anywhere in `EBC_Alternates`.
**Dollar value:** no cost exists to measure; likely immaterial (no additional blanket is shown on any drawing beyond the one already priced), but the wording technically asserts a held price that isn't there.
**Severity:** LOW.
**Remedy:** either drop "blankets other than the drawn kitchen fire [blanket]" from the Appendix B sentence (nothing beyond the drawn unit is documented, so there is nothing to hold a price against), or add a trivial placeholder line if the Director wants the position formally reserved.

---

## 3. Converse check — EBC/alternate entries referenced nowhere externally

Every EBC and alternate line in both models was checked against both submissions, the RFI Schedule, and `01_SCOPE_MATRIX.md` for an external reference with a matching dollar figure.

| Entity | EBC/Alt line | Value | Externally referenced? | Verdict |
|---|---|---:|---|---|
| TPS | EBC-1 Sewer rising main | $15,717.29 | Yes — docx §112/§594, Table 10 row C1, RFI C1, matrix 2.1-x2, D6 register | **PASS** |
| TPS | EBC-2 Trade waste application | $4,147.67 | Yes — docx §114, Table 10 row C8, matrix X3, CONFLICT_LOG A2 | **PASS** |
| TPS | EBC-3 Fire extinguisher supply | $2,540.78 | Yes — docx §86/§350, Table 6/8/10 (C10), matrix 4.11-d/3.11-d, CONFLICT_LOG B8 | **PASS** |
| TPS | EBC-4 Pump station (evidence-only, NO PRICE CARRIED) | n/a (evidence, not a price) | Yes, correctly as *evidence*, not as a held reinstatement price — docx §112, `LABOUR_REVIEW_PACK.md` P08 | **PASS** (intentionally not offered — station is Council's scope, not TPS's, so no add-price is appropriate) |
| TPS | ALT-1 Ø200 copper main alternate | $36,891.78 sell delta | **Deliberately not offered** — docx §52 states "no in-ground copper alternate offered" explicitly, matching the model's own note "retained here as a cost record only" and the locked §5.5 decision | **PASS** (consistent non-disclosure, not a silent orphan — the non-offer is itself stated) |
| TPS | ALT-2 Building water >DN22 copper alternate | $1,169.23 sell delta | Yes — docx §10/§53, value ties exactly | **PASS** |
| TCS | EBC E1 Kerb chutes | $55,429.90 | Yes — docx §172, Table 8 row 8, RFI B8, matrix 2.3-x1, CONFLICT_LOG F1, D6-F1 | **PASS** |
| **TCS** | **EBC E2 Detention basin / concrete spillway** | **$52,523.57** | **No.** The submission (§7.7, §130/§132, Table 3 row 3 col 3, Table 8 row 5 col 4) and RFI B5 state only that the basin/spillway is "excluded — not in the drainage package" / "not priced". None of these external-facing documents say an add-price is held or can be provided on request — unlike the sibling kerb-chute exclusion, which uses exactly that language. | **ORPHANED — UC-07** |
| TCS | EBC E3 Subsoil/strip-filter (excluded, by others) | n/a — status record, not a held price | Yes, correctly recorded as a stated exclusion with an interface point (docx §7, matrix 2.3-x2/2.5-x3) — no add-price is claimed or expected since it is a genuine "by others" boundary, not TCS scope on option | **PASS** |

**Finding UC-07 (converse direction), in full:** TCS's own internal documents (`EBC` sheet cell `G24`: *"Reinstatement: set Stage1A_Drainage labour B-07 = 10 cd; enter spillway material rows at X1; add 5 plant-days 3-5T."*; `TCS_CHANGE_LOG.md` §5 item 9; the D6 register D6-F3; `RUN_STATUS.md`) all treat the $52,523.57 spillway build-up as a live, reinstatement-ready add-price exactly like the kerb chutes. But the client-facing text never says so — it reads as a flat, no-recourse exclusion. This is the mirror image of UC-01–UC-04: there, words promised a price that doesn't exist; here, a price exists that the words never promise. Both are the same underlying defect (a broken link between sentence and cell), just travelling in opposite directions.
**Severity:** MEDIUM — no cost is wrong, but if detention-basin/spillway scope is later assigned to TCS (a live open item per RFI B5 and D6-F3), the current wording gives TCS no contractual foothold to claim the pre-built $52,523.57 price; it would look like an unbudgeted variation instead of a pre-agreed add-price.
**Remedy:** Director call — either reword §7.7/§130/§132/Table 8 to match the kerb-chute pattern ("excluded; an add-price is held and can be provided on request"), or leave it deliberately silent as a considered negotiating position — but the choice should be made consciously, not by omission, and should be documented as a decision either way.

---

## 4. Pattern analysis — where this comes from and why it recurred on two independently-built models

**The common mechanism: sentence-before-cell.** Every defective claim in this audit (UC-01 through UC-06) was written as a **statement of intent** — usually lifted near-verbatim from an upstream planning document (`SUBMISSION_TEMPLATE_ANALYSIS.md` row N11 for shop drawings; the RFI Schedule's own query wording for the lodgement claim; a generic "Noted Inclusions" clause for RPEQ and compaction testing) — **before** the corresponding cost cell existed, on the working assumption that the model would be built out to match. In every failing case, that second step was never completed or was completed only partially (UC-03's excavation-yes/quarry-no split is the clearest example: the easy half of a compound instruction was wired in, the harder half — a brand-new material row — was not).

Every claim that **passed** (§3's PASS rows, plus EBC-1/2/3 TPS and EBC E1 TCS) shows the opposite construction order: the cost was built first as a small, closed, cell-referenced block (`EBC_Alternates!F12`, `F19`, `F26`; `EBC!F14`; `Prelim_OH!B26`), and the client-facing sentence was written afterwards to quote that block's number. Sentence-follows-cell produces a verifiable claim by construction; cell-follows-sentence produces an aspirational one that is only verifiable by accident.

**Why it happened independently on two entities, not just once:** TPS and TCS were built by different drafters/passes (TPS repaired, TCS rebuilt — `COST_MODEL_REBUILD_DECISION.md`), but both inherited the **same shared upstream template clause** for departures from spec (`SUBMISSION_TEMPLATE_ANALYSIS.md` N11: "excluded — flagged departure … add-price carried"), applied as boilerplate to every H002/VOL 38 clause the drafters chose to depart from. Because the clause reads identically regardless of whether a cost exists behind it, and because it was copied into both submissions from the same source, the shop-drawings gap (UC-01) is not two coincidental defects — it is one shared defect expressed twice. The GT quarry gap (UC-03) shows a related but distinct mechanism: the migration engineer correctly saw that the *old* workbook's GT package was orphaned (fed no roll-up) and reinstated the loud, visually obvious half (channel supply + trash boxes + labour — easy to check, because it produces a large, checkable dollar jump), while the quiet half (a missing term in an existing SUM formula) escaped the same scrutiny precisely because nothing failed loudly — the bedding-stone cell still computed a plausible non-zero number, just the wrong one (missing ~123 tonnes of stone). The converse case (UC-07) shows the same disconnect running the other way: once the cost side is done correctly, there is no equivalent gate that forces the wording side to catch up — one sibling clause (kerb chutes) got the disclosure sentence and the near-identical adjacent clause (spillway) did not, purely because of which pass or drafter touched which paragraph, not because of any difference in the underlying facts.

**Root cause, in one sentence:** wording and cost-modelling are performed as two separate activities by two different (or differently-timed) actors, and nothing in the process requires a claim-bearing sentence to cite — and a QA pass to verify — its own specific `Sheet!Cell` reference before that sentence is allowed to leave the internal team.

---

## 5. Recommended convention

**Adopt one rule: "no cell, no claim" — cell before sentence, every time, both directions.**

> Any sentence in any external-facing document (submission, RFI Schedule, risk register) that uses the words *add-price*, *held*, *reinstated*, *carried*, *included*, *costed*, or *priced elsewhere* in connection with a named scope item must be drafted **after**, and must cite in an adjacent internal drafting note (not necessarily in the client-facing text itself), the exact `Sheet!Cell` or EBC-row reference where that price lives. Before that sentence is allowed to leave the internal register into any client-facing or RFI document, an independent reviewer must open the cited cell and confirm: (1) it is non-zero, (2) it feeds a live SUM/roll-up that reaches a totalled figure (not an orphaned formula), and (3) for compound claims ("A and B", "excavation and quarry"), each conjunct is checked independently — a claim is only as strong as its weakest half. The same rule runs in reverse for every EBC/alternate line built into either model: before the model is signed off, every such line must have a matching client-facing sentence drafted from it (or a documented Director decision to keep it silent) — a costed line with no sentence is graded exactly the same as a sentence with no costed line.

This single convention would have caught all four originally-known instances and all three newly-found ones (UC-04, UC-05, UC-07) at first-draft stage, because in every failing case here the missing link is the same one: no cell was cited, or the cited cell was never checked, before the sentence shipped.

---

## 6. Files read (read-only, none modified)

- `Working_Proposals\TPS\TPS_ROK_Tender_Submission.docx`, `Working_Proposals\TCS\TCS_ROK_Tender_Submission.docx`
- `Working_Cost_Models\TPS\ROK_TPS_CostModel_V2.xlsx` (12 sheets, both `data_only` modes), `Working_Cost_Models\TPS\TPS_CHANGE_LOG.md`
- `Working_Cost_Models\TCS\ROK_TCS_CostModel_V2.xlsx` (11 sheets, both `data_only` modes), `Working_Cost_Models\TCS\TCS_CHANGE_LOG.md`
- `Working_Cost_Models\TCS\MIGRATION_RECONCILIATION.xlsx` (`Summary`/`Bridge`/`Register`/`CellIndex`)
- `_Tender_Control\03_Scope_and_Interfaces\01_SCOPE_MATRIX.md`, `CONFLICT_LOG.md`
- `_Tender_Control\04_Quantity_Reconciliation\QUANTITY_RECONCILIATION_SUMMARY.md`
- `_Tender_Control\06_Material_and_Quote_Register\QUOTE_REGISTER_NOTES.md`
- `_Tender_Control\07_Commercial_Reconciliation\EQUIPMENT_TEST_TPS.md`, `EQUIPMENT_TEST_TCS.md`, `COST_MODEL_REBUILD_DECISION.md`
- `_Tender_Control\08_Risks_Assumptions_Qualifications\RFI_SCHEDULE.md`, `06_ASSUMPTION_GAP_RISK_REGISTER.md`
- `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.md`, `SCOPE_TO_COST_CONCORDANCE_TCS.md`, `SUBMISSION_TEMPLATE_ANALYSIS.md`
- `_Tender_Control\00_Run_Status\RUN_STATUS.md`
- `_Tender_Control\05_Programme_Labour_Plant\LABOUR_REVIEW_PACK.md`
- `TENDER_PROMPT.md`

No file outside `_Tender_Control\09_QA_and_Red_Team\UNBACKED_CLAIMS_AUDIT.md` (this file) was created, edited, or committed.
