---
mode: agent
description: >-
  Tracks customer product usage and adoption metrics. Shows total customers,
  advanced deployers (using 3+ features), monthly active users, and weekly
  active users. Connects to any data source the user configures (telemetry
  API, database, CSV export, or manual input). Use when asked about customer
  adoption, usage tracking, feature engagement, MAU/WAU, or deployment depth.
---

# Customer Usage Tracker

Generate a customer usage and adoption report showing who is using your product, how deeply, and how often.

## When to Use

- Tracking customer adoption and engagement over time
- Identifying which customers have advanced vs. basic deployments
- Measuring monthly and weekly active usage
- Finding customers at risk of churn (low or declining usage)
- Preparing usage data for executive reviews or QBRs

## When NOT to Use

- Tracking bugs or feature requests (use the other feedback skills)
- Analyzing sentiment (use the weekly/cumulative feedback skills)

## Configuration

Customize these settings before running:

- **Product name:** [Your Product Name]
- **Data source:** telemetry API | database query | CSV export | manual input
- **Connection details:** [endpoint, query, or file path depending on source]
- **Feature list:** [list of trackable UX features in your product]
- **Advanced deployment threshold:** 3 (number of features a customer must use to count as "advanced")
- **Reporting period:** last 30 days
- **Output file:** `customer-feedback/YYYY-MM-DD-usage-report.md`

## Definitions

| Metric | Definition |
|--------|-----------|
| **Total customers** | All customers with an active account or license |
| **Advanced deployers** | Customers using 3 or more distinct UX features (configurable threshold) |
| **Monthly active (MAU)** | Customers with at least one usage event in the past 30 days |
| **Weekly active (WAU)** | Customers with at least one usage event in the past 7 days |
| **Feature adoption rate** | Percentage of total customers using a specific feature |
| **Deployment depth** | Number of distinct features a customer has used |

## Data Source Integration

This skill is designed to work with whatever data source you have. Configure one of the following:

### Telemetry API
- Provide the API endpoint and auth method
- The skill will query for usage events grouped by customer and feature
- Example: Application Insights, Mixpanel, Amplitude, Pendo, or custom telemetry

### Database Query
- Provide the connection string and a query template
- The skill will execute the query and parse results
- Example: SQL database, Kusto/ADX cluster, BigQuery

### CSV Export
- Export usage data as CSV with columns: `customer_name`, `feature_name`, `last_used_date`, `usage_count`
- Place the file in the configured data path
- The skill will read and aggregate

### Manual Input
- Provide a markdown table or list of customers and their feature usage
- The skill will structure and analyze it

## Operating Rules

1. **Connect to data source** using the configured method
2. **Retrieve usage events** for the reporting period
3. **Aggregate by customer** to calculate deployment depth and activity
4. **Classify each customer** into usage tiers
5. **Calculate summary metrics** (totals, percentages, trends)
6. **Generate the report** following the template below

## Report Structure

```markdown
# Customer Usage Report: [Product Name]

**Report date:** YYYY-MM-DD
**Reporting period:** [start] — [end]
**Data source:** [configured source]

---

## Summary Dashboard

| Metric | Count | % of Total |
|--------|-------|------------|
| Total customers | | 100% |
| Advanced deployers (3+ features) | | |
| Monthly active (MAU) | | |
| Weekly active (WAU) | | |
| Inactive (no usage in 30 days) | | |

---

## Customer Roster

| # | Customer | Features Used | Deployment Depth | Last Active | MAU | WAU | Status |
|---|----------|--------------|-----------------|-------------|-----|-----|--------|
| 1 | | | | | Yes/No | Yes/No | Active / At Risk / Inactive |

**Status definitions:**
- **Active**: Used the product in the past 7 days
- **At Risk**: Used in the past 30 days but not in the past 7 days
- **Inactive**: No usage in 30+ days

---

## Feature Adoption

| # | Feature | Customers Using | Adoption Rate | Trend |
|---|---------|----------------|---------------|-------|
| 1 | | | | |

---

## Deployment Depth Distribution

| Features Used | Customers | % of Total |
|---------------|-----------|------------|
| 1 feature | | |
| 2 features | | |
| 3 features | | |
| 4 features | | |
| 5+ features | | |

---

## Usage Trends

### Month-over-Month

| Metric | This Month | Last Month | Change |
|--------|-----------|------------|--------|
| MAU | | | |
| WAU | | | |
| Advanced deployers | | | |
| Avg features per customer | | | |

### Engagement Segments

| Segment | Count | Description |
|---------|-------|-------------|
| Power users | | WAU + 4+ features |
| Regular users | | MAU + 2-3 features |
| Light users | | MAU + 1 feature |
| At risk | | No usage in 7-30 days |
| Churned | | No usage in 30+ days |

---

## At-Risk Customers

Customers showing declining usage or inactivity:

| # | Customer | Last Active | Features Used | Previous MAU | Risk Signal |
|---|----------|-------------|--------------|-------------|-------------|
| 1 | | | | | Declining usage / Feature drop-off / Inactive |

---

## Recommended Actions

| Priority | Action | Customer(s) | Rationale |
|----------|--------|-------------|-----------|
| 🔴 High | | | |
| 🟡 Medium | | | |
| 🟢 Low | | | |

---

## Methodology

- Data source: [configured source and connection method]
- Reporting period: [date range]
- Feature list: [enumerated features tracked]
- Advanced deployment threshold: [N] features
- Activity windows: WAU = 7 days, MAU = 30 days
- All customer names and data are sourced from [configured data source]
```

## Output Checklist

Before delivering the report, verify:

- [ ] All customers from the data source are included
- [ ] Deployment depth is calculated correctly per customer
- [ ] MAU and WAU classifications match the defined time windows
- [ ] Feature adoption rates add up (each customer counted once per feature)
- [ ] At-risk customers are flagged with specific risk signals
- [ ] Summary metrics match the detailed roster
- [ ] No real customer data is included in example outputs
