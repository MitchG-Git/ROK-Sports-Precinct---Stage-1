# Denis Email Updates — Instruction Register

**Source folder:** `TriCore Docs\Denis Email updates\` (4 files = 2 email sources + 1 embedded attachment)

## Documents & revision/date (verified INSIDE the documents)

| Source | Verified from inside | Date/Rev |
|---|---|---|
| A. "260724 : ROK Sports Precinct, CIVIL SW V1 Summaries" (.msg + .pdf print) | .msg metadata: From Denis Zhong - TCS <denis.z@tricorecivil.com.au> To Mitch - TCS <mitch@tricorecivil.com.au>; PDF header block identical | Sent **Fri 24 Jul 2026 17:30:06 (+10:00)**; contains full quoted email "260717: ROK Sports Precinct, CIVIL SW V1 Summaries" sent **Fri 17 Jul 2026 12:27 PM** |
| B. "260724_ ROK SPORTS Hydraulic Summaries" (.msg + .pdf print) | .msg metadata: same sender/recipient; PDF header identical | Sent **Fri 24 Jul 2026 17:28:54 (+10:00)** (PDF header shows 5:29 PM — same email, minute rounding) |
| C. Attachment to B: `1066143_ROCKHAMPTON_SPORTS_PRECINCT.pdf` — Tradelink QUOTATION 1066143/SP | Quote header inside PDF: Tradelink Pty Limited, 411 Yaamba Rd Rockhampton; prepared by Alexia Griffin | Quote prepared **15/07/26**, expiry **13/08/26**; addressed to **TRICORE CIVIL SERVICES PTY LTD**; project "ROCKHAMPTON SPORTS PRECINCT STAGE 1A & 1B, 544 YAAMBA RD, PARKHURST J/N-28703083" |

### .msg vs .pdf equivalence check
- **Source A:** .msg body text and the PDF print are the SAME email chain (24 Jul reply + quoted 17 Jul email). PDF additionally renders the 10 inline screenshot images (image001–010.png) that the .msg carries as embedded attachments. **Treat as one source.** No document attachments in A — inline images only. (The original 17 Jul .msg is not in this folder; it survives only as quoted text + screenshots inside the 24 Jul email.)
- **Source B:** same email; **BUT the PDF print CLIPS the right-hand rate/value columns of the copper table on p.1** (only "m / 135" etc. visible) and does not render the file attachment (name listed in header only). The **.msg body preserves the full rates** ($343.30/m, $46,345.00 etc. — see quantities below) and carries the Tradelink PDF attachment. **The .msg is the controlling copy of Source B.**
- **Attachment C** extracted from the .msg and **MD5-verified byte-identical** (99B27B385B439093C5CF3D04CAC8C0AE, 38,312 bytes) to the repo copy at `Material\01 - Project Specific\Fixtures\tradelink\1066143_ROCKHAMPTON_SPORTS_PRECINCT.pdf` — not a new document; cross-reference only, no separate register entry needed.

---

## Scope items found (with refs)

**Civil SW (TCS) — Source A:**
- Civil SW take-off complete and transferred to pricing spreadsheet; quotes held for "rcp, rcbc, trench grate, head wall, hdpe pipe etc" (17 Jul email, opening para).
- Grated trench drains + trash boxes: priced from Reece but **excluded from total material price**, set aside at $164,860.30 (17 Jul pt 1).
- 100mm subsoil drain: measured 2,173 m, **excluded from total material price** (17 Jul pt 2).
- Swales: **all excluded** (17 Jul pt 3; PDF p.2 legend image — grassed swale w/ concrete-lined invert, grassed swale, vegetated swale, existing creek/swale).
- Kerb chutes: 17 Jul pt 4 allowed rock + erosion control mat only (excl. concrete kerb); **24 Jul pt 1 then excluded kerb chute material entirely** — "kerb chute is not the work scope".
- Stormwater pits: taken off from drawings (not the pit schedule) in Groundplan; material allowance 1 base + 1 "aspro" + 1 cover per pit given shallow depths (24 Jul pt 2).
- In-ground pipe excavation: 1,883 m total L/M at average depth, covering RCP + HDPE + PVC + drainage culverts (17 Jul pt 5).
- WSUD filtration system: Atlan estimate carried on front page of spready (17 Jul pt 6; table image PDF p.5).

**Hydraulic (TPS) — Source B:**
- Site works water: 200mm copper from **authority water main to water meter** ("The scope is from authority water main to water meter , measure in yellow"), incl. tee, bend, $800 connection-point material, "all the valves and fitting captured as well" (pt 1; drawing ref **25015-H003**; spec ref VOL 38 hydraulic services spec s10 Cold Water table — in-ground authority main to boundary meter = Kembla Copper Type B, sleeved — Denis's copper selection for the in-ground main complies with this row).
- NBC clubhouse / public amenities above-ground water: priced PEX <DN22 and **copper >DN22** (deviation — drawing **25015-H-NBC-002** & note WS2 require **316 stainless steel press-fit >DN22**) (pt 2).
- NBC hot water: 2x Rheem HWU + 1 hot water pump assumed from drawing **25015-H-NBC-200**; Reece rates, pump quoted at higher duty because no pump spec exists (pt 3).
- Pipe supports: hanger rods to be allowed — "the soil is high active according to geo report"; seismic restraint per drawing **25015-H0002** note 9 (bracing spacings: ductile 12m transverse / 24m longitudinal >65mm dia, 9m/18m <65mm; non-ductile 6m/12m) and VOL 38 spec cl 3.14 Fixing & supporting (Unistrut-equal galvanised channel, two-piece clamps, timber blocks, Flexistrut, slide guides; 2:1 safety margin; sleeves at penetrations w/ fire-rated packing; no explosive power tools) (pt 4).
- Fixtures: quantities still being finalised; Tradelink fixture quote received (pt 5 + attachment C: Netball Clubhouse + Public Amenities Block schedule, $252,694.77 ex GST).

---

## Quantities stated (with refs)

| Item | Qty / rate | Ref |
|---|---|---|
| Grated trench drain + trash box package (Reece), EXCLUDED, set aside | **$164,860.30** | A, 17 Jul pt 1 ("exclude in the total material price , total as 164860.30 put aside in green highlighted") |
| GT1 Recyfix Pro 200 Cl B125 type 010 Fibretec slotted grating | 129 m | A, PDF p.2 schedule image |
| GT2 ditto | 144 m | A, PDF p.2 |
| GT3 ditto | 146 m | A, PDF p.2 |
| GT4 ditto | 144 m | A, PDF p.2 |
| GT5 Recyfix Pro 100 Cl B125 SS anti-slip heelguard | 16 m | A, PDF p.2 |
| GT6 Recyfix Pro 200 Cl D400 heelguard G-Tec ductile iron | 32 m | A, PDF p.2 |
| GT7 / GT8 / GT9 Recyfix Pro 100 Cl B125 SS heelguard | 4 / 6 / 4 m | A, PDF p.2 |
| End caps 100mm / 200mm trench grate | 10 / 8 ea | A, PDF p.2 |
| Hauraton trash box 100 / 200 | 4 / 25 ea | A, PDF p.2 |
| Transport estimate for grate trench + trash box | 1 item | A, PDF p.2 |
| 100mm subsoil drain ("100mm socked ag pipe"), EXCLUDED | **2,173 m** | A, 17 Jul pt 2 |
| Kerb chute rock pad: "ROCK :DIA 100 , 180 thickness (measure area 56m2)" + erosion control matting | 56 m2 | A, PDF p.2 spready image (now superseded by 24 Jul pt 1 exclusion) |
| Kerb chute detail: rock pad D=100mm, 180mm min thickness, erosion control mat lapped (1.0m TMR Type 28) | — | A, PDF p.4 drawing F1325 section C image |
| L/M in-ground pipe (average depth), ALL stormwater pipes incl. culverts | **1,883 m** | A, 17 Jul pt 5 |
| WSUD filtration: cost $88,838.00 + 10% markup = charge $97,721.80; install estimate $6,000.00; fuel levy estimate $2,500.00; **total $106,221.80** | — | A, PDF p.5 table image (17 Jul pt 6) |
| 200mm Pipe Kembla Copper Type B | **135 m @ $343.30 = $46,345.00** | B .msg pt 1 (rates clipped in PDF print) |
| 200mm copper tee | 2 ea @ $390.00 = $780.00 | B .msg pt 1 |
| 200mm copper 90° bend | 1 ea @ $420.00 = $420.00 | B .msg pt 1 |
| 200mm copper connection point (material) | 1 ea @ $800.00 | B .msg pt 1 |
| Rheem HWU / hot water pump (NBC) | 2 ea / 1 ea (assumed) | B pt 3 |
| Tradelink fixture quote 1066143/SP total | **$252,694.77 ex GST / $277,439.33 inc GST** | C, p.7 |

All quantities above are Denis's take-off figures, not contract quantities (lump sum tender — schedule quantities are estimates only).

---

## Instruction register (every statement/instruction, one row each)

| # | Src / point | Denis's statement (quoted where load-bearing) | Type | Status |
|---|---|---|---|---|
| 1 | A 17/7 intro | "Civil SW take off done and transferred into spready, all the quote of main items (rcp , rcbc , trench grate , head wall , hdpe pipe etc ) are available" | Status report | Actioned |
| 2 | A 17/7 pt1 | Grated trench box + trash box "exclude in the total material price , total as 164860.30 put aside in green highlighted" (Reece prices held) | Exclusion | Actioned (still open: decision whether to include in tender) |
| 3 | A 17/7 pt2 | "100 mm sub soil drain , measure as 2173 meters on plan , put it aside , exclude in the total material price" | Exclusion + qty | Actioned (still open: scope decision — subsoil drainage likely IS drainage scope) |
| 4 | A 17/7 pt3 | "exclude all the swales" | Exclusion | Actioned |
| 5 | A 17/7 pt4 | "for all the kerb chute , only allow for rock and erosion contraol mat, exclude concrete kerb" (rock 56m2) | Assumption/exclusion | **Superseded** by row 9 |
| 6 | A 17/7 pt5 | "L/M of Inground Pipe (Average Depth) , total meter is 1883 meters , which include all the rcp pipe . hdpe pipe , pvc pipe , and also drainage culvert , need to put more ... allowance for excavation and bedding material of the CULVERT ?" | Question to Mitch | **Still open** — no extra culvert exc/bedding allowance currently carried |
| 7 | A 17/7 pt5 | "have excluded the excavation and quarry for treanc drainage now , need to put allowance for the excavation and quarry for them if decide to include grate trench and trash box into the quote ?" | Question to Mitch | **Still open** — if trench drains reinstated, exc+quarry must be added back |
| 8 | A 17/7 pt6 | "WSUD FILTRATION SYSTEM in the front page , Atlan estimate it due to lack of specific model no" (carried $106,221.80 incl $6,000 install + $2,500 fuel levy estimates) | Assumption/provisional price | **Still open** — model no. needed; Atlan figure is an estimate only; RFI candidate |
| 9 | A 24/7 pt1 | "Had already exclude thew material regarding to kerb chute as required . ( summaries point 4 had already excluded , as kerb chute is not the work scope )" | Exclusion (per Mitch's prior direction — "as required") | Actioned — supersedes row 5; verify spready removed the 56m2 rock + mat too (see Conflicts 3) |
| 10 | A 24/7 pt2 | "Due to the pit schedule is not consist with the drawing, I did the take off directly on drawing in GP ( items on drawing are more than the pit schedule )" | Method statement + doc-conflict report | Actioned; conflict itself **still open** — tender RFI candidate |
| 11 | A 24/7 pt2 | "the depth of them is really shallow , so allow for 1 base ,one aspro , one cover should be enough for cover the material cost of the pits" | Assumption | Actioned (estimator to ratify against pit schedule depths before close) |
| 12 | A 24/7 pt3 | "Hume amended the price , change in spready accordingly" (Humes RCP/RCBC supplier) | Price update | Actioned — verify latest Humes quote rev captured in spready |
| 13 | B pt1 | "Site work section hydraulic , had allow for 200mm copper pipe . tee, bend and $800 material cost for 200mm copper connection point ( all the valves and fitting captured as well ). The scope is from authority water main to water meter , measure in yellow." 135m @ $343.30 | Allowance + qty + scope boundary | Actioned |
| 14 | B pt2 | Drawing 25015-H-NBC-002: "indicate above ground, less than dn22, use pex, larger than dn22 using 316 stainless steel with press fit couplings, I have used pex for less than dn22, and copper for larger than dn22 as talked before , pls do some allowance for the stainless steel , requested from tlink , but they did not provide rate of steel pipe" | Deviation + request to Mitch | **Still open** — Mitch to price/allow copper→316SS delta; no supplier rate held |
| 15 | B pt3 | "assume there are 2 of RHEEM HWU and 1 of hot water pump ( no spec on hot water pump) ... allow Reece rate on HWU and Hot water pump ( reece quote the pump with higher duty )" | Assumption | Actioned as assumption; **still open** — pump spec gap = RFI candidate |
| 16 | B pt4 | "Need to allow for the hanger rods for the pipe work as below , the soil is high active according to geo report" (seismic restraint note 9, dwg 25015-H0002; spec 3.14) | Instruction to Mitch | **Still open** — email says "need to allow"; not confirmed as priced |
| 17 | B pt5 | "Still finalized the fixture quanrirty , but not finished , trade link provide quote of fixture already" (quote 1066143/SP, $252,694.77 ex GST) | Status report | **Still open** — fixture take-off incomplete as at 24 Jul; quote expires 13/08/26 |

---

## Obligations on us

- TCS to carry Reece trench-drain/trash-box package ($164,860.30) as a live but excluded provisional item; decision + exc/quarry add-back required before submission (rows 2, 7).
- TCS pit material basis is a minimum allowance (1 base / 1 "aspro" / 1 cover) — must hold against actual pit schedule/drawing depths (row 11).
- TPS scope per spec VOL 38 s10.1 (quoted in B): "Supply and install all cold water pipes from the existing Authorities water main to all fixtures, fittings and taps requiring cold water. Include for all pipework, bends, offsets, brackets, taps and sundry equipment"; in-ground copper to be sleeved.
- TPS connection/meter works subject to authority requirements and approval — H003 callouts (clipped): assemblies "AUTHORITY'S RE[QUIREMENTS] AND APPROVAL"; connection "TO AUTHORITY'S WATER MA[IN]... ROCKHAMPTON REGIONAL C[OUNCIL]" (= Fitzroy River Water/RRC); 4m x 2m slab for water meter assembly complete with bollards.
- TPS must comply with seismic restraint of non-structural components (dwg 25015-H0002 note 9, AS1170.4) and spec 3.14 fixing/supporting (hanger rods sized against buckling, 2:1 safety margin, galvanised channel, adjustable hangers for fall, sleeves w/ fire-rated packing, no explosive power tools) — cost not yet confirmed as allowed (row 16).
- Water services notes WS1–WS10 (screenshot with pt 2/3) impose: removal/redirection of redundant services (WS1), PEX/316SS material regime (WS2–WS4), NCC hot-water insulation (WS5), GE ZB007 vacuum breakers on external hose taps to AS3500.1 (WS6), reticulation via ceiling space, no longitudinal in-wall runs (WS8), risers/droppers in conduit (WS9), Harsmith 'Fluid Apron' at wall taps (WS10).
- Tradelink quote conditions (if used): prices valid only for delivery by **13/08/26**; indicative delivery schedule required prior to order; storage costs may apply; 20% restocking; non-metro delivery price increases possible (C p.1).

## Conflicts & discrepancies

1. **Pit schedule vs drawings** — "the pit schedule is not consist with the drawing ... items on drawing are more than the pit schedule" (A 24/7 pt2). Take-off based on drawings (higher count). Lump-sum risk; RFI candidate.
2. **Above-ground pipe material** — drawing 25015-H-NBC-002/WS2 requires 316SS press-fit >DN22; priced as copper >DN22 (B pt2). Deliberate deviation "as talked before"; SS allowance outstanding and NO stainless rate held (Tradelink declined to price). Qualification or delta needed.
3. **Kerb chute scope reversal** — 17 Jul pt4 (rock + mat allowed, 56m2) vs 24 Jul pt1 (kerb chute material excluded, "not the work scope"). Later email governs, but wording is ambiguous as to whether the rock/erosion-mat allowance was also stripped; verify spready and state the exclusion in the tender qualifications either way.
4. **VOL 38 s10.1 cold-water table internal ambiguity** (as reproduced in B): duplicate rows give alternative materials for the same location ("In-ground from Boundary Water Meter" = Kembla Copper Type B AND Cromford Blue Stripe PE PN16; "Cold Water Main Runs through building" = Kembla Copper AND Viega Sanpress Inox; rough-in = Kembla Copper Type B AND Rehau Rautitan Platinum; note: "All pipe sizing has been based on copper. If Rehau or Cromford is to be used, then a sizing adjustment must be made..." — clipped). Basis-of-pricing qualification needed.
5. **Tradelink quote entity + address** — quote addressed to **TriCore CIVIL Services Pty Ltd** although fixtures are TPS (hydraulic) scope; project address "544 YAAMBA RD, PARKHURST QLD 4702" vs tender site 554-700 Yaamba Rd, Norman Gardens. Header errors only, but correct entity/address before any order.
6. **Tradelink quote validity 13/08/26 vs anticipated 2027 commencement** — fixture pricing will not survive to construction; escalation risk on ~$252.7k ex GST.
7. **Culvert excavation/bedding** — the 1,883 m average-depth figure includes culverts with no additional allowance; Denis's own question flags likely under-allowance (A 17/7 pt5). Unresolved.
8. **Expected items NOT found in these emails** (do not cite Denis's emails for them): average trench 0.9m x 0.45m; fire main 218m DN125 HDPE + booster + dual pillar hydrant (only a clipped "PROPOSED Ø100mm FIRE WA..." callout appears in the H003 screenshot); pump station ~$545,700 sell. If these figures are in the estimate they originate from another source/conversation, not from these two emails.

## Interfaces (others' work touching ours)

- **Authority (Fitzroy River Water / RRC):** TPS 200mm copper connects existing Authority Ø250 MPVC cold water main to the water meter; H003 callouts (clipped) reference Ø200 cold water connection to Authority's water main, Ø100 fire water assembly + Ø100 cold water assembly subject to Authority's requirements and approval, 4m x 2m water meter slab with bollards.
- **Kerb chutes / concrete kerb / swales:** excluded — treated as civil/earthworks (others') scope per Mitch's direction quoted by Denis; TCS drainage discharges interface with them.
- **100mm subsoil drain (2,173 m):** set aside — typically pavement/court subsoil interfacing with TCS pits; ownership undecided.
- **Trench drains + trash boxes (netball courts):** currently sitting outside both TCS material and excavation pricing — tender brief places netball court trench drains in TCS scope, so if left excluded this is a direct scope gap against the tender.
- **Suppliers:** Reece (trench drain package, HWU, hot water pump), Humes (RCP/RCBC — price amended), Atlan (WSUD filtration — estimate only, model TBC), Tradelink "tlink" (fixtures quote 1066143/SP; declined to rate SS pipe), Kembla (copper).
- **Geotech report:** "soil is high active" drives hanger-rod/support requirement — others' report, our cost.
- **NBC building fitout/structure:** fixture supply interfaces with builder's joinery (Tradelink lines include custom benches, baby change stations — confirm supply-only vs install split); seismic bracing, penetration sleeves and ceiling-space reticulation require coordination with builder's structure and fire-rating.

## Could not verify

- **A PDF p.2:** second "ROCK AND EROSION CONTROL MATTING f..." spready block truncated at page edge; erosion control matting row shows NO legible quantity (only rock 56m2 legible); subsoil spready image cut off after "100mm socked ag pipe" with a partially legible next row reading approx. "MU Step Irons (2?0mm Wide)" — cannot be confidently read.
- **Kerb chute count:** ground-plan table image (A PDF p.3) shows only rows 13-02 to 18-02 "KERB CHUTE 1.000" — table clearly partial; total kerb chute count not verifiable from this email.
- **B PDF p.1:** rate/value columns of copper table clipped in the PDF print (recovered from .msg body instead); drawing 25015-H003 callout texts clipped at right edge (fire/cold water assembly notes incomplete).
- **B PDF pp.2–6:** WS2 note text, s10.1 table note, spec 3.14 items and seismic note 9 lines all clipped at right margin; full wording must be taken from VOL 38 spec / the drawings themselves, not this email. WS1–WS10 screenshot placement makes its parent drawing ambiguous (appears between pt 2 and pt 3; likely 25015-H-NBC-002).
- **"aspro"** (A 24/7 pt2) — Denis's term, presumed precast pit adaptor/converter component; meaning not defined in the email.
- **Hume price amendment** — direction is "change in spready accordingly"; the amount/direction of Humes' amendment is not stated.
- **"measure in yellow"** (B pt1) — the yellow-highlighted 135m route is a graphical measurement on 25015-H003; cannot be independently re-measured from this email.
- **The "spready" (Excel estimate) and "GP" (Groundplan take-off) files are not attached** — every price/quantity above is as reported by Denis, unverified against the live estimate.
- **Attachment C:** cover-letter acceptance line leaves page count blank ("contains ____ pages"); line-item arithmetic of the $252,694.77 total not re-checked line by line.
- Inline images (spec extracts, drawing crops) are partial screenshots; anything outside their crop is unverified.

## Page coverage

- Source A PDF: 5/5 pages read (visual). Source A .msg: full body + headers extracted (extract_msg); 10 attachments listed — all hidden inline images (image001–010.png), no document attachments.
- Source B PDF: 7/7 pages read (visual). Source B .msg: full body + headers extracted; 9 attachments listed — **1066143_ROCKHAMPTON_SPORTS_PRECINCT.pdf (38,312 bytes, the only real attachment)** + 8 inline images.
- Attachment C (Tradelink quote): 7/7 pages read; MD5-verified identical to repo copy at `Material\01 - Project Specific\Fixtures\tradelink\`.
- Total: 19 of 19 pages across the three paginated documents, plus both .msg bodies in full.
