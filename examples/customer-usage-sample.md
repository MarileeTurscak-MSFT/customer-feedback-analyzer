# Customer Usage Report: AI Cost Analyzer

**Report date:** 2026-05-29
**Reporting period:** 2026-04-29 — 2026-05-29
**Data source:** Product telemetry API

---

## Summary Dashboard

| Metric | Count | % of Total |
|--------|-------|------------|
| Total customers | 13 | 100% |
| Advanced deployers (3+ features) | 6 | 46% |
| Monthly active (MAU) | 11 | 85% |
| Weekly active (WAU) | 8 | 62% |
| Inactive (no usage in 30 days) | 2 | 15% |

---

## Customer Roster

| # | Customer | Features Used | Depth | Last Active | MAU | WAU | Status |
|---|----------|--------------|-------|-------------|-----|-----|--------|
| 1 | Contoso Financial | Scan, Dashboard, Alerts, Reports, API | 5 | May 29 | Yes | Yes | Active |
| 2 | Northwind Traders | Scan, Dashboard, Reports, Tagging | 4 | May 28 | Yes | Yes | Active |
| 3 | Fabrikam Healthcare | Scan, Dashboard, Alerts, Tagging | 4 | May 27 | Yes | Yes | Active |
| 4 | Woodgrove Bank | Scan, Dashboard, Reports | 3 | May 29 | Yes | Yes | Active |
| 5 | Tailspin Toys | Scan, Dashboard, Alerts | 3 | May 26 | Yes | Yes | Active |
| 6 | Alpine Ski House | Scan, Dashboard, API | 3 | May 25 | Yes | Yes | Active |
| 7 | Adatum Corp | Scan, Dashboard | 2 | May 28 | Yes | Yes | Active |
| 8 | Proseware Inc | Scan, Dashboard | 2 | May 24 | Yes | Yes | Active |
| 9 | Relecloud | Scan, Reports | 2 | May 18 | Yes | No | At Risk |
| 10 | Wingtip Toys | Scan | 1 | May 12 | Yes | No | At Risk |
| 11 | Margie's Travel | Scan | 1 | May 3 | Yes | No | At Risk |
| 12 | Litware Inc | Scan | 1 | Apr 15 | No | No | Inactive |
| 13 | VanArsdel Ltd | Dashboard | 1 | Apr 2 | No | No | Inactive |

---

## Feature Adoption

| # | Feature | Customers Using | Adoption Rate | Trend |
|---|---------|----------------|---------------|-------|
| 1 | Resource Scan | 12 | 92% | → Stable |
| 2 | Cost Dashboard | 11 | 85% | ↑ +1 from last month |
| 3 | Stale Resource Alerts | 4 | 31% | ↑ +1 from last month |
| 4 | Scheduled Reports | 4 | 31% | → Stable |
| 5 | Resource Tagging | 3 | 23% | ↑ New this month |
| 6 | REST API | 2 | 15% | → Stable |

---

## Deployment Depth Distribution

| Features Used | Customers | % of Total |
|---------------|-----------|------------|
| 1 feature | 3 | 23% |
| 2 features | 4 | 31% |
| 3 features | 3 | 23% |
| 4 features | 2 | 15% |
| 5+ features | 1 | 8% |

---

## Usage Trends

### Month-over-Month

| Metric | This Month | Last Month | Change |
|--------|-----------|------------|--------|
| MAU | 11 | 10 | +10% |
| WAU | 8 | 7 | +14% |
| Advanced deployers | 6 | 4 | +50% |
| Avg features per customer | 2.5 | 2.1 | +19% |

### Engagement Segments

| Segment | Count | Description |
|---------|-------|-------------|
| Power users | 3 | WAU + 4+ features (Contoso, Northwind, Fabrikam) |
| Regular users | 5 | WAU + 2-3 features |
| Light users | 3 | MAU + 1 feature |
| At risk | 3 | No usage in 7-30 days (Relecloud, Wingtip, Margie's) |
| Churned | 2 | No usage in 30+ days (Litware, VanArsdel) |

---

## At-Risk Customers

| # | Customer | Last Active | Features Used | Previous MAU | Risk Signal |
|---|----------|-------------|--------------|-------------|-------------|
| 1 | Relecloud | May 18 | 2 | Yes | Declining: was weekly active last month, now 11 days since last use |
| 2 | Wingtip Toys | May 12 | 1 | Yes | Only uses Scan. Never adopted Dashboard or Alerts. Low engagement depth |
| 3 | Margie's Travel | May 3 | 1 | Yes | Only used Scan once in May. Was more active in April. Possible churn |
| 4 | Litware Inc | Apr 15 | 1 | No | Inactive 44 days. Used Scan once during trial, never returned |
| 5 | VanArsdel Ltd | Apr 2 | 1 | No | Inactive 57 days. Opened Dashboard but never ran a Scan. Onboarding failure |

---

## Recommended Actions

| Priority | Action | Customer(s) | Rationale |
|----------|--------|-------------|-----------|
| 🔴 High | Re-engage Litware and VanArsdel with onboarding call | Litware, VanArsdel | Inactive 44+ days, likely churn without intervention |
| 🔴 High | Check in with Relecloud on usage drop | Relecloud | Was weekly active, now 11 days silent. May indicate a blocker |
| 🟡 Medium | Promote Alerts feature to 2-feature customers | Adatum, Proseware | Easy upsell: they use Scan + Dashboard, Alerts is the natural next step |
| 🟡 Medium | Share "getting started" lab with Wingtip and Margie's | Wingtip, Margie's | Low depth suggests they haven't seen the full value yet |
| 🟢 Low | Highlight API integration to power users | Contoso, Northwind, Fabrikam | Already deep adopters, API would enable automation workflows |

---

## Methodology

- Data source: Product telemetry API (usage events)
- Reporting period: April 29 — May 29, 2026
- Features tracked: Resource Scan, Cost Dashboard, Stale Resource Alerts, Scheduled Reports, Resource Tagging, REST API
- Advanced deployment threshold: 3 features
- Activity windows: WAU = 7 days, MAU = 30 days
- **Note:** This is a sample report using fictional data for demonstration purposes
