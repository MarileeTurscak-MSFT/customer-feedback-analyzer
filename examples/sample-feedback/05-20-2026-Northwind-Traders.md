# Customer Feedback — Northwind Traders

**Date:** 2026-05-20  
**Meeting:** AI Cost Analyzer — Pilot Onboarding  
**Attendees (Product Team):** Alex Chen, Morgan Lee  
**Attendees (Customer):** Dana Singh (Cloud FinOps Manager), Riley Ortiz (Platform Engineering Lead)  
**Customer Segment:** Enterprise / Retail

---

## Summary
Northwind Traders is at the very beginning of their pilot, but the first impression was notably strong. Both Dana and Riley said the stale resource detection quality stood out compared to other tools they have evaluated. Riley specifically called out the accuracy of the findings, which is important because the team has already been burned by noisy optimization tools that create more cleanup work than value.

Most of the discussion centered on reporting and organizational mapping rather than detection quality. Northwind wants to group resources by **application portfolio using tags** and report savings by **department**, not just by subscription. They also emphasized that **multi-cloud visibility** will matter quickly because a large share of their footprint sits in AWS. Today, the team is stitching together spreadsheets to reconcile savings and ownership across environments, and they see AI Cost Analyzer as promising but incomplete until it can support that broader operating model.

---

## Key Takeaways
1. **Detection quality created immediate credibility.** Northwind sees the stale-resource identification as better than competing tools they have tested.
2. **Business reporting matters more than infrastructure-level detail.** The customer needs savings framed in departmental terms for leadership discussions.
3. **Tagging support would improve operational fit.** Grouping by application portfolio is important for how Northwind organizes accountability.
4. **Multi-cloud support will be required for expansion.** With roughly 60% of their environment in AWS, Azure-only value will be limited.

---

## Feature Requests
| Request | Priority | Notes |
|---------|----------|-------|
| Department attribution | High | Needed to show quarterly savings by department instead of by subscription. |
| Tag-based app grouping | Medium | Customer wants grouping by application portfolio using existing tags. |
| Multi-cloud view | High | AWS visibility is especially important due to current footprint mix. |

---

## Bugs / Issues Reported
No bugs reported this session.

---

## Pain Points
- **Can't show per-department ROI:** Leadership wants outcomes by department, not technical subscription boundaries.
- **Manual Excel reconciliation for multi-cloud:** Current process is tedious and makes reporting slow.
- **Limited organizational grouping:** Subscription-level views do not line up well with their application portfolio model.

---

## Quotes
> "My boss doesn't care about individual VMs. He wants to know: how much did we save this quarter, by department?"
> — Dana Singh, Cloud FinOps Manager

> "Best stale resource detection we've tested."
> — Riley Ortiz, Platform Engineering Lead

---

## Follow-up Actions
- [ ] **Morgan Lee:** Schedule a design session focused on tag-based grouping and application portfolio views.
- [ ] **Alex Chen:** Share examples of how other customers are framing savings at the department level.
- [ ] **Product:** Capture Northwind's AWS-heavy footprint in ongoing multi-cloud prioritization.
