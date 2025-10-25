# Risk Register Template

Track and manage project risks throughout the project lifecycle.

---

## Project
[Project Name]

## Risk Owner
[Project Manager Name]

## Review Frequency
Weekly (or as specified)

---

## Risk Register

| ID | Description | Category | Impact | Likelihood | Severity | Owner | Mitigation Plan | Contingency Plan | Status | Last Updated |
|----|-------------|----------|--------|------------|----------|-------|-----------------|------------------|--------|--------------|
| R-001 | [Risk description] | [Technical/Resource/Dependency/Timeline/Quality/Stakeholder/External] | H/M/L | H/M/L | [1-9] | [Name] | [Proactive actions to reduce risk] | [What to do if risk materializes] | Open/Monitoring/Closed/Materialized | [Date] |
| R-002 | API vendor may deprecate endpoint we rely on | Dependency | High | Medium | 6 | @tech-lead | Monitor vendor announcements; build abstraction layer | Implement fallback to alternative API within 2 sprints | Monitoring | 2025-10-25 |
| R-003 | Key developer may be unavailable for 2 weeks | Resource | Medium | Medium | 4 | @pm | Cross-train team on critical components; document architecture | Shift timeline by 1 week if needed; hire contractor | Open | 2025-10-25 |

---

## Risk Severity Matrix

Calculate severity as: **Impact × Likelihood**

| Impact / Likelihood | High (3) | Medium (2) | Low (1) |
|---------------------|----------|------------|---------|
| **High (3)** | 9 - Critical | 6 - High | 3 - Medium |
| **Medium (2)** | 6 - High | 4 - Medium | 2 - Low |
| **Low (1)** | 3 - Medium | 2 - Low | 1 - Low |

### Impact Definitions
- **High (3)**: Project fails or is significantly delayed (>2 weeks), major budget overrun, or critical quality issue
- **Medium (2)**: Some delay (1-2 weeks) or quality impact, manageable cost increase
- **Low (1)**: Minor inconvenience, easily managed with existing resources

### Likelihood Definitions
- **High (3)**: Very likely to occur (>60% probability)
- **Medium (2)**: Possible (30-60% probability)
- **Low (1)**: Unlikely but possible (<30% probability)

---

## Risk Categories

**Technical**: Architecture decisions, technology choices, technical debt, complexity  
**Resource**: Team availability, skill gaps, hiring delays, competing priorities  
**Dependencies**: External team dependencies, third-party integrations, vendor reliability  
**Timeline**: Aggressive deadlines, scope creep, estimation accuracy  
**Quality**: Testing coverage, performance requirements, security vulnerabilities  
**Stakeholder**: Changing requirements, unclear priorities, communication gaps  
**External**: Market changes, regulatory updates, competitive pressure  

---

## Risk Status Definitions

- **Open**: Newly identified, mitigation plan in development or execution
- **Monitoring**: Mitigation actions in place, actively watching for triggers
- **Materialized**: Risk has occurred and is now an issue requiring active management
- **Closed**: No longer relevant or successfully mitigated

---

## Action Items from Risk Review

Track specific actions to mitigate risks:

| Date | Action | Owner | Due Date | Related Risk IDs | Status |
|------|--------|-------|----------|------------------|--------|
| 2025-10-25 | Create abstraction layer for vendor API | @dev-lead | 2025-11-15 | R-002 | In Progress |
| 2025-10-25 | Document authentication module | @dev-1 | 2025-11-01 | R-003 | Not Started |

---

## Escalation Triggers

Escalate risks immediately when:
- Severity increases to 6 or higher
- Risk materializes (status changes to "Materialized")
- Mitigation actions are blocked or ineffective
- Timeline impact exceeds 2 days on critical path
- Budget impact exceeds 10% of project budget
- Multiple related risks create compound effect

**Escalation Path**: Team → PM → Product Lead → Sponsor

---

## Risk Review Meeting Notes

### [Date]
**Attendees**: [Names]

**New Risks Identified**:
- [ID]: [Brief description]

**Updated Risks**:
- [ID]: [What changed and why]

**Closed Risks**:
- [ID]: [Why closed]

**Action Items**:
- [Action with owner and due date]

**Next Review**: [Date]

---

## Top Risks (Severity ≥ 6)

*This section auto-populates from risks with severity 6 or higher*

1. **R-002** (Severity 6): API vendor deprecation - *Monitoring*
2. [Next highest severity risk]

---

**Document Owner**: [PM Name]  
**Last Updated**: [Date]  
**Next Review**: [Date]

---

## Instructions for Use

1. **Add new risks** as they're identified (don't wait for scheduled review)
2. **Review weekly** in PM sync meeting
3. **Update status** and reassess impact/likelihood as conditions change
4. **Close risks** when no longer relevant - don't let the list grow stale
5. **Escalate** per the triggers above - don't wait if something is urgent
6. **Track effectiveness** - note if mitigation plans are working

This is a living document - keep it current!
