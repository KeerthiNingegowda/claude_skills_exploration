---
name: meeti
description: Formats and summarizes meeting transcripts into clear, concise, actionable notes. Use when processing meeting transcripts, notes, or recordings for any meeting type including 1:1s, standups, team discussions, knowledge transfer sessions, or general meetings. Transforms raw transcripts into structured summaries with action items, decisions, and follow-ups.
---

# Meeti

Transform meeting transcripts into actionable, type-aware summaries.

## Workflow

1. **Extract metadata**: Meeting title, attendees, duration
2. **Identify meeting type**: Match to one of the four types below
3. **Load type-specific guidance**: Read the appropriate reference file
4. **Process transcript**: Apply core principles + type-specific rules
5. **Output structured notes**: Use the format from the reference file

## Meeting Type Detection

Analyze the transcript content and title to determine type:

| Type | Indicators |
|------|------------|
| **1:1** | Two participants, career/feedback discussion, manager-report dynamic |
| **Standup** | Multiple brief updates, blockers mentioned, daily/recurring cadence |
| **Knowledge Transfer** | One person explaining systems/processes, onboarding context, heavy Q&A |
| **Team Discussion** | Multiple participants, specific topic focus (feature, incident, brainstorm) |

Load the matching reference file:
- `references/one-on-one.md` — 1:1 meetings
- `references/standup.md` — Daily standups
- `references/knowledge-transfer.md` — KT sessions
- `references/team-discussion.md` — All other team meetings

## Core Principles (Apply to All Types)

### Always Capture
- **Meeting title** (infer from content if not provided)
- **Attendees** (list all participants mentioned)
- **Duration** (if available, otherwise omit)
- **Meeting goal** (deduce from title + discussion content)

### Summarization Rules
- Keep summaries short—users will read the transcript if they want full details
- Remove filler words, broken phrasing, tangents
- Write in clear, direct language
- Use bullet points sparingly; prefer concise prose

### Vague But Important Statements
If a statement seems significant but lacks specifics, include it in a **Notable Mentions** section rather than discarding it.

Example:
> "We should probably think about that thing Sarah mentioned last week..."

→ Add to Notable Mentions: "Reference to previous discussion with Sarah—topic unclear, may need follow-up"

### Action Items (Required)
Always document action items in this format:

| Action | Owner | Due Date |
|--------|-------|----------|
| [Task description] | [Name] | [Date or TBD] |

**Rules:**
- Never omit an action item because details are missing
- Use "TBD" for unknown owners or dates
- Include implicit commitments ("I'll send that over" → action item)

### Risks, Concerns, and Open Questions
Always capture in dedicated sections:
- **Concerns Raised**: Worries, objections, hesitations expressed
- **Risks Identified**: Potential problems, dependencies, blockers
- **Open Questions**: Unresolved questions needing answers

### Meeting Improvement Tips
When applicable, end with 1-2 concrete suggestions for running better meetings of this type. Only include if genuinely useful—skip for well-run meetings.

## Output Structure

Use this base structure, then add type-specific sections from reference files:

```
# [Meeting Title]

**Attendees:** [Names]
**Duration:** [Time] (if known)
**Meeting Type:** [Type]
**Goal:** [Inferred goal]

## Summary
[2-4 sentences capturing the essence]

## Key Discussion Points
[Organized by topic, not chronologically]

## Decisions Made
[Bulleted list of decisions]

## Action Items
| Action | Owner | Due Date |
|--------|-------|----------|
| ... | ... | ... |

## Concerns & Risks
[If any were raised]

## Open Questions
[If any remain unresolved]

## Notable Mentions
[Vague but potentially important items]

[Type-specific sections from reference file]

## Meeting Improvement Tips
[Optional, only if warranted]
```
