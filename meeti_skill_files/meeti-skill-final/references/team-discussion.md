# Team Discussion Notes

## Key Focus Areas

Team discussions cover varied topics: feature planning, incident reviews, brainstorming, documentation, etc. Apply all core principles strictly and focus on:
- Clear articulation of the meeting's purpose
- Key decisions and their rationale
- Assigned responsibilities
- Follow-up requirements

## Discussion Subtypes

Adapt emphasis based on discussion type:

| Subtype | Additional Focus |
|---------|------------------|
| **Feature Planning** | Requirements clarity, scope boundaries, timeline |
| **Incident Review** | Root cause, timeline of events, preventive measures |
| **Brainstorming** | Ideas generated (even rough ones), evaluation criteria |
| **Documentation** | What needs documenting, ownership, deadlines |
| **Process Discussion** | Current pain points, proposed changes, rollout plan |

## Additional Sections for Team Discussions

After the standard output structure, add:

### Discussion Type
[Subtype from table above, or describe if other]

### Key Decisions & Rationale
For each decision, capture the reasoning:
- **Decision**: [What was decided]
  - **Rationale**: [Why this choice]
  - **Alternatives Considered**: [Other options discussed, if any]

### Meeting Necessity Critique

Provide a brief, honest assessment:

**Was this meeting necessary?** [Yes / Partially / No]

**Assessment**: [1-2 sentences explaining why]

Signs a meeting may have been unnecessary:
- Could have been an email/Slack thread
- No decisions were made
- Only 1-2 people spoke; others were passive
- Information was one-way broadcast
- No action items resulted
- Scope was unclear throughout

If the meeting was avoidable, suggest an alternative format.

## Example Output Snippet

```
### Discussion Type
Incident Review (Payment Processing Outage, Nov 15)

### Key Decisions & Rationale
- **Decision**: Implement circuit breaker pattern for payment gateway calls
  - **Rationale**: Cascading failures caused 45-min outage; circuit breaker would isolate failures
  - **Alternatives Considered**: Retry with exponential backoff (rejected—doesn't prevent cascade)

- **Decision**: Add payment health check to deployment pipeline
  - **Rationale**: Outage was caused by bad deploy; health check would catch earlier
  - **Alternatives Considered**: Manual smoke test (rejected—too slow, error-prone)

### Meeting Necessity Critique

**Was this meeting necessary?** Yes

**Assessment**: Incident reviews benefit from real-time discussion to build shared understanding of the timeline and collaboratively identify root causes. The decision on circuit breaker required input from both backend and infra teams present.
```

```
### Meeting Necessity Critique

**Was this meeting necessary?** No

**Assessment**: This was a status broadcast with no decisions made. The 30-minute meeting could have been a Slack post in #project-updates. Suggest async updates with a weekly digest format instead.
```

## Common Team Discussion Improvement Tips

- Start with a clear agenda and desired outcome
- Timebox discussion topics
- Assign a note-taker and decision tracker
- End with explicit action items and owners
- Default to async; meet only when synchronous discussion adds value
