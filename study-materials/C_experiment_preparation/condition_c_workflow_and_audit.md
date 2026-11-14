# Condition C: checking workflow, sign-off and audit record

Content needed for the Condition C screens. The claims, sources and cues come from the same set JSON as the other conditions.

## 1. Workflow

1. **Review queue.** The 12 claims as cards, each with its status badge (icon and text label, never colour alone), confidence and agent note.
2. **Inspect.** Selecting a claim shows its source passages next to it, highlighted in the document (`claims[].sources[].element_id` and `highlight`).
3. **Decide.** Each claim gets one decision: **Approve**, **Edit** (the reviewer types the corrected sentence) or **Reject**. Decisions can be undone until sign-off.
4. **Sign-off gate.** Sign-off is blocked while any claim is undecided; a warning is shown if a claim marked Uncertain or Discrepancy was decided without opening its source (SR-01).
5. **Sign-off.** The reviewer chooses the final decision and confirms the statement below.
6. **Audit record.** Shown after sign-off and saved to the log.

## 2. Sign-off statement

> I have reviewed the AI agent's draft summary against the client documents. I have approved, corrected or rejected each statement. I understand that I, not the AI agent, am responsible for the summary I approve.

Final decision options: **Approve as written**, **Approve with my corrections**, **Reject and return to the agent**.

## 3. Audit record fields

| Field | Meaning |
|---|---|
| `record_id`, `set_id`, `condition` | Which task this record belongs to |
| `reviewer_id` | Anonymous participant ID (P01 to P10), never a name |
| `agent_output` | What the agent produced: number of claims, statuses it assigned |
| `events[]` | Time-stamped actions: `task_started`, `document_opened`, `source_opened`, `claim_decision`, `decision_undone`, `signoff_blocked`, `signoff_completed` |
| `claim_decisions[]` | For each claim: final decision, whether its source was opened, the corrected text if edited |
| `signoff` | Final decision, statement confirmed, time |
| `summary_counts` | Approved, edited, rejected, sources opened |

A third person should be able to read the record and say what the agent did, what the human checked, and who approved what. `audit_log_example.json` shows a complete example for Set 1. It contains no correctness information, so it is safe to display to the participant.

The same event log, without the sign-off parts, should be recorded in Conditions A and B for analysis.
