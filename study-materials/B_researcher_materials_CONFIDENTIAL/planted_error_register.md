# Planted error register

> **CONFIDENTIAL. Researchers only. Do not show to participants and do not load into any participant-visible screen.**

Every deliberate error in the AI summaries. Each test set has the same five error slots, so the sets are matched; the practice set has two.

| Error ID | Set | Claim | Slot | Category | Error type | Severity | Cue in B and C | AI statement says | Correct information | Evidence |
|---|---|---|---|---|---|---|---|---|---|---|
| S1-E1 | Set 1 | 2 | DET | Factual error | Incorrect client information | Low | Uncertain / Medium | States 31 employees. | The company currently employs 34 staff. 31 was last year's figure. The ownership part of the claim is correct. | D1 §1 “Number of employees”<br>D3 §1 “Number of employees” |
| S1-E2 | Set 1 | 5 | CMP | Incorrect comparison | Incorrect year-on-year comparison | High | Discrepancy / Low | States the previous-year operating profit as £162,000, so reports an increase. | Previous-year operating profit was £182,000. Operating profit fell by £8,000 (4.4%) to £174,000. | D2 §1 “Operating profit”<br>D3 §2 “Operating profit” |
| S1-E3 | Set 1 | 8 | FIG | Factual error | Incorrect financial amount | Medium | Supported / High | States the personal guarantee limit as £57,000. | The personal guarantee from Eleanor Harlow is limited to £75,000. | D4 §2 “Personal guarantee” |
| S1-E4 | Set 1 | 11 | OMI | Omission | Missing important information | High | Uncertain / Medium | Says no other material changes were identified. The two differences it lists are correct. | The client declared a new HMRC Time to Pay arrangement (agreed November 2025) for £48,000 of VAT arrears, with £32,000 still outstanding. Last year's review recorded no tax arrears. | D1 §4 “Tax arrears or payment arrangements with HMRC?”<br>D3 §1 “Tax arrears or HMRC arrangements” |
| S1-E5 | Set 1 | 12 | CON | Unsupported claim | Incorrect conclusion | High | Uncertain / Low | Concludes the position is stronger on every key measure. | Several measures weakened: operating profit (£182,000 to £174,000), net profit (£120,000 to £109,000), cash (£95,000 to £62,000), current ratio (1.49 to 1.40), customer concentration (27% to 38%) and account conduct (no excesses to three). Only revenue and net assets improved. | D3 §2 “Operating profit”<br>D3 §2 “Net profit after tax”<br>D3 §2 “Cash at bank”<br>D3 §2 “Current ratio”<br>D2 §3 “Current ratio”<br>D2 §2 “Cash at bank” |
| S2-E1 | Set 2 | 4 | DET | Factual error | Wrong date | Medium | Uncertain / Medium | States the next review date as 30 November 2026. | The next review date is 30 November 2025. The interest rate part of the claim is correct. | D4 §1 “Next review date” |
| S2-E2 | Set 2 | 7 | CMP | Incorrect comparison | Incorrect year-on-year comparison | High | Discrepancy / Low | Says interest cover is unchanged from the previous year. | Interest cover fell from 6.0x to 4.0x. It is still above the 3.5x minimum, but the headroom has narrowed sharply. | D2 §3 “Interest cover (operating profit ÷ interest payable)”<br>D3 §2 “Interest cover” |
| S2-E3 | Set 2 | 8 | FIG | Factual error | Incorrect financial amount | Medium | Supported / High | States total bank borrowing as £395,000. | Total bank borrowing at 30 September 2025 was £430,000 (overdraft £176,000 plus term loan £254,000). £395,000 was the previous year's figure. | D2 §2 “Total bank borrowing”<br>D3 §2 “Total bank borrowing” |
| S2-E4 | Set 2 | 10 | CON | Unsupported claim | Incorrect conclusion | Medium | Uncertain / Low | Concludes that customers are paying more quickly. The two debtor figures quoted are correct. | Debtors rising while revenue falls means customers are paying more slowly. Debtor days increased from 56 to 66. | D2 §3 “Debtor days”<br>D3 §2 “Debtor days” |
| S2-E5 | Set 2 | 12 | OMI | Omission | Missing important information | High | Uncertain / Medium | Says no other material changes were identified. The differences it lists are correct. | Ownership and management changed: Gareth Aldred resigned on 30 June 2025 and transferred his 45% shareholding to Thomas Aldred, who became a director the same day. Last year's review lists Gareth Aldred as 45% shareholder. | D1 §4 “Changes to directors or shareholders since the last review?”<br>D1 §2 “Thomas Aldred”<br>D3 §1 “Directors and shareholdings” |
| S3-E1 | Set 3 | 3 | FIG | Factual error | Incorrect financial amount | High | Supported / High | States the requested overdraft limit as £160,000. | The requested limit is £180,000, an increase of £60,000. | D1 §3 “Requested facility”<br>D1 §3 “Increase requested” |
| S3-E2 | Set 3 | 6 | CMP | Incorrect comparison | Incorrect year-on-year comparison | Medium | Discrepancy / Low | States the previous-year gross margin as 43.0%, so reports an improvement. | Previous-year gross margin was 45.0%. Gross margin fell by one percentage point to 44.0%. | D2 §3 “Gross margin”<br>D3 §2 “Gross margin” |
| S3-E3 | Set 3 | 8 | DET | Factual error | Incorrect client information | Medium | Uncertain / Medium | Names Daniel Reyes as the guarantor. | The personal guarantee is given by Helen Ashcombe. The £60,000 limit and the debenture are correct. | D4 §2 “Personal guarantee” |
| S3-E4 | Set 3 | 10 | OMI | Omission | Missing important information | High | Uncertain / Medium | Says no other material changes were identified. The differences it lists are correct. | The client declared a county court claim for £41,500 issued on 14 April 2026 by a former supplier, Fernbrook Nurseries. Last year's review recorded no legal actions. | D1 §4 “Legal actions or court claims?”<br>D3 §1 “Legal actions or court claims” |
| S3-E5 | Set 3 | 11 | CON | Unsupported claim | Incorrect conclusion | Medium | Uncertain / Low | Concludes that stock is selling through more quickly. The two stock figures quoted are correct. | Stock growing much faster than sales means stock is selling more slowly. Stock days increased from 75 to 89. | D2 §3 “Stock days”<br>D3 §2 “Stock days” |
| P-E1 | Practice set | 2 | FIG | Factual error | Incorrect financial amount | High | Supported / High | States the loan requested as £45,000. | The loan requested is £40,000. | D1 §2 “Loan requested” |
| P-E2 | Practice set | 4 | CMP | Incorrect comparison | Incorrect year-on-year comparison | High | Discrepancy / Low | States previous-year net profit as £26,000, so reports an increase. | Previous-year net profit was £36,000. Net profit fell to £31,000. | D1 §3 “Net profit after tax”<br>D2 §1 “Net profit after tax” |

## Slot definitions

- **FIG**: Wrong figure
- **DET**: Wrong date or client detail
- **CMP**: Wrong year-on-year comparison
- **CON**: Conclusion not supported by the evidence
- **OMI**: Omission of a material change

## Error positions

| Set | Claim numbers that are incorrect | Claim numbers that are correct |
|---|---|---|
| Set 1 | 2, 5, 8, 11, 12 | 1, 3, 4, 6, 7, 9, 10 |
| Set 2 | 4, 7, 8, 10, 12 | 1, 2, 3, 5, 6, 9, 11 |
| Set 3 | 3, 6, 8, 10, 11 | 1, 2, 4, 5, 7, 9, 12 |
| Practice set | 2, 4 | 1, 3, 5, 6 |
