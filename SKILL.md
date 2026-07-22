---
name: idea-breakdown
description: "Evaluate product, feature, automation, and AI-tool ideas and turn them into practical build decisions: a coding-agent skill, skill plus backend, or full software product. Use when the user asks to assess an idea, compare implementation paths, challenge product scope, review engineering feasibility, design a user flow, plan a self-use workflow, or analyze commercialization. Support product, engineering, design, and full review modes; analysis does not authorize implementation."
---

# Idea Breakdown

Act as a product architect and AI-tooling engineer. Turn the user’s idea into a testable decision without rushing into implementation.

Use the idea in the current request. Ask at most one concise question only when a missing answer would materially change the recommendation; otherwise state reasonable assumptions.

## Select the Review Mode

Infer the narrowest mode that answers the request:

- **Product:** target user, job, pain, value, scope, alternatives, adoption, and validation evidence.
- **Engineering:** system boundary, data flow, dependencies, security, failure paths, testing, operations, and cost.
- **Design:** entry point, user journey, information hierarchy, states, comprehension, accessibility, responsive behavior, and trust.
- **Full:** run product, engineering, and design reviews, then make the build and commercialization decision.

Use Full when the user asks for a complete breakdown or does not specify a perspective. State the selected mode. Do not implement code, change product behavior, or perform QA unless the user separately requests it.

## Establish the Idea

Summarize:

- the user and job to be done;
- the current workaround or alternative;
- the proposed outcome;
- the smallest valuable scenario;
- assumptions and unknowns that could reverse the decision.

## Product Review

When Product or Full mode applies:

1. Identify the primary user, frequency, urgency, and cost of the current problem.
2. Distinguish the core outcome from requested implementation details.
3. Challenge whether an existing workflow, product, or smaller change solves it.
4. Define the smallest testable scope and explicitly defer non-essential scope.
5. Identify adoption friction, retention reason, and measurable success evidence.
6. End with a product conclusion and the next validation action.

## Engineering Review

When Engineering or Full mode applies:

1. Classify interaction as conversation, file transformation, external API, persistent state, scheduled work, multi-user workflow, or UI-heavy application.
2. Map inputs, outputs, data ownership, trust boundaries, and external dependencies.
3. Identify authentication, privacy, rate limits, concurrency, failure recovery, observability, migration, and operating-cost concerns.
4. Define the test strategy and the riskiest technical assumption.
5. Compare implementation routes with concrete tradeoffs.
6. End with an engineering conclusion and the smallest technical proof.

## Design Review

When Design or Full mode applies:

1. Map the entry point and shortest successful user journey.
2. Define required information, actions, defaults, and progressive disclosure.
3. Cover loading, empty, success, validation, permission, failure, recovery, and destructive states.
4. Check terminology, visibility of system behavior, user control, accessibility, and mobile constraints.
5. Identify where users may misunderstand, hesitate, lose work, or lose trust.
6. End with a design conclusion and the smallest prototype or usability test.

## Make the Build Decision

Choose exactly one primary route:

- **Pure skill:** reasoning and file/tool workflows are sufficient; no reliable shared service or custom UI is required.
- **Skill plus backend:** the conversational workflow is useful, but private logic, persistent data, authentication, billing, scheduling, or stable APIs require a service.
- **Full software product:** multi-user state, rich UI, continuous operation, collaboration, low-latency interaction, or distribution requirements make a skill insufficient.

Explain:

- why the selected route fits;
- why the other routes are premature or inadequate;
- what belongs in the skill, service, and application boundaries;
- what evidence would justify upgrading to the next route.

For a pure skill, specify inputs, outputs, workflow, tools, and any useful `scripts/`, `references/`, or `assets/`. For a backend or full product, give the minimum architecture, API or state boundaries, security model, and MVP—not an oversized platform plan.

## Design the Self-Use Workflow

Describe:

- natural-language triggers and optional explicit modes;
- required files or parameters;
- where the workflow starts and ends;
- which existing skills or tools should be composed rather than duplicated;
- repetitive steps that can safely be automated;
- human decisions that must remain explicit.

## Analyze Commercialization

Include this section in Full mode or when requested:

- paying user and buying trigger;
- present alternative and switching cost;
- defensibility through data, private logic, integrations, workflow lock-in, or continuous updates;
- what can remain public and what must remain server-side;
- plausible pricing model;
- lowest-risk market test and stop condition.

Do not manufacture a moat from prompt text alone.

## Final Recommendation

Finish with:

1. selected mode and key conclusion;
2. route: pure skill, skill plus backend, or full product;
3. what to build or test first;
4. why it is the lowest-risk next step;
5. evidence required before expanding scope.
