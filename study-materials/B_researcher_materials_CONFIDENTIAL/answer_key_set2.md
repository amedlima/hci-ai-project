# Answer key: Set 2, Tidewell Freight Services Ltd

> **CONFIDENTIAL. Researchers only. Do not show to participants and do not load into any participant-visible screen.**

- Claims in the AI summary: **12**
- Correct claims: **7** (claims 1, 2, 3, 5, 6, 9, 11)
- Planted errors: **5** (claims 4, 7, 8, 10, 12)
- Correct final decision: **Approve with corrections** or **Reject**. Approving the summary unchanged is the wrong decision.

## 1. Full claim table

| ID | AI summary statement | Verdict | Correct information | Source document | Error type | Severity |
|---|---|---|---|---|---|---|
| S2-C01 | Tidewell Freight Services Ltd is a regional road haulage and pallet distribution company based in Estonbridge, incorporated in September 2008, with 46 employees. | Correct | As stated | D1 §1 Business details, “Nature of business”: Regional road haulage and pallet distribution<br>D1 §1 Business details, “Date of incorporation”: 9 September 2008<br>D1 §1 Business details, “Number of employees”: 46 | None | n/a |
| S2-C02 | It is owned by its two directors, Priya Deshmukh (55%) and Thomas Aldred (45%). | Correct | As stated | D1 §2 Directors and shareholders, “Priya Deshmukh”: 55%<br>D1 §2 Directors and shareholders, “Thomas Aldred”: 45% | None | n/a |
| S2-C03 | The company is requesting an increase in its overdraft limit from £200,000 to £275,000 to fund working capital for longer payment terms on a proposed supermarket distribution contract. | Correct | As stated | D1 §3 Facility request, “Existing facility”: Overdraft, limit £200,000<br>D1 §3 Facility request, “Requested facility”: Overdraft, limit £275,000<br>D1 §3 Facility request, “Purpose”: Working capital for longer payment terms on a proposed supermarket distribution contract | None | n/a |
| S2-C04 (S2-E1) | The existing overdraft is priced at base rate + 3.75% and is next due for review on 30 November 2026. | **INCORRECT** | The next review date is 30 November 2025. The interest rate part of the claim is correct. | D4 §1 Facility terms, “Next review date”: 30 November 2025 | Factual error: Wrong date | Medium |
| S2-C05 | Revenue fell 4.0% to £3,360,000 in the year ended 30 September 2025 (previous year: £3,500,000). | Correct | As stated | D2 §1 Profit and loss summary, “Revenue”: £3,360,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Revenue”: £3,500,000 | None | n/a |
| S2-C06 | Operating profit fell to £156,000 from £210,000, and net profit after tax was £88,000. | Correct | As stated | D2 §1 Profit and loss summary, “Operating profit”: £156,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Operating profit”: £210,000<br>D2 §1 Profit and loss summary, “Net profit after tax”: £88,000 | None | n/a |
| S2-C07 (S2-E2) | Interest cover was 4.0x, unchanged from the previous year and above the covenant minimum of 3.5x. | **INCORRECT** | Interest cover fell from 6.0x to 4.0x. It is still above the 3.5x minimum, but the headroom has narrowed sharply. | D2 §3 Key ratios, “Interest cover (operating profit ÷ interest payable)”: 4.0x<br>D3 §2 Financial figures, year ended 30 September 2024, “Interest cover”: 6.0x | Incorrect comparison: Incorrect year-on-year comparison | High |
| S2-C08 (S2-E3) | Total bank borrowing at the year end was £395,000, made up of the overdraft and a vehicle term loan. | **INCORRECT** | Total bank borrowing at 30 September 2025 was £430,000 (overdraft £176,000 plus term loan £254,000). £395,000 was the previous year's figure. | D2 §2 Balance sheet extract at 30 September 2025, “Total bank borrowing”: £430,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Total bank borrowing”: £395,000 | Factual error: Incorrect financial amount | Medium |
| S2-C09 | Cash at bank fell to £41,000 from £88,000; the current ratio was 1.20, above the covenant minimum of 1.10. | Correct | As stated | D2 §2 Balance sheet extract at 30 September 2025, “Cash at bank”: £41,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Cash at bank”: £88,000<br>D2 §3 Key ratios, “Current ratio”: 1.20<br>D4 §3 Financial covenants, “Minimum current ratio”: 1.10 | None | n/a |
| S2-C10 (S2-E4) | Trade debtors rose to £612,000 from £540,000 even though revenue fell, which indicates that customers are paying more quickly than last year. | **INCORRECT** | Debtors rising while revenue falls means customers are paying more slowly. Debtor days increased from 56 to 66. | D2 §3 Key ratios, “Debtor days”: 66<br>D3 §2 Financial figures, year ended 30 September 2024, “Debtor days”: 56 | Unsupported claim: Incorrect conclusion | Medium |
| S2-C11 | The request would raise the overdraft limit by £75,000 (37.5%) and does not take effect until the Bank confirms credit approval. | Correct | As stated | D1 §3 Facility request, “Increase requested”: £75,000 (37.5%)<br>D1 §3 Facility request, “Paragraph”: All requests are subject to credit approval by the Bank. No change to the facility takes effect until the Bank confirms approval in writing. | None | n/a |
| S2-C12 (S2-E5) | Compared with last year's review, the differences flagged are lower profit, lower cash and one overdraft excess in the past 12 months (two in the previous review period). No other material changes were identified. | **INCORRECT** | Ownership and management changed: Gareth Aldred resigned on 30 June 2025 and transferred his 45% shareholding to Thomas Aldred, who became a director the same day. Last year's review lists Gareth Aldred as 45% shareholder. | D1 §4 Client declarations, “Changes to directors or shareholders since the last review?”: Yes. Gareth Aldred resigned as a director on 30 June 2025 and transferred his 45% shareholding to Thomas Aldred, who was appointed a director on the same day.<br>D1 §2 Directors and shareholders, “Thomas Aldred”: 30 June 2025<br>D3 §1 Client snapshot at last review, “Directors and shareholdings”: Priya Deshmukh (55%), Gareth Aldred (45%) | Omission: Missing important information | High |

## 2. Planted errors in detail

### S2-E1: claim 4 (Wrong date or client detail)

- **AI statement:** The existing overdraft is priced at base rate + 3.75% and is next due for review on 30 November 2026.
- **What is wrong:** States the next review date as 30 November 2026.
- **Correct information:** The next review date is 30 November 2025. The interest rate part of the claim is correct.
- **Evidence:** D4 §1 Facility terms, “Next review date”: 30 November 2025
- **Classification:** Factual error (Wrong date)
- **Severity:** Medium
- **Why it matters:** Suggests the facility has a year left to run when it is in fact due for review now.
- **Cue shown in Conditions B and C:** Uncertain, Medium confidence
- **Corrected statement:** The existing overdraft is priced at base rate + 3.75% and is next due for review on 30 November 2025.
- **Expected reviewer action:** Edit (correct it) or Reject

### S2-E2: claim 7 (Wrong year-on-year comparison)

- **AI statement:** Interest cover was 4.0x, unchanged from the previous year and above the covenant minimum of 3.5x.
- **What is wrong:** Says interest cover is unchanged from the previous year.
- **Correct information:** Interest cover fell from 6.0x to 4.0x. It is still above the 3.5x minimum, but the headroom has narrowed sharply.
- **Evidence:** D2 §3 Key ratios, “Interest cover (operating profit ÷ interest payable)”: 4.0x; D3 §2 Financial figures, year ended 30 September 2024, “Interest cover”: 6.0x
- **Classification:** Incorrect comparison (Incorrect year-on-year comparison)
- **Severity:** High
- **Why it matters:** Hides a marked deterioration in the company's ability to service its debt, just as it asks to borrow more.
- **Cue shown in Conditions B and C:** Discrepancy, Low confidence
- **Corrected statement:** Interest cover fell to 4.0x from 6.0x the previous year; it remains above the covenant minimum of 3.5x.
- **Expected reviewer action:** Edit (correct it) or Reject

### S2-E3: claim 8 (Wrong figure)

- **AI statement:** Total bank borrowing at the year end was £395,000, made up of the overdraft and a vehicle term loan.
- **What is wrong:** States total bank borrowing as £395,000.
- **Correct information:** Total bank borrowing at 30 September 2025 was £430,000 (overdraft £176,000 plus term loan £254,000). £395,000 was the previous year's figure.
- **Evidence:** D2 §2 Balance sheet extract at 30 September 2025, “Total bank borrowing”: £430,000; D3 §2 Financial figures, year ended 30 September 2024, “Total bank borrowing”: £395,000
- **Classification:** Factual error (Incorrect financial amount)
- **Severity:** Medium
- **Why it matters:** Understates the company's debt by £35,000 by using last year's figure.
- **Cue shown in Conditions B and C:** Supported, High confidence
- **Corrected statement:** Total bank borrowing at the year end was £430,000, made up of the overdraft and a vehicle term loan.
- **Expected reviewer action:** Edit (correct it) or Reject

### S2-E4: claim 10 (Conclusion not supported by the evidence)

- **AI statement:** Trade debtors rose to £612,000 from £540,000 even though revenue fell, which indicates that customers are paying more quickly than last year.
- **What is wrong:** Concludes that customers are paying more quickly. The two debtor figures quoted are correct.
- **Correct information:** Debtors rising while revenue falls means customers are paying more slowly. Debtor days increased from 56 to 66.
- **Evidence:** D2 §3 Key ratios, “Debtor days”: 66; D3 §2 Financial figures, year ended 30 September 2024, “Debtor days”: 56
- **Classification:** Unsupported claim (Incorrect conclusion)
- **Severity:** Medium
- **Why it matters:** Turns a warning sign about cash collection into a positive, on the very issue the new borrowing is meant to fund.
- **Cue shown in Conditions B and C:** Uncertain, Low confidence
- **Corrected statement:** Trade debtors rose to £612,000 from £540,000 even though revenue fell; debtor days lengthened from 56 to 66, so customers are paying more slowly than last year.
- **Expected reviewer action:** Edit (correct it) or Reject

### S2-E5: claim 12 (Omission of a material change)

- **AI statement:** Compared with last year's review, the differences flagged are lower profit, lower cash and one overdraft excess in the past 12 months (two in the previous review period). No other material changes were identified.
- **What is wrong:** Says no other material changes were identified. The differences it lists are correct.
- **Correct information:** Ownership and management changed: Gareth Aldred resigned on 30 June 2025 and transferred his 45% shareholding to Thomas Aldred, who became a director the same day. Last year's review lists Gareth Aldred as 45% shareholder.
- **Evidence:** D1 §4 Client declarations, “Changes to directors or shareholders since the last review?”: Yes. Gareth Aldred resigned as a director on 30 June 2025 and transferred his 45% shareholding to Thomas Aldred, who was appointed a director on the same day.; D1 §2 Directors and shareholders, “Thomas Aldred”: 30 June 2025; D3 §1 Client snapshot at last review, “Directors and shareholdings”: Priya Deshmukh (55%), Gareth Aldred (45%)
- **Classification:** Omission (Missing important information)
- **Severity:** High
- **Why it matters:** A new director and 45% owner has not been assessed by the bank. This is exactly the kind of change from last year the agent was asked to flag.
- **Cue shown in Conditions B and C:** Uncertain, Medium confidence
- **Corrected statement:** Compared with last year's review, the differences flagged are lower profit, lower cash, one overdraft excess in the past 12 months (two in the previous review period), and a change of director and 45% shareholder from Gareth Aldred to Thomas Aldred on 30 June 2025.
- **Expected reviewer action:** Edit (correct it) or Reject

## 3. Correct claims

| ID | Statement | Supporting evidence | Cue shown in B and C |
|---|---|---|---|
| S2-C01 | Tidewell Freight Services Ltd is a regional road haulage and pallet distribution company based in Estonbridge, incorporated in September 2008, with 46 employees. | D1 §1 Business details, “Nature of business”: Regional road haulage and pallet distribution<br>D1 §1 Business details, “Date of incorporation”: 9 September 2008<br>D1 §1 Business details, “Number of employees”: 46 | Supported, High |
| S2-C02 | It is owned by its two directors, Priya Deshmukh (55%) and Thomas Aldred (45%). | D1 §2 Directors and shareholders, “Priya Deshmukh”: 55%<br>D1 §2 Directors and shareholders, “Thomas Aldred”: 45% | Supported, High |
| S2-C03 | The company is requesting an increase in its overdraft limit from £200,000 to £275,000 to fund working capital for longer payment terms on a proposed supermarket distribution contract. | D1 §3 Facility request, “Existing facility”: Overdraft, limit £200,000<br>D1 §3 Facility request, “Requested facility”: Overdraft, limit £275,000<br>D1 §3 Facility request, “Purpose”: Working capital for longer payment terms on a proposed supermarket distribution contract | Supported, High |
| S2-C05 | Revenue fell 4.0% to £3,360,000 in the year ended 30 September 2025 (previous year: £3,500,000). | D2 §1 Profit and loss summary, “Revenue”: £3,360,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Revenue”: £3,500,000 | Supported, High |
| S2-C06 | Operating profit fell to £156,000 from £210,000, and net profit after tax was £88,000. | D2 §1 Profit and loss summary, “Operating profit”: £156,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Operating profit”: £210,000<br>D2 §1 Profit and loss summary, “Net profit after tax”: £88,000 | Supported, High |
| S2-C09 | Cash at bank fell to £41,000 from £88,000; the current ratio was 1.20, above the covenant minimum of 1.10. | D2 §2 Balance sheet extract at 30 September 2025, “Cash at bank”: £41,000<br>D3 §2 Financial figures, year ended 30 September 2024, “Cash at bank”: £88,000<br>D2 §3 Key ratios, “Current ratio”: 1.20<br>D4 §3 Financial covenants, “Minimum current ratio”: 1.10 | Uncertain, Medium **(deliberate false alarm)** |
| S2-C11 | The request would raise the overdraft limit by £75,000 (37.5%) and does not take effect until the Bank confirms credit approval. | D1 §3 Facility request, “Increase requested”: £75,000 (37.5%)<br>D1 §3 Facility request, “Paragraph”: All requests are subject to credit approval by the Bank. No change to the facility takes effect until the Bank confirms approval in writing. | Supported, High |

## 4. Scoring

- **Error found (hit):** the participant marks an incorrect claim as wrong (flags, edits or rejects it). Count it even if their correction is not exactly right; record correction accuracy separately.
- **Missed error (over-trust):** an incorrect claim left unmarked or approved.
- **False rejection (under-trust):** a correct claim marked as wrong.
- Detection rate = hits ÷ 5. False-rejection rate = false rejections ÷ 7.
- For the omission, accept any answer that identifies the missing item, even if the participant attaches it to a different claim or says it in the final comment.
