# User Interview Copilot

Workspace Agent package for a Product Owner interview assistant.

## Purpose

User Interview Copilot helps POs run quality-first user interviews across end users, internal operators, customer support teams, merchants, partners, and other stakeholders.

It supports three phases:

1. Pre-interview preparation: clarify context, research objective, assumptions, interview mode, and produce a question list.
2. During-interview support: use voice input where the runtime supports it, or transcript chunks otherwise, to suggest neutral follow-up questions.
3. Post-interview synthesis: summarise transcript evidence into key insights, pain points, quotes/evidence, jobs-to-be-done, opportunities, PO suggestions, and open questions.

## Files

- `agent.json`: versioned agent metadata and starter prompts.
- `instructions.md`: full agent instructions for Workspace Agents.
- `templates/pre-interview-plan.md`: Confluence-ready preparation output format.
- `templates/interview-synthesis.md`: Confluence-ready synthesis output format.

## Live Agent

- Draft agent name: `User Interview Copilot`
- Draft agent ID: `agt_6a574ef5ac1881919534aabf83c5fc61`
- Status: draft created, not published from Codex

## Voice Behaviour

The agent is written as voice-first, but this repo package does not configure a dedicated voice channel. It relies on the ChatGPT/Workspace Agent runtime to provide direct voice input. When voice is unavailable, the agent should accept pasted transcript chunks or notes.

## Publish Checklist

Before publishing:

1. Review `instructions.md` for the expected interview quality bar.
2. Confirm the starter prompts in `agent.json` match the desired PO workflow.
3. Test one pre-interview preparation prompt.
4. Test one live transcript chunk and confirm the agent suggests one concise follow-up.
5. Test one post-interview transcript and confirm the synthesis separates evidence from inference.

