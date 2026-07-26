# EQUIPMENT_TEST_TPS — Rule 4 fixture & equipment test
**Tender:** TEN16699 Rockhampton Sports Precinct Stage 1A & 1B · **Entity:** TriCore Plumbing Services (hydraulic)
**Model tested:** `Working_Cost_Models\TPS\ROK_TPS_CostModel_V2.xlsx` (post-repair, recalculated 27 Jul 2026)
**Rule applied:** TENDER_PROMPT §2 Rule 4, third test — *"for every fixture, tapware item, bubbler, hot water unit, pump and piece of equipment, determine SEPARATELY: supply · delivery · storage · installation · fixings · accessories · connection · testing · controls · and whether it is builder-supplied or Principal-supplied. Never write 'fixtures included' when only installation or connection has been costed."*
**Sources:** workbook rows as cited · Phase 7 `PROGRAMME_LABOUR_PLANT.xlsx` sheet `TPS_Activities` (activity IDs) · `01_SCOPE_MATRIX.md` · `MATERIAL_QUOTE_REGISTER.xlsx`

**Result: 14 equipment items tested · 12 complete on first pass · 2 genuine gaps found and closed · 4 duplicate installation tokens found and neutralised.** No item remains MISSING.

---

## 1. Method and the double-count trap that drove this test

The big-ticket blocks on `TCS $ Sched` carry a cell literally labelled **`Installation_MH`** holding a *dollar* figure — GIT $250, HW pump $200, NBC HWUs $600, PAM HWU $200 (**$1,250 total**). These are legacy CQU-template tokens, not hour counts. $250 plainly does not install a 1500 L in-ground grease arrestor.

The question Rule 4 forces is not "is the token big enough" but **"where is installation actually priced, and is it priced once?"** Testing each item against Phase 7 showed that **every one of the four has full crew-day installation labour already loaded into the work-area labour blocks**. The tokens were therefore *duplicates*, not shortfalls — retaining them would double-count. All four are now **$0 with an in-cell note naming the covering activity ID**; the labour they were shadowing stays where it belongs, in the crew-day rows.

> **Correction to an earlier reading.** A search of the Phase 7 `Activity` column for "hot water" returns nothing, which suggested HWU and pump installation were uncosted. That is a column artefact: the words "Hot water" sit in the **`System`** column, while the **`Activity`** column reads *"2x Rheem 315L HWU + HW circulating pump + flow/return loop"* (**T4-03**, 3 crew-days, Crew 4) and *"PAM Rheem 50L HWU + TMV + Ø32 check-meter assembly"* (**T4-06**, 1 crew-day, Crew 4). Both were already loaded into the model — NBC Crew 4 = 21 crew-days (T4-01 12 + T4-02 3 + **T4-03 3** + T4-04 1 + T4-07 2); PAM Crew 4 = 5 crew-days (T4-05 4 + **T4-06 1**). Hot water unit and pump installation **is** costed. Verified against the source workbook, not inferred.

---

## 2. The test table

Legend: **✓** priced, location shown · **N/A** not applicable · **OTHERS** another party's scope, correctly excluded · **GAP→FIXED** was missing, now closed (row cited)
Sheet abbreviations: **SW** = `Siteworks ` · **NBC** = `ClubHouse (NBC )` · **PAM** = `Public Amenities (PAM)` · **TCS** = `TCS $ Sched`

### 2.1 Grease arrestor — 1500 L Viking PanelTim in-ground GIT × 1 (NBC)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | TCS `W11` = $6,110 tank + $2,413.28 lids (Tradelink 1066334; Reece Graf alternative $4,010.30 noted cheaper) |
| Delivery | ✓ | TCS `W15` freight $250 + crane/HIAB NBC r149 (15 hr @ $180) |
| Storage | ✓ | SW r153 long-lead storage allowance (new) + 20 ft site container, Prelim & OH `B80` |
| Installation | ✓ | **T1-08** — 8 crew-days Crew 1; rate basis explicitly *"GIT excavation/set"*; plant 3–5 T excavator 4 d + crane truck 1 d |
| Fixings / accessories | ✓ | Lids in supply; bedding/backfill via the take-off helper (SW `I902`/`M902`) |
| Connection | ✓ | Trade waste pipework NBC r813–r838 (110 HDPE 54.78 m, Geberit 50, junctions, risers, DT traps) |
| Testing / commissioning | ✓ | **T5-02** *"GIT commissioning"* (3 crew-days Crew 5) |
| Controls | N/A | Passive gravity arrestor — no controls |
| Supply ownership | **TPS** | Sized 1500 L per H-NBC-102; size conflict 1500 / 2000 / 550–5000 L unresolved → PC-allowance basis, RFI CL B6 |
| Token | Duplicate | `W16` $250 → **$0**, note cites T1-08 |

### 2.2 Hot water units — 2 × Rheem 613/315 315 L (NBC)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | TCS `AC11` $3,438.29 ea × **qty 2** (`AC14`, corrected from 3 — take-off double-count) |
| Delivery | ✓ | TCS `AC15` freight $300 + crane truck 0.5 d inside T4-03 + NBC r149 HIAB |
| Storage | ✓ | SW r153 (new); Rheem lead time 4–6 wks per Phase 7 long-lead flags |
| Installation | ✓ | **T4-03** — 3 crew-days Crew 4, *"2x Rheem 315L HWU + HW circulating pump + flow/return loop"* |
| Fixings / accessories | **GAP→FIXED** | Safe trays ✓ TCS `AC12` $52.80/unit · seismic strap ✓ NBC r932 hardware + **T4-07** labour · **SS plinth/stand was priced nowhere → NBC r933 added, 2 EA @ $260** |
| Connection | ✓ | Flow/return loop in T4-03; NBC water rough-in T4-01 (r420/r423 316 SS + B-press set) |
| Testing / commissioning | ✓ | **T5-06** *"TMV certs ×11, RPZD tests, **HWU**, Form 72"* (4 crew-days Crew 5) |
| Controls | **OTHERS** | Electrical isolators by the electrical trade per H-NBC-301 / matrix 4.11-a — correctly excluded |
| Supply ownership | **TPS** | |
| Token | Duplicate | `AC16` $600 → **$0**, note cites T4-03 |

### 2.3 Hot water unit — 1 × Rheem 613/050 50 L (PAM)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | TCS `W25` $2,016.08 — **rate corrected during the repair** from $3,438.29 (the 315 L model's rate had been used for a 50 L unit) |
| Delivery | ✓ | TCS `W29` freight $150 |
| Storage | ✓ | SW r153 (new) |
| Installation | ✓ | **T4-06** — 1 crew-day Crew 4, *"PAM Rheem 50L HWU + TMV + Ø32 check-meter assembly"* |
| Fixings / accessories | **GAP→FIXED** | Safe tray ✓ TCS `W26` $52.80 · seismic ✓ PAM r853 · **SS plinth/stand → PAM r854 added, 1 EA @ $260** |
| Connection | ✓ | PAM water rough-in T4-05; safe-tray waste in the 0.45 m sewer pick-up on plan F (PAM r695) |
| Testing / commissioning | ✓ | **T5-06** |
| Controls | **OTHERS** | Electrical isolator by the electrical trade — matrix 3.11-a |
| Supply ownership | **TPS** | 3 × 3.6 kW, 240 L FHD; PTR valve supplied with the unit |
| Token | Duplicate | `W30` $200 → **$0**, note cites T4-06 |

### 2.4 Hot water circulating pump set — Grundfos UPS32-80N dual SS (NBC)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | TCS `Z11` $6,775.83 (Reece Q-459014431) |
| Delivery | ✓ | TCS `Z15` freight $150 |
| Storage | ✓ | SW r153 (new) |
| Installation | ✓ | **T4-03** — same 3 crew-days, activity names the pump explicitly |
| Fixings / accessories | ✓ | Seismic/hanger restraint NBC r932 + T4-07 |
| Connection | ✓ | Flow/return loop in T4-03; isolation/check valves NBC r699/r700/r702 |
| Testing / commissioning | ✓ | **T5-06** |
| Controls | **OTHERS** | Integrated pump control; external panel, power and cabling by the electrical trade. Quote note *"excludes panel, manifolding, install"* → qualification stated |
| Supply ownership | **TPS** | Count is **L-confidence** — Denis counted 1, vol06_11 review found *"pumps: none shown"* (Opens #15). Retained conservatively; verify before award |
| Token | Duplicate | `Z16` $200 → **$0**, note cites T4-03 |

### 2.5 Backflow prevention — RPZDs and check valves

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | NBC r690 20 mm RPZD × **4** (adopted higher) · NBC r834 50 mm RPZD × **2** · NBC r699 20 mm check × 4 · NBC r835 100 mm check (TW) × 1 · SW r661 100 mm check × 6 |
| Delivery | ✓ | Work-area delivery allowances (NBC `F940` $6,500 · SW `F871` $5,000) |
| Storage | ✓ | 20 ft container, Prelim & OH `B80` |
| Installation | ✓ | **T4-02** *"NBC TMVs ×10 + RPZD/check sets + isolation valves"* (3 crew-days) · site checks in **T2-05** |
| Fixings / accessories | ✓ | Ball valves/strainers inside the Valvcheq assembly rates |
| Connection | ✓ | T4-01 / T4-05 water rough-in |
| Testing / commissioning | ✓ | **T5-06** *"RPZD tests"* + first-year certification |
| Controls | N/A | Mechanical devices |
| Supply ownership | **TPS** | **Note:** device *registration* with the water authority rides with plumbing approval lodgement, which is **excluded** (cross-cutting X2) — stated, not silent. Possible 50 mm/20 mm position overlap → Opens #15 |

### 2.6 Thermostatic mixing valves — 11 total (NBC × 10, PAM × 1)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | NBC r712 × 10 @ $587.96 · PAM r682 × 1 @ $587.96 — **rate includes the SS lockable cabinet/box** |
| Delivery | ✓ | Work-area delivery allowances |
| Storage | ✓ | 20 ft container |
| Installation | ✓ | **T4-02** (NBC, 3 crew-days) · **T4-06** (PAM, 1 crew-day) |
| Fixings / accessories | ✓ | Lockable SS cabinet in the supply rate; recess boxes per the Reece curve |
| Connection | ✓ | T4-01 / T4-05 rough-in |
| Testing / commissioning | ✓ | **T5-06** *"TMV certs ×11"* — count reconciles exactly to 10 + 1 |
| Controls | N/A | Thermostatic, self-regulating |
| Supply ownership | **TPS** | NBC count 10 is Denis's; vol06_11 found no TMV count or cabinet note on NBC-200/201/202 → allow per warm-water groups, RFI Opens #28 |

### 2.7 Water meters — site primary (100 mm fire + 100 mm CW) and PAM Ø32 check meter

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | SW r689 = **1 EA** covering **both** assemblies @ $5,500 (legend groups them as one item — qty corrected from 0.5) · PAM r680 Ø32 check-meter assembly $949 |
| Delivery | ✓ | SW `F871` delivery allowance |
| Storage | ✓ | 20 ft container |
| Installation | ✓ | **T2-03** *"100 fire + 100 CW meter assemblies + 4×2 m slab + bollards"* (4 crew-days, congestion penalty stated) · **T4-06** for the PAM check meter |
| Fixings / accessories | ✓ | 4 × 2 m concrete slab + bollards inside T2-03; SW r166 valve margin strip/signage |
| Connection | ✓ | T2-02 authority Ø300 tapping cluster |
| Testing / commissioning | ✓ | **T2-10** hydrostatic test + disinfection |
| Controls | N/A | |
| Supply ownership | **TPS** | Interface **L7**: TPS carries assemblies, slab and bollards as drawn on H003 — priced once, never by TCS. If FRW elects to supply the meter bodies themselves that is a **credit**, flagged. No PRV at PAM vs NBC 500 kPa → RFI CL C8 |

### 2.8 Fire booster assembly and cabinet (site)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | SW r293 150 mm H-pattern booster assembly $2,350 · SW r294 booster cabinet with doors + stickers $1,155 |
| Delivery | ✓ | SW r152 crane/HIAB 10 hr @ $180 + `F871` |
| Storage | ✓ | SW r153 (new) — **10–12 week lead time**, the longest-lead fire item |
| Installation | ✓ | **T2-08** *"150 H-pattern booster assembly + cabinet + 100 dual pillar hydrant"* (3 crew-days; 8 T excavator 1 d + crane truck 1 d) |
| Fixings / accessories | ✓ | Cabinet doors/stickers in the supply rate |
| Connection | ✓ | 125 REDLINE fire main T2-07; Plasson PE×galv adapter SW r198 |
| Testing / commissioning | ✓ | SW r149 **boost test $3,560** + SW r150 3 × full hydro test @ $1,945 + SW r151 Form 72; QFES 2-week notice per VOL38 §12.17/25 |
| Controls | N/A | No electrical boost pump in this design |
| Supply ownership | **TPS** | Fire extent qualified — 217.73 m + 1 booster + 1 hydrant looks light vs AS2419.1, RFI Opens #13 |

### 2.9 Dual pillar hydrant — 100 mm flanged base 1500 high (site)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | SW r296 $365 (only hydrant on the whole site take-off) |
| Delivery / storage | ✓ | `F871` / SW r153 |
| Installation | ✓ | **T2-08** (3 crew-days) |
| Fixings / accessories | ✓ | Riser + landing valves in the supply description; valve box/spindle riser rates available |
| Connection | ✓ | Fire main T2-07 |
| Testing / commissioning | ✓ | SW r149/r150 |
| Controls | N/A | |
| Supply ownership | **TPS** | Coverage RFI Opens #13 |

### 2.10 Drinking fountains — 2 chilled CF400 (NBC, 1A) + 2 non-chilled (PAM, 1B)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ **PC SUM** | TCS `N72` 1A 2 × $11,050 + 15% = $25,415 · TCS `N75` 1B 2 × $7,200 benchmark + 15% = $16,560 |
| Delivery | ✓ | Tradelink delivery $31.82/drop inside the work-area delivery allowances |
| Storage | ✓ | SW r153 / container |
| Installation | ✓ | **T5-04a** *"ODF drinking fountains ×2 (chilled — PC Sum) incl water/waste connections"* (1 crew-day Crew 5) |
| Fixings / accessories | ✓ | Wall-mount fixings in the unit price. **Signage is explicitly extra** on the quote (*"IF WANTED SGINAGE THEI WILL BE ADDED COST"*) — excluded and stated |
| Connection | ✓ | Supply/waste rough-in in 4.11-c / 3.11-c Base; T5-04a connections |
| Testing / commissioning | ✓ | T5-06 |
| Controls | ✓ | Chiller integral to the unit; power by the electrical trade |
| Supply ownership | **TPS (PC Sum)** | Non-chilled CF400 **unpriced by anyone** (Gap #6) — $7,200 benchmark, re-quote pending. Same-SKU chilled/non-chilled confusion → RFI CL C10 |

### 2.11 Water bubbler stations — 4 site DF/BT positions (1B recreational park)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ **PC SUM** | TCS `N76` 4 × $7,200 benchmark + 15% = $33,120 |
| Delivery / storage | ✓ | As 2.10 |
| Installation | ✓ | **T5-04b** *"Water bubbler stations install (PC Sum units) + supply/waste connections"* (1 crew-day Crew 5) |
| Fixings / accessories | ✓ | In the unit price |
| Connection | ✓ | **T2-09** 1B branch take-offs — *"bubbler/DF supplies + wastes"* (4 crew-days) |
| Testing / commissioning | ✓ | T5-06 |
| Controls | N/A | Non-chilled |
| Supply ownership | **TPS (PC Sum)** | **Slabs and surrounds by others** per matrix 4.5-c — correctly excluded. Unit type undefined in the H003 legend → RFI CL C10 |

### 2.12 Billi Quadra 4180 boiling/chilled unit × 5 (NBC canteen) — **PRINCIPAL-SUPPLIED**

| Component | Status | Where priced |
|---|---|---|
| Supply | **PRINCIPAL (RCC)** | **Deducted** from the fixtures PC sum: −$38,261 at TCS `S73`, labelled *"SUPPLIED BY RCC per FF&E VOL25"*. TPS carries **no** supply cost — confirmed |
| Delivery | **PRINCIPAL** | With the unit |
| Storage | **PRINCIPAL** | |
| Installation | ✓ **TPS** | **T5-02** *"Billi install (RCC-supplied) + Stoddart sink benches taphole/connect + spray rinse"* (3 crew-days Crew 5) |
| Fixings / accessories | ✓ TPS | Benchtop tapholes drilled on site per VOL 25 — inside T5-02 |
| Connection | ✓ TPS | Water + waste connection in T5-02; underbench tundish in NBC r833 |
| Testing / commissioning | ✓ TPS | T5-06 |
| Controls | **OTHERS** | Electrical supply and isolation by the electrical trade |
| Supply ownership | **PRINCIPAL — install/connect only** | This is exactly the Rule 4 trap: the submission must say *"installation and connection of the Principal-supplied Billi units"*, never *"Billi units included"* |

### 2.13 Fire hose reel, fire blanket and AS1851 maintenance (NBC)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | NBC r307 FHR 36 m with 25 mm isolation valve $125 · NBC r308 fire blanket $60 (added in the repair) |
| Delivery / storage | ✓ | `F940` / container |
| Installation | ✓ | **T4-04** *"NBC FHR ×1 + FB ×1"* (1 crew-day) |
| Fixings / accessories | ✓ | Bracket/isolation valve in the supply rate |
| Connection | ✓ | T4-01 rough-in; supply source to the FHR unconfirmed → CL C8 |
| Testing / commissioning | ✓ | SW r149/r150; **NBC r309 AS1851 12-month maintenance & tagging $2,500** |
| Controls | N/A | |
| Supply ownership | **TPS** | **Fire extinguishers × 9 (NBC 8 + PAM 1) are EBC** — VOL38 §14.1 says the plumber prices them, the drawing note says the builder provides them; carried as EBC-3 add-price $2,540.78 + RFI CL B8. Never stated as included |

### 2.14 Automatic trap primers × 2 (NBC)

| Component | Status | Where priced |
|---|---|---|
| Supply | ✓ | NBC r717 × 2 @ $99.49 |
| Delivery / storage | ✓ | `F940` / container |
| Installation | ✓ | **T4-02** valving lot |
| Fixings / connection | ✓ | T4-01 rough-in |
| Testing | ✓ | T5-06 |
| Controls | N/A | Mechanical |
| Supply ownership | **TPS** | |

---

## 3. Findings summary

| # | Item | Result |
|---|---|---|
| 1 | 1500 L Viking GIT | Complete — token $250 was a duplicate of T1-08 |
| 2 | Rheem 315 L HWU × 2 (NBC) | **Fixings gap** (SS plinth) → closed; token $600 duplicate of T4-03 |
| 3 | Rheem 50 L HWU × 1 (PAM) | **Fixings gap** (SS plinth) → closed; token $200 duplicate of T4-06 |
| 4 | HW circulating pump set | Complete — token $200 was a duplicate of T4-03 |
| 5 | RPZDs / check valves | Complete (registration correctly excluded with X2) |
| 6 | TMVs × 11 | Complete — commissioning count ties exactly |
| 7 | Water meters (site + PAM) | Complete |
| 8 | Fire booster + cabinet | Complete |
| 9 | Dual pillar hydrant | Complete |
| 10 | Drinking fountains | Complete (signage excluded and stated) |
| 11 | Water bubbler stations | Complete (slabs by others) |
| 12 | Billi × 5 | Complete — **Principal-supplied, install/connect only** |
| 13 | FHR / FB / AS1851 | Complete (extinguishers EBC, not "included") |
| 14 | Trap primers | Complete |
| — | **Storage, all items** | **Gap across the board** → closed with SW r153 |

**12 of 14 complete on first pass; 2 fixings gaps + 1 cross-cutting storage gap closed; 4 duplicate tokens neutralised.**

---

## 4. Changes made to the model

| Change | Cell / row | Effect |
|---|---|---|
| `Installation_MH` token → $0, note names T1-08 | TCS `W16` | −$250 |
| `Installation_MH` token → $0, note names T4-03 | TCS `Z16` | −$200 |
| `Installation_MH` token → $0, note names T4-03 | TCS `AC16` | −$600 |
| `Installation_MH` token → $0, note names T4-06 | TCS `W30` | −$200 |
| HWU 316 SS plinth/stand + fixings, 2 EA @ $260 | NBC r933 | +$520 cost |
| HWU 316 SS plinth/stand + fixings, 1 EA @ $260 | PAM r854 | +$260 cost |
| Long-lead equipment storage & double-handling allowance | SW r153 | +$1,200 cost |

Every token cell retains an in-cell note naming the covering activity ID, so the labour is **traceable, not lost**. Cost additions total **$1,980** pre-contingency (**$2,305.20** after contingency), which at the 41.5% chain is **+$3,261.86** of sell; less the $1,250 of removed tokens, the net movement is **+$2,011.86**.

---

## 5. Director decision — big-ticket markup quantum

The four big-ticket blocks sit **outside** the normal cost→markup chain: they take purchase × 1.15, then add freight un-marked-up. This is pre-existing TriCore architecture and has been **left exactly as it is**. Quantified so the decision can be made against a number:

| Item | Cost (purchase + freight) | Current sell (×1.15 + freight) | Normal chain (cost × 1.415) | Delta |
|---|---:|---:|---:|---:|
| 1500 L Viking GIT + lids | 8,773.28 | 10,051.77 | 12,414.19 | +2,362.42 |
| HW circulating pump set | 6,925.83 | 7,942.20 | 9,800.05 | +1,857.84 |
| Rheem 315 L HWU × 2 + safe trays | 7,282.18 | 8,329.51 | 10,304.28 | +1,974.78 |
| Rheem 50 L HWU × 1 + safe tray | 2,218.88 | 2,529.21 | 3,139.72 | +610.50 |
| **TOTAL** | **25,200.17** | **28,852.70** | **35,658.24** | **+6,805.55** |

**Current effective margin on this equipment: 14.49%. The normal chain would give 41.50%. Adopting it would add $6,805.55 of sell** (1A +$6,195.05, 1B +$610.50), lifting the grand total from $2,009,794.18 to **$2,016,599.73**.

Two things the Director should weigh:
1. **$850 of freight is currently carried with no margin at all.** Under the normal chain freight sits inside cost and attracts markup like every other cost dollar.
2. The 14.49% recovers little more than handling. Now that installation labour is proven to sit in the crew-day blocks, the ×1.15 is doing **only** a supply-margin job — it is not a disguised installation allowance, which is what such tokens usually turn out to be.

**Not changed.** Recorded here and in `TPS_CHANGE_LOG.md` for decision.

---

## 6. Rule 4 wording controls for the submission

Language the submission must use, straight off this test:

- **"Installation and connection of the Principal-supplied Billi Quadra 4180 units"** — never "Billi units included". Supply is RCC's.
- **Fixture supply is a separate PC Sum line** (Tradelink 1066143 basis + 15%), install labour in the Base. Never "fixtures included" as a blanket phrase — the PC line defines exactly what supply is covered, and the adopted-count extension (+$25,000) is stated.
- **Drinking fountains and bubblers are calculated PC Sums** — units supplied under the PC, installed by TPS, **slabs and surrounds by others**, **signage excluded**.
- **Fire extinguishers are excluded (EBC-3)** with an add-price held — never implied by "fire compliance included".
- **Backflow device registration** rides with plumbing approval lodgement, which is excluded (X2). Devices are supplied, installed, tested and certified; *registration* is not.
- **Electrical isolators, panels, power and control cabling to the HWUs, pump set and chilled fountains are by the electrical trade** — TPS states this so "hot water installed" cannot be read as including power.
- **Grease arrestor is priced at 1500 L** on an allowance basis with the three-way size conflict (1500/2000/550–5000 L) stated and RFI'd.

---

*Test completed 27 Jul 2026 against the recalculated model. Excel COM `CalculateFullRebuild` re-run after every change: **0 formula errors across all 12 sheets**, tie check `N88 = 0`, 14 computed-vs-expected checks with 0 divergent cells.*
