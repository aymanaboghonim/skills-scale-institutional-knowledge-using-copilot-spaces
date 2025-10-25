# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register

### Risk Register Template
Maintain risks in a shared document or project tracking tool:

| ID | Description | Impact | Likelihood | Severity | Owner | Mitigation Plan | Status | Last Updated |
|----|-------------|--------|------------|----------|-------|-----------------|--------|--------------|
| R-001 | [Risk description] | High/Med/Low | High/Med/Low | [Score 1-9] | [Name] | [Action plan] | Open/Monitoring/Closed | [Date] |

### Risk Severity Scoring
Calculate severity as: Impact × Likelihood

| Impact/Likelihood | High (3) | Medium (2) | Low (1) |
|-------------------|----------|------------|---------|
| **High (3)** | 9 - Critical | 6 - High | 3 - Medium |
| **Medium (2)** | 6 - High | 4 - Medium | 2 - Low |
| **Low (1)** | 3 - Medium | 2 - Low | 1 - Low |

### Risk Categories
Common project risk categories to consider:
- **Technical**: Architecture decisions, technology choices, technical debt
- **Resource**: Team availability, skill gaps, hiring delays
- **Dependencies**: External team dependencies, third-party integrations, vendor reliability
- **Timeline**: Aggressive deadlines, scope creep, estimation accuracy
- **Quality**: Testing coverage, performance requirements, security vulnerabilities
- **Stakeholder**: Changing requirements, unclear priorities, communication gaps
- **External**: Market changes, regulatory updates, competitive pressure

## Risk Lifecycle

### 1. Identify
When to identify risks:
- During project planning and kickoff
- At the start of each sprint/iteration
- During weekly team syncs
- When new information emerges
- After retrospectives and post-mortems

How to identify:
- Pre-mortem exercise: "What could go wrong?"
- Review dependencies and external factors
- Analyze assumptions and constraints
- Learn from similar past projects

### 2. Assess
For each risk, evaluate:
- **Impact**: What happens if this risk materializes?
  - High: Project fails or is significantly delayed (>2 weeks)
  - Medium: Some delay or quality impact (1-2 weeks)
  - Low: Minor inconvenience, easily managed
  
- **Likelihood**: How probable is this risk?
  - High: Very likely to occur (>60% chance)
  - Medium: Possible (30-60% chance)
  - Low: Unlikely but possible (<30% chance)

### 3. Mitigate
Risk response strategies:
- **Avoid**: Change plans to eliminate the risk
- **Reduce**: Take actions to decrease impact or likelihood
- **Transfer**: Shift responsibility (insurance, outsourcing)
- **Accept**: Acknowledge and monitor, prepare contingency plan

For high-severity risks (score ≥6):
- Assign a dedicated owner
- Define specific mitigation actions with deadlines
- Establish monitoring triggers
- Prepare contingency plans

### 4. Monitor
- Review risk register weekly in PM sync
- Update status and reassess as conditions change
- Close risks when no longer relevant
- Add new risks as they emerge
- Track effectiveness of mitigation actions

### Risk Status Values
- **Open**: Newly identified, mitigation plan in progress
- **Monitoring**: Mitigation in place, actively watching
- **Materialized**: Risk has occurred, now an issue
- **Closed**: No longer relevant or successfully mitigated

## Stakeholder Communication

### Identifying Stakeholders
Create a stakeholder map at project initiation:
- **Core Team**: PM, Product Manager, Tech Lead, Developers, QA
- **Extended Team**: Design, Marketing, Sales, Support, Legal
- **Leadership**: Sponsors, VPs, C-level executives
- **External**: Customers, Partners, Vendors

For each stakeholder group, define:
- Communication frequency (daily, weekly, milestone-based, on-demand)
- Preferred channels (email, Slack, meetings, dashboards)
- Information needs (strategic updates vs. detailed status)
- Decision-making authority

### Communication Cadence
- **Daily standups**: Core delivery team (15 min)
- **Weekly status**: PM to stakeholders and leadership
- **Bi-weekly demos**: Showcase progress to extended team
- **Monthly reviews**: Strategic updates for leadership
- **Ad-hoc**: Critical issues, blockers, and decisions

### Single Source of Truth
Maintain project status in one primary location:
- Project README with current status section
- GitHub Projects board for work tracking
- Shared wiki or documentation site for decisions and context
- Release notes document for deployment communications

## Communication Templates

### Weekly Status Update Template
```
**Project**: [Project Name]
**Period**: [Date Range]
**Status**: 🟢 On Track | 🟡 At Risk | 🔴 Blocked

**Progress This Week**:
- [Key accomplishment 1]
- [Key accomplishment 2]
- [Metrics: X features completed, Y PRs merged]

**Next Steps**:
- [Planned work for next week]
- [Upcoming milestones]

**Risks & Blockers**:
- [Risk/blocker with severity and mitigation]

**Decisions Needed**:
- [Decision 1 - owner, deadline]

**Asks**:
- [Support needed from stakeholders]
```

### Stakeholder Communication Plan Template
```
| Stakeholder | Role | Communication Frequency | Channel | Content Type |
|-------------|------|------------------------|---------|--------------|
| [Name] | [Role] | [Daily/Weekly/Monthly] | [Email/Slack/Meeting] | [Status/Decisions/Metrics] |
```

### Milestone Update Template
```
**Milestone**: [Milestone Name]
**Status**: [Completed / In Progress / Delayed]
**Completion Date**: [Actual or Projected]

**Key Deliverables**:
- [Deliverable 1]: ✅ Complete
- [Deliverable 2]: 🔄 In Progress
- [Deliverable 3]: ⏳ Not Started

**Highlights**:
- [Notable achievements]

**Challenges**:
- [Issues encountered and resolutions]

**Impact on Timeline**:
- [Any adjustments to downstream milestones]
```

### Incident Communication Template
```
**INCIDENT ALERT**
**Severity**: [P0/P1/P2] - [Critical/High/Medium]
**Status**: [Investigating / Mitigating / Resolved]
**Impact**: [User-facing impact description]

**What Happened**:
- [Brief description of the incident]

**Current Actions**:
- [Steps being taken to resolve]
- [Incident commander: Name]

**Timeline**:
- [Detected at: Time]
- [Expected resolution: Time]

**Next Update**: [Time for next communication]

**Post-Incident**:
- Blameless retrospective scheduled: [Date/Time]
- Root cause analysis: [Due date]
```

## Escalation Paths

### Risk and Blocker Escalation
Use this decision tree to determine appropriate escalation:

**Level 1 - Team Level** (Resolve within 1 day)
- Daily standup or immediate team discussion
- Tech lead or senior developer can resolve
- Examples: Code review delays, minor technical blockers

**Level 2 - PM/Product Lead** (Resolve within 2-3 days)
- Escalate when team cannot resolve independently
- Requires cross-team coordination or resource reallocation
- PM triages and coordinates with Product Lead and dependent teams
- Examples: Dependency blockers, scope clarification needed, resource constraints

**Level 3 - Sponsor/Leadership** (Resolve within 1 week)
- Business-impacting issues requiring executive decisions
- Budget, timeline, or scope trade-offs needed
- PM presents options and recommendations to sponsor
- Examples: Major timeline slippage, significant scope changes, budget overruns

### Escalation Triggers
Escalate immediately when:
- **Timeline Impact**: >2 days delay to critical path milestone
- **Budget Impact**: Unplanned costs exceeding 10% of project budget
- **Quality Impact**: Security vulnerabilities or critical bugs blocking release
- **Resource Impact**: Key team member unavailable for >3 days
- **Stakeholder Impact**: Customer-facing commitments at risk
- **Risk Materialization**: High-impact risk becomes an issue

### Security and Compliance Escalation
- **Security incidents**: Follow security incident runbook, notify Security on-call immediately
- **Compliance issues**: Notify Legal and Compliance teams within 24 hours
- **Data breaches**: Escalate to CISO and Legal immediately, regardless of severity

---

## See Also

- [Project Initiation](octoacme-project-initiation.md) - For creating the initial stakeholder communication plan
- [Execution & Tracking](octoacme-execution-and-tracking.md) - For decision log and metrics tracking
- [Retrospective](octoacme-retrospective-and-continuous-improvement.md) - For continuous process improvements
- [Templates](templates/) - Reusable templates for communication and risk management

### Escalation Communication Format
```
**ESCALATION REQUIRED**
**Level**: [1/2/3]
**Priority**: [High/Critical]

**Issue**:
[Clear, concise description of the problem]

**Impact**:
- Timeline: [Affected milestones]
- Budget: [Cost implications]
- Quality: [Risk to deliverables]

**Attempts at Resolution**:
- [What has been tried]
- [Why it didn't work]

**Options**:
1. [Option A with pros/cons]
2. [Option B with pros/cons]

**Recommendation**: [Preferred path forward]

**Decision Needed By**: [Date/Time]
**Owner**: [Who needs to decide]
```
