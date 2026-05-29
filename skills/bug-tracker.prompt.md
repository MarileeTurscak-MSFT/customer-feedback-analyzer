---
mode: agent
description: >-
  Tracks all customer-reported bugs from feedback sources. Classifies by
  severity, impact, repro status, and resolution state. Cross-references
  with issue trackers to identify untracked bugs. Use when asked to review
  bugs, track bug status, generate a bug report, or find unresolved
  customer issues.
---

# Bug Tracker

Generate a focused report on all customer-reported bugs. Extracts bugs from feedback sources, classifies severity, tracks resolution, and identifies patterns.

## When to Use

- Reviewing all open customer-reported bugs
- Preparing bug triage or review meetings
- Identifying the highest-impact bugs to fix next
- Finding bugs reported by customers but missing from the issue tracker
- Tracking bug resolution velocity over time

## Configuration

- **Product name:** [Your Product Name]
- **Feedback folder:** `customer-feedback/`
- **Issue tracker:** Azure DevOps | GitHub Issues | Jira | Linear | none
- **Project/repo:** [your-org/your-project]
- **Output file:** `customer-feedback/YYYY-MM-DD-bug-report.md`
- **Reporting period:** last 30 days

## Severity Definitions

| Severity | Criteria |
|----------|----------|
| 🔴 Critical | Data loss, security vulnerability, complete feature outage, or blocks customer deployment |
| 🟠 High | Major feature broken, significant workaround required, affects multiple customers |
| 🟡 Medium | Feature partially broken, minor workaround available, limited customer impact |
| 🟢 Low | Cosmetic issue, edge case, or minor inconvenience with easy workaround |

## Operating Rules

1. **Scan all feedback sources** for bug signals: errors, crashes, "doesn't work," unexpected behavior, regressions, data issues
2. **Deduplicate** bugs reported by multiple customers into a single entry
3. **Classify severity** based on customer impact, not just technical complexity
4. **Check issue tracker** for matching work items and resolution status
5. **Flag gaps** where customers reported bugs with no tracker entry
6. **Generate the report** with prioritized actions

## Report Structure

```markdown
# Bug Report: [Product Name]

**Report date:** YYYY-MM-DD
**Reporting period:** [start] — [end]
**Feedback sources reviewed:** [list]
**Issue tracker:** [tracker name]

---

## Summary

| Metric | Count |
|--------|-------|
| Total bugs reported | |
| 🔴 Critical | |
| 🟠 High | |
| 🟡 Medium | |
| 🟢 Low | |
| ✅ Resolved this period | |
| ⏳ Open / unresolved | |
| ⚠️ Not in tracker | |

---

## Critical & High Bugs

Bugs that need immediate attention:

| # | Bug | Severity | Customers Affected | Reported | Status | Work Item | Repro Steps Available |
|---|-----|----------|-------------------|----------|--------|-----------|----------------------|
| 1 | | | | | Open / In Progress / Resolved | [link] | Yes / No |

### Detail: [Bug title]

- **Description:** [What happens]
- **Expected behavior:** [What should happen]
- **Customers affected:** [list]
- **Customer quotes:**
  > "[verbatim quote]" — [Customer], [date]
- **Workaround:** [if any]
- **Root cause:** [if known]

---

## Medium & Low Bugs

| # | Bug | Severity | Customers | Reported | Status | Work Item |
|---|-----|----------|-----------|----------|--------|-----------|
| 1 | | | | | | |

---

## Bug Patterns

Recurring themes or clusters:

| # | Pattern | Related Bugs | Possible Root Cause |
|---|---------|-------------|-------------------|
| 1 | | | |

---

## Resolution Velocity

| Metric | This Period | Last Period | Trend |
|--------|-----------|------------|-------|
| Bugs opened | | | |
| Bugs resolved | | | |
| Avg days to resolve | | | |
| Oldest open bug (days) | | | |

---

## Bugs Not in Tracker

| # | Bug | Severity | Customer(s) | Source | Recommended Action |
|---|-----|----------|-------------|-------|-------------------|
| 1 | | | | | Create work item |

---

## Recommended Actions

| Priority | Action | Bug(s) | Rationale |
|----------|--------|--------|-----------|
| 🔴 High | | | |
| 🟡 Medium | | | |
| 🟢 Low | | | |
```

## Output Checklist

- [ ] All bugs from feedback are captured and deduplicated
- [ ] Severity is assigned based on customer impact
- [ ] Issue tracker cross-reference is complete
- [ ] Untracked bugs are flagged
- [ ] Critical and high bugs have detail sections with customer quotes
- [ ] Bug patterns are identified
- [ ] Resolution velocity is calculated
