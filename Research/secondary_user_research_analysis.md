# Secondary User Research Analysis

## 1. Introduction

To design a helpful interface, we first need to understand our potential users, how they currently work with AI, and what goes wrong when they delegate document tasks to an AI agent. Instead of relying on guesswork before building our prototype, this document analyses real user data from six published Human-Computer Interaction (HCI) studies, covering a combined total of $N = 1,240$ participants.

Looking at this existing user data helps us see common user habits, frustrations and mistakes when people check AI-generated summaries. These findings directly shape the requirements and design rules in [User Requirements and Design Guidelines](./user_requirements_and_design_guidelines.md).

## 2. Target Users and Scenarios

In this project, the target users and their main tasks are defined as follows:

- **Target Users:** Analysts, clerks and managers who work with heavy documents in areas like finance, banking, law, insurance and healthcare administration. These users delegate routine reading and summarising tasks to AI agents to save time.
- **Scenario A (Summarising a File and Spotting Changes from Last Year):** A financial analyst asks an AI agent to summarise a client's multi-page credit file and point out anything that does not match last year's record. The user then has to check the AI's summary against the original documents to catch any mistakes or made-up facts (hallucinations).
- **Scenario B (Approving the Draft with a Clear Record of Responsibility):** A manager or clerk reviews the AI agent's draft summary before it is sent to a client or saved to a record. The user must check, fix or reject wrong statements and complete a clear sign-off step. This creates an audit log showing what the AI did, what the human checked and who approved the final result.

## 3. Summary of Existing User Studies

The user insights in Section 4 come from the following user studies reviewed in our [Literature Review](./literature_review.md):

| Study reference | Participants and method | What users had to do | What the study measured |
|---|---|---|---|
| [Kim *et al.* (2025), Literature Review, Section 2.2](./literature_review.md#22-fostering-appropriate-reliance-on-large-language-models-the-role-of-explanations-sources-and-inconsistencies) | $N = 308$ participants; controlled user experiment | Check AI-generated answers with and without AI explanations, source links and highlighted contradictions | How often users trusted wrong AI answers (over-trust), rejected right answers (under-trust) and clicked on source links |
| [Kim *et al.* (2024), Literature Review, Section 2.4](./literature_review.md#24-im-not-sure-but-examining-the-impact-of-large-language-models-uncertainty-expression-on-user-reliance-and-trust) | $N = 404$ participants; controlled user experiment | Review AI answers written either in a confident tone or with clear uncertainty notes | How confident users felt, how often they agreed with wrong AI answers and their overall accuracy |
| [Bansal *et al.* (2021), Literature Review, Section 2.5](./literature_review.md#25-does-the-whole-exceed-its-parts-the-effect-of-ai-explanations-on-complementary-team-performance) | $N = 528$ participants; multi-condition user study | Complete reading and decision tasks with AI suggestions and explanations | Combined human-AI accuracy and how often users blindly agreed with the AI when it was wrong |
| [Westphal *et al.* (2023), Literature Review, Section 2.6](./literature_review.md#26-decision-control-and-explanations-in-human-ai-collaboration-improving-user-perceptions-and-compliance) | Controlled user study on human-AI teamwork | Review AI suggestions with different levels of user control and explanation length | How mentally tiring the task felt, how much control users felt they had and whether they followed the workflow |
| [Fok and Weld (2024), Literature Review, Section 2.3](./literature_review.md#23-in-search-of-verifiability-explanations-rarely-enable-complementary-performance-in-ai-advised-decision-making) | Review and analysis of multiple human-AI user studies | Check AI answers using AI explanations versus checking original source evidence directly | How long checking took, how many errors users caught and whether the human-AI team beat the AI alone |

## 4. What Users Do Now and What Goes Wrong

### 4.1 Pain Point 1: Trusting Fluent AI Answers Too Much (Automation Bias)

- **What users do now:** When people use standard AI chat tools (which matches **Condition A** in this project), they read a smooth, well-written summary paragraph and quickly skim it to see if it sounds reasonable.
- **What goes wrong (Evidence from User Data):** Across $N = 528$ users in [Bansal *et al.* (2021)](./literature_review.md#25-does-the-whole-exceed-its-parts-the-effect-of-ai-explanations-on-complementary-team-performance) and $N = 308$ users in [Kim *et al.* (2025)](./literature_review.md#22-fostering-appropriate-reliance-on-large-language-models-the-role-of-explanations-sources-and-inconsistencies), people showed strong **over-trust (automation bias)**. Because the AI writes in a confident, natural style, users frequently accept wrong or made-up claims without questioning them. Even worse, when the AI gives a convincing-sounding explanation *without* showing the original source text, users actually trust wrong answers *more* than when no explanation is given.
- **What this means for our design:** Showing a plain AI summary is unsafe for important documents. Our interface needs to break long summaries into separate, bite-sized claims and link each one to the original document text (`UR-01`, `UR-02`).

### 4.2 Pain Point 2: Checking Long Documents by Hand is Slow and Tiring

- **What users do now:** To check if a number, date or rule in an AI summary matches a long client PDF, users currently have to switch between windows, scroll up and down through pages, or use `Ctrl+F` to search for keywords across different files.
- **What goes wrong (Evidence from User Data):** [Fok and Weld (2024)](./literature_review.md#23-in-search-of-verifiability-explanations-rarely-enable-complementary-performance-in-ai-advised-decision-making) show that when checking the original source takes too much time and effort, users get tired and stop checking carefully. Instead, they start guessing or trusting the AI to save time, which causes them to miss small but important mistakes—like a figure in a client's credit file changing from last year.
- **What this means for our design:** Checking must be fast and effortless. Clicking a source link on any AI claim should immediately scroll to and highlight the exact matching paragraph in the document right next to it (`UR-02`, `UR-06`, `DG-01`).

### 4.3 Pain Point 3: Missing Contradictions When There Are No Visual Warnings

- **What users do now:** Even when an AI tool gives numbered citation links (like in Adobe Acrobat AI or Gemini Notebook, which matches **Condition B** in this project), users usually click the first one or two links, see that they look fine, and assume the rest of the summary is also correct.
- **What goes wrong (Evidence from User Data):** In [Kim *et al.* (2025)](./literature_review.md#22-fostering-appropriate-reliance-on-large-language-models-the-role-of-explanations-sources-and-inconsistencies) ($N = 308$), users often missed cases where the AI summary said the opposite of the source document unless the interface clearly pointed out the **contradiction**. When the interface visually flagged conflicting information alongside the source text, users caught far more AI mistakes.
- **What this means for our design:** Our interface should clearly label whether a claim is *Supported*, has a *Discrepancy/Contradiction*, or is *Uncertain*, and give visual hints on which claims need the most attention (`UR-03`, `UR-04`, `DG-02`).

### 4.4 Pain Point 4: Not Knowing When the AI is Guessing (Over-Trust vs. Under-Trust)

- **What users do now:** Once users realise an AI can make mistakes, two problems happen: some users become overly suspicious and waste time rejecting correct statements (**under-trust** / false rejections), while others still accept low-confidence AI guesses (**over-trust**).
- **What goes wrong (Evidence from User Data):** In [Kim *et al.* (2024)](./literature_review.md#24-im-not-sure-but-examining-the-impact-of-large-language-models-uncertainty-expression-on-user-reliance-and-trust) ($N = 404$), standard confident AI wording made it hard for users to judge when to trust the system. However, when the AI expressed **uncertainty** in plain, everyday wording on claims it was unsure about, users knew exactly where to focus their checking. They rejected wrong claims more often while still accepting accurate ones, which improved their overall score.
- **What this means for our design:** The interface must show clear, easy-to-read uncertainty notes when a claim lacks strong evidence (`UR-04`, `DG-03`). In our evaluation, we also need to measure both missed errors (over-trust) and falsely rejected correct claims (under-trust).

### 4.5 Pain Point 5: Information Overload and Unclear Responsibility

- **What users do now:** When an AI generates a finished draft on its own, human reviewers often fall into a "rubber-stamping" habit—clicking approve without feeling personally responsible for the result. On the other hand, if the interface shows long, complicated AI explanations for every sentence, users feel overwhelmed.
- **What goes wrong (Evidence from User Data):** [Westphal *et al.* (2023)](./literature_review.md#26-decision-control-and-explanations-in-human-ai-collaboration-improving-user-perceptions-and-compliance) found that long explanations made tasks feel much more mentally exhausting without helping users perform better. By contrast, giving users direct **decision control** (buttons to accept, edit or reject items) made them feel more engaged and responsible. Similarly, [Balakayeva *et al.* (2025)](./literature_review.md#28-an-intelligent-enterprise-system-with-processing-and-verification-of-business-documents-using-big-data-and-ai) show that in business workflows, responsibility stays blurry unless there is a required human sign-off step and an audit log.
- **What this means for our design:** Keep evidence highlights short and simple to avoid mental overload (`DG-05`), give users clear *Approve*, *Edit* and *Reject* buttons for each claim (`UR-05`), and require a final sign-off checkbox that saves a clear audit log of who approved what (`UR-07`, `UR-08`, `DG-04`, `DG-06`).

## 5. Connecting User Pain Points to Project Requirements

The table below shows how each user problem from the studies connects to our requirements in [User Requirements and Design Guidelines](./user_requirements_and_design_guidelines.md):

| User problem found in the studies | Supporting user study data | Matching requirement and design guideline |
|---|---|---|
| Users trust smooth, plain AI paragraphs too easily | Bansal *et al.* (2021) ($N = 528$); Kim *et al.* (2025) ($N = 308$) | `UR-01` (Break summary into claims), `UR-02` (Source links) |
| Searching through long PDFs by hand is slow and tiring | Fok & Weld (2024); Morrison *et al.* (2023) | `UR-02` (Fast click-to-highlight source view), `UR-06` (Year-over-year diff), `DG-01` (Side-by-side layout) |
| Users miss subtle contradictions and changes from last year | Kim *et al.* (2025) ($N = 308$) | `UR-03` (Status labels), `UR-04` (Checking hints), `DG-02` (Accessible badges) |
| Users either blindly accept guesses or wrongly reject true claims | Kim *et al.* (2024) ($N = 404$) | `UR-04` (Uncertainty notes), `DG-03` (Plain-language uncertainty) |
| Long AI explanations overwhelm users and increase workload | Westphal *et al.* (2023) | `UR-09` (Keep workload low on NASA-TLX), `DG-05` (Keep evidence simple) |
| Passive reviewing leads to "rubber-stamping" and unclear responsibility | Westphal *et al.* (2023); Balakayeva *et al.* (2025) | `UR-05` (Accept/edit/reject buttons), `UR-07` (Sign-off step), `UR-08` (Audit log), `DG-04`, `DG-06` |

## 6. Limitations and Next Steps

Using data from published user studies ($N = 1,240$ participants in total) gives us strong evidence of how people behave when checking AI outputs before we build our prototype. However, as an honest limitation, these studies tested general AI question-answering and business document tasks rather than our exact interface. To address this, we will run our own within-subject user study ($5\text{--}10$ participants) once our prototype is built, using automatic logging, NASA-TLX, SUS questionnaires and short interviews to test our design directly.

## 7. Declaration of AI Usage

AI tools were used as supporting tools throughout the preparation of this secondary user research analysis for the following purposes:

- Identifying participant numbers and user behaviour findings from the reviewed research papers.
- Organising user pain points around the project's target users and scenarios.
- Connecting the user study findings to our testable requirements and design guidelines.
- Structuring and formatting the `secondary-user-research-analysis.md` file.
