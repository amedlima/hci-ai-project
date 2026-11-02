# Delegating to AI Agents: Interfaces That Make Checking Easy

A prototype web app and user study for LZSCC.241 Human-Computer Interaction.

## What is this project?

More and more work is delegated to AI agents, for example "summarise this client's credit file and flag anything that differs from last year". The human's job then shifts from doing the work to checking the AI's result and being responsible for it. People tend to over-trust fluent answers, and checking long documents is slow.

We are designing and testing an interface for delegating a document task to an AI agent that makes mistakes easy to find and makes responsibility clear.

**Research question:** Do interfaces that show sources, uncertainty and a clear sign-off step help people find AI mistakes better, and know who is responsible, than interfaces that show only the AI's answer?

## Conditions compared

| Condition | Description |
|---|---|
| A | Plain AI answer only (baseline) |
| B | Answer with source links, highlights and a confidence note |
| C | Our own design: checking workflow, side-by-side evidence, approval step and audit log |

We run a within-subject study (every participant tries every condition, with counterbalanced order) using synthetic documents with deliberately planted errors in the AI summary.

## Project status

Early stage (week 1: planning). See the wiki for the current state.

## Documentation

- [Project Plan](../../wiki/Project-Plan)
- [Weekly Log](../../wiki/Weekly-Log)
- [Contributions](../../wiki/Contributions)
- Task board: 

## Team

Muslima Akhmedova, Demirhan Demir, Hashir Sarfaraz Mian, Thaqi Sadathulla Syed, Alexandr Tichonov, Alen Yildiz

Roles and individual contributions are on the wiki Contributions page.

## Requirements and installation

*To be completed once the prototype exists. The final version will cover:*

- Required software and versions: TBC
- How to install: TBC (ideally one setup script or a short list of commands)
- How to compile: TBC
- How to run: TBC
- How to reproduce the analysis: TBC
- Example of expected output: TBC

Tested on an Ubuntu lab computer: not yet.

## What is simulated

- **The AI agent:** TBC (pre-written summaries with planted errors, and/or a local LLM such as Ollama)
- **The client documents:** synthetic, made up by us. No real client data is used.

## Data and privacy

- Only synthetic documents are used.
- Study data in this repository is anonymised. We never publish participant names, signed consent forms, photos or recordings.

## AI-use statement

We use AI tools in this project as allowed by the course. We state here which tools we used and for which parts. AI-assisted files or commits are marked in the commit message or the table below.

| Tool | Used for | Files / commits | Team member |
|---|---|---|---|
| GitHub Copilot | Code suggestions for the logging module | ` ` |  |

Every team member can explain the code they committed.

## Licence

TBC
