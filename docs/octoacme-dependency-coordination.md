# OctoAcme Dependency & Cross-Team Coordination Template

Use this template to manage dependencies and coordinate across teams to reduce blockers and improve project visibility.

## Project Details
- **Project Name**: [Project Name]
- **Project Manager**: [PM Name]
- **Tracking Tool**: [Link to project board]

---

## Dependency Inventory

Identify all dependencies upfront to enable proactive management.

| Dependency ID | Description | Dependent Team | Owner | Target Completion | Impact if Delayed | Mitigation Plan | Status |
|---|---|---|---|---|---|---|---|
| D001 | [Describe dependency] | [Team A] | [Owner name] | [Date] | [Impact if late] | [Plan if delayed] | 🟢 On track |
| D002 | [Describe dependency] | [Team B] | [Owner name] | [Date] | [Impact if late] | [Plan if delayed] | 🟡 At risk |

---

## Dependency Categories

### External Dependencies (Outside Org)
- Third-party APIs or services
- Vendor integrations
- Open-source library releases

**Owner**: [Team Lead]  
**How to manage**: Create issue, set reminder, establish fallback plan

### Cross-Team Dependencies
- Engineering team A waits for Engineering team B
- Product changes affect multiple product lines
- Infrastructure changes needed before deployment

**Owner**: [PM + dependent team leads]  
**How to manage**: Weekly sync, shared project board, escalation path

### Internal Technical Dependencies
- Feature A depends on Feature B
- Refactor must complete before new feature
- Database schema migration needed first

**Owner**: [Technical Lead]  
**How to manage**: Backlog ordering, sprint planning, code review

---

## Dependency Management Process

### 1. Identify Dependencies (Planning Phase)
During project planning, identify and document all dependencies:
- What external systems/teams are you dependent on?
- What deliverables do they need from us?
- What blockers might occur?
- When do they need each piece?

**Checklist**:
- [ ] Interviewed all stakeholder teams
- [ ] Created dependency list with dates
- [ ] Identified criticality (blocking vs. nice-to-have)
- [ ] Confirmed with dependent teams
- [ ] Added to project dashboard or board

### 2. Track Dependencies Weekly (Execution Phase)
At weekly syncs, review dependency status:

**Status Categories**:
- 🟢 **Green**: On track, no issues
- 🟡 **Yellow**: At risk, may miss target date
- 🔴 **Red**: Off track, will miss target date

| Dependency | Owner | Current Status | Due Date | Risk | Action |
|---|---|---|---|---|---|
| API team delivers endpoint | [Name] | 🟡 Yellow | May 20 | Design review delayed | Escalate to API lead; get interim API mock |
| Database team provisions DB | [Name] | 🟢 Green | May 15 | None | Continue monitoring |

### 3. Escalate & Mitigate (As Needed)
If a dependency goes yellow or red:
- [ ] Immediately notify PM and dependent team lead
- [ ] Activate mitigation plan
- [ ] Assess impact on project timeline
- [ ] Adjust project plan if needed
- [ ] Communicate changes to stakeholders

### 4. Close Dependencies (Delivery Phase)
When dependency is delivered:
- [ ] Verify it meets acceptance criteria
- [ ] Document any surprises or learnings
- [ ] Mark as complete and move on

---

## Cross-Team Coordination Meeting Template

**When**: Weekly on [DAY] at [TIME]  
**Who**: PMs, Tech Leads, and owners of active dependencies  
**Duration**: 30 minutes  
**Agenda**:

1. **Dependency Status Update** (15 min)
   - Quick review of Yellow and Red items
   - Any new blockers?
   - Wins/unblocks?

2. **Risk Discussion** (10 min)
   - What could go wrong in the next 2 weeks?
   - What do we need from each other?
   - Any competing priorities?

3. **Next Steps & Decisions** (5 min)
   - Assignments and action items
   - Escalations to leadership if needed
   - Next meeting agenda

**Note-taker**: [Rotating role]  
**Shared doc**: [Link to meeting notes]

---

## Shared Project Dashboard

Create a shared view of all active projects and dependencies.

### Dashboard Layout
- **Columns**: Project, Status (On track / At risk / Blocked), Key Milestone, Owner, Next Review
- **Color coding**: 🟢 Green / 🟡 Yellow / 🔴 Red
- **Updated**: Weekly (Friday EOD)
- **Access**: [Link]

### Example Entry
| Project | Status | Milestone | Target Date | Owner | Blockers | Notes |
|---------|--------|-----------|------------|-------|----------|-------|
| Mobile App v2.0 | 🟡 At risk | Backend APIs ready | May 20 | PM: Jane | API team 1 week behind | Mitigating with mock APIs |
| Analytics Dashboard | 🟢 Green | Initial release | June 1 | PM: Bob | None | On track for launch |

---

## Dependency Risk Register

Capture potential risks and mitigation plans.

| Risk ID | Description | Probability | Impact | Owner | Mitigation | Contingency Plan |
|---------|---|---|---|---|---|---|
| R001 | Vendor API delayed | Medium | High | [Owner] | Weekly check-ins, parallel mock implementation | Use fallback API or defer feature |
| R002 | Infrastructure team overloaded | High | High | [Owner] | Prioritize with infra team; offer resources | Pre-allocate infrastructure; deploy early |
| R003 | Data migration underestimated | Medium | Medium | [Owner] | Pilot migration on subset of data | Extended timeline; communication plan |

---

## Coordination Patterns

### Pattern 1: Handoff Dependencies
**Scenario**: Team A must complete before Team B starts

**Mitigation**:
- Clear acceptance criteria for Team A's deliverable
- Team B reviews and approves before moving to next phase
- Buffer time built into plan
- If delayed, Team B identifies early alternatives

**Example**: Backend team delivers API → Mobile team integrates

### Pattern 2: Parallel Dependencies
**Scenario**: Teams work on independent pieces but must integrate

**Mitigation**:
- Clear API contracts or interfaces upfront
- Mock implementations used for integration testing
- Regular integration checkpoints (weekly or bi-weekly)
- Automated testing ensures compatibility

**Example**: Frontend team builds UI while backend team builds API; integrate weekly

### Pattern 3: Blocking Dependencies
**Scenario**: Can't start until external blocker is resolved

**Mitigation**:
- Identify early in planning
- Escalate to leadership for priority
- Create fallback/workaround plan
- Plan parallel work if possible
- Daily status checks while blocked

**Example**: Waiting for compliance approval to move to production

---

## Communication Templates

### Dependency Status Email
```
Subject: [Weekly] Project [Name] - Dependency Status [Week of MM/DD]

Hi Team,

Here's the dependency status for [Project]:

🟢 ON TRACK (3):
- API team delivering endpoints (target: May 20) ✅
- Database provisioning (target: May 15) ✅
- Compliance review (target: May 18) ✅

🟡 AT RISK (1):
- Mobile app SDK update: Originally May 15, now May 25 ⚠️
  Impact: Delays mobile feature by ~1 week
  Action: Escalating to Product Lead for prioritization

🔴 BLOCKED (0):
- None currently

If you own any dependencies, please reply with updates.

Next sync: [Day/Time]

Thanks,
[PM Name]
```

### Escalation Notice
```
Subject: [ESCALATION] [Project Name] - Dependency at Risk

Problem:
[Team] was supposed to deliver [deliverable] by [date]. They now estimate [new date].

Impact:
- Our project milestone [Y] will slip from [original date] to [new date]
- This affects [dependent teams] and [go-live date]

What we've tried:
- [Mitigation attempts]

What we need:
- Prioritization from leadership to re-allocate resources to [Team]
- OR approval to delay our milestone
- OR alternative approach (defer feature, use fallback)

Requested by: [Date]  
Owner: [Name]
```

### Dependency Closure Memo
```
Dependency: [ID] - [Description]
Status: ✅ CLOSED
Actual Delivery Date: [Date]
Planned Delivery Date: [Date]
Variance: [+/- X days]

Learnings:
- What went well: [...]
- What could improve: [...]
- Recommendations: [...]

Signed off by: [Owner] on [Date]
```

---

## Retrospective: Dependency Management

After project completion, review how dependencies were managed:

**Questions to discuss**:
- Were dependencies identified early enough?
- Did we catch Yellow/Red status in time to mitigate?
- Did mitigation plans actually work?
- Were escalations clear and timely?
- How could we improve coordination for next project?

**Action items** from retrospective:
- [ ] Update dependency templates with lessons learned
- [ ] Improve integration testing or mock setup
- [ ] Add buffer time to dependent items
- [ ] Increase sync frequency for critical paths

---

## Tools & Integrations

| Tool | Purpose | How to Use |
|------|---------|-----------|
| **GitHub Projects** | Track backlog + dependencies | Link PRs/issues to dependencies |
| **Jira** | Cross-team backlog visibility | Create "Blocker" issue type |
| **Slack** | Quick notifications | `/remind` for dependency dates |
| **Shared Google Sheet** | Real-time dependency dashboard | Weekly update by Friday EOD |
| **Confluence** | Document dependency matrix | Update during planning phase |

---

## Approval & Sign-Off

**Dependency Plan Created By**: [Name] on [Date]  
**Reviewed By**: [PM, Product Lead] on [Date]  
**Approved By**: [Sponsor/Leader] on [Date]

---

## Quick Reference: Dependency Checklist

✅ **Before Execution**:
- [ ] All dependencies identified and documented
- [ ] Dependencies ranked by criticality
- [ ] Dependent teams confirmed dates and dependencies
- [ ] Mitigation plans created for high-risk items
- [ ] Escalation path defined
- [ ] Weekly sync scheduled

✅ **During Execution**:
- [ ] Weekly status updates on all dependencies
- [ ] Yellow/Red items escalated within 1 business day
- [ ] Mitigation plans activated immediately
- [ ] Project plan adjusted if needed
- [ ] Communication to stakeholders updated

✅ **At Completion**:
- [ ] All dependencies marked complete/closed
- [ ] Variance from plan documented
- [ ] Learnings captured in retrospective
- [ ] Process improved for next project

---

**Last Updated**: 2026-05-15  
**For questions or improvements**: Submit issue using [Add Content to Process Docs](../../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml) template
