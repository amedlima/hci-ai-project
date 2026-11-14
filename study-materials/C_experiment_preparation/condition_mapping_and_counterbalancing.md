# Mapping of document sets to conditions, and counterbalancing

## 1. Design

- Within-subject: every participant completes all three conditions (A plain answer, B answer with evidence, C checking workflow).
- Each participant sees each test set exactly once, so no one meets the same documents or the same errors twice.
- The practice set is used before the first scored task and is never scored.
- No set belongs to a condition. Any set can be shown in any condition, because each set's JSON file carries everything all three conditions need.

## 2. Why both the order and the pairing are rotated

- Rotating the **order of conditions** stops practice and tiredness from favouring one interface.
- Rotating the **set-to-condition pairing** stops a slightly easier or harder set from favouring one interface.

## 3. Assignment table

Assign participants in order of arrival. Rows 1 to 6 are one complete block; rows 7 to 10 repeat rows 1 to 4.

| Participant | 1st task | 2nd task | 3rd task |
|---|---|---|---|
| P01 | Condition A, Set 1 | Condition B, Set 2 | Condition C, Set 3 |
| P02 | Condition B, Set 3 | Condition C, Set 1 | Condition A, Set 2 |
| P03 | Condition C, Set 2 | Condition A, Set 3 | Condition B, Set 1 |
| P04 | Condition A, Set 1 | Condition C, Set 3 | Condition B, Set 2 |
| P05 | Condition B, Set 3 | Condition A, Set 2 | Condition C, Set 1 |
| P06 | Condition C, Set 2 | Condition B, Set 1 | Condition A, Set 3 |
| P07 | Condition A, Set 1 | Condition B, Set 2 | Condition C, Set 3 |
| P08 | Condition B, Set 3 | Condition C, Set 1 | Condition A, Set 2 |
| P09 | Condition C, Set 2 | Condition A, Set 3 | Condition B, Set 1 |
| P10 | Condition A, Set 1 | Condition C, Set 3 | Condition B, Set 2 |

Balance within a complete block of six (P01 to P06):

- every condition appears twice in each position (first, second, third);
- every set is paired with every condition exactly twice;
- every set appears twice in each position.

One limit remains: with only six rows, the first task always pairs A with Set 1, B with Set 3 and C with Set 2. A fully crossed design needs 18 participants.

With 5 participants the design is nearly balanced; with 7 to 10 it is slightly uneven. Say so in the limitations. If you can recruit 6 or 12, the design is fully balanced.

## 4. Session procedure (about 35 to 40 minutes)

| Step | What happens | Material |
|---|---|---|
| 1 | Welcome, purpose, consent form, right to stop | Consent form |
| 2 | Practice round in the participant's first condition; answer questions; briefly show what the other two screens look like before each later task | Practice set |
| 3 | Task 1 as assigned | Set and condition from the table |
| 4 | Short questionnaire: NASA-TLX, confidence in own result, "who is responsible for the approved summary?" | Questionnaire |
| 5 | Task 2, then the same questionnaire | Set and condition from the table |
| 6 | Task 3, then the same questionnaire | Set and condition from the table |
| 7 | SUS for Condition C, short interview, thanks | SUS, interview guide |

Do not tell participants whether they found the errors until the whole session is over, and ask them not to discuss the documents with classmates who have yet to take part.

## 5. What to log for every task

Participant ID (P01 to P10), condition, set, position in session, start and end time, each claim decision with timestamp, each source or document opened, the final decision, and any corrected text. Score the log against `answer_keys.json` after the session, never on the participant's screen.
