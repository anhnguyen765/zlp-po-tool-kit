---
name: onboard-personal-memory
description: Step-by-step onboarding workflow for interviewing a person and turning the answers into portable personalised memory for AI agents such as Codex, Claude, ChatGPT, Antigravity, or other assistants. Use when a user wants to create, refresh, audit, or migrate AI memory/profile context covering role, goals, communication preferences, decision style, technical preferences, tool stacks, collaboration norms, privacy boundaries, and agent-specific memory formats.
---

# Onboard Personal Memory

## Overview

Use this skill to run a structured onboarding interview and produce concise, portable personalised memory that an AI agent can safely use across tools. Optimise for durable collaboration context, not biography.

## Core Principles

- Separate durable preferences from temporary facts.
- Ask progressively; do not interrogate the user with a long questionnaire at once.
- Capture how the user wants agents to think and collaborate, not only what the user does.
- Distinguish facts, preferences, assumptions, and unknowns.
- Avoid sensitive data unless the user explicitly wants it included.
- Produce memory that is tool-portable first, then adapt format for a specific agent when requested.

## Workflow

### 1. Establish Scope

Ask where the memory will be used and how detailed it should be. If the user is unsure, default to a portable Markdown profile that can be pasted into any AI agent.

Clarify only the essentials:

- Target agents or tools: Codex, Claude, ChatGPT, Antigravity, Cursor, Gemini, custom agent, or all.
- Output location or format: Markdown, plain text, YAML, JSON, AGENTS.md-style instructions, Claude project instructions, ChatGPT custom instructions, or another format.
- Privacy level: minimal, practical, or rich.

### 2. Interview in Rounds

Ask 3 focused questions per round by default; use up to 5 only when the user explicitly wants a faster, richer onboarding pass. Summarise after each round and ask the user to correct anything important before continuing.

Use these rounds:

1. Role and context: work, responsibilities, domains, current projects, and audiences.
2. Goals and outcomes: what the user wants agents to help improve, avoid, or optimise for.
3. Collaboration style: directness, challenge level, explanation depth, planning preferences, autonomy, status updates.
4. Thinking and decision preferences: frameworks, trade-offs, risk posture, evidence standards, blind spots to watch.
5. Writing and communication: tone, structure, language, audience, terminology to prefer or avoid.
6. Technical profile when relevant: preferred languages, frameworks, cloud providers, package managers, architecture style, testing expectations, security/reliability priorities, and tools.
7. Privacy and boundaries: what not to remember, what to ask before using, and what must never be inferred.

If the user is technical, include the technical round by default. If not, ask whether tools, workflows, or domain systems matter.

### 3. Synthesize Memory

Read `references/memory-template.md` when drafting the final output.

Write memory as concise instructions an agent can follow. Prefer stable statements such as "Prefer concise, structured updates" over overfit claims such as "The user liked a table in one conversation."

Include these labels where useful:

- `Durable`: likely stable for months.
- `Contextual`: useful for current work but may change.
- `Ask first`: sensitive, high-risk, or situation-dependent.
- `Do not store`: explicitly excluded.

### 4. Validate with the User

Before finalising, present the draft and ask:

- What is inaccurate?
- What is too personal or should be removed?
- What is missing that would materially improve AI collaboration?
- What should be shorter for everyday agent memory?

### 5. Adapt to Agent Format

When the user names a target agent, adapt the portable memory:

- Codex or AGENTS.md: use directive language, engineering defaults, validation expectations, and repo/workspace instructions.
- Claude project instructions: use collaboration style, context boundaries, and writing preferences.
- ChatGPT custom instructions: split into "What should ChatGPT know?" and "How should ChatGPT respond?"
- Antigravity or coding agents: emphasise autonomy level, preferred stack, code review style, testing expectations, and safety boundaries.
- Custom system prompt: write concise behavioural instructions with stable memory separated from task-specific context.

## Question Bank

Use these questions selectively.

Role:
- What role should an AI assume you are in when helping you?
- What domains, products, systems, or audiences do you work with most?
- What context do agents usually miss about your work?

Outcomes:
- What do you want AI agents to help you do better?
- What does good assistance look like for you?
- What should agents avoid optimising for?

Collaboration:
- Should agents act autonomously, ask before acting, or propose plans first?
- How direct should feedback be?
- When should an agent challenge your reasoning?

Decision-making:
- What trade-offs do you care about most?
- What evidence should change a recommendation?
- What blind spots should an agent watch for?

Technical:
- What languages, frameworks, databases, cloud providers, package managers, and tools do you prefer?
- What engineering defaults should agents follow?
- What should agents verify before saying work is done?

Privacy:
- What should never be stored in memory?
- What can be used during a task but should not become durable memory?
- What should agents ask before inferring?

## Output Quality Bar

The final memory should be:

- specific enough to change agent behaviour
- short enough to fit into common memory or instruction fields
- written as instructions, not a profile article
- free of secrets and unnecessary private details
- separated into durable memory, technical preferences, collaboration style, and boundaries
- portable across tools unless the user requests a specific format
