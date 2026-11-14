# Study materials: synthetic client documents and AI summaries

Materials for the user study in *Delegating to AI Agents: Interfaces That Make Checking Easy* (LZSCC.241, Project 6). Everything here is synthetic: the bank, the clients, the people, the figures and the dates are invented. The "AI agent" is simulated with pre-written summaries that contain deliberately planted mistakes.

## Contents

### Part A: participant materials (`A_participant_materials/`)

| Folder | Client | Contents |
|---|---|---|
| `practice/` | Lark & Lantern Bakery Ltd | task instruction, 2 client documents, AI summary (plain and with evidence), `practice.json` |
| `set1/` | Harlow & Finch Joinery Ltd | task instruction, 4 client documents, AI summary (plain and with evidence), `set1.json` |
| `set2/` | Tidewell Freight Services Ltd | task instruction, 4 client documents, AI summary (plain and with evidence), `set2.json` |
| `set3/` | Ashcombe Garden Centres Ltd | task instruction, 4 client documents, AI summary (plain and with evidence), `set3.json` |

- `ai_summary_plain.md` is the Condition A view. `ai_summary_with_evidence.md` is the same summary with sources and confidence notes, for Conditions B and C and for paper prototyping.
- `<set>.json` holds the documents, claims, source references and cues in one file for the prototype to load. It contains no answers.

### Part B: researcher materials (`B_researcher_materials_CONFIDENTIAL/`)

- `answer_key_<set>.md`: full claim table, each planted error explained, correct claims, scoring rules.
- `answer_keys.json`: the same keys for automatic scoring.
- `planted_error_register.md`, `correct_statement_register.md`, `source_references.md`, `difficulty_and_comparability.md`.

**Keep Part B away from participants.** If the GitHub repository is public and participants are classmates, do not push this folder until the study has finished (add it to `.gitignore` or keep it in a private location).

### Part C: experiment preparation (`C_experiment_preparation/`)

- `condition_mapping_and_counterbalancing.md`: which participant gets which set in which condition, and the session procedure.
- `keeping_conditions_consistent.md`: which data each condition shows, the rules, and the measures.
- `condition_c_workflow_and_audit.md` and `audit_log_example.json`: checking workflow, sign-off wording, audit record.

## Design at a glance

| | Each test set | Practice set |
|---|---|---|
| Client documents | 4 (request form, current-year statement, last year's review record, facility agreement) | 2 |
| Claims in the AI summary | 12 | 6 |
| Correct claims | 7 | 4 |
| Planted errors | 5 | 2 |

## AI-use statement

These study materials (documents, summaries, answer keys and experiment notes) were drafted with Claude (Anthropic). The team should review them and record this in the AI-use table in the main README. Names were invented and have not been checked against company registers; any resemblance to real organisations or people is coincidental.
