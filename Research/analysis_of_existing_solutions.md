# Analysis of Existing Solutions

## 1. Introduction

This analysis examines 11 existing software products and AI-powered platforms that provide functionality related to document summarisation, claim-level verification, source traceability, discrepancy detection, version comparison and human oversight with audit logging.

The objective is to understand how existing commercial and research solutions address these capabilities, identify their strengths and limitations in relation to delegating document tasks to AI agents, and establish practical interface patterns that inform the prototype design in this project.

The selected platforms cover AI fact-checking, document intelligence, legal and financial compliance, academic literature synthesis and document version comparison.

## 2. Evaluation Criteria

The platforms are evaluated against the following capabilities required for this project:

- **Document analysis:** Ability to upload, extract and process multi-page client or enterprise documents.
- **AI summarisation:** Ability to generate structured summaries and extract key points from documents.
- **Claim-level verification:** Ability to break outputs into individual statements that can be checked independently.
- **Source traceability:** Ability to link generated claims directly to highlighted passages in the original source documents.
- **Contradiction and discrepancy detection:** Ability to flag conflicting evidence, unsupported claims or differences from previous documents (e.g., year-over-year changes).
- **Uncertainty communication:** Ability to communicate confidence levels or warn when a statement cannot be verified.
- **Human oversight and audit trail:** Ability to let users review, edit, approve or reject AI findings, and record a traceable log of who decided what.

> [!NOTE]
> The advantages and disadvantages below are assessed specifically in relation to this project. A limitation means that a particular capability is not established in public documentation or falls outside the product's primary purpose; it does not mean that the product performs poorly in its target market.

## 3. Existing Solutions

### 3.1 AI Verification and Fact-Checking Platforms

#### 3.1.1 Factiverse

**Product:** [https://www.factiverse.ai/](https://www.factiverse.ai/)

**Domain:** AI fact-checking, hallucination detection, media monitoring and LLM output evaluation.

**Brief description:**

Factiverse is an AI-powered claim detection and verification platform. It analyses text to segment individual factual claims and evaluates them against reference sources. Its interface distinguishes between supported, disputed and mixed claims, displaying retrieved evidence snippets alongside each claim.

**Advantages:**
- Automatically segments longer text into individual checkable claims.
- Retrieves and displays supporting and contradicting evidence side by side.
- Classifies each claim with a clear verification status badge.
- Explicitly targets hallucination detection in LLM-generated text.

**Disadvantages:**
- Primarily verifies claims against web or external databases rather than comparing a client's current file against last year's internal file.
- Focuses on claim assessment rather than providing an end-to-end document approval and sign-off workflow.
- Public documentation does not establish a formal third-party audit trail of human sign-off decisions.

**Relevance to the project:**

Factiverse is one of the closest functional references for claim segmentation in this project. Its pattern of breaking an AI summary into discrete claims with status badges (Supported, Disputed, Unverified) directly informs our Condition C interface.

#### 3.1.2 Full Fact AI

**Product:** [https://fullfact.ai/product/](https://fullfact.ai/product/)

**Domain:** Fact-checking workflows, misinformation monitoring and collaborative human verification.

**Brief description:**

Full Fact AI helps verification teams identify and investigate potentially misleading statements. It pairs automated claim detection with a structured human review queue where reviewers inspect flagged statements, evaluate priority scores and explicitly confirm or dismiss claims.

**Advantages:**
- Provides a structured human review queue for confirming or dismissing AI-flagged claims.
- Clearly separates automated detection from the final human verification judgement.
- Tracks previously reviewed claims and records reviewer decisions.
- Prioritises which claims most urgently require human checking.

**Disadvantages:**
- Designed for monitoring public broadcasts and news rather than summarising confidential client files.
- Its harm scoring focuses on public impact rather than factual source alignment within uploaded PDFs.

**Relevance to the project:**

Full Fact AI is a strong reference for human-in-the-loop control and hints on which claims most need checking. Its review queue demonstrates how an interface can guide a human reviewer through flagged items before completing sign-off.

#### 3.1.3 Scite

**Product:** [https://scite.ai/](https://scite.ai/)

**Domain:** Academic evidence evaluation, citation analysis and source-grounded AI synthesis.

**Brief description:**

Scite analyses how publications reference one another and classifies citations as *Supporting*, *Contrasting* or *Mentioning* a claim. Its AI assistant generates answers grounded in literature while exposing the exact supporting or contrasting snippets behind every statement.

**Advantages:**
- Explicitly distinguishes between supporting, contrasting and merely mentioning evidence.
- Displays the exact surrounding text snippet from the source document.
- Helps users immediately spot when a source contradicts a stated claim.

**Disadvantages:**
- Specialised for scientific literature rather than financial, legal or administrative client files.
- Does not include a human editing, approval or compliance sign-off log for generated summaries.

**Relevance to the project:**

Scite inspires the contradiction-detection indicators in this project. Showing whether a linked source passage actively *supports* or *contradicts* a summary claim helps users catch subtle errors much faster than plain citation links.

### 3.2 AI Document Summarisation and Traceability Platforms

#### 3.2.1 Adobe Acrobat AI Assistant

**Product:** [https://www.adobe.com/acrobat/generative-ai-pdf.html](https://www.adobe.com/acrobat/generative-ai-pdf.html)

**Domain:** PDF document analysis, summarisation and inline citation traceability.

**Brief description:**

Adobe Acrobat AI Assistant integrates generative AI summaries directly alongside PDF documents. It generates structured overviews and answers user queries with clickable numbered citations that scroll to and highlight the corresponding passage in the original PDF.

**Advantages:**
- Generates structured summaries of multi-page PDF documents.
- Provides clickable inline citations linked to exact locations in the source document.
- Automatically scrolls to and highlights the relevant passage in the adjacent PDF viewer.
- Supports analysing multiple documents within a workspace.

**Disadvantages:**
- Citations show where text was retrieved from, but the interface does not warn users when the AI misinterprets a figure or misses a contradiction.
- Does not provide claim-by-claim accept/reject controls or an accountable sign-off workflow.
- Presents responses in a confident tone without explicit claim-level uncertainty indicators.

**Relevance to the project:**

Adobe Acrobat AI Assistant represents a practical reference for **Condition B** in this project (an interface showing the AI summary with clickable source links and passage highlights, but lacking structured claim sign-off and audit logging).

#### 3.2.2 Gemini Notebook (formerly NotebookLM)

**Product:** [https://notebook.google.com/](https://notebook.google.com/)

**Domain:** Source-grounded document synthesis and research analysis.

**Brief description:**

Gemini Notebook allows users to upload source documents and generate grounded summaries and briefings. Hovering over or clicking inline citations displays the exact quoted passage from the uploaded source material alongside the generated summary.

**Advantages:**
- Strictly grounds generated summaries in user-uploaded documents.
- Displays direct source quotations immediately upon interacting with a citation badge.
- Supports comparing information across multiple uploaded files (e.g., two annual files).

**Disadvantages:**
- Does not classify whether a cited passage genuinely supports or contradicts the generated sentence.
- Lacks an editing, approval or audit-trail mechanism for regulated sign-off workflows.
- Does not explicitly express uncertainty on individual extracted claims.

**Relevance to the project:**

Gemini Notebook provides an exemplary interaction pattern for fast evidence inspection (hover/click citation previews) that reduces the time cost of checking source documents.

#### 3.2.3 Hebbia

**Product:** [https://www.hebbia.com/](https://www.hebbia.com/)

**Domain:** Financial due diligence, banking, legal analysis and enterprise document intelligence.

**Brief description:**

Hebbia is an enterprise document analysis platform built for financial analysts and legal teams. Its Matrix interface organises multi-document extractions into structured rows and columns, linking every extracted cell to exact verbatim quotes in the underlying client files.

**Advantages:**
- Purpose-built for the target users of this project (financial analysts, legal clerks and due-diligence managers).
- Breaks dense document summaries into a structured, inspectable grid.
- Links every extracted figure or clause directly to highlighted source passages.
- Supports cross-document comparison (e.g., comparing financial statements across years).

**Disadvantages:**
- Enterprise-scale matrix layouts can be complex for straightforward single-client summary sign-offs.
- Public documentation focuses on extraction speed rather than explicit human accountability sign-off logs.

**Relevance to the project:**

Hebbia demonstrates how financial and legal professionals verify AI-delegated document tasks in practice, validating a side-by-side layout that pairs structured AI claims with verbatim source evidence.

#### 3.2.4 Litera Kira

**Product:** [https://www.litera.com/products/kira](https://www.litera.com/products/kira)

**Domain:** Legal contract review, clause comparison and compliance auditing.

**Brief description:**

Litera Kira extracts key provisions from contracts and financial agreements, displaying the AI-extracted summary alongside the original document viewer. It highlights differences between clauses and allows legal analysts to review and validate extracted fields.

**Advantages:**
- Side-by-side document viewer with synchronized passage highlighting.
- Flags deviations and differences across contract versions or standard templates.
- Allows human reviewers to confirm or edit extracted summaries during due diligence.

**Disadvantages:**
- Highly specialised around legal clause taxonomies rather than general narrative client summaries.
- Does not focus on communicating generative LLM uncertainty in natural language.

**Relevance to the project:**

Kira directly informs the side-by-side verification layout in this project and demonstrates how professionals compare current documents against prior baselines while tracking review status.

#### 3.2.5 Anara

**Product:** [https://anara.com/](https://anara.com/)

**Domain:** Document analysis, source-linked summarisation and evidence annotation.

**Brief description:**

Anara provides an integrated workspace combining an AI summary panel on one side with an interactive PDF viewer on the other. Clicking any sentence or citation badge in the AI output immediately highlights the exact paragraph in the PDF.

**Advantages:**
- Clean, low-clutter split-screen interface pairing the AI summary with the source PDF.
- Bidirectional linking between summary claims and highlighted source text.
- Lowers the visual search effort required to locate evidence in long documents.

**Disadvantages:**
- Does not automatically flag semantic contradictions or express claim-level uncertainty.
- Lacks a formal accept/reject sign-off step or compliance audit log.

**Relevance to the project:**

Anara serves as a clean visual benchmark for the split-screen UI design in this project, ensuring that source navigation remains fast and uncluttered.

#### 3.2.6 Elicit

**Product:** [https://elicit.com/](https://elicit.com/)

**Domain:** Evidence synthesis, structured data extraction and human screening.

**Brief description:**

Elicit extracts structured claims and findings from documents into reviewable tables, providing supporting quotes for each extraction and allowing human users to override AI screening judgements.

**Advantages:**
- Presents supporting quotes directly beneath or beside every AI extraction.
- Explicitly allows users to override and correct AI decisions.
- Tracks human screening criteria and overrides systematically.

**Disadvantages:**
- Tailored to academic literature reviews rather than client financial or administrative files.
- Does not generate a compliance sign-off certificate or third-party audit log for individual client cases.

**Relevance to the project:**

Elicit illustrates how human override controls can be embedded directly into each row of an AI summary so users can correct mistakes inline.

### 3.3 Regulated Compliance and Version Comparison Tools

#### 3.3.1 Spektr AI for Doc Review

**Product:** [https://www.spektr.com/ai-agent/ai-for-doc-review](https://www.spektr.com/ai-agent/ai-for-doc-review)

**Domain:** Financial compliance, banking onboarding, discrepancy detection and audit logging.

**Brief description:**

Spektr automates the review of client compliance files in regulated financial institutions. It cross-checks extracted client data across documents, flags discrepancies or outdated information, escalates uncertain cases to a human compliance officer and records an immutable audit trail of who approved or rejected the file.

**Advantages:**
- Built specifically for regulated financial workflows requiring strict human accountability.
- Automatically flags discrepancies and conflicting data across client records.
- Enforces an explicit human approval or rejection step before a case is completed.
- Generates a third-party readable audit trail recording AI actions and human sign-off decisions.

**Disadvantages:**
- Focuses primarily on structured KYC fields rather than free-text narrative document summaries.
- Relies heavily on external registry integrations that are outside the scope of this project.

**Relevance to the project:**

Spektr is the primary commercial reference in this project for **accountability, human sign-off and audit trail logging**—directly addressing the need to record what the agent did, what the human checked and who approved the final output.

#### 3.3.2 ABBYY FineReader PDF (Document Comparison)

**Product:** [https://pdf.abbyy.com/finereader-pdf/](https://pdf.abbyy.com/finereader-pdf/)

**Domain:** Document version comparison ("diffing") and PDF discrepancy highlighting.

**Brief description:**

ABBYY FineReader includes a dedicated Compare Documents view that aligns two versions of a file side by side (such as last year's client statement and this year's statement) and highlights additions, deletions and changed figures in a change log.

**Advantages:**
- Synchronised side-by-side scrolling across two versions of a document.
- Automatically highlights numerical and textual changes between years.
- Generates a structured list of changes that users can step through one by one.

**Disadvantages:**
- Performs lexical/character-level comparison rather than semantic AI summarisation.
- Cannot verify whether an AI-generated summary faithfully reflects the underlying documents.

**Relevance to the project:**

ABBYY's comparison view directly informs **Scenario A** in this project (*summarising a client file and flagging differences from last year*) as well as a *"what changed since last time"* view.

## 4. Comparative Feature Matrix

The following matrix compares the 11 platforms against the core requirements of this project.

**Legend:**
- **Yes:** Capability is explicitly supported in the product's core workflow.
- **Partial:** Related functionality exists, but does not fully satisfy this project's specific verification or sign-off need.
- **No:** The capability is absent or outside the product's purpose.

| Platform | Document summarisation | Claim-level breakdown | Inline source traceability | Contradiction / year-over-year diff | Uncertainty indicator | Human accept/reject controls | Accountable sign-off & audit log |
|---|---|---|---|---|---|---|---|
| Factiverse | Partial | Yes | Yes | Yes (disputed claims) | Yes | Partial | No |
| Full Fact AI | Partial | Yes | Yes | Yes | Partial (harm score) | Yes | Partial |
| Scite | Yes | Yes | Yes | Yes (contrasting citations) | No | No | No |
| Adobe Acrobat AI | Yes | No | Yes | No | No | No | No |
| Gemini Notebook | Yes | No | Yes | Partial (multi-source) | No | No | No |
| Hebbia | Yes | Yes | Yes | Partial | No | Partial | Partial |
| Litera Kira | Yes | Yes | Yes | Yes (clause diff) | No | Yes | Partial |
| Anara | Yes | No | Yes | No | No | No | No |
| Elicit | Yes | Yes | Yes | Partial | No | Yes | No |
| Spektr | Partial | Yes (fields) | Yes | Yes (discrepancies) | Yes (escalation) | Yes | Yes |
| ABBYY FineReader | No | No | No | Yes (version diff) | No | Partial (annotations) | No |

> [!NOTE]
> As shown in the matrix, existing mainstream AI document tools (such as Adobe Acrobat AI and Gemini Notebook) provide source links but lack contradiction flags, explicit uncertainty notes, claim-level accept/reject controls and an accountable sign-off audit log. Bridging this gap is the core contribution of this project.

## 5. Implications for the Project

Based on the analysis of existing solutions, the following interface capabilities are selected for the prototype in this project:

| Proposed prototype capability | Inspired by existing solutions | Target condition in this project |
|---|---|---|
| Inline citations with click-to-highlight source passages | Adobe Acrobat AI, Gemini Notebook, Anara | Condition B & Condition C |
| Claim-level uncertainty / confidence indicators | Factiverse, Spektr | Condition B & Condition C |
| Discrete claim segmentation with status badges (Supported, Discrepancy, Uncertain) | Factiverse, Scite | Condition C (Custom Design) |
| Year-over-year discrepancy highlighting ("what changed since last year") | ABBYY FineReader, Litera Kira, Hebbia | Condition C (Scenario A) |
| Hints prioritising which claims most need human checking | Full Fact AI, Spektr | Condition C (Custom Design) |
| Claim-by-claim human accept, edit and reject controls | Full Fact AI, Elicit, Litera Kira | Condition C (Scenario B) |
| Explicit final human sign-off step blocking unapproved actions | Spektr | Condition C (Scenario B) |
| Third-party readable audit log of AI outputs, human checks and sign-off | Spektr | Condition C (Scenario B) |

## 6. Declaration of AI Usage

AI tools were used as supporting tools throughout the preparation of this analysis of existing solutions for the following purposes:

- Identifying relevant commercial products and applications across fact-checking, document intelligence and compliance domains.
- Suggesting relevant research terms and discovery directions.
- Reviewing product documentation and identifying relevant functionalities.
- Organising product information into advantages, limitations and project relevance.
- Comparing the capabilities of different platforms against the project's requirements.
- Structuring and formatting the `analysis-of-existing-solutions.md` file.

> [!NOTE]
> AI assisted in the research and analysis. Product capabilities were evaluated using public documentation rather than direct commercial testing.
