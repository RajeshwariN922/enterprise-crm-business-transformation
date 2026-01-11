# As-Is vs To-Be Process (Enterprise CRM Transformation)

## Scope of This Process
This project focuses on a common enterprise scenario:
- Customer/Member/Client requests arrive through multiple channels (email, phone, web form)
- Teams manually route and resolve requests
- Leadership lacks consistent reporting and SLA visibility

---

## As-Is Process (Current State)

### Trigger
A request is received from a customer/client via email/phone/web.

### Current Workflow
1. Request is logged manually (spreadsheet/email inbox/shared mailbox).
2. A coordinator assigns it to a team member based on judgment.
3. The assignee requests missing information via email/phone.
4. Updates are tracked inconsistently across email threads and notes.
5. Escalations happen ad hoc when deadlines are missed.
6. Resolution is communicated back to the customer.
7. Reporting is built manually (weekly/monthly) from scattered sources.

### Pain Points / Root Causes
- Duplicate and inconsistent records (no single source of truth)
- Manual routing causes delays and misassignment
- Limited SLA tracking and poor escalation controls
- High dependency on individuals (tribal knowledge)
- Leadership reporting is delayed and error-prone
- Data quality issues prevent reliable analytics

---

## To-Be Process (Future State)

### Trigger
A request is created as a structured Case/Work Item in Salesforce.

### Future Workflow (Salesforce-enabled)
1. Request is captured via standardized intake (web-to-case/email-to-case/manual entry).
2. Salesforce applies validation rules to ensure minimum required fields.
3. Automated routing assigns the case based on category, priority, geography, or queue rules.
4. SLA timers and milestone tracking drive proactive alerts and escalations.
5. Users collaborate through standardized fields, tasks, and case comments (auditable history).
6. Resolution is logged with a consistent outcome code and closure notes.
7. Dashboards provide real-time visibility into volume, aging, SLA compliance, and bottlenecks.

### Expected Improvements
- Faster routing and reduced cycle time
- Better compliance and auditability (centralized case history)
- Consistent data capture enables analytics and forecasting
- Reduced manual reporting effort
- Clear ownership and standardized escalation paths

---

## Business Rules (Examples)
- Priority is assigned based on request type + business impact.
- A case cannot move to “In Progress” without required fields completed.
- Escalation triggers when a case is within X hours of SLA breach.
- Closure requires an outcome code and resolution summary.

---

## Metrics / KPIs
- Average time to first response
- Average resolution time
- SLA compliance rate
- Case aging (by bucket)
- Reopen rate
- Volume by category / channel
- Backlog by queue / owner

---

## Assumptions and Dependencies
- Users follow a standardized intake process (training required)
- Data migration is phased to reduce operational disruption
- Integration dependencies exist for customer/master data and reporting

---

## What I Would Validate in Discovery (If This Were Real)
- Top 10 request categories and their true routing logic
- Where SLA definitions differ by team or customer segment
- Current sources of truth for customer data
- Common reasons for rework / reopen cases
- Reporting needs by leadership vs frontline teams
