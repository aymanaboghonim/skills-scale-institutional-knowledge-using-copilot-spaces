# Pre-Release Checklist

Ensure all requirements are met before releasing to production.

---

## Project: [Project Name]
**Release Version**: [e.g., v1.2.0]  
**Target Release Date**: [Date]  
**Release Manager**: [Name]  

---

## Code Quality

- [ ] All planned features completed and merged to release branch
- [ ] All PRs reviewed and approved per team standards
- [ ] CI/CD pipeline passing (all tests, linting, security scans)
- [ ] Code coverage meets or exceeds team standards (typically >80%)
- [ ] No high-severity security vulnerabilities (P0, P1)
- [ ] Technical debt items documented and prioritized
- [ ] Code freeze in effect (no new features, only critical fixes)

---

## Testing

### Automated Testing
- [ ] All unit tests passing (>80% coverage)
- [ ] Integration tests passing for critical paths
- [ ] End-to-end tests passing for key user flows
- [ ] Performance tests completed (if applicable)
- [ ] Load testing completed for expected traffic (if applicable)
- [ ] Regression testing suite executed and passing

### Security Testing
- [ ] Dependency vulnerability scan passed
- [ ] Static code analysis (SAST) passed
- [ ] Container/infrastructure scanning passed
- [ ] Penetration testing completed (for major releases)
- [ ] Security review conducted for sensitive changes

### Manual Testing
- [ ] QA sign-off received on all features
- [ ] Manual exploratory testing completed
- [ ] Cross-browser testing (Chrome, Firefox, Safari, Edge)
- [ ] Mobile testing (iOS, Android if applicable)
- [ ] Accessibility testing (WCAG compliance)
- [ ] Usability testing for new user-facing features

### Test Environment
- [ ] Release candidate deployed to staging environment
- [ ] Smoke tests passed in staging
- [ ] Data migrations tested in staging (if applicable)
- [ ] Rollback tested in staging
- [ ] Performance validated in staging

---

## Documentation

### Technical Documentation
- [ ] API documentation updated (if APIs changed)
- [ ] Architecture diagrams updated (if architecture changed)
- [ ] Database schema changes documented
- [ ] Configuration changes documented
- [ ] README and setup instructions current

### User Documentation
- [ ] User-facing documentation updated
- [ ] Help center articles updated (if applicable)
- [ ] In-app tooltips/help updated
- [ ] FAQ updated with new features

### Operational Documentation
- [ ] Runbooks updated for operations
- [ ] Monitoring playbooks updated
- [ ] Incident response procedures updated
- [ ] Deployment runbook created/updated

---

## Release Preparation

### Release Artifacts
- [ ] Release notes drafted and reviewed
  - New features listed with descriptions
  - Bug fixes documented
  - Breaking changes highlighted
  - Migration steps included (if any)
  - Known issues listed
- [ ] Changelog updated
- [ ] Version numbers updated in all relevant places
- [ ] Release branch created and tagged

### Deployment Readiness
- [ ] Deployment window scheduled and communicated
- [ ] Database backup/snapshot completed
- [ ] Feature flags configured (if using)
- [ ] Environment variables configured
- [ ] Database migrations prepared and tested
- [ ] Rollback plan documented and tested
- [ ] Deployment runbook reviewed

### Monitoring & Observability
- [ ] Monitoring dashboards created/updated
- [ ] Alerts configured for critical metrics
- [ ] Logs configured and accessible
- [ ] Error tracking configured
- [ ] Performance monitoring in place
- [ ] On-call schedule confirmed

---

## Communication

### Internal Communication
- [ ] Stakeholders notified of release schedule
- [ ] Support team briefed on new features
- [ ] Marketing team briefed (if customer-facing)
- [ ] Sales team briefed (if applicable)
- [ ] Internal announcement prepared
- [ ] Post-release communication plan ready

### External Communication
- [ ] Customer notification prepared (if needed)
- [ ] Public announcement drafted (if applicable)
- [ ] Social media posts drafted (if applicable)
- [ ] Partner notifications sent (if applicable)

### Team Coordination
- [ ] All team members aware of release timing
- [ ] On-call engineer identified and available
- [ ] Incident response team on standby
- [ ] War room/communication channel established

---

## Compliance & Legal

- [ ] Legal review completed (if required)
- [ ] Compliance requirements validated
- [ ] Privacy impact assessment completed (if data handling changed)
- [ ] Terms of service updated (if needed)
- [ ] License compliance verified

---

## Risk Management

- [ ] Risk register reviewed
- [ ] High-severity risks have mitigation plans
- [ ] Rollback criteria defined
- [ ] Incident escalation path confirmed
- [ ] Disaster recovery plan reviewed

---

## Final Approvals

- [ ] Product Manager approval: ___________  Date: ______
- [ ] Tech Lead approval: ___________  Date: ______
- [ ] Security approval: ___________  Date: ______
- [ ] QA approval: ___________  Date: ______
- [ ] Release Manager approval: ___________  Date: ______
- [ ] Sponsor/Stakeholder approval: ___________  Date: ______

---

## Post-Release

*To be completed after deployment*

- [ ] Deployment completed successfully
- [ ] Smoke tests passed in production
- [ ] Monitoring shows healthy metrics
- [ ] Release announcement sent
- [ ] Support team notified of successful release
- [ ] Post-release retrospective scheduled (within 2-3 days)

---

## Rollback Triggers

Deploy will be rolled back if any of these occur:
- [ ] Smoke tests fail in production
- [ ] Error rate exceeds [X]% for more than [Y] minutes
- [ ] Critical functionality is broken
- [ ] Performance degrades beyond acceptable thresholds
- [ ] Security vulnerability detected

**Rollback Owner**: [Name]  
**Rollback Procedure**: [Link to rollback runbook]

---

## Notes

[Any additional notes, context, or special considerations for this release]

---

**Checklist Completed By**: [Name]  
**Date**: [Date]  
**Release Decision**: [ ] GO [ ] NO-GO  
**If NO-GO, Reason**: [Explain what's blocking]

---

## Instructions

1. Start this checklist 1 week before target release date
2. Assign owners to incomplete items
3. Review daily in the days leading up to release
4. Do not proceed with release until all critical items are checked
5. Some items may be marked N/A if not applicable - document why
6. Archive completed checklist with release artifacts
