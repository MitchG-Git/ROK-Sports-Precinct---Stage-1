# RUN STATUS — tender-run-01
Updated: 26 Jul 2026

| Phase | Status | Gate evidence |
|---|---|---|
| 0 — Document control | **COMPLETE** | `01_Document_Register/00_DOCUMENT_CONTROL.md` (PRESENT 11/43, MISSING impact-assessed, UNREGISTERED mapped); `02_Addenda_and_Precedence/ADDENDUM_PRECEDENCE_REGISTER.md` (two-stream sequence resolved, effective revisions established); duplicates hash-identified (22 groups); `UNREADABLE_OR_MISSING_FILES.md` (0 unreadable; 7 DWG registered not-pretended-read; 2 owner-encrypted PDFs decrypt clean) |
| 1 — Read everything | **COMPLETE** | 12/12 structured notes in `01_Document_Register/notes/` + 7 addendum notices read by orchestrator. Tender-document page coverage: 100% of unique pages (duplicates reviewed once against primaries; combine PDFs = same sheets). TriCore internal docs staged by phase: workbooks audited (P3 done), Groundplan take-offs → P4, quotes → P5 (in progress), submission examples → P8. `CONFLICT_LOG.md` categories A–H populated. Geotech verified 184/184 incl. §5.5 values; deltas H1–H5 logged (refusal 25/36 locations; batter rule applies <2 m). |
| 2 — Scope matrix | **COMPLETE** | `03_Scope_and_Interfaces/01_SCOPE_MATRIX.md` — 184 schedule rows allocated, zero blanks, no double-count; POD boundary corrected per §5.1 corollary (all civil-sheet drainage = TCS); appendices: contradictions, gap check, interface ledger. |
| 3 — Cost model audit | **COMPLETE** | `07_Commercial_Reconciliation/COST_MODEL_REBUILD_DECISION.md` + `workbook_audit_raw.json` + 30 sheet dumps. Decision: Hyd REPAIR / Civ REBUILD on CQU-Hyd architecture. New defect found: NBC 3× Rheem HWU ($12,944.26) orphaned from all roll-ups. Pump station $545,700 computed but never rolled up. Civil $890,849.95 is materials-only (labour=$0, plant=$0). Profit currently compounds on prelim+OH (45.73% eff. vs 41.5% per §5.4) — Director flag. |
| 4 — Quantity verification | pending | |
| 5 — Quote register | pending | |
| 6 — Rebuild models | pending | |
| 7 — Programme/labour/plant | pending | |
| 8 — Submissions | pending | |
| 9 — QA/red-team | pending | |

## Key run facts
- Repo: `ROK Sports Precinct - Stage 1`, branch **tender-run-01** (off main @ 324cddc). No push/merge without Director approval.
- 257 files / 233 PDFs / 1,077 PDF pages; all hydrated, all readable.
- Addenda: RRC official Nos. 7–10 held; RRC 1–6 NOT held; Hutchies circulars 01/02/5 held (5 = pre-issue of RRC 9).
- All discipline drawings effective at **T1**; Design Report **Rev B** modifies civil design intent post-T1.
- ITT closing date printed 20 Jul 2026 vs our locked submission date 24 Jul 2026 — flagged to D6, locked decision applied.
- Paynters register Volume 43 row is blank (register defect).

## Open items feeding D6
1. VOL 35 civil spec absent — TCS governing spec (confidence ceiling Medium until resolved)
2. RRC Addenda 1–6 unsighted — narrow qualification + acknowledgement handling
3. ITT §27 Appendix Folder (ShareFile) not downloaded — **Mitch action**
4. VOL 32 Hawkesbury bifold-door drainage — direct hydraulic scope absent
5. F1324/F1325 both "DETAILS SHEET 5"; long-sections Sheet 13 absent from series — verify from drawing index
6. Submission-date vs closing-date discrepancy — Director aware (locked)
