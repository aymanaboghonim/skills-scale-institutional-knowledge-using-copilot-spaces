# Stakeholder Communication Plan Template

Define how you'll communicate with different stakeholder groups throughout the project.

---

## Project
[Project Name]

## Communication Owner
[Project Manager Name]

---

## Stakeholder Map

### Core Team
Directly involved in day-to-day execution.

| Name | Role | Communication Needs | Frequency | Channel | Artifacts |
|------|------|---------------------|-----------|---------|-----------|
| [Name] | Project Manager | Status, blockers, decisions | Daily | Slack, Standup | Status updates |
| [Name] | Product Manager | Priorities, scope, metrics | Daily/Weekly | Slack, Meetings | Roadmap, metrics |
| [Name] | Tech Lead | Architecture, blockers | Daily | Slack, Standup | Design docs |
| [Name] | Developer(s) | Tasks, reviews, blockers | Daily | Slack, Standup, PRs | Code, PRs |
| [Name] | QA/Testing | Test plans, bugs, sign-off | Daily/Weekly | Slack, Meetings | Test reports |

### Extended Team
Peripherally involved, need awareness.

| Name/Group | Role | Communication Needs | Frequency | Channel | Artifacts |
|------------|------|---------------------|-----------|---------|-----------|
| [Name/Team] | Design | UI/UX decisions, reviews | Weekly | Meetings | Design specs |
| [Name/Team] | Marketing | Launch dates, features | Bi-weekly | Email, Meetings | Release notes |
| [Name/Team] | Support | Feature training, docs | Pre-launch | Meetings | User docs |
| [Name/Team] | Sales | Launch timing, capabilities | Monthly | Email | Feature briefs |
| [Name/Team] | Legal/Compliance | Compliance needs | As needed | Email, Meetings | Compliance docs |

### Leadership
Strategic oversight and approvals.

| Name | Role | Communication Needs | Frequency | Channel | Artifacts |
|------|------|---------------------|-----------|---------|-----------|
| [Name] | Sponsor | Status, risks, decisions | Weekly | Email, Meetings | Executive summary |
| [Name] | VP Engineering | Resource needs, blockers | Bi-weekly | Meetings | Status reports |
| [Name] | VP Product | Strategic direction | Monthly | Meetings | Roadmap updates |

### External
Customers, partners, vendors.

| Name/Group | Role | Communication Needs | Frequency | Channel | Artifacts |
|------------|------|---------------------|-----------|---------|-----------|
| [Customer Group] | Beta Users | Feature previews, feedback | Bi-weekly | Email, Surveys | Beta releases |
| [Partner] | Integration Partner | API changes, timeline | Monthly | Email, Meetings | API docs |

---

## Communication Cadence

### Daily
- **What**: Team standup (15 min)
- **Who**: Core delivery team
- **Format**: What I did, what I'm doing, blockers
- **Channel**: Video call / Slack

### Weekly
- **What**: PM + Product sync
- **Who**: PM, Product Manager, Tech Lead
- **Format**: Progress review, risk assessment, decision-making
- **Channel**: Video call
- **Artifacts**: Updated risk register, decision log

- **What**: Stakeholder status update
- **Who**: PM to extended team and leadership
- **Format**: Written status using standard template
- **Channel**: Email, shared doc
- **Artifacts**: Status report

### Bi-weekly
- **What**: Sprint demo / milestone review
- **Who**: Core team + extended team stakeholders
- **Format**: Demo of completed work, Q&A
- **Channel**: Video call
- **Artifacts**: Demo recording, release notes draft

### Monthly
- **What**: Leadership review
- **Who**: PM, Product Manager, Sponsor, VPs
- **Format**: Strategic update, metrics review, ask for resources/decisions
- **Channel**: Video call
- **Artifacts**: Executive summary, metrics dashboard

### Ad-hoc
- **What**: Critical issues, blockers, decisions
- **Who**: Relevant stakeholders based on issue
- **Format**: Immediate notification with impact and ask
- **Channel**: Slack (urgent), Email (important)
- **Artifacts**: Incident report, escalation document

---

## Communication Standards

### Status Updates
- Use the [weekly status template](weekly-status-update.md)
- Always include: progress, next steps, risks, decisions needed
- Send by EOD Friday (or agreed day)
- Highlight changes in status (🟢 → 🟡 → 🔴)

### Escalations
- Follow the [escalation guidelines](../octoacme-risks-and-communication.md#escalation-paths)
- Be clear about impact and urgency
- Provide options and recommendations
- State decision deadline

### Single Source of Truth
Project status is maintained in: [Specify location]
- GitHub Projects board for work tracking
- Wiki/Confluence for documentation
- Slack channel #project-name for discussions

---

## Stakeholder Preferences

Document individual communication preferences:

| Stakeholder | Prefers | Avoid | Best Time to Reach |
|-------------|---------|-------|-------------------|
| [Name] | Slack, brief updates | Long emails | Mornings (9-11am) |
| [Name] | Scheduled meetings | Surprise pings | Afternoons |
| [Name] | Detailed written docs | Verbal only | Anytime async |

---

## Special Scenarios

### Launch Communication
- **T-2 weeks**: Alert support, marketing, sales with feature details
- **T-1 week**: Confirm go/no-go with stakeholders
- **Launch day**: Announce to all stakeholders, monitor for issues
- **T+1 week**: Share adoption metrics and feedback

### Incident Communication
- Use [incident communication template](incident-communication.md)
- Notify immediately: core team, on-call, affected stakeholders
- Regular updates every [X hours] until resolved
- Post-incident: blameless retro summary to all stakeholders

### Scope Changes
- PM proposes change with impact analysis
- Product Manager approves/rejects
- If approved, PM updates timeline and notifies all stakeholders
- Log decision in decision log

---

**Document Owner**: [PM Name]  
**Last Updated**: [Date]  
**Review Frequency**: Monthly or when stakeholders change
