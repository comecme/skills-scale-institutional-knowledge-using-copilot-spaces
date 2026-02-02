# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared
- Cross-functional sign-offs:
  - Technical Writer: release notes and documentation updated
  - Security Champion: security review completed (if applicable)
  - DevOps Engineer: deployment pipeline ready and tested
  - Customer Support Lead: support team briefed and ready
  - UX Designer: design implementation validated (if applicable)

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support
- [ ] DevOps Engineer: monitors deployment metrics and system health
- [ ] Customer Support Lead: notified and has access to updated documentation
- [ ] Technical Writer: confirms all documentation is live and accurate
- [ ] Security Champion: validates security controls are functioning (if security-related changes)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items
  - Involve cross-functional team:
    - DevOps Engineer: executes rollback and system recovery
    - Customer Support Lead: communicates with affected users
    - Security Champion: assesses security implications (if applicable)
    - Technical Writer: updates status pages and incident communications

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
