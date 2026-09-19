# PROJECT PROPOSAL STRUCTURER & TITLE GENERATOR

## 1. Description

This skill transforms a project title, draft project idea, or both into a structured, coherent, professional project proposal.

The skill can work in two complementary modes:

1. **Proposal Structuring Mode** — when the user provides a project title, idea, or both, develop the concept into a structured project proposal.
2. **Title Generation Mode** — when the user provides a draft idea without a satisfactory title, analyze the idea and suggest exactly **3 alternative project titles** before structuring the proposal.

The skill should preserve the user's original intent while improving clarity, specificity, logical structure, and proposal readiness.

---

## 2. Purpose

The purpose of this skill is to help users move from an initial project concept to a clearly articulated project proposal.

It should:

* Understand the user's project idea.
* Identify the project's central problem or opportunity.
* Clarify the intended objectives and outcomes.
* Generate three suitable title options when a draft idea is provided.
* Select or preserve the user's title appropriately.
* Organize the concept into a logical proposal structure.
* Identify gaps, ambiguities, and unsupported assumptions.
* Distinguish information explicitly provided by the user from reasonable inferences.
* Produce a proposal that can serve as a strong first draft for further development.

The skill should **structure and strengthen the idea, not silently invent substantive project facts**.

---

## 3. Scope

### In Scope

The skill may:

* Interpret a project title.
* Interpret a rough or incomplete project idea.
* Convert notes into proposal language.
* Generate exactly three alternative titles.
* Improve title clarity without changing the underlying project.
* Identify the project problem or need.
* Define objectives based on the provided concept.
* Develop proposed activities or interventions.
* Identify expected outputs and outcomes.
* Suggest indicators where appropriate.
* Structure implementation logic.
* Identify beneficiaries or target groups.
* Identify assumptions, risks, and dependencies.
* Identify missing information.
* Produce a professional proposal draft.
* State assumptions explicitly when they are necessary to proceed.

### Out of Scope

The skill should not:

* Fabricate statistics, research findings, budgets, partnerships, beneficiaries, or evidence.
* Claim that a project is feasible without sufficient information.
* Invent funding requirements or donor criteria unless supplied or specifically researched.
* Change the fundamental purpose of the user's project.
* Present assumptions as confirmed facts.
* Automatically conduct external research unless the user requests research or the execution environment specifically requires it.

---

## 4. Trigger Conditions

Activate this skill when the user asks to:

* Structure a project proposal.
* Develop a project idea into a proposal.
* Turn a project concept into a proposal.
* Draft a project proposal.
* Organize a project idea.
* Improve a project concept.
* Create a proposal from a title.
* Create a proposal from rough notes.
* Suggest project titles and develop the proposal.
* Turn an initial idea into a structured project plan/proposal.

Examples:

> "Structure a proposal around the title: Community Digital Skills Hub"

> "I have an idea about helping unemployed young people learn digital skills. Turn it into a project proposal."

> "Can you develop this project idea and give me three possible titles?"

---

## 5. Non-Trigger Conditions

Do not use this skill as the primary workflow when the user only wants:

* A definition of a project-management term.
* A simple proofreading task unrelated to proposal development.
* A complete grant application requiring a specific funder's form unless the user explicitly asks for proposal structuring.
* A business plan unless the request is specifically framed as a project proposal.
* A literature review without a proposal-development objective.
* A political campaign proposal or electoral persuasion document without adapting to applicable political-content requirements.
* A purely creative project name with no proposal-development objective.

---

## 6. Inputs

### Required

At least one of the following must be provided:

* **Project title**
* **Draft project idea**

A title alone is sufficient to begin.

A draft idea alone is sufficient to begin.

### Optional

The user may provide:

* Project background.
* Problem statement.
* Target population.
* Geographic area.
* Project duration.
* Objectives.
* Proposed activities.
* Expected outcomes.
* Available resources.
* Partners.
* Budget information.
* Funding context.
* Donor or institutional requirements.
* Sector/domain.
* Preferred proposal format.
* Word/page limit.
* Existing notes or documents.

### Contextual

The skill should use relevant information already present in the conversation, including:

* Previously stated project objectives.
* Previously discussed beneficiaries.
* Previously established terminology.
* Existing project constraints.
* Existing proposal-format requirements.

Do not ask the user to repeat information already available.

### Automatically Derived

The AI should infer, where reasonable:

* The likely project domain.
* The central theme.
* The likely problem addressed.
* The likely intended beneficiaries.
* The relationship between activities and intended outcomes.
* The appropriate level of proposal structure.

These are **inferences**, not facts. Where the inference materially affects the proposal, label it as an assumption or ask for clarification.

---

## 7. Outputs

The primary output is a structured project proposal.

### When the user provides only a title

Produce:

1. Project title.
2. Project concept interpretation.
3. Structured proposal.
4. Clearly identified assumptions and information gaps.

Do not generate alternative titles unless the user asks for them.

### When the user provides a draft idea

Produce:

1. **Three alternative project titles**
2. Recommended working title based on fit with the stated idea, without presenting it as objectively "best."
3. Structured project proposal.
4. Assumptions and information gaps.

The three titles should be meaningfully different, for example:

* **Descriptive title** — directly communicates what the project does.
* **Outcome-oriented title** — emphasizes the intended change.
* **Conceptual/engaging title** — memorable while remaining professionally appropriate.

Exactly **3 titles** should be provided unless the user explicitly requests a different number.

### Proposal Structure

Unless the user provides a different required format, use:

1. Project Title
2. Executive Summary
3. Background and Context
4. Problem Statement
5. Project Rationale
6. Overall Goal
7. Specific Objectives
8. Target Beneficiaries
9. Proposed Activities
10. Expected Outputs
11. Expected Outcomes
12. Implementation Approach
13. Timeline / Key Phases
14. Monitoring and Evaluation
15. Risks and Mitigation Measures
16. Sustainability
17. Key Assumptions
18. Information Gaps / Items Requiring Confirmation

If a section cannot reasonably be developed from the available information, state what is missing rather than fabricating content.

---

## 8. Core Principles

### 8.1 Preserve the Idea

The proposal must remain faithful to the user's underlying concept.

### 8.2 Improve Structure, Not Substance Without Basis

The AI may improve wording, organization, and logical connections, but must not introduce unsupported substantive claims.

### 8.3 Separate Facts From Inference

Clearly distinguish:

* User-provided information.
* Reasonable interpretation.
* Proposed elements.
* Information requiring confirmation.

### 8.4 Make the Logic Explicit

The proposal should demonstrate a logical chain:

**Problem → Need → Goal → Objectives → Activities → Outputs → Outcomes → Impact**

### 8.5 Minimize Unnecessary Questions

Proceed with reasonable assumptions when they do not materially change the project.

### 8.6 Flag Material Uncertainty

If missing information could substantially change the proposal, identify it explicitly.

### 8.7 Keep Titles Faithful to the Concept

Alternative titles must represent the actual project rather than exaggerating its scope or expected impact.

---

## 9. Execution Workflow

### Phase 1 — Parse the Input

**Objective:** Understand what the user has supplied.

**Actions:**

1. Determine whether the user supplied:

   * A title.
   * A draft idea.
   * Both.
2. Extract explicit project information.
3. Identify the project's apparent domain.
4. Identify the central intended change.
5. Identify any explicit constraints.

**Decision:**

* If either title or idea exists → proceed.
* If neither exists → ask the user for a project title or draft idea.

---

### Phase 2 — Analyze the Project Concept

Identify:

* What problem the project appears to address.
* Who is affected.
* What the project proposes to do.
* What change it seeks to produce.
* Where the project operates, if known.
* What resources or actors appear relevant.
* What information is missing.

Create an internal concept model:

**Problem → Target Group → Intervention → Outputs → Intended Outcomes**

Do not treat inferred elements as confirmed facts.

---

### Phase 3 — Generate Titles When Needed

If a draft idea is supplied and a suitable title is not already provided:

Generate exactly three titles.

Each title must:

* Reflect the actual project idea.
* Be concise.
* Be professionally usable.
* Avoid unsupported claims.
* Avoid unnecessary jargon.
* Be distinguishable from the other two.

Use three different title strategies:

**Title A — Descriptive**

Clearly describes the project.

**Title B — Outcome-Oriented**

Emphasizes the change or result the project seeks to achieve.

**Title C — Engaging**

Uses a memorable concept while retaining professional clarity.

If the user already supplied a title, preserve it as the working title unless the user asks for alternatives.

---

### Phase 4 — Establish the Proposal Logic

Construct the proposal's causal structure.

#### Problem

What issue or unmet need is the project responding to?

#### Rationale

Why does the proposed intervention logically address the identified problem?

#### Goal

What broad change does the project seek?

#### Objectives

What specific changes should the project achieve?

Objectives should be:

* Specific where information allows.
* Logically connected to the goal.
* Realistic relative to the stated project.
* Measurable where sufficient information exists.

Do not invent numerical targets merely to make objectives appear measurable.

#### Activities

Translate objectives into concrete project actions.

#### Outputs

Identify the immediate products or deliverables resulting from activities.

#### Outcomes

Identify the changes expected to result from those outputs.

---

### Phase 5 — Build the Proposal

Write each proposal section using the strongest information available.

Use professional proposal language while avoiding unnecessary verbosity.

Where information is insufficient:

> "To be confirmed: project duration."

rather than inventing a duration.

Where an inference is useful:

> "Assumption: the primary target group is expected to be..."

---

### Phase 6 — Identify Gaps

Review the proposal for missing information.

Typical gaps include:

* Geographic scope.
* Target population size.
* Project duration.
* Baseline information.
* Specific objectives.
* Implementation partners.
* Budget.
* Funding source.
* Evidence supporting the problem.
* Monitoring indicators.
* Sustainability arrangements.

Prioritize gaps that materially affect proposal quality.

---

### Phase 7 — Quality Control

Before returning the proposal, verify:

* The proposal matches the user's original idea.
* The title accurately represents the project.
* The three generated titles, when required, represent the same underlying idea.
* Objectives logically connect to activities.
* Activities logically connect to outputs.
* Outputs logically connect to outcomes.
* No unsupported facts have been introduced.
* Assumptions are identifiable.
* Missing information is clearly marked.
* No requested proposal component is omitted.
* The writing is internally consistent.
* The proposal can be used as a coherent first draft.

---

## 10. Decision Logic

### Title vs. Draft Idea

**IF** the user provides both a title and draft idea
→ Use the title as the working title and use the idea to validate and develop it.

**IF** the user provides only a title
→ Interpret the likely project concept and structure a proposal around it, while identifying assumptions.

**IF** the user provides only a draft idea
→ Generate exactly three title options, then structure the proposal.

**IF** the user provides neither
→ Ask for a project title or draft idea.

### Ambiguity

**IF** ambiguity does not materially affect the proposal
→ Make a reasonable assumption and label it.

**IF** ambiguity materially changes the project's purpose, beneficiaries, intervention, or outcomes
→ Ask a focused clarification question.

### Missing Information

**IF** information is missing but a reasonable generic formulation is possible
→ Continue and flag the information as requiring confirmation.

**IF** the missing information is essential to the project's logic
→ Ask for it before finalizing that component.

### Unsupported Claims

**IF** a claim cannot be supported by user-provided information or available evidence
→ Do not present it as fact.

### User Changes Requirements

**IF** the user subsequently changes the title, target group, objectives, or scope
→ Rebuild the affected sections while preserving unaffected information.

---

## 11. Tool Strategy

This skill does not inherently require external tools.

### Files

Use available file tools when the user supplies:

* Existing proposal drafts.
* Project concept notes.
* Guidelines.
* Templates.
* Donor requirements.
* Reference documents.

When using a supplied document, preserve its terminology and requirements.

### Web Research

Use web research only when:

* The user explicitly asks for research.
* The proposal requires current factual evidence.
* The user asks for statistics, policy context, market information, or other externally verifiable information.

When research is performed:

* Prefer authoritative sources.
* Cite externally sourced factual claims.
* Separate researched facts from the user's original project concept.

### Other Tools

Do not invoke tools merely to make the proposal appear more sophisticated. Use them only when they materially improve accuracy or fulfill an explicit requirement.

---

## 12. Information & Source Validation

The skill must distinguish three information categories:

### Confirmed

Explicitly provided by the user or verified through an appropriate source.

### Inferred

Reasonably derived from the user's description but not explicitly confirmed.

### Proposed

A suggested component introduced to make the proposal structurally complete.

Use labels such as:

* **Assumption**
* **Proposed**
* **To be confirmed**

Never turn an inference into a factual claim.

---

## 13. Ambiguity Handling

The skill should avoid unnecessary clarification questions.

### Low-impact ambiguity

Proceed using the most reasonable interpretation.

Example:

If the user says:

> "A project helping young people with digital skills"

The skill can proceed with a general youth digital-skills project rather than asking immediately for a precise age range.

### High-impact ambiguity

Ask for clarification when the difference would substantially change the proposal.

Example:

> "Is the project intended for unemployed young adults, secondary-school students, or university students?"

This distinction materially affects activities, beneficiaries, indicators, and implementation.

---

## 14. Error Handling

### Empty Input

Ask for a project title or draft idea.

### Very Short Input

Do not reject the request. Develop a preliminary proposal and clearly identify assumptions.

### Highly Complex Input

Extract the central project logic first, then organize secondary information into the appropriate proposal sections.

### Contradictory Input

Identify the contradiction and ask the user to resolve it if it materially affects the proposal.

### Unclear Scope

Use the narrowest reasonable interpretation and state the assumption.

### Insufficient Information

Produce the strongest defensible draft possible and include an "Information Gaps" section.

---

## 15. Edge Cases

### User provides a title that is too broad

Interpret it conservatively and identify the missing project dimensions.

### User provides a title that implies outcomes not supported by the idea

Do not amplify the claim. Flag the mismatch.

### User provides an extremely detailed idea

Do not unnecessarily simplify it. Extract and reorganize the existing detail.

### User provides multiple project ideas

Separate them conceptually and ask whether they should be treated as:

* One integrated project, or
* Separate proposals,

unless the relationship is obvious.

### User provides a proposal template

Follow the template instead of automatically imposing the default structure.

### User requests a specific word count

Respect the requested limit while preserving the proposal's essential logic.

### User requests only titles

Do not generate a full proposal unless requested.

---

## 16. User Interaction Rules

### Proceed Automatically When

The user has provided enough information to construct a meaningful proposal.

### Ask Questions When

A missing detail would materially alter:

* Project purpose.
* Target beneficiaries.
* Main intervention.
* Geographic scope.
* Expected outcomes.
* Required proposal format.

### State Assumptions When

A reasonable interpretation allows the work to continue without materially changing the concept.

### Offer Choices When

The user could reasonably choose between substantially different proposal structures or title styles.

### Do Not

* Ask for every possible project detail before starting.
* Repeatedly request information already provided.
* Present invented specifics as facts.
* Overcomplicate a simple project idea.

---

## 17. Quality-Control Checklist

Before finalizing, confirm:

### Concept

* [ ] The project idea is accurately understood.
* [ ] The central problem is identifiable.
* [ ] The intended change is clear.

### Titles

When title generation is required:

* [ ] Exactly three titles are provided.
* [ ] Titles are meaningfully differentiated.
* [ ] All three accurately represent the idea.
* [ ] None makes unsupported claims.

### Proposal Logic

* [ ] Problem connects to rationale.
* [ ] Rationale connects to goal.
* [ ] Goal connects to objectives.
* [ ] Objectives connect to activities.
* [ ] Activities produce outputs.
* [ ] Outputs contribute to outcomes.

### Accuracy

* [ ] No facts were fabricated.
* [ ] Assumptions are identifiable.
* [ ] Proposed elements are distinguishable from confirmed information.
* [ ] Missing information is acknowledged.

### Usability

* [ ] The proposal is coherent.
* [ ] The structure is easy to navigate.
* [ ] The language is professional.
* [ ] The user can continue developing the proposal without reconstructing the logic.

---

## 18. Failure Modes & Recovery

### Failure: No usable input

**Detection:** No title or project idea is available.

**Recovery:** Ask the user for a title or draft idea.

### Failure: Title and idea conflict

**Detection:** The title describes a substantially different project from the draft idea.

**Recovery:** Identify the mismatch and ask whether the title or idea should take precedence.

### Failure: Proposal requires unsupported facts

**Detection:** A section would require statistics, evidence, or factual claims not supplied.

**Recovery:** Mark the section as requiring evidence or conduct research only if requested/appropriate.

### Failure: Objectives are too vague

**Detection:** Objectives cannot be distinguished from activities or broad aspirations.

**Recovery:** Rewrite them into clearer objective statements without inventing numerical targets.

### Failure: Activities do not support objectives

**Detection:** The causal relationship between activities and objectives is weak or absent.

**Recovery:** Flag the inconsistency and propose structurally appropriate activities as suggestions.

### Failure: Scope is excessive

**Detection:** The project attempts to address unrelated problems or populations.

**Recovery:** Identify the scope issue and preserve the user's intent while suggesting a clearer boundary.

---

## 19. Performance & Efficiency Rules

1. Do not ask questions that can reasonably be answered through inference.
2. Do not generate unnecessary research.
3. Do not repeat the user's information excessively.
4. Generate exactly three titles when title generation is triggered.
5. Prioritize the project's logical structure over decorative language.
6. Use concise proposal language unless the user requests extensive detail.
7. Preserve useful detail from complex source material.
8. Identify only material information gaps.
9. Avoid unnecessary tools.
10. Prefer a complete preliminary proposal over a long list of questions.

---

## 20. Security / Privacy / Safety Considerations

* Do not expose private information unnecessarily.
* Do not invent personal information about beneficiaries, partners, staff, or organizations.
* Treat user-provided sensitive project information as confidential within the task.
* Do not fabricate credentials, endorsements, partnerships, funding commitments, or institutional approvals.
* Do not imply that a proposal has been approved, funded, validated, or endorsed unless that is explicitly established.
* If the project concerns a regulated, high-risk, or sensitive domain, clearly distinguish proposal drafting from professional or regulatory validation.

---

## 21. Examples

### Example 1 — Draft Idea Without a Title

**User input:**

> "I want to create a project that helps unemployed young people learn digital skills so they can access better employment opportunities."

**Expected behavior:**

Generate exactly three titles, such as:

1. A descriptive title focused on youth digital skills.
2. An outcome-oriented title focused on employment opportunities.
3. A more engaging professional title.

Then develop the proposal around:

**Problem → Youth unemployment/digital-skills gap → Training intervention → Skills development → Improved employment readiness**

The proposal should not invent unemployment statistics, participant numbers, locations, or employment rates.

---

### Example 2 — Title Only

**User input:**

> "Community Digital Skills Hub"

**Expected behavior:**

Use the title as the working title.

Develop a preliminary proposal around the likely concept while identifying assumptions such as:

* Target community.
* Specific digital skills.
* Intended beneficiaries.
* Delivery model.
* Duration.
* Expected outcomes.

Do not pretend these details were supplied by the user.

---

### Example 3 — Title and Draft Idea

**User input:**

> Title: "Green Schools Initiative"

> Idea: "A project that helps secondary schools reduce waste by introducing recycling systems, student environmental clubs, and practical environmental education."

**Expected behavior:**

Retain the supplied title.

Build the proposal around:

* School waste management.
* Student engagement.
* Environmental education.
* Recycling systems.
* Expected behavioral and operational changes.

The proposal should distinguish confirmed information from proposed implementation details.

---

### Example 4 — Ambiguous Idea

**User input:**

> "I want a project to help women become financially independent."

**Expected behavior:**

Do not immediately assume whether the project involves:

* Employment,
* Entrepreneurship,
* Financial literacy,
* Vocational training,
* Access to finance,
* Or another intervention.

If a preliminary proposal is requested, provide a broad draft and explicitly state that the intervention model needs confirmation.

If the intervention type is essential to the requested proposal, ask a focused clarification question.

---

### Example 5 — Existing Detailed Idea

**User input:**

> "We want to work with 10 secondary schools over two years. Each school will establish a student environmental club, conduct waste audits, introduce recycling stations, and run monthly environmental awareness activities..."

**Expected behavior:**

Do not ask the user to repeat information.

Extract:

* Target institutions.
* Duration.
* Activities.
* Outputs.
* Intended outcomes.

Then structure the information into the proposal framework and identify only genuinely missing components.

---

## 22. Final Execution Instructions

When this skill is triggered:

1. Read the user's project title and/or draft idea.
2. Extract all explicit project information.
3. Identify the central problem, target group, intervention, intended outputs, and intended outcomes.
4. Distinguish confirmed information from assumptions and proposed elements.
5. If the user provides a draft idea without an established title, generate **exactly three distinct, professionally appropriate title options**.
6. If the user provides a title, preserve it unless the user explicitly requests alternatives.
7. Build the proposal using the standard structure unless the user provides a different format.
8. Establish a clear **Problem → Goal → Objectives → Activities → Outputs → Outcomes** logic.
9. Do not invent statistics, targets, partners, budgets, locations, evidence, or other substantive facts.
10. Where information is missing but a reasonable draft can proceed, make a clearly stated assumption.
11. Where missing information materially changes the project, ask a focused clarification question.
12. Identify important information gaps at the end of the proposal.
13. Perform the quality-control checklist before returning the result.
14. Ensure the final proposal is coherent, professionally written, faithful to the user's idea, and usable as a foundation for further development.
15. If the user later changes a requirement, revise the affected proposal components while preserving valid existing information.
