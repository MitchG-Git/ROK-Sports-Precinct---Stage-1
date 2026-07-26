# EQUIPMENT_TEST_TCS — Rule 4 fixture & equipment test (CALIBRATED RE-RUN)

**Tender:** TEN16699 Rockhampton Sports Precinct Stage 1A & 1B · **Entity:** TriCore Civil Services (TCS, civil stormwater)
**Model tested:** `Working_Cost_Models\TCS\ROK_TCS_CostModel_V2.xlsx` (loaded twice, `data_only=True` and `data_only=False`, all 11 sheets, every populated cell + note)
**Rule applied:** TENDER_PROMPT §2 Rule 4, third test — *"for every fixture, tapware item, bubbler, hot water unit, pump and piece of equipment, determine SEPARATELY: supply · delivery · storage · installation · fixings · accessories · connection · testing · controls · and whether it is builder-supplied or Principal-supplied. Never write 'fixtures included' when only installation or connection has been costed."* Applied here to TCS's civil/drainage proprietary-product and precast population, per TENDER_PROMPT §5.3 (In/Out) and the locked reinstatement instruction *"Denis also set aside the excavation and quarry for these — reinstate that too."*
**Supersedes:** an earlier uncalibrated run that returned 4 product groups. That run searched only category-level ("Hauraton GT", "precast pits") rather than individual product/designation level and consequently could not test the reinstatement claim against the actual materials block. This run itemises at designation level, as instructed.
**Read-only:** no cell in the model, submission, PDF, or any register was altered by this test.

**Result: 21 items tested (vs the prior run's 4; TPS's calibration benchmark was 14) · 11 COMPLETE · 9 GAP · 1 MISSING (deliberate, Rule-5-compliant zero).** The headline finding is that the Hauraton GT reinstatement is **real but partial**: channel supply, delivery, trash boxes, end caps and excavation labour are genuinely reinstated and priced; the **quarry/bedding material component that both the EBC register and `01_SCOPE_MATRIX.md` explicitly claim is priced is not actually present anywhere in the materials block.** See §5.

---

## 1. Method

Each item below is tested against the nine Rule 4 determinations — **Supply · Delivery · Storage · Installation · Fixings/accessories · Connection · Testing/commissioning · Controls · Supply ownership** — with a cell reference for every ✓. Verdict legend: **✓** priced, location shown · **N/A** determination does not apply to this product · **OTHERS** correctly excluded, another party's scope · **GAP** a real shortfall against a written claim or a reasonable expectation, evidenced · **MISSING** no cost exists to measure (Rule 2 — a valid, stated verdict, not an estimate).

Sheet abbreviations: **1A** = `Stage1A_Drainage` · **1B** = `Stage1B_Drainage` · **MM** = `Materials_Master` · **EM** = `Equip_Master` · **EBC** = `EBC` · **SM** = `_Tender_Control\03_Scope_and_Interfaces\01_SCOPE_MATRIX.md` · **QR** = `_Tender_Control\04_Quantity_Reconciliation\QUANTITY_RECONCILIATION.xlsx` (sheet `TCS_Civil`) · **QRN** = `QUOTE_REGISTER_NOTES.md`.

The population was built from: the two work-area sheets (materials A-block, labour B-block, plant C-block), `Materials_Master` (87 rate rows with source + escalation-decision column), `Equip_Master` (58 rows incl. the migrated-but-unused Civ reference block), `EBC` (Director-pending and excluded-but-costed items), `Sched3_Extract` (the GT Schedule-3 roll-up, tested as an independent cross-check of the same population), `QUANTITY_RECONCILIATION.xlsx` `TCS_Civil` sheet, and the narrative quantity-reconciliation notes (`groundplan_civil_sw.md`).

---

## 2. The test table

### 2.1 WSUD StormFilter — 22× Ocean Protect Tall (690) PSorb cartridges, DN3300 manhole

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ **PC SUM** | `TCS $ Sched` D27 = $90,064.63 (Reece Q-459014431, only project-specific price on file) |
| Delivery | ✓ **PC SUM** | `TCS $ Sched` D28 = $7,142.10 freight, separate line inside the PC base (D29) |
| Storage | GAP | No dedicated long-lead allowance. Only the generic `Prelim_OH` r9 "20 ft container / site storage" $900 total (6 mo × $150), itself flagged *"register weekly rates implausibly low"* — shared across the whole site, not sized for a precast DN3300 manhole/false-floor assembly |
| Installation | ✓ | 1A **C-05** *"WSUD DN3300 manhole install + 22 StormFilter cartridges (supply = PC Sum)"* — 8 crew-days, priced in the **base lump sum, not the PC** (locked 5.3; `EBC` H31 confirms) |
| Fixings/accessories | **GAP** | The only comparable-project OP install documents on file (`Material\...\Anaconda_Material`, register refs C05–C11) state false floor, sealant, cranage and anti-flotation are **"by others"** in that scope. The Reece PC line here has **"no spec/drawing basis stated"** (Register Gap #1) and C-05's description does not name a false floor, anti-flotation collar or sealant allowance. Cannot confirm these accessories are inside either the PC or the base labour — genuine gap, not an assumption either way |
| Connection | ✓ | Bypass/backfill/connection named inside C-05's install scope; `EBC` H31 confirms connection is in the base lump sum |
| Testing/commissioning | **GAP** | No line anywhere names WSUD commissioning, cartridge fit-out inspection or first-flush/flow certification. 1A **A-09** "Testing + CCTV attendance" is a pipe-CCTV activity, not a filter-system commissioning activity. Register Gap #1 explicitly flags *"interrogate what the Reece line includes (cartridges? false floor? install?) before adoption"* — the scope of what's actually inside the $90,064.63 figure is unverified |
| Controls | N/A | Passive filtration system — no controls |
| Supply ownership | **TCS** | Confirmed TCS, not Principal-supplied — SM row L3: *"Entirely TCS — supply + delivery of the 22 StormFilter cartridges/internals as PC Sum +15%, installation, bypass, connections and backfill inside the TCS lump sum; TPS has no scope at this structure."* No other GPT/treatment device exists in scope — the old Atlan package (38× Stormsack pit inserts + 10× FIL-3.0 + 14.9 kL detention tank, quote P02) was an **entirely superseded alternate WSUD design**, correctly dropped, not silently folded in (`EBC` B32/F32 "SUPERSEDED — PC"; Design Report §7.4 confirms current treatment train is swale + StormFilter only, no raingarden, no separate GPT) |

**Verdict: GAP.** Supply/delivery/installation/connection/ownership are sound. Storage is thin (shared, not sized) and, more materially, **commissioning and the false-floor/anti-flotation accessory scope are unconfirmed** — a live Rule 4 exposure on the single largest proprietary item in the model.

---

### 2.2 Grated trench GT1–GT4 — Hauraton Recyfix PRO200 T010 Fibretec B125 (1A `G1`, 548.8 m)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `G1` 548.8 m @ $321.4572 = $176,415.71 (MM `M48`, Reece Q-459014445 lines 21–28, ×1.38 PE family) |
| Delivery | ✓ | 1A `D2` "Freight — Reece (Hauraton + PP + winged headwalls)" 11 loads @ $1,133.16 = $12,464.76 |
| Storage | GAP | Same generic $900 site container line only — no channel-specific allowance |
| Installation (excavation + set) | ✓ | 1A `C-06` "Grated trench drains GT1-GT4 + GT7-GT9 (561.9 m)" 23 crew-days = $65,835.80 |
| Fixings/accessories — **bedding/quarry material for the channel run itself** | **GAP — see §5** | 1A `Q1` bedding-stone formula `=ROUND(0.203*(C6+C8+C10+C11+C12+C13+C14+C16+C17+C18),0)` sums **only the pipe-line rows (P1,P3,P5–P9,P11–P13)**. `C54` (this row, GT1-4) is **not** in that sum. No other materials row carries GT bedding/haunch/surround. Yet `EBC` B27 states GT was *"REINSTATED... including excavation & quarry"* and `01_SCOPE_MATRIX.md` row L1 states TCS prices *"GT1–GT4, GT7–GT9, trash boxes, connection pits, excavation and quarry"* — both assert quarry is priced; it is not |
| Connection | ✓ | To trash boxes/end caps within `C-06`'s crew-day scope |
| Testing/commissioning | N/A | Gravity surface channel — no CCTV/pressure test applicable, correctly not claimed |
| Controls | N/A | Passive |
| Supply ownership | **TCS** | SM row L1; locked 5.1 corollary (Sch 1A 3.5 "Hydraulic" heading does not move it to TPS) |

**Verdict: GAP** (bedding/quarry material — see §5 for the full reasoning and the Hauraton GT calibrated verdict).

---

### 2.3 Grated trench GT7–GT9 — Hauraton Recyfix PRO100 T010 SS heelguard (1A `G2`, 13.1 m)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `G2` 13.1 m @ $508.1712 = $6,657.04 (MM `M49`, Reece Q-459014445) |
| Delivery | ✓ | Same 1A `D2` Reece freight lot as 2.2 |
| Storage | GAP | As 2.2 |
| Installation | ✓ | Same 1A `C-06` crew-days (combined 561.9 m activity with GT1-4) |
| Fixings/accessories (bedding/quarry) | **GAP** | Same `Q1` formula exclusion as 2.2 — this run's metres are also absent from the bedding-stone sum |
| Connection | ✓ | Within `C-06` scope |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | SM L1 |

**Verdict: GAP** (same quarry-material shortfall as 2.2).

---

### 2.4 Grated trench GT5 — Hauraton Recyfix PRO100 T010 SS heelguard (1B `G1`, 15.2 m)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1B `G1` 15.2 m @ $508.1712 = $7,724.20 (MM `M49`) |
| Delivery | ✓ | 1B `D1` "Freight — Reece (GT5/GT6/TB100)" 1 load @ $1,133.16 |
| Storage | GAP | As 2.2 (site-wide, not stage-specific) |
| Installation | ✓ | 1B `C-08` "GT5 + GT6 trench drains 46.6 m" 3 crew-days = $8,587.28 |
| Fixings/accessories (bedding/quarry) | **GAP** | 1B `Q1` formula `=ROUND(0.203*C6,1)` where `C6` is the 150 PVC DWV line (29.6 m) **only** — GT5's 15.2 m is not included. No quarry line anywhere for GT5 |
| Connection | ✓ | Within `C-08` scope |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | SM L10 — stage split per VOL 20 hatch (RFI to confirm boundary, but entity is TCS either way) |

**Verdict: GAP** (quarry material).

---

### 2.5 Grated trench GT6 — Hauraton Recyfix PRO200 G-tec D400 ductile (1B `G2`, 31.4 m) — **specification substitution flag**

| Component | Status | Where priced |
|---|---|---|
| Supply | **GAP — spec mismatch, not just quarry** | 1B `G2` priced at MM `M50` PRO200 G-tec D400 $387.6282/m, but the note on the same row and `TCS_CHANGE_LOG.md` §5.6/§7 both record: **the drawing schedule specifies PRO100 D400 G-tec code 47245; Reece's quote offers PRO200 G-tec (32 m) instead** — a different channel width class than specified. Register Gap #7 is open: *"exact item absent from Reece quote... Confirm equivalence or re-quote."* This is a live, unresolved product-substitution question, not a closed item |
| Delivery | ✓ | 1B `D1` Reece freight lot (shared with GT5/TB100) |
| Storage | GAP | As 2.2 |
| Installation | ✓ | 1B `C-08` (combined with GT5, 46.6 m, 3 crew-days) |
| Fixings/accessories (bedding/quarry) | **GAP** | Same 1B `Q1` exclusion — GT6's 31.4 m is not in the bedding-stone formula either |
| Connection | ✓ | Within `C-08` |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | SM L10 |

**Verdict: GAP (two separate gaps: unresolved spec substitution + quarry material).** GT6 is the weakest single line in the whole GT population — it carries both the substitution risk and the bedding-material absence.

---

### 2.6 Hauraton trash boxes — TB200 × 25 (1A) + TB100 × 4 (1B)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `G3` 25 × $738.7002 = $18,467.50 (MM `M51`); 1B `G3` 4 × $295.4856 = $1,181.94 (MM `M52`) |
| Delivery | ✓ | Inside the same Reece freight lots as the channels (1A `D2`, 1B `D1`) |
| Storage | GAP | As 2.2, generic only |
| Installation | ✓ | 1A `C-07` "Trash Box 200 x25 + 150 DWV laterals (grades to 29.2%)" 13 crew-days = $37,211.54; 1B `C-09` "1B lines 60/61/83 + TB100 x4 + connections" 4 crew-days = $11,449.70 |
| Fixings/accessories | ✓ | Mud bucket + Fibretec grate integral to the MM `M51`/`M52` supply rate (Reece SKU description: *"trash box... c/w galv mud bucket + Fibretec grate"* / *"...PE mud bucket + Fibretec grate"*) — accessories are inside supply, correctly not double-counted |
| Connection | ✓ | 150 PVC DWV laterals P12 (1A, 33.25 m) and lines 60/61/83 (1B) connect the boxes to pits/pipes, both priced |
| Testing | N/A | Gravity structure |
| Controls | N/A | |
| Supply ownership | **TCS** | QR row 66/67 confirms schedule count (25 + 4) reconciles exactly to F1310 |

**Verdict: COMPLETE.** This is the one part of the GT population where the classic Rule 4 accessory trap does **not** materialise — mud bucket and grate are correctly bundled in the per-unit supply rate, and install labour is a named, separate activity in both stages.

---

### 2.7 GT end caps — PRO200 × 8 (1A `G4`) + PRO100 × 10 (1A `G5`) + PRO100 × 4 (1B `G4`)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `G4` 8 × $32.4714 (MM `M53`, "c/w DN100 PVC outlet") + 1A `G5` 10 × $12.9858 (MM `M54`, "closed... 200 deep") + 1B `G4` 4 × $12.9858 |
| Delivery | ✓ | Inside the Reece freight lots |
| Storage | N/A | Negligible small-goods item |
| Installation | ✓ | Bundled inside `C-06`/`C-08` GT installation crew-days (end caps are fitted as part of channel assembly, not a separate labour activity — standard practice, not a gap) |
| Fixings/accessories — **locking devices** | GAP (minor, evidence-limited) | No document on file (no Hauraton install guide, no spec extract) confirms whether locking bars/bolts are required over and above the standard T010 grate assembly for this pedestrian (B125) / vehicle (D400) grade mix in a public precinct. Not costed as a separate line, and not confirmed as bundled — cannot determine either way from evidence on file (Rule 2: MISSING confirmation, not a defect) |
| Connection | ✓ | PRO200 end cap explicitly "c/w DN100 PVC outlet" — the outlet stub is priced in the unit rate |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | |

**Verdict: GAP (minor)** — the locking-device question is unresolved by any document on file, correctly not guessed either way.

---

### 2.8 Road gully inlets (RGU) — on-grade × 28 + sag × 5, CMDG-D-020

| Component | Status | Where priced |
|---|---|---|
| Supply | **GAP — sourcing** | 1A `S1`/`S2` 33 × $1,350 (MM `M39`). MM column I states explicitly: *"Old Civ workbook allowance (benchmark — NO current RGU quote: sourcing gap)"* — this is a self-flagged, unresolved rate with zero current-quote backing anywhere in the 41-document register |
| Delivery | GAP (unconfirmed) | No named freight line covers RGU specifically (D1–D6 name Humes/Reece/Tradelink/Jaybro/rock/"remaining materials" — RGU is not a Humes, Reece or Jaybro product per the register, so it likely falls inside `D6` "remaining materials" catch-all $3,000 lot, but this is inferred, not stated) |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `B-01` "RGU inlets x33 install" 22 crew-days = $62,973.37 |
| Fixings/accessories — **lintel/grate** | GAP (evidence-limited) | The MM `M39` description reads *"RGU inlet unit 2.4 m lintel (CMDG-D-020) supply set"* — unlike the 600×600 field inlets (which carry separate body **and** grate&frame lines, `S9`+`S10`/MM `M46`+`M47`), the RGU line does not separate a grate/frame component. Cannot confirm from the CMDG-D-020 standard detail (not on file) whether the "supply set" wording already includes the grate, or whether a grate/frame needs to be added the way it was for the 600×600 pits |
| Connection | ✓ | Within `B-01` install scope (pipe stub-ins to RGU per F1310) |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | |

**Verdict: GAP.** RGU is the weakest-sourced supply rate in the entire model (self-flagged benchmark, no quote) and carries an unresolved grate-bundling question — a genuine accessory-completeness risk on a 33-unit population.

---

### 2.9 Precast access chambers — 1050 mm × 13 (CMDG-D-030)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `S3` 13 × $364 (MM `M40`, "Humes-era benchmark") + `S4` Aspro cover slab 13 × $400 (MM `M41`) |
| Delivery | ✓ | 1A `D1` Humes freight (35 loads, includes precast) |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `B-02` "1050 access chambers x13" 13 crew-days = $37,211.54 |
| Fixings/accessories — grate/frame | ✓ | `S8` "Grate & frame 600x900 Class D" 17 EA @ $298 (MM `M45`) covers chamber covers across the 1050+1200 chamber population (13+4=17, exact reconciliation) |
| Connection | ✓ | Pipe stub-ins within `B-02` |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | |

**Verdict: COMPLETE.**

---

### 2.10 Precast access chambers — 1200×900 × 3 + 1200×1200 × 1 (25-03/26-02/26-03/26-05)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `S5` 3 × $1,101 (MM `M42`) + `S6` 1 × $1,403 (MM `M43`, 26-02's 0.467 m internal upstand) + `S7` Aspro cover slabs 4 × $400 (MM `M44`) |
| Delivery | ✓ | 1A `D1` Humes freight |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `B-03` "1200 access chambers x4 incl 26-02 upstand formwork" 6 crew-days = $17,174.56 — upstand formwork explicitly named, not silently assumed |
| Fixings/accessories | ✓ | Covered by the shared `S8` grate & frame line (17 EA total across both chamber sizes) |
| Connection | ✓ | Within `B-03` |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | QR row 62 — schedule governs at 4 total (Denis's 3 → Opens #4, adopted qty is correct at 4) |

**Verdict: COMPLETE.**

---

### 2.11 600×600 field inlet pits, Type 2 × 3 (81-02, 81-07, 87-02)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `S9` 3 × $229.50 (MM `M46`, Tradelink 1065005 R1) + `S10` grate&frame 3 × $365.20 (MM `M47`) — **body and grate priced as separate lines**, the correct pattern this product category should follow |
| Delivery | ✓ | 1A `D3` Tradelink freight lot |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `B-04` "600x600 field inlets x3" 2 crew-days = $5,724.85 |
| Fixings/accessories | ✓ | Grate & frame is its own priced line (`S10`) |
| Connection | ✓ | Within `B-04` |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | QR row 63 notes an unresolved chainage label discrepancy (81-08 vs 81-07, Opens #9) — a documentation defect, not a pricing gap |

**Verdict: COMPLETE.**

---

### 2.12 RCP 375 CL3+CL4 mainline (714.9 m incl. C09 twin barrels)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `P1` 714.9 m @ $105 (MM `M01`, Humes Q21642316 REV2) |
| Delivery | ✓ | 1A `D1` Humes freight, 35 loads @ $852 |
| Storage | GAP | Generic only; Humes's own terms flag *"pricing subject to Mould availability at the time of order"* — a real precast lead-time risk with no dedicated allowance |
| Installation | ✓ | 1A `A-03` "RCP375 CL3 mainline incl C09 twin barrels (45 m/day, flat-grade laser penalty)" 16 crew-days + `A-04` CL4 short runs 1 crew-day |
| Fixings/accessories (rubber rings) | ✓ | 1A `P2` "375 rubber rings (1 per 2.44 m length)" — formula-driven `=ROUNDUP(C6/2.44,0)` = 293 @ $4.80 (MM `M02`) — this is the exact defect (D7 in the change log) that was fixed in the V1→V2 rebuild; verified still correct in V2 |
| Connection | ✓ | Pipe-to-pipe/pipe-to-culvert allowance `F8` (MM `M20`, 20 EA @ $310) covers scheduled P2P connections |
| Testing/commissioning | ✓ | CCTV metre-count in `Prelim_OH` `C24` explicitly sums this pipe run (`Stage1A_Drainage!C6` is in the formula) @ MM `M72` $5.75/m |
| Controls | N/A | |
| Supply ownership | **TCS** | Take-off discrepancy (Humes 299 vs Reece 262 lengths) noted and adopted-length governs (MM `I11`) |

**Verdict: COMPLETE.**

---

### 2.13 RCP 600 CL3 stub (3.31 m, line 26)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `P3` 3.31 m @ $183.5656 (MM `M03`) |
| Delivery | ✓ | 1A `D1` Humes freight |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `A-04` "RCP375 CL4 + RCP600 short runs" 1 crew-day |
| Fixings (rubber rings) | ✓ | 1A `P4` 2 EA @ $24 (MM `M04`, allowance) |
| Connection | ✓ | Within `F8` allowance / `A-04` |
| Testing | ✓ | Included in the CCTV metre-count formula (`Stage1A_Drainage!C8` is in the `Prelim_OH` C24 sum) |
| Controls | N/A | |
| Supply ownership | **TCS** | |

**Verdict: COMPLETE.**

---

### 2.14 RCBC crowns — 6 sizes (600×300 / 750×300 / 900×450 / 1200×600 / LBC 1500×600 / LBC 2700×1200), `C1`–`C6`

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `C1`–`C6`, all sourced Humes Q21642316 REV2 (MM `M22`–`M27`), each with an explicit Reece-price comparison recorded and Humes adopted as cheaper on every size |
| Delivery | ✓ | 1A `D1` Humes freight |
| Storage | GAP | Generic only; the 2700×1200 (C10 basin outlet) is explicitly called "heavy lift" (`C6` note) with no dedicated laydown/handling allowance beyond the crane plant line |
| Installation | ✓ | 1A `C-01` (C10 2700×1200, crane set + shields, 6 cd) · `C-02` (small culverts 600×300/750×300/900×450, 9 cd) · `C-03` (1200×600 + 1500×600, 8 cd) |
| Fixings/accessories (extra-over bedding at zero/negative cover headwalls) | ✓ | 1A `Q2` "Bedding stone — culvert extra-over (0.4 T/m × 130.76 m RCBC)" 52 T @ $62 = $3,224 — **this is exactly the bedding-material line the GT population is missing** (see §5); its presence here for RCBC confirms the modeller knows to price channel/culvert bedding separately and simply never built the equivalent GT row |
| Connection | ✓ | Culvert-to-headwall connection within the culvert install activities |
| Testing | N/A | Box culverts are man-enterable / visually inspected, not CCTV'd — correctly excluded from the CCTV metre formula |
| Controls | N/A | |
| Supply ownership | **TCS** | Humes-vs-Reece take-off discrepancy (LBC1500×600 13 vs 8 lengths) noted, adopted 29.04 m governs (MM `M26`) |

**Verdict: COMPLETE.**

---

### 2.15 Small pipe headwalls — RCP375 / twin-375 / 150 PVC / 225 PVC / 300 PP (`H1`–`H5`)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `H1` 5×$317.05 (Reece, MM `M28`) · `H2` 2×$588.80 (Humes, MM `M29`) · `H3` 1×$158 (Jaybro, MM `M30`) · `H4` 1×$280 (Jaybro, MM `M31`) · `H5` 1×$352 (Jaybro, MM `M32`) — supplier selected per lowest compliant rate, each source stated |
| Delivery | ✓ | 1A `D2` (Reece 375 headwall) / `D1` (Humes twin-375) / `D4` "Freight — Jaybro headwalls lot" $1,500 (Jaybro's own terms state *"No allowance for freight"* — the D4 adder exists precisely to cover that gap; correctly not double-counted per the Register's double-count trap table) |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `B-06` "Pipe headwalls x10" 10 crew-days = $28,624.26 |
| Fixings/accessories | ✓ | Wingwall/beaching interface named in `C-04` (see 2.18) where headwalls meet rock protection |
| Connection | ✓ | Within `B-06` |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | QR row shows the 225 PVC headwall count (2 measured vs 1 schedule) — adopted qty 1 per F1310 schedule, a resolved quantity question, not a sourcing gap |

**Verdict: COMPLETE.**

---

### 2.16 Box-culvert (BCC) headwalls — 600×300 through 2700×1200, `H6`–`H11` — **supply-ownership test**

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ — **and this is the determination-9 test named in the brief** | Jaybro's own email states verbatim *"We don't do rcbc box culvert headwalls sorry"* (QRN P06) — Jaybro **declined** to supply any RCBC headwall. The model correctly does **not** rely on Jaybro for `H6`–`H11`: all six sizes are sourced Humes Q21642316 REV2 (MM `M33`–`M38`), with the Jaybro decline recorded in the rate note itself (*"Jaybro declined all RCBC headwalls"*, MM `M33` col E) |
| Delivery | ✓ | 1A `D1` Humes freight (same 35-load lot) |
| Storage | GAP | Generic only |
| Installation | ✓ | 1A `C-04` "Culvert headwalls x20 incl wingwalls + beaching interface" 16 crew-days = $45,798.82 |
| Fixings/accessories (wingwalls + beaching interface) | ✓ | Named explicitly in `C-04`'s description, and priced separately at `R1` rock beaching (see 2.18) |
| Connection | ✓ | Within `C-04` |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS — confirmed, no Principal-supply and no Jaybro-supply exposure** | This is the one determination-9 question the brief specifically flagged, and the model passes it: supply was correctly re-routed to Humes the moment Jaybro declined, and that re-routing is traceable in the rate note, not silent |

**Verdict: COMPLETE.** No gap — the Phase 5 Jaybro-decline is correctly resolved, not a live exposure.

---

### 2.17 Subsoil / strip-filter drainage — 2,172.4 m (excluded) + 283.71 m 100 PVC outlet stubs (included)

| Component | Status | Where priced |
|---|---|---|
| Supply (subsoil pipe system, 2,172.4 m) | **OTHERS** | Correctly excluded "by others" per locked §5.3 / SM rows 2.3-x2, 2.5-x3, `EBC` B28. QR row 22 confirms the 2,172.4 m measured total and the exclusion basis (no independent schedule exists to reconcile against) |
| Supply (outlet stubs / DP laterals, 283.71 m) | ✓ | 1A `P13` 283.71 m @ $9.9061 (MM `M12`) — this is the TCS-scope interface component |
| Delivery | ✓ | Inside 1A `D3` Tradelink freight lot (100 PVC is a Tradelink item) |
| Storage | N/A | Small-bore PVC, no special storage |
| Installation | ✓ | 1A `A-07` "100 PVC DWV subsoil outlets / DP laterals" 4 crew-days = $11,449.70 |
| Fixings/accessories | ✓ | Bends (`F1`,`F2`) and junctions (`F4`) include 100 PVC sizes in their EA counts |
| Connection — **interface definition** | ✓ | SM row L12 states explicitly: *"TCS accepts strip-filter/subsoil connections only at TCS collector pits; the strip-filter system itself... is by others — connection point = the pit wall penetration."* This is exactly the interface-definition discipline Rule 4 requires for an excluded system with an included stub |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **OTHERS (system) / TCS (stub only)** | Correctly split and stated, not blanket-excluded or blanket-included |

**Verdict: COMPLETE** (as a scope-boundary item — the exclusion and the interface are both explicit and consistent across `EBC`, `01_SCOPE_MATRIX.md` and the workbook; no silent zero).

---

### 2.18 Rock beaching / erosion protection (headwalls + basin), `R1`–`R3`

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | 1A `R1` 25.344 m³ @ $110 (culvert headwalls D50=200) · `R2` 32.3208 m³ @ $120 (d50=100) · `R3` 236.997 m³ @ $110 (C10 basin D50=500) — all MM `M63`/`M64` |
| Delivery | ✓ | 1A `D5` "Freight — rock cartage" $5,700 lot |
| Storage | N/A | Delivered direct to placement location, no special storage need |
| Installation | ✓ | 1A `B-08` "Rock pads / beaching 513 m²" 9 crew-days = $25,761.83 |
| Fixings/accessories | N/A | Loose rock placement, no fixings |
| Connection | N/A | |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS** | |

**Verdict: COMPLETE.**

---

### 2.19 Kerb chutes × 9 — **Director decision D6-F1, both positions carried**

| Component | Status | Where priced |
|---|---|---|
| Supply (base) | **$0 — deliberate** | 1A base carries $0 per Denis's 24-Jul email exclusion (`EBC` B6) |
| Supply (add-price) | ✓ (held on EBC only) | `EBC` B8 concrete invert/kerb returns/R1000 9×$850 (MM `M79`) + B9 rock 10.02 m³ @ $150 (MM `M81`) + B10 matting 56 m² @ $7 (MM `M80`) |
| Delivery | ✓ (in add-price) | Rolled into the EBC materials subtotal, ×1.18 contingency (`EBC` F11) |
| Storage | N/A | |
| Installation (add-price) | ✓ (held on EBC only) | `EBC` B12 "Labour B-09 — 9 crew-days" = $25,761.83; B13 plant 9 days 3-5T excavator |
| Fixings/accessories | ✓ (in add-price) | Erosion matting is its own line |
| Connection | N/A | |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS (if reinstated)** | `EBC` F14 = $55,429.90 fully computed sell, with an explicit reinstatement instruction (G14): *"add labour row B-09... add the three material rows... add 9 plant-days"* — genuinely one-cell-set away from being live |

**Verdict: GAP — Director-pending, Rule-5-compliant.** This is **not** a Rule 4 failure: the base correctly carries $0, the exclusion is external and qualified (SM 2.3-x1), and a complete, re-priced (not stale-benchmark) add-price sits ready on `EBC`. Flagged here only because the submission wording must not silently say "kerb chutes included" — see §6.

---

### 2.20 Detention basin earthworks + concrete spillway — **NOT PRICED**

| Component | Status | Where priced |
|---|---|---|
| Supply (spillway concrete/mesh/sub-base) | **MISSING (base) / held on EBC** | 1A `X1` = $0 explicit flagged row; `EBC` B18–B20 gives the full spillway concrete (10.3 m³ 25 MPa), mesh (12 sheets) and sub-base (13 T) build-up |
| Delivery | N/A (base) / in EBC subtotal | |
| Storage | N/A | |
| Installation | **MISSING (base) / held on EBC** | 1A `B-07` "Concrete spillway weir 50 m — HELD AT 0 (allocation RFI pending; 10 cd on EBC sheet)" |
| Fixings/accessories | N/A (base) / in EBC | |
| Connection | N/A | |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **UNRESOLVED — Opens #26 + Director** | Basin **bulk earthworks** (as distinct from the spillway) is not quantified in *any* drawing (F1305 annotation only) — `EBC` B17 states this cannot be priced at all, not even as an add-price, because no quantity exists to price against |

**Verdict: MISSING — correctly stated, not guessed.** This is the one item in the whole population where Rule 2's *"a flagged gap is a success"* applies literally: the spillway (a quantifiable structure) has a full add-price ready on EBC; the basin bulk-shaping (an unquantified drawing annotation) has **no number anywhere**, and none was invented.

---

### 2.21 Big-lift plant allowances — 50t mobile crane, Franna, trench shields

| Component | Status | Where priced |
|---|---|---|
| Supply (hire) | ✓ (rate) | EM `D16` $3,800/day (50t crane) · `D17` $2,200/day (Franna) · `D18` $120/day (trench shields) |
| Delivery/mobilisation | **GAP** | EM column F flags all three: *"N — FLAG: NOT IN HIRE REGISTERS"* / *"ALLOWANCE — quote at award."* No separate mob/demob fee line exists for trucking a 50t crane or Franna to a Rockhampton FIFO site — day rate only |
| Storage | N/A | Hired, not stored |
| Installation (the crane/Franna's own use) | ✓ | 1A `C-01` (C10 2700×1200 crane set), `C-05` (WSUD DN3300), `C-03`/`B-06` (culvert crown/headwall sets) all draw plant-days from these EM rates |
| Fixings/accessories | N/A | |
| Connection | N/A | |
| Testing | N/A | |
| Controls | N/A | |
| Supply ownership | **TCS (hired plant, not Principal)** | Correctly flagged as an allowance pending quote at award (Cover_Control assumption #19) — an acknowledged, non-silent gap |

**Verdict: GAP — acknowledged, not closable now.** Consistent Rule 2 treatment: flagged, not estimated further, quote-at-award condition stated in three places (EM, Cover_Control, TCS_CHANGE_LOG).

---

## 3. Findings summary

| # | Item | Verdict | Nature of gap (if any) |
|---|---|---|---|
| 1 | WSUD StormFilter 22-cart DN3300 | **GAP** | Storage thin; commissioning + false-floor/anti-flotation accessory scope unconfirmed |
| 2 | GT1–GT4 PRO200 Fibretec | **GAP** | Quarry/bedding material absent despite reinstatement claim |
| 3 | GT7–GT9 PRO100 SS heelguard | **GAP** | Same quarry-material absence |
| 4 | GT5 PRO100 SS heelguard | **GAP** | Same quarry-material absence |
| 5 | GT6 PRO200 G-tec D400 ductile | **GAP** | Quarry-material absence **+** unresolved spec substitution (Gap #7) |
| 6 | Trash boxes TB200×25 / TB100×4 | **COMPLETE** | — |
| 7 | GT end caps PRO200×8 / PRO100×14 | **GAP (minor)** | Locking-device requirement undetermined from evidence |
| 8 | RGU inlets ×33 | **GAP** | Supply rate self-flagged as unsourced benchmark; grate-bundling unconfirmed |
| 9 | 1050 mm chambers ×13 | **COMPLETE** | — |
| 10 | 1200×900/1200×1200 chambers ×4 | **COMPLETE** | — |
| 11 | 600×600 field inlets ×3 | **COMPLETE** | — |
| 12 | RCP375 CL3+CL4 (714.9 m) | **COMPLETE** | — |
| 13 | RCP600 CL3 stub (3.31 m) | **COMPLETE** | — |
| 14 | RCBC crowns, 6 sizes | **COMPLETE** | — |
| 15 | Small pipe headwalls H1–H5 | **COMPLETE** | — |
| 16 | BCC headwalls H6–H11 | **COMPLETE** | Determination-9 test passes — Jaybro decline correctly re-routed to Humes |
| 17 | Subsoil system + outlet stubs | **COMPLETE** | Exclusion + interface both explicit |
| 18 | Rock beaching R1–R3 | **COMPLETE** | — |
| 19 | Kerb chutes ×9 | **GAP (Director-pending, Rule-5-compliant)** | Base $0 correct; wording control required |
| 20 | Detention basin + spillway | **MISSING (deliberate, Rule-5-compliant)** | Spillway costed on EBC; basin bulk earthworks genuinely unquantifiable |
| 21 | Big-lift plant allowances | **GAP (acknowledged)** | Mob/demob not in any hire register; quote-at-award |

**11 COMPLETE · 9 GAP · 1 MISSING.** Zero items were silently assumed complete without a cell reference, and zero items were silently zeroed without a register entry.

---

## 4. Gaps found — closable now vs needing RFI/Director call

| Gap | Closable from existing evidence? | Action |
|---|---|---|
| **GT quarry/bedding material (items 2–5)** | **Partially.** The bedding-stone *rate* ($62/T, MM `M62`) and the *factor convention* (0.203 T/m, used for every piped line) already exist in the model. Applying the same factor to the 608.5 m of GT length gives a **calculable exposure estimate of ≈$7,626 pre-contingency / ≈$9,001 contingent / ≈$12,736 at sell** (561.9 m × 0.203 T/m × $62 = $7,068 in 1A; 46.6 m × 0.203 T/m × $62 = $558 in 1B). **But** no Hauraton install guide, manufacturer detail or drawing note exists anywhere in the repository (confirmed — no file matching "Hauraton" or "Recyfix" exists outside the register/model) to confirm whether the channel requires granular bedding stone at all, or a concrete haunch/surround instead (the more common manufacturer detail for trafficked-grade drainage channels). **This is a genuine Rule 2 "cannot determine" — do not silently adopt the pipe-bedding factor for a surface channel product.** RFI action: confirm the Hauraton installation detail (bedding vs concrete surround) before pricing; hold the $12,736 figure only as an indicative exposure range, not an adopted cost |
| **WSUD commissioning + false-floor/anti-flotation** | Not closable from evidence on file. Register Gap #1 already calls for a direct Ocean Protect re-quote (needs the MUSIC model). Add to that RFI: confirm whether the $90,064.63 + $7,142.10 Reece line includes false floor, sealant, anti-flotation and commissioning, or whether these sit in the base install labour (`C-05`) and simply weren't named in its description |
| **GT6 spec substitution (PRO100 D400 vs PRO200 G-tec offered)** | Already an open register item (Gap #7). Not closable without a Reece confirmation or re-quote |
| **RGU inlet supply rate + grate bundling** | Not closable — self-flagged benchmark with zero current quotes anywhere in the 41-document register. RFQ action already implied by the existing flag; add the grate-bundling question to the same RFQ |
| **GT end-cap locking devices** | Not closable — no document addresses it. Low materiality (small-goods item); note as a stated assumption-pending item, not worth a standalone RFI unless the Superintendent raises vandalism/security requirements |
| **Storage/long-lead allowance (WSUD, RCP/RCBC precast, GT channel)** | **Director call, not an RFI.** The $900 total site-container line is thin relative to Humes's own stated mould-availability risk and the WSUD's long-lead cartridge supply. This is a commercial sizing decision, not a missing fact — flag to the Director as TPS flagged its equivalent (SW r153) |
| **Big-lift plant mob/demob (crane, Franna, shields)** | Already correctly flagged as "quote at award" in three places. No further action needed before submission beyond keeping the qualification live |
| **Kerb chutes / detention basin** | **Director decisions**, both already correctly parked with full costed alternatives (kerb chutes) or a stated non-quantifiable basis (basin bulk earthworks). No new action — carried forward as-is |

---

## 5. Hauraton GT verdict — calibrated result

**Prior uncalibrated run: "Hauraton GT: FAIL (quarry material)."**

**Calibrated result: REFINED — neither a blanket confirmation nor a full overturn.**

The prior run was right to flag quarry material as the fault line, but it was too coarse to say anything else about the product, because it tested "Hauraton GT" as one undifferentiated group. Tested at the four-designation level the population actually exists at (GT1–GT4 PRO200 Fibretec; GT5 PRO100 SS heelguard; GT6 PRO200 G-tec D400 ductile; GT7–GT9 PRO100 SS heelguard), the picture is genuinely mixed:

- **Channel supply** (all four designations, 4 separate rates, all Reece Q-459014445-sourced, all correctly escalated ×1.38 PE family) — **CONFIRMED COMPLETE.** Not a fail.
- **Delivery** (Reece freight lots, both stages) — **CONFIRMED COMPLETE.**
- **Trash boxes and end caps** (the classic Rule 4 accessory trap) — **CONFIRMED COMPLETE.** Mud buckets and grates are correctly bundled into the per-unit Reece rate; installation labour for the boxes is a named, separate crew-day activity in both stages. This is the opposite of a fail.
- **Excavation/installation labour** (`C-06`, `C-08`) — **CONFIRMED COMPLETE** as labour. Both activities are named, quantified crew-day lines with sensible production rates (24.4 m/day for GT1-4+GT7-9; 15.5 m/day for GT5+GT6).
- **Quarry/bedding material** — **CONFIRMED AS A FAIL, and now precisely located and quantified.** The prior run was correct that this component does not exist in the model. The calibrated test adds three things the prior run did not have:
  1. **Proof the gap is real, not a search miss.** The bedding-stone formulas in both stage sheets (`Stage1A_Drainage!Q1`, `Stage1B_Drainage!Q1`) were read cell-by-cell; both formulas explicitly enumerate the pipe-line rows they sum and explicitly exclude every GT row (`C54`/`C55` in 1A; the GT7/G1/G2 rows in 1B). This is not an omission that might be hiding in a rounding allowance — it is a formula that structurally cannot include GT metres.
  2. **Proof the gap contradicts a written claim, twice over**, which is a more serious finding than a simple shortfall: `EBC` row E3 states GT was *"REINSTATED into base... including excavation & quarry"*, and `01_SCOPE_MATRIX.md` row L1 states TCS prices GT *"in full (GT1–GT4, GT7–GT9, trash boxes, connection pits, excavation and quarry)"*. Both documents assert quarry is priced. It is not. This is exactly the Rule 4 failure mode the rule exists to catch — a controlled document stating an inclusion that the cost model does not actually contain.
  3. **A cross-check that the modeller knows how to do this correctly, and simply didn't do it for GT.** `Stage1A_Drainage!Q2` prices "Bedding stone — culvert extra-over" for the RCBC/box-culvert population (52 T @ $62/T = $3,224) as a discrete, separately-identified material line, distinct from ordinary pipe bedding. The same discipline was never applied to the 608.5 m of GT channel. This rules out "quarry material is implicitly inside the crew-day rate" as an explanation — crew-day rates are pure labour (`LabourRates_Master!$G$15`), and the model's own convention is to price granular material separately whenever it applies.

**Net effect on the number:** using the model's own bedding-stone factor (0.203 T/m, the same figure used for every piped line) as an indicative-only cross-check, the unpriced exposure is approximately **$7,626 pre-contingency (≈$12,736 at sell)** — small in absolute terms against the $2.99M grand total, but immaterial size does not change the finding: a written reinstatement claim is not backed by a cost line, and no evidence on file confirms the pipe-bedding factor is even the correct basis for a surface channel (concrete haunching is at least as plausible a requirement and would carry a different, likely higher, cost). **Verdict: REFINED to "excavation and installation labour are genuinely reinstated; quarry/bedding material is not, and the written claim that it is should be corrected or the cost added, pending confirmation of the correct install detail."**

---

## 6. Rule 4 wording controls for the submission

| Finding | Required wording control |
|---|---|
| GT quarry/bedding material gap | Do **not** carry forward `EBC` E3's "including excavation & quarry" or `01_SCOPE_MATRIX.md` L1's "excavation and quarry" into the external submission without first resolving §5. If unresolved at submission, the qualification must read: *"grated trench drain installation includes excavation and channel setting; bedding/surround material is qualified as an allowance pending confirmation of the manufacturer's installation detail."* Never state "grated trench drains supplied and installed" unmodified while this is open. |
| WSUD StormFilter commissioning / false floor | *"Supply and delivery of 22× Ocean Protect Tall (690) PSorb StormFilter cartridges and DN3300 manhole is a PC Sum + 15%; installation, connection and backfill are in the base lump sum."* Add: *"Commissioning, false-floor and anti-flotation provisions are qualified pending confirmation of the nominated supplier's scope of supply."* Never say "WSUD system complete" or "filtration system included" without that second sentence while Register Gap #1 is open. |
| GT6 spec substitution | *"GT6 grated channel is priced on the Recyfix PRO200 G-tec offer; the drawing schedule nominates PRO100 D400 G-tec (code 47245) — equivalence to be confirmed prior to order."* Never represent GT6 as priced strictly to the drawing schedule until Gap #7 closes. |
| RGU inlet sourcing | *"Road gully inlet units are priced on a historical rate basis; current supplier confirmation to be obtained prior to order."* Do not represent RGU pricing as quote-backed — it is the one supply rate in the whole civil population with zero current quotes. |
| BCC headwalls (determination-9 pass) | Safe to state plainly: *"Box-culvert headwalls are supplied ex Humes."* Do **not** name Jaybro anywhere near RCBC/box-culvert headwalls in the submission — Jaybro declined that scope in writing, and any submission text implying otherwise would misstate the supply chain. |
| Kerb chutes | *"Kerb chutes are excluded from the base offer; rock protection and erosion-control matting to the chute locations are included. Full kerb-chute construction is available as a priced variation."* Never say "site drainage complete" or "kerb works included" as a blanket statement. |
| Detention basin / spillway | *"Detention basin bulk earthworks and the concrete spillway structure are excluded from this offer pending confirmation of trade allocation."* Never describe the detention basin as "constructed" or "complete" under this offer. |
| Subsoil / strip-filter system | *"The subsoil/strip-filter drainage system is excluded from this offer (by others); TCS's scope is limited to accepting connections at the wall of TCS-supplied collector pits."* Never say "all civil drainage included" while this exclusion stands — it is precisely the prohibited blanket wording Rule 4 names. |
| Big-lift plant (crane/Franna/shields) | Internal-only qualification, but if referenced in the submission programme narrative: *"Major lifting plant (50t crane, Franna) and trench shielding are allowed at indicative rates; firm pricing to be confirmed at award."* Never imply these are contracted/firm-priced. |
| General — "all civil services" / "complete system" | Per Rule 4's prohibited-wording list, neither phrase may appear in the TCS submission while items 1, 2–5, 7, 8, 19, 20 and 21 above carry any open qualification. |

---

*Test completed 27 Jul 2026 against `ROK_TCS_CostModel_V2.xlsx` as currently committed. No workbook, submission, PDF, register or prior concordance file was modified — this is a read-only Rule 4 test. All 21 items carry a cell reference for every ✓, and every GAP/MISSING verdict is evidenced against a specific formula, cell, or the absence of a corroborating document, per Rule 2.*
