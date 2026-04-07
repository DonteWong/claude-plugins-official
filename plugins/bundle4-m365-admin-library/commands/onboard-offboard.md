# IT Onboarding & Offboarding Checklists

## Description

Generates tenant-specific, role-based checklists for hiring, transfers, and departures. Output includes Day 1 provisioning, M365 setup, account cleanup, licensing alignment, and compliance verification. Perfect for ensuring consistent, audit-ready user lifecycle management.

**Use this command when**:
- Formalizing onboarding procedures for new hires or transfers.
- Ensuring offboarding compliance (data retention, access cleanup, account preservation for litigation).
- Scaling HR-IT coordination across growing teams.
- Preparing for compliance audits (user access controls, account lifecycle).
- Building templates for different user types (employee, contractor, vendor, external partner).

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<tenant_size>User count (e.g., "100–250 users", "500–1000 users")</tenant_size>

<licensed_skus>Default licensing (e.g., "E5 for employees, E3 for contractors", "All E3")</licensed_skus>

<user_types>Roles to onboard/offboard (e.g., "Employee (Full-time)", "Contractor", "Executive", "Vendor/Partner", "Consultant")</user_types>

<compliance_frameworks>Applicable regulations (e.g., "SOC 2, HIPAA, GDPR, NIST")</compliance_frameworks>

<data_residency_requirement>Data sovereignty needs (e.g., "EU only (GDPR)", "No restrictions", "US only")</data_residency_requirement>

<process_automation_level>Desired automation (e.g., "Manual checklist", "Partially automated (Power Automate)", "Fully automated")</process_automation_level>
```

---

## Command Invocation

```
/onboard-offboard --tenant "Acme Corp" --size "250 users" --licenses "E5 standard, E3 contractors" --user-types "Employee, Contractor, Executive, Vendor" --compliance "SOC 2, HIPAA" --residency "EU/US split" --automation "Partially automated"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate onboarding and offboarding checklists.

**Context**:
- Tenant: <tenant_name>, <tenant_size>
- Default licenses: <licensed_skus>
- User types: <user_types>
- Compliance: <compliance_frameworks>
- Data residency: <data_residency_requirement>
- Automation: <process_automation_level>

**Output Structure**:

1. **Overview & Process Flow**
   - High-level onboarding and offboarding workflows (swimlane diagrams if helpful).
   - Stakeholders and their roles (HR, IT Admin, Manager, Facilities, etc.).
   - Timeline expectations (Day 1 activities, first week, first month).
   - Automation opportunities (Power Automate flows for provision/deprov).

2. **Onboarding Checklist — Employee (New Hire)**

   **Pre-Day 1 (Before start date)**
   - [ ] Receive hire approval from HR with role, department, manager name.
   - [ ] Create user in Azure AD (UPN: firstname.lastname@tenant.com).
   - [ ] Assign M365 license (default: E5; note any exceptions).
   - [ ] Create Exchange mailbox (auto-provision with AAD user).
   - [ ] Create Teams account (auto-provision with AAD user).
   - [ ] Add user to security groups (by department/role).
   - [ ] Create OneDrive account (auto-provision with AAD user).
   - [ ] Assign Intune device enrollment (default policy or role-specific).
   - [ ] Send welcome email (templated, from IT Ops with setup instructions).

   **Day 1 Activities**
   - [ ] New hire receives laptop/mobile device (inventory tracking).
   - [ ] Device enrolls in Intune (user-driven, guided).
   - [ ] User changes password (enforced on first login).
   - [ ] Enable MFA (Authenticator app, phone, FIDO2 key).
   - [ ] Access to manager's shared OneNote/planner added (manager coordinates).
   - [ ] Verification: User can send/receive email, access Teams.

   **First Week**
   - [ ] Department shared drives access (add to appropriate groups).
   - [ ] Role-specific app access (Power BI, project management tools, etc.).
   - [ ] Manager creates recurring 1:1 in Teams/calendar.
   - [ ] IT security training (password management, phishing awareness, MFA).
   - [ ] Verification: User has all necessary applications.

   **First Month**
   - [ ] VPN/remote access provisioned (if applicable).
   - [ ] Role-specific Intune policies applied (if needed).
   - [ ] Contractor/vendor agreements signed (if applicable).
   - [ ] Compliance acknowledgments (acceptable use, data protection).
   - [ ] 30-day follow-up: User satisfaction, technical issues, access gaps.

   **Compliance & Audit Trail**
   - [ ] Provisioning log created (date, owner, licensing, groups assigned).
   - [ ] Approval documented (hire request, license approval).
   - [ ] User identity verification completed.

3. **Onboarding Checklist — Contractor/Vendor**

   **Pre-Onboarding**
   - [ ] Contractor agreement signed (IT security clauses, data protection, NDA).
   - [ ] Determine access scope (guest user vs. member, data/apps allowed).
   - [ ] Determine license level (often E1 or F1, not E5).
   - [ ] Determine access duration (end date for auto-deprovision).

   **Onboarding (B2B Guest or Licensed User)**
   - [ ] If guest user:
     - [ ] Create B2B guest invite (send invite email to contractor's email).
     - [ ] Guest accepts, registers in Azure AD.
     - [ ] Add to resource groups only (not global distribution lists).
   - [ ] If licensed user (contractor long-term):
     - [ ] Create user account (similar to employee, but with contractor license).
     - [ ] Add "contractor" tag or custom attribute for tracking.
   - [ ] Assign specific resource access (Teams channel, SharePoint site, etc., not all org defaults).
   - [ ] MFA enforcement (same as employees).
   - [ ] Device compliance (if accessing from corporate device; contractors often use personal devices).
   - [ ] Set account expiration date (e.g., contract end date + 30 days for data preservation).

   **Compliance**
   - [ ] Contractor marked as "Guest" or "Contractor" in Azure AD (for easy identification).
   - [ ] Contractor agreement stored in compliance file.
   - [ ] Audit log note: Contractor access reason, duration, approver.

4. **Onboarding Checklist — Executive/C-Suite**

   **Special Considerations**
   - [ ] Executive license: E5 + advanced Defender features (if available).
   - [ ] Priority support (white-glove setup, dedicated IT contact).
   - [ ] Calendar management: Assistant's account may manage exec's calendar (shared mailbox setup).
   - [ ] Privileged access: If exec has IT/admin duties, add to appropriate admin groups with MFA enforcement.
   - [ ] Security briefing: Custom session on phishing/social engineering risks (executives targeted more).
   - [ ] Device setup: Secure mobile device enrollment, strong encryption.

   **Compliance & Audit**
   - [ ] Executive added to VIP/executive group for monitoring and alerts.

5. **Offboarding Checklist — Employee Departure**

   **Departure Notice (2 Weeks Before)**
   - [ ] HR notifies IT with departure date and reason (retirement, termination, transfer, etc.).
   - [ ] Determine data handling: Preserve email/files, transfer to manager, delete, archive.
   - [ ] Identify contractor/vendor systems (VPN, GitHub, etc.) to disable.

   **Last Day of Employment**
   - [ ] Retrieve corporate equipment (laptop, phone, badge, keys).
   - [ ] Disable physical access (badge, building access).
   - [ ] Disable VPN/remote access immediately.
   - [ ] Export user's email (if needed for data preservation/litigation).
   - [ ] Convert email to shared mailbox OR archive (manager/successor gets access).
   - [ ] Transfer OneDrive files (owner's manager or successor, audit logged).
   - [ ] Remove from Teams channels (except archive channel for continuity).
   - [ ] Disable Teams calling.

   **Immediate Post-Departure (Same Day)**
   - [ ] Reset password (employee no longer has access).
   - [ ] Disable MFA/Authenticator (employee can't use).
   - [ ] Disable cloud access in Conditional Access if applicable (block legacy account).
   - [ ] Remove from active security groups (but keep audit/archive groups).
   - [ ] Verify: User cannot send emails, access Teams, or sign into M365.

   **Post-Departure (Next Business Day)**
   - [ ] Manager confirms all work items transferred or closed.
   - [ ] Finance disables Dynamics/ERP access (if applicable).
   - [ ] Remove from distribution lists (all except legal hold groups).
   - [ ] Schedule mailbox archive (e.g., 90 days out) if not preserved for legal.

   **Post-Departure (30 Days)**
   - [ ] Audit departing user's file access (ensure no residual permissions).
   - [ ] Delete OneDrive if not transferred (retention policy applies).
   - [ ] Deactivate license (if preservation/archive complete).
   - [ ] Remove user from external/vendor systems (SaaS apps, client portals).

   **Long-Term (6–12 Months)**
   - [ ] Delete or archive user account (per retention policy/legal hold).
   - [ ] Verify no residual access or data leakage.
   - [ ] Document closure in compliance log.

   **Compliance & Audit Trail**
   - [ ] Offboarding log created (departure date, equipment returned, access disabled timeline).
   - [ ] Data preservation documented (what was kept, why, who has access, until when).
   - [ ] Approval from HR/Legal/Manager.

6. **Transfer/Role Change Checklist**

   **When User Moves to Different Department/Role**
   - [ ] New manager approves new role and required access.
   - [ ] Audit current access (what should be removed vs. kept).
   - [ ] Remove old groups: Previous department, previous role-specific access.
   - [ ] Add new groups: New department, new role-specific access.
   - [ ] Update manager relationship in Azure AD.
   - [ ] Update job title and department in Azure AD (user profile).
   - [ ] If promotion involves admin duties: Add to admin groups, enforce MFA on admin account.
   - [ ] Send updated IT access list to user and manager (verification).
   - [ ] Verification: User has new access, old access revoked.

7. **Automation Opportunities**

   **Power Automate Integration**
   - If <process_automation_level> includes automation:
     - [ ] **New Hire Flow**: HR submits form → Creates Azure AD user → Assigns license → Adds to groups → Sends welcome email.
     - [ ] **Offboarding Flow**: Manager submits departure form → Disables account → Transfers mailbox → Removes from groups → Logs to audit.
     - [ ] **Transfer Flow**: Manager submits transfer form → Adds new groups → Removes old groups → Sends confirmation email.

8. **User Communication Templates**

   **Onboarding Welcome Email** (template snippet)
   ```
   Subject: Welcome to [Org]! Your IT Setup Guide

   Hi [First Name],

   Welcome! Here's your M365 setup:
   - Email: [UPN]
   - Teams: Search your name in the Teams client
   - OneDrive: access.microsoft.com/onedrive
   - Share: Your department shared drive (folder name): [path]

   You should have received an invite to join Teams channels and groups. Accept them to get started.

   Need help? Contact IT Support: support@[org].com or Teams: IT Support channel.
   ```

   **Offboarding Notification** (to manager/team)
   ```
   Subject: [User Name] Offboarding — Access Changes on [Date]

   [User] is departing on [Date]. On that date:
   - Email will be transferred to [Manager]
   - Teams access will be removed
   - All shared files are in [Manager's name] OneDrive

   Questions? Contact IT.
   ```

9. **Compliance & Audit Evidence**

   - Checklist completion status (date, owner, sign-off).
   - Approval trail (HR approval, IT sign-off, manager confirmation).
   - Audit logs: User creation, license assignment, group membership changes, email forwarding, account disablement.
   - Data preservation artifacts (email archive, OneDrive transfer confirmation).
   - Legal hold status (if applicable).

10. **Supporting Resources**

    - Links to Intune device enrollment docs.
    - MFA setup guide (user-friendly, step-by-step).
    - Password manager recommendations.
    - IT support contact info and SLA.
    - Azure AD custom attributes used for tracking (contractor, executive, legal hold, etc.).

**Tone**: Operational, checklist-focused, audit-ready.

---

## Sample Output (Teaser)

**Document Title**: IT Onboarding & Offboarding Checklists — Acme Corp

**New Hire Checklist (Employee)**
- [ ] Pre-Day 1: Create Azure AD user (DONE)
- [ ] Pre-Day 1: Assign E5 license (IN PROGRESS)
- [ ] Day 1: Verify email access (PENDING)
- [ ] Day 1: Enable MFA (PENDING)
- [ ] First week: Add to department groups (PENDING)

**Offboarding Checklist (Employee)**
- [ ] Departure notice received (Date: 2026-04-15)
- [ ] Manager identified successor for files (PENDING)
- [ ] Last day: Disable VPN access (PENDING)
- [ ] Last day: Convert email to shared mailbox (PENDING)
- [ ] Post-departure: Delete OneDrive (scheduled for 30 days)

---

## Related Commands

- `/flow-docs` — Automate onboarding/offboarding flows with Power Automate documentation.
- `/intune-policy` — Ensure new devices enroll and receive compliance policies automatically.
- `/conditional-access` — Add new hires to appropriate risk-based access policies.

---

## Tips

- **HR-IT coordination**: Establish clear communication (email, shared form) for onboarding/offboarding triggers.
- **Contractor tracking**: Use Azure AD custom attributes to easily filter contractors vs. employees for audits.
- **Data preservation**: Clarify with Legal/HR: preserve emails forever? Archive? Delete immediately? Different policies by role (executive vs. IC)?
- **Offboarding speed**: Disabling access should happen same-day; full cleanup can take weeks.
- **Automated licensing**: Use group-based licensing (Intune or AAD) to auto-assign licenses by department/role.
- **Test your process**: Dry-run onboarding with a test user; dry-run offboarding before first real termination.
