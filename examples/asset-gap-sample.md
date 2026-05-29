# Asset Gap Report: AI Cost Analyzer

**Report date:** 2026-05-29
**Reporting period:** 2026-04-29 — 2026-05-29
**Feedback sources reviewed:** cumulative-report-sample.md, weekly-report-sample.md

---

## Summary

| Metric | Count |
|--------|-------|
| Total asset gaps identified | 16 |
| 🔴 Missing | 7 |
| 🟡 In Progress | 3 |
| 🔵 Exists but inadequate | 3 |
| 🟣 Discoverability issue | 2 |
| ✅ Resolved (this period) | 1 |

**Top friction area:** Onboarding & initial setup

---

## Asset Gaps by Category

### Documentation

| # | Gap | Topic Area | Customers Mentioning | Impact | Status | Owner | Notes |
|---|-----|-----------|---------------------|--------|--------|-------|-------|
| 1 | GCP setup and configuration guide | Multi-cloud setup | 3 | 🔴 High | 🔴 Missing | — | Customers assume Azure-like flow; GCP auth is different |
| 2 | Service principal permissions reference | Security / Auth | 2 | 🔴 High | 🔴 Missing | — | Customers don't know which permissions to grant |
| 3 | Troubleshooting guide for scan failures | Operations | 2 | 🟡 Med | 🟡 In Progress | — | Draft exists, needs silent failure scenarios |
| 4 | Cost calculation methodology explainer | Trust / Transparency | 1 | 🟡 Med | 🔴 Missing | — | Customer questioned savings estimates |

### Videos

| # | Gap | Topic Area | Customers Mentioning | Impact | Status | Owner | Notes |
|---|-----|-----------|---------------------|--------|--------|-------|-------|
| 1 | Getting started walkthrough (< 5 min) | Onboarding | 4 | 🔴 High | 🔴 Missing | — | Most-requested content format |
| 2 | Dashboard features tour | Product awareness | 2 | 🟡 Med | 🟡 In Progress | — | Script drafted, recording scheduled |
| 3 | Multi-cloud scanning setup | Multi-cloud | 2 | 🟡 Med | 🔴 Missing | — | Depends on GCP docs being written first |

### Labs / Tutorials

| # | Gap | Topic Area | Customers Mentioning | Impact | Status | Owner | Notes |
|---|-----|-----------|---------------------|--------|--------|-------|-------|
| 1 | Hands-on lab: "Find $10K in waste in 30 minutes" | Onboarding / Value | 3 | 🔴 High | 🔴 Missing | — | Would accelerate time-to-value dramatically |
| 2 | Tutorial: Custom tagging rules | Advanced config | 2 | 🟡 Med | 🔴 Missing | — | Customers building workarounds without guidance |

### Sample Code / Reference Architectures

| # | Gap | Topic Area | Customers Mentioning | Impact | Status | Owner | Notes |
|---|-----|-----------|---------------------|--------|--------|-------|-------|
| 1 | API integration sample (Python/PowerShell) | Automation | 2 | 🟡 Med | 🟡 In Progress | — | Python sample in PR review |
| 2 | Terraform module for scheduled scans | IaC | 1 | 🟢 Low | 🔴 Missing | — | Feature request from infrastructure teams |

### Marketing / Product Awareness

| # | Gap | Topic Area | Customers Mentioning | Impact | Status | Owner | Notes |
|---|-----|-----------|---------------------|--------|--------|-------|-------|
| 1 | Feature comparison: AI Cost Analyzer vs. native tools | Competitive positioning | 3 | 🟡 Med | 🔵 Exists but inadequate | — | Current comparison misses recent Azure Cost Mgmt updates |
| 2 | Customer success story / case study | Social proof | 1 | 🟢 Low | 🔵 Exists but inadequate | — | Existing case study is 8 months old |

### FAQs / Comparison Guides

| # | Gap | Topic Area | Customers Mentioning | Impact | Status | Owner | Notes |
|---|-----|-----------|---------------------|--------|--------|-------|-------|
| 1 | "What counts as stale?" definition page | Core concept | 4 | 🔴 High | 🔵 Exists but inadequate | — | Current docs mention it but don't define thresholds or logic |
| 2 | FAQ: Reserved instances, savings plans, spot pricing | Pricing concepts | 2 | 🟡 Med | 🟣 Discoverability issue | — | Exists in blog post but not linked from docs |

---

## Friction Hotspots

| # | Area | Gaps | Combined Impact | Root Cause |
|---|------|------|----------------|------------|
| 1 | Onboarding & first scan | 4 (GCP docs, getting started video, hands-on lab, permissions ref) | 🔴 Critical | New users hit a wall — no video, no lab, incomplete docs for non-Azure clouds |
| 2 | Understanding cost recommendations | 3 (methodology explainer, "what counts as stale", reserved instance FAQ) | 🟡 High | Customers don't trust recommendations they can't verify. Erodes confidence. |
| 3 | Multi-cloud setup | 3 (GCP docs, multi-cloud video, AWS parity docs) | 🟡 High | Non-Azure users feel like afterthoughts. Creates churn risk. |

---

## Discoverability Issues

| # | Asset | Location | Problem | Recommended Fix |
|---|-------|----------|---------|----------------|
| 1 | Reserved instance pricing FAQ | Company blog (Feb 2026 post) | Not linked from product docs or dashboard | Add link to docs sidebar + tooltip in dashboard |
| 2 | API rate limiting guidance | GitHub wiki page | Not findable via docs site search | Move to main docs site, add to API reference section |

---

## Recently Resolved

| # | Gap | Asset Created/Updated | Date | Link |
|---|-----|----------------------|------|------|
| 1 | Azure setup quickstart | Updated getting-started doc with screenshots | 2026-05-10 | /docs/quickstart-azure.md |

---

## Recommended Actions

| Priority | Action | Category | Impact | Effort |
|----------|--------|----------|--------|--------|
| 🔴 High | Create 5-min getting started video | Video | Unblocks onboarding for visual learners | Medium |
| 🔴 High | Write GCP setup guide | Docs | Unblocks multi-cloud customers | Medium |
| 🔴 High | Define "what counts as stale" with thresholds | Docs/FAQ | Builds trust in recommendations | Quick win |
| 🔴 High | Build "Find $10K in waste" hands-on lab | Lab | Accelerates time-to-value | Large |
| 🟡 Medium | Publish service principal permissions reference | Docs | Reduces support tickets on auth | Quick win |
| 🟡 Medium | Link reserved instance FAQ from docs + dashboard | Discoverability | Zero-effort content, just needs linking | Quick win |
| 🟡 Medium | Update competitive comparison page | Marketing | Current version is stale | Medium |
| 🟢 Low | Create Terraform module sample | Sample code | Serves infrastructure-as-code users | Medium |

---

## Methodology

- Feedback sources: cumulative-report-sample.md (all-time), weekly-report-sample.md (week of 2026-05-19)
- Signal detection: Scanned for how-to questions, confusion indicators, "I couldn't find" phrases, repeated topic questions, and explicit asset requests
- Asset inventory: Cross-referenced against docs site table of contents and known blog posts
- Impact scoring: Based on customer mention frequency and friction severity (blocking vs. inconvenient)
- **Note:** This is a sample report using fictional data for demonstration purposes
