# Customer Feedback — Tailspin Toys

**Date:** 2026-05-23  
**Meeting:** AI Cost Analyzer — Noise & Threshold Feedback  
**Attendees (Product Team):** Morgan Lee, Sam Rivera  
**Attendees (Customer):** Kai Patel (Platform Engineer), Reese Kim (Cloud Ops Manager)  
**Customer Segment:** Enterprise / Manufacturing

---

## Summary
Tailspin Toys gave the most mixed feedback of the week. The customer still believes the overall concept is right and agrees there is value in finding stale cloud resources, but the current alerting experience is creating too much noise to be usable day to day. Kai said they were receiving more than **200 alerts per day**, many for extremely low-cost idle resources, which made it difficult for engineers to distinguish meaningful recommendations from background chatter.

The concern became more serious when Reese described a near miss involving a resource that showed a **"safe to delete" badge despite active network connections**. That did not result in an incident, but it significantly reduced trust in the recommendation logic. The team turned off alerts after the first week because the volume was overwhelming. Their feedback was constructive but clear: if AI Cost Analyzer can reduce noise, improve confidence scoring, and make alerts easier to batch and prioritize, they would be willing to re-engage.

---

## Key Takeaways
1. **Alert fatigue is suppressing adoption.** High-volume, low-value notifications caused the team to disable alerts entirely.
2. **Prioritization needs to be cost-aware and context-aware.** Tailspin wants the product to distinguish penny-level waste from meaningful savings opportunities.
3. **Safe-to-delete logic needs stronger confidence controls.** A false-positive badge on an actively connected resource created a material trust issue.
4. **The customer is not lost, but patience is limited.** They still like the direction of the product, but execution needs tuning quickly.

---

## Feature Requests
| Request | Priority | Notes |
|---------|----------|-------|
| Configurable alert thresholds | High | Customer wants to suppress low-value alerts below meaningful savings thresholds. |
| Alert batching / digest | Medium | A daily or weekly digest would be easier to consume than individual notifications. |
| Smart "safe to delete" confidence scoring | High | They want recommendations to reflect stronger risk signals before badging resources as safe. |

---

## Bugs / Issues Reported
| Issue | Severity | Notes |
|-------|----------|-------|
| "Safe to delete" badge shown on resources with active network connections | High | Near miss that damaged trust in deletion recommendations. |

---

## Pain Points
- **Alert fatigue drowns out high-value recommendations:** Engineers are spending attention on low-cost noise instead of meaningful cleanup opportunities.
- **Engineers ignore the tool when signal quality drops:** Once notifications became repetitive, the team disengaged.
- **Trust in deletion guidance is fragile:** One risky-looking false positive can outweigh many good recommendations.

---

## Quotes
> "We're getting 200 alerts a day for things that cost pennies. I need this tool to be smarter about what's worth my time."
> — Kai Patel, Platform Engineer

> "After the first week we turned off alerts because there were too many. Fix the noise problem and we're all in."
> — Reese Kim, Cloud Ops Manager

---

## Follow-up Actions
- [ ] **Morgan Lee:** File a feature request for configurable thresholds using Tailspin's concrete alert examples.
- [ ] **Sam Rivera:** Investigate the safe-to-delete logic for resources with active network connections.
- [ ] **Product:** Evaluate batching and digest options to reduce alert fatigue for operations teams.
