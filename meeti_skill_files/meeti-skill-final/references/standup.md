# Standup Meeting Notes

## Key Focus Areas

Standups are brief team syncs focused on coordination and unblocking. Prioritize:
- Progress updates (what's done)
- Current focus (what's in progress)
- Blockers and dependencies
- Team coordination moments

## Team Health Assessment (Required)

Assess overall team health based on standup dynamics:

| Status | Criteria |
|--------|----------|
| 🟢 **Green** | Team is on track, updates are clear, blockers are manageable |
| 🟡 **Yellow** | Some friction—unclear priorities, accumulating blockers, or coordination gaps |
| 🔴 **Red** | Unproductive meeting—disorganized, unclear updates, major blockers, or team misalignment |

**Always include a 1-2 sentence justification** for the assigned status.

## Additional Sections for Standups

After the standard output structure, add:

### Team Health: [🟢/🟡/🔴] [Status]
[1-2 sentence justification]

### Blockers & Dependencies
| Blocker | Owner | Dependency/Waiting On |
|---------|-------|----------------------|
| [Issue] | [Name] | [Who/what is blocking] |

### Collaboration Moments
Note instances where team members helped unblock each other or offered assistance.

### Disruptions
Document unexpected obstacles, scope changes, or external interruptions affecting the team.

### Parking Lot
Items raised but deferred for separate discussion:
- [Topic] — suggested owner or forum
- [Topic] — suggested owner or forum

**Always include a Parking Lot section**, even if empty ("No items parked").

## Example Output Snippet

```
### Team Health: 🟡 Yellow
Two engineers blocked on API access; standup ran 5 minutes over due to scope creep discussion.

### Blockers & Dependencies
| Blocker | Owner | Dependency/Waiting On |
|---------|-------|----------------------|
| Can't test payment flow | Maria | Staging API credentials from DevOps |
| PR review delayed | James | Waiting on Sarah (OOO until Thursday) |

### Collaboration Moments
- Chen offered to pair with Maria on payment flow testing using mock data
- Team agreed to redistribute Sarah's review load

### Disruptions
- PM announced scope addition for compliance feature mid-standup
- CI pipeline failures causing 20-min delays on all PRs

### Parking Lot
- Compliance feature scoping — follow-up with PM async
- CI reliability — bring to platform team sync
```

## Common Standup Improvement Tips

- Keep to 15 minutes max; use a timer
- Save detailed discussions for parking lot
- Focus on blockers, not status reports
- Stand up (literally) to keep energy high
- Rotate facilitator to maintain engagement
