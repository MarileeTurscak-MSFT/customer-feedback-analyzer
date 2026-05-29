# Bug Report: AI Cost Analyzer

**Report date:** 2026-05-29
**Reporting period:** 2026-04-29 — 2026-05-29
**Feedback sources reviewed:** cumulative-report-sample.md, weekly-report-sample.md, sample-feedback files
**Issue tracker:** Azure DevOps (CostAnalyzer project)

---

## Summary

| Metric | Count |
|--------|-------|
| Total bugs reported | 12 |
| 🔴 Critical | 2 |
| 🟠 High | 3 |
| 🟡 Medium | 4 |
| 🟢 Low | 3 |
| ✅ Resolved this period | 5 |
| ⏳ Open / unresolved | 5 |
| ⚠️ Not in tracker | 2 |

---

## Critical & High Bugs

| # | Bug | Severity | Customers Affected | Reported | Status | Work Item | Repro |
|---|-----|----------|-------------------|----------|--------|-----------|-------|
| 1 | Dashboard timeout on 10k+ resources | 🔴 Critical | Contoso Financial, Alpine Ski House | Apr 12 | ✅ Resolved | AB#4821 | Yes |
| 2 | Scan fails silently on expired service principal | 🔴 Critical | Tailspin Toys | May 23 | ⏳ Open | — | Yes |
| 3 | False positives flagging active dev/test environments | 🟠 High | Fabrikam Healthcare, Northwind Traders | Apr 20 | ✅ Resolved | AB#4790 | Yes |
| 4 | GCP cost projection chart shows $0 | 🟠 High | Woodgrove Bank, Relecloud | May 1 | ⏳ In Progress | AB#4833 | Yes |
| 5 | Incorrect savings estimate for reserved instances | 🟠 High | Woodgrove Bank | Apr 28 | ✅ Resolved | AB#4845 | Yes |

### Detail: Scan fails silently on expired service principal

- **Description:** When the service principal credentials expire, scans fail without any error message. The dashboard shows the last successful scan date with no indication of failure.
- **Expected behavior:** Clear error notification when credentials expire, with instructions to renew.
- **Customers affected:** Tailspin Toys
- **Customer quotes:**
  > "We didn't realize our scans hadn't run for two weeks. There was no alert, no error, nothing. We just had stale data." — Tailspin Toys, May 23
- **Workaround:** Manually check service principal expiry dates and renew proactively
- **Root cause:** Scan pipeline catches the auth error but swallows it. No retry or notification path.

### Detail: Dashboard timeout on 10k+ resources (RESOLVED)

- **Description:** Dashboard would spin indefinitely for accounts with more than 10,000 resources.
- **Resolution:** Added server-side pagination. Dashboard now loads in under 5 seconds for any account size.
- **Customers affected:** Contoso Financial, Alpine Ski House
- **Resolved:** May 15, 2026

---

## Medium & Low Bugs

| # | Bug | Severity | Customers | Reported | Status | Work Item |
|---|-----|----------|-----------|----------|--------|-----------|
| 1 | Duplicate entries after re-scan | 🟡 Medium | Tailspin Toys | Apr 15 | ✅ Resolved | AB#4830 |
| 2 | CSV export truncates names over 64 chars | 🟡 Medium | Woodgrove Bank | May 5 | ✅ Resolved | AB#4756 |
| 3 | Dashboard doesn't render on Safari 18 | 🟡 Medium | Northwind Traders | May 26 | ⏳ Open | — |
| 4 | Alert emails missing resource group name | 🟡 Medium | Contoso Financial | May 10 | ⏳ Open | AB#4855 |
| 5 | Sorting by cost descending resets page to 1 | 🟢 Low | Adatum Corp | May 14 | ⏳ Open | AB#4862 |
| 6 | Tooltip text overlaps on narrow screens | 🟢 Low | Proseware Inc | May 20 | ⏳ Backlogged | AB#4870 |
| 7 | Scan history shows UTC instead of local time | 🟢 Low | Fabrikam Healthcare | May 8 | ⏳ Backlogged | AB#4858 |

---

## Bug Patterns

| # | Pattern | Related Bugs | Possible Root Cause |
|---|---------|-------------|-------------------|
| 1 | Silent failures / missing error messages | Expired SP silent fail, no scan failure alert | Error handling swallows exceptions without notifying |
| 2 | Display/rendering issues across browsers | Safari 18 rendering, tooltip overlap, sort reset | Insufficient cross-browser testing |
| 3 | Data accuracy on non-Azure clouds | GCP $0 projections, GCP docs gaps | GCP integration was MVP-quality at launch |

---

## Resolution Velocity

| Metric | This Period | Last Period | Trend |
|--------|-----------|------------|-------|
| Bugs opened | 4 | 6 | ↓ Improving |
| Bugs resolved | 5 | 3 | ↑ Improving |
| Avg days to resolve | 18 | 24 | ↑ Improving |
| Oldest open bug (days) | 28 | 35 | ↑ Improving |

---

## Bugs Not in Tracker

| # | Bug | Severity | Customer(s) | Source | Recommended Action |
|---|-----|----------|-------------|-------|-------------------|
| 1 | Scan fails silently on expired SP | 🔴 Critical | Tailspin Toys | Weekly 05-23 | Create work item immediately |
| 2 | Safari 18 rendering broken | 🟡 Medium | Northwind Traders | Weekly 05-26 | Create work item, assign to frontend team |

---

## Recommended Actions

| Priority | Action | Bug(s) | Rationale |
|----------|--------|--------|-----------|
| 🔴 High | Create work item and fix silent scan failure | Expired SP bug | Critical: customers running on stale data without knowing |
| 🔴 High | Add scan health monitoring and alerts | Silent failure pattern | Systemic: error handling gap affects trust |
| 🟡 Medium | Fix Safari 18 rendering | Safari bug | Key account affected, create tracker item |
| 🟡 Medium | Resolve GCP cost projection chart | GCP $0 bug | Already in progress, confirm target date |
| 🟢 Low | Schedule cross-browser testing sprint | Display pattern | Three display bugs suggest testing gap |

---

## Methodology

- Feedback sources: All sample feedback files, weekly and cumulative reports
- Issue tracker: Azure DevOps, CostAnalyzer project
- Severity assigned based on customer impact and breadth
- Bugs deduplicated across customers (same bug, multiple reporters = one entry)
- **Note:** This is a sample report using fictional data for demonstration purposes
