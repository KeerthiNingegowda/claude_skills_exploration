# Knowledge Transfer Session Notes

## Key Focus Areas

KT sessions transfer institutional knowledge from experts to learners. Prioritize:
- Who led the session and their expertise area
- Technical systems and their history
- Product context and business logic
- Organizational knowledge (people, processes)
- Practical tips and pitfalls

## Additional Sections for KT Sessions

After the standard output structure, add:

### Session Leader
**[Name]** — [Role/Expertise area]

### Knowledge Summary

Organize transferred knowledge into these categories:

#### Technical History
- System architecture evolution
- Key technical decisions and their rationale
- Legacy constraints or technical debt

#### Product Background
- Feature origins and business drivers
- User needs the system addresses
- Product roadmap context

#### People & Organization
- Key stakeholders and their interests
- Team ownership boundaries
- Escalation paths and decision makers

#### Tips, Pitfalls & Troubleshooting
- Common mistakes to avoid
- Non-obvious gotchas
- Debugging techniques
- Workarounds for known issues

### Resource Checklist

Collect all resources shared during the session:

| Type | Resource | Location/Link |
|------|----------|---------------|
| 📁 Repo | [Name] | [URL] |
| 📄 Doc | [Name] | [URL] |
| 🔗 Link | [Name] | [URL] |
| 📊 Dashboard | [Name] | [URL] |
| 💬 Slack | [Channel/Thread] | [URL] |
| 📹 Recording | [Name] | [URL] |
| Other | [Description] | [URL] |

**Always include this table**, even if no resources were shared ("No resources shared during session").

## Example Output Snippet

```
### Session Leader
**Marcus Chen** — Senior Backend Engineer, Auth Team (3 years)

### Knowledge Summary

#### Technical History
The auth service was originally a monolith feature, extracted in 2022. JWT implementation was chosen over sessions for mobile app compatibility. The "legacy_auth" table still exists for migration edge cases.

#### Product Background
SSO was added in Q3 2023 for enterprise customers. The current flow supports SAML and OIDC but not LDAP—this is a known gap for government contracts.

#### People & Organization
- Security reviews: route through @security-team Slack
- Token policy changes: need sign-off from Legal (compliance@)
- Auth oncall: rotates weekly, check #auth-oncall

#### Tips, Pitfalls & Troubleshooting
- **Pitfall**: Token refresh race condition on slow networks—always implement retry with jitter
- **Gotcha**: Staging and prod use different JWT secrets; don't copy tokens between envs
- **Debug tip**: Enable verbose logging with `AUTH_DEBUG=1` flag; logs go to Datadog

### Resource Checklist

| Type | Resource | Location/Link |
|------|----------|---------------|
| 📁 Repo | auth-service | github.com/company/auth-service |
| 📄 Doc | Auth Architecture | confluence.com/auth-arch |
| 📄 Doc | SSO Integration Guide | confluence.com/sso-guide |
| 📊 Dashboard | Auth Metrics | datadog.com/dash/auth |
| 💬 Slack | #auth-questions | slack.com/auth-questions |
```

## Common KT Session Improvement Tips

- Record the session for future team members
- Prepare a structured agenda covering all categories
- Leave time for hands-on walkthrough, not just slides
- Create a follow-up doc with post-session Q&A
- Schedule a 30-day check-in to address gaps
