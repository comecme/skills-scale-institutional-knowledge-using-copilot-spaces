# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support, UX, security)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status
- Ensure cross-functional visibility:
  - Customer Support Lead: keeps support team informed of changes and known issues
  - Technical Writer: maintains documentation currency
  - DevOps Engineer: shares infrastructure and deployment status
  - Security Champion: communicates security posture and vulnerabilities

## Communication Templates
Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled
- Cross-functional coordination:
  - DevOps Engineer: system recovery and monitoring
  - Customer Support Lead: user communication and impact assessment
  - Security Champion: security incident evaluation (if applicable)
  - Technical Writer: incident communication and documentation updates

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security Champion and Security on-call
- For deployment/infrastructure issues, escalate to DevOps Engineer and operations team
- For customer-impacting issues, notify Customer Support Lead immediately
