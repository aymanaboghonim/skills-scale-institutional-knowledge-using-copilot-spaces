# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows

### Development Workflow

**1. Work Item Selection**
- Pick items from "Ready" column that match current sprint goals
- Verify acceptance criteria are clear
- Confirm no blockers or dependencies
- Assign to yourself and move to "In Progress"

**2. Development**
- Create feature branch from main: `feature/issue-123-short-description`
- Write code following team conventions
- Write tests alongside code (TDD encouraged)
- Commit frequently with clear messages
- Keep changes focused on single issue

**3. Pull Request (PR)**
- Create PR when work is complete and tests pass locally
- Fill out PR template completely:
  - Link to issue/story
  - Description of changes
  - How to test
  - Screenshots for UI changes
  - Checklist: tests, docs, security considerations
- Request review from appropriate team members
- Respond to feedback constructively

**4. Code Review**
- Reviewer checks within 24 hours (team SLA)
- Focus on: correctness, tests, security, maintainability
- Approve or request changes with specific feedback
- Author addresses feedback and re-requests review

**5. Merge and Deploy**
- Squash or merge based on team convention
- Delete feature branch after merge
- Verify CI/CD pipeline success
- Monitor deployment and verify in staging
- Move issue to "Done"

### Project Board Workflow

Use GitHub Projects or similar with these columns:

**Backlog**
- All identified work, prioritized by product
- Not yet ready for development
- May lack full details or acceptance criteria

**Ready**
- Refined and estimated
- Acceptance criteria defined
- No blockers
- Can be picked up by any team member

**In Progress**
- Actively being worked on
- Limit WIP (work in progress) to prevent thrashing
- Recommended: 1-2 items per developer

**In Review**
- PR created and awaiting review
- Includes code review and QA review if needed
- PR link attached to issue

**QA** (if separate QA process)
- Deployed to test environment
- QA validating against acceptance criteria
- Bugs found are either fixed or documented

**Done**
- Meets Definition of Done
- Merged to main branch
- Deployed and verified
- Accepted by product owner

### Work in Progress (WIP) Limits

To maintain flow and reduce context switching:
- Developers: 1-2 items in progress maximum
- Team: Total WIP ≤ team size × 1.5
- If WIP limit reached, help others finish before starting new work

### PR Size Guidelines

| Size | Lines Changed | Review Time | Recommendation |
|------|---------------|-------------|----------------|
| Small | < 200 | < 30 min | ✅ Ideal |
| Medium | 200-400 | 30-60 min | ✅ Good |
| Large | 400-800 | 1-2 hours | ⚠️ Consider splitting |
| X-Large | > 800 | > 2 hours | ❌ Must split |

**Benefits of small PRs:**
- Faster reviews
- Easier to understand
- Less risk
- Quicker feedback loop
- Easier to revert if needed

### Pull Request Template

```markdown
## Description
[Brief description of changes and motivation]

## Related Issue
Closes #[issue-number]

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
- [ ] Unit tests added/updated
- [ ] Integration tests added/updated
- [ ] Manual testing completed

**How to test:**
1. [Step 1]
2. [Step 2]
3. [Expected result]

## Checklist
- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] Documentation updated
- [ ] No new warnings
- [ ] Tests pass locally
- [ ] Security considerations reviewed

## Screenshots (if applicable)
[Add screenshots for UI changes]

## Additional Notes
[Any other context, dependencies, or migration steps]
```

Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done

### Pull Request Workflow
- **Small PRs** (<= 400 lines when possible)
- Include issue link and acceptance criteria in PR description  
- Run automated tests and linting in CI before requesting review
- Require at least one approval before merging (or team-defined policy)

### Code Review Best Practices

**For Authors:**
- Provide context in PR description
- Self-review before requesting review
- Keep PRs focused on single concern
- Respond to feedback promptly
- Ask questions if feedback unclear

**For Reviewers:**
- Review within 24 hours
- Be constructive and specific
- Focus on important issues, not nitpicks
- Approve if changes are good enough (don't block on perfection)
- Use GitHub suggestions for easy fixes

**Review Focus Areas:**
1. **Correctness**: Does it solve the problem?
2. **Tests**: Are changes adequately tested?
3. **Security**: Any security implications?
4. **Performance**: Any performance concerns?
5. **Maintainability**: Is code readable and maintainable?

### CI/CD Pipeline Requirements

Before merge to main, CI must pass:
- [ ] All tests (unit, integration)
- [ ] Linting and code style checks
- [ ] Security scans (dependencies, code analysis)
- [ ] Build successful
- [ ] Code coverage threshold met (e.g., 80%)

Auto-deployment:
- Merges to `main` → auto-deploy to staging
- Merges to `release/*` → auto-deploy to production (after approvals)
- Tags → create GitHub release

## Quality & Testing

Quality is everyone's responsibility and integrated throughout development, not a separate phase at the end.

### Testing Strategy

**Unit Tests**
- Test individual functions and methods in isolation
- Aim for >80% code coverage on business logic
- Fast execution (<1 second per test)
- Run automatically in CI on every commit
- Mock external dependencies

**Integration Tests**
- Test interactions between components
- Verify database operations, API calls, service integrations
- Test happy path and common error scenarios
- Run in CI before merge to main branch

**End-to-End (E2E) Tests**
- Test critical user flows through the entire system
- Focus on high-value, high-risk paths
- Keep E2E suite small and focused (< 30 minutes runtime)
- Run before releases and on deployment branches
- Examples: user login, checkout flow, key workflows

**Smoke Tests**
- Quick validation that critical functionality works after deployment
- Run immediately after each deployment
- Alert team immediately if smoke tests fail
- Should complete in < 5 minutes

**Performance Tests**
- Load testing for expected traffic patterns
- Stress testing to find breaking points
- Identify performance regressions early
- Run on staging before major releases

**Security Scanning**
- Static code analysis (SAST) in CI
- Dependency vulnerability scanning
- Container and infrastructure scanning
- Penetration testing for major releases

### Quality Checklist (Before Release)

**Code Quality**
- [ ] All PRs reviewed and approved
- [ ] CI/CD pipeline passing (tests, linting, security scans)
- [ ] Code coverage meets team standards (typically >80%)
- [ ] No high-severity security vulnerabilities
- [ ] Technical debt documented and prioritized

**Testing**
- [ ] Unit tests passing for all new code
- [ ] Integration tests covering critical paths
- [ ] E2E tests passing for key user flows
- [ ] Performance testing completed (if applicable)
- [ ] Manual exploratory testing for UX validation
- [ ] Accessibility testing (WCAG compliance)

**Documentation**
- [ ] API documentation updated
- [ ] User-facing documentation updated
- [ ] README and setup instructions current
- [ ] Runbooks updated for operations
- [ ] Architecture diagrams reflect changes

**Release Readiness**
- [ ] Feature flags configured (if using)
- [ ] Database migrations tested
- [ ] Rollback plan documented
- [ ] Monitoring and alerts configured
- [ ] Stakeholders notified of upcoming release

### Definition of Done (DoD)

A work item is considered "Done" when:

**Development**
- Code is written and peer-reviewed
- All acceptance criteria are met
- Unit tests written and passing
- Code committed to version control
- No known defects

**Testing**
- Integration tests passing
- Manual testing completed by QA
- Performance acceptable (meets requirements)
- Security scan passed
- Edge cases considered and tested

**Documentation**
- Code is documented (comments, README)
- User documentation updated (if user-facing)
- API documentation updated (if applicable)
- Test plan documented

**Deployment**
- Merged to main/release branch
- Deployed to staging and validated
- Ready for production deployment
- Rollback plan exists

### Test Coverage Guidelines

| Component Type | Minimum Coverage | Target Coverage |
|----------------|------------------|-----------------|
| Business Logic | 80% | 90% |
| API Endpoints | 70% | 85% |
| Utilities | 90% | 95% |
| UI Components | 60% | 75% |

### Bug Severity Levels

**P0 - Critical**
- System down or unusable
- Data loss or corruption
- Security breach
- Action: Fix immediately, hotfix if in production

**P1 - High**
- Major feature broken
- Significant user impact
- Workaround exists but difficult
- Action: Fix in current sprint

**P2 - Medium**
- Feature partially broken
- Moderate user impact
- Reasonable workaround available
- Action: Fix in next sprint or two

**P3 - Low**
- Minor issue
- Low user impact
- Easy workaround
- Action: Backlog, fix when convenient

### Security Scanning in CI

Required scans before merge:
- **Dependency scanning**: Check for known vulnerabilities in libraries
- **Static analysis**: Identify potential security issues in code
- **Secret scanning**: Prevent credentials from being committed
- **License compliance**: Verify compatible open-source licenses

Tools integration:
- GitHub Advanced Security (Dependabot, CodeQL, Secret Scanning)
- SonarQube or similar for code quality
- Snyk or WhiteSource for dependency scanning
- Container scanning for Docker images

### Manual QA Process

**When manual QA is needed:**
- New user-facing features
- Complex business logic changes
- Visual/UX changes
- Cross-browser/device compatibility
- Accessibility requirements

**QA Handoff Checklist:**
- [ ] Feature description and acceptance criteria
- [ ] Test environment with feature deployed
- [ ] Test data and user accounts
- [ ] Known limitations or edge cases
- [ ] Expected vs. actual behavior documented

**QA Sign-off Criteria:**
- All acceptance criteria validated
- No P0 or P1 bugs found
- P2 bugs documented and assessed
- Test results documented
- Regression testing completed on related features

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

### Key Metrics to Track

**Delivery Metrics**
- **Velocity**: Story points or items completed per sprint
- **Cycle Time**: Time from "In Progress" to "Done"
- **Lead Time**: Time from "Backlog" to "Done"
- **Deployment Frequency**: How often code ships to production
- **Change Failure Rate**: % of deployments causing incidents

**Quality Metrics**
- **Bug Escape Rate**: Bugs found in production vs. caught in dev/QA
- **Test Coverage**: % of code covered by automated tests
- **Code Review Time**: Time from PR creation to merge
- **Defect Density**: Bugs per 1000 lines of code

**Business Metrics**
- Success metrics from Project One-pager (customer-specific)
- User engagement and adoption rates
- Performance (latency, uptime, error rates)

### Dashboards

Maintain visibility dashboards for:
- **Team Dashboard**: Current sprint progress, blockers, PR queue
- **Product Dashboard**: Feature adoption, user metrics, success criteria
- **Technical Dashboard**: System health, errors, performance, deployments
- **Stakeholder Dashboard**: High-level status, milestones, risks

## Decision Log

Track important technical and product decisions to provide context for future team members and prevent revisiting settled discussions.

### When to Log a Decision

Document decisions that:
- Impact architecture or technical direction
- Affect multiple teams or have long-term consequences
- Involve significant trade-offs
- Reverse previous decisions
- Are frequently questioned or discussed
- Involve compliance, security, or legal considerations

### Decision Log Template

```markdown
## Decision: [Short Title]

**Date**: [YYYY-MM-DD]
**Status**: [Proposed / Accepted / Deprecated / Superseded]
**Deciders**: [Names of people who made the decision]
**Consulted**: [People consulted for input]

### Context
[What is the issue we're facing? What factors are driving this decision?]

### Decision
[What did we decide to do?]

### Rationale
[Why did we choose this option? What were the key factors?]

### Alternatives Considered
1. **[Alternative 1]**
   - Pros: [Benefits]
   - Cons: [Drawbacks]
   - Why rejected: [Reason]

2. **[Alternative 2]**
   - Pros: [Benefits]
   - Cons: [Drawbacks]
   - Why rejected: [Reason]

### Consequences
**Positive:**
- [Expected benefit 1]
- [Expected benefit 2]

**Negative:**
- [Trade-off 1]
- [Trade-off 2]

**Mitigations:**
- [How we'll address negative consequences]

### Implementation Notes
[Any specific guidance for implementing this decision]

### Review Date
[Optional: Date to review if this decision is still valid]

### Related Decisions
- Links to related or superseded decisions

### References
- [Links to RFCs, research, discussions, etc.]
```

### Decision Log Examples

**Example 1: Technology Choice**
```markdown
## Decision: Use PostgreSQL for Main Database

**Date**: 2025-10-15
**Status**: Accepted
**Deciders**: @tech-lead, @architect
**Consulted**: @dev-team, @ops

### Context
Need to select a database for our new microservice that will handle 
user profiles and preferences with complex relational queries.

### Decision
Use PostgreSQL as the primary database.

### Rationale
- Strong ACID compliance for data integrity
- Excellent JSON support for flexible schema parts
- Team expertise with PostgreSQL
- Proven performance at our scale
- Open source with strong community

### Alternatives Considered
1. **MongoDB**
   - Pros: Flexible schema, good for rapid iteration
   - Cons: Less ACID guarantees, team less familiar
   - Why rejected: Need strong consistency for user data

2. **MySQL**
   - Pros: Team knows it, good performance
   - Cons: Weaker JSON support, licensing concerns for future
   - Why rejected: PostgreSQL offers more features we need

### Consequences
**Positive:**
- Better data consistency
- JSON support for flexible fields
- Rich query capabilities

**Negative:**
- Additional operational complexity
- Requires PostgreSQL expertise on-call

**Mitigations:**
- Training for team on PostgreSQL best practices
- Set up monitoring and backups from day one

### Implementation Notes
- Use version 14 or higher for performance improvements
- Enable connection pooling via PgBouncer
- Follow 12-factor app principles for configuration
```

### Managing the Decision Log

**Location**: Store in repository (e.g., `docs/decisions/` folder)

**Naming**: `YYYYMMDD-short-title.md` (e.g., `20251015-use-postgresql.md`)

**Index**: Maintain a `README.md` in decisions folder with:
- Chronological list of all decisions
- Status of each (accepted, superseded, etc.)
- Tags/categories for easy searching

**Review**: 
- Reference decisions in design reviews
- Update status when decisions change
- Link to decisions from related code/docs

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly ([use template](templates/risk-register.md))
- [ ] Weekly status updates sent to stakeholders ([use template](templates/weekly-status-update.md))
- [ ] Decision log maintained for important choices ([use template](templates/decision-log-entry.md))
