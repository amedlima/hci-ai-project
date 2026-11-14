# Keeping the three conditions consistent

The comparison is only fair if the AI is equally right and equally wrong in every condition. The interface may change; the content may not.

## 1. One data file per set

Each set has one JSON file (`set1.json`, `set2.json`, `set3.json`, `practice.json`). All three conditions must render from that same file. Do not keep separate copies of the summary text per condition.

| Field in the set JSON | Condition A | Condition B | Condition C |
|---|---|---|---|
| `documents` (the four client documents) | Shown | Shown | Shown |
| `summary.paragraphs` (plain prose) | Shown | Shown, with citation markers | Not needed |
| `claims[].text` (the same sentences, one per claim) | Used only to let the participant mark a sentence | Shown | Shown as claim cards |
| `claims[].sources` (document, section, row, highlight text) | Hidden | Shown as links and highlights | Shown side by side with the claim |
| `claims[].cue.status`, `confidence`, `note` | Hidden | Shown as a confidence note | Shown as a status badge with note |
| `claims[].cue.check_hint` | Hidden | Hidden | Optional ("which claims most need checking") |
| `year_on_year` (previous and current values taken from the documents) | Hidden | Hidden | Optional "what changed since last year" view |
| Approve / Edit / Reject per claim, sign-off, audit log | No | No | Yes |

The paragraphs in `summary.paragraphs` are the claim sentences joined in order, so the wording is identical in every condition.

## 2. Rules

1. Never edit a claim, a source or a cue for one condition only. If a correction is needed, change the set JSON and re-run all checks.
2. Do not add or remove planted errors, and do not reorder claims between conditions.
3. The cue fields are part of the simulated AI output. They are the same in B and C, and they are deliberately imperfect: one error per set is marked Supported with High confidence, and one correct claim per set is marked Uncertain. Do not "fix" them.
4. Collect the same answers in every condition: a correct / incorrect judgement for each of the 12 sentences, and one final decision (approve, approve with corrections, reject). In Condition A and B this can be as simple as clicking a sentence to mark it wrong. Without this, detection rates cannot be compared across conditions.
5. The answer keys must never reach the participant's browser. Score from the log afterwards.
6. Use the same task instruction in every condition. Add only one sentence that explains the controls on that screen.
7. State in the report and README that the AI agent is simulated with pre-written summaries containing planted mistakes.

## 3. Two design choices that affect what the study shows

- **`year_on_year` in Condition C.** This list is built from the documents, not from the summary, so it shows the omitted change in every set. If you include it, Condition C will probably catch the omission far more often. That is a real effect of your design, but report that the view was present. If it is not built, leave the field unused.
- **`check_hint` in Condition C.** It adds no information beyond the status badge; it only orders attention. It will not help with the one error per set that is marked Supported.

## 4. Measures these materials support

| Measure | How to compute | Requirement |
|---|---|---|
| Share of planted errors found | incorrect claims marked wrong ÷ 5 | UR-01 (target ≥ 80% in C) |
| False-rejection rate | correct claims marked wrong ÷ 7 | UR-03 (target ≤ 15%) |
| Year-on-year errors found | CMP and OMI marked wrong ÷ 2 | UR-06 (target ≥ 80%) |
| Flagged claims inspected (B and C) | sources opened for the 5 claims with an Uncertain or Discrepancy cue ÷ 5 | UR-04 (target ≥ 85%) |
| Over-trust trap | whether the High-confidence wrong figure (FIG) was caught | Calibrated trust |
| Under-trust trap | whether the Uncertain but correct claim was rejected | Calibrated trust |
| Time per task | end time minus start time | UR-09 |
| Correct final decision | approve with corrections or reject | UR-07 |
