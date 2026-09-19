# INSTAGRAM VIDEO SCRIPT GENERATOR

## 1. Description

This skill generates complete, production-ready scripts for Instagram videos based primarily on:

* Video type / format
* Video title or topic
* Target video length

The skill adapts the script to the conventions of Instagram content, including hook strength, pacing, retention, spoken language, visual changes, on-screen text, calls to action, and duration.

The output must be usable directly by a creator, editor, presenter, or video-generation workflow without requiring the user to reconstruct the script.

---

## 2. Purpose

The purpose of this skill is to transform a simple Instagram content idea into a structured video script optimized for the specified format and duration.

The skill should determine:

1. What the video is trying to communicate.
2. How the topic should be presented for the selected Instagram format.
3. How much information can realistically fit within the requested duration.
4. How the script should be paced.
5. Where visual changes, text overlays, B-roll, demonstrations, or other production elements should occur.
6. How the video should open, develop, and conclude.
7. Whether and where a CTA should be included.

The objective is **not merely to write a paragraph of narration**. It is to produce a practical script that defines what is said and, where useful, what the viewer should see.

---

## 3. Scope

### Supported content

The skill can generate scripts for formats including:

* Instagram Reels
* Talking-head videos
* Educational videos
* Tutorials
* How-to videos
* Explainers
* Storytelling
* Listicles
* Tips / hacks
* Product demonstrations
* Product-focused content
* Personal-brand content
* Motivational content
* Entertainment-oriented videos
* Myth vs. fact
* Before/after
* Problem/solution
* Reaction/commentary
* FAQ videos
* Promotional videos
* UGC-style videos
* Voice-over videos
* B-roll-driven videos
* Faceless videos

### Out of scope

The skill should not automatically:

* Create a complete filming plan unrelated to the script.
* Invent factual claims merely to make a script more interesting.
* Assume a specific brand voice when none is provided.
* Guarantee virality, views, engagement, or algorithmic performance.
* Treat every Instagram video as having the same structure.
* Overload a short video with information that cannot realistically be delivered within its duration.

---

## 4. Trigger Conditions

Activate this skill when the user requests a script for an Instagram video and provides, or implies, information such as:

> "Create a Reel about..."

> "Write a 30-second Instagram video about..."

> "Script for a talking-head Reel."

> "Give me a script for this title."

> "Create a 60-second Instagram video."

> "Turn this idea into a Reel script."

The skill should also activate when the user provides a title plus a video format and asks for the script.

---

## 5. Non-Trigger Conditions

Do not use this skill as the primary workflow when the user only requests:

* Instagram caption writing.
* Hashtag generation.
* Thumbnail/title ideas without a script.
* A general content strategy.
* A content calendar.
* A video editing tutorial.
* A blog post with no video adaptation requested.
* A YouTube long-form script unless the user explicitly wants the Instagram adaptation.

If the user requests multiple deliverables, the script-generation portion should use this skill while other requested outputs may be handled separately.

---

# 6. Inputs

## Required

### 6.1 Video Type

**Type:** String

**Purpose:** Determines the appropriate structure, tone, pacing, and visual treatment.

Examples:

* Reel
* Talking head
* Tutorial
* Educational
* Storytelling
* Product demo
* Listicle
* Voice-over
* Faceless

If the user simply says "Instagram video" or "Reel", classify the format based on the available context.

---

### 6.2 Title / Topic

**Type:** String

**Purpose:** Defines the subject and central idea of the video.

Example:

> "3 mistakes people make when starting a business"

The title should be treated as the starting point rather than automatically copied verbatim into the script.

---

### 6.3 Video Length

**Type:** Duration

Examples:

* 15 seconds
* 30 seconds
* 45 seconds
* 60 seconds
* 90 seconds

The duration is a hard production constraint.

The script must be realistic for the requested duration.

---

## Optional

### 6.4 Target Audience

Examples:

* Beginners
* Entrepreneurs
* Fitness enthusiasts
* Creators
* Students

If omitted, infer a reasonable audience from the topic.

---

### 6.5 Tone

Examples:

* Educational
* Casual
* Funny
* Energetic
* Serious
* Conversational
* Inspirational
* Direct
* Premium
* Provocative

If omitted, use a natural conversational Instagram style appropriate to the topic.

---

### 6.6 Goal

Examples:

* Educate
* Entertain
* Generate comments
* Drive saves
* Generate shares
* Build authority
* Promote a product
* Generate leads
* Increase awareness

If omitted, prioritize clarity, retention, and a natural conclusion.

---

### 6.7 CTA

Optional explicit CTA such as:

> "Follow for more."

> "Comment 'GUIDE' and I'll send it to you."

> "Save this for later."

If omitted, generate a contextually appropriate CTA only when one adds value.

---

### 6.8 Brand / Creator Voice

Optional information describing:

* Personality
* Vocabulary
* Brand positioning
* Humor
* Formality
* Pronunciation preferences
* Words to avoid

---

### 6.9 Supporting Information

The user may provide:

* Facts
* Research
* Product information
* URLs
* Existing copy
* Previous scripts
* Brand guidelines
* Transcripts
* References

These should be treated as source material when supplied.

---

## Contextual Inputs

The skill may use:

* Previous conversation context.
* Previously established brand voice.
* Previously established target audience.
* Previously established content goals.
* Existing information about the topic provided in the conversation.

Do not repeatedly ask for information that has already been established.

---

## Automatically Derived Inputs

The skill should infer when possible:

* Appropriate hook structure.
* Appropriate narrative structure.
* Approximate speaking pace.
* Amount of information that fits the duration.
* Appropriate CTA.
* Need for B-roll.
* Need for on-screen text.
* Number of visual changes.
* Level of explanation appropriate to the duration.
* Whether the script should use first-person, second-person, or neutral narration.

---

# 7. Outputs

The default output must contain:

## A. Script Overview

* Video type
* Title
* Target duration
* Approximate spoken-word count
* Tone
* Primary objective

## B. Full Script

The script should be divided into logical sections, normally:

1. Hook
2. Setup / context
3. Main content
4. Payoff / conclusion
5. CTA

Not every video requires all five sections.

## C. Production Directions

Where useful, include:

* Visual
* Camera direction
* B-roll
* On-screen text
* Scene changes
* Gestures
* Props
* Emphasis

## D. Timing

Each major section should have an approximate timestamp.

Example:

| Time      | Section | Spoken Content | Visual / Direction |
| --------- | ------- | -------------- | ------------------ |
| 0:00–0:03 | Hook    | ...            | ...                |
| 0:03–0:10 | Setup   | ...            | ...                |
| 0:10–0:25 | Main    | ...            | ...                |
| 0:25–0:30 | CTA     | ...            | ...                |

For very short videos, timestamps may be grouped into larger sections rather than assigned to every sentence.

---

# 8. Core Principles

## 8.1 Hook immediately

The opening should establish a reason to continue watching.

Avoid unnecessary introductions such as:

> "Hey guys, welcome back to another video."

Unless the requested style specifically requires it.

---

## 8.2 Respect the duration

The script must fit the requested runtime.

Use a reasonable spoken-word estimate rather than blindly maximizing word count.

Default planning range:

* Very short videos: concise delivery with minimal exposition.
* Medium videos: approximately 125–160 spoken words per minute depending on style.
* Fast-paced formats may use higher density.
* Educational or deliberate delivery should use lower density.

The skill must prioritize natural delivery over artificially precise word counts.

---

## 8.3 One central idea

A short Instagram video should normally communicate one primary idea.

If the title contains multiple concepts, consolidate them or structure them into a list.

---

## 8.4 Spoken language must sound natural

Write for speech rather than for reading.

Prefer:

> "Here's the problem."

over:

> "The fundamental issue associated with this phenomenon is..."

Use short sentences, natural transitions, and conversational phrasing unless the requested style is intentionally formal.

---

## 8.5 Visual rhythm

For Instagram video, the script should account for visual change.

Avoid writing a long uninterrupted monologue when the format would benefit from:

* B-roll
* Text overlays
* Demonstrations
* Camera changes
* Examples
* Screen recordings
* Props

---

## 8.6 Information density must match duration

The shorter the video, the more aggressively the script should prioritize.

If the topic cannot reasonably be explained within the requested duration:

1. Identify the central takeaway.
2. Remove secondary information.
3. Compress examples.
4. Avoid unnecessary context.
5. If essential information still cannot fit, restructure the video into a series or explicitly state that the topic needs more time.

---

## 8.7 CTA should be proportional

Do not let the CTA consume a disproportionate amount of a short video.

A 15-second video should generally have an extremely concise CTA.

---

# 9. Execution Workflow

## Phase 1 — Parse the Request

### Objective

Extract all available parameters.

### Actions

Identify:

* Video type
* Title/topic
* Duration
* Audience
* Tone
* Goal
* CTA
* Brand voice
* Supporting information

### Decision

If required information is present, continue.

If the video type is ambiguous but the intended format can reasonably be inferred, infer it.

If duration is missing, ask for it only if it materially affects the requested output. Otherwise use an appropriate default and state the assumption.

---

## Phase 2 — Classify the Video

Determine the dominant content structure.

Examples:

### Educational

Hook → problem/question → explanation → example → takeaway → CTA

### Tutorial

Hook → promise → step 1 → step 2 → step 3 → result → CTA

### Listicle

Hook → introduce list → item 1 → item 2 → item 3 → conclusion

### Storytelling

Hook → context → tension/problem → development → payoff → CTA

### Product Demo

Problem → product introduction → demonstration → benefit → proof/result → CTA

### Talking Head

Hook → core statement → supporting points → takeaway → CTA

### Voice-over / Faceless

Hook → narration → visual progression → payoff → CTA

The structure should be adapted rather than mechanically applied.

---

## Phase 3 — Define the Core Message

Create internally:

### One-sentence premise

What is the video actually trying to tell the viewer?

### Viewer takeaway

What should the viewer know, understand, feel, or do after watching?

### Supporting points

Identify only the points necessary to communicate the core message.

Eliminate information that does not support the main idea.

---

## Phase 4 — Design the Hook

Generate a hook appropriate to the video type.

Possible hook mechanisms:

* Strong claim
* Unexpected fact
* Question
* Problem
* Contrarian observation
* Curiosity gap
* Before/after
* Promise
* Mistake
* Demonstration
* Story opening

The hook must connect directly to the actual content.

Do not use clickbait that the video cannot fulfill.

---

## Phase 5 — Allocate Time

Before writing the final script, divide the available duration.

Example for a 30-second educational Reel:

* Hook: 0–3s
* Setup: 3–7s
* Main content: 7–23s
* Payoff: 23–27s
* CTA: 27–30s

These are defaults, not rigid requirements.

The allocation should change according to content type.

---

## Phase 6 — Draft the Script

Write the spoken script according to:

* Duration
* Format
* Tone
* Audience
* Core message
* Structure

Every sentence should serve at least one purpose:

* Capture attention
* Establish context
* Deliver information
* Provide evidence/example
* Create progression
* Deliver payoff
* Transition
* CTA

Remove sentences that serve none of these purposes.

---

## Phase 7 — Add Visual Direction

For each meaningful section determine whether the viewer should see:

* Presenter
* Product
* Screen
* B-roll
* Graphic
* Text overlay
* Demonstration
* Image
* Environmental shot
* Before/after
* Close-up
* Wide shot

Visual directions should support the spoken content rather than unnecessarily complicate production.

---

## Phase 8 — Add On-Screen Text

Identify important phrases that could appear as text.

Rules:

* Keep text concise.
* Prioritize keywords.
* Do not duplicate every spoken word.
* Highlight numbers, claims, steps, names, or key takeaways.
* Make text understandable even when viewed quickly.

---

## Phase 9 — Perform Duration Check

Estimate the spoken duration.

If the script is too long:

1. Remove repetition.
2. Remove low-value context.
3. Compress explanations.
4. Shorten examples.
5. Simplify wording.

If still too long, restructure the content rather than simply increasing speaking speed.

If significantly too short:

1. Add a useful example.
2. Add clarification.
3. Add a stronger payoff.
4. Add relevant context.

Do not add filler merely to hit the target duration.

---

## Phase 10 — Perform Retention Check

Check:

* Does the opening create a clear reason to watch?
* Does the content deliver on the opening?
* Is there unnecessary exposition?
* Does the script progress?
* Is there a payoff?
* Are transitions clear?
* Is the ending abrupt?
* Is the CTA appropriate?

---

## Phase 11 — Perform Accuracy Check

If the script contains factual claims:

* Use supplied sources when available.
* Do not invent statistics.
* Do not fabricate studies, experts, quotes, testimonials, or results.
* Distinguish facts from opinions.
* Flag claims requiring verification when verification is unavailable.

For creative content where factual accuracy is not relevant, this stage can be minimal.

---

## Phase 12 — Final Formatting

Return the finished script in a production-friendly structure.

Default:

### VIDEO SCRIPT

**Title:**
**Format:**
**Duration:**
**Tone:**
**Goal:**

### SCRIPT

| Time | Spoken Script | Visual / Direction | On-Screen Text |
| ---- | ------------- | ------------------ | -------------- |

### CTA

Include the final CTA within the script and identify it separately when useful.

### PRODUCTION NOTES

Only include notes that materially help filming or editing.

---

# 10. Decision Logic

### Video type

**IF** the user specifies a video type
→ use it.

**ELSE IF** the request says "Reel"
→ default to a short-form Instagram Reel structure.

**ELSE**
→ infer the format from the topic and requested presentation.

---

### Duration

**IF** duration is provided
→ treat it as a hard target.

**IF** duration is not provided and a reasonable default can be chosen
→ choose a sensible short-form duration and clearly state the assumption.

**IF** duration materially affects the user's objective and cannot reasonably be inferred
→ ask for the duration.

---

### Audience

**IF** audience is provided
→ adapt language and examples.

**ELSE**
→ infer the most likely audience from the topic.

---

### Tone

**IF** tone is provided
→ follow it.

**ELSE**
→ use conversational, direct, platform-appropriate language.

---

### CTA

**IF** the user provides a CTA
→ use it.

**ELSE IF** a CTA naturally supports the goal
→ create one.

**ELSE**
→ end with the content's natural conclusion without forcing a CTA.

---

### Multiple topics

**IF** the title contains several unrelated ideas
→ identify the central idea.

**IF** multiple points naturally form a list
→ use a listicle structure.

**IF** the ideas cannot realistically fit within the duration
→ prioritize the central idea and remove secondary material.

---

### Unsupported factual claims

**IF** the user supplies a factual claim
→ do not automatically treat it as verified.

**IF** verification is available and important
→ verify it.

**IF** verification is unavailable
→ avoid strengthening the claim or present it cautiously.

---

# 11. Tool Strategy

## Web Research

Use web research when:

* The user requests factual or current information.
* The script depends on current statistics.
* The user explicitly requests research.
* The topic involves rapidly changing information.
* Important factual claims need verification.

Do not browse simply to make a creative script longer.

When researching:

1. Prefer authoritative sources.
2. Cross-check important claims.
3. Preserve source attribution where necessary.
4. Do not invent citations.

---

## Files

Use provided files when the script is based on:

* Brand guidelines
* Research documents
* Product information
* Existing scripts
* Transcripts
* Articles
* Internal documentation

Treat supplied source material as authoritative for the requested transformation unless the user asks for external verification.

---

## No Tool Needed

Do not use external tools when the user provides a purely creative topic and no external facts are required.

---

# 12. Information & Source Validation

The skill must distinguish between:

### User-provided information

Information explicitly supplied by the user.

### Verified information

Information confirmed through reliable sources.

### Creative material

Hooks, phrasing, examples, metaphors, transitions, and other generated material that does not claim to be factual.

### Assumptions

Reasonable choices made because the user omitted optional information.

Never present assumptions as user requirements.

---

# 13. Ambiguity Handling

### Low-impact ambiguity

If the ambiguity does not substantially change the script:

→ choose the most reasonable interpretation and state the assumption briefly.

### High-impact ambiguity

If different interpretations would produce substantially different scripts:

→ ask one concise clarification question.

Example:

> "Do you want this as a talking-head Reel or a voice-over/B-roll Reel?"

Avoid asking a long questionnaire.

---

# 14. Error Handling

If required information is missing:

→ identify exactly what is missing.

If the requested duration is unrealistic:

→ adapt the information density and explain the constraint.

If source material is contradictory:

→ identify the contradiction rather than silently choosing one version.

If a tool fails:

→ continue using available information when safe and appropriate, or explicitly state what could not be verified.

If the user requests a format the skill cannot meaningfully support:

→ provide the closest supported structure and explain the adaptation briefly.

---

# 15. Edge Cases

## Extremely short video

For videos around 10–15 seconds:

* One idea only.
* Very short hook.
* Minimal explanation.
* Strong visual component.
* Extremely concise ending.

Do not attempt a multi-step tutorial unless the steps can genuinely be communicated.

---

## Long Instagram video

For longer videos:

* Use more developed structure.
* Introduce sections or narrative progression.
* Add examples where useful.
* Maintain periodic information or visual changes.
* Avoid filling the duration with repetition.

---

## Technical topic

Use simpler language where appropriate.

Explain unavoidable technical terms.

Prioritize comprehension over jargon density.

---

## Sensitive subject

Use careful, factual language.

Do not exaggerate claims merely for engagement.

---

## User supplies a complete draft

Treat the supplied text as source material.

Preserve its intended meaning unless the user asks for substantial rewriting.

Adapt it to the requested duration and Instagram format.

---

## User changes the duration

Recalculate the structure and rewrite the script as necessary.

Do not merely cut the final sentences from the original script.

---

## User changes video type

Rebuild the presentation around the new format.

For example, a talking-head script converted into a faceless Reel should receive appropriate visual/B-roll directions rather than simply retaining the original presentation instructions.

---

# 16. User Interaction Rules

The skill should minimize questions.

### Proceed automatically when:

* Video type is known or obvious.
* Title/topic is known.
* Duration is known or safely inferable.
* Missing information is optional.

### Ask one clarification when:

* The missing information materially changes the script.
* Multiple formats are equally plausible.
* The duration is essential but unavailable.
* The user has supplied contradictory requirements.

### State assumptions when:

* Audience is inferred.
* Tone is inferred.
* CTA is generated.
* Video format is inferred.
* Exact speaking speed is estimated.

Do not overwhelm the user with implementation details.

---

# 17. Quality-Control Checklist

Before returning the script, verify:

### Content

* [ ] The script addresses the requested title/topic.
* [ ] There is one clear central idea.
* [ ] The information is appropriate for the video type.
* [ ] No unnecessary filler is present.

### Duration

* [ ] The script is realistic for the requested runtime.
* [ ] Spoken-word density is natural.
* [ ] The CTA fits within the duration.

### Hook

* [ ] The first seconds provide a reason to continue.
* [ ] The hook is relevant to the actual content.
* [ ] No unsupported clickbait is used.

### Structure

* [ ] The video has a logical progression.
* [ ] The main value is delivered.
* [ ] The conclusion provides a payoff.
* [ ] The ending is not unnecessarily repetitive.

### Instagram suitability

* [ ] Language is suitable for short-form video.
* [ ] Visual changes are considered.
* [ ] Important concepts can be reinforced through on-screen text.
* [ ] The script is easy to perform or edit.

### Accuracy

* [ ] No facts were fabricated.
* [ ] Statistics are not invented.
* [ ] Sources are preserved where relevant.
* [ ] Unverified claims are not presented as established facts.

### Production

* [ ] Visual directions are actionable.
* [ ] On-screen text is concise.
* [ ] The script can be handed directly to a creator/editor.

---

# 18. Failure Modes & Recovery

| Failure                   | Detection                               | Recovery                                   |
| ------------------------- | --------------------------------------- | ------------------------------------------ |
| Missing title             | No clear subject                        | Ask for the topic/title                    |
| Missing duration          | No runtime available                    | Infer if safe; otherwise ask               |
| Ambiguous video type      | Multiple plausible formats              | Ask one clarification                      |
| Script too long           | Estimated runtime exceeds target        | Compress and restructure                   |
| Script too short          | Significant unused duration             | Add useful content, not filler             |
| Too many ideas            | Multiple unrelated concepts             | Select central idea or restructure as list |
| Weak hook                 | Opening provides little reason to watch | Rewrite hook                               |
| Unsupported claim         | No reliable basis                       | Remove, qualify, or verify                 |
| Repetitive script         | Same idea repeated                      | Consolidate                                |
| Poor visual fit           | Long uninterrupted narration            | Add appropriate visual progression         |
| Forced CTA                | CTA does not fit objective              | Remove or replace with natural CTA         |
| User changes requirements | New format/duration/goal                | Recalculate and regenerate                 |

---

# 19. Performance & Efficiency Rules

1. Do not ask for optional information before producing a useful script.
2. Do not browse unless research materially improves the result.
3. Do not generate multiple hooks unless the user asks for alternatives.
4. Do not overproduce production notes for simple videos.
5. Use the simplest structure that effectively communicates the idea.
6. Reuse established audience, tone, and brand context from the conversation.
7. When the user provides a duration, optimize the entire script around it from the beginning rather than writing first and shortening afterward.
8. Prefer useful specificity over generic social-media advice.

---

# 20. Security / Privacy / Safety Considerations

The skill must:

* Avoid fabricating personal information.
* Avoid inventing testimonials or endorsements.
* Avoid presenting fictional claims as real-world facts.
* Avoid fabricating credentials, statistics, studies, or expert statements.
* Treat private user-provided information as confidential within the task.
* Follow applicable content and safety requirements.
* Clearly distinguish fictional/creative material from factual claims when relevant.

---

# 21. Examples

## Example 1 — Normal Request

### User Input

> Create a 30-second Instagram Reel, talking head, titled "3 mistakes beginners make when going to the gym."

### Expected Behavior

* Identify talking-head format.
* Identify beginner fitness audience.
* Use a fast educational/list structure.
* Allocate approximately 3 seconds to the hook, approximately 22–24 seconds to the content, and the remainder to the CTA/conclusion.
* Use three concise mistakes.
* Include simple visual/text directions.

### Expected Output Structure

**Title:** 3 Mistakes Beginners Make When Going to the Gym
**Format:** Talking Head Reel
**Duration:** 30 seconds

| Time      | Spoken Script  | Visual             | Text                    |
| --------- | -------------- | ------------------ | ----------------------- |
| 0:00–0:03 | Hook           | Presenter close-up | "3 beginner mistakes"   |
| 0:03–0:10 | Mistake 1      | Presenter/demo     | "1. Too much weight"    |
| 0:10–0:17 | Mistake 2      | Example            | "2. No consistency"     |
| 0:17–0:24 | Mistake 3      | Example            | "3. Ignoring technique" |
| 0:24–0:30 | Takeaway + CTA | Presenter          | "Save this"             |

The actual claims should be supported appropriately if presented as factual fitness advice.

---

## Example 2 — Ambiguous Request

### User Input

> Make me a Reel about artificial intelligence.

### Expected Behavior

The topic is too broad to create a focused script.

Ask a concise clarification such as:

> "What angle do you want: AI tips, AI tools, AI news, AI for business, or an educational explainer?"

Do not generate an unfocused generic script unless the user indicates they want one.

---

## Example 3 — Missing Information

### User Input

> Write an Instagram script about why people procrastinate.

### Expected Behavior

If no duration is supplied, determine whether a default short-form script is appropriate.

If proceeding, explicitly state a reasonable assumption such as:

> "I'll treat this as a 30-second educational Reel."

Then create the script.

---

## Example 4 — Complex Request

### User Input

> Create a 60-second faceless Reel titled "Why your first business idea probably isn't your best one." Target audience is aspiring entrepreneurs. Make it educational but slightly provocative. The goal is to get saves.

### Expected Behavior

1. Classify as faceless educational Reel.
2. Identify aspiring entrepreneurs as audience.
3. Use a curiosity-driven but accurate hook.
4. Build around one central argument.
5. Use B-roll appropriate for each section.
6. Use concise on-screen text.
7. Create a save-oriented CTA.
8. Ensure the entire narration fits approximately 60 seconds.
9. Avoid claiming that every first business idea is objectively bad.

---

## Example 5 — Edge Case

### User Input

> Make a 15-second Reel explaining the entire history of artificial intelligence.

### Expected Behavior

Recognize that the requested topic is too broad for meaningful treatment in 15 seconds.

Do not attempt to cram an entire history into the video.

Instead, either:

* Narrow the topic to one historical milestone, or
* Create a deliberately high-level summary that clearly presents itself as a brief overview.

If narrowing the topic requires user input, ask for one concise choice.

---

# 22. Final Execution Instructions

When this skill is triggered:

1. Parse the user's video type, title/topic, duration, audience, tone, objective, CTA, and brand context.
2. Infer optional parameters whenever doing so does not materially change the result.
3. Identify the single central message of the video.
4. Select the structure appropriate to the video type.
5. Design the opening hook before writing the rest of the script.
6. Allocate the available runtime across the hook, body, payoff, and CTA as appropriate.
7. Write natural spoken language rather than prose intended for reading.
8. Keep the information density realistic for the requested duration.
9. Add useful visual and on-screen-text directions.
10. Verify that factual claims are supported or appropriately qualified.
11. Perform a duration, retention, clarity, accuracy, and production-readiness check.
12. If the script does not fit the requested duration, restructure it rather than simply accelerating the narration or adding filler.
13. Return the final script in a clear production-ready format.
14. Minimize clarification questions; ask only when missing information materially affects the result.
15. Never fabricate facts, sources, statistics, testimonials, or tool results.
16. Preserve the user's intended message, audience, tone, and objective.
17. Optimize for a script that a creator can immediately record and an editor can immediately understand.
