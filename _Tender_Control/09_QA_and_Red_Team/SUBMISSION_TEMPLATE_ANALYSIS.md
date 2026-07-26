# SUBMISSION_TEMPLATE_ANALYSIS — TEN16699 ROK Sports Precinct Stage 1
Run: tender-run-01 · Compiled: 26 Jul 2026 · Author role: QA / red-team (submission-writing basis)
Sources: all 8 files in `TriCore Docs\Submission EXAMPLES\` (6 docx extracted in full — body, tables, headers, footers, via python-docx; 2 testimonial PDFs). Dispositions cross-checked against `_Tender_Control\03_Scope_and_Interfaces\01_SCOPE_MATRIX.md` (matrix) and `CONFLICT_LOG.md` (CL). Evidence keys used below: matrix row refs (e.g. 1A 2.5-x5, L6), CL refs (A1–H5), locked TENDER_PROMPT decisions (§5.x).

---

## 1. STRUCTURE MAP

### 1.1 CQUTafe_CIV SW.docx — MASTER FORMAT, civil package (TCS)

**Section order (exact headings, in order):**
1. Title block (unstyled): `BUDGET QUOTATION` / project name / `Civil Stormwater Drainage Services`
2. Admin table (5 rows × 4 cols): Date · Quote # | Prepared For · Attention | Project · Site Address | Tender Basis · Validity | Submission Type
3. Salutation + one-sentence basis paragraph ("Please find enclosed our tender proposal… based on receipt and review of the issued civil stormwater documentation…")
4. `Tender Value` (H1) — table
5. `Description of Proposed Services and Scope of Works` (H1) — bullets by work area + boundary paragraph
6. `Drawing and Documentation Packages` (H1) — bullets
7. `Work Area Pricing Summary` (H1) — table w/ clarification column
8. `Base Building Allocation Summary` (H1) — table splitting direct works vs allocated prelims/QA
9. `Civil Design / Documentation Basis` (H1) — construct-budget paragraph
10. `Noted Inclusions: Civil Stormwater Drainage Services` (H1) — bullets
11. `Building-Specific Scope Clarifications` (H1) — 2-col table
12. `Provisional Sums and Tender Allowances Included` (H1) — table (Building | Type | Item | Basis | Amount)
13. `Demolition, Isolation and Access Basis` (H1) — Included:/Excluded: bullets
14. `Exclusions / Notes: Civil Drainage & Civil Stormwater Services` (H1) — bullets ("No allowance has been made for…")
15. `Conditions` (H1) — four standing conditions (paragraphs, not bullets — HYD master uses bullets; align on bullets)
16. Closing invitation sentence + signature block

**Header (default, all pages):** table — left cell empty (logo image) | right cell: `CQU Rockhampton TAFE Consolidation - Stage 2 / Civil Stormwater Drainage Tender Proposal`
**Footer (verbatim):** `TriCore Civil Services Pty Ltd | PO Box 7081 Hemmant QLD 4174 | Tel: 07 3390 5803 | tricorecivil.com.au`

**Signature block (verbatim):**
```
Sincerely,
Mitch Hannan
__________________
Mitch Hannan
TRICORE CIVIL SERVICES PTY LTD
ATF THE TRICORE CIVIL SERVICES TRUST
ABN 89 195 291 365
PO Box 7081 Hemmant Q 4174
Tel. 07 3390 5803
tricorecivil.com.au
```
Note: **no QBCC number appears on any TCS example** (CQU CIV, SPS CIV, BACPLAY all omit it). Confirm whether the TCS QBCC licence number should be added for ROK — the TPS master carries one.

**Validity wording:** admin-table cell `Validity | 30 days from proposal date`.
**Pricing tabulation:** 3-col `Description | Basis | Amount` with rows Base Tender Value (ex GST) → Provisional Sums & Allowances (ex GST) → Tender Carry ex GST → GST 10% → Tender Carry inc GST; then per-work-area table with clarification column; then allocation table showing prelims/QA spread into building lump sums ("so that the pricing can be read by building rather than by a separate project preliminaries line").

### 1.2 CQUTafe_HYD.docx — MASTER FORMAT, hydraulic package (TPS)

**Section order:** as CIV master with these insertions/differences:
- After Work Area Pricing Summary table: **ROK092 in-ground allocation call-out table** (single-item breakout: "…included within the ROK092 complete building price and is not an additional cost") and `Temporary Services Allowances Included` (H2) — per-building table.
- `Hydraulic Design` (H1) after Work Area Pricing (D&C-specific — drops for ROK construct-only).
- `Noted Inclusions: Hydraulic Services` (H1); `Building-Specific Scope Clarifications` (H1, table); `Hydraulic Fixtures and Equipment Allowance` (H1, per-building allowance table + pointer to Appendix A); `Provisional Sums and Tender Allowances Included` (H1); `Demolition, Isolation and Access Basis` (H1); `Exclusions / Notes: Hydraulic Services` (H1); `Conditions` (H1, bulleted); signature block; **`Appendix A - Hydraulic Fixture and Equipment Register`** (H1) — no-pricing register table (Building | Qty | Code | Description / Basis | Status) with "Final confirmation required" status flags.

**Header:** table — left cell empty (logo) | `CQU Rockhampton TAFE Consolidation - Stage 2 / Hydraulic Services Tender Proposal` (section 2 linked to previous).
**Footer (verbatim):** `TriCore Plumbing Services Pty Ltd | PO Box 7081 Hemmant QLD 4174 | Tel: 07 3390 5803 | tricoreplumbing.com.au`

**Signature block (verbatim, INCLUDING THE DEFECT):**
```
Sincerely,
Mitch Hannan
__________________
Mitch Hannan
TRICORE PLUMBING SERVICES PTY LTD
ABN 9 620 147 935          ← DEFECT (see below)
QBCC 15100514
PO Box 7081 Hemmant Q 4174
Tel. 07 3390 5803
tricoreplumbing.com.au
```

> **CONFIRMED DEFECT — TPS ABN.** `CQUTafe_HYD.docx` prints `ABN 9 620 147 935` — **10 digits**. Location: signature block, final body paragraphs (the paragraph immediately after `TRICORE PLUMBING SERVICES PTY LTD` and immediately before the `QBCC 15100514` line). Verified in `word/document.xml`: this is the **only** ABN occurrence in the file (headers/footers carry no ABN). Correct ABN is **89 620 147 935** (11 digits) — as printed correctly in `SPS_HYD_Tender_Proposal_Q2381.docx`. The leading "8" was dropped. **Do not reuse the CQU HYD signature block without correcting this. Both ROK submissions' signature blocks must be red-team checked character-by-character against the ABR record.**

**Validity wording:** `Validity | 30 days from proposal date`. Tender basis cell: `Lump Sum D&C - subject to clarifications herein` (ROK: construct-only — use the SPS wording `Lump Sum construct-only — subject to clarifications herein`).
**Pricing tabulation:** simple Tender Value ex GST → GST → inc GST (no PS split line, PS shown as a row inside the Work Area Pricing Summary: `PSUM/ALLOW | Provisional Sums and Tender Allowances`); prices rolled up per building code with a DESIGN line.

### 1.3 SPS_CIVSW_Tender_Proposal_Q2380.docx (13 Jun 2026, TCS)

**Section order:** Title lines → `BUDGET QUOTATION` block → admin table (adds a full-width Project row) → salutation → `Tender Value` (scope-split rows: Scope A / Scope B / Total ex GST / GST / inc GST) → `Description of Proposed Services and Scope of Works` (scope-keyed paragraphs citing pay-table refs) → `Drawing and Documentation Packages` (revision-specific cites) → `Work Area Pricing Summary` (with **Pay Table Ref column**) → `Construct-Only Basis` → `Noted Inclusions` → `Building-Specific Scope Clarifications` (carries builder-query refs Q31) → `Provisional Sums and Tender Allowances Included` → `Exclusions / Notes` (opens with **cross-refer exclusions**: "Bulk earthworks… refer TriCore Civil Earthworks proposal 2379"; "Internal / roof hydraulic stormwater… refer TriCore Hydraulic Services proposal 2381") → `Conditions` → signature block (correct TCS identifiers, as CIV master).
**Header:** none. **Footer:** `TriCore  |  2380  |  Civil Stormwater Drainage Services  |  Page 1`
**Validity:** `30 days from proposal date`. Tender basis: `Lump Sum construct-only civil pricing — subject to clarifications herein`.

### 1.4 SPS_HYD_Tender_Proposal_Q2381.docx (13 Jun 2026, TPS)

Same skeleton as 1.3 plus: `Construct-Only / Documentation Basis` (Form 15 / AS 3500.3:2021 certification cited; "Design changes, performance solutions or re-certification arising after tender are variations"), `Demolition, Isolation and Access Basis` (paragraph form), quantified PS build-ups (concrete cutting: "6 lm saw cutting and 3 hrs tradesman labour per proposed fixture… maximum existing slab depth 100mm"), Appendix A fixture register with **FU (fixture unit) column** tied to the hydraulic drawing table ("37 fixtures / 76 fixture units per H0003").
**Footer:** `TriCore  |  2381  |  Hydraulic Services  |  Page 1`
**Signature block:** correct `ABN 89 620 147 935` but **omits the QBCC line** that the CQU HYD master carries, and the URL is typed `Tricoreplumbing.com.au` (capital T — inconsistent). ROK TPS block should carry ABN (correct) + QBCC 15100514 + lower-case URL.

### 1.5 BACPLAY_Civil_SW.1.docx (30 Jun 2026, TCS)

Same skeleton as SPS CIV; notable content differences: real client/contact in admin table (Xenia Constructions / Jarred Crome — personalised salutation "Dear Jarred"); titled `QUOTATION` not `BUDGET QUOTATION`; highly quantified inclusions (benching method named, grate classes, subsoil tail lengths, crane radius "crane set-up within 10m of truck", HumeFilter install-only split); a full compaction/testing procedure brief inside the exclusions (98% Standard HILF, 30 lm test frequency, within 3m of structures, TriCore ITPs); an unusual PS offered **outside** the tender value ("excluded from the tender value above; may be added if required: supply only of one 300mm wide Class D grate and frame — $3,150 ex GST").
**Defect:** an empty `Heading 1` paragraph sits between the Work Area Pricing Summary and Construct-Only Basis (blank heading artifact — would show as an empty TOC entry; do not copy).
**Footer:** `TriCore  |  2385  |  Civil Stormwater Drainage Services  |  Page 1`. Signature block: correct TCS identifiers.

### 1.6 Limestone Creek - Tender Letter & Methodology.docx (23 Jul 2026 — most recent format)

**A different genre:** letter + methodology + qualifications pack, not a quote sheet.
**Order:** Letterhead lines in body (`TRICORE CIVIL SERVICES PTY LTD` / `9 Ramsay Road, Hemmant QLD 4174 | PO Box 7081 | Ph (07) 3390 5803`) → date → addressee → `RE:` line → intro + one-paragraph capability statement ("Tricore Civil Services is a Queensland-based civil and hydraulic contractor with an established presence in Central Queensland…") → `1. Tender Sum` (package × project matrix table + attachments statement: "A fully priced copy of your Bill of Quantities is attached… together with our rate build-ups so that the basis of every rate is transparent and auditable.") → `2. Basis of this Tender` → `3. Tender Queries` ("twenty matters requiring clarification, six of which we consider material to price… together with the assumption we have adopted pending your response. Where a response alters an assumption, we reserve the right to adjust our price accordingly.") → `4. Validity and Contact` → signature → Attachments list → page break → `SECTION A — CONSTRUCTION METHODOLOGY` (A1 establishment … A9 programme) → `SECTION B — QUALIFICATIONS, CLARIFICATIONS AND EXCLUSIONS` in **four blocks: B1 Basis of Tender / B2 Included / B3 Excluded / B4 Qualifications**.
**Header/footer:** none. **Validity wording:** "This tender is open for acceptance for thirty (30) days from the date of this letter. Supplier quotations underpinning our material rates carry their own validity periods and may be subject to re-quote."
**Defects/notes:** unfilled placeholders `[DATE] [NAME] [POSITION] [PHONE] [EMAIL]` — it is a template, not an issued document; signature line uses `Tricore Civil Services Pty Ltd` (lower-case "c" vs `TriCore` brand elsewhere); no ABN/QBCC in the letterhead or signature — the letter genre still needs the identifier block for ROK. Street address `9 Ramsay Road, Hemmant` appears **only** in this document — confirm current registered/trading address before reuse.

### 1.7 Identifier block reference (for the ROK red-team character check)

| Entity | Correct block per examples | Seen defects |
|---|---|---|
| TCS | `TRICORE CIVIL SERVICES PTY LTD / ATF THE TRICORE CIVIL SERVICES TRUST / ABN 89 195 291 365 / PO Box 7081 Hemmant Q 4174 / Tel. 07 3390 5803 / tricorecivil.com.au` (consistent in CQU CIV, SPS CIV, BACPLAY) | No QBCC number anywhere; Limestone letterhead omits ABN entirely and introduces "9 Ramsay Road" |
| TPS | `TRICORE PLUMBING SERVICES PTY LTD / ABN 89 620 147 935 / QBCC 15100514 / PO Box 7081 Hemmant Q 4174 / Tel. 07 3390 5803 / tricoreplumbing.com.au` (composite of the two HYD examples' correct parts) | CQU HYD: **ABN printed 10-digit `9 620 147 935`** (confirmed, signature block only); SPS HYD: QBCC line missing, `Tricoreplumbing.com.au` capitalisation |

Also noted: both testimonial letters address TriCore at "PO Box **7801**" — the correct box per every TriCore document is **7081** (the error is the letter-writers', harmless, but do not transcribe it).

---

## 2. BEST-PRACTICE DELTAS — ranked adopt-list for ROK

What the newer SPS (Jun-26), BACPLAY (Jun-26) and Limestone (Jul-26) documents do better than the CQU masters, ranked by value to the two ROK submissions:

1. **Tender Query Schedule with adopted-assumption wording (Limestone §3).** "…together with the assumption we have adopted pending your response. Where a response alters an assumption, we reserve the right to adjust our price accordingly." This is exactly the mechanism ROK *requires*: H002 n.15 / VOL38 §3.58 deem un-raised conflicts priced at the larger quantity / more expensive component (CL B4). Every RFI in the Phase 8 schedule should ride in the submission this way, each with its priced assumption stated.
2. **A "Basis of this Tender" section up front (Limestone §2 / B1).** States quantity provenance, rate build-up basis, supplier-quote status and geotech basis before any exclusion appears. ROK needs this to carry: measurement basis (H003 prints no pipe lengths — quantities by scaled measurement, CL C1), priced documentation basis (T1 sheets as modified by RPT006_B §6.1/§9.1 — CL E1), rock regime priced (CL B5), and the stage-split basis (VOL 20 hatch Rev B — matrix header, RFI CL A4).
3. **Cross-referral between sibling proposals with named boundaries (SPS pair).** "Internal / roof hydraulic stormwater and downpipes (refer TriCore Hydraulic Services proposal 2381)" / "Civil stormwater beyond building connection points (refer TriCore Civil Stormwater proposal 2380)." This is the template for the ROK L1/L2 interface statements — but ROK versions must name the exact boundary artefacts (DP "CONNECT TO CIVIL" stubs; F1310 structures; Sch 1A 3.5 cross-refer), since matrix Rule 6 forbids any structure appearing in both submissions.
4. **Pricing presented against the client's own schedule references (SPS Pay Table Ref column).** ROK equivalent: a column of Schedule 3 line refs (1A 2.1-b, 1A 2.5-a, 1B 2.2-b…) in each Work Area Pricing Summary so the builder can transpose without interpretation — and so the entry-mechanics defects (CL A3) get surfaced on our terms.
5. **Four-block qualification architecture (Limestone Section B: Basis / Included / Excluded / Qualifications).** Cleaner than the masters' single exclusion wall: statements of fact (basis), positive scope, negative scope and conditional positions are separated, which is precisely how the matrix distinguishes Base / E+Q / EBC / qualified-N-A rows.
6. **Quantified thresholds instead of adjectives (BACPLAY).** "Dewatering beyond that manageable by a single site dewatering (Flexidrive) pump", 98% Standard HILF + 30 lm test frequency, crane set-up within 10 m. Adjective-based exclusions ("heavy dewatering") are argument bait; ROK should quantify every threshold (but re-base BACPLAY's specific numbers — see E08, E11, E13 below).
7. **Construct-only clause that names the certification artefact (SPS HYD).** "The works will be constructed to the issued, certified documentation (Form 15 to AS 3500.3:2021…). Design changes, performance solutions or re-certification arising after tender are variations." ROK versions cite the T1 set + RPT006_B and the RPEQ/ADAC deliverables we do carry.
8. **Rate-mechanics wording (Limestone B4).** "The provisional item… carries a rate but no quantity… and therefore contributes nothing to the tender sum. It will be valued at the scheduled rate if and when a quantity is directed." Reuse for the $20,000 as-directed provisionals (§5.4, CL A3) and the 4-way rock/unsuitable rate lines (written-direction regime, CL A5).
9. **Catch-all scope confinement (Limestone B3 final bullet).** "Any item not expressly scheduled in the priced Bills of Quantities." Matrix G3 requires exactly this in both ROK submissions against Schedule 3's "Any other works not covered above" line.
10. **Named builder-query trail (SPS Q31/Q33/Q34).** Clarifications carry the builder's own query numbers — adopt for ROK addenda/RFI references so precedence is traceable (APR).
11. **Methodology + capability letter genre (Limestone).** If the ROK returnables call for methodology, Limestone A1–A9 is the vehicle; its one-paragraph CQ-presence capability statement is also the right home for the two testimonials (Section 5).

---

## 3. STANDARD EXCLUSIONS INVENTORY (core deliverable)

Every exclusion / qualification clause appearing in any example, deduplicated across documents, near-verbatim, with ROK disposition. Sources: **CQ-C** = CQUTafe_CIV SW · **CQ-H** = CQUTafe_HYD · **SP-C** = SPS_CIVSW Q2380 · **SP-H** = SPS_HYD Q2381 · **BAC** = BACPLAY · **LIM** = Limestone. Dispositions: **KEEP** (still correct for ROK) / **AMEND** (reword for ROK — reason given) / **DROP** (contradicts a ROK priced inclusion or locked decision) / ADD-NEW rows follow at 3.8.

### 3.1 Design, documentation & approvals

| # | Clause (near-verbatim) | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E01 | "No allowance… for development, submission or fees for applications / approvals with regulatory authorities, except normal coordination and attendance…" | CQ-C, SP-C, BAC | **AMEND** | ITT §16 splits authority work (CL A1, matrix X2): TPS must exclude **RRC plumbing lodgement specifically** (a flagged departure from tender clauses — add-price carried), and merely *record* FRW Private Works Application lodgement + water/sewer connection completion as Principal Contractor **as written**. Never write "all approvals excluded". Connection fees ride the $20,000 as-directed provisionals (§5.4), reimbursed at cost — say so. |
| E02 | "No allowance… for professional design responsibility, redesign, workshop drawing design responsibility or professional indemnity. This proposal is a construct budget based on the current issued design information, with as-constructed documentation only." | CQ-C, SP-C, BAC | **AMEND** | Construct-only core survives (matrix X4), but three ROK carve-outs: (a) shop drawings excluded as a **flagged departure** from H002 n.2 with add-price (X1); (b) seismic restraint — install to the specified system priced, restraint **layout drafting only**, no engineering design liability (CL C7); (c) do not let "documentation only" read against the priced as-cons/ADAC/RPEQ deliverables (item 1.6). |
| E03 | "Design changes, performance solutions or re-certification arising after tender are variations." | SP-H | **KEEP** | Directly reusable; pair with T1+RPT006_B priced-basis statement (CL E1). |
| E04 | "No allowance… for Level 1 survey certification, ADAC or third-party survey as-constructed documentation." | CQ-C, SP-C, BAC (expanded: survey conduit, surveyor engagement) | **DROP** | Contradicts priced inclusions: Sch item 1.6 both stages — each entity delivers **ADAC XML, RPEQ certification and CCTV for its own assets** (ITT §19; VOL38 §3.56). Replace with: "primary control survey by others; trade set-out from Principal-supplied control included" (matrix 1.5). |
| E05 | "Development of coordinated multidisciplinary penetration plans is excluded. Hydraulic penetration inputs, sizes and mark-ups for our scope are included." | CQ-H, SP-H | **KEEP** | TPS both buildings; unchanged. |
| E06 | "Professional indemnity/design insurance for the hydraulic design component is to be carried by the engaged hydraulic consultant." (D&C design section) | CQ-H | **DROP** | ROK is construct-only — the whole `Hydraulic Design` section and its insurance clause do not apply; X4 wording replaces it. |

### 3.2 Ground conditions & excavation

| # | Clause | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E07 | "No allowance has been made for excavation, removal, delay or replacement costs arising from rock / unrippable material." | CQ-C, SP-C, BAC, CQ-H (bundled), LIM B3 | **AMEND** | **Rock is geotech-answered at ROK** — NQL2024-0320 read in full: 25/36 test locations refused, shallowest 0.70 m (CL H1). A blanket rock exclusion is non-conforming: H002 n.24 **mandates** tendered extra-over rates (soft AND hard × trenches AND pits = 4 rates per entity, own excavations only — matrix 7.0-a/1B 5.0-a). Replace with: rates tendered; extent of bore-log rock deemed included stated precisely; the three inconsistent regimes (ITT §18.2 written-direction vs VOL38 §7.7 deemed-included vs n.24) named and RFI'd with the priced regime stated (CL B5/A5). |
| E08 | "Unrippable material defined as existing product not capable of being excavated/ripped via an 8T hydraulic excavator at design depths." | BAC | **DROP** | Do not copy — TEN16699 defines rock against a **20–30 t excavator with ripper** (CL A5). Importing the 8T definition would contradict the tender definition and void the rate schedule's meaning. |
| E09 | "Rock excavation — Provisional Sum only, aligned to Pay Table PS1.0.07." | SP-C | **AMEND** | The client-mechanism-alignment pattern is right; the instrument is wrong for ROK — align to the Schedule 3 §18 rate lines (extra-over rates as directed), not a PS. |
| E10 | "No allowance has been made for heavy dewatering / groundwater management." | CQ-C, SP-C | **AMEND** | Adjective "heavy" is argument bait — adopt the BACPLAY quantified-threshold form (E11) with ROK-checked thresholds; note VOL38 §7.11 deems water-charged bedding included (three-regime RFI, CL B5); perched water triggers 3H:1V/benching per geotech (CL H2). |
| E11 | "No allowance… beyond that manageable by a single site dewatering (Flexidrive) pump; dewatering requirements beyond this are by the builder." / "Dewatering beyond nominal, including wellpointing or sustained groundwater control." | BAC, LIM | **AMEND** | Best-in-class form — keep the quantified threshold, restate against ROK geotech findings and the §7.11 conflict; state which regime is priced. |
| E12 | "No allowance… for the treatment or removal of contaminated spoil, excess spoil, asbestos, PASS or other regulated material." | CQ-C, SP-C, BAC, CQ-H | **AMEND** | **EMR §17.9 + Addendum 2 change the geometry: no spoil leaves site** (matrix 1.3; CL E5). "Removal from site" wording is now wrong both ways — there is no off-site disposal to exclude, and on-site stockpiling to directed locations must be included. Reword: contamination testing/treatment/classification excluded; unexpected-finds regime per EMR; spoil (including unsuitable) stockpiled on site at Principal-directed locations; off-site disposal neither required nor priced. |
| E13 | "Site-won material is assumed suitable for general backfill where reused." (+ BAC 98% HILF version "use of excavated, site-won material expected suitable…") | CQ-C, SP-C, BAC | **AMEND** | Geotech kills the assumption: site-won high-plasticity clay is **unsuitable for reuse without treatment**, imported fill recommended (CL E5/H4); dispersion/soil-class behaviour is geotech-answered — assumption-based boilerplate must give way to the evidence-based position: imported bedding/backfill priced, unsuitable site-won stockpiled on site (per E12). Keep BACPLAY's compaction-procedure brief but conform it to the adopted compaction spec (VOL38 §3.62 internal conflict → RFI, CL C6). |
| E14 | "No allowance has been made for trench shoring or shielding — installation is via benching excavation method." | BAC | **DROP** | Geotech §5.3.3 batter rule is verified as **1.5H:1V for excavations under 2 m** with personnel entry (CL H2) — an unshored/benched-only basis is non-conforming at ROK. Replace with the ADD-NEW batter/shield basis statement (N6); Director option (shields vs batter widening) feeds Phase 6/7 pricing. |
| E15 | "Rock excavation, excavation in unsuitable material, and disposal of contaminated material [excluded]." | LIM B3 | **AMEND** | Split three ways per above: rock → E07 rate regime; unsuitable → mirror ITT §18.1 **written-direction** regime in the rate wording (CL A5; matrix 7.0-b); contaminated disposal → E12 on-site regime. |
| E16 | "No geotechnical report has been issued… Our pricing assumes excavation in ordinary material." | LIM §2/B4 | **DROP** | The opposite is true at ROK — NQL2024-0320 issued and read 184/184. Any assumed-ordinary-material wording is falsified by our own documents basis and would poison the rock-rate position. Replaced by N5/N6. |

### 3.3 Reinstatement, surfaces & adjoining trades

| # | Clause | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E17 | "Excluded: demolition and reinstatement of existing concrete, asphalt, pavements, pavers, gardens, landscaping, kerbs, hardstand and external finished surfaces…" / "final reinstatement of external footpaths, verges, pavements… backfill, compact and make safe only." | CQ-C, CQ-H, SP-C, BAC | **KEEP** | Pavements, kerb, landscaping are Not Ours by trade (matrix 2.3-c…h, 2.6). Trench-reinstatement-to-make-safe-only remains the right boundary; greenfield, so the "existing surfaces" flavour is light-touch. |
| E18 | "No allowance for hardstands, slabs, plinths or concrete surrounds outside the direct [package] structures specifically measured in this proposal." | CQ-C, SP-C, BAC | **AMEND** | Correct as default, but ROK priced concrete must be carved in by name: TPS — 4 m × 2 m meter slab + bollards (matrix 2.1-c, L7); TCS — 50 m concrete spillway, culvert outlet structures, headwalls (2.5-x4); bubbler/DF unit slabs and surrounds stay by others (1B 4.5-c). |
| E19 | "No allowance for imported backfill, CBR, roadbase or final trench pavement materials, excluding normal bedding / surround gravels." | CQ-C, SP-C, BAC | **AMEND** | Imported bedding/backfill **is priced** at ROK (spoil regime, E12/E13); the exclusion narrows to pavement-box materials (CBR/roadbase as final trench seal) only. Gomersall Rd/Council fill quality by others (CL H5). |
| E20 | "No allowance for civil earthworks, cut / fill, swale drains, bio basins, erosion / sediment controls, pavements, hardstands, kerb / channel, retaining wall drainage or other general civil siteworks." | CQ-C (BAC variant) | **AMEND** | Must be unbundled — one limb now contradicts a priced inclusion: **ESC local to our own open trenches is Base scope for both entities** (matrix 1.3); only the site-wide ESMP (DA Cond 6) is by the Principal Contractor. Swales (2.5-x1) and bio-basin media/planting (2.5-x2, L11 — "TCS stops at structural backfill of its own pipes, pits, spillway and outlet structures") stay excluded but with the defined interfaces stated. Bulk earthworks Not Ours (trench/pit excavation is inside each Base line — matrix G1). |
| E21 | "No allowance… for any agg or subsoil drainage to retaining walls or kerbs, etc. (subsoil tails to the upstream of pits are included…)" | BAC (CQ-C subsoil limb) | **AMEND** | The excluded thing changed shape at ROK: subsoils re-nominated as **type 2 strip filters** (RPT006_B §6.1, CL F5). Qualification must name the strip-filter system "by others" and fix the interface: connections accepted **at TCS collector pits only — pit wall penetration** (matrix 2.3-x2/2.5-x3, L12). |
| E22 | "No allowance… for supply or installation of channel trench grates or frames (formed and installed by the concreter)…" (+ CQ-C "final placement / forming up / setting… by concreter / pavement contractor") | BAC, CQ-C | **DROP** | Contradicts a locked priced inclusion: Sch 1A 3.5 grated trench drains are **TCS Base in full** — GT1–GT4 + GT7–GT9 (561.9 m) incl. trash boxes, connection pits, **excavation and quarry** (matrix 3.5, L1); GT5/GT6 (46.6 m) priced in 1B 2.3-a. TPS's submission carries the mirror-image cross-refer exclusion instead (L1). |
| E23 | "No allowance for stormwater treatment devices or filter products other than [named PS]…" (+ BAC: HumeFilter chamber install allowed, supply by others; "Jellyfish, gully enviro pods, stormsacks etc." excluded) | CQ-C, SP-C, BAC | **DROP** | Contradicts the locked WSUD treatment: 22 no. Ocean Protect StormFilter cartridges O.A.E. — **supply + delivery as PC Sum +15%, installation (excavation, bedding, cranage, placement, connection, backfill) inside the TCS lump sum, not separately exposed** (matrix 2.5-c, L3). Replace with that PC-sum statement plus one retained limb: WSUD maintenance beyond DLP excluded (CL E2). BACPLAY's install-only crane/radius drafting is the right *style* for the installation description. |
| E24 | "No allowance… for the supply of pit filter baskets, inlet protection or proprietary inlet inserts." | BAC | **AMEND** | Trash boxes per the F1320 GT schedule (~29 no.) are priced (CL D7); the exclusion survives only for proprietary inserts *beyond* the documented trash boxes. |
| E25 | "No allowance for electrical components, power, controls, telemetry, BMS, level sensors, alarms or accessories required for pump stations, GPTs or other proprietary devices…" | CQ-C, SP-C, CQ-H (partial) | **AMEND** | Keep the default, with two ROK edits: (a) VOL38 §24.1.2 puts **pumps-to-panel wiring inside the hydraulic subcontract** — carve in for equipment TPS actually carries; (b) the sewer pump station itself is excluded on Addendum 2 with the full L6 interface list (see N1) — the generic device-exclusion must not be the only place the station is mentioned. |
| E26 | "No allowance… for supporting, adjusting, relocating or fees associated with authority services and other utilities, including Energex, communications, gas and similar services." (+ BAC "TriCore to coordinate and manage only") | CQ-C, SP-C, BAC | **KEEP** | Unchanged; BACPLAY's coordinate-and-manage-only tail is the better version. |
| E27 | "No allowance has been made for traffic or pedestrian permits, approvals, management or controls." (+ SP-C "Traffic control and traffic management (including for Turbine Rd works) — by others"; LIM) | CQ-C, BAC, SP-C, LIM | **AMEND** | Partially contradicts Base scope: each entity **includes traffic control for its own works and deliveries** (matrix 1.2). Exclusion narrows to the site-wide TMP (DA Cond 7 — Principal Contractor) and public-road permits. |
| E28 | "Vacuum excavation is excluded." / "No allowance has been made for vacuum excavation." | CQ-C, CQ-H, SP-H, BAC | **AMEND** | The VFMP makes **water/non-destructive excavation within tree NRZs a priced obligation** for both entities (CL G: AQF5 arborist supervision, water excavation in NRZs, root guards near sewer lines). Exclusion survives only outside NRZs / for third-party locating scopes. |
| E29 | "No allowance has been made for disconnection of existing non-[package] services." | CQ-C, SP-C, BAC | **KEEP** | Greenfield; harmless and still correct. |
| E30 | "No allowance for delays, alterations or additional works if existing service locations / depths / levels differ from supplied drawings or undocumented clashes are encountered… TriCore to notify and detail any clashes/errors… for instruction." | CQ-C, BAC, CQ-H, SP-H | **KEEP** | Keep with the BACPLAY notify-for-instruction tail. Note VOL38 §9.22 joint sewer locate is a template leftover — RFI to confirm N/A (CL B9). |
| E31 | "Builder's works in connection, architectural openings, access panels, hatches, cupboards/recesses, plinths, slabs, bollards, plant screens, roof works, gutters, downpipes and waterproof membranes are excluded unless specifically noted as included." | CQ-H, SP-H | **AMEND** | Roofing/roof plumbing/gutters/DPs are a locked §5.3 exclusion, but the bare list is not enough at ROK — the wording must carry the **boundary chain**: roofer/builder owns gutters and DPs to the DP "CONNECT TO CIVIL" point; TPS owns the in-ground connection stubs only as drawn on the hydraulic sheets; TCS owns everything on the civil sheets onward (matrix 4.3/1B 3.3, L2/L14). PAM sheets show **no** connect-to-civil note and DP counts mismatch — RFI'd (CL C8); wording must survive that gap. |
| E32 | "No allowance has been made for any plumbing / hydraulic services, including roofwater pipework / roofwater drainage and downpipes…" (civil-package mirror) | CQ-C, BAC | **AMEND** | TCS mirror of E31 — must state the **corrected POD boundary**: ALL F1310/civil-sheet structures and drainage — including lines 81/83/87 in full — are TCS with no carve-out; TPS ends at the hydraulic-sheet DP stubs (matrix 2.5-x5, Appendix C-1, L2). Wording must not push building-stormwater connections back onto TPS or exclude the connection INTO civil pits. |
| E33 | "Civil stormwater beyond building connection points (refer TriCore Civil Stormwater proposal 2380)." / "Internal / roof hydraulic stormwater and downpipes (refer TriCore Hydraulic Services proposal 2381)." | SP-H, SP-C | **KEEP** | The cross-refer pattern is mandated at ROK (L1/L2; Rule 6 double-count control). Update artefact names: Schedule 3 line refs + drawing callouts, both directions, both stages. |
| E34 | "Supply, certification and responsibility for [prefab] internal plumbing is by others. TriCore includes connection and commissioning only." | CQ-H (ROK076) | **KEEP** | Keep as a pattern — direct ROK use: external BBQs have no documented water/waste supply, TPS carries nothing + RFI so H002 n.15 silence cannot bite (matrix 1B 4.5-b, G8); bubbler units PC Sum installed by TPS, slabs by others (1B 4.5-c). |

### 3.4 Fire & metering (TPS)

| # | Clause | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E35 | "Electrical fire and dry-fire systems are excluded, including FIP/FDCIE/EWIS, detectors, MCPs, WIPs, speakers, bells, VADs, ASD, fibre, networking, fire alarm cabling, terminations, programming and cause/effect." | CQ-H, SP-H | **KEEP** | Verbatim reuse for TPS. |
| E36 | "Portable extinguishers, fire blankets, portable signage and all sprinkler systems are excluded…" | CQ-H, SP-H | **AMEND** | Sprinkler limb keeps. Extinguisher limb changes: VOL38 §14.1 says the plumber prices FE supply/install, its own note says builder generally provides; NBC shows 8×FE unallocated — ROK carries **FE supply as Excluded-But-Costed + RFI, stated in the submission** (matrix 4.11-d/1B 3.11-d, CL B8). FHR + FB are priced; **12-month AS1851 maintenance/tagging is priced** (VOL38) — say so, or the exclusion list implies otherwise. |
| E37 | "Site-wide water, sewer, stormwater or fire system testing, reconfiguration, augmentation or authority-driven upgrade beyond the documented scope and named allowances is excluded." | CQ-H, SP-H | **KEEP** | Keep, and pair with the fire-extent qualification: extent not verifiable from H003 (no lengths, no legible symbols) — priced to scaled measurement + AS2419.1 coverage check, extent qualified + RFI (matrix 2.4-c, CL C1/F3). |
| E38 | "AMR/BMS/electronic/smart metering systems, meter head-end/software, BMS graphics, programming, trending, alarming and integration are excluded beyond local equipment terminals/contacts where included." | CQ-H, SP-H | **KEEP** | Verbatim reuse. |
| E39 | "Cold water meters are carried to each building only as a provisional sum. AMR/metering system components are excluded." | CQ-H, SP-H | **AMEND** | ROK meters sit in **Base**, twice-structured: primary metering at the H003 meter slab (1A 2.1-c) and NBC/PAM Ø32 **check**-meter assemblies (4.11-c/3.11-c) — boundary at the building entry isolation point, each assembly priced exactly once (CL C11, L8). Drop the PS treatment; keep the AMR limb; PAM missing PRV → RFI (CL C8). |

### 3.5 In-building (TPS)

| # | Clause | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E40 | "Slab scanning/x-ray, structural approvals for coring and remedial works arising from concealed structural/services conditions are excluded." | CQ-H, SP-H | **KEEP** | New-build; low heat; keep. |
| E41 | "Drainage articulation is included as swivel/expansion entering the building footprint only. Strapping to slab and expansion treatment to every riser are excluded unless later directed and priced." | CQ-H, SP-H | **DROP** | Contradicts the ROK priced inclusion: articulation to geotech class H1/"P" **increased provisions** is Base — swivel/expanda joints, combo joints, lagging, DP expansion joints at ≤6 m (matrix 4.11-c/3.11-c; CL G; RPT006 §14.3). Replace with a positive inclusion statement of the H1/"P" articulation regime. |
| E42 | "Excluded: access, repairs and reinstatement to existing ceilings, ceiling tiles, walls, linings, joinery, waterproofing, tiling, painting and architectural finishes, except direct passive fire stopping and service penetration sealing expressly carried in our scope." | CQ-H | **KEEP** | Keep (light relevance — new builds); the passive-fire carve-in tail is good drafting. |
| E43 | "Supply of temporary fixtures, fountains, pumps, tanks or temporary appliances is excluded. Temporary service allowance is limited to typical connection material only." | CQ-H, SP-H | **AMEND** | ITT §17.3: **no site power or water is provided** — each entity prices its own generators and temporary potable water storage + distribution in full, nothing shared, sized for a standalone 1B award (matrix 2.2-b/1B 2.1-a, L5). The connection-materials-only model understates a real priced obligation — reword as a positive prelims inclusion with its own boundary. |
| E44 | "Non-hydraulic FF&E items such as grab rails, baby change tables, mirrors… are excluded unless specifically identified as a plumbing component." (+ fixture allowance framing) | CQ-H | **AMEND** | Keep the non-hydraulic FF&E limb. Fixture treatment changes: **supply = completely separate PC line, Tradelink quote 1066143/SP + 15%; installation labour in Base** (locked §5.3; matrix 4.12-c/1B 3.12-a). Add the F4 qualifications: quote expires 13/08/26 vs 2027 commencement (escalation/validity), header address defect, quantities unfinalised — Phase 4 counts. **Rule 4 fixture test: never write "fixtures included" beyond what the PC line covers.** |
| E45 | "Any post-tender scope growth, redesign of other disciplines, changes arising from final room layouts, equipment changes, authority comments, certifier requirements or undocumented existing conditions are excluded unless instructed and valued as a variation or covered by a named provisional sum." | CQ-H, SP-H | **KEEP** | One of the masters' best clauses — verbatim reuse in both submissions. |

### 3.6 Programme, hours & access

| # | Clause | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E46 | "No allowance has been made for out-of-hours works. Work hour basis: 06:30 AM to 4:30 PM Monday to Friday." (+ LIM: "Liquidated damages, acceleration costs, and out-of-hours or weekend work [excluded]") | CQ-C, SP-C, BAC, LIM | **KEEP** | Keep hours basis; note internally that the VFMP 6 pm–6 am machinery curfew near retained trees sits inside these hours anyway (CL G). LD/acceleration limb: check against executed-contract terms before adopting verbatim. |
| E47 | "Unless agreed otherwise, prices are based on completion of the works in sequence during a single logical mobilisation." | CQ-C, SP-C, BAC | **AMEND** | ROK is two standalone stages with **1B-alone viability required** (§5.2) and ROK FIFO supervision (matrix 1.7). Restate per submission: works in sequence within the tendered stage on continuous released work fronts; remobilisation beyond the tendered basis chargeable. Pair with the programme-basis qualification (E51/N8). |
| E48 | "Access is assumed to be clear and coordinated by the builder with normal working-hour access and logical work fronts… Restricted access, staged access delays, after-hours works or multiple remobilisations outside the tender basis are excluded." | CQ-C, CQ-H, LIM A9 | **KEEP** | Keep; matrix already assumes builder-coordinated fronts. Access via Norman Rd only, no CQU access (matrix 1.1) — worth one factual line. |

### 3.7 Commercial conditions & validity

| # | Clause | Source | Disposition | ROK reasoning |
|---|---|---|---|---|
| E49 | "Title of all works, including consumables, remains the property of [entity] until payment has been received in full." | CQ-C, CQ-H, SP-C, SP-H, BAC | **KEEP** | Standing condition, both entities (correct entity name per submission). |
| E50 | "Due to supply/manufacturer price securement and procurement requirements, reasonable claim may be made for major project materials procured and delivered to site or otherwise secured for the project." | all TriCore-format | **KEEP** | Keep — materially important given 2027 start and quote validities (F4). |
| E51 | "Extension of time and associated costs may apply for wet weather, latent conditions, design changes, authority changes, restricted access, shutdown constraints, public holidays, Christmas shutdown, third-party interruption or circumstances outside TriCore control." | all TriCore-format | **AMEND** | Collides with ITT §20.h — only **5 days combined weather + latent** programme allowance (CL A6), unrealistic for CQ wet season/2027. Keep the clause but add an explicit programme-basis qualification stating the allowance carried and reserving position beyond it. |
| E52 | "This tender is open for acceptance for thirty (30) days… Supplier quotations underpinning our material rates carry their own validity periods and may be subject to re-quote." | LIM (30-days-flat in all others) | **AMEND** | Adopt the Limestone two-part form and extend: Tradelink fixture quote expires 13/08/26 against a 2027 commencement — escalation and re-quote rights must be explicit (CL F4). |
| E53 | "[Head contractor]'s subcontract terms, programme, retention, insurance and back-charge provisions have not been sighted and are not reflected in this pricing." | LIM | **AMEND** | ROK contract terms ARE sighted — convert to targeted qualifications: **10% of hydraulic contract value withheld until final as-builts/O&M approved** (VOL38 §4.4.1(3) — cashflow QUAL, CL B3); §20.h programme cap (E51). The not-sighted form survives only for genuinely unsighted documents → N9 (VOL 35; RRC addenda 1–6). |
| E54 | "Any item not expressly scheduled in the priced Bills of Quantities [is excluded]." | LIM B3 | **KEEP** | Adopt in both submissions (recast to Schedule 3/pricing-summary language). Required by matrix G3 against the "Any other works not covered above" catch-all line — Rule 4's backstop. |
| E55 | "Quantities are those stated in [the builder's] issued Bill of Quantities… rates are applied to the stated quantities only, and the works should be remeasured and valued at the scheduled rates." | LIM B1 | **KEEP** | Keep as the pattern for every rate line; ROK lump-sum lines instead carry the measurement-basis statement (H003 no lengths → scaled quantities, CL C1) in the Basis section (N9). |
| E56 | "The provisional item… carries a rate but no quantity in the issued Bill of Quantities, and therefore contributes nothing to the tender sum. It will be valued at the scheduled rate if and when a quantity is directed." | LIM B4 | **KEEP** | Reuse for: $20,000 connection-fee provisionals carried **as directed, not re-priced** (§5.4; entry-mechanics RFI CL A3) and the 4-way rock/unsuitable rate lines (written-direction regime, CL A5). |
| E57 | "The Water RFQ references SEQ Water standards; the project falls within Livingstone Shire Council. Tricore has priced to CMDG. Confirmation of the applicable standard is requested…" | LIM B4 | **KEEP** (pattern) | The named-standards-mismatch qualification is exactly the ROK template-contamination treatment — see N14 for the ROK instance (NSW/VIC/NT template leftovers → priced to QLD/RRC/FRW framework). |

### 3.8 ADD-NEW — gaps the examples never covered that ROK needs

| # | New clause required | Basis |
|---|---|---|
| N1 | **Sewer pump station exclusion citing Addendum 2** ("Sewage Pump Station will be getting installed by Council") with the full interface list stated verbatim so "pump station excluded" cannot be read as excluding the connecting works: TPS carries the gravity sewer to and terminating at the station inlet DICL pipe piece ("LIMIT OF Q-MAX WORKS"); station supply/install, excavation and slab by Council/others; electrical supply, controls and commissioning cabling by the electrical trade. Cite Add 2 as governing over both documented stations (H003/VOL17 QMax vs VOL38 §24 Sulzer — CL B1). | Matrix 2.1-x1, L6; APR Add 2; CL B1/C5 |
| N2 | **Sewer rising main — excluded and qualified, add-price carried.** Discharge location "to be confirmed and coordinated", no tie-in shown; ownership ambiguous once Council installs the station. Wording must prevent the builder deeming it inside the sewer-mains line; RFI. | Matrix 2.1-x2; CL C4 |
| N3 | **Watermain material departure statement:** base offer Ø200 ID HDPE PE100 SDR11 — selected **within the specification's own §10.1 equivalence table**, therefore not a substitution under the §27 HK Solutions process; **no buried Type B copper alternate offered**. | §5.5 four-leg; matrix 2.1-c; CL B10 |
| N4 | **316 SS both-ways pricing statement:** conforming tendered sum = 316 stainless press-fit >DN22 + PEX ≤DN22 per WS2; copper priced as a clearly labelled alternate. Applies NBC and PAM. | §5.5; matrix 4.11-c/3.11-c; CL C9 |
| N5 | **Rock rate schedule statement:** four extra-over rates per entity (soft/hard × trench/pit), applying to that entity's own excavations only; extent of bore-log rock deemed included stated against NQL2024-0320 (25/36 refusals, shallowest 0.70 m); the three inconsistent regimes named, the priced regime stated, RFI raised. | Matrix 7.0-a/b, 1B 5.0-a/b; CL A5/B5/H1 |
| N6 | **Batter/shield basis statement:** geotech §5.3.3 requires 1.5H:1V batters for excavations under 2 m with personnel entry (3H:1V/benching at perched water, or shoring); tendered basis states which (trench shields for entered runs vs batter widening — Director option) so the trench profile priced is on the record. | CL H2; Phase 6/7 |
| N7 | **Spoil regime clause:** no spoil to leave site (Addendum 2; EMR §17.9); unsuitable/surplus stockpiled on site at Principal-directed locations; imported bedding/backfill priced; Council/imported fill quality by others (Gomersall Rd stockpile untested — Add 1 follow-up never issued). | Matrix 1.3; CL E5/H5; APR |
| N8 | **EDQ condition programme gates:** EDQ Conditions 16/17 impose 20-business-day review windows before stormwater commencement; lawful discharge point is a creek on CQU land with **no land agreement in place** — carried as a programme gate/qualification, expressly not a risk we price or solve. | CL E3 |
| N9 | **Documents-basis statement (unsighted + defective documents):** VOL 35 not sighted; **RRC addenda 1–6 unsighted** (numbering starts at Add 7 in our set); H004 referenced twice by H003 but never supplied; priced basis = T1 drawing set **as modified by RPT006_B §6.1/§9.1** (100%DD changes never reissued into T1); quantities for unscaled hydraulic sheets by scaled measurement. | CL C1/C2/E1; APR |
| N10 | **Trade waste application + grease arrestor:** trade waste application excluded as EBC + RFI (VOL 21 silent despite canteen; H002 n.25 assigns it to TPS); arrestor hardware carried as PC/allowance pending size resolution (1500 L drawing / 2000 L report / 550–5000 L spec). | Matrix X3; CL A2/B6 |
| N11 | **Shop drawings excluded — flagged departure.** Direct departure from H002 n.2, declared as such with add-price carried; as-cons/ADAC drafting expressly distinguished and retained. | Matrix X1; §5.3 |
| N12 | **Seismic restraint statement:** AS1170.4 EDC 2 restraint installation to the specified system is priced; TPS provides restraint **layout drafting only** — no engineering design liability inside a construct-only package. | Matrix X4; CL C7 |
| N13 | **Maintenance + retention terms:** 12-month maintenance of works including AS1851 fire tagging is priced (VOL38); qualification against §4.4.1(3) 10% withheld-until-as-builts (cashflow). | CL B3/G |
| N14 | **Template-contamination clause (one narrow sentence):** works priced to the QLD/RRC/FRW statutory framework and the nominated-equipment schedules, which govern over interstate template text (NSW EP&A, VIC signage/Legionella, PAM sheet's NT Building Regulations note); non-potable/lilac hydrant contradiction RFI'd. | CL B2/C8 |
| N15 | **Stage-split and standalone-award statements (both submissions):** works inside the Stage 1A hatch on VOL 20 SE_12306_SKT_CMP Rev B priced in 1A, 1B hatch in 1B (consequences named: detention basin + WSUD manhole = 1A; GT5/GT6 = 1B), hatch boundary RFI'd; the 1B "Retention Basin" line carried unpriced with an explicit qualification (no second basin documented — priced once in 1A); each stage tender is standalone and viable if awarded alone (§5.2). | Matrix header, 2.5-b, 1B 2.3-b, G2; CL A4 |

**Inventory counts: 22 KEEP · 26 AMEND · 8 DROP (E04, E06, E08, E14, E16, E22, E23, E41) · 15 ADD-NEW.**
Note: no example clause excludes seismic restraint, WSUD supply, or ADAC by *name and intent* for this project — the DROP rows are where an example clause as-worded would collide with a ROK priced inclusion or locked decision if pasted forward. Every DROP row has its replacement identified above.

---

## 4. TONE NOTES

### 4.1 Confident, economical wording worth reusing verbatim / near-verbatim

- "Tender value is submitted as a lump sum excluding GST and is subject to the inclusions, exclusions, clarifications, provisional sums and allowances stated in this proposal." (CQU masters — the single-sentence frame for everything that follows.)
- "Works are priced strictly in accordance with the current design details and measurable documentation." (CQU CIV — "measurable" is the load-bearing word; keep it.)
- "This tender is construct-only. No design services, design development or professional indemnity for design are included… Design changes, performance solutions or re-certification arising after tender are variations." (SPS HYD.)
- "…carried as a named provisional sum." / "Allowance is limited to…" (CQU HYD — the named-and-limited pattern keeps every allowance bounded.)
- "TriCore to notify and detail any clashes/errors to the principal contractor/engineer for instruction." (BACPLAY — obligation stated as cooperation, not refusal.)
- "…so that the basis of every rate is transparent and auditable." (Limestone — auditable-basis framing suits the ROK Schedule 3 ref column.)
- "Where a response alters an assumption, we reserve the right to adjust our price accordingly." (Limestone — the RFI-assumption hinge.)
- "It will be valued at the scheduled rate if and when a quantity is directed." (Limestone — exact fit for the ROK rate lines and $20k provisionals.)
- "Rates are built from first principles — labour, plant, materials, preliminaries, overhead and margin — from Tricore's current Central Queensland cost base." (Limestone — regional-capability signal relevant to a Rockhampton job.)
- The Included:/Excluded: paired-bullet form of the masters' "Demolition, Isolation and Access Basis" section — the cleanest boundary-drafting device in the set.

### 4.2 Do-not-copy — wording that violates ROK Rule 4 discipline (or a locked decision)

| Offending wording | Source | Why it fails at ROK |
|---|---|---|
| "Supply and installation of **complete hydraulic services** on a construct-only basis, comprising: …" | SPS HYD scope | "Complete" is a deemed-inclusion hook. ROK scope sentences must enumerate and close: "necessary to deliver the **included** [package] scope **only**" (the CQU masters' own formula) — never "complete system"/"all hydraulic services". |
| "**All** pit, pipe, culvert, headwall and outlet works as documented…" | SPS CIV inclusions | "As documented" bounds it, but "all" + a defective document set (141 structures vs 121 in F1310; C09A/B detailed nowhere — CL D1) = priced-at-larger-quantity exposure. Enumerate: structures per the adopted basis (layouts + F1321 + long sections), counts stated, C09A/B RFI'd. |
| "…included within the ROK092 **complete building price** and is not an additional cost." | CQU HYD allocation table | "Complete building price" invites the builder to sweep unlisted building scope in. Say "included within the ROK092 building price for the scope stated herein". |
| "In-wall domestic water rough-ins are allowed as PEX. **Mains and remaining domestic water services are allowed as copper** unless otherwise detailed…" | CQU HYD inclusions | Contradicts both ROK locked material positions: Ø200 HDPE PE100 SDR11 mains with no buried copper alternate (N3) and 316 SS press-fit >DN22 + PEX ≤DN22 with copper only as a labelled alternate (N4). Do not let this sentence migrate. |
| "Unrippable material defined as… 8T hydraulic excavator…" | BACPLAY | Contradicts the TEN16699 rock definition (20–30 t excavator with ripper — CL A5). |
| "No geotechnical report has been issued… assumes excavation in ordinary material." | Limestone | Falsified at ROK; poisonous to the rate-schedule position if pasted. |
| "We have priced the works **in full**…" | Limestone letter | Tolerable there only because B3's catch-all closes it; at ROK prefer "We have priced every item allocated to us under the enclosed pricing summary" — Rule 4 wants the universe defined by the list, not by "in full". |
| Blanket ADAC/as-cons survey exclusion; blanket trench-drain-by-concreter; blanket treatment-device exclusion; articulation-limited-to-footprint | CQ-C/BAC/CQ-H/SP-H | The four DROP families of Section 3 — each now contradicts a ROK priced inclusion (item 1.6 ADAC/CCTV; Sch 1A 3.5; WSUD install; H1/"P" articulation). |

Rule-4 drafting rule for both ROK submissions: every scope sentence names its boundary artefact (drawing callout, schedule line, flange, pit wall, stub) — the examples that do this (BACPLAY, SPS cross-refers) never argue; the ones that say "all/complete" do.

---

## 5. TESTIMONIALS

**CQU Testimonial Letter.pdf** — Gordon Boytell, Senior Project Manager, Central Queensland University (M 0407 066 539, g.boytell@cqu.edu.au), dated Monday 8 September 2025, on CQUniversity letterhead, addressed to Mitch Hannan. Subject: "Testimonial of TCS on the ROK Nth Fire Main Construction Project" (completed 2025). Credits TCS with professionalism ("integrity, responsibility, respect, and competence in conduct and communication"), transparency, and cooperation with all stakeholders; closes "Central Queensland University (CQU) strongly recommends the product and services that TCS have provided" and looks forward to future opportunities. Unsigned graphic but named signatory with direct contact details.

**GHD Testimonial Letter.pdf** — Bryan Percival, Senior hydraulic and fire consultant, GHD Pty Ltd (ABN 39 008 488 373, 145 Ann Street Brisbane), dated 10 December 2025, signed. Same project (styled "Central Queensland University Fire Hydrant Upgrade Project"), TCS as **Principal Contractor** under Mitch Hannan. Itemises the scope (hydrant mains, valves, boosters; civil and plumbing infrastructure across multiple campus zones; earthworks/roadworks; testing, commissioning and certification with authorities) and the delivery qualities (project management, safety/quality, communication, "ability to manage live campus environments with minimal disruption"); as lead fire system designer GHD "confidently recommend TriCore Civil Services for future civil, plumbing, or fire infrastructure projects requiring a capable and reliable Principal Contractor."

**Recommended placement (both submissions, each standalone):**
- Attach **both letters as an appendix** ("Appendix — Client and Consultant References") in each of the two ROK submissions — each tender must stand alone (§5.2), so neither can rely on the other carrying them.
- Reference them in **one sentence inside a Limestone-style capability paragraph** in each cover letter — e.g. the Rockhampton-delivery point: the referenced project is a completed **Rockhampton fire-main job on the CQU campus** — the same city as TEN16699, direct evidence of CQ delivery capability on live sites, and CQU is the adjoining landowner relevant to the EDQ discharge condition (CL E3). Do not overclaim the CQU relationship beyond the letter's words.
- **Attribution care:** both letters name **TriCore Civil Services (TCS)** as the contractor. In the TCS civil submission they are first-party references. In the **TPS hydraulic submission**, present them accurately as group/PM-capability references (same management, Mitch Hannan; GHD's letter expressly recommends "civil, plumbing, or fire infrastructure") — do not caption them as TPS project references.
- Transcription note: both letters show "PO Box 7801"; TriCore's correct box is 7081 — quote nothing from the address blocks.

---

## QA actions arising (for the red-team checklist)

1. Signature-block character check both ROK submissions: TPS ABN **89 620 147 935** + QBCC 15100514; TCS ABN 89 195 291 365 (+ decide whether to add TCS QBCC — absent from every example).
2. Do not reuse the CQU HYD file as a template without fixing the 10-digit ABN; do not reuse SPS HYD block without re-adding the QBCC line; fix `Tricoreplumbing.com.au` capitalisation.
3. Confirm current street address before using the Limestone letterhead line (9 Ramsay Road appears only there).
4. Remove BACPLAY's empty Heading-1 artifact if that file seeds the ROK document.
5. Tender basis cell: `Lump Sum construct-only — subject to clarifications herein`; Validity: adopt Limestone two-part wording + escalation (E52).
6. Every DROP-row replacement (E04, E06, E08, E14, E16, E22, E23, E41) has a named successor clause in Sections 3.2–3.8 — verify none of the dropped wordings survives a copy-paste pass.
