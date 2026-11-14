# Answer key: Practice set, Lark & Lantern Bakery Ltd

> **CONFIDENTIAL. Researchers only. Do not show to participants and do not load into any participant-visible screen.**

- Claims in the AI summary: **6**
- Correct claims: **4** (claims 1, 3, 5, 6)
- Planted errors: **2** (claims 2, 4)
- Correct final decision: **Approve with corrections** or **Reject**. Approving the summary unchanged is the wrong decision.

## 1. Full claim table

| ID | AI summary statement | Verdict | Correct information | Source document | Error type | Severity |
|---|---|---|---|---|---|---|
| P-C01 | Lark & Lantern Bakery Ltd is a craft bakery and café based in Sorrelgate, incorporated in June 2017. | Correct | As stated | D1 §1 Business details, “Nature of business”: Craft bakery and café<br>D1 §1 Business details, “Date of incorporation”: 6 June 2017 | None | n/a |
| P-C02 (P-E1) | It is requesting a £45,000 loan over four years to replace its deck oven. | **INCORRECT** | The loan requested is £40,000. | D1 §2 Loan request, “Loan requested”: £40,000 | Factual error: Incorrect financial amount | High |
| P-C03 | Revenue rose 7.0% to £412,000 in the year ended 31 March 2026 (previous year: £385,000). | Correct | As stated | D1 §3 Latest financial figures (year ended 31 March 2026), “Revenue”: £412,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Revenue”: £385,000 | None | n/a |
| P-C04 (P-E2) | Net profit after tax increased to £31,000 from £26,000 the previous year. | **INCORRECT** | Previous-year net profit was £36,000. Net profit fell to £31,000. | D1 §3 Latest financial figures (year ended 31 March 2026), “Net profit after tax”: £31,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Net profit after tax”: £36,000 | Incorrect comparison: Incorrect year-on-year comparison | High |
| P-C05 | The business employs 12 staff, one more than last year, and is wholly owned by Naomi Lark. | Correct | As stated | D1 §1 Business details, “Number of employees”: 12<br>D2 §1 Position at last review (year ended 31 March 2025), “Number of employees”: 11<br>D1 §1 Business details, “Owner”: Naomi Lark (100% shareholder and sole director) | None | n/a |
| P-C06 | Cash at bank was £18,000 at the year end (previous year: £22,000), and the business had no borrowing with the Bank at the last review. | Correct | As stated | D1 §3 Latest financial figures (year ended 31 March 2026), “Cash at bank”: £18,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Cash at bank”: £22,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Borrowing from the Bank”: None | None | n/a |

## 2. Planted errors in detail

### P-E1: claim 2 (Wrong figure)

- **AI statement:** It is requesting a £45,000 loan over four years to replace its deck oven.
- **What is wrong:** States the loan requested as £45,000.
- **Correct information:** The loan requested is £40,000.
- **Evidence:** D1 §2 Loan request, “Loan requested”: £40,000
- **Classification:** Factual error (Incorrect financial amount)
- **Severity:** High
- **Why it matters:** The amount requested is the core of the decision.
- **Cue shown in Conditions B and C:** Supported, High confidence
- **Corrected statement:** It is requesting a £40,000 loan over four years to replace its deck oven.
- **Expected reviewer action:** Edit (correct it) or Reject

### P-E2: claim 4 (Wrong year-on-year comparison)

- **AI statement:** Net profit after tax increased to £31,000 from £26,000 the previous year.
- **What is wrong:** States previous-year net profit as £26,000, so reports an increase.
- **Correct information:** Previous-year net profit was £36,000. Net profit fell to £31,000.
- **Evidence:** D1 §3 Latest financial figures (year ended 31 March 2026), “Net profit after tax”: £31,000; D2 §1 Position at last review (year ended 31 March 2025), “Net profit after tax”: £36,000
- **Classification:** Incorrect comparison (Incorrect year-on-year comparison)
- **Severity:** High
- **Why it matters:** Reverses the direction of the profit trend.
- **Cue shown in Conditions B and C:** Discrepancy, Low confidence
- **Corrected statement:** Net profit after tax fell to £31,000 from £36,000 the previous year.
- **Expected reviewer action:** Edit (correct it) or Reject

## 3. Correct claims

| ID | Statement | Supporting evidence | Cue shown in B and C |
|---|---|---|---|
| P-C01 | Lark & Lantern Bakery Ltd is a craft bakery and café based in Sorrelgate, incorporated in June 2017. | D1 §1 Business details, “Nature of business”: Craft bakery and café<br>D1 §1 Business details, “Date of incorporation”: 6 June 2017 | Supported, High |
| P-C03 | Revenue rose 7.0% to £412,000 in the year ended 31 March 2026 (previous year: £385,000). | D1 §3 Latest financial figures (year ended 31 March 2026), “Revenue”: £412,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Revenue”: £385,000 | Supported, High |
| P-C05 | The business employs 12 staff, one more than last year, and is wholly owned by Naomi Lark. | D1 §1 Business details, “Number of employees”: 12<br>D2 §1 Position at last review (year ended 31 March 2025), “Number of employees”: 11<br>D1 §1 Business details, “Owner”: Naomi Lark (100% shareholder and sole director) | Uncertain, Medium **(deliberate false alarm)** |
| P-C06 | Cash at bank was £18,000 at the year end (previous year: £22,000), and the business had no borrowing with the Bank at the last review. | D1 §3 Latest financial figures (year ended 31 March 2026), “Cash at bank”: £18,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Cash at bank”: £22,000<br>D2 §1 Position at last review (year ended 31 March 2025), “Borrowing from the Bank”: None | Supported, High |

## 4. Scoring

- **Error found (hit):** the participant marks an incorrect claim as wrong (flags, edits or rejects it). Count it even if their correction is not exactly right; record correction accuracy separately.
- **Missed error (over-trust):** an incorrect claim left unmarked or approved.
- **False rejection (under-trust):** a correct claim marked as wrong.
- Detection rate = hits ÷ 2. False-rejection rate = false rejections ÷ 4.
- For the omission, accept any answer that identifies the missing item, even if the participant attaches it to a different claim or says it in the final comment.
