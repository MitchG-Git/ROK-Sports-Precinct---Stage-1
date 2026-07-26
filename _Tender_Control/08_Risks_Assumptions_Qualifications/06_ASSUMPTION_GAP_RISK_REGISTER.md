# D6 — ASSUMPTION, GAP & RISK REGISTER (INTERNAL)
TEN16699 Rockhampton Sports Precinct Stage 1A & 1B · TCS + TPS · tender-run-01 · 27 July 2026
**INTERNAL ONLY — NOT FOR ISSUE.** Confidence is rated on four separate dimensions per §9.1 because a blended rating hides where the risk actually sits: **Qty** (quantity confidence) · **Lab** (labour) · **Mat** (material price) · **Prog** (programme). H = high, M = medium, L = low.

Cross-references: `03_Scope_and_Interfaces/CONFLICT_LOG.md` (CL-x) · `08_.../RFI_SCHEDULE.md` (RFI A1–C14) · `04_Quantity_Reconciliation/QUANTITY_RECONCILIATION.xlsx` (Opens #n) · `06_Material_and_Quote_Register/` (Gap #n) · `Working_Cost_Models/*/`*_CHANGE_LOG.md.

---

## 1. DIRECTOR DECISIONS REQUIRED BEFORE ISSUE

| # | Decision | Position now | Why it needs you | $ effect |
|---|---|---|---|---|
| **D6-F1** | **Kerb chutes — in or out?** | Base price EXCLUDES them; add-price held on the TCS EBC sheet | Denis's 17 Jul note allowed rock + erosion mat (56 m²); his 24 Jul note excluded kerb chutes entirely as "not the work scope". §5.3 of your prompt says "kerb chute concrete excluded (rock and erosion control mat only, per Denis)". The two Denis positions conflict and the later one governs by date — but §5.3 codified the earlier one. Design Report §6.1 *increases* kerb-chute extent (they now replace pit-and-pipe headwall outlets), so this is growing scope, not shrinking. 9 structures in F1310. | Add-price on EBC (9 chutes + rock/mat + 9 crew-days) |
| **D6-F2** | **TPS big-ticket markup** | Left as-is: ×1.15 + freight, no prelims/OH/profit. Equipment test now proves installation labour sits in the crew-day blocks (T1-08/T4-03/T4-06), so the ×1.15 is doing a pure supply-margin job — **14.49% effective vs the model's 41.5%**, and $850 of freight carries no margin at all. Purchase+freight cost $25,200.17; current sell $28,852.70; normal chain $35,658.24. | **+$6,805.55** exactly (1A +$6,195.05, 1B +$610.50) → grand total $2,016,599.73 if adopted |
| **D6-F3** | **Detention basin earthworks + 50 m concrete spillway weir** | Carried at **$0** with a flagged row; RFI raised (RFI B5) | Annotated on the drainage drawings but quantified in no schedule by anyone — not by SportEng, not by Denis. Almost certainly bulk earthworks (not our package), but if it lands on TCS it is a material unpriced scope. 10 crew-days held on the EBC sheet. | Unquantified until the RFI answers; EBC labour held |
| **D6-F4** | **TPS prelims shortfall** | Bottom-up prelims $83,425 vs the 5.5% allowance $63,670 = **31% over** | Unlike TCS (which resolved once supervision moved to direct labour, now +$49k surplus), TPS's genuine prelims still exceed the pool — driven by a 10-month programme across **three separate mobilisations** and its own standalone temp services. Options: carry the delta out of OH/profit, or lift the prelims percentage. Do not invent a new corporate percentage without your call. | ≈ **$19,755** currently absorbed by margin |
| **D6-F5** | **TPS ABN** | Using **91 620 147 935** (verified on the ABR) | Both prior submissions AND the master prompt carry invalid numbers (`9 620 147 935` / `89 620 147 935` — the latter fails the ABN check-digit test). Needs your confirmation, and a look at where the invalid number may have gone out before. See `09_QA_and_Red_Team/ENTITY_IDENTIFIER_VERIFICATION.md`. | Nil to price; compliance/credibility risk |
| **D6-F6** | **Plumbing approval lodgement excluded** | Excluded per §5.3; add-price held on EBC | ITT Pt 2 §16, H002 note 2 and note 25 each place obligations on the plumbing subcontractor. Excluding them is defensible (and §16 gives FRW Private Works to the Principal Contractor anyway), but it is a **departure from three specific clauses** and a builder could price it back in or mark TPS non-conforming. Surfaced exactly as your prompt directed. | EBC add-price held |

---

## 2. RISK REGISTER

### 2.1 TCS — Civil Stormwater

| Risk | Cost code / area | Source | In/Out | Qty | Lab | Mat | Prog | Contingency location | Potential impact | Prob | Rating | Treatment |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **VOL 35 Civil & Field of Play Specification not issued** — the governing specification for the entire TCS submission | All TCS | Paynters register vs docs received | Priced on drawings + CMDG + RPT006_B | M | M | M | M | None specific — systemic | Unknown requirements beyond CMDG (testing regimes, material classes, tolerances) | Med | **HIGH** | Narrow qualification + RFI A7. **§12 rule applied: no TCS scope section may be rated High while this is missing** |
| **Rock beyond the geotech-inferable band** | Trenching, pits | NQL2024-0320: refusal at 25/36 locations, shallowest 0.70 m; XW rock 0.2–2.2 m at 6 pits | Base allows anticipated band (10 crew-days) | M | **L** | H | M | A-08 labour allowance + ×1.18 on materials | Extra-over rates tendered ($239–$598/m³) recover it **only on written direction** (ITT §18) | High | **HIGH** | Rate schedule tendered per H002 n.24; RFI A2 to settle which of three rock regimes governs |
| **Trench support method** — geotech requires 1.5H:1V batters for excavations <2 m, or shielding, for personnel entry | All trenching | Geotech §5.3.3 | Shields priced for entered runs | M | M | M | M | Plant allowance | Battering instead of shielding widens every trench: excavation, spoil, bedding, backfill all grow | Med | **HIGH** | RFI A3; basis stated in submission |
| **C09A/C09B twin culvert detailed nowhere** | Culverts | F1304 layout vs F1310 vs F1321 | Priced as standard precast headwalls | **L** | M | M | H | ×1.18 materials | Non-standard structure could be materially different | Med | MED | RFI B1 with the corrected-schedule request |
| **Design Report Rev B changes not drafted into T1 sheets** | Kerb chutes, strip filters, SE culvert, basin | RPT006_B §6.1/§9.1 vs un-reissued T1 | Priced T1-as-modified | M | M | M | M | ×1.18 | A further reissue changes quantities | Med | MED | Basis stated + RFI B4 |
| **EDQ Conditions 16/17 — 20-business-day review gates before stormwater start** | Programme | RPT006_B §3.1 | Remob allowance as a line (not spread) | H | M | H | **L** | Prelims remob line + 4 crew-days | Delay/remobilisation beyond the allowance | Med | MED | Qualified; not our approval to obtain |
| **Reece Fibretec rate anomaly** — $232.94/m charged vs an embedded "$198.00" annotation | Trench drains | Reece Q-459014445 | Priced at quoted rate | H | H | **L** | H | — | **$19,217 saving** if the lower rate is real | Med | MED (opportunity) | Confirm with Reece before award |
| **Humes vs Reece take-off disagreement** (RCP375 299 vs 262 lengths) | Pipe supply | Quote register | Adopted 714.9 m governs | M | H | M | H | ×1.18 | Supplier quantity dispute at order | Low | LOW | Our adopted quantity governs; reconcile at order |
| **Crane / franna / trench shields absent from all hire registers** | Plant | Equip_Master flag | Estimator allowances | H | M | **L** | H | Plant allowance | Rate risk on unbenchmarked items | Med | MED | Obtain rates before award |

### 2.2 TPS — Hydraulic

| Risk | Cost code / area | Source | In/Out | Qty | Lab | Mat | Prog | Contingency location | Potential impact | Prob | Rating | Treatment |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **Fixture counts** — 7 of 9 architectural sheets never counted; architectural volumes 03/08 not issued | NBC + PAM fit-off, fixture PC | Denis "unfinished"; recount adopted 21 WC / 14 basins / 10 showers / PAM 8 WC | Priced at adopted counts | **L** | **L** | M | M | PC extension + ×1.18 | Drives both the fixture PC sum **and** the fit-off labour (93 fixtures at 7 EA/day) | High | **CRITICAL** | Recount mandatory before issue; RFI C6 on quantities + supply split; Tradelink reconciliation |
| **Pump station interface undefined** — Council installs, but the rising main discharge is "location to be confirmed" and no tie-in to the Ø225 main is shown | Site sewer | Add 2 vs H003 vs VOL 38 §24 | Station excluded; rising main EBC 110 m | **L** | M | M | M | EBC $15,717 | H002 n.15 could deem connecting works included if not raised | High | **CRITICAL** | RFI C1 defines all six interfaces; EBC add-price ready |
| **Fire service extent** — one dual pillar hydrant + one booster for 16 courts and two buildings; H003 shows no lengths and no legible hydrant symbols | Fire main | H003; measured 217.73 m DN125 | Priced as drawn | M | M | M | M | ×1.18 | AS 2419.1 coverage assessment could require more hydrants + mains | Med | **HIGH** | RFI C3 + block plan request (VOL 38 §25 requires pre-manufacture approval) |
| **316 stainless press-fit >DN22** — no supplier rate obtainable (Tradelink refused) | NBC + PAM water | H-NBC-002 WS2 | Conforming SS as base; copper as labelled alternate | M | M | **L** | H | Benchmark-derived (copper ×1.5 on fittings) | Rate risk on the base offer's principal material | High | **HIGH** | Gap #2 RFQ before award; alternate held outside the sum |
| **Ø200 HDPE main** — no project quote; benchmark-derived from smaller SDR11 rates | Site water main | VOL 38 §10.1 equivalence | HDPE base; copper alternate +$36,892 | H | H | **L** | H | Benchmark tag in-cell | Rate risk; and rejection of the departure forces copper | Med | **HIGH** | Gap #5 RFQ; four-legged qualification drafted (spec table, authority, geotech aggressivity, whole-of-life) |
| **Equipment installation coverage** (HWUs, hot water pump) | Big-ticket | `Installation_MH` tokens $200–$600 | **RESOLVED — test passed** | H | M | H | H | n/a | Equipment test complete: 14 items, 12 complete on first pass, installation proven in T1-08/T4-03/T4-06, 4 duplicate tokens zeroed with traceability notes, 2 genuine gaps closed (HWU SS plinths $520; long-lead storage $1,200). See `07_Commercial_Reconciliation/EQUIPMENT_TEST_TPS.md` | Closed | **CLOSED** | Wording controls captured for the submission (Billi Principal-supplied install-only with $38,261 deducted from PC; fountain slabs by others; extinguishers EBC; backflow registration rides with excluded lodgement) |
| **Three separate mobilisations** dependent on builder structure windows (months 3/5/7/8 assumed) | Programme, prelims | Phase 7 | Assumed windows stated | H | M | H | **L** | Prelims (already 31% over pool) | Window slip = standing time or remobilisation | High | **HIGH** | Assumptions stated; D6-F4 prelims decision |
| **June-2024 cached rates now frozen literals** — ≥2 years old at a 2027 start | Material masters | Link severance | Frozen + tagged | H | H | **L** | H | ×1.38/×1.18 factors | Must not double-count escalation against already-loaded rates | High | **HIGH** | Phase 5 re-sourcing outstanding; per-rate safe-to-multiply flags recorded |
| **10% withheld until as-builts/O&M approved** (VOL 38 §4.4.1(3)) | Commercial | VOL 38 | Noted + qualified | H | H | H | M | — | Cash-flow on ~$200k | High | MED | Qualified in submission; RFI C14 |
| **12-month maintenance incl. AS1851 fire tagging** | Post-PC | VOL 38 §3.8/§12.13/§13.7 | Priced as a line | M | M | M | H | — | Under-allowance if attendance frequency is higher than assumed | Med | MED | Priced; basis stated |
| **Grease arrestor size** — 1500 L drawn / 2000 L in report / 550–5000 L unselected in spec | NBC trade waste | Three documents | Priced 1500 L as drawn | M | M | M | H | ×1.18 | Larger unit changes excavation, unit cost, connection | Med | MED | RFI C7 |

### 2.3 Both entities

| Risk | Source | Qty | Lab | Mat | Prog | Rating | Treatment |
|---|---|---|---|---|---|---|---|
| **RRC Addenda 1–6 never received** | Paynters/RRC streams | M | M | M | M | **HIGH** | Narrow qualification; acknowledgements for 7–10 returned; RFI A7 |
| **ITT §27 Appendix Folder (DA conditions) not accessible** | ITT §27 | M | M | M | M | MED | RFI A8; **Mitch to download** |
| **5-day combined weather + latent allowance** against a CQ wet season and a VFMP 6pm–6am curfew that removes evening float | ITT §20.h; VFMP | H | M | H | **L** | **HIGH** | Qualified; EOT relief relied on, no acceleration priced |
| **No site power or water** (ITT §17.3) | ITT | H | M | M | H | MED | Temp water cartage + gensets in each entity's own prelims (no sharing) |
| **Spoil must stay on site; site-won clay unsuitable for reuse** | Add 2, ITT §17.9, RPT006_B §4.3 | M | M | M | M | **HIGH** | RFI A4 on stockpile location/haul and imported-bedding acceptance |
| **VFMP constraints** — arborist supervision, water excavation in root zones, root guards near sewer lines, machinery curfew | Attachment 14 | M | **L** | H | **L** | MED | Productivity penalties applied in Phase 7; qualified |
| **CCTV + ADAC/RPEQ obligations split between two packages** | VOL 38 §3.56; ITT §19 | H | M | M | H | LOW | Each entity carries its own; RFI A6 confirms |

---

## 3. STANDING ASSUMPTIONS (each becomes a stated basis in the submissions)

1. Quantities: the ADOPTED column of `QUANTITY_RECONCILIATION.xlsx` is the sole pricing basis; Denis's originals are retained alongside, never overwritten.
2. Priced basis = T1 drawings **as modified by** Design Report SE_12306_RPT006_B Rev B §6.1/§9.1.
3. Structures priced from layouts + F1321 (141) rather than pit schedule F1310 (121).
4. Rock: geotech-inferable band in the lump sum; beyond that, the tendered extra-over rates on written direction.
5. Trench support: shields for personnel-entry runs; one geotechnical inspection attendance.
6. Escalation to 2027 applied **once**, only where the quote register's safe-to-multiply flag permits.
7. Labour: FIFO roster Example #3, ROK rates ×1.08; Leading Hand priced as **direct labour** per TriCore's own methodology.
8. Each entity fully standalone — no shared prelims, establishment, supervision, accommodation or plant recovery.
9. All sums ex-GST; 60-day validity; submission dated 24 July 2026; addressed to "Tenderer".

## 4. OPEN VERIFICATION ITEMS
28 quantity opens (owners: Denis 10 · RFI 11 · Phase 6 5 · Director 2) in `QUANTITY_RECONCILIATION.xlsx` sheet `Opens`; 11 material gaps in the quote register `Gaps` sheet; 30 tender queries in `RFI_SCHEDULE.md`. **The tender may not be marked complete while any Director-owned item above is unanswered.**
