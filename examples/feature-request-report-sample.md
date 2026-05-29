# Feature Request Report: AI Cost Analyzer

**Report date:** 2026-05-29
**Reporting period:** All time (new requests highlighted from last 30 days)
**Feedback sources reviewed:** cumulative-report-sample.md, weekly-report-sample.md, sample-feedback files
**Issue tracker:** Azure DevOps (CostAnalyzer project)

---

## Summary

| Metric | Count |
|--------|-------|
| Total unique feature requests | 18 |
| 🔴 Critical | 2 |
| 🟠 High | 4 |
| 🟡 Medium | 7 |
| 🟢 Low | 5 |
| ✅ Shipped / Resolved | 4 |
| 🗺️ On Roadmap | 5 |
| 📋 Backlogged | 4 |
| ⚠️ Not in tracker | 3 |
| 🆕 New this period | 3 |

---

## Top Feature Requests (Ranked by Demand)

| Rank | Feature Request | Priority | Customers | First Requested | Status | Work Item |
|------|----------------|----------|-----------|-----------------|--------|-----------|
| 1 | Slack/Teams alert integration | 🔴 Critical | 5 | Mar 10 | 🗺️ On Roadmap | AB#4860 |
| 2 | AWS multi-account scanning parity | 🔴 Critical | 4 | Mar 15 | 🗺️ On Roadmap | AB#4712 |
| 3 | Scheduled PDF reports for executives | 🟠 High | 4 | Apr 2 | 🗺️ On Roadmap | AB#4875 |
| 4 | Terraform/IaC state comparison | 🟠 High | 3 | Apr 18 | 🗺️ On Roadmap | AB#4890 |
| 5 | Custom tagging schema support | 🟠 High | 3 | Apr 5 | 📋 Backlogged | AB#4805 |
| 6 | Cost trend sparklines on dashboard | 🟠 High | 3 | Mar 28 | ✅ Shipped | AB#4689 |
| 7 | "Keep" tagging to exclude resources | 🟡 Medium | 2 | Apr 10 | ✅ Shipped | AB#4790 |
| 8 | Scan completion notifications | 🟡 Medium | 2 | Mar 20 | ✅ Shipped | AB#4701 |
| 9 | REST API for automation | 🟡 Medium | 2 | Apr 22 | ✅ Shipped | AB#4700 |
| 10 | Export to Power BI format | 🟡 Medium | 1 | May 28 | ⚠️ Not in tracker | — |

---

## Request Details

### 1. Slack/Teams alert integration

- **Priority:** 🔴 Critical
- **Customers requesting:** Contoso Financial (Mar 10), Woodgrove Bank (Mar 22), Fabrikam Healthcare (Apr 5), Adatum Corp (Apr 15), Proseware Inc (May 1)
- **Use case:** Teams want cost alerts delivered where they already work, not in a separate dashboard they have to check.
- **Representative quotes:**
  > "I need cost alerts in Slack, not another dashboard to check." — Contoso Financial, Mar 10
  > "Our ops team lives in Teams. If alerts don't show up there, they don't get seen." — Fabrikam Healthcare, Apr 5
- **Status:** On Roadmap, target v2.4 (June 2026)
- **Work item:** AB#4860 (In Progress)
- **Effort estimate:** M
- **Strategic value:** Top request by customer count. Drives daily engagement and stickiness.

### 2. AWS multi-account scanning parity

- **Priority:** 🔴 Critical
- **Customers requesting:** Northwind Traders (Mar 15), Woodgrove Bank (Apr 1), Alpine Ski House (Apr 12), Relecloud (May 5)
- **Use case:** Multi-cloud customers need equal scanning depth across Azure and AWS. Current AWS support is limited to single-account.
- **Representative quotes:**
  > "Azure scanning is great but our AWS accounts feel like second-class citizens." — Northwind Traders, Mar 15
  > "We can't recommend this to our AWS team until multi-account works." — Alpine Ski House, Apr 12
- **Status:** On Roadmap, target v2.5 (July 2026)
- **Work item:** AB#4712 (In Progress)
- **Effort estimate:** L
- **Strategic value:** Blocking multi-cloud adoption. Four customers waiting on this.

### 3. Scheduled PDF reports for executives

- **Priority:** 🟠 High
- **Customers requesting:** Contoso Financial (Apr 2), Woodgrove Bank (Apr 8), Tailspin Toys (Apr 20), Northwind Traders (May 10)
- **Use case:** Executives and finance teams want automated weekly/monthly PDF summaries they can review without logging into a dashboard.
- **Representative quotes:**
  > "My CFO won't log into a dashboard. Give me a weekly PDF I can forward." — Contoso Financial, Apr 2
- **Status:** On Roadmap, target v2.4 (June 2026)
- **Work item:** AB#4875 (Planned)
- **Effort estimate:** M
- **Strategic value:** Expands product reach beyond technical users to finance stakeholders.

---

## Recently Shipped

| # | Feature | Requested By | Times Requested | Shipped Date | Work Item |
|---|---------|-------------|-----------------|--------------|-----------|
| 1 | Cost trend sparklines | Northwind, Contoso, Fabrikam | 3 | May 12 | AB#4689 |
| 2 | "Keep" tagging (exclude resources) | Fabrikam, Tailspin | 2 | May 18 | AB#4790 |
| 3 | Scan completion notifications | Contoso, Alpine | 2 | May 3 | AB#4701 |
| 4 | REST API for automation | Contoso, Woodgrove | 2 | Apr 30 | AB#4700 |

### Customer Impact

- **Cost trend sparklines:** Northwind Traders uses these in weekly FinOps reviews. Most-requested dashboard enhancement.
- **"Keep" tagging:** Eliminated Fabrikam Healthcare's #1 complaint (false positives on dev/test environments).
- **Scan notifications:** Contoso Financial's ops team stopped polling the dashboard manually. Saves ~30 min/day.
- **REST API:** Woodgrove Bank built automated nightly scans into their CI/CD pipeline within a week of launch.

---

## On the Roadmap

| # | Feature | Priority | Customers | Target Release | Work Item | Status |
|---|---------|----------|-----------|----------------|-----------|--------|
| 1 | Slack/Teams alerts | 🔴 Critical | 5 | v2.4 (June) | AB#4860 | In Progress |
| 2 | AWS multi-account parity | 🔴 Critical | 4 | v2.5 (July) | AB#4712 | In Progress |
| 3 | Scheduled PDF reports | 🟠 High | 4 | v2.4 (June) | AB#4875 | Planned |
| 4 | Terraform/IaC comparison | 🟠 High | 3 | v2.6 (Aug) | AB#4890 | Planned |
| 5 | GCP scanning improvements | 🟡 Medium | 2 | v2.5 (July) | AB#4835 | Planned |

---

## Not in Tracker

| # | Feature Request | Priority | Customer(s) | Source | Recommended Action |
|---|----------------|----------|-------------|-------|-------------------|
| 1 | Export to Power BI format | 🟡 Medium | Contoso Financial | Weekly 05-28 | Create work item. Evaluate Power BI connector vs. export format |
| 2 | Compare costs across Azure subscriptions | 🟡 Medium | Contoso Financial | Weekly 05-19 | Merge with AB#4712 (multi-account parity) |
| 3 | Mobile-friendly dashboard view | 🟢 Low | Tailspin Toys | Cumulative | Create work item. Low priority but easy responsive CSS fix |

---

## Request Themes

| # | Theme | Requests | Total Customers | Top Request |
|---|-------|----------|----------------|-------------|
| 1 | Alerting & notifications | 3 | 6 | Slack/Teams integration |
| 2 | Multi-cloud parity | 3 | 5 | AWS multi-account scanning |
| 3 | Reporting & export | 4 | 5 | Scheduled PDF reports |
| 4 | Customization & config | 3 | 4 | Custom tagging schemas |
| 5 | IaC & automation | 3 | 4 | Terraform state comparison |

---

## Demand Trends

| Metric | This Period | Last Period | Trend |
|--------|-----------|------------|-------|
| New requests | 3 | 5 | ↓ Stabilizing |
| Requests shipped | 4 | 2 | ↑ Improving |
| Avg requests per customer | 2.8 | 2.3 | ↑ Growing |
| Most-requested feature | Slack/Teams alerts (5) | AWS parity (4) | Changed |

---

## Recommended Actions

| Priority | Action | Request(s) | Rationale |
|----------|--------|-----------|-----------|
| 🔴 High | Ship Slack/Teams alerts in v2.4 | #1 request | 5 customers waiting. Top demand signal. |
| 🔴 High | Confirm AWS multi-account timeline | #2 request | 4 customers blocked on multi-cloud. Churn risk. |
| 🟡 Medium | Create tracker items for 3 untracked requests | Power BI, cross-sub, mobile | Customer feedback not being captured as work |
| 🟡 Medium | Communicate shipped features to requesting customers | Sparklines, Keep tags, Notifications, API | Close the loop. Customers should know their feedback drove changes. |
| 🟢 Low | Evaluate custom tagging feasibility | Backlogged, 3 customers | Design review needed before committing to roadmap |

---

## Methodology

- Feedback sources: All sample feedback files, weekly and cumulative reports
- Issue tracker: Azure DevOps, CostAnalyzer project
- Priority based on customer count, strategic value, and blocking impact
- Requests deduplicated across customers (same request, multiple askers = one entry with demand count)
- **Note:** This is a sample report using fictional data for demonstration purposes
