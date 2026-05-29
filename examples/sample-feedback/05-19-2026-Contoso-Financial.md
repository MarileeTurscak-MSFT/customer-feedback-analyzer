# Customer Feedback — Contoso Financial

**Date:** 2026-05-19  
**Meeting:** AI Cost Analyzer — Week 3 Check-in  
**Attendees (Product Team):** Alex Chen, Sam Rivera  
**Attendees (Customer):** Jordan Matthews (VP Cloud Infrastructure), Casey Park (Cloud FinOps Manager)  
**Customer Segment:** Enterprise / Financial Services

---

## Summary
Contoso Financial came into the week 3 check-in with strong momentum and a noticeably positive tone. The team shared that AI Cost Analyzer has already helped them identify enough stale infrastructure to drive an estimated **$42K/month in savings** after only three weeks of use. Jordan framed the product as something they wish they had a year earlier, especially given the amount of spend that had accumulated in unused cloud resources across the organization.

The conversation quickly shifted from proving value to scaling value. Their biggest ask is better **department-level cost attribution**, because the current subscription-level view is not enough for internal ROI conversations with finance and business unit leaders. They also pushed hard on **multi-cloud support**, noting that Azure-only visibility limits adoption for teams operating across AWS and GCP. Despite the enthusiasm, they reported a credibility issue: savings calculations are currently **double-counting shared disks** attached to multiple VMs, which inflates projected savings and could erode trust if not corrected quickly.

---

## Key Takeaways
1. **The product is already demonstrating meaningful financial impact.** Contoso estimates $42K/month in savings after three weeks, which makes this one of the strongest early success stories in the current customer set.
2. **Attribution is now the main blocker to broader internal adoption.** The team needs to explain savings by department and cost center, not just by technical boundary like subscription.
3. **Multi-cloud support is a strategic requirement.** Azure-only coverage is useful for pilots, but not sufficient for enterprise rollout at Contoso.
4. **Trust in savings estimates must remain high.** The shared-disk double-counting bug is material because it affects executive-facing numbers.

---

## Feature Requests
| Request | Priority | Notes |
|---------|----------|-------|
| Department / cost-center attribution | High | Needed for finance reporting and business-unit ROI conversations. |
| Multi-cloud savings view | High | Customer wants AWS + GCP alongside Azure in a single view. |
| Historical savings trend dashboard | Medium | They want to see trajectory over time, not only current-state savings. |

---

## Bugs / Issues Reported
| Issue | Severity | Notes |
|-------|----------|-------|
| Savings calculation double-counts shared disks | High | Shared disks attached to multiple VMs are inflating projected savings totals. |

---

## Pain Points
- **No department-level ROI reporting:** Current views do not help the team explain value to finance or line-of-business leaders.
- **Single-cloud limitation:** Azure-only coverage leaves major blind spots for teams also running AWS and GCP.
- **Confidence risk from inflated estimates:** Even one obvious calculation issue can reduce trust in the broader recommendation set.

---

## Quotes
> "We burned $1.2 million last year on resources nobody was using. If this tool had existed, we'd have caught it in the first month."
> — Jordan Matthews, VP Cloud Infrastructure

> "Show me the trajectory, not just a snapshot."
> — Casey Park, Cloud FinOps Manager

---

## Follow-up Actions
- [ ] **Alex Chen:** Share department-attribution mockups with the Contoso team.
- [ ] **Sam Rivera:** Send a preview of the multi-cloud roadmap, including current thinking on AWS and GCP coverage.
- [ ] **Engineering:** Triage and fix the shared-disk double-counting bug in savings calculations.
