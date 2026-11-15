# Delegating to AI Agents: Interfaces That Make Checking Easy

A prototype web app and user study for LZSCC.241 Human-Computer Interaction (Project 6).

## What is this project?

More and more work is delegated to AI agents, for example "summarise this client's credit file and flag anything that differs from last year". The human's job then shifts from doing the work to checking the AI's result and being responsible for it. People tend to over-trust fluent answers, and checking long documents is slow.

We are designing and testing an interface for delegating a document task to an AI agent that makes mistakes easy to find and makes responsibility clear.

**Research question:** Do interfaces that show sources, uncertainty and a clear sign-off step help people find AI mistakes better, and know who is responsible, than interfaces that show only the AI's answer?

## Conditions compared

| Condition | Description |
|---|---|
| A | Plain AI answer only (baseline) |
| B | Answer with source links, highlights and a confidence note |
| C | Our own design: claim-by-claim checking, side-by-side evidence, sign-off step and audit record |

We run a within-subject study: every participant tries every condition, in counterbalanced order, with a different synthetic client file in each. The AI summaries contain deliberately planted mistakes.

## Project status

**Week 3 (9–15 Nov): design phase complete.**

| Phase | Status |
|---|---|
| Research and requirements | Done |
| Design: sketches, storyboard, wireframes, low-fidelity prototype tested with 2 people | Done |
| Study materials: synthetic client documents and AI summaries | Done |
| Prototype v1 (web app) | Starts in week 4 |
| User study and analysis | Planned for weeks 6–7 |

## Repository contents

| Folder | Contents |
|---|---|
| [`Research/`](./Research) | [Literature review](./Research/literature_review.md), [analysis of existing solutions](./Research/analysis_of_existing_solutions.md), [secondary user research](./Research/secondary_user_research_analysis.md), [user requirements](./Research/user_requirements.md) |
| [`Design/`](./Design) | [Design document](./Design/design.md): alternatives, storyboard, wireframes for Conditions A, B and C, design rationale and the low-fidelity test |
| [`study-materials/`](./study-materials) | Synthetic client documents, AI summaries and task instructions for three client files and a practice file |

## Documentation

- [Project Plan](../../wiki/Project-Plan)
- [Weekly Log](../../wiki/Weekly-Log)
- [Contributions](../../wiki/Contributions)
- [Task board](https://github.com/users/amedlima/projects/1)
## Team

Muslima Akhmedova, Demirhan Demir, Hashir Sarfaraz Mian, Thaqi Sadathulla Syed, Alexandr Tichonov, Alen Yildiz

Roles and individual contributions are on the wiki [Contributions](../../wiki/Contributions) page.

## Requirements and installation

The prototype does not exist yet. This section will be completed with prototype v1 and will cover: required software and versions, how to install, how to compile, how to run, how to reproduce the analysis, and an example of expected output.

Tested on an Ubuntu lab computer: not yet.

## What is simulated

- **The AI agent:** simulated with pre-written summaries that contain deliberately planted mistakes. No live AI model produces the summaries.
- **The client documents:** synthetic, made up for this project. No real client data is used.
- **The low-fidelity prototype:** a click-through in Figma with pre-filled decisions and one linked path.

## Data and privacy

- Only synthetic documents are used.
- Study data in this repository will be anonymised. We never publish participant names, signed consent forms, photos or recordings.
- The answer keys for the study materials are kept out of this repository until the study is finished, so participants cannot see them.

## AI-use statement

We use AI tools in this project as allowed by the course. This table states which tools we used and for which parts. AI-assisted commits are also marked in the commit message.

| Tool | Used for | Files | Team member |
|---|---|---|---|
| AI tool | Supporting the research documents | `Research/` | Hashir Sarfaraz Mian |
| Claude  | Synthetic client documents | `study-materials/` | Muslima Akhmedova |
| Claude  | Storyboard, the design document | `Design/` | Muslima Akhmedova |


## Licence

TBC
