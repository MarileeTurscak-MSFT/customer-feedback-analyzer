# Customer Feedback — Weekly Summary

**Date:** 2026-05-26
**Period Covered:** May 19 – May 25, 2026
**Meetings Analyzed:** 5
**Customers This Week:** Contoso Financial, Northwind Traders, Fabrikam Healthcare, Woodgrove Bank, Tailspin Toys

---

## Coverage Summary

| Meeting | Date | Customer | Transcript | Chat | Notes |
|---------|------|----------|-----------|------|-------|
| Week 3 Check-in | 05-19 | Contoso Financial | ✅ | — | Strong early ROI signal; raised attribution, multi-cloud, and savings-calculation trust issues. |
| Pilot Onboarding | 05-20 | Northwind Traders | ✅ | — | Strong confidence in detection quality; focused on reporting and org mapping gaps. |
| Security & Compliance Review | 05-21 | Fabrikam Healthcare | ✅ | — | Positive on insights, but blocked on approvals and auditability. |
| Week 2 Progress | 05-22 | Woodgrove Bank | ✅ | — | Value expanded into security posture; executive reporting needs surfaced clearly. |
| Noise & Threshold Feedback | 05-23 | Tailspin Toys | ✅ | — | Mixed sentiment driven by alert fatigue and trust concerns around deletion guidance. |

---

## Key Takeaways

- **Stale-resource detection is landing as the core value proposition.** Every meeting validated the underlying problem-solution fit, whether through hard savings (Contoso), better detection quality versus alternatives (Northwind), or security-adjacent wins like orphaned app discovery (Woodgrove).
- **The next barrier is operationalizing value for the business, not proving the analytics.** Multiple customers now need savings explained by department, application, or executive audience rather than by subscription or raw infrastructure detail.
- **Trust must be earned before customers will act on deletion recommendations.** Fabrikam needs CAB approval and audit trails, Tailspin flagged a false-positive “safe to delete” label, and Contoso’s shared-disk bug shows that even small credibility issues can slow expansion.
- **Customers want the product to fit cross-functional workflows.** Finance, engineering, security, and executive stakeholders all need different views, which is driving asks around leadership reports, RBAC, approval workflows, and better prioritization.
- **Expansion pressure is already appearing.** Multi-cloud visibility, smarter grouping, and better alert controls are becoming requirements for broader rollout rather than future nice-to-haves.

---

## Top Trends This Week

| Theme | Summary | Sources |
|-------|---------|---------|
| Detection quality is not the problem | Customers consistently praised stale-resource identification quality and early value discovery. The conversation has moved from “does it work?” to “how do we scale it safely?” | Contoso, Northwind, Fabrikam, Woodgrove |
| Department-level reporting is becoming table stakes | Customers need savings framed around departments, cost centers, or business portfolios to support internal ROI conversations. | Contoso, Northwind |
| Trust and governance gate adoption | Approval steps, audit evidence, and recommendation accuracy all surfaced as blockers to taking action on cleanup suggestions. | Contoso, Fabrikam, Tailspin |
| Reporting must serve non-operators | Executives and finance teams want polished outputs they can consume without logging into the product. | Woodgrove, Fabrikam, Contoso |
| Multi-cloud visibility is required for expansion | Azure-only coverage is useful for pilots but increasingly insufficient for enterprise-wide adoption. | Contoso, Northwind |
| Alert prioritization needs work | Customers want the product to distinguish material savings opportunities from background noise and low-value alerts. | Tailspin, Woodgrove |

---

## Feature Requests

| Request | Priority | Source | Notes |
|---------|----------|--------|-------|
| Department / cost-center attribution | High | Contoso, Northwind | Most consistent reporting ask; needed for finance conversations and departmental ROI proof. |
| Multi-cloud savings view | High | Contoso, Northwind | Azure-only visibility limits adoption for customers with meaningful AWS and GCP spend. |
| Approval workflow before deletion | High | Fabrikam, Woodgrove | Required to safely operationalize recommendations and route actions through governance. |
| Leadership-ready scheduled reports | High | Woodgrove, Fabrikam | Customers want recurring PDF/email outputs that executives can review without product login. |
| Compliance audit trail for deletions | High | Fabrikam | Important for regulated customers that need approval and execution evidence tied to controls. |
| Smart safe-to-delete confidence scoring | High | Tailspin | Customers want stronger risk signals before resources are labeled safe to remove. |
| Configurable alert thresholds | High | Tailspin | Needed to suppress penny-level alerts and focus engineers on meaningful savings opportunities. |
| Tag-based application grouping | Medium | Northwind | Helps align recommendations to application portfolios rather than subscriptions. |
| Historical savings trend dashboard | Medium | Contoso | Customers want progress over time, not just a current-state snapshot. |
| RBAC for savings data | Medium | Woodgrove | Different audiences need different levels of cost and resource detail. |
| Alert batching / digest delivery | Medium | Tailspin | Daily or weekly digests would reduce interruption and make alerting more usable. |

---

## Bugs / Issues Reported

| Issue | Severity | Source | Status |
|-------|----------|--------|--------|
| Savings calculation double-counts shared disks | High | Contoso Financial | Acknowledged |
| Email report formatting breaks in Outlook desktop | Medium | Woodgrove Bank | Open |
| “Safe to delete” badge shown on resources with active network connections | High | Tailspin Toys | Acknowledged |

---

## Pain Points

- **Savings are hard to socialize beyond engineering:** Contoso and Northwind both need departmental or business-facing rollups to justify adoption with finance and leadership.
- **Insight-to-action workflows are incomplete:** Fabrikam cannot operationalize recommendations without approvals and auditability, and Woodgrove wants a safer review path before acting.
- **Trust is fragile when deletion guidance is wrong or unclear:** Contoso’s inflated savings math and Tailspin’s false-positive badge both show how fast confidence can erode.
- **Executives still depend on manual reporting:** Woodgrove and Fabrikam want polished, repeatable outputs rather than screenshots, ad hoc notes, or product logins.
- **Current views do not match how customers organize accountability:** Northwind wants tag-based application grouping, while others want clearer segmentation by function or role.
- **Alert volume can suppress adoption entirely:** Tailspin turned alerts off after the first week because high-volume, low-value notifications overwhelmed the team.

---

## Quotes

> "We burned $1.2 million last year on resources nobody was using. If this tool had existed, we'd have caught it in the first month."
> — Jordan Matthews, Contoso Financial

> "My boss doesn't care about individual VMs. He wants to know: how much did we save this quarter, by department?"
> — Dana Singh, Northwind Traders

> "I love the recommendations, but I can't click 'delete' on a production resource without my change advisory board seeing it first."
> — Chris Ramirez, Fabrikam Healthcare

> "That's not just cost savings — that's attack surface reduction."
> — Jamie Lawson, Woodgrove Bank

> "After the first week we turned off alerts because there were too many. Fix the noise problem and we're all in."
> — Reese Kim, Tailspin Toys

---

## Cross-Cutting Themes

| Theme | Summary |
|-------|---------|
| From detection to deployment | Customers no longer need convincing that stale resources exist; they need safe, repeatable workflows to act on recommendations. |
| Business attribution drives expansion | The product is increasingly judged on whether it can map technical findings to departments, portfolios, and leadership outcomes. |
| Trust is the adoption currency | Recommendation accuracy, defensible savings math, and approval controls determine whether customers will expand usage. |
| Reporting is a product surface, not a nice-to-have | Executive-ready exports, emailed summaries, and audience-specific views are central to how customers share value internally. |
| Prioritization matters as much as discovery | Customers want fewer, smarter, higher-confidence recommendations rather than more raw findings. |

---

## Follow-up Actions

- [ ] **Engineering:** Fix the shared-disk double-counting bug and validate savings math in executive-facing reports.
- [ ] **Product:** Prioritize department/cost-center attribution designs that can also support application-level grouping.
- [ ] **Product + Engineering:** Define an approval workflow pattern with impact preview, auditability, and stronger safe-to-delete confidence controls.
- [ ] **Design:** Prototype leadership-ready PDF/email reports that render correctly in Outlook desktop.
- [ ] **Product:** Refine alerting with configurable thresholds, batching, and clearer prioritization by savings impact.
- [ ] **PM:** Share an updated multi-cloud roadmap with customers who are already constrained by Azure-only coverage.

---

## Gaps & Manual Review Needed

- None. All five meetings had transcripts available, and no manual backfill was required.
