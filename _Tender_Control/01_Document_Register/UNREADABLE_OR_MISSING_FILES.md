# UNREADABLE / PARTIALLY READABLE FILES — tender-run-01, 26 Jul 2026

No file in the repo is fully unreadable. Two classes need special handling:

## 1. CAD (.dwg) — 7 files, cannot be opened natively in this environment

| File | Source | TCS/TPS/stage impact of not opening |
|---|---|---|
| `Addendum 1/Civil/x01_pf_02-07-2026 (For Information Only).dwg` | Hutchies Add 01 | None material — issued "For Information Only", PDF governs per the Add 01 CAD disclaimer. No quantity may be derived from CAD anyway. |
| `Addendum 1/Civil/x01_pd_02-07-2026 (For Information Only).dwg` | Hutchies Add 01 | As above (drainage layout — PDF F13xx series governs) |
| `Addendum 1/Landscape/24523-ST1-MDC-L-SITE_02-07-2026 (For Information Only).dwg` | Hutchies Add 01 | None — landscape, not our trade |
| `Addendum 8/SE_12306_3DM001_STG1_DESIGN_3D Component_13-07-2026.dwg` (+ hash-dup in Add 10) | RRC Add 8 | Low — FSL tin for earthworks tendering. Our trench depths derive from invert levels on PDF long sections + FSL on layouts. Noted: no independent surface-model check performed. |
| `Addendum 10/ROCKHAMPTON SPORTS PRECINCT _ March 2025.dwg` | RRC Add 10 | Low — detail survey; PDF drawings carry the design levels we price from. |
| `Addendum 10/ROCKHAMPTON SPORTS PRECINCT RevB.dwg` | RRC Add 10 | As above (RevB latest) |

**Treatment:** registered, hash-verified, not pretended read. All quantities derive from PDF drawings (visual review). If a CAD-only discrepancy exists it cannot be detected here — risk noted in D6 register (low, because Add 01 disclaimer makes the PDFs the reference copy contractually).

## 2. Outlook .msg — 3 files, readable via extract-msg (Python), not natively

| File | Pair status |
|---|---|
| `TriCore Docs/Denis Email updates/260724 _ ROK Sports Precinct_ CIVIL SW V1 Summaries .msg` | Has sibling PDF print — equivalence check in Phase 1; treat as ONE source |
| `TriCore Docs/Denis Email updates/260724_ ROK SPORTS Hydraulic Summaries .msg` | Has sibling PDF print — as above |
| `Material/01 - Project Specific/Material/CIVIL SW QUOTE/RCP HEADWALL CULVERT ETC/Jaybro/stephen quote.msg` | No PDF sibling — must be extracted in Phase 5 (attachments may contain the actual quote) |

## 3. Encrypted PDFs — 2 files, decrypt with empty password (owner-locked only)

- `Material/01 - Project Specific/Material/Hydraulic/APS SEWER STATION/Quote_No_14065 - Rockhampton Sports Precinct.pdf`
- `Material/02 - Other Recent ROK Proj/CQUTafe_Material/big ticket and misc/aps pumps/Quote_No_13825 - CQU Rockhampton.pdf`

Both fully readable after empty-password decrypt; no content loss.

## 4. Not present at all (external dependencies)

- RRC ShareFile Appendix Folder (ITT §27) — mandatory reading, not downloaded. **Action for Mitch.**
- IFC models (Add 9 ShareFile link) — tender/sequencing only; not needed for pricing.
- 32 of 43 register volumes — see MISSING table in 00_DOCUMENT_CONTROL.md.
