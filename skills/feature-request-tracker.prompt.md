---
mode: agent
description: >-
  Tracks all customer feature requests from feedback sources. Ranks by
  customer demand, strategic value, and effort. Cross-references with
  issue trackers and roadmap. Use when asked to review feature requests,
  prioritize the backlog, generate a feature request report, or identify
  top customer asks.
---

# Feature Request Tracker

Generate a focused report on all customer feature requests. Extracts requests from feedback, ranks by demand and impact, and tracks roadmap status.

## When to Use

- Reviewing all open customer feature requests
- Prioritizing the backlog based on customer demand
- Preparing roadmap planning or prioritization meetings
- Identifying requests from customers that aren't in the backlog
- Communicating request status back to customers

## Configuration

- **Product name:** [Your Product Name]
- **Feedback folder:** `customer-feedback/`
- **Issue tracker:** Azure DevOps | GitHub Issues | Jira | Linear | none
- **Project/repo:** [your-org/your-project]
- **Output file:** `customer-feedback/YYYY-MM-DD-feature-request-report.md`
- **Reporting period:** all time (with trend data from last 30 days)

## Priority Framework

| Priority | Criteria |
|----------|----------|
| 🔴 Critical | Blocks adoption or expansion for multiple customers. Strategic importance. |
| 🟠 High | Requested by 3+ customers or a key account. Clear business value. |
| 🟡 Medium | Requested by 1-2 customers. Would improve experience but not blocking. |
| 🟢 Low | Nice-to-have. Single mention or edge case. |

## Operating Rules

1. **Scan all feedback sources** for feature signals: "I wish," "can you add," "it would be great if," "we need," "is there a way to," explicit feature requests
2. **Deduplicate** requests across customers into consolidated entries
3. **Count demand** by tracking how many customers requested each feature
4. **Rank by priority** using the framework above
5. **Check issue tracker** for matching work items and roadmap status
6. **Flag gaps** where customers requested features with no tracker entry
7. **Generate the report** with prioritized recommendations

## Report Structure

```markdown
# Feature Request Report: [Product Name]

**Report date:** YYYY-MM-DD
**Reporting period:** all time (new requests highlighted from last 30 days)
**Feedback sources reviewed:** [list]
**Issue tracker:** [tracker name]

---

## Summary

| Metric | Count |
|--------|-------|
| Total unique feature requests | |
| 🔴 Critical | |
| 🟠 High | |
| 🟡 Medium | |
| 🟢 Low | |
| ✅ Shipped / Resolved | |
| 🗺️ On Roadmap | |
| 📋 Backlogged | |
| ⚠️ Not in tracker | |
| 🆕 New this period | |

---

## Top Feature Requests (Ranked by Demand)

| Rank | Feature Request | Priority | Customers | First Requested | Status | Work Item |
|------|----------------|----------|-----------|-----------------|--------|-----------|
| 1 | | | | | | |

---

## Request Details

### 1. [Feature title]

- **Priority:** [level]
- **Customers requesting:** [list with dates]
- **Use case:** [Why they want it]
- **Representative quotes:**
  > "[verbatim quote]" — [Customer], [date]
  > "[verbatim quote]" — [Customer], [date]
- **Status:** [Not tracked / Backlogged / On Roadmap / In Progress / Shipped]
- **Work item:** [link if exists]
- **Effort estimate:** [if known: S/M/L/XL]
- **Strategic value:** [How this aligns with product direction]

---

## Recently Shipped

Feature requests that were delivered this period:

| # | Feature | Requested By | Times Requested | Shipped Date | Work Item |
|---|---------|-------------|-----------------|--------------|-----------|
| 1 | | | | | |

### Customer Impact

- **[Feature]:** [How it changed the customer experience. Specific outcomes.]

---

## On the Roadmap

| # | Feature | Priority | Customers | Target Release | Work Item | Status |
|---|---------|----------|-----------|----------------|-----------|--------|
| 1 | | | | | | Planned / In Progress |

---

## Not in Tracker

Requests from customers with no matching work item:

| # | Feature Request | Priority | Customer(s) | Source | Recommended Action |
|---|----------------|----------|-------------|-------|-------------------|
| 1 | | | | | Create work item / Merge with [existing] / Decline with rationale |

---

## Request Themes

Group related requests into themes:

| # | Theme | Requests | Total Customers | Top Request |
|---|-------|----------|----------------|-------------|
| 1 | | | | |

---

## Demand Trends

| Metric | This Period | Last Period | Trend |
|--------|-----------|------------|-------|
| New requests | | | |
| Requests shipped | | | |
| Avg requests per customer | | | |
| Most-requested feature | | | |

---

## Recommended Actions

| Priority | Action | Request(s) | Rationale |
|----------|--------|-----------|-----------|
| 🔴 High | | | |
| 🟡 Medium | | | |
| 🟢 Low | | | |
```

## Output Checklist

- [ ] All feature requests from feedback are captured and deduplicated
- [ ] Demand count (number of customers) is accurate per request
- [ ] Priority ranking reflects customer demand and strategic value
- [ ] Issue tracker cross-reference is complete
- [ ] Untracked requests are flagged with recommended actions
- [ ] Recently shipped features include customer impact descriptions
- [ ] Request themes group related asks together
