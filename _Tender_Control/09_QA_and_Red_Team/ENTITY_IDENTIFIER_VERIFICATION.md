# ENTITY IDENTIFIER VERIFICATION — primary-source check before issue
tender-run-01 · verified 27 July 2026 · source: Australian Business Register (abr.business.gov.au), the primary source nominated in the master prompt

## ⚠️ FINDING 1 — THE TPS ABN IS WRONG IN EVERY SOURCE WE HOLD, INCLUDING THE MASTER PROMPT

| Source | TPS ABN stated | Verdict |
|---|---|---|
| `CQUTafe_HYD.docx` (submission template, signature block) | `9 620 147 935` | **10 digits** — invalid on its face |
| `SPS_HYD_Tender_Proposal_Q2381.docx` | `89 620 147 935` | 11 digits but **FAILS the ABN check-digit algorithm** |
| Master prompt §3 ("use the eleven-digit figure") | `89 620 147 935` | **Also wrong** — inherited the SPS error |
| **Australian Business Register (verified)** | **`91 620 147 935`** | ✅ **VALID** — checksum passes, entity active |

**Verified register entry:**
> **ABN 91 620 147 935** — TRICORE PLUMBING SERVICES PTY LTD · Australian Private Company · **Active from 30 Jun 2017** · GST registered from 30 Jun 2017 · QLD 4122

**Proof the prompt's figure cannot be right.** The ABN algorithm (subtract 1 from the first digit, apply weights 10,1,3,5,7,9,11,13,15,17,19, sum must be divisible by 89) gives `89 620 147 935` → weighted sum 532, 532 mod 89 = 87 → invalid. We also tested **every** possible leading digit against the 10-digit fragment `9 620 147 935` — 1 through 9 — and **none produces a valid ABN**. So the error was never a dropped leading digit: the prefix itself is wrong. The correct prefix is **91**, and `91 620 147 935` → weighted sum 534 → divisible by 89 → valid, and it resolves on the register to the correct legal entity.

**Action:** use **ABN 91 620 147 935** on the TPS submission. **Director confirmation requested before issue** — this contradicts two prior TriCore submissions and the master prompt, so if `89 620 147 935` has been used on issued documents previously, that is worth knowing about beyond this tender (invoices, contracts, ATO records).

## ✅ FINDING 2 — THE TCS ABN IS CORRECT

> **ABN 89 195 291 365** — "The Trustee for THE TRICORE CIVIL SERVICES TRUST" · Discretionary Trading Trust · **Active from 07 Sep 2018** · GST registered from 07 Sep 2018 · QLD 4174

Checksum valid; matches the master prompt exactly. Note the register renders the entity as **"The Trustee for The TriCore Civil Services Trust"** — the submission should present the trustee/trust relationship consistently with this (i.e. *TriCore Civil Services Pty Ltd ATF The TriCore Civil Services Trust, ABN 89 195 291 365*), which is how the master prompt states it.

## FINDING 3 — QBCC licence and postal addresses

| Item | Stated | Status |
|---|---|---|
| TPS QBCC licence | **15100514** | Corroborated by TriCore's own public web presence; **still to be confirmed against the QBCC licence register** by the Director before issue (licence class and currency matter — ITT §15 requires a QBCC-licensed contractor be nominated for the Clubhouse and Public Amenities buildings) |
| TCS QBCC licence | *(none in any example submission)* | **Gap** — no TriCore Civil Services QBCC number appears in any prior submission. Confirm whether TCS holds a licence and whether one is required for its scope |
| Tender postal address | PO Box 103, Rockhampton QLD 4700 | Per master prompt (Director instruction) — use as directed |
| Brisbane office | PO Box 7081, Hemmant QLD 4174 | **Discrepancy**: public listings show **PO Box 7801**, Hemmant 4174 (digits transposed?). Confirm before printing on a submission |
| TPS registered business location | QLD **4122** on the ABR | Differs from the Hemmant 4174 operating address — normal (ABR often shows the accountant's address), but noted so nobody "corrects" the letterhead to match the register |

## Why this check was run
Master prompt §2.2: *"Never treat a folder name, a filename, or a statement in this prompt as proof"* and §3: *"Before issue, independently verify both ABNs, the QBCC licence number and the postal addresses against a primary source … Do not carry a business identifier onto a tender simply because it appeared in a prior document or in this prompt."* The instruction was correct to insist: the prompt's own figure did not survive verification.

## Pre-issue checklist (Director)
- [ ] Confirm TPS ABN **91 620 147 935** for the submission
- [ ] Consider where the invalid `89 620 147 935` may have been used previously
- [ ] Confirm QBCC 15100514 currency/class on the QBCC register
- [ ] Confirm whether TCS requires/holds a QBCC licence
- [ ] Confirm Hemmant PO Box (7081 vs 7801)
- [ ] Confirm PO Box 103 Rockhampton is the correct tender address for both entities
