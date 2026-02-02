# OctoAcme Project Management Framework

Welcome to OctoAcme's project management framework documentation. This README provides a comprehensive overview of how we run projects, from initiation to retrospective, and serves as a go-to resource for team members and stakeholders.

## Table of Contents

- [Purpose and Scope](#purpose-and-scope)
- [Core Principles](#core-principles)
- [Project Lifecycle](#project-lifecycle)
- [Personas and Roles](#personas-and-roles)
- [Communication Strategies](#communication-strategies)
- [Quality Assurance Practices](#quality-assurance-practices)
- [Key Artifacts](#key-artifacts)
- [Additional Resources](#additional-resources)

---

## Purpose and Scope

### Purpose
This framework provides a concise, shareable introduction to how OctoAcme runs projects, enabling new teammates to quickly understand our approach, roles, and key artifacts.

### Scope
Applies to all cross-functional projects that deliver product features, services, or integrations across the organization.

---

## Core Principles

Our project management approach is built on five foundational principles:

1. **Customer-first**: Prioritize customer value and usability in all decisions
2. **Iterative delivery**: Deliver small, testable increments rather than large releases
3. **Clear ownership**: Each project has a named Project Manager (PM) and Product Lead
4. **Data-informed decisions**: Measure impact and iterate based on evidence and metrics
5. **Psychological safety**: Encourage feedback, learning, and continuous improvement

---

## Project Lifecycle

OctoAcme projects follow a structured lifecycle with five key phases:

### 1. Initiation

**Goal**: Validate and authorize work, align stakeholders, and create a lightweight plan.

**Key Activities**:
- Confirm business need and measurable outcome
- Identify stakeholders and champions
- Define success criteria and initial timeline
- Decide go/no-go for planning

**Deliverables**:
- Project One-pager (Problem, Goal, Success Metrics)
- Stakeholder list and communication plan
- High-level timeline and key milestones
- Initial risk list
- Resource needs assessment

**Decision Gate**: Move to planning when success metrics are clear, stakeholders agree on priority, and team availability is confirmed.

### 2. Planning

**Goal**: Turn an approved initiative into an actionable plan and backlog for delivery.

**Key Activities**:
- Hold kickoff meeting with stakeholders and delivery team
- Create prioritized backlog with acceptance criteria
- Estimate scope (T-shirt sizing or story points)
- Define Definition of Done (DoD)
- Identify dependencies and integration points
- Create release plan and milestone map

**Deliverables**:
- Prioritized and estimated backlog
- Release timeline with milestones
- Definition of Done documentation
- Initial test plan and QA approach
- Risk register with mitigation plans

### 3. Execution & Tracking

**Goal**: Manage day-to-day execution and track progress toward project milestones.

**Team Rhythm**:
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

**Workflows**:
- Use project board with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging

**Quality & Testing**:
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

**Blocker Escalation**:
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

### 4. Release & Deployment

**Goal**: Standardize how OctoAcme releases features to production to reduce risk and improve observability.

**Release Types**:
- **Patch**: Hotfixes addressing critical production issues
- **Minor**: Incremental features and improvements
- **Major**: Significant functionality or breaking changes

**Pre-release Requirements**:
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback/mitigation plan documented
- Smoke tests prepared

**Deployment Checklist**:
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

**Rollback & Incident Response**:
If a deployment fails or causes a critical issue:
- Trigger incident response and notify on-call
- Rollback to last known-good release if necessary
- Triage root cause and capture action items

### 5. Retrospective & Continuous Improvement

**Goal**: Capture learnings and convert them into actionable improvements.

**When**: After each sprint, release, or important milestone. Also after incidents.

**Structure**:
- What went well
- What could be improved
- Action items (owner, due date)
- Follow-up on previous action items

**Best Practices**:
- Timebox: 45–75 minutes depending on team size
- Use an anonymous idea board if needed to encourage candor
- Prioritize 2–3 top action items to avoid overload
- Track action items in the project backlog with clear owners and timelines
- Review outstanding actions in the weekly PM sync

---

## Personas and Roles

### Project Manager (PM)

**Role Summary**: Coordinates delivery activities, manages schedules, risks, and communications. Enables the team to deliver on commitments efficiently.

**Responsibilities**:
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

**Goals**:
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Product Manager (PdM)

**Role Summary**: Defines what should be built to deliver customer and business value. Owns the product vision, prioritizes the backlog, and measures outcomes.

**Responsibilities**:
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

**Goals**:
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Developers

**Role Summary**: Design, build, test, and deliver software components. Collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

**Responsibilities**:
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

**Goals**:
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### QA/Testing

**Role Summary**: Validate quality and acceptance criteria to ensure features meet requirements before release.

**Responsibilities**:
- Execute manual and automated tests
- Validate acceptance criteria and user workflows
- Identify and report defects
- Collaborate on test strategy and coverage

### Stakeholders

**Role Summary**: Provide inputs, requirements, and approvals to ensure project alignment with business objectives.

**Responsibilities**:
- Define business requirements and constraints
- Review progress and provide feedback
- Approve key decisions and releases
- Champion the project within their organizations

---

## Communication Strategies

Effective communication is critical to project success. OctoAcme follows these communication patterns:

### Regular Cadences

- **Daily Standups** (15 min, twice weekly or as agreed)
  - Focus: Progress, blockers, dependencies
  - Audience: Delivery team

- **Weekly PM + PdM Sync**
  - Focus: Alignment on priorities, risks, and decisions
  - Audience: Project Manager and Product Manager

- **Weekly Delivery Sync**
  - Focus: Progress updates, flagged risks, upcoming work
  - Audience: Delivery team and key stakeholders

- **Monthly Stakeholder Updates**
  - Focus: High-level status, milestones, metrics
  - Audience: Leadership and business stakeholders

- **Sprint/Milestone Demos**
  - Focus: Showcase completed work and gather feedback
  - Audience: Team, stakeholders, and interested parties

### Communication Templates

**Weekly Status Template**:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

**Incident Communication**:
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

### Escalation Paths

- **Level 1**: Team-level triage in daily standup
- **Level 2**: PM escalates to Product Lead and dependent teams
- **Level 3**: Sponsor-level escalation for business-impacting issues
- **Security Incidents**: Follow security incident runbook and notify Security on-call

---

## Quality Assurance Practices

Quality is embedded throughout the delivery lifecycle, not just at the end:

### Automated Testing

- **Unit Tests**: Required for new logic and critical paths
- **Integration Tests**: Validate component interactions
- **End-to-End Tests**: Smoke tests for critical user flows before release
- **Security Scanning**: Automated scans run in CI pipeline
- **Linting**: Code quality checks enforced before merge

### Manual QA

- **Feature Acceptance Testing**: Validate that features meet acceptance criteria
- **Exploratory Testing**: Uncover edge cases and usability issues
- **User Acceptance Testing (UAT)**: Stakeholder validation of features

### Release Quality Gates

Pre-release requirements ensure quality:
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback/mitigation plan documented
- Smoke tests prepared and executed in staging

### Definition of Done (DoD)

Each team defines their DoD, typically including:
- Code implemented and reviewed
- Unit tests written and passing
- Integration tests passing
- Documentation updated
- Acceptance criteria validated
- No critical or high-severity bugs

### Risk Management

**Risk Register**: Maintain a simple table with:
- ID, Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

**Risk Lifecycle**:
- **Identify**: During planning and ongoing execution
- **Assess**: Estimate impact and likelihood
- **Mitigate**: Reduce via actions and contingency plans
- **Monitor**: Review at weekly syncs and update status

---

## Key Artifacts

These artifacts support project execution and provide a single source of truth:

1. **Project Charter / One-pager**: Problem statement, goals, success metrics
2. **Roadmap and Release Plan**: High-level timeline and milestones
3. **Sprint/Iteration Backlog**: Prioritized work items with acceptance criteria
4. **Acceptance Criteria & Definition of Done**: Clear requirements and completion standards
5. **Risk Register**: Identified risks, mitigations, and status
6. **Retrospective Notes**: Learnings and action items for continuous improvement
7. **Release Notes**: Summary of changes, migration steps, and known issues

### How to Use These Docs

- Keep the Project Charter updated in the project repo
- Add process-specific docs into `.copilot/` if you want Copilot Spaces to use them as context
- Use this README as an onboarding resource for new team members
- Reference specific detailed guides for each lifecycle phase

---

## Additional Resources

For detailed information about specific phases and practices, see:

- [Project Management Overview](./octoacme-project-management-overview.md)
- [Project Initiation Guide](./octoacme-project-initiation.md)
- [Project Planning](./octoacme-project-planning.md)
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)
- [Risk Management & Communication](./octoacme-risks-and-communication.md)
- [Roles and Personas](./octoacme-roles-and-personas.md)

---

**Questions or feedback?** Contact your Project Manager or Product Manager, or submit suggestions through your team's feedback channels.
