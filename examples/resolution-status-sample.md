# Resolution Status Report: AI Cost Analyzer

**Report date:** 2026-05-29
**Reporting period:** 2026-04-29 — 2026-05-29
**Issue tracker:** Azure DevOps (CostAnalyzer project)
**Feedback sources reviewed:** cumulative-report-sample.md, weekly-report-sample.md

---

## Summary Dashboard

| Metric | Count |
|--------|-------|
| Total customer-reported items | 22 |
| ✅ Resolved / Fixed | 7 |
| 🗺️ On Roadmap | 5 |
| 📋 Backlogged | 4 |
| ⏳ Open / Untriaged | 3 |
| ⚠️ No work item found | 3 |

**Resolution rate:** 32%
**Roadmap coverage:** 55%

---

## Recently Resolved

| # | Issue | Type | Reported By | Resolved Date | Work Item | Notes |
|---|-------|------|-------------|---------------|-----------|-------|
| 1 | Dashboard timeout on 10k+ resources | Bug | Contoso Financial | 2026-05-15 | AB#4821 | Pagination added to resource loading |
| 2 | CSV export truncates long resource names | Bug | Woodgrove Bank | 2026-05-08 | AB#4756 | Character limit increased to 256 |
| 3 | Duplicate entries after re-scan | Bug | Tailspin Toys | 2026-05-20 | AB#4830 | Deduplication logic added to scan pipeline |
| 4 | Add cost trend sparklines to dashboard | Feature | Northwind Traders | 2026-05-12 | AB#4689 | 7-day and 30-day sparklines now available |
| 5 | Support tagging resources as "keep" | Feature | Fabrikam Healthcare | 2026-05-18 | AB#4790 | Exclusion tags prevent false positives |
| 6 | Improve scan completion notifications | Feature | Contoso Financial | 2026-05-03 | AB#4701 | Email + webhook notifications added |
| 7 | Fix incorrect savings estimate for reserved instances | Bug | Woodgrove Bank | 2026-05-22 | AB#4845 | Reserved instance pricing now excluded |

### Customer Impact

- **Dashboard timeout on 10k+ resources**: Enterprise customers with large accounts can now load the full dashboard in under 5 seconds. Contoso Financial confirmed the fix resolved their blocking issue.
- **CSV export truncation**: Woodgrove Bank's naming convention (avg 80 characters) now exports cleanly. No more manual corrections.
- **Duplicate entries after re-scan**: Tailspin Toys no longer needs to clear cache before re-scanning. Saves ~15 minutes per scan cycle.
- **Cost trend sparklines**: Northwind Traders uses these in their weekly FinOps reviews. Most-requested dashboard feature.
- **"Keep" tagging**: Fabrikam Healthcare's dev/test environments are no longer flagged as stale. Eliminated their #1 false positive source.
- **Scan notifications**: Contoso Financial's ops team now gets Slack alerts when scans complete instead of polling the dashboard.
- **Reserved instance savings**: Woodgrove Bank's savings estimates dropped from an inflated $180K to an accurate $142K. Builds trust in recommendations.

---

## On the Roadmap

| # | Issue | Type | Priority | Target Release | Work Item | Status |
|---|-------|------|----------|----------------|-----------|--------|
| 1 | Slack/Teams alert integration | Feature | P1 | v2.4 (June) | AB#4860 | In Progress |
| 2 | AWS multi-account scanning parity | Feature | P1 | v2.5 (July) | AB#4712 | In Progress |
| 3 | Scheduled PDF reports for executives | Feature | P2 | v2.4 (June) | AB#4875 | Planned |
| 4 | GCP cost projection chart fix | Bug | P1 | v2.4 (June) | AB#4833 | In Progress |
| 5 | Terraform/IaC state comparison | Feature | P2 | v2.6 (Aug) | AB#4890 | Planned |

---

## Backlogged

| # | Issue | Type | Requested By | Times Mentioned | Work Item | Notes |
|---|-------|------|--------------|-----------------|-----------|-------|
| 1 | Custom tagging schema support | Feature | Woodgrove Bank, Contoso | 3 | AB#4805 | Needs design review for arbitrary tag schemas |
| 2 | Multi-currency display | Feature | Northwind Traders | 2 | AB#4810 | Low effort but low demand |
| 3 | Role-based dashboard access | Feature | Fabrikam Healthcare | 2 | AB#4822 | Blocked on auth infrastructure upgrade |
| 4 | Historical cost comparison (YoY) | Feature | Contoso Financial | 1 | AB#4840 | Requires data retention policy decision |

---

## Open / Untriaged

| # | Issue | Type | Reported By | Date Reported | Urgency |
|---|-------|------|-------------|---------------|---------|
| 1 | Scan fails silently on expired service principal | Bug | Tailspin Toys | 2026-05-23 | 🔴 High |
| 2 | Dashboard doesn't render on Safari 18 | Bug | Northwind Traders | 2026-05-26 | 🟡 Medium |
| 3 | Request: export to Power BI format | Feature | Contoso Financial | 2026-05-28 | 🟢 Low |

---

## No Work Item Found

| # | Feedback Item | Type | Source Report | Customer(s) | Recommended Action |
|---|--------------|------|---------------|-------------|-------------------|
| 1 | AI recommendations feel generic | Pain Point | Weekly 05-23 | Fabrikam Healthcare | Create work item — investigate personalization options |
| 2 | Onboarding docs assume Azure CLI expertise | Pain Point | Cumulative | Tailspin Toys, Woodgrove | Create docs improvement work item |
| 3 | Want to compare costs across Azure subscriptions | Feature | Weekly 05-19 | Contoso Financial | Merge with AB#4712 (multi-account parity) |

---

## Trends

### Resolution Velocity
- Items resolved this period: **7**
- Items resolved last period: **4**
- Trend: **↑ Improving** (+75%)

### Top Unresolved Themes

| # | Theme | Open Items | Customers Affected | Oldest Report Date |
|---|-------|------------|-------------------|-------------------|
| 1 | AWS scanning gaps | 2 | 4 | 2026-03-15 |
| 2 | Alerting & notifications | 1 | 3 | 2026-04-02 |
| 3 | GCP support | 2 | 2 | 2026-04-18 |

### Aging Items

| # | Issue | Type | Days Open | Status | Work Item |
|---|-------|------|-----------|--------|-----------|
| 1 | AWS multi-account scanning parity | Feature | 75 | On Roadmap | AB#4712 |
| 2 | Slack/Teams alert integration | Feature | 57 | On Roadmap | AB#4860 |
| 3 | Custom tagging schema support | Feature | 45 | Backlogged | AB#4805 |

---

## Recommended Follow-ups

| Priority | Action | Rationale |
|----------|--------|-----------|
| 🔴 High | Triage the silent scan failure (expired SP) | Customer-impacting bug, data integrity risk |
| 🔴 High | Create work items for the 3 untracked feedback items | Customer feedback is being lost |
| 🟡 Medium | Communicate resolved items to affected customers | Close the loop — customers should know their feedback drove changes |
| 🟡 Medium | Prioritize Safari rendering bug before next release | Northwind Traders is a key account |
| 🟢 Low | Review backlogged items for quick wins | Multi-currency display is low effort and would delight international customers |

---

## Methodology

- Feedback sources: cumulative-report-sample.md (all-time), weekly-report-sample.md (week of 2026-05-19)
- Issue tracker: Azure DevOps, CostAnalyzer project, queried via WIQL
- Status mapping: New → Open, Active/In Progress → On Roadmap, Resolved/Closed → Fixed, Backlog → Backlogged
- Matching: Keyword + tag matching between feedback items and work items
- Items with no match were flagged for manual review
- **Note:** This is a sample report using fictional data for demonstration purposes
