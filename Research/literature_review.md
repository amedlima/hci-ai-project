# Literature Review

## 1. Introduction

This literature review examines eight academic papers and three foundational HCI standards relevant to designing interfaces that help users delegate document tasks to AI agents, verify AI-generated summaries, detect errors and establish clear human accountability. The research focuses on human-AI interaction, appropriate reliance, automation bias, uncertainty communication, verifiability and human-in-the-loop document workflows.

The objective is to establish an evidence-based foundation for an interface in this project that enables users to inspect AI-generated claims against source documents, identify planted or hallucinated errors and retain explicit responsibility over final decisions.

## 2. Academic Literature Review

### 2.1 Guidelines for Human-AI Interaction

**Authors:** Amershi *et al.* (2019)  
**DOI:** [10.1145/3290605.3300233](https://doi.org/10.1145/3290605.3300233)

**Brief description:**  
Introduces 18 design guidelines for effective human-AI interaction, validated across 20 AI products with 49 design practitioners. The guidelines cover setting initial expectations, displaying contextually relevant information, communicating system capabilities and supporting efficient correction and dismissal when the AI makes mistakes.

**Relevance to the project:**
- Provides foundational HCI principles (specifically Guideline G2: *Make clear how well the system can do what it can do*, G8: *Support efficient dismissal*, and G9: *Support efficient correction*).
- Supports giving human reviewers explicit control over AI-generated document summaries.
- Emphasises communicating AI limitations and uncertainty clearly.
- Highlights the importance of granular user correction and rejection mechanisms.
- Establishes evidence-based design rules for the verification and sign-off workflow in this project.

### 2.2 Fostering Appropriate Reliance on Large Language Models: The Role of Explanations, Sources, and Inconsistencies

**Authors:** Kim *et al.* (2025)  
**DOI:** [10.1145/3706598.3714020](https://doi.org/10.1145/3706598.3714020)

**Brief description:**  
Investigates how explanations, source links and highlighted inconsistencies influence users' reliance on LLM-generated answers. A controlled experiment involving $N = 308$ participants found that while standalone AI explanations often increase over-reliance on incorrect answers, providing primary sources and surfacing inconsistencies significantly reduces inappropriate reliance on erroneous AI outputs.

**Relevance to the project:**
- Provides direct empirical evidence supporting source citations and contradiction highlighting in AI summaries.
- Demonstrates how primary sources reduce over-trust (automation bias) on incorrect AI claims.
- Shows that fluent AI explanations alone can mislead users into accepting false statements.
- Directly informs the experimental comparison in this project between plain AI summaries (Condition A) and verification-enhanced interfaces showing sources and inconsistencies (Conditions B and C).

### 2.3 In Search of Verifiability: Explanations Rarely Enable Complementary Performance in AI-Advised Decision Making

**Authors:** Fok and Weld (2024)  
**DOI:** [10.1002/aaai.12182](https://doi.org/10.1002/aaai.12182)

**Brief description:**  
Examines why human-AI teams frequently fail to achieve complementary performance (performing better together than either the human or AI alone). The authors demonstrate that standard AI explanations merely illustrate *how* the model reached a conclusion, whereas users require *verifiability*—the ability to rapidly test whether an AI claim is actually true against ground-truth evidence.

**Relevance to the project:**
- Establishes the critical theoretical distinction between *explainability* and *verifiability*.
- Explains why checking long documents is slow and prone to human oversight unless the interface lowers the cost of verification.
- Justifies linking individual AI-generated claims directly to highlighted passages in the original client documents.
- Provides the theoretical foundation for the project's central research question on helping users find AI mistakes more effectively.

### 2.4 "I'm Not Sure, But...": Examining the Impact of Large Language Models' Uncertainty Expression on User Reliance and Trust

**Authors:** Kim *et al.* (2024)  
**DOI:** [10.1145/3630106.3658941](https://doi.org/10.1145/3630106.3658941)

**Brief description:**  
Investigates how expressions of uncertainty influence user trust and reliance on LLMs. A controlled experiment with $N = 404$ participants found that explicit natural-language uncertainty expressions reduced blind confidence in erroneous AI answers, fostered calibrated reliance and improved overall decision accuracy compared to confident default phrasing.

**Relevance to the project:**
- Supports communicating uncertainty explicitly alongside AI-generated summary claims.
- Demonstrates that understandable uncertainty phrasing calibrates user trust and mitigates over-reliance.
- Justifies flagging low-confidence or unverified claims so reviewers know which statements most need checking.
- Informs the design of confidence and uncertainty notes in Conditions B and C of this project.

### 2.5 Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance

**Authors:** Bansal *et al.* (2021)  
**DOI:** [10.1145/3411764.3445717](https://doi.org/10.1145/3411764.3445717)

**Brief description:**  
Evaluates human-AI decision-making across text and question-answering tasks ($N = 528$). The findings reveal that fluent AI justifications increase human agreement with the AI regardless of whether the AI is right or wrong, amplifying automation bias when the AI errs.

**Relevance to the project:**
- Explains the core problem addressed in this project: people tend to trust fluent AI answers too much.
- Demonstrates the need to evaluate both missed errors (over-trust) and falsely rejected correct claims (under-trust).
- Reinforces designing an active verification workflow rather than relying on passive AI justifications.

### 2.6 Decision Control and Explanations in Human-AI Collaboration: Improving User Perceptions and Compliance

**Authors:** Westphal *et al.* (2023)  
**DOI:** [10.1016/j.chb.2023.107714](https://doi.org/10.1016/j.chb.2023.107714)

**Brief description:**  
Examines how granting users decision control versus providing complex explanations affects human-AI collaboration. The study shows that explicit decision control improves user compliance, perceived autonomy and accountability, whereas overly complex explanations significantly increase perceived cognitive task load.

**Relevance to the project:**
- Supports retaining explicit human control over final document approval and sign-off.
- Justifies allowing users to accept, reject or edit individual AI claims before finalising a summary.
- Warns against overwhelming reviewers with dense explanations that increase cognitive workload.
- Informs the design of a streamlined, low-friction human-in-the-loop sign-off workflow.

### 2.7 Evaluating the Impact of Human Explanation Strategies on Human-AI Visual Decision-Making

**Authors:** Morrison *et al.* (2023)  
**DOI:** [10.1145/3579481](https://doi.org/10.1145/3579481)

**Brief description:**  
Investigates how different strategies for presenting evidence and explanations impact human accuracy and reliance during AI-assisted tasks. The study shows that structuring evidence clearly helps users detect AI errors, whereas poorly structured explanations can mislead reviewers.

**Relevance to the project:**
- Supports separating the AI's generated claim from the raw original evidence in the interface layout.
- Justifies a side-by-side verification layout where source documents and extracted claims can be compared directly.
- Reinforces testing multiple interface conditions in a within-subject evaluation.

### 2.8 An Intelligent Enterprise System with Processing and Verification of Business Documents Using Big Data and AI

**Authors:** Balakayeva *et al.* (2025)  
**DOI:** [10.1515/jisys-2024-0446](https://doi.org/10.1515/jisys-2024-0446)

**Brief description:**  
Proposes an enterprise document-processing workflow combining LLMs with rule-based validation and business-process management. Crucially, the system incorporates confidence-based escalation to human reviewers and maintains structured audit logs for compliance in regulated business environments.

**Relevance to the project:**
- Demonstrates how AI document summarisation integrates into regulated workflows (e.g., finance, legal and administration).
- Introduces confidence-based routing that directs human attention to uncertain or conflicting document fields.
- Supports maintaining a traceable audit log of what the AI generated and what the human reviewer approved or corrected.

## 3. Relevant HCI Design and Accessibility Standards

To ensure the prototype in this project follows established interface design rules, accessibility conventions and standard usability benchmarks, three core HCI standards are applied:

### 3.1 Nielsen's 10 Usability Heuristics for User Interface Design

**Authors:** Nielsen (1994)  
**DOI:** [10.1145/191666.191729](https://doi.org/10.1145/191666.191729)

**Brief description:**  
Introduces and validates fundamental usability heuristics for evaluating and designing interactive user interfaces, focusing on system status visibility, user control, error prevention and reducing memory load.

**Relevance to the project:**
- **Visibility of system status:** Justifies showing clear verification badges (Supported, Discrepancy, Uncertain) and a live progress counter of how many claims have been checked.
- **User control and freedom:** Supports providing fast inline *Approve*, *Edit*, *Reject* and *Undo* actions so users remain in control of the summary.
- **Error prevention:** Justifies requiring an explicit human sign-off step and warning users before they approve a summary containing uninspected discrepancies.
- **Recognition rather than recall:** Supports displaying source document passages side by side with AI claims so users do not have to remember figures from another page.

### 3.2 Web Content Accessibility Guidelines (WCAG 2.1)

**Authors:** World Wide Web Consortium (W3C) (2018)  
**Standard URL:** [https://www.w3.org/TR/WCAG21/](https://www.w3.org/TR/WCAG21/) *(Last Accessed: 7 November 2026)*

**Brief description:**  
Establishes the official W3C technical standard for web accessibility, defining testable success criteria to make interactive web content perceivable, operable, understandable and robust for all users.

**Relevance to the project:**
- **Use of Colour (Criterion 1.4.1):** Ensures that claim statuses (Supported, Discrepancy, Uncertain) never rely on colour alone (such as green, red or amber), but always include distinct icons and text labels.
- **Contrast Minimum (Criterion 1.4.3):** Establishes a testable contrast target of at least $4.5:1$ for text and highlighted document passages so users can read client files comfortably.
- **Keyboard Accessible (Criterion 2.1.1):** Ensures all core checking and sign-off controls can be operated easily on a standard laptop using a mouse or keyboard.

### 3.3 Standardised HCI Evaluation Benchmarks (SUS and NASA-TLX)

**Authors:** Brooke (1996); Hart and Staveland (1988)  
**DOI (SUS):** [10.1201/9781498710411-35](https://doi.org/10.1201/9781498710411-35)  
**DOI (NASA-TLX):** [10.1016/S0166-4115(08)62386-9](https://doi.org/10.1016/S0166-4115(08)62386-9)

**Brief description:**  
Introduces two foundational HCI evaluation questionnaires: the System Usability Scale (SUS) for measuring perceived interface usability across a 10-item scale, and the NASA Task Load Index (NASA-TLX) for measuring subjective cognitive workload across mental demand, effort and frustration.

**Relevance to the project:**
- **System Usability Scale (SUS):** Provides a standard 10-item questionnaire scored from $0$ to $100$, establishing a clear quantitative benchmark ($68$ represents average usability) to test whether our final interface design is easy to use.
- **NASA Task Load Index (NASA-TLX):** Provides a validated scale for measuring mental demand, effort and frustration, allowing this project to verify that adding source links and sign-off steps does not overwhelm the user.

## 4. Research Synthesis and Identified Gap

The reviewed papers and HCI standards reveal five major themes that shape this project:

| Theme | Relevant sources | Key insight |
|---|---|---|
| Human-AI interaction and control | Amershi *et al.* (2019); Westphal *et al.* (2023); Nielsen (1994) | Users need explicit control, low-friction correction tools and clear sign-off steps without excessive cognitive load. |
| Calibrated trust and uncertainty | Kim *et al.* (2025); Kim *et al.* (2024); Bansal *et al.* (2021) | Fluent AI text induces over-trust; showing primary sources, inconsistencies and verbal uncertainty reduces reliance on wrong answers. |
| Verifiability over explainability | Fok & Weld (2024); Morrison *et al.* (2023) | Explanations alone do not help users catch errors; interfaces must minimise the effort required to check claims against raw source text. |
| Accountability and audit trails | Balakayeva *et al.* (2025); Nielsen (1994) | Delegated document workflows require flagging uncertain claims, explicit human approval and a readable audit log of decisions. |
| Accessible design and usability | WCAG 2.1; Brooke (1996); Hart & Staveland (1988) | Verification interfaces must use accessible visual cues (icons, text and colour) and achieve high usability (SUS $\ge 68$) with manageable workload. |

## 5. Key Research Implications

The literature and standards highlight six core implications for this project:

- **Verifiability:** AI-generated claims must be linked directly to exact passages in the source document that users can inspect side by side.
- **Appropriate reliance:** The interface must help users catch planted errors (preventing over-trust) without causing them to reject accurate statements (preventing under-trust).
- **Uncertainty and discrepancy communication:** Uncertain claims and year-over-year discrepancies must be flagged using clear language and accessible visual badges.
- **Human control and sign-off:** The agent must never finalise or send an important summary without explicit human review and sign-off.
- **Accountability and audit trail:** Every AI output, human source inspection, claim edit/rejection and final sign-off must be logged in a clear audit record.
- **Manageable workload:** Verification tools should streamline checking rather than overwhelming users with verbose AI explanations.

## 6. Declaration of AI Usage

AI tools were used as supporting tools throughout the preparation of this literature review for the following purposes:

- Ensuring generated text is easy to follow, understand and clear and communicates the ideas researched.
- Understanding project requirements and identifying relevant academic research and HCI standards.
- Suggesting keywords and search terms for literature searches.
- Obtaining general overviews and understanding the key findings of research papers.
- Identifying information most relevant to the project's objectives and requirements.
- Clarifying academic concepts and terminology that were difficult to understand.
- Filtering out off-topic papers to keep the literature review focused strictly on human-AI interaction and summary verification.
- Synthesising common research themes across the academic papers and HCI standards into a structured comparison table.
- Organising research findings and formatting the `literature_review.md` file to ensure a clear structure, logical flow and consistent presentation.
