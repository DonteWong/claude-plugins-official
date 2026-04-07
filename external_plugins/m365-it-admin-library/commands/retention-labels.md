# Purview Retention Label Strategy

## Description

Builds a retention and deletion schedule aligned with regulatory frameworks and organizational needs. Output includes label taxonomy, policy mapping, deployment checklist, and compliance evidence. Covers email, documents, Teams messages, and more across Exchange Online, SharePoint, OneDrive, and Teams.

**Use this command when**:
- Building a new retention and eDiscovery strategy from scratch.
- Preparing for a compliance audit (GDPR, HIPAA, SOX, NIST, etc.).
- Migrating from legacy document management or file plans.
- Implementing records management across M365.
- Automating retention and deletion to reduce manual compliance burden.

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<tenant_size>User count (e.g., "100–250 users", "500–1000 users")</tenant_size>

<licensed_skus>Licensing (e.g., "E3, E5, Purview Premium")</licensed_skus>

<compliance_frameworks>Applicable regulations (e.g., "GDPR, HIPAA, SOX, NIST, CJIS")</compliance_frameworks>

<data_types>Content to manage (e.g., "Email, documents, Teams messages, instant messages, OneDrive files")</data_types>

<workload_scope>M365 workloads (e.g., "Exchange Online, SharePoint Online, OneDrive, Teams, Yammer")</workload_scope>

<records_management_requirement>Whether you need records management (true/false) and what kind (e.g., "Legal hold, regulatory records, department-specific retention")</records_management_requirement>
```

---

## Command Invocation

```
/retention-labels --tenant "Acme Corp" --size "250 users" --licenses "E5, Purview Premium" --compliance "GDPR, HIPAA, SOX" --data-types "Email, docs, Teams" --workloads "Exchange, SharePoint, OneDrive, Teams" --records-mgmt "true"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate a Purview retention label strategy and deployment document.

**Context**:
- Tenant: <tenant_name>, <tenant_size>
- Licenses: <licensed_skus>
- Compliance: <compliance_frameworks>
- Data types: <data_types>
- Workloads: <workload_scope>
- Records management: <records_management_requirement>

**Output Structure**:

1. **Retention & Disposal Strategy Overview**
   - Business drivers (e.g., legal hold, regulatory compliance, cost optimization).
   - Regulatory requirements breakdown (retention periods by framework).
   - High-level label taxonomy and governance model.

2. **Retention Label Taxonomy**
   - List 6–12 retention labels, each with:
     - **Label name**: Descriptive (e.g., "Email: Transient (30 days)", "Financial: Tax Records (7 years)", "Personal: Confidential (Delete on Request)").
     - **Purpose**: Business justification (e.g., "Daily email notifications, not business-critical").
     - **Retention period**: Duration (30 days, 1 year, 7 years, permanent, etc.).
     - **Action after retention**: Delete, retain only, start disposal review, etc.
     - **Applicable workloads**: Which M365 services (Exchange, SharePoint, Teams, etc.).
     - **Applicable content types**: Email, documents, messages, meetings, etc.
     - **License requirement**: Purview standard or premium.
     - **Compliance mapping**: Which frameworks require this label (e.g., "GDPR Article 5 (storage limitation)", "HIPAA §164.312(b) (audit controls)").

3. **Automatic Application Strategy**
   - Condition-based auto-labeling (e.g., "Label as 'Transient' if email contains 'out of office' or 'automated notification'").
   - Department/location-based labeling (SharePoint site retention policies).
   - Sensitivity/classification integration (if using Data Classification).

4. **Portal Navigation & Configuration**
   - Step-by-step creation of labels in Purview Compliance Portal.
   - Retention policy configuration (auto vs. user-applied labels).
   - Publishing and rollout plan.

5. **Compliance Mapping Table**
   - Matrix showing which labels satisfy which regulatory requirements.
   - Evidence for auditors (label definitions, policy configurations, audit logs).

6. **Deployment Roadmap**
   - Phase 1: Core labels (transient, standard retention, records).
   - Phase 2: Auto-application policies (condition-based, location-based).
   - Phase 3: Monitoring and optimization.
   - Effort estimates, stakeholder communication, user training.

7. **User Guidance & Communication**
   - Non-technical summary of what retention labels do (retention ≠ security).
   - When and how to apply labels (manual vs. automatic).
   - What happens when retention expires (delete, disposal review, etc.).
   - FAQ (Can I recover deleted files? What if I don't label something? Can I request an exception?).

8. **Audit & Evidence Trail**
   - Retention logs and audit queries (Advanced Audit, eDiscovery).
   - How to prove compliance with retention policies for auditors.
   - Label application audit trail (who applied what label when).

9. **eDiscovery & Legal Hold Integration** (if applicable)
   - Interaction between retention labels and eDiscovery holds.
   - How to preserve content for litigation while respecting retention schedules.
   - Query examples (Advanced Hunting, eDiscovery searches).

**Tone**: Pragmatic, audit-ready, regulatory-focused.

---

## Sample Output (Teaser)

**Document Title**: Purview Retention Label Strategy — Acme Corp

**Label 1: Email – Transient (30 Days)**
- Applicable to: Transactional email (order confirmations, meeting invites, automated notifications).
- Retention: 30 days from creation.
- Action after retention: Automatically delete.
- Auto-apply rule: Email with keywords "out of office", "automatic reply", "meeting invitation".
- License: Purview (included in E3+).
- Compliance mapping: None specific; reduces storage burden.

**Label 2: Financial – Tax Records (7 Years)**
- Applicable to: Tax documents, financial statements, audit reports, vendor contracts.
- Retention: 7 years from end of fiscal year.
- Action after retention: Dispose (delete after approval).
- Auto-apply rule: Document from Finance department OR contains metadata "category=Financial".
- License: Purview (included in E5; Premium for advanced auto-apply).
- Compliance mapping: SOX §802 (records retention), NIST SP 800-53 AU-11 (audit records).

**Label 3: Personal – Confidential (Delete on Request)**
- Applicable to: Personal/sensitive employee data, medical records, background checks.
- Retention: User-determined (no auto-delete).
- Action after retention: Require manual disposal review.
- Manual application: User or admin applies label in Teams, SharePoint, Outlook.
- License: Purview (included in E3+).
- Compliance mapping: GDPR Article 5 (purpose limitation, storage limitation), HIPAA §164.312(b) (audit controls).

---

## Related Commands

- `/intune-policy` — Ensure devices don't preserve restricted data offline.
- `/security-posture` — Monitor data classification and retention compliance rates.
- `/onboard-offboard` — Ensure offboarded users' data is properly retained/deleted.

---

## Tips

- **Retention ≠ deletion**: Retention policies preserve data for compliance; they don't delete. Users should understand the difference.
- **Auto-apply + manual**: Combine auto-application (reduce burden) with manual labeling (allow exceptions).
- **Litigation hold**: Before deleting large amounts of old data, check with Legal to ensure no active litigation holds.
- **Multi-workload complexity**: Retention policies work differently in Exchange (message-level) vs. SharePoint (document-level). Plan for both.
- **License tiers**: Auto-apply with advanced conditions requires Purview Premium; basic labels come with E3+.
- **eDiscovery integration**: eDiscovery holds override retention policies. Always verify held content when compliance reviewing.
