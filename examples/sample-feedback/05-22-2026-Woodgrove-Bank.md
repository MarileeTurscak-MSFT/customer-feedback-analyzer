# Customer Feedback — Woodgrove Bank

**Date:** 2026-05-22  
**Meeting:** AI Cost Analyzer — Week 2 Progress  
**Attendees (Product Team):** Alex Chen, Taylor Brooks  
**Attendees (Customer):** Jamie Lawson (Identity Team Lead), Pat Morrison (CTO Office)  
**Customer Segment:** Enterprise / Financial Services

---

## Summary
Woodgrove's feedback was energetic and outcome-focused, with the conversation broadening beyond cost optimization into security posture. Jamie shared that the team identified **340 orphaned app registrations on day one**, which immediately reframed the value of AI Cost Analyzer as both a savings tool and an attack-surface reduction tool. That dual value proposition clearly resonated with the customer and gives the product a stronger internal story at the bank.

At the same time, Woodgrove highlighted two adoption gaps around communication and access. Pat said the CTO wants a **weekly PDF report** delivered by email without needing to log into the product, because executive consumption today is happening through screenshots pasted into PowerPoint. They also want **role-based access control** so finance users can see savings data while engineering users can work with resource-level detail. The only bug raised was around **Outlook desktop rendering**, where email report tables collapse and become difficult to read.

---

## Key Takeaways
1. **Security-adjacent value is a major differentiator.** Orphaned app registration detection created immediate impact beyond pure cost savings.
2. **Executive reporting is currently too manual.** Leadership wants polished, recurring outputs that do not require product login.
3. **Audience-specific access matters.** Woodgrove wants cost visibility and resource visibility separated by role.
4. **Email presentation quality matters for adoption.** Broken Outlook rendering weakens the usefulness of reports for leadership stakeholders.

---

## Feature Requests
| Request | Priority | Notes |
|---------|----------|-------|
| Automated leadership reports via PDF / email | High | Weekly executive delivery is a direct ask from the CTO office. |
| Role-based access control for savings data | Medium | Finance should see cost outcomes while engineers focus on resources. |
| Approval workflow | High | Customer wants a safer review path before actioning recommendations. |

---

## Bugs / Issues Reported
| Issue | Severity | Notes |
|-------|----------|-------|
| Email report formatting breaks in Outlook desktop | Medium | Tables collapse in desktop Outlook, making leadership reports hard to consume. |

---

## Pain Points
- **No executive reporting without product login:** Leadership currently depends on screenshots and manual presentation prep.
- **Reporting workflow is inefficient:** The CTO office is receiving information secondhand instead of directly.
- **Access model is too broad:** They want more separation between finance audiences and engineering audiences.

---

## Quotes
> "The stale app detection alone justified the cost. We found 340 app registrations that hadn't been used in over a year."
> — Jamie Lawson, Identity Team Lead

> "That's not just cost savings — that's attack surface reduction."
> — Jamie Lawson, Identity Team Lead

---

## Follow-up Actions
- [ ] **Alex Chen:** Create a prototype for leadership-ready PDF export and weekly delivery.
- [ ] **Taylor Brooks:** Investigate the Outlook desktop rendering issue for emailed reports.
- [ ] **Product:** Explore RBAC options that separate savings visibility from technical resource workflows.
