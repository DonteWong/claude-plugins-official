# Power Automate Flow Documentation

## Description

Generates comprehensive runbooks and architecture documentation for critical Power Automate flows. Output includes flow inventory, trigger/action mapping, data flow diagrams, troubleshooting guides, and disaster recovery procedures. Perfect for knowledge transfer, compliance audits, and runbook automation.

**Use this command when**:
- Documenting mission-critical automation flows for your organization.
- Handing off flows to another team or contractor.
- Preparing flows for compliance review (audit trails, change control).
- Building a runbook library for support teams.
- Designing disaster recovery and failover strategies for automated processes.

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<flow_type>Type of flow (e.g., "Cloud flow (Automated, Instant, Scheduled)", "Desktop flow (RPA)")</flow_type>

<flow_purpose>What the flow does (e.g., "Provision user accounts in M365 and onboarding systems", "Escalate Defender alerts to ServiceNow", "Sync data from SharePoint to SQL database")</flow_purpose>

<trigger_source>What triggers the flow (e.g., "When an item is created/modified in SharePoint", "When an email arrives", "Manual trigger", "Scheduled hourly")</trigger_source>

<critical_actions>Key actions the flow takes (e.g., "Creates user in AAD, licenses in M365, sends welcome email, creates Slack channel")</critical_actions>

<dependencies>Systems & connectors involved (e.g., "Azure AD, Exchange Online, SharePoint, Teams, ServiceNow")</dependencies>

<current_state>Existing flow state (e.g., "None documented", "Existing flow without runbook")</current_state>
```

---

## Command Invocation

```
/flow-docs --tenant "Acme Corp" --flow-type "Cloud flow (Automated)" --purpose "Provision new users to M365 + onboarding systems" --trigger "When user created in AAD" --actions "Create account, assign licenses, send welcome email" --dependencies "Azure AD, Exchange, Teams, ServiceNow, Slack" --state "Existing flow"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate Power Automate flow documentation and runbook.

**Context**:
- Tenant: <tenant_name>
- Flow type: <flow_type>
- Purpose: <flow_purpose>
- Trigger: <trigger_source>
- Key actions: <critical_actions>
- Dependencies: <dependencies>
- Current state: <current_state>

**Output Structure**:

1. **Flow Overview & Business Purpose**
   - What problem does this flow solve?
   - Business value (time saved, error reduction, compliance benefit).
   - Criticality level (tier 1 mission-critical, tier 2 important, tier 3 nice-to-have).
   - SLA expectations (response time, availability, error tolerance).

2. **Flow Architecture Diagram (ASCII or Description)**
   - High-level flow (trigger → actions → outputs).
   - Major decision points (conditions, branches).
   - External system integrations (connectors, APIs).
   - Data flow and transformation logic.

3. **Detailed Flow Walkthrough**
   - Trigger: How is the flow initiated (event, schedule, manual)?
   - Actions: Step-by-step description of each action.
     - Action name, connector, inputs, outputs.
     - Transformation/expression logic (if complex).
     - Error handling (try-catch, approval gates, rollback).
   - Success/failure paths and notifications.

4. **Connector & API Reference**
   - List all connectors used (Azure AD, Exchange, Teams, custom API, etc.).
   - Authentication method (service principal, shared mailbox, user delegation, etc.).
   - Required permissions and licenses.
   - API throttling/rate limits (if applicable).

5. **Data Mapping & Transformation**
   - Input schema (what data triggers the flow).
   - Output schema (what data is produced).
   - Field mapping examples (source → target systems).
   - Expression/JSON logic (if parsing, filtering, or transforming data).

6. **Error Handling & Contingency**
   - What can go wrong (API timeout, permission denied, duplicate data, etc.).
   - Error detection and alerting (email, Teams, webhook).
   - Automated remediation (retry logic, exponential backoff).
   - Manual intervention procedures (when to escalate to IT/admin).

7. **Deployment & Testing Runbook**
   - Pre-deployment checklist (permissions, connectors configured, test data ready).
   - Deployment steps (create flow, publish, scope to users/apps).
   - Testing procedures (unit test scenarios, edge cases).
   - Rollback plan (disable flow, restore previous version).

8. **Monitoring & Alerting**
   - Key metrics to monitor (run count, success rate, execution time).
   - Alert thresholds (e.g., "Alert if >5% of runs fail").
   - Dashboards or reports (Power Automate Analytics, custom Power BI).
   - Escalation procedures (to IT, to business owner, to external support).

9. **Troubleshooting Guide**
   - Common failure modes and solutions.
     - "Flow runs but action X always fails" → Check permissions, API limits, input data.
     - "New user not getting created in system Y" → Validate connector authentication.
   - Debug procedures (run history, action inputs/outputs, expression testing).
   - Escalation contacts and Microsoft Support options.

10. **Change Control & Versioning**
    - How to propose changes (request form, approval gate).
    - Testing and validation (dev/test/prod environments if applicable).
    - Rollback procedures for failed updates.
    - Change log template (track what changed, when, by whom, why).

11. **Disaster Recovery & Failover**
    - How to restore the flow if it's deleted or corrupted.
    - Backup strategy (export flow as package, version control).
    - Failover options (duplicate flow, manual process, alternative automation).
    - RTO/RPO targets (Recovery Time Objective, Recovery Point Objective).

12. **Compliance & Audit Trail**
    - Audit logging (Flow run history, connector usage, data access).
    - Retention policy for logs.
    - Regulatory relevance (if the flow handles PII, PHI, or regulated data).
    - Evidence for compliance auditors.

**Tone**: Detailed, runbook-ready, operationally focused.

---

## Sample Output (Teaser)

**Document Title**: Power Automate Flow Documentation — New User Provisioning

**Flow Name**: M365 New User Provisioning

**Criticality**: Tier 1 (mission-critical; any failure delays onboarding by 1+ day).

**Business Purpose**: Automatically provision new hires in Azure AD, assign M365 licenses, send welcome email, and notify IT Ops.

**Trigger**: When a new user is created in Azure AD (via HR system integration or manual creation).

**Flow Steps**:
1. Trigger: User created in Azure AD
2. Create mailbox in Exchange Online
3. Assign E5 license (with conditional logic: if contractor, assign E3)
4. Create Teams account
5. Send welcome email (templated, from IT Ops)
6. Create entry in ServiceNow (IT ticket for follow-up)
7. Notify IT Ops team (Teams message)

**Dependencies**:
- Azure AD (trigger source, user creation)
- Exchange Online (create mailbox)
- Teams (create account)
- ServiceNow (ticketing)
- Outlook/Office 365 (send email)

**Error Handling**:
- If mailbox creation fails: Send alert to IT Ops, retry after 5 minutes
- If licensing fails: Create manual ticket in ServiceNow, escalate to Licensing admin
- If Teams creation fails: Proceed (Teams can be created manually), but alert IT Ops

**Monitoring**:
- Expected runs: ~5–10 per day
- Expected success rate: >95%
- Alert if: >2 failures in 1 hour OR >20% failure rate

---

## Related Commands

- `/onboard-offboard` — Integrate flow with complete onboarding/offboarding checklist.
- `/security-posture` — Monitor automation impact on access control and data protection.
- `/intune-policy` — Ensure provisioned devices automatically enroll and receive policies.

---

## Tips

- **Expression testing**: Test complex expressions in the Power Automate expression editor before deploying.
- **Throttling**: Power Automate APIs have rate limits. Monitor flow analytics for throttling.
- **Connector authentication**: Service principal auth is more reliable than user delegation; prefer service principal.
- **Variable scope**: Use variables for frequently-used values (tenant name, admin email) to simplify maintenance.
- **Approval gates**: Add approval steps for sensitive operations (licensing high-cost SKUs, deleting data).
- **Scheduling**: Scheduled flows avoid user perception of slowness; run heavy lifting off-hours if possible.
- **Testing environment**: Clone flows to a test environment; test against test tenants before production.
