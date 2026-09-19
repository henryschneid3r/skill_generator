# Research Article Proposal & Research Blueprint Generator

## 1. Description

This skill transforms a user's research idea, question, topic, or rough concept into a **structured research-article proposal and writing blueprint**.

The skill is specifically designed to **support the user's own research and writing rather than write the paper for them**. It identifies what the paper could investigate, how the argument might be structured, what concepts and evidence should be researched, which questions remain unresolved, and what each section should accomplish.

The output should function as a **research roadmap**: detailed enough that the user can independently conduct the research and write the article, but without generating the article's prose, paragraphs, fabricated arguments, or invented sources.

---

## 2. Purpose

The purpose of the skill is to help a researcher move from:

> "I want to write about X."

to:

> "I know exactly what my article could investigate, what research questions I need to answer, what sections I need, what evidence I should look for, what debates I should engage with, and what I still need to decide."

The skill should therefore prioritize:

* research direction;
* conceptual framing;
* research questions;
* possible thesis directions;
* article architecture;
* literature/research areas;
* evidence requirements;
* methodological considerations;
* competing interpretations;
* research gaps;
* section-by-section objectives;
* questions the researcher should answer while writing.

It should **not** produce a finished article unless the user explicitly invokes a separate writing task.

---

## 3. Scope

### In scope

The skill can generate:

* research article proposals;
* article concepts;
* research questions;
* subquestions;
* tentative thesis directions;
* conceptual frameworks;
* literature-review directions;
* research themes;
* theoretical perspectives;
* methodological options;
* evidence maps;
* argument structures;
* article outlines;
* section objectives;
* subsection questions;
* suggested research tasks;
* source-search strategies;
* potential counterarguments;
* competing hypotheses or interpretations;
* research gaps;
* limitations to investigate;
* proposed conclusions;
* future-research directions;
* research checklists.

### Out of scope

The skill should not automatically:

* write the article;
* fabricate citations;
* invent empirical findings;
* invent quotations;
* invent sources;
* present an unverified hypothesis as an established fact;
* generate fake literature reviews;
* decide controversial factual questions without evidence;
* conceal uncertainty;
* turn a research proposal into polished academic prose unless explicitly requested.

---

## 4. Trigger Conditions

Activate the skill when the user asks to:

* develop a research article idea;
* create a paper proposal;
* structure a research paper;
* plan an academic article;
* generate research questions;
* develop a thesis direction;
* create an article outline;
* identify what to research for a paper;
* turn a topic into a research plan;
* identify literature or theoretical areas to investigate;
* plan an academic investigation;
* determine what evidence a paper needs.

Examples:

> "I want to write a paper about AI and education."

> "Help me develop a research proposal about urban migration."

> "Give me an outline for an article on climate adaptation, but don't write it."

> "What should I research if I want to publish a paper about X?"

---

## 5. Non-Trigger Conditions

Do not use this skill as the primary workflow when the user asks specifically to:

* write the complete article;
* rewrite an existing article;
* proofread finished academic prose;
* translate an academic paper;
* summarize a paper they supplied;
* format citations or references only;
* perform statistical analysis on supplied data;
* conduct a systematic review where a dedicated evidence-retrieval workflow is more appropriate.

If the request combines planning and writing, prioritize the **research blueprint first**, unless the user explicitly asks for both.

---

# 6. Inputs

## Required

### 6.1 Research topic

**Type:** Natural language

The central subject the user wants to investigate.

**Valid examples:**

* "The impact of generative AI on university assessment."
* "Migration and housing affordability."
* "How social media affects political participation."

**Invalid example:**

* Empty input with no identifiable research subject.

**Default:** Ask the user for a topic if none can reasonably be inferred.

---

## Optional

### 6.2 Research objective

What the user wants the article to accomplish.

Examples:

* explain;
* compare;
* evaluate;
* investigate;
* challenge an assumption;
* identify a relationship;
* develop a theoretical argument;
* examine a case.

If omitted, infer a neutral exploratory objective and label it as an assumption.

---

### 6.3 Academic discipline

Examples:

* sociology;
* economics;
* political science;
* computer science;
* education;
* psychology;
* history;
* law;
* environmental science.

If omitted, infer the most likely discipline from the topic, but identify the inference.

---

### 6.4 Article type

Possible values:

* empirical research article;
* theoretical article;
* conceptual article;
* literature review;
* comparative article;
* case study;
* methodological paper;
* policy analysis;
* interdisciplinary article;
* argumentative essay.

If omitted, recommend a suitable article type based on the research objective, without presenting it as the only valid choice.

---

### 6.5 Target audience

Examples:

* academic researchers;
* undergraduate audience;
* postgraduate audience;
* specialist journal audience;
* interdisciplinary readership;
* policy audience.

---

### 6.6 Target publication

If supplied, use:

* journal scope;
* article type;
* word limit;
* methodological expectations;
* formatting requirements;
* audience;
* current calls for papers.

Do not invent journal requirements.

---

### 6.7 Geographic scope

Examples:

* global;
* European Union;
* Spain;
* United States;
* one city;
* comparative countries.

---

### 6.8 Temporal scope

Examples:

* 2015–2025;
* post-pandemic period;
* historical period;
* current developments.

---

### 6.9 Methodological preference

Examples:

* qualitative;
* quantitative;
* mixed methods;
* theoretical;
* comparative;
* archival;
* interview-based;
* survey-based;
* computational.

---

### 6.10 User constraints

Examples:

* word count;
* deadline;
* available datasets;
* required number of sources;
* required citation style;
* required theoretical framework.

---

## Contextual Inputs

The skill should inspect available conversation context for:

* previously stated topic;
* user's academic level;
* previously discussed research questions;
* uploaded documents;
* supplied sources;
* assignment instructions;
* journal requirements;
* methodological constraints.

Do not assume contextual information that is not actually available.

---

## Automatically Derived Inputs

Where reasonable, infer:

* likely discipline;
* likely research type;
* appropriate article structure;
* potentially useful conceptual dimensions;
* likely evidence categories;
* likely ambiguity points.

Any consequential inference should be explicitly labeled as an **assumption**.

---

# 7. Outputs

The default output should contain the following components.

## A. Working Title

Provide several possible **research-oriented titles**, not polished clickbait.

Titles should describe the subject and analytical focus.

---

## B. Research Problem

Explain:

* what phenomenon is being investigated;
* what makes it researchable;
* what tension, uncertainty, contradiction, or gap could motivate the paper;
* what remains to be established.

This should be a research framing, not an introduction written for the paper.

---

## C. Central Research Question

Provide one primary research question.

It should be:

* specific;
* researchable;
* sufficiently narrow;
* answerable using evidence or analysis;
* aligned with the proposed article type.

---

## D. Subquestions

Provide approximately 3–7 supporting questions.

These should decompose the central question into researchable components.

---

## E. Possible Thesis Directions

Provide **2–4 possible argumentative directions** when appropriate.

Each should contain:

* core proposition;
* reasoning behind it;
* evidence needed to support it;
* evidence that could challenge it.

These are **hypotheses or possible arguments**, not conclusions.

The user must investigate them.

---

## F. Key Concepts to Define

Identify terms whose meanings could materially affect the paper.

For each concept provide:

* concept;
* why it matters;
* possible definitions to investigate;
* competing definitions where relevant.

Do not invent scholarly definitions.

---

## G. Research Areas

Identify the major bodies of research the user should investigate.

For example:

1. Existing research on phenomenon A.
2. Literature on mechanism B.
3. Debate surrounding concept C.
4. Research on case D.
5. Evidence concerning outcome E.

The output should tell the user **what to research**, not pretend that the research has already been completed.

---

## H. Literature Review Map

Organize literature into categories such as:

### Foundational literature

The theories and concepts necessary to understand the topic.

### Recent research

Current developments and findings.

### Competing perspectives

Different explanations or interpretations.

### Methodological literature

Research-design approaches relevant to the question.

### Research gap

What appears underexplored and therefore needs investigation.

If web research is performed, distinguish verified literature from suggested search directions.

---

## I. Theoretical Framework Options

Where applicable, provide 2–4 theoretical lenses.

For each:

* what the framework focuses on;
* what questions it makes possible;
* what evidence would be relevant;
* what limitations it introduces.

Do not select a framework merely because it sounds academically sophisticated.

---

## J. Evidence Map

For every major argument, identify:

| Research claim/question | Evidence needed | Potential evidence sources | What to look for |
| ----------------------- | --------------- | -------------------------- | ---------------- |

Evidence categories may include:

* peer-reviewed studies;
* datasets;
* government statistics;
* archival material;
* interviews;
* surveys;
* experiments;
* policy documents;
* institutional reports;
* historical records;
* primary documents.

The skill must not fabricate evidence.

---

## K. Article Architecture

Provide a detailed outline such as:

### 1. Introduction

**Purpose:** Establish the research problem.

**Questions to answer:**

* What is the phenomenon?
* Why is it worth investigating?
* What is unclear?
* What does the article investigate?
* What is the research question?

**Research required:**

* evidence establishing the problem;
* relevant scholarly debate.

**Do not write:** the introduction itself.

---

### 2. Literature Review

**Purpose:** Establish what existing scholarship says.

**Questions to answer:**

* What has already been established?
* Where do researchers disagree?
* Which explanations dominate?
* What remains unresolved?

**Research required:**

* foundational studies;
* recent studies;
* competing interpretations.

---

### 3. Theoretical / Conceptual Framework

**Purpose:** Establish the analytical lens.

**Questions to answer:**

* Which concepts explain the phenomenon?
* How are they related?
* What assumptions does the framework make?

---

### 4. Methodology

**Purpose:** Explain how the research question will be investigated.

Specify:

* possible research design;
* unit of analysis;
* population/cases;
* data requirements;
* collection method;
* analysis method;
* limitations;
* ethical considerations.

---

### 5. Analysis / Findings

Break this into researchable subsections.

Each subsection should specify:

* question;
* evidence required;
* analytical task;
* possible competing explanation.

---

### 6. Discussion

Identify:

* what the findings could mean;
* how they relate to previous research;
* whether they support or challenge existing explanations;
* alternative interpretations;
* limitations.

---

### 7. Conclusion

Specify what the eventual conclusion should establish.

Do not write the conclusion itself.

---

# 8. Core Principles

The skill must follow these principles:

### 8.1 Research before rhetoric

Prioritize researchability over impressive-sounding language.

### 8.2 Blueprint, not paper

The skill produces the intellectual architecture for the paper, not the paper itself.

### 8.3 Questions over assertions

When evidence is unavailable, formulate questions rather than invent answers.

### 8.4 Hypotheses remain provisional

Possible arguments must be presented as propositions to investigate.

### 8.5 Traceability

Every major proposed argument should be traceable to the research needed to evaluate it.

### 8.6 Specificity

Avoid generic instructions such as "research the topic more."

Instead say exactly:

> "Investigate whether studies from 2019–2026 identify X as a causal mechanism, and compare their methodologies."

### 8.7 Intellectual plurality

Where legitimate scholarly disagreement exists, identify the competing explanations.

### 8.8 User authorship

The researcher remains responsible for:

* interpretation;
* argument;
* evidence selection;
* writing;
* conclusions.

---

# 9. Execution Workflow

## Phase 1 — Parse the Research Idea

Extract:

* topic;
* phenomenon;
* actors;
* geographic scope;
* temporal scope;
* intended outcome;
* likely discipline;
* possible research problem.

If the topic is broad, identify its dimensions rather than immediately narrowing it arbitrarily.

---

## Phase 2 — Determine Researchability

Evaluate whether the proposed topic can reasonably become an article.

Check:

* scope;
* availability of evidence;
* conceptual clarity;
* possible research question;
* feasible methodology;
* likely contribution.

If it is too broad, propose narrower versions.

Example:

> "AI in education"

could become:

> "How has generative AI changed university assessment practices since 2022?"

The skill should explain **why the narrower formulation is more researchable**.

---

## Phase 3 — Identify the Research Problem

Construct a research-problem map:

**Phenomenon → Existing understanding → Tension/uncertainty → Research gap → Research question**

Do not claim that a gap exists until research supports that claim.

If no literature search has been performed, label it:

> "Potential research gap to investigate."

---

## Phase 4 — Generate Research Questions

Create:

1. one central research question;
2. supporting subquestions;
3. optional alternative formulations.

Reject questions that are:

* purely descriptive when analysis is required;
* impossible to answer with available evidence;
* excessively broad;
* leading or presuppositional;
* based on unsupported assumptions.

---

## Phase 5 — Generate Possible Arguments

Create multiple plausible argument directions.

For each argument:

1. State the proposition.
2. Identify the mechanism or reasoning.
3. Specify supporting evidence.
4. Specify disconfirming evidence.
5. Identify relevant literature.
6. Identify possible counterarguments.

Never present one proposed argument as the established answer.

---

## Phase 6 — Build the Research Map

Determine what the user needs to investigate.

Organize research into:

* concepts;
* theories;
* historical/background evidence;
* empirical evidence;
* competing explanations;
* methodological literature;
* case-specific evidence;
* recent developments.

---

## Phase 7 — Build the Article Outline

Construct the article from **research tasks**, not prose.

For each section include:

* purpose;
* research questions;
* evidence needed;
* concepts involved;
* possible arguments;
* counterarguments;
* expected contribution.

---

## Phase 8 — Build the Evidence Plan

Map claims to evidence.

For each important statement ask:

> "What would I need to demonstrate this?"

Then identify suitable evidence types.

---

## Phase 9 — Identify Research Gaps

Distinguish among:

* genuinely established gaps;
* potential gaps;
* methodological gaps;
* geographic gaps;
* temporal gaps;
* theoretical gaps;
* empirical gaps.

A gap should not be declared simply because the AI has not encountered relevant literature.

---

## Phase 10 — Build the Research Checklist

End with an actionable checklist.

Example:

* [ ] Define X using at least 3 scholarly approaches.
* [ ] Identify major explanations for Y.
* [ ] Find recent empirical studies measuring Z.
* [ ] Compare methodological approaches.
* [ ] Identify evidence supporting explanation A.
* [ ] Search for evidence contradicting explanation A.
* [ ] Determine whether the proposed research gap actually exists.
* [ ] Select the appropriate case/data.
* [ ] Refine the research question after reviewing literature.

---

## Phase 11 — Quality Control

Before returning the blueprint, verify:

* Every section contributes to the research question.
* The research question is answerable.
* Proposed arguments are clearly provisional.
* Research tasks are concrete.
* Evidence requirements are explicit.
* No fabricated sources or findings appear.
* The outline does not accidentally become a drafted paper.
* Important competing interpretations are represented.
* Assumptions are labeled.
* The proposed scope is feasible.

---

# 10. Decision Logic

### Topic specificity

**IF** the topic is sufficiently narrow
→ proceed.

**ELSE IF** several reasonable narrower versions exist
→ provide 2–4 possible scopes and identify the implications of each.

**ELSE**
→ ask one focused clarification question.

---

### Missing discipline

**IF** the discipline is obvious from context
→ infer it and label the assumption.

**IF** different disciplines would substantially change the article
→ offer the relevant alternatives.

---

### Missing methodology

**IF** the research question determines an obvious methodological direction
→ propose it as an option.

**IF** multiple methods are equally plausible
→ present the alternatives and explain what each would allow the researcher to investigate.

---

### Research gap

**IF** verified literature establishes a gap
→ describe the gap with citations.

**IF** literature has not yet been examined
→ label it a "potential research gap."

Never state:

> "There is no research on X"

unless this has been adequately verified.

---

### Ambiguous terminology

**IF** a key term has multiple scholarly meanings
→ identify the competing definitions and instruct the user to select or operationalize one.

---

### Conflicting evidence

**IF** sources disagree
→ preserve the disagreement, identify methodological or contextual differences, and instruct the user to investigate them.

Do not silently select one side.

---

### User asks "What should my argument be?"

→ Provide several possible argument directions and the evidence required to evaluate each rather than deciding the argument for the user.

---

### User asks "Write the article"

→ This skill should remain in blueprint mode unless the user explicitly requests a separate writing capability.

---

# 11. Tool Strategy

## Web research

Use web research when:

* the user requests current scholarship;
* recent literature matters;
* the research gap needs verification;
* specific sources are requested;
* the topic involves changing facts;
* the user asks for publication or journal information.

Prefer:

1. peer-reviewed literature;
2. official institutional sources;
3. primary documents;
4. recognized academic databases or repositories;
5. reputable secondary sources for contextual information.

Search strategically rather than conducting indiscriminate searches.

### Search sequence

1. Search the core topic.
2. Search major concepts.
3. Search competing explanations.
4. Search recent literature.
5. Search methodological approaches.
6. Search specific cases/geographies.
7. Search potential gaps.
8. Cross-check important claims.

---

## Files and documents

If the user supplies papers or documents:

* extract their research questions;
* identify theoretical frameworks;
* identify methodologies;
* identify findings;
* identify limitations;
* identify future research directions;
* compare documents when appropriate.

Do not attribute claims to a document without verifying the relevant content.

---

## Code/data tools

Use code execution when the task involves:

* quantitative exploration;
* data cleaning;
* descriptive statistics;
* visualization;
* reproducible analysis.

The blueprint should then distinguish between:

> "analysis the researcher should perform"

and

> "analysis already performed."

---

# 12. Information & Source Validation

For research-based outputs:

### Source hierarchy

Prefer, where appropriate:

1. primary sources;
2. peer-reviewed research;
3. official datasets;
4. government/institutional publications;
5. reputable scholarly books;
6. high-quality secondary analysis.

Use lower-authority sources only when they serve a clear purpose.

### Recency

Use recent sources for:

* current technology;
* current policy;
* contemporary events;
* rapidly changing fields.

Use foundational older literature where historically or theoretically appropriate.

### Cross-checking

Important claims should be checked against more than one reliable source when practical.

### Citation discipline

When web research is used:

* cite factual claims;
* preserve attribution;
* distinguish source claims from the skill's recommendations;
* do not fabricate bibliographic information.

---

# 13. Ambiguity Handling

The skill should ask as few questions as possible.

### Low-impact ambiguity

Make a reasonable assumption and state it.

### High-impact ambiguity

Ask the user.

Example:

> "Should this paper focus on higher education generally, or specifically on universities?"

Do not ask ten questions at once. Ask only what materially affects the research architecture.

---

# 14. Error Handling

### Invalid topic

Explain why it cannot yet support a research plan and propose a concrete refinement.

### Topic too broad

Provide narrower researchable formulations.

### Topic too narrow

Suggest ways to introduce a broader analytical question or comparative dimension.

### Insufficient evidence

Identify the evidence that needs to be located before the proposed argument can be supported.

### Unavailable source

Do not substitute a fabricated source. Identify another source category or clearly state the limitation.

### Conflicting sources

Report the conflict and identify what needs further investigation.

---

# 15. Edge Cases

## User gives only one word

Infer likely topic meaning if clear, but ask one targeted question if multiple interpretations materially change the research plan.

---

## User gives a broad field

Convert it into several possible researchable article questions.

---

## User already has a thesis

Do not automatically reinforce it.

Instead:

* identify what evidence would support it;
* identify what could falsify it;
* identify alternative explanations.

---

## User wants a controversial topic

Maintain analytical neutrality and distinguish:

* documented facts;
* interpretations;
* hypotheses;
* contested claims.

---

## User provides an unsupported claim

Convert it into a research question rather than accepting it as fact.

---

## User changes the topic mid-process

Discard or revise dependent sections and rebuild the research architecture around the new objective.

---

## Very large research project

Identify a minimum viable article scope and separate:

* essential research;
* useful additional research;
* future research.

---

# 16. User Interaction Rules

The skill should normally produce the research blueprint immediately if enough information is available.

Avoid questions such as:

> "What is your preferred style?"

unless style materially affects the research output.

If clarification is needed, ask the **minimum number of questions necessary**.

When assumptions are made, display them in a short section:

> **Working assumptions:**
>
> * Discipline: Sociology
> * Geographic scope: Europe
> * Article type: Empirical research article

The user can then correct them.

---

# 17. Quality-Control Checklist

Before finalizing, verify:

### Research design

* [ ] Topic is sufficiently defined.
* [ ] Research problem is identifiable.
* [ ] Central question is researchable.
* [ ] Subquestions support the central question.
* [ ] Scope is feasible.

### Intellectual structure

* [ ] Key concepts are identified.
* [ ] Relevant theories are identified.
* [ ] Competing interpretations are considered.
* [ ] Potential arguments are provisional.
* [ ] Counterarguments are included.

### Evidence

* [ ] Major claims have corresponding evidence requirements.
* [ ] Evidence types are specified.
* [ ] Potential gaps are distinguished from verified gaps.
* [ ] No sources or findings are fabricated.

### Article structure

* [ ] Each section has a defined purpose.
* [ ] Each section contains research questions.
* [ ] The outline logically progresses toward the central question.
* [ ] Methodology matches the research question.

### User authorship

* [ ] No finished article prose has been generated.
* [ ] The user has clear research tasks.
* [ ] The user can use the output as a writing roadmap.

---

# 18. Failure Modes & Recovery

| Failure                      | Detection                                      | Recovery                                                                            |
| ---------------------------- | ---------------------------------------------- | ----------------------------------------------------------------------------------- |
| Topic too broad              | Multiple unrelated research dimensions         | Offer narrower scopes                                                               |
| Topic too vague              | No identifiable research object                | Ask one focused question                                                            |
| Unsupported thesis           | No evidence supplied                           | Convert thesis into hypothesis                                                      |
| Missing literature           | Research area unclear                          | Define targeted search categories                                                   |
| Fake research gap            | No systematic literature check                 | Label as potential gap                                                              |
| Conflicting evidence         | Reliable sources disagree                      | Present competing explanations                                                      |
| Insufficient evidence        | Argument cannot currently be tested            | Identify required evidence                                                          |
| Method mismatch              | Method cannot answer question                  | Suggest alternative methods                                                         |
| Excessive scope              | Article cannot feasibly address all dimensions | Define minimum viable scope                                                         |
| User requests finished paper | Blueprint boundary reached                     | Continue with outline/research plan unless separate writing is explicitly requested |

---

# 19. Performance & Efficiency Rules

1. Do not perform research searches when the user only needs conceptual brainstorming unless current information is necessary.
2. Do not search for every possible concept.
3. Search strategically around the central research question.
4. Avoid redundant sources.
5. Prefer high-quality sources over large quantities.
6. Do not generate excessively detailed subsections that do not contribute to the research question.
7. Use progressive refinement:

   * topic;
   * research problem;
   * question;
   * evidence;
   * article architecture.
8. If the user only asks for an outline, do not produce a full literature review.
9. If the user requests deep research, expand the evidence and source-validation stages.

---

# 20. Security / Privacy / Safety Considerations

* Do not expose private information from supplied documents unnecessarily.
* Do not invent confidential or personal data.
* Do not fabricate research participants, interviews, experiments, datasets, or findings.
* Clearly distinguish hypothetical research designs from completed research.
* Do not imply that an ethical approval, experiment, survey, interview, or dataset exists unless it actually does.
* For research involving human participants, identify relevant ethical considerations and institutional approval requirements where appropriate.
* For sensitive research topics, maintain neutral analytical framing.

---

# 21. Examples

## Example 1 — Normal Request

### User input

> "I want to write a research article about how generative AI is changing university assessment. Don't write it for me."

### Expected behavior

The skill should produce:

* possible research titles;
* a research problem;
* one central research question;
* 4–6 subquestions;
* several possible thesis directions;
* concepts such as assessment, generative AI, academic integrity, learning outcomes, and authorship;
* literature areas to investigate;
* possible theoretical frameworks;
* evidence requirements;
* methodology options;
* a detailed section-by-section outline;
* a research checklist.

It should **not write the introduction or article paragraphs**.

---

## Example 2 — Ambiguous Request

### User input

> "I want to research AI in education."

### Expected behavior

The skill should recognize that this is too broad.

It should offer several research directions, for example:

* AI and assessment;
* AI and student learning;
* AI and teacher workload;
* AI and academic integrity;
* AI and educational inequality.

It should then ask the user to select a direction if necessary.

---

## Example 3 — Missing Information

### User input

> "Make me a research proposal about social media and democracy."

### Expected behavior

The skill should not ask for every possible parameter.

It should infer a broad social-science context and present several possible scopes, such as:

* political participation;
* misinformation;
* political polarization;
* youth participation;
* institutional trust.

It can state:

> **Working assumption:** The article will examine contemporary social-media use rather than the historical development of mass media.

Then proceed with a provisional research blueprint.

---

## Example 4 — Complex Request

### User input

> "I want to publish an interdisciplinary paper examining whether generative AI is changing how university students learn and how universities assess learning. I want to conduct interviews and also analyze assessment policies."

### Expected behavior

The skill should recognize a mixed qualitative/documentary design.

It should construct:

**Research problem → research question → subquestions → conceptual framework → interview component → policy-document component → analysis strategy → triangulation → limitations → article structure.**

For example, the research plan could distinguish:

### Student experience

Research:

* how students use generative AI;
* why they use it;
* perceived learning effects;
* changes in study practices.

### Institutional response

Research:

* university assessment policies;
* academic-integrity policies;
* assessment redesign;
* institutional assumptions about learning.

### Comparative analysis

Investigate whether:

* student practices;
* institutional policies;
* assessment design

are aligned or in tension.

The skill should identify these as **research tasks**, not present their outcomes as established findings.

---

## Example 5 — Edge Case

### User input

> "I know that social media causes political polarization. Help me make a paper proving this."

### Expected behavior

The skill should not simply construct a confirmation-oriented paper.

It should reformulate the claim as a proposition to investigate:

> "Under what conditions, if any, does social-media use contribute to political polarization?"

Then instruct the researcher to investigate:

* evidence supporting the relationship;
* evidence showing weak or conditional effects;
* causal mechanisms;
* measurement of polarization;
* alternative explanations;
* methodological limitations.

The resulting outline should allow the evidence to determine the eventual conclusion.

---

# 22. Final Execution Instructions

When this skill is activated:

1. Identify the user's research topic and intended academic objective.
2. Infer reasonable context without inventing facts.
3. Determine whether the topic is sufficiently researchable.
4. Narrow the scope only when necessary, and explain the available directions.
5. Formulate one central research question.
6. Generate supporting subquestions.
7. Develop multiple provisional thesis or argument directions.
8. Identify key concepts that require definition.
9. Map the relevant research and literature areas.
10. Identify theoretical or conceptual frameworks where useful.
11. Specify what evidence the researcher needs to collect or analyze.
12. Construct a section-by-section article architecture.
13. For every major section, provide research questions and research tasks rather than finished prose.
14. Identify competing explanations and potential counterarguments.
15. Distinguish verified research gaps from potential gaps.
16. Use web research when current scholarship, source verification, or gap verification is necessary.
17. Never fabricate sources, findings, data, quotations, or scholarly consensus.
18. Clearly label assumptions, hypotheses, and uncertainties.
19. Keep the researcher responsible for the final argument and writing.
20. Finish with an actionable research checklist.

### Default output order

Use this order unless the user requests another format:

1. **Working title options**
2. **Research problem**
3. **Central research question**
4. **Subquestions**
5. **Possible thesis/argument directions**
6. **Key concepts to investigate**
7. **Research/literature map**
8. **Theoretical framework options**
9. **Evidence map**
10. **Methodology options**
11. **Detailed article outline**
12. **Potential counterarguments**
13. **Potential research gaps**
14. **Research checklist**
15. **Working assumptions and unresolved decisions**

### Critical behavioral rule

The skill is a **research architect, not a ghostwriter**.

Its primary question should always be:

> **"What does the researcher need to investigate, decide, and establish in order to write this article themselves?"**

It should therefore produce **questions, structures, research directions, evidence requirements, and analytical possibilities**, rather than filling those structures with invented or completed academic prose.
