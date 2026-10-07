Using the generator’s implementation-ready structure and decision-making requirements, I’ve designed this as a planning skill rather than a simple calendar generator. It treats time, energy, priorities, deadlines, projects, study, work, recovery, and personal life as a constrained system. 

# PERSONAL PLANNING & SCHEDULING ENGINE

## 1. Description

The Personal Planning & Scheduling Engine transforms a user's goals, projects, responsibilities, activities, commitments, deadlines, study requirements, work obligations, and personal priorities into a realistic schedule covering days, weeks, and months.

The skill is designed around sustainable execution rather than maximum calendar utilization. It must balance productivity with sleep, exercise, meals, downtime, social life, personal maintenance, recovery, and reasonable transition time. The objective is not to fill every available hour, but to create a schedule that gives the user the highest realistic probability of accomplishing what matters without systematically creating exhaustion or overload.

The skill operates at multiple planning horizons:

* Long-term: monthly objectives and major milestones.
* Medium-term: weekly priorities and workload allocation.
* Short-term: daily time blocks and concrete actions.
* Ongoing: reviews, adjustments, unfinished work, and schedule adaptation.

The resulting schedule must be actionable enough that the user can follow it without having to repeatedly decide what to do next.

---

## 2. Purpose

The primary purpose is to answer:

> "Given everything I need and want to accomplish, how should I allocate my available time so that I make meaningful progress while maintaining a healthy and sustainable life?"

The skill should convert vague ambitions such as "study more", "work on my project", "exercise regularly", or "finish this by the end of the month" into measurable time allocations, sessions, milestones, and concrete next actions.

It must distinguish between:

* Things that must happen.
* Things that should happen.
* Things the user wants to happen.
* Things that can happen if capacity remains.
* Things that should explicitly be postponed or removed.

The skill must be willing to tell the user when their requested workload exceeds realistic capacity.

---

## 3. Scope

### Included

The skill handles:

* Monthly planning.
* Weekly planning.
* Daily scheduling.
* Project scheduling.
* Study scheduling.
* Work scheduling.
* Personal goal scheduling.
* Habit scheduling.
* Exercise and health routines.
* Deep-work allocation.
* Administrative tasks.
* Recurring commitments.
* Deadlines.
* Milestones.
* Task prioritization.
* Time estimation.
* Capacity analysis.
* Workload balancing.
* Recovery and downtime.
* Schedule optimization.
* Weekly reviews.
* Monthly reviews.
* Rescheduling after missed work.
* Detecting unrealistic plans.
* Breaking large objectives into scheduled sessions.
* Creating realistic buffers.

### Outside Scope

The skill should not:

* Act as a medical professional.
* Diagnose health conditions.
* Prescribe medical treatment.
* Assume a specific productivity philosophy unless requested.
* Schedule every minute of the user's life unnecessarily.
* Treat leisure as wasted time.
* Optimize solely for productivity.
* Guarantee that goals will be achieved.
* Invent commitments, deadlines, available hours, or obligations.

---

## 4. Trigger Conditions

Activate when the user asks to:

* Plan their week.
* Plan their month.
* Schedule upcoming work.
* Organize their time.
* Build a study schedule.
* Balance work and personal projects.
* Fit several goals into their available time.
* Create a daily routine.
* Turn goals into a calendar.
* Determine what they can realistically accomplish.
* Reorganize an existing schedule.
* Recover from falling behind.
* Plan a project alongside work/study/life.
* Decide how many hours to dedicate to different objectives.
* Build a sustainable productivity system.

Typical requests include:

> "Plan my next month."

> "I work 40 hours, want to study 10 hours, exercise 4 times, and finish this project. Build my schedule."

> "Here are all my goals and commitments. Tell me how to structure the next three weeks."

> "I fell behind this week. Rebuild my schedule."

---

## 5. Non-Trigger Conditions

Do not use this skill when the user only wants:

* A simple list of tasks.
* A project roadmap without calendar allocation.
* Generic productivity advice.
* A single reminder.
* A simple one-off event recommendation.
* A general explanation of time management.
* A project breakdown where no scheduling is requested.

If scheduling becomes necessary during such a request, the skill may be activated.

---

# 6. Inputs

## Required

The skill requires enough information to establish the user's planning horizon and available capacity.

### Planning Horizon

Type: date range or relative period.

Examples:

* "Next week."
* "October."
* "The next three months."
* "From October 10 to November 15."

Default:

If the user does not specify a horizon, default to the next 7 days for an immediate scheduling request or the current calendar month for a broader planning request.

### Objectives / Activities

Type: list of goals, projects, tasks, commitments, habits, or activities.

Each item should contain whatever information the user knows:

* Name.
* Desired outcome.
* Deadline.
* Estimated effort.
* Priority.
* Frequency.
* Dependencies.
* Preferred times.
* Minimum acceptable progress.

Do not require all fields.

### Fixed Commitments

Examples:

* Work.
* Classes.
* Appointments.
* Meetings.
* Commute.
* Family obligations.
* Existing recurring activities.

These represent time that cannot normally be allocated elsewhere.

---

## Optional

The skill should accept:

### Working Hours

Example:

> Monday-Friday, 09:00-17:00.

### Sleep Schedule

Example:

> Usually sleep 23:30-07:30.

### Exercise Preferences

Example:

> Gym Monday, Wednesday, Friday.

### Study Preferences

Example:

> Best concentration in the morning.

### Productivity Preferences

Examples:

* Morning deep work.
* Short sessions.
* Long uninterrupted blocks.
* Pomodoro.
* Flexible schedule.
* Fixed routine.

### Energy Patterns

Examples:

* High energy in mornings.
* Low energy after lunch.
* Strong evenings.

### Social / Personal Requirements

Examples:

* One free evening.
* Weekend family time.
* Saturday completely free.
* Daily reading.

### Existing Schedule

A calendar, timetable, list of recurring obligations, or previous plan.

### Task Estimates

Estimated duration for individual tasks.

### Deadlines

Hard deadlines should be explicitly distinguished from preferred deadlines.

---

## Contextual Inputs

The skill may use information already provided earlier in the conversation, including:

* Previous schedules.
* Existing goals.
* Project plans.
* Stated working hours.
* Previously established routines.
* Previously discussed deadlines.
* Current progress.
* User preferences.

Do not repeatedly ask for information that is already available.

---

## Automatically Derived Inputs

The skill should calculate or infer:

* Available hours.
* Fixed versus flexible time.
* Required versus discretionary time.
* Remaining capacity.
* Estimated workload.
* Deadline pressure.
* Priority.
* Scheduling conflicts.
* Required weekly effort.
* Project runway.
* Buffer requirements.
* Overload risk.
* Appropriate session lengths.
* Suitable scheduling windows.

These are derived values, not facts. Clearly distinguish estimates from user-provided information.

---

# 7. Outputs

The skill should produce a schedule appropriate to the requested planning horizon.

## Monthly Plan

When planning a month, provide:

1. Monthly objectives.
2. Major deadlines.
3. Major milestones.
4. Weekly allocation of effort.
5. Project progression.
6. Study progression.
7. Work obligations.
8. Personal and health commitments.
9. Recovery periods.
10. Expected outcomes by the end of the month.

The month should be treated as a sequence of weekly execution periods rather than one giant task list.

---

## Weekly Plan

Provide:

* Weekly priorities.
* Key outcomes.
* Total planned work/study/project hours.
* Daily allocation.
* Fixed commitments.
* Deep-work blocks.
* Administrative blocks.
* Exercise.
* Personal time.
* Recovery.
* Buffer.
* Important deadlines.
* Explicit "if capacity remains" items.

---

## Daily Schedule

When appropriate, provide:

* Time.
* Activity.
* Objective.
* Duration.
* Priority.
* Optional notes.

Example structure:

| Time        | Activity               | Type      | Priority |
| ----------- | ---------------------- | --------- | -------- |
| 07:30–08:00 | Morning routine        | Personal  | Required |
| 08:00–10:00 | Project implementation | Deep work | High     |
| 10:00–10:30 | Break                  | Recovery  | Required |
| 10:30–12:00 | Work                   | Work      | High     |

Do not create artificial precision when the user's life does not require it.

---

## Capacity Report

Every substantial planning operation should internally calculate:

* Fixed hours.
* Required life-maintenance hours.
* Planned productive hours.
* Flexible hours.
* Unallocated buffer.
* Overloaded hours.
* Optional workload.

If the requested activities exceed realistic capacity, explicitly identify the conflict.

---

## Schedule Risk Assessment

Classify the plan as:

* Comfortable.
* Sustainable but demanding.
* Aggressive.
* Overloaded.

Explain the primary reason.

---

# 8. Core Principles

### Principle 1 — Capacity Before Goals

Never schedule objectives before determining available capacity.

### Principle 2 — Reality Over Ambition

The schedule must reflect the user's actual available time rather than the amount of work they wish they could accomplish.

### Principle 3 — Health Is Part of the Schedule

Sleep, meals, exercise, rest, downtime, hygiene, and personal life are legitimate scheduling requirements.

They must not automatically be treated as disposable time.

### Principle 4 — Fixed Commitments First

Hard commitments are allocated before flexible activities.

### Principle 5 — Priorities Determine Allocation

High-priority goals receive capacity before low-priority goals.

### Principle 6 — Buffers Are Mandatory

Do not schedule 100% of theoretical free time.

Unexpected events, transitions, fatigue, overruns, and administrative work require capacity.

### Principle 7 — Deep Work Is Protected

Important cognitively demanding work should receive sufficiently long uninterrupted blocks whenever practical.

### Principle 8 — Avoid Context Switching

Do not unnecessarily alternate between unrelated tasks throughout the day.

### Principle 9 — Every Goal Needs Execution Time

A goal without scheduled execution capacity is not part of the plan.

### Principle 10 — Plans Must Be Adjustable

The schedule is a decision system, not a rigid contract.

When reality changes, reschedule rather than treating missed blocks as personal failure.

### Principle 11 — Do Not Over-Schedule

A good plan should leave enough flexibility for normal life.

### Principle 12 — Completion Beats Busyness

Measure success through meaningful outcomes rather than hours spent looking busy.

---

# 9. Execution Workflow

## Phase 1 — Parse the Request

### Objective

Understand what the user wants to accomplish and over what period.

### Actions

Extract:

* Planning horizon.
* Goals.
* Projects.
* Tasks.
* Commitments.
* Deadlines.
* Recurring activities.
* Desired routines.
* Constraints.

### Decision

If enough information exists, continue.

If a missing detail materially changes the schedule, ask for it.

Otherwise infer a reasonable default.

---

## Phase 2 — Build the Activity Inventory

Create a normalized inventory.

For each item determine:

* Category.
* Desired outcome.
* Estimated duration.
* Frequency.
* Deadline.
* Priority.
* Flexibility.
* Energy requirement.
* Dependency.
* Preferred time.
* Whether it is mandatory or optional.

Classify each activity as:

### Fixed

Must occur at a specific time.

### Flexible Required

Must occur but can move.

### Strategic

Important progress toward a goal.

### Maintenance

Necessary recurring life activity.

### Optional

Useful but expendable.

---

## Phase 3 — Establish Available Capacity

Calculate:

`Total Time = Planning Period × 24 hours`

Then subtract:

* Sleep.
* Fixed commitments.
* Meals.
* Necessary personal maintenance.
* Commute.
* Existing obligations.

Then establish realistic discretionary capacity.

Do not assume every remaining hour is productive.

Create a planning reserve for:

* Breaks.
* Transitions.
* Unexpected tasks.
* Delays.
* Recovery.

---

## Phase 4 — Determine Priorities

Rank activities using:

1. Hard deadlines.
2. Consequences of missing them.
3. Importance to the user's stated objectives.
4. Dependencies.
5. Strategic value.
6. Effort required.
7. Available time.

Priorities should be divided into:

* Critical.
* High.
* Medium.
* Low.
* Optional.

Do not assign importance merely because an activity is urgent.

---

## Phase 5 — Calculate Required Effort

For each major objective estimate:

`Required Weekly Effort = Remaining Effort / Remaining Weeks`

For recurring activities:

`Weekly Effort = Session Duration × Frequency`

For projects with milestones:

`Milestone Effort = Estimated Work Required Before Milestone`

Compare required effort against actual available capacity.

---

## Phase 6 — Detect Capacity Conflicts

Compare:

`Required Capacity + Planned Buffer`

against:

`Available Capacity`

If:

`Required Capacity <= Available Capacity`

continue normally.

If:

`Required Capacity > Available Capacity`

identify the overload.

Do not silently compress sleep, recovery, meals, or basic health activities to make the schedule fit.

Instead:

1. Remove optional work.
2. Reduce low-priority work.
3. Reduce unnecessary context switching.
4. Move flexible work.
5. Negotiate deadlines if appropriate.
6. Reduce scope.
7. Increase available time only if realistically possible.
8. Present the remaining conflict to the user.

---

## Phase 7 — Build the Monthly Structure

For monthly plans:

1. Place major deadlines.
2. Place major milestones.
3. Divide projects into weekly targets.
4. Allocate recurring activities.
5. Assign weekly workload.
6. Add recovery periods.
7. Add buffer.
8. Keep the final week from becoming overloaded.

Do not distribute work evenly if deadlines or dependencies make uneven allocation more sensible.

---

## Phase 8 — Build the Weekly Structure

For each week:

1. Identify 1–3 primary outcomes.
2. Place fixed commitments.
3. Place health and maintenance activities.
4. Place high-priority work.
5. Place project blocks.
6. Place study blocks.
7. Place secondary tasks.
8. Add personal time.
9. Add buffers.
10. Reserve unscheduled capacity.

Avoid giving the user an unrealistic list of ten "top priorities."

---

## Phase 9 — Build Daily Blocks

Convert weekly objectives into concrete sessions.

Prefer blocks such as:

* 60–120 minute deep-work sessions.
* 30–60 minute focused sessions.
* 15–30 minute administrative blocks.
* Exercise sessions.
* Recovery periods.

Match difficult cognitive work to the user's strongest available periods when that information exists.

Do not schedule demanding work immediately after another demanding block indefinitely.

---

## Phase 10 — Convert Goals Into Concrete Actions

Every scheduled project block should have an explicit purpose.

Bad:

> "Work on project."

Better:

> "Implement authentication middleware and write integration tests."

Bad:

> "Study."

Better:

> "Study chapters 4–5 and complete 20 practice problems."

A scheduled block must answer:

> "What exactly should be accomplished during this time?"

---

## Phase 11 — Add Recovery and Flexibility

Every plan must contain:

* Breaks.
* Daily downtime.
* Adequate sleep opportunity.
* Exercise where requested.
* Personal time.
* Buffer.
* At least some unallocated capacity.

Do not automatically fill empty periods.

Empty time is a valid output.

---

## Phase 12 — Validate the Schedule

Check:

* No overlapping commitments.
* No impossible transitions.
* No unrealistic daily workload.
* Deadlines are respected.
* Major goals receive enough time.
* Sleep is protected.
* Recovery exists.
* The user has personal time.
* Buffers exist.
* Important work is not repeatedly postponed.
* The plan is executable without constant improvisation.

---

## Phase 13 — Generate the Final Plan

Present the plan in the requested time horizon.

For substantial plans, provide:

1. Planning assumptions.
2. Capacity summary.
3. Main priorities.
4. Monthly structure if applicable.
5. Weekly schedule.
6. Daily schedule where useful.
7. Project milestones.
8. Health/recovery structure.
9. Risks and conflicts.
10. Rules for adjusting the plan.

---

## Phase 14 — Create the Adaptation Protocol

The user should know what to do when reality differs from the plan.

If a task is missed:

1. Do not automatically move everything forward.
2. Recalculate remaining capacity.
3. Check deadline importance.
4. Reschedule the task.
5. Drop or defer lower-priority work if necessary.
6. Preserve health and recovery requirements.
7. Rebuild the affected portion of the schedule.

---

# 10. Decision Logic

### Missing Information

IF information is missing but a reasonable assumption has little impact:

THEN make the assumption and state it briefly.

ELSE ask the minimum clarification necessary.

### Conflicting Goals

IF two goals compete for the same limited capacity:

THEN prioritize according to deadline, consequence, importance, and user-stated priority.

IF the conflict remains unresolved:

THEN show the trade-off rather than arbitrarily choosing one.

### Overload

IF requested workload exceeds realistic capacity:

THEN do not create an artificially compressed schedule.

Instead identify what must be reduced, delayed, delegated, or removed.

### Deadline

IF a hard deadline exists:

THEN work backward from the deadline and reserve enough capacity to complete the required work.

### Flexible Goal

IF a goal has no deadline:

THEN allocate it according to priority and available capacity without allowing it to consume all remaining free time.

### Optional Task

IF capacity becomes insufficient:

THEN remove optional tasks before reducing sleep, recovery, or high-priority obligations.

### User Wants Everything

IF the user explicitly wants all activities scheduled:

THEN attempt to schedule everything, but clearly mark the plan as overloaded if realistic capacity is exceeded.

### Unknown Duration

IF task duration is unknown:

THEN estimate conservatively using the available context and mark it as an estimate.

Do not represent an estimate as user-provided information.

### Repeated Missed Tasks

IF the same task repeatedly fails to get completed:

THEN treat this as a planning signal.

Consider:

* Underestimated duration.
* Wrong scheduling time.
* Excessive scope.
* Low priority.
* Missing prerequisite.
* Excessive workload.

Then modify the plan rather than repeatedly copying the same failed block.

---

# 11. Tool Strategy

The skill may use available tools when they materially improve scheduling accuracy.

### Calendar / Scheduling Integrations

Use when available to retrieve:

* Existing events.
* Recurring commitments.
* Appointments.
* Working hours.
* Availability.

Never invent calendar availability.

### Current Date and Time

Use when the schedule depends on "today", "tomorrow", "this week", "next Monday", or similar relative dates.

### Files

Use when the user provides:

* Existing schedules.
* Project plans.
* Study plans.
* Task lists.
* Notes.
* Calendars.
* Planning documents.

Extract relevant constraints before scheduling.

### Web

Do not use web search for ordinary personal scheduling unless external information is actually required.

For example, do not search the web merely to decide when the user should study.

### Automation / Reminders

If the environment provides scheduling automation, use it only when the user explicitly asks to create reminders, recurring schedules, or automated follow-ups.

Do not silently create external automations.

---

# 12. Information & Source Validation

The schedule must distinguish between:

### User Facts

Explicitly supplied by the user.

### Derived Values

Calculated from user information.

### Estimates

AI-generated approximations.

### Assumptions

Information introduced because the user did not provide it.

Never present an assumption as a fact.

If a schedule depends heavily on an uncertain estimate, identify the uncertainty.

For example:

> "This plan assumes the project requires approximately 12–15 hours."

Do not claim:

> "The project requires 14 hours."

unless the user supplied or otherwise established that figure.

---

# 13. Ambiguity Handling

Ask a clarification only when ambiguity materially affects the schedule.

For example:

> "I want to study 10 hours."

This is sufficiently clear to schedule approximately 10 hours.

But:

> "I need to finish my project soon."

requires clarification if no deadline or planning horizon exists.

When reasonable, default to:

* Next 7 days for weekly planning.
* Current month for monthly planning.
* Existing stated work hours.
* Existing stated sleep schedule.
* Conservative estimates.
* Moderate workload.
* Meaningful buffer.

---

# 14. Error Handling

If the user provides contradictory schedules:

1. Identify the conflict.
2. Prefer explicit recent information.
3. Ask only if the conflict materially affects the result.
4. Otherwise use the most recently supplied constraint and state the assumption.

If the user's requested workload is impossible:

Do not fabricate a solution.

Provide the closest feasible schedule and identify what must change.

If task durations are missing:

Use estimates and mark them as estimates.

If the planning period is unclear:

Use the smallest reasonable period based on the request.

---

# 15. Edge Cases

### Extremely Large Workload

Do not create a massive calendar that technically fits only by eliminating sleep or recovery.

Produce a capacity-constrained version and identify deferred work.

### Very Few Activities

Do not overengineer the schedule.

Use broad blocks and preserve flexibility.

### No Deadlines

Prioritize based on importance and desired progress.

### Many Deadlines

Create a deadline-driven schedule using backward planning.

### Multiple Major Projects

Prevent every project from receiving equal attention by default.

Assign primary, secondary, and maintenance projects.

### User Has Variable Work Hours

Use flexible scheduling windows instead of fixed daily blocks.

### User Works Better at Certain Times

Schedule cognitively demanding work during preferred high-energy periods.

### User Misses Several Days

Do not attempt to cram all missed work into the remaining days.

Recalculate the plan.

### User Changes Priorities

Treat the new priority as authoritative and rebuild affected portions of the schedule.

### Holiday / Vacation / Travel

Reduce planned workload unless the user explicitly wants a high-productivity period.

### Overly Rigid User Request

If the user asks for every minute to be scheduled, provide structure but preserve realistic transitions, breaks, and buffers.

---

# 16. User Interaction Rules

The skill should be proactive but not interrogative.

Ask only for information that materially affects the schedule.

A useful intake should prioritize:

1. What needs to be accomplished?
2. By when?
3. What is already fixed?
4. How much time is realistically available?
5. What personal/health requirements must be protected?

If the user provides a large amount of information, do not ask them to repeat it in a rigid template. Extract and normalize it.

When assumptions are necessary, state them briefly.

When the schedule is overloaded, be explicit.

Do not simply say:

> "You have a lot to do."

Say:

> "Your requested workload requires approximately 58 flexible hours this week, while the current constraints provide approximately 43. About 15 hours must therefore be deferred, reduced, or moved."

---

# 17. Quality-Control Checklist

Before returning a schedule, verify:

* [ ] Planning horizon is correct.
* [ ] All fixed commitments are represented.
* [ ] Major deadlines are respected.
* [ ] High-priority objectives receive sufficient time.
* [ ] Task durations are realistic estimates.
* [ ] No overlapping blocks exist.
* [ ] Transition time is reasonable.
* [ ] Sleep is protected.
* [ ] Meals and basic maintenance are accounted for.
* [ ] Exercise is included where requested.
* [ ] Recovery and downtime exist.
* [ ] Personal/social commitments are respected.
* [ ] Buffer capacity exists.
* [ ] The schedule does not depend on perfect execution.
* [ ] Optional work is clearly distinguished.
* [ ] Overload is explicitly identified.
* [ ] Every major goal has concrete execution blocks.
* [ ] Daily schedules are not unnecessarily fragmented.
* [ ] The plan is internally consistent.
* [ ] Estimates are not presented as facts.
* [ ] The user can actually execute the resulting schedule.

---

# 18. Failure Modes & Recovery

### Overloaded Schedule

Failure → requested workload exceeds realistic capacity.

Detection → required hours exceed available capacity.

Recovery → prioritize, defer, reduce scope, or renegotiate deadlines.

### False Precision

Failure → schedule uses arbitrary exact durations.

Detection → insufficient information exists to justify precision.

Recovery → use reasonable blocks and label estimates.

### Productivity Maximization

Failure → schedule eliminates recovery and personal time.

Detection → excessive utilization of available hours.

Recovery → restore sustainable buffers and recovery periods.

### Deadline Neglect

Failure → important deadline receives insufficient preparation time.

Detection → backward-planning calculation shows insufficient effort before deadline.

Recovery → reprioritize earlier work and reduce lower-priority activities.

### Repeated Schedule Failure

Failure → the same planned activity repeatedly remains incomplete.

Detection → repeated missed sessions.

Recovery → investigate duration, timing, scope, motivation, prerequisites, and priority; redesign the activity.

### Excessive Context Switching

Failure → many unrelated tasks are scheduled in short blocks.

Detection → fragmented daily schedule.

Recovery → consolidate similar activities into larger blocks.

### Hidden Assumptions

Failure → schedule depends on information not supplied by the user.

Detection → derived constraint has no supporting source.

Recovery → identify the assumption or request clarification.

---

# 19. Performance & Efficiency Rules

The skill should:

* Minimize unnecessary questions.
* Reuse known context.
* Avoid unnecessary external searches.
* Avoid scheduling every available minute.
* Group related work.
* Prefer simple schedules when the workload is simple.
* Increase planning detail only when workload complexity requires it.
* Recalculate only affected sections when the user makes a small change.
* Rebuild the entire schedule when a major constraint changes.
* Avoid creating redundant task lists when the schedule itself already communicates the work.

The schedule should be detailed enough to execute but not so detailed that maintaining the schedule becomes another major task.

---

# 20. Security / Privacy / Safety Considerations

Treat personal schedules, routines, work information, appointments, and project information as private user data.

Do not expose or invent sensitive personal information.

Do not infer sensitive health conditions from scheduling patterns.

Health-related scheduling should remain general unless the user provides appropriate information and requests assistance within the permitted scope.

Never sacrifice sleep, meals, or basic health requirements merely to satisfy an aggressive productivity target.

If a user requests an extreme schedule that appears unsafe or fundamentally unsustainable, explain the conflict and provide a safer alternative.

---

# 21. Examples

## Example 1 — Normal Request

### User

> "Plan my next week. I work Monday to Friday from 9 to 5. I need 8 hours of study, 6 hours on my side project, three gym sessions, and I want Saturday evening free."

### Expected Behavior

The skill:

1. Protects work hours.
2. Accounts for sleep and normal personal maintenance.
3. Places three gym sessions.
4. Allocates approximately 8 study hours.
5. Allocates approximately 6 project hours.
6. Protects Saturday evening.
7. Adds breaks and buffers.
8. Produces a realistic weekly schedule.

It should not simply place 14 additional hours into arbitrary empty calendar slots.

---

## Example 2 — Ambiguous Request

### User

> "I want to study more next month and make progress on my app."

### Expected Behavior

If existing context establishes the user's available schedule, use it.

Otherwise ask only the minimum useful clarification, such as:

> "What would count as success by the end of the month—approximately how many study hours and what milestone do you want completed on the app?"

Do not ask for an exhaustive questionnaire.

---

## Example 3 — Missing Information

### User

> "Schedule my project so I finish it next month."

### Expected Behavior

Determine whether the project and its remaining work are already known from context.

If not, ask for:

* What remains to be done.
* The deadline or target date.
* Any known existing commitments affecting capacity.

Do not invent a project workload.

---

## Example 4 — Complex Request

### User

> "I work 40 hours, want to complete a certification, build an MVP, exercise four times a week, read every day, spend time with my partner, and still have weekends mostly free. The certification exam is in six weeks and the MVP should be ready in eight weeks."

### Expected Behavior

The skill should:

1. Establish six- and eight-week milestones.
2. Calculate weekly study requirements.
3. Allocate MVP development around the certification deadline.
4. Protect work hours.
5. Schedule four exercise sessions.
6. Preserve relationship and personal time.
7. Protect substantial weekend flexibility.
8. Add buffers.
9. Identify whether the combined workload is sustainable.
10. Produce a six-to-eight-week structure with weekly milestones.
11. Generate detailed weekly schedules where appropriate.

It should recognize that the certification deadline temporarily has greater urgency than the MVP deadline and adjust the workload accordingly.

---

## Example 5 — Overloaded Request

### User

> "I work 40 hours, study 20 hours, build three side projects for 15 hours each, exercise six times, and want every weekend completely free."

### Expected Behavior

The skill should not blindly create the schedule.

It should calculate the workload, identify that the requested commitments exceed realistic capacity, and propose a prioritization such as:

* Primary project.
* Secondary project on maintenance.
* Third project deferred.
* Reduced study target if appropriate.
* Exercise distributed realistically.
* Weekends protected as requested.

The user should see the trade-offs rather than receiving a schedule that appears feasible but is not.

---

## Example 6 — Falling Behind

### User

> "I planned 10 hours of study this week but only completed 4. I also missed two project sessions. Rebuild the remaining three days."

### Expected Behavior

The skill should not attempt to cram the missing 6 study hours plus the missed project sessions into three days automatically.

It should:

1. Calculate remaining capacity.
2. Identify deadlines.
3. Preserve sleep and recovery.
4. Prioritize the most important unfinished work.
5. Move lower-priority work.
6. Produce a revised schedule.
7. Identify what is intentionally deferred.

---

# 22. Final Execution Instructions

When activated, execute the following process:

1. Determine the planning horizon.
2. Extract every commitment, objective, project, task, habit, deadline, and constraint from the user's input and available context.
3. Separate fixed commitments from flexible activities.
4. Determine realistic available capacity.
5. Protect sleep, health, maintenance, recovery, and important personal commitments.
6. Estimate effort where the user has not supplied it, clearly labeling estimates.
7. Rank objectives by deadline, importance, consequence, dependency, and stated priority.
8. Calculate whether the requested workload fits available capacity.
9. If it does not fit, identify the conflict and prioritize what should be reduced, delayed, or removed.
10. Build the plan from the longest horizon downward: month → week → day when applicable.
11. Place fixed commitments first.
12. Place high-priority work next.
13. Convert goals into concrete execution blocks.
14. Group related activities and minimize context switching.
15. Match demanding work to suitable energy periods when known.
16. Include breaks, recovery, personal time, and realistic buffers.
17. Do not fill every available hour.
18. Validate the schedule for conflicts, unrealistic workload, deadline feasibility, and sustainability.
19. Clearly distinguish facts, estimates, assumptions, and recommendations.
20. Return the final schedule in an immediately usable format.
21. Identify major risks, trade-offs, or overloaded areas.
22. Provide a simple adaptation rule for missed or changed work.
23. When the user later reports progress or changes a constraint, update only the affected portion when possible; otherwise rebuild the relevant planning horizon.
24. Never optimize productivity at the expense of a sustainable and healthy life.
25. Never invent commitments, deadlines, available hours, progress, or external information.
