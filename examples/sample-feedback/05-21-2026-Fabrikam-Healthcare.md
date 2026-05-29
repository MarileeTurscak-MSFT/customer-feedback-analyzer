# Customer Feedback — Fabrikam Healthcare

**Date:** 2026-05-21  
**Meeting:** AI Cost Analyzer — Security & Compliance Review  
**Attendees (Product Team):** Sam Rivera, Taylor Brooks  
**Attendees (Customer):** Dr. Avery Nguyen (CISO), Chris Ramirez (Sr. Cloud Engineer)  
**Customer Segment:** Enterprise / Healthcare

---

## Summary
This was a thoughtful, cautious conversation shaped heavily by security and compliance requirements. Fabrikam Healthcare responded positively to the core stale-resource detection capabilities and did not question the usefulness of the recommendations themselves. Chris was especially clear that the product is surfacing value. The issue is not whether the recommendations are good; it is whether the organization has a safe, compliant path to act on them.

The current workflow breaks down at the point of action. Fabrikam cannot operationalize any "safe to delete" recommendation without going through its **Change Advisory Board (CAB)** process first, and they also require a durable **audit trail** for changes that maps back to HIPAA controls. That puts them in a blocked-but-interested category: the product has strong potential, but without approval workflow and deletion auditability, they cannot move from insight to execution in a regulated environment.

---

## Key Takeaways
1. **The recommendation engine is viewed positively.** Fabrikam sees real promise in the stale resource detection and did not raise concerns about the analytical quality.
2. **Approval workflow is a hard requirement, not a nice-to-have.** Any deletion-related action must be routed through CAB before they can adopt the product operationally.
3. **Auditability is essential for compliance.** Fabrikam needs a record of who approved, who executed, and what changed for HIPAA-related controls.
4. **Adoption risk is procedural, not conceptual.** The product is aligned with their needs, but blocked by governance gaps.

---

## Feature Requests
| Request | Priority | Notes |
|---------|----------|-------|
| Human approval workflow before deletion | High | Required to fit existing CAB process before any cleanup action. |
| Compliance audit trail for deletions | High | Must support HIPAA-oriented review and evidence gathering. |
| Scheduled leadership reports | Medium | Helpful for communicating progress to security and operations leadership. |

---

## Bugs / Issues Reported
No bugs reported this session.

---

## Pain Points
- **Can't use deletion recommendations without approval chain:** Current product flow assumes faster action than their governance process allows.
- **No audit trail for HIPAA compliance:** They need evidence of approvals and resource changes for internal and external review.
- **Execution gap despite strong insights:** Recommendations are useful, but operationally stranded without workflow support.

---

## Quotes
> "I love the recommendations, but I can't click 'delete' on a production resource without my change advisory board seeing it first."
> — Chris Ramirez, Sr. Cloud Engineer

> "We need an audit trail that maps to our HIPAA controls."
> — Dr. Avery Nguyen, CISO

---

## Follow-up Actions
- [ ] **Sam Rivera:** Schedule a deeper session on approval workflow requirements and current product gaps.
- [ ] **Taylor Brooks:** Map Fabrikam's CAB process end-to-end and identify likely workflow checkpoints.
- [ ] **Product:** Evaluate audit trail requirements against healthcare compliance use cases.
