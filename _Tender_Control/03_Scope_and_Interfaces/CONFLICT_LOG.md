# CONFLICT LOG — TEN16699, tender-run-01, 26 Jul 2026
Sources: 11 structured document notes in `01_Document_Register/notes/` (per-doc detail lives there) + Phase 0 addendum register + Phase 3 workbook audit. Disposition codes: **RFI** = raise with builder at tender (H002 n.15 + VOL38 §3.58 make this mandatory to preserve position — conflicts otherwise deemed priced at the larger quantity/more expensive component) · **QUAL** = qualification in submission · **PRICE** = resolve by pricing treatment · **INT** = internal register only.

## A. Contract & schedule (VOL 21 + Schedule 3)

| # | Conflict | Disposition |
|---|---|---|
| A1 | ITT §16 splits authority work: TPS lodges ALL plumbing applications with RRC + pays fees (reimbursed via Provisional Sums), but **Principal Contractor owns FRW Private Works Applications and water/sewer connection completion**. Refines the §5.3 locked exclusion — TPS wording must exclude FRW lodgement specifically, not "all approvals". | QUAL + Director note (already flagged §5.3) |
| A2 | Trade Waste never mentioned in VOL 21 despite kiosk/canteen; H002 n.25 + VOL38 make TPS responsible for the application. | RFI + PRICE (Excluded-But-Costed) |
| A3 | Schedule 3 workbook: 1A lump-sum `=SUM(F6:F131)` **omits Section 6.0 entirely**; both tabs' SUM ranges include section-Total rows AND line rows (double-count risk); $20k provisional sits in Qty column with empty price cell; 1A provisional total row outside SUM range. | RFI (how to enter prices + roll-up correction) |
| A4 | "WSUD Basin?" (1A R52) and "Rebound wall?" (1B R92) carry literal question marks; 1B Drainage has **no WSUD line** — stage allocation of filtration unclear. | RFI |
| A5 | §25 lump sum vs §18 remeasurable rock/unsuitable/over-depth/imported-fill rates payable **only with prior written Superintendent direction**; rock defined vs 20–30t excavator w/ ripper; notification at first encounter is a condition of entitlement. | QUAL (mirror the regime in our rate schedule wording) |
| A6 | §20.h allows only 5 days combined weather+latent programme allowance — unrealistic for CQ wet season, 2027 start. | QUAL (programme basis stated) |
| A7 | Schedule 3 file was re-saved locally 24 Jul 2026 by "Mitch - TPS" — price into a verified virgin copy of the issued original. | INT (Phase 8 handling) |
| A8 | 1B rate schedule lacks piling over-depth rate that 1A has; duplicate "Fencing" lines 1B R34/R36; 1B section 4.0 has no Total row. | RFI (minor, bundle) |

## B. VOL 38 spec — template contamination & commercial hooks

| # | Conflict | Disposition |
|---|---|---|
| B1 | **Two different sewer pump stations specified**: VOL38 §24 = 2× Sulzer ABS XFP 100E chopper, duty 10 L/s; H003/VOL17 = QMax Fortis 3200 ("or equally approved"); Addendum 2 = **Council installs the station**. Addendum (latest, highest precedence) governs → exclusion stands; cite all three in the interface ledger. | QUAL (exclusion wording cites Add 2) |
| B2 | NSW/VIC template leftovers throughout: EP&A Act, NSW Health, Building Professionals Board, "Fire and Rescue VIC" signage, VIC Legionella testing, Queanbeyan vendor, "Rockhampton City Council", swimming pool backwash, bio-septic, RO service under an "Extinguishers" heading, gas clauses with no gas scope, §12.15/§13.11 non-potable lilac hydrant system on a potable FRW job. | QUAL (one narrow clause: priced to QLD/RRC/FRW statutory framework; nominated-equipment schedule governs over template text) + RFI for the non-potable/hydrant contradiction |
| B3 | **10% of hydraulic contract value withheld until final as-builts/O&M approved** (§4.4.1(3)); 12-month maintenance of works incl. fire AS1851 tagging (§3.8/§12.13/§13.7). | PRICE (cashflow + maintenance line) + QUAL on terms |
| B4 | §3.58/H002 n.15: conflicts deemed priced at larger/more expensive unless raised at tender. | Drives the whole RFI schedule |
| B5 | §7.7/§7.11: rock and water-charged bedding **deemed included**; vs H002 n.24 extra-over rate regime; vs ITT §18 written-direction regime. Three inconsistent rock frameworks. | RFI + QUAL (state which regime we priced) |
| B6 | Grease arrestor Halgan 550–5000L **no size selected**; Design Report says 2000L "pending kitchen layouts"; H-NBC-102 shows 1500L Viking Paneltim GIT. Three sizes in three documents. | PRICE as PC/allowance + QUAL |
| B7 | Fire booster/DCDA equipment schedule referenced "at rear of specification" — absent; no hot water plant schedule anywhere despite pricing line. | RFI |
| B8 | §14.1 extinguishers: plumber prices supply/install, note says builder/sprinkler contractor generally provides; NBC drawings show 8×FE with no trade allocation. | RFI + Excluded-But-Costed |
| B9 | §9.22 joint sewer locate/re-lay/encase — template leftover on greenfield, but live obligation as written. | RFI (confirm N/A) |
| B10 | Material substitution only via HK Solutions form (§27) — constrains VE; relevant to HDPE main + copper-alternate positions: our §10.1-table-based HDPE offer is INSIDE the spec's own alternatives, not a substitution. | QUAL wording leverage |

## C. Hydraulic drawings (VOL 17 / 06 / 11)

| # | Conflict | Disposition |
|---|---|---|
| C1 | **H003 prints NO pipe lengths** and no legible hydrant/booster symbols; H300 has only 4 details. Fire service extent cannot be established from the site drawing — Denis's 218 m DN125 + 1 booster + 1 dual hydrant is not verifiable from H003 alone. | PRICE (Phase 4 scaled measurement) + RFI (hydrant coverage design intent vs AS2419) |
| C2 | H003 twice refers "FOR CONTINUATION REFER TO DRAWING H004" — **H004 not in H001 schedule, not supplied**. | RFI |
| C3 | H002 n.26 water main connection size left blank "........mm" while H003 shows Ø200 tapping. | RFI (confirm Ø200) |
| C4 | Rising main: H003 labels Ø100, QMax vendor sheets show DN110/DN160 PE; discharge "location to be confirmed and coordinated" with no tie-in to the Ø225 authority main shown. Interfaces around the Council-installed station are undefined. | RFI — critical to the §5.3 interface ledger |
| C5 | QMax sheets are generic Rev A "SAMPLE" vendor drawings (27.03.2024) though H001 lists them as T1; sample well ~6.7 m deep vs H003 SL/IL implying ~1.7 m. | INT (station excluded; note for interface depth) |
| C6 | H002 n.17 "COMPACTION SCHEDULE" is a verbatim duplicate of n.16 deliverables list — no compaction spec on drawings; VOL38 §3.62 tables conflict internally (95% Std vs 93–98% Mod MDD). | RFI (adopt 3.62 pending) |
| C7 | Seismic: restraint design by contractor, AS1170.4 EDC 2 (spec §3.15) — design obligation inside construct-only package; H002 n.9. | QUAL (install to specified system; restraint *layout drafting* only, no engineering design liability) + PRICE |
| C8 | NBC/PAM sheet defects: PAM-002 invokes **NT Building Regulations**; page numbering broken both sets; SD6 note missing both sets; DP count mismatches (PAM 4 roof vs 2 UG; NBC 11 vs 12 labels); undefined TR/DT labels; PAM meter has no PRV vs NBC 500 kPa; hose-tap backflow triple-inconsistency. | RFI (bundle) + PRICE conservative |
| C9 | **316 SS press-fit for ALL >DN22** (WS2) vs Denis priced copper with no stainless rate obtained. Locked decision §5.5: price BOTH (stainless conforming + copper labelled alternative). | PRICE (Phase 5 stainless rates needed) |
| C10 | 4× "DF" + 1× "BT" marks on H003 undefined in legend (presumed drinking fountains/bubbler tap) vs FF&E chilled/non-chilled CF400 confusion (VOL25 chilled, VOL28 "non-chilled", same SKU). | RFI + PC Sum (calculated, per §5.3) |
| C11 | Both building meter assemblies are CHECK meters — primary metering must exist in TPS site mains (H003 meter slab) — boundary alignment needed between building and site packages (both TPS, but schedule lines differ). | PRICE (matrix) |

## D. Civil drawings (VOL 15)

| # | Conflict | Disposition |
|---|---|---|
| D1 | Layouts show **141 drainage structures vs 121 in pit schedule F1310**: 20 C-series culvert end structures absent from F1310; 18 dimensioned on F1321; **C09A/C09B (twin 2×375 RCP, F1304) detailed nowhere**. Confirms Denis's "drawings show more than schedule" — adopted basis = layouts + F1321 + long sections. | RFI (C09 details + corrected F1310) + PRICE from drawings |
| D2 | F1310 internal defects: pit 87-02 listed twice with conflicting attributes; remarks/cover columns shifted one row for 5 pits; ref typos (12306_12320, F650). | RFI (bundle) + PRICE conservative reading |
| D3 | F1324 and F1325 titleblocks **both** read "Details Sheet 5" (content differs: WSUD filtration vs kerb outlet) — filename suspicion confirmed inside the documents. | RFI (minor) |
| D4 | Long-section sheet titles skip Sheet 13 (F1361=Sh12, F1362=Sh14) though drawing numbers are consecutive; no index sheet in set. | RFI (confirm no missing sheet) |
| D5 | Pit 81-07 missing from line-81 sequence on F1361 vs listed in F1310. | RFI |
| D6 | C09B IL higher than C09A (34.911 vs 34.825) — flow direction unclear; IL steps UP 0.467 m at 26-02 (presumed tank outlet control); printed capacity ratios >1.0 on lines 25/26/30/39 (design surcharge); segments with 0.0 L/s design flow. | INT (construct-only; record) + fold into D1 RFI |
| D7 | GT schedule F1320: GT2 "4 pits" doesn't reconcile with layouts (5 trash boxes + 7 connection pits); GT6 is Class D ductile iron vs Class B elsewhere. **GT1–GT9 total 608.5 m** trench drain + ~29 trash boxes (25×200 + 4×100). | PRICE (Phase 4 count) + RFI |
| D8 | Culvert cover: C01–C03, C05–C08 zero/negative cover; C10 ~0.11–0.15 m — load class/surface tie-in questions; only Line 25 exceeds 1.5 m depth (geotech inspection trigger); **no run exceeds 2.0 m** (batter trigger) — but tank structural excavation deeper and not shown. | PRICE + QUAL (rock/batter basis stated) |
| D9 | Court drainage material: Design Report §6.7 says PP + PVC-U DWV; long sections show PP collectors + PVC-U DWV laterals + RCP trunks; one run 375 **CL4** (line 05) among CL3. | PRICE (don't price all-RCP or all-CL3) |

## E. Design Report Rev B vs T1 civil set

| # | Conflict | Disposition |
|---|---|---|
| E1 | 100%DD changes (kerb chutes replace pit-and-pipe headwall outlets; type 2 strip filters; SE maintenance culvert; enlarged basin; swale headwalls/scour) **not reissued into T1 sheets**; report cites civil set Rev D2; no supersession statement. | QUAL (priced basis = T1 sheets as modified by RPT006_B §6.1/§9.1) + RFI |
| E2 | §7.1 "WSUD Key Changes: None" vs §7.4 raingarden→22-StormFilter swap vs §7.5 floating raingarden readoption — WSUD simultaneously settled and unsettled. | PC Sum treatment (§5.3) + QUAL supply basis, exclude maintenance beyond DLP |
| E3 | EDQ Conditions 16/17: 20-business-day review windows before stormwater commencement; lawful discharge is a creek on CQU land with **no land agreement**. | QUAL (programme gate; not our risk to solve) |
| E4 | Basin embankment stability assessment not undertaken; basin footprint grew at 100%DD; detention (RL29.70 spillway) not "retention". | QUAL (terminology + basis) |
| E5 | Geotech-in-report: site-won high-plasticity clay unsuitable for reuse without treatment; imported fill recommended; AS3798 Level 1 supervision — vs Add 2 "no spoil to leave site" and EMR §17.9 spoil retention. Spoil strategy = on-site stockpile of unsuitable + imported bedding/backfill. | PRICE (Phase 4/6 spoil & import quantities) + QUAL |

## F. Denis vs documents vs workbook

| # | Conflict | Disposition |
|---|---|---|
| F1 | Kerb chute: 17 Jul allowed rock+erosion mat (56 m²); 24 Jul email excludes kerb chute entirely as "not the work scope" — later email governs BUT locked decision §5.3 says "kerb chute concrete excluded (rock and erosion control mat only, per Denis)". **Director decision needed: 24-Jul full exclusion vs §5.3 rock+mat.** | Director (D6) |
| F2 | WSUD figure: Denis email $106,221.80 Atlan estimate vs workbook V1 W7 $88,838 cost (+15% = $102,163.70) — two different Atlan bases; both superseded by Ocean Protect nomination. | PRICE (Phase 5 re-quote Ocean Protect) |
| F3 | Fire 218 m DN125 + booster + dual hydrant, avg trench 0.9×0.45, pump station $545,700: present in workbook, **absent from Denis's emails** — provenance is the workbook only; all three flagged for independent verification (fire extent looks light; trench profile vs long-section depths OK — max 1.67 m). | PRICE (Phase 4) |
| F4 | Tradelink fixture quote 1066143/SP $252,694.77 ex GST, dated 15/07/26, **expires 13/08/26** vs 2027 commencement; header says "544 Yaamba Rd Parkhurst" vs site 554-700 Yaamba Rd Norman Gardens. Fixture quantities "not finalised" per Denis; FF&E schedules carry NO quantities and NO supply-responsibility statement for ~30 fixture types. | PRICE (Tradelink+15% PC per §5.3; escalation + validity QUAL; Phase 4 counts from layouts) + Director confirm supply split |
| F5 | Subsoil 100 mm 2,173 m excluded by Denis = matches locked §5.3 "by others"; but Design Report re-nominates subsoils as type 2 strip filters — the excluded thing changed shape. | QUAL wording: exclude subsoil/strip-filter system "by others", define interface at collector pits |

## G. Cross-cutting obligations priced nowhere yet (from notes; feed Phase 4/6/7)

- CCTV all in-ground drainage, independent approved firm, Superintendent present (VOL38 §3.56) — split TCS/TPS
- ADAC XML as-cons + RPEQ certification (ITT §19; Sch item 1.6 both stages) — both entities
- Temp potable water storage/distribution + generators (ITT §17.3) — both entities' prelims
- 12-month maintenance + AS1851 fire tagging (VOL38) — TPS
- 10% retention-until-as-builts (VOL38 §4.4.1(3)) — TPS cashflow/QUAL
- Third-party-witnessed testing, 1-hr static held to reinstatement, photo evidence (G4 notes) — TPS QA time
- Seismic EDC 2 restraints + scissor/EWP access (spec §3.15, H002 n.9) — TPS
- Articulation on H1/"P": swivel/expanda joints, combo joints, lagging, DP expansion ≤6 m (WS notes, RPT006 §14.3) — TPS
- In-blockwork conduiting for risers/droppers, no in-wall longitudinal runs (WS8/9) — TPS labour adder
- VFMP: AQF5 arborist supervision, water excavation in NRZs, root guards near sewer lines, 6pm–6am machinery curfew, FSC gate clearing — both entities near retained trees
- Electrical wiring pumps-to-panel is in the hydraulic subcontract (VOL38 §24.1.2) — TPS (matters for any pump we DO carry)
- Hydrant block plan approval BEFORE manufacture; FRQ final inspection 2-week notice (VOL38 §12.17/§25) — TPS programme
- Rock rate schedule MUST be tendered: extra-over soft AND hard, trenches AND pits (H002 n.24) — both entities

## H. Geotech (NQL2024-0320 Rev 0 — read 184/184, all §5.5 values verified)

| # | Conflict / delta | Disposition |
|---|---|---|
| H1 | Refusal is broader than the prompt's 11 locations: **25 of 36 test locations refused**, shallowest TP03 0.70 m; XW rock 0.2–2.2 m at 6 test pits. Rock exposure on shallow trenching is materially more likely than the 11-location list implies. | PRICE (rock allowance basis states "bore results available" per H002 n.24 — extent quantified in Phase 4 overlay) + rate schedule |
| H2 | §5.3.3 batter rule verified as 1.5H:1V for excavations **less than 2 m deep** (not only beyond 2 m). Read literally, every trench with personnel entry needs 1.5H:1V batters, 3H:1V/benching at perched water, or shoring — Denis's 0.45 m wide vertical-wall profile is non-conforming wherever workers enter. | PRICE (Director options: trench-shield allowance for entered runs vs batter widening; Phase 6/7 carries shields) + QUAL (basis stated) |
| H3 | Addendum 7 Q3 premise "collapsible sand indicated by the Geotech report" — the phrase/condition appears **nowhere** in NQL2024-0320. | INT (record; no action — screw-pile question isn't ours) |
| H4 | Design subgrade CBR 1.5%, swell to 7.5%; high-plasticity clays excluded from structural fill; **no survey levels for any test location** (borehole depths cannot be tied to design RLs precisely). | QUAL (refusal-vs-invert overlay is approximate — stated) |
| H5 | Gomersall Rd stockpile (Council fill source) not covered by this report; Add 1 said further testing "to follow" — never issued. | QUAL (imported/Council fill quality by others) |

**Master rule driving RFIs: H002 n.15 / VOL38 §3.58 — every ambiguity above that we don't RFI is deemed priced at the larger quantity / more expensive component. RFI schedule to be drafted in Phase 8 pack (08_Risks_Assumptions_Qualifications/RFI_SCHEDULE.md).**
