# OctoAcme — Retrospective & Continuous Improvement

## Purpose
Capture learnings and convert them into actionable improvements.

## When
After each sprint, release, or important milestone. Also after incidents.

## Structure

### Retrospective Agenda (60-75 minutes)

**1. Set the Stage (5 min)**
- Review purpose: learn and improve, not blame
- Establish safety: Vegas rule, focus on systems not people
- Review previous action items and their impact

**2. Gather Data (15 min)**
- Timeline review: key events, milestones, surprises
- Metrics review: velocity, quality, deployment stats
- Individual reflection: what stood out to you?

**3. Generate Insights (20 min)**
Use one of these formats:
- **Start/Stop/Continue**: What should we start doing? Stop doing? Continue doing?
- **Glad/Sad/Mad**: What made you glad? What made you sad? What made you mad?
- **4Ls**: Liked, Learned, Lacked, Longed For
- **Sailboat**: Wind (what helped), Anchor (what slowed us), Rocks (risks ahead)

**4. Decide What to Do (15 min)**
- Group similar themes
- Vote on top 2-3 items to address
- Define specific, measurable actions
- Assign owners and deadlines

**5. Close (5 min)**
- Summarize action items
- Appreciation round: call out great contributions
- Preview next retrospective date

### Facilitator Guidelines
- **Rotate facilitators** to share the load and bring fresh perspectives
- **Time-box discussions** to maintain energy and focus
- **Encourage quiet voices** through written input or smaller breakouts
- **Stay neutral** - facilitator doesn't dominate the conversation
- **Capture in real-time** on shared board or document

## Running a Retrospective

### Preparation (Before the Meeting)
- [ ] Schedule retrospective within 2-3 days of sprint/milestone completion
- [ ] Send calendar invite with agenda and retrospective format
- [ ] Set up anonymous idea collection tool (Miro, Jamboard, etc.)
- [ ] Gather relevant data: metrics, incident reports, team feedback
- [ ] Review previous retrospective actions to report on progress

### During the Retrospective
- **Create psychological safety**
  - Prime Directive: "Regardless of what we discover, we understand and truly believe that everyone did the best job they could, given what they knew at the time, their skills and abilities, the resources available, and the situation at hand."
  - Ground rules: No blame, focus on learning, everything shared is confidential
  
- **Use time-boxes ruthlessly**
  - Keeps energy high and ensures all phases get covered
  - Use a visible timer
  
- **Balance participation**
  - Round-robin sharing
  - Silent brainstorming before discussion
  - Anonymous input for sensitive topics
  
- **Focus on actionable outcomes**
  - Every insight doesn't need an action
  - Prioritize high-impact, achievable changes
  - Make actions SMART (Specific, Measurable, Achievable, Relevant, Time-bound)

### After the Retrospective
- [ ] Document action items in project tracking system
- [ ] Share retrospective summary with stakeholders (sanitized if needed)
- [ ] Add action items to team backlog or sprint plan
- [ ] Schedule follow-ups for action item owners
- [ ] Archive retrospective notes for future reference

### Retrospective Output Template
```markdown
## Retrospective: [Sprint/Milestone Name]
**Date**: [Date]
**Facilitator**: [Name]
**Attendees**: [List]

### What Went Well ✅
- [Item 1]
- [Item 2]
- [Item 3]

### What Could Be Improved 🔄
- [Item 1]
- [Item 2]
- [Item 3]

### Action Items 🎯
| ID | Action | Owner | Due Date | Priority |
|----|--------|-------|----------|----------|
| RETRO-2025-10-01 | [Action] | [Name] | [Date] | High |

### Previous Actions Review 📊
| ID | Action | Status | Outcome |
|----|--------|--------|---------|
| RETRO-2025-09-01 | [Previous action] | ✅ Completed | [Impact achieved] |

### Metrics
- Velocity: [X points/stories]
- Deployment frequency: [X deploys]
- Bug escape rate: [X%]
- Team happiness: [Score/10]

### Key Insights
[1-2 paragraphs capturing the most important learnings]
```

### Timebox: 45–75 minutes depending on team size
- Small teams (3-5): 45 minutes
- Medium teams (6-10): 60 minutes  
- Large teams (11+): 75 minutes

### Remote-Friendly Practices
- Use visual collaboration tools (Miro, Mural, FigJam)
- Enable video for better engagement
- Use breakout rooms for smaller discussions
- Record session (with permission) for absent team members
- Use polls and emoji reactions for quick feedback

### Use an anonymous idea board if needed to encourage candor
Tools that support anonymous brainstorming:
- Miro with hidden authorship
- Google Forms for initial input
- Slido for Q&A and voting
- Post-it notes (physical or virtual) without names

When to use anonymity:
- New teams still building trust
- Discussing sensitive topics
- Organizational or leadership concerns
- After conflicts or incidents

### Prioritize 2–3 top action items to avoid overload
**Why limit actions?**
- Teams can only absorb so much change at once
- Better to fully implement a few improvements than partially implement many
- Maintains focus and accountability
- Prevents retrospective action fatigue

**How to prioritize:**
1. Dot voting: Each person gets 3 votes to place on proposed actions
2. Impact/Effort matrix: Plot items by impact vs. effort, choose high impact/low effort
3. Team discussion: Reach consensus on top priorities
4. Consider: What will have the biggest positive impact on our next iteration?

## Tracking Improvements

### Action Item Template
Each retrospective action should be tracked with clear accountability:

```
**Action ID**: [RETRO-YYYY-MM-##]
**Title**: [Brief, action-oriented title]
**Description**: [What needs to be done and why]
**Category**: [Process/Tool/Team/Communication]
**Owner**: [Name - who is responsible]
**Due Date**: [Realistic completion date]
**Priority**: [High/Medium/Low]
**Success Criteria**: [How we know it's done and working]
**Status**: [Not Started/In Progress/Completed/Blocked]
**Related To**: [Project/Team/General Process]
```

### Action Tracking Board
Use GitHub Issues or project tracking tool to manage retrospective actions:

| Action ID | Title | Owner | Due Date | Status | Impact |
|-----------|-------|-------|----------|--------|--------|
| RETRO-2025-10-01 | Automate deployment checklist | @engineer | 2025-11-15 | In Progress | Medium |
| RETRO-2025-10-02 | Add API integration tests | @qa-lead | 2025-11-01 | Completed | High |

### Review Cadence
- **Weekly PM sync**: Review action item progress, identify blockers
- **Monthly team meeting**: Share completed improvements, celebrate wins
- **Next retrospective**: Review all previous actions as first agenda item

### Tracking Best Practices
1. **Limit to 2-3 high-impact actions per retrospective** - Avoid action fatigue
2. **Make actions specific and measurable** - "Improve documentation" → "Add deployment runbook to wiki by MM/DD"
3. **Assign clear owners** - Never leave actions unassigned
4. **Set realistic deadlines** - Consider team capacity
5. **Follow up consistently** - Don't let actions become invisible
6. **Close completed actions** - Acknowledge progress and impact
7. **Escalate blocked actions** - Surface impediments early

### Measuring Improvement Impact
Track metrics to validate that changes are working:
- **Process changes**: Cycle time, lead time, deployment frequency
- **Quality improvements**: Bug rates, test coverage, escaped defects
- **Team health**: Retrospective participation, psychological safety score
- **Communication**: Stakeholder satisfaction, clarity of status updates

Create a "Continuous Improvement Log":
```
| Date | Change Implemented | Expected Benefit | Actual Outcome | Keep/Adjust/Stop |
|------|-------------------|------------------|----------------|------------------|
| 2025-10 | Added pre-merge CI checks | Reduce prod bugs by 30% | Bug rate down 25% | Keep - refine further |
```

## Example Action Item Template
- Title:
- Description:
- Owner:
- Due date:
- Success criteria:

## Continuous Improvement Culture
- Measure impact of action items
- Celebrate improvements and make small, iterative changes
