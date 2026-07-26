# SCOPE_TO_COST_CONCORDANCE_TPS — Rule 4 Scope-to-Cost Concordance Pass

**Tender:** TEN16699 Rockhampton Sports Precinct Stage 1A & 1B — **TPS (hydraulic) submission only.** TCS is out of scope for this pass and was not opened, analysed or written to.

**Submission tested:** `Working_Proposals\TPS\TPS_ROK_Tender_Submission.docx` (pre-concordance draft, treated as unverified per instruction)
**Cost model tested:** `Working_Cost_Models\TPS\ROK_TPS_CostModel_V2.xlsx` — 12 sheets, loaded both `data_only=True` (cached, Excel-COM-recalculated) and `data_only=False` (formulas)
**Companion deliverable:** `SCOPE_TO_COST_CONCORDANCE_TPS.xlsx` (4 sheets: Forward_Test, Reverse_Test, Equipment_Test_Reconciliation, Findings_Summary)
**Method:** every sentence in the draft asserting, implying or capable of being read as asserting inclusion of scope was enumerated (not sampled) across the cover letter, Basis of Tender, Description of Proposed Services, Hydraulic Basis, Noted Inclusions, Building-Specific Scope Clarifications, Fixture and Equipment Allowance, Access and Attendance Basis, Provisional Sums, and Construct-Only Basis sections. Each was traced against the 12-sheet workbook (row-level), `01_SCOPE_MATRIX.md`, `CONFLICT_LOG.md`, `EQUIPMENT_TEST_TPS.md` and the supporting registers. **Read-only** — nothing in the submission, cost model or any register was edited.

---

## 1. Headline: is the draft fit to proceed to red-team?

**Not yet — proceed only after four fixes.** The submission is, on the whole, an unusually well-disciplined piece of Rule 4 drafting — quantities reconcile to the cost model to the centimetre in every case checked (fire main 217.73 m, CW spine 236.88 m, branches 111.51 m, gravity sewer 207.53 m, NBC sanitary 268.4 m, NBC trade waste 54.78 m, PAM sanitary 68.09 m all tie exactly), the Billi Principal-supply wording is exactly right, the four Rule 4 prohibited-wording patterns were searched for and none were found, PC Sums reconcile to the fixture quote build-up to the dollar, and the headline commercial figures tie exactly to the locked figures (see §2). But four defects would fail a red-team pass as currently worded, and none are cosmetic:

1. **Two "add-price held" claims are unbacked** (plumbing approval lodgement, §114/C8; shop drawing production, §116) — no costed line exists anywhere in `EBC_Alternates` or any register despite three separate documents (the proposal, the RFI Schedule, and the Assumption/Gap/Risk Register) asserting one is "held."
2. **Compaction testing is claimed package-wide but priced NBC-only** — Siteworks and PAM both carry the rate line at zero quantity, while Siteworks holds the longest trench runs on the entire package.
3. **RPEQ certification has no cost anywhere in the 12-sheet model**, despite being named as an included deliverable twice (§79, §145).
4. **The "Stage 1B remains viable and capable of award alone" claim rests on a proportional crew-day split of one combined-programme prelim/mobilisation cost**, not an independently-costed stand-alone scenario — a real risk to the standalone-viability assertion Locked Decision §5.2 requires.

None of these are the kind of over-claiming Rule 4 exists to catch in the worst case (nobody is told "all hydraulic services" are included when they aren't) — they are quieter defects: claims that are *technically true in direction* (something is excluded, or something is included) but *not fully backed by a traceable, complete cost allowance* behind the specific words used. That is exactly what Rule 4's forward/reverse tests are designed to surface, and this pass surfaced four of them plus seven lower-severity items.

---

## 2. Verdict counts

**Forward test (41 rows — one row per inclusion assertion or group of closely related assertions):**

| Verdict | Count |
|---|---|
| PASS | 30 |
| PARTIAL | 5 |
| FAIL | 5 |
| UNTRACEABLE | 0 (folded into FAIL rows FT-38/FT-39/FT-32 where the defect is a total absence of cost, per Rule 2 — flagged, not invented) |

**Reverse test (16 rows — one row per major cost-model cluster, hunting for cost with no external home):**

| Verdict | Count |
|---|---|
| PASS (clean) | 9 |
| PASS with a caveat / cross-reference | 5 |
| PARTIAL | 1 |
| FAIL | 1 (RPEQ, cross-referencing the same forward-test finding) |

**Equipment test reconciliation (14 items, per `EQUIPMENT_TEST_TPS.md`):** **14 of 14 MATCH.** Every wording control in that test's §6 was checked against the actual draft sentence-by-sentence and every one is correctly applied — most importantly, the Billi Quadra 4180 wording ("installation and connection only of the five Principal-supplied Billi Quadra 4180 units") is exact, never "Billi units included." This confirms the draft was updated **after** the equipment test closed its two fixings gaps (HWU stainless plinths) — the submission text explicitly names the plinths, which only exist in the model because of that repair.

**Prohibited wording (§2 Rule 4) — zero hits.** Searched the full document text for "all hydraulic services", "complete system", "fixtures included", "priced in full" (as a self-referential claim), "comprehensive", "fully compliant", "entire scope", "guarantee/warrant". The only "priced in full" hit refers to **TCS's** scope (grated trench drains, correctly cross-referred and excluded from TPS), not a TPS self-claim. No blanket introductory language was found that could override the detailed exclusions.

---

## 3. Figures — tie-out against the locked numbers

| Figure | Locked | Draft / model | Status |
|---|---|---|---|
| Stage 1A total | $1,743,304.82 | $1,743,304.8183 → $1,743,304.82 | **Ties exactly** |
| Stage 1B total | $266,489.36 | $266,489.3588 → $266,489.36 | **Ties exactly** |
| Grand total ex GST | $2,009,794.18 | $2,009,794.1771 → $2,009,794.18 | **Ties exactly** |
| PC Sums (separately identified) | $339,613.84 | $339,613.8355 → $339,613.84 | **Ties exactly**, and correctly NOT folded into the headline lump-sum figures in Table 1 |
| TPS ABN | 91 620 147 935 | 91 620 147 935 (cover letter, cover table, signature block — all three instances checked) | **Correct, 11 digits, no 89-prefix or 10-digit defect found anywhere in this document** |
| Markup | 41.5% (5.5% prelim + 18% O/H + 18% profit, each on cost, after ×1.18 contingency) | TCS $ Sched R42/43/47/51 confirm exactly this sequence and rate | **Correct** — with one disclosed exception: the four big-ticket equipment blocks (GIT, HWU×2, pump, HWU×1) still carry the legacy ×1.15 token instead of the 41.5% chain, a live Director decision already quantified in `EQUIPMENT_TEST_TPS.md` §5 ($6,805.55 sell delta if normalised) — not a new finding, carried forward. |
| Pump station | Removed, Add-2 note | `EBC_Alternates` EBC-4 confirms "NO PRICE CARRIED"; proposal §112 states the Addendum 2 interface in full (gravity sewer to inlet piece / rising main add-price / electrical exclusion) | **Correct** |
| GST | Removed, ex-GST throughout | Confirmed — "ex GST" stated on every pricing table, cover table and Conditions clause | **Correct** |

**No figure in the submission fails to tie to the locked set.** The workbook's internal tie check (`TCS $ Sched` N88, "Tie check (N64+N78-N87)=0") reads exactly 0.

---

## 4. Every FAIL and UNTRACEABLE, in full, with dollar exposure

### FAIL 1 — Plumbing approval lodgement "add-price held" is unbacked (FT-38)
> §114: *"Plumbing approval lodgement, application documentation and attendance at approval inspections are excluded — a stated departure from the Plumbing Subcontractor provisions of ITT Part 2 §16, with an add-price held (Appendix B query C8)."*

Searched all 12 workbook sheets and `EBC_Alternates` for "lodge / lodgement / approval application" — **no cost line exists.** The RFI Schedule (query C8: *"an add-price applies (held internally)"*) and the Assumption/Gap/Risk Register (D6-F6: *"add-price held on EBC"*) both repeat the same unbacked claim. This is distinct from EBC-2 (Trade Waste application specifically, $4,147.67, correctly costed) — the broader ITT §16 lodgement obligation has never had a line built for it.
**Dollar exposure:** unquantified — not to be assumed equal to EBC-2's figure, which covers a narrower obligation. Director must build a fresh cost estimate.

### FAIL 2 — Shop drawing production "add-price held" is unbacked (FT-39)
> §116: *"Shop drawing production is excluded — a stated departure from H002 note 2, with an add-price held and available on request."*

Same defect as FAIL 1. `Sched3_Extract` R51 even cross-references *"shop drawings (X1 - EBC in the tender control register)"* — but that register entry was never created anywhere in `_Tender_Control`.
**Dollar exposure:** unquantified for the same reason.

### FAIL 3 — Compaction testing priced NBC-only, claimed package-wide (FT-30)
> §77 (Noted Inclusions, applies to the whole package, no NBC-only qualifier): *"Compaction testing of our own trench backfill at the allowance carried, to the adopted standard stated at Appendix B query C13."*

The rate line ("Compaction Testing - TEST" $115/ea, "Compaction Testing - Site Establishment" $90/ea) exists identically on all three work-area sheets, but only `ClubHouse (NBC )` carries a non-zero quantity (15 tests + 4 establishments = $2,085). `Public Amenities (PAM)` and — critically — `Siteworks ` (which carries the Ø200 main, the 236.88 m CW spine, the 217.73 m fire main and the 207.53 m gravity sewer, i.e. the great majority of trench length in the whole package) both show **QTY = 0** against the identical rate.
**Dollar exposure:** not currently priced for Siteworks/PAM (effectively $0); the NBC comparator ($2,085 for a materially shorter trench run) indicates the true gap is a multiple of that, but a precise figure must be estimated fresh rather than assumed — flagged per Rule 2, not invented.

### FAIL 4 — RPEQ certification has no cost anywhere in the model (FT-32 / RT-14)
> §79 (Noted Inclusions): *"As-constructed documentation, RPEQ certification and ADAC-compliant XML deliverables for the hydraulic package's own water, sewer and fire assets…"* — repeated at §145 (Construct-Only Basis).

Searched all 12 sheets for "RPEQ" — **zero matches.** RPEQ sign-off is normally a discrete external-consultant engagement with a real fee; nothing in the model — not even a round-number allowance of the kind used for articulation/seismic — represents it.
**Dollar exposure:** unquantified; no comparator exists in the model to anchor an estimate. Director must obtain a quote or set a disclosed allowance before repeating the claim.

*(The CCTV/ADAC single-line-coverage question, also raised at FT-32, is graded PARTIAL not FAIL — a $5,000 allowance does exist, its basis just doesn't cleanly reconcile to the full package's in-ground drainage length; see §5 below.)*

### FAIL 5 (forward-test numbering FT-13) — Traffic control, erosion/sediment control and trade set-out carry zero itemised cost
> §59 (Noted Inclusions): *"…traffic control for our own works and deliveries, erosion and sediment control local to our own open trenches, and trade set-out from Principal-supplied survey control."*

No material/plant/labour rate exists anywhere in the 12-sheet model for any of these three items — unlike genset, porta loo, potable water and container hire, which ARE itemised bottom-up on `00_ TCS Prelim & OH`. They rest entirely on the blanket 5.5% prelim percentage, which the model's own cross-check (R89–91) already shows running **$19,628 (+30.8%) short** against the items it *does* itemise.
**Dollar exposure:** the $19,628 (cost) / ≈$27,772 (sell, at the 41.5% chain) prelim shortfall is already disclosed by the model itself, before these three unpriced items are even added on top.

---

## 5. PARTIAL findings (not FAIL, but material enough to name)

- **FT-01 — Standalone-viability claim for Stage 1B.** The proposal states twice ("§6", "§8") that Stage 1B "remains viable and capable of award alone," but its prelim/OH/mobilisation cost is computed once for the combined 9.4-month, 3-mobilisation programme and apportioned to 1B by a simple 20/166 crew-day ratio — not independently re-estimated for a stand-alone smaller award, which typically carries a *higher*, not lower, overhead percentage. **HIGH severity**, no dollar figure assigned (structural/methodology risk, not a specific missing cost).
- **FT-08 — HDPE main rate is benchmark-derived, not project-quoted (Gap #5).** The single most confidently-worded technical position in the whole submission (the copper-vs-HDPE departure, §52) rests on a rate that is flagged internally as pending RFQ. **MEDIUM severity.**
- **FT-32 — CCTV/ADAC coverage.** A single $5,000 allowance sits on `Siteworks ` only, basis "~385 m," against a package-wide in-ground drainage total (NBC + PAM + Site) of materially more than that. **MEDIUM severity.**
- **FT-41 — Downpipe count internally inconsistent** across Table 6 ("eleven"), Query C11 ("11 NBC + 4 PAM as drawn") and Table 8 ("19 adopted" for a combined row), while the cost model actually prices 23 (19 NBC + 4 PAM) — no dollar exposure since the model over-covers, but a red-team reader will flag the self-contradiction. **LOW severity.**
- **RT-02/RT-03 — Prelim/O/H cross-subsidy.** At the combined level the O/H allowance ($208,791) exceeds bottom-up O/H ($169,200) by $39,591, more than offsetting the prelim shortfall (RT-02) — so the *total* price is not short, but the labelling (calling a prelim shortfall "covered" by an unrelated O/H surplus) is a governance/presentation issue worth tidying internally. **MEDIUM severity**, not counted twice against the FAIL total.
- **RT-12 — Fixture quote header defect.** The $252,694.77 Tradelink 1066143 quote underlying the entire fixture PC Sum is addressed to "TriCore CIVIL Services Pty Ltd" at the wrong street number and suburb. Not a proposal-wording defect (the draft doesn't repeat the error) but a real Rule 1 traceability/order-placement risk before award. **LOW severity** for the tender itself.

---

## 6. Prohibited-wording scan — result and why nothing needed replacing

Every phrase in §2 Rule 4's prohibited list was searched for verbatim and by close paraphrase across the full document text (181 paragraphs, 11 tables): "all hydraulic services," "all civil services," "complete system," broad introductory scope language, and any unqualified claim that fixtures/tapware/bubblers/equipment are included. **None were found in a form that oversells the priced scope.** The nearest candidates and why each is compliant:

- §30 closing scope statement ("includes the supply, installation, testing, commissioning, certification, handover and defects liability obligations necessary to deliver the included hydraulic scope **only**") — correctly self-limiting, not a broadening statement.
- §60 "Temporary site services for our own works **in full**" — scoped to "our own works," not a package-wide blanket. Compliant, though see FT-13/FT-14 for whether the underlying cost is actually complete.
- §106 "priced **in full** by TriCore Civil Services" — refers to TCS's scope (grated trench drains), correctly excluded from and cross-referred out of the TPS submission, not a TPS self-claim.
- §83 is a model example of the *opposite* of prohibited wording — an explicit narrowing clause: *"No fixture, tapware or equipment supply is included elsewhere, and no statement in this submission is to be read as including supply beyond the PC Sums stated."*

No suggested replacement wording is required for any prohibited-wording hit, because none was found. The wording work required by this pass is confined to the four FAIL items in §4 (either cost the claim, or soften the wording to match what is actually costed) and the standalone-viability claim in §5.

---

## 7. What must change before the draft goes to red-team (ranked)

1. **Build EBC-5 (plumbing approval lodgement) and EBC-6 (shop drawing production) in `EBC_Alternates`** with genuine cost build-ups, or remove the "add-price held / available on request" language from §114/§116 and the RFI Schedule/Risk Register until real figures exist.
2. **Add Siteworks and PAM compaction-testing quantities** (or explicitly narrow §77's wording to NBC-only) before the package-wide claim is true.
3. **Cost or qualify RPEQ certification** — either add a consultant-fee line or state in §79/§145 that RPEQ certification is provided by a named/TBC sub-consultant at cost, not a bundled inclusion.
4. **Test the Stage 1B standalone-viability claim against an independent stand-alone cost scenario**, or soften §6/§8 to acknowledge the apportionment method until that scenario exists.
5. Close **Gap #5 (HDPE main rate)** with a live project quote before the tender's headline technical position is finalised.
6. Reconcile the **CCTV/ADAC $5,000 allowance basis** against the full ~600 m package-wide in-ground drainage length, or confirm/replace it with a per-entity figure.
7. Correct the **downpipe count inconsistency** (Table 6 "eleven" / Query C11 "11+4" / Table 8 "19") to a single, internally consistent figure (23 total, matching the cost model).
8. Obtain a **corrected-header confirmation from Tradelink** for quote 1066143 before order placement (not a submission blocker, but should not wait until after award).
9. Tidy the **prelim/O/H cross-subsidy labelling** (RT-02/RT-03) for internal governance clarity — no external wording change required, total price is not short.
10. Carry forward (already logged, not new): the **big-ticket equipment margin decision** (14.49% vs 41.5% chain, $6,805.55 sell delta) from `EQUIPMENT_TEST_TPS.md` §5 remains open for the Director.

---

## 8. What did NOT need fixing — confirming the draft's strengths

- Every quantity claim checked against the cost model reconciled exactly (see §1) — no evidence of proposal quantities drifting from priced quantities anywhere in the sanitary, trade waste, fire, water or gravity-sewer systems.
- The Billi Quadra wording, the PC Sum "no statement… is to be read as including supply beyond the PC Sums stated" clause, the rising main EBC-1 add-price, the trade waste EBC-2 add-price, and the fire extinguisher EBC-3 add-price are all model examples of correct Rule 4/Rule 5 treatment — quantified, disclosed, and worded exactly as the equipment test's wording controls require.
- No prohibited blanket wording exists anywhere in the document.
- All locked commercial figures (§5.4 of `TENDER_PROMPT.md`) tie exactly, including the PC Sum figure being kept visibly separate from the headline lump sums.
- The ABN is correct (91 620 147 935, 11 digits) in all three places it appears — no repeat of the CQU HYD template's 10-digit defect.

---

## 9. Files produced

- `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.xlsx` — 4 sheets: `Forward_Test` (41 rows), `Reverse_Test` (16 rows), `Equipment_Test_Reconciliation` (14 rows, 14/14 match), `Findings_Summary` (11 ranked findings, most severe first).
- `_Tender_Control\09_QA_and_Red_Team\SCOPE_TO_COST_CONCORDANCE_TPS.md` — this file.

Nothing else was created, edited or touched. TCS's submission, cost model and registers were not opened.
