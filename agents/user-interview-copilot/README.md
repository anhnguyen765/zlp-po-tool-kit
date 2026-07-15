# User Interview Copilot

User Interview Copilot is a ChatGPT agent for Product Owners who need to prepare, run, and synthesise quality-first user interviews.

## Who It Helps

Use this agent when interviewing:

- End users
- Internal operators
- Customer support teams
- Merchants
- Partners
- Other product stakeholders

## What The Agent Does

The agent supports three interview phases:

1. Pre-interview preparation: clarify interview context, research objective, interviewee type, assumptions, interview mode, and produce a structured question list.
2. During-interview support: suggest neutral follow-up questions from direct voice input where available, or from pasted transcript chunks and notes.
3. Post-interview synthesis: turn transcript evidence into key insights, pain points, evidence/quotes, jobs-to-be-done, opportunities, PO suggestions, and open questions.

## How To Use

Start with one of these requests:

- "Help me prepare a user interview for [persona/context]."
- "I am conducting an interview now. Suggest follow-up questions from this transcript."
- "Clean this rough interview transcript into a working script."
- "Synthesize this interview transcript into a Confluence-ready report."

## Inputs To Provide

For the best result, provide:

- Product or workflow area
- Interviewee type and persona/context
- Research objective or PO decision the interview should inform
- Interview mode: discovery, validation, usability, merchant/partner adoption, operational workflow, or mixed
- Known assumptions or hypotheses
- Interview timebox
- Transcript, voice-derived notes, or raw interview notes for synthesis

## Outputs

The agent produces Markdown that can be pasted into Confluence:

- Interview preparation plan
- Research questions
- Interview question list
- Live follow-up suggestions
- Clean working transcript/script
- Interview synthesis report
- Jobs-to-be-done
- Opportunities and suggested PO next steps

## Quality Principles

- Ask neutral, non-leading questions.
- Probe concrete behaviour, examples, trade-offs, workarounds, and pain.
- Separate evidence from inference.
- Do not fabricate quotes or transcript evidence.
- Avoid overclaiming from one interview.
- Tailor the interview to the interviewee type and research mode.

## Agent Files

- `instructions.md`: agent behaviour and workflow instructions.
- `templates/pre-interview-plan.md`: preparation output format.
- `templates/interview-synthesis.md`: synthesis output format.
