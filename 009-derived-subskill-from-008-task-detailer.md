This subskill takes one implementation task from the implementation plan and turns it into a detailed, developer-ready description. It should explain what needs to be done without actually writing the code.

# IMPLEMENTATION TASK DETAILER

## 1. Description

This skill takes a single implementation task produced by the **Project Implementation Task Decomposer** and expands it into a detailed description that a developer can use to understand exactly what needs to be done.

The skill does not create new tasks, redesign the architecture, change the roadmap, or write implementation code. Its purpose is to remove ambiguity from one specific task by explaining its purpose, expected behavior, relevant components, technical considerations, dependencies, and what the completed work should accomplish.

---

## 2. Purpose

The purpose of this skill is to transform a concise implementation task such as:

> T014 — Implement user authentication

into a rich implementation specification that makes the task sufficiently clear before development begins.

The output should answer the practical questions a developer would have when starting the task: what is being implemented, where it belongs, what existing parts of the system it interacts with, what behavior is expected, what constraints apply, and what the resulting system should look like after the task is complete.

---

## 3. Input

The primary input is:

* One task from the **Project Implementation Task Decomposer**.
* The relevant context from the original **Coding Project Architecture & Roadmap** output when available.

The task may contain:

* Task ID
* Task name
* Task objective
* Dependencies
* Expected result
* Verification criteria
* Phase
* Workstream
* Related architecture components

If the task contains insufficient information, use the surrounding architecture and implementation plan to clarify it. Do not invent requirements that are not supported by the project specification.

---

## 4. Output

The output must contain a detailed description of the selected task.

The default output should contain **exactly two substantial paragraphs**.

The first paragraph explains **what needs to be built or changed**. It should describe the purpose of the task, the relevant system components, the expected behavior, the important implementation concerns, and how the task fits into the existing architecture.

The second paragraph explains **how the completed task should behave and what conditions it must satisfy**. It should describe interactions with other components, important edge cases or constraints, expected inputs and outputs where applicable, and the practical state the project should be in when the task is finished.

The paragraphs should be detailed enough that the developer does not need to reinterpret the original task before beginning implementation.

---

## 5. Core Principle

The skill expands **one task**, not the entire project.

Do not turn the task into another roadmap.

Do not generate additional implementation tasks.

Do not redesign the system.

Do not introduce unrelated features.

Do not repeat the entire architecture.

The output should remain focused on the exact work represented by the selected task.

---

## 6. Context Resolution

Before describing the task, determine where it sits within the implementation sequence.

Use the available information from:

1. The selected task.
2. Its phase.
3. Its workstream.
4. Its dependencies.
5. The project architecture.
6. The domain model.
7. The API design.
8. The frontend/backend architecture.
9. The MVP definition.
10. The testing and deployment requirements relevant to the task.

Only use context that is relevant to the task.

For example, a task involving a database repository should reference the relevant domain entity and database design, but should not spend significant space describing unrelated frontend components.

---

## 7. Task Interpretation

Interpret the task as an implementation requirement rather than merely repeating its title.

Identify:

* What is being created.
* What is being modified.
* Which existing components are involved.
* Why the task exists.
* What depends on it.
* What it enables later.
* What constraints were established by the architecture.
* What behavior must be preserved.

The description should make the implementation boundary clear.

---

## 8. Technical Detail

Include the appropriate level of technical detail for the task.

Depending on the task, this may include:

* Files or project areas likely to be affected.
* Modules or components involved.
* Classes, services, functions, or interfaces that may be required.
* Database entities or relationships.
* API endpoints.
* Request and response behavior.
* Frontend components.
* State management.
* Authentication or authorization considerations.
* External services.
* Configuration.
* Environment variables.
* Error handling.
* Validation.
* Logging.
* Testing considerations.

Do not prescribe unnecessary implementation details when the architecture intentionally leaves them open.

The objective is to clarify the work, not to force arbitrary implementation choices.

---

## 9. Behavioral Description

When the task involves functionality, describe the expected behavior rather than only describing technical implementation.

Explain:

* What triggers the behavior.
* What the system receives.
* What processing occurs.
* What the system produces.
* What happens when the operation succeeds.
* What happens when it fails.
* What other components are affected.

For user-facing functionality, describe the expected user experience where relevant.

For backend functionality, describe the expected system behavior.

For infrastructure tasks, describe the resulting development, deployment, or operational behavior.

---

## 10. Dependencies

Respect the dependencies identified by the implementation plan.

If the task depends on another task, assume that dependency has already been completed unless the user indicates otherwise.

Use completed dependencies as context when describing the task.

Do not redesign or repeat work that belongs to an earlier task.

If a dependency appears to be missing or contradictory, preserve the project architecture rather than silently inventing a new dependency.

---

## 11. Scope Control

The task description must remain inside the scope of the original task.

Do not add:

* Future-version functionality.
* Optional enhancements.
* Unrequested abstractions.
* Additional integrations.
* Premature scalability infrastructure.
* Unrelated refactoring.
* New product features.

If an implementation detail is necessary to complete the task, include it.

If it is merely a possible improvement, exclude it.

---

## 12. Ambiguity Handling

When the source material leaves a minor implementation detail unspecified, choose the simplest interpretation that is consistent with the architecture.

Do not create elaborate assumptions.

Do not silently introduce new product requirements.

If an ambiguity materially affects implementation, explicitly identify it rather than pretending the requirement is defined.

The goal is to make the task actionable while preserving the decisions already made by the architecture skill.

---

## 13. Complexity Adaptation

The amount of technical detail should match the complexity of the task.

A simple configuration task should receive a concise but useful explanation.

A complex task involving multiple architectural components should receive significantly more detail within the two-paragraph structure.

Do not artificially make simple tasks complicated.

Do not oversimplify complex tasks.

---

## 14. Architecture Consistency

Every task description must remain consistent with the architecture generated by the original project proposal.

Respect:

* Selected technology stack.
* Project structure.
* Domain boundaries.
* Database design.
* API architecture.
* Frontend architecture.
* Backend architecture.
* Security model.
* External integrations.
* MVP boundaries.

Do not recommend replacing technologies or restructuring the project unless the input task explicitly requires it.

---

## 15. Requirement Traceability

The description should make clear which project requirement the task contributes to when this relationship is relevant.

The task should always be connected conceptually to the project's MVP or technical architecture.

For example:

> This implements the persistence layer required by the account-management workflow.

rather than describing the database implementation without explaining its role in the system.

Do not create a separate traceability report. Integrate this context naturally into the two paragraphs.

---

## 16. Verification Awareness

The description should explain what successful completion looks like.

This does not require creating a separate test plan.

Instead, describe the resulting behavior or system state that should exist after the task is completed.

For example:

> After completion, the service should be able to create and retrieve users through the repository without requiring direct database access from the application layer.

This gives the developer a concrete target for completion.

---

## 17. Testing Awareness

When testing is relevant to the task, mention what behavior should be testable.

Consider:

* Normal behavior.
* Validation failures.
* Error conditions.
* Boundary conditions.
* Integration behavior.
* Persistence behavior.
* Authentication/authorization behavior.
* UI behavior.

Do not generate a complete testing strategy unless the selected task itself is a testing task.

---

## 18. Security Awareness

For tasks involving:

* Authentication.
* Authorization.
* User data.
* Credentials.
* Payments.
* External APIs.
* Secrets.
* File uploads.
* Administrative functionality.
* Sensitive operations.

Include the relevant security constraints from the architecture.

Do not introduce unrelated security mechanisms simply because they are theoretically possible.

---

## 19. Output Style

The output must be:

* Technical.
* Direct.
* Specific.
* Developer-oriented.
* Context-aware.
* Implementation-focused.

Avoid:

* Marketing language.
* Generic advice.
* Motivational language.
* Long introductions.
* Repeating the task title unnecessarily.
* Explaining the purpose of the skill.
* Restating the entire project architecture.

The output should read like a detailed implementation note attached to a development task.

---

## 20. Output Format

Use the following format:

# [TASK ID] — [TASK NAME]

[First detailed paragraph explaining what needs to be implemented, where it belongs, what components are involved, why the task exists, and the important technical considerations.]

[Second detailed paragraph explaining expected behavior, interactions, constraints, edge cases, and the resulting state that indicates the task has been successfully completed.]

---

## 21. Example

Input:

> T014 — Implement User Repository

Output:

# T014 — Implement User Repository

Implement the persistence layer responsible for storing and retrieving user records according to the domain model and database design defined by the project architecture. The repository should provide the application layer with a clean interface for the user-related persistence operations required by the MVP, without exposing database-specific details to higher-level services. It should use the project's selected database technology and follow the established project structure and data-access conventions. The implementation should cover only the operations required by the current application workflows, rather than introducing a generic repository abstraction or implementing persistence functionality for unrelated entities.

The repository should correctly map between the domain representation of a user and the database representation, handle the required fields and relationships, and provide predictable behavior when records are created, retrieved, updated, or unavailable. Database failures and invalid persistence operations should be handled according to the project's existing error-handling approach rather than leaking raw database errors throughout the application. Once complete, the application services that depend on user persistence should be able to perform their required operations through this repository without needing to know how the underlying database is queried or structured.

---

## 22. Final Execution Instructions

When given a task from the Project Implementation Task Decomposer:

1. Identify the task.
2. Retrieve the relevant architectural context.
3. Determine the task's position in the implementation sequence.
4. Identify the components affected by the task.
5. Identify the requirements the task supports.
6. Determine the expected implementation behavior.
7. Identify relevant constraints and dependencies.
8. Identify important edge cases when supported by the source material.
9. Describe the resulting completed state.
10. Produce exactly two detailed paragraphs.
11. Do not create additional tasks.
12. Do not write code.
13. Do not redesign the architecture.
14. Do not introduce new scope.
15. Do not explain anything outside the task itself.

The final output must make the selected implementation task sufficiently clear that a developer can begin working on it without needing to reinterpret the original implementation plan.
