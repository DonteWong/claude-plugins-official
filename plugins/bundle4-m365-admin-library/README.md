# M365 IT Admin Prompt Library

**Production-Ready Documentation Generators for Intune, Defender, Entra ID, Purview & More**

Generated with 7 Claude Code commands. Build audit-ready M365 admin documentation in minutes instead of hours.

---

## Table of Contents

1. [Installation](#installation)
2. [Quick Start](#quick-start)
3. [The 7 Commands](#the-7-commands)
4. [Variable Reference](#variable-reference)
5. [Usage Examples](#usage-examples)
6. [Tips & Best Practices](#tips--best-practices)
7. [Troubleshooting](#troubleshooting)
8. [Author & License](#author--license)

---

## Installation

### Option 1: Claude Code (Recommended)

1. Open [Claude Code](https://claude.com) in your browser.
2. Click **Plugins** or navigate to the plugins directory.
3. Search for **"M365 IT Admin Prompt Library"** or visit:
   ```
   https://dontewong.gumroad.com/l/m365-it-admin-library
   ```
4. Click **Install** or **Load Plugin**.
5. Verify installation by running:
   ```
   /intune-policy --help
   ```

### Option 2: Manual Setup

1. Download the plugin files (this folder and subfolders).
2. In Claude Code or your editor, load the skill file:
   ```
   /skills/m365-admin.md
   ```
3. Run any of the 7 commands (see below).

---

## Quick Start

### 30-Second Example

Generate an Intune compliance policy baseline for your organization:

```
/intune-policy \
  --tenant "Acme Corp" \
  --size "250 users" \
  --licenses "E3, E5" \
  --compliance "SOC 2, HIPAA" \
  --platforms "Windows, iOS" \
  --focus "Mobile device security" \
  --deployment "Phased by department"
```

**You get**:
- Policy inventory (3–6 recommended policies)
- Portal navigation (step-by-step in Intune admin center)
- Device groups and targeting
- Compliance alignment (SOC 2, HIPAA controls)
- Deployment roadmap (pilot, rollout, monitoring)

Copy-paste ready. Customize for your environment.

---

## The 7 Commands

### 1. `/intune-policy` — Intune Compliance Policy Builder

**What it does**: Generates comprehensive Intune compliance policies tailored to your tenant configuration.

**When to use**: Building device security baselines, hardening policies for compliance audits, rolling out MAM/MDM.

**Key inputs**:
- Tenant name, size, licensing tier
- Compliance frameworks (SOC 2, HIPAA, etc.)
- Device platforms (Windows, macOS, iOS, Android)
- Primary focus (encryption, app control, etc.)

**Output**:
- Policy inventory by platform
- Portal navigation (Intune admin center steps)
- Compliance alignment (regulatory controls)
- Deployment phases and validation

**Example**:
```
/intune-policy --tenant "North Star Industries" --size "500 users" --licenses "E5" --compliance "HIPAA, CJIS" --platforms "Windows, Android" --focus "Encryption and device restrictions" --deployment "Pilot then full rollout"
```

---

### 2. `/conditional-access` — Conditional Access Explainer & Builder

**What it does**: Documents Conditional Access policies in plain English with risk-based flow diagrams and gap analysis.

**When to use**: Implementing Zero Trust, documenting CA for audits, explaining policies to stakeholders.

**Key inputs**:
- Tenant name, size, licensing tier
- Risk focus (unmanaged devices, external users, legacy auth)
- Target apps (Exchange, SharePoint, Teams, etc.)
- Existing policy count

**Output**:
- CA policy recommendations (5–8 policies)
- Plain English explanations (non-technical summaries)
- Policy flow diagrams (ASCII)
- Gap analysis (missing policies, conflicts)
- Pilot/rollout roadmap

**Example**:
```
/conditional-access --tenant "Acme Corp" --size "100 users" --licenses "E5, Premium P1" --compliance "Zero Trust" --risk-focus "Legacy authentication" --apps "Exchange Online, SharePoint, Teams" --existing "None"
```

---

### 3. `/defender-triage` — Defender Triage Template

**What it does**: Systematically triages Defender alerts and incidents with remediation tracking and compliance correlation.

**When to use**: Responding to alerts, building incident response runbooks, integrating with SIEM.

**Key inputs**:
- Tenant name, size, licensing
- Defender modules active (Endpoint, Office, Cloud App Security, Identity)
- Incident context (phishing, malware, unusual access, etc.)
- SIEM integration (Sentinel, Splunk, etc.)

**Output**:
- Incident severity assessment
- Defender alert triage workflow
- Remediation tracking
- SIEM/ticketing integration format
- Compliance evidence trail

**Example**:
```
/defender-triage --tenant "Acme Corp" --size "250 users" --licenses "E5 + Defender for Identity" --modules "Endpoint, Office, Cloud App Security" --compliance "SOC 2, NIST" --context "Ransomware detected on 3 devices" --siem "Sentinel"
```

---

### 4. `/retention-labels` — Purview Retention Label Strategy

**What it does**: Builds retention and deletion schedules aligned with compliance frameworks (GDPR, HIPAA, SOX, etc.).

**When to use**: Implementing records management, prepping for compliance audits, automating data lifecycle.

**Key inputs**:
- Tenant name, size, licensing
- Compliance frameworks (GDPR, HIPAA, SOX, NIST, etc.)
- Data types (email, documents, Teams messages)
- M365 workloads (Exchange, SharePoint, OneDrive, Teams)
- Records management needs (yes/no)

**Output**:
- Retention label taxonomy (6–12 labels)
- Auto-application rules (condition-based labeling)
- Compliance mapping (labels → regulatory controls)
- Portal navigation (create labels in Purview)
- User guidance (how to apply, what happens)
- eDiscovery & legal hold integration

**Example**:
```
/retention-labels --tenant "FinServ Corp" --size "500 users" --licenses "E5, Purview Premium" --compliance "SOX, NIST, GDPR" --data-types "Email, documents, Teams" --workloads "Exchange, SharePoint, OneDrive, Teams" --records-mgmt "true"
```

---

### 5. `/flow-docs` — Power Automate Flow Documentation

**What it does**: Generates runbooks and architecture documentation for critical automation flows.

**When to use**: Documenting mission-critical flows, handing off to another team, disaster recovery planning.

**Key inputs**:
- Tenant name
- Flow type (cloud flow automated/instant/scheduled, or desktop/RPA)
- Flow purpose (what it does)
- Trigger (what starts it)
- Key actions (what it does)
- Dependencies (systems involved)
- Current state (new or existing)

**Output**:
- Flow overview & business value
- Architecture diagram (ASCII)
- Detailed step-by-step walkthrough
- Connector & API reference
- Data mapping & transformation logic
- Error handling & contingency procedures
- Deployment & testing runbook
- Monitoring & alerting dashboard
- Troubleshooting guide
- Change control & versioning procedures
- Disaster recovery & failover strategy

**Example**:
```
/flow-docs --tenant "Acme Corp" --flow-type "Cloud flow (Automated)" --purpose "Provision new users to M365 + HR systems" --trigger "When user created in Azure AD" --actions "Create mailbox, assign licenses, send welcome email, create ServiceNow ticket" --dependencies "Azure AD, Exchange, Teams, ServiceNow, Slack" --state "Existing flow"
```

---

### 6. `/security-posture` — Security Posture Assessment Report

**What it does**: Synthesizes Defender, Conditional Access, Intune, and Entra ID signals into an executive summary.

**When to use**: Quarterly security reviews, board reporting, compliance audit prep, strategic planning.

**Key inputs**:
- Tenant name, size, licensing
- Compliance frameworks
- Report period (Q1 2026, last 12 months, etc.)
- Prior assessment date (for trend comparison)
- Assessment focus areas

**Output**:
- Executive summary with overall rating
- Security scorecard (identity, endpoint, threats, data, compliance)
- Detailed assessment by domain (Identity, Endpoint, Detection, Data, Compliance)
- Risk matrix with likelihood/impact
- Compliance alignment matrix
- 12-month remediation roadmap (phased priorities)
- Metrics & KPIs to monitor
- Comparison to prior assessment (trends)
- Industry benchmarking (if applicable)
- Audit evidence & artifacts

**Example**:
```
/security-posture --tenant "Acme Corp" --size "250 users" --licenses "E5, Premium P2, Defender for Identity" --compliance "SOC 2, ISO 27001, HIPAA" --period "Q1 2026" --prior "2025-10-01" --focus "Overall posture, incident response, compliance gaps"
```

---

### 7. `/onboard-offboard` — IT Onboarding & Offboarding Checklists

**What it does**: Generates role-based checklists for hiring, transfers, and departures.

**When to use**: Formalizing HR-IT onboarding, offboarding compliance, scaling across teams, audit prep.

**Key inputs**:
- Tenant name, size, licensing
- User types (employee, contractor, executive, vendor, etc.)
- Compliance frameworks
- Data residency requirements
- Automation level (manual, partially automated, fully automated)

**Output**:
- High-level process flows
- **Onboarding checklists** (Pre-Day 1, Day 1, First Week, First Month) for:
  - New Hire (Employee)
  - Contractor/Vendor
  - Executive/C-Suite
- **Offboarding checklist** (Departure notice, Last Day, Post-departure, Long-term)
- **Transfer/Role Change checklist**
- Automation opportunities (Power Automate flows)
- User communication templates (welcome email, offboarding notification)
- Compliance & audit evidence requirements

**Example**:
```
/onboard-offboard --tenant "Acme Corp" --size "250 users" --licenses "E5 standard, E3 contractors" --user-types "Employee, Contractor, Executive, Vendor" --compliance "SOC 2, HIPAA" --residency "EU/US split" --automation "Partially automated"
```

---

## Variable Reference

All commands use these common variables. Provide them as command-line arguments:

### Universal Variables

```
--tenant <name>          Organization name (e.g., "Acme Corp", "North Star Industries")
--size <range>           User count (e.g., "100–250 users", "500–1000 users")
--licenses <list>        M365 licenses (e.g., "E3, E5, Defender for Office standalone")
--compliance <list>      Regulatory frameworks (e.g., "SOC 2, HIPAA, GDPR, ISO 27001, NIST")
```

### Command-Specific Variables

**Intune Policy**:
```
--platforms <list>       Devices (e.g., "Windows, macOS, iOS, Android")
--focus <description>    Policy focus (e.g., "Encryption and device restrictions")
--deployment <strategy>  Rollout approach (e.g., "Pilot group (25 devices)" or "Phased by department")
```

**Conditional Access**:
```
--risk-focus <area>      Primary concern (e.g., "External user access", "Legacy authentication")
--apps <list>            Protected apps (e.g., "Exchange, SharePoint, Teams, Power BI")
--existing <count>       Current CA policies (e.g., "None", "5–10 existing")
```

**Defender Triage**:
```
--modules <list>         Active modules (e.g., "Endpoint, Office, Cloud App Security, Identity")
--context <description>  Incident type (e.g., "Phishing campaign", "Ransomware detection")
--siem <platform>        SIEM integration (e.g., "Sentinel", "Splunk", "None")
```

**Retention Labels**:
```
--data-types <list>      Content (e.g., "Email, documents, Teams messages")
--workloads <list>       M365 services (e.g., "Exchange, SharePoint, OneDrive, Teams")
--records-mgmt <bool>    Records management (e.g., "true" or "false")
```

**Flow Docs**:
```
--flow-type <type>       Flow category (e.g., "Cloud flow (Automated)", "Desktop flow (RPA)")
--purpose <description>  What the flow does
--trigger <description>  What starts the flow
--actions <list>         Key steps
--dependencies <list>    Systems involved
--state <state>          "New" or "Existing flow"
```

**Security Posture**:
```
--period <timeframe>     Review window (e.g., "Q1 2026", "Last 12 months")
--prior <date>           Previous assessment date (e.g., "2025-10-01" for trends)
--focus <areas>          Priority areas (e.g., "Overall posture, incident response, compliance gaps")
```

**Onboarding/Offboarding**:
```
--user-types <list>      Roles (e.g., "Employee, Contractor, Executive, Vendor")
--residency <req>        Data sovereignty (e.g., "EU only (GDPR)", "No restrictions")
--automation <level>     Automation desired (e.g., "Manual", "Partially automated", "Fully automated")
```

---

## Usage Examples

### Example 1: MSP Supporting SMB Clients

You manage 5 SMB tenants (50–100 users each) and need compliance documentation for a SOC 2 audit.

**Command**:
```
/security-posture \
  --tenant "ClientName SMB" \
  --size "75 users" \
  --licenses "E3" \
  --compliance "SOC 2 Type II" \
  --period "Last 12 months" \
  --focus "Overall posture, compliance gaps"
```

**Output**:
- Executive summary of security controls aligned to SOC 2.
- Gaps (e.g., "MFA adoption only 40%"; "No DLP policies").
- 90-day roadmap to close gaps and achieve compliance.

**Next steps**: Use `/intune-policy` and `/conditional-access` to implement missing controls.

---

### Example 2: Onboarding at Scale

Your organization is hiring 20 new employees this quarter. You need a formal, audit-ready onboarding process.

**Command**:
```
/onboard-offboard \
  --tenant "Acme Corp" \
  --size "250 users" \
  --licenses "E5 for employees, E3 for contractors" \
  --user-types "Employee, Contractor, Executive" \
  --compliance "SOC 2, HIPAA" \
  --residency "No restrictions" \
  --automation "Partially automated (Power Automate)"
```

**Output**:
- Role-based onboarding checklists (employee vs. contractor).
- Pre-Day 1, Day 1, First Week, First Month timelines.
- Power Automate flow suggestions (auto-create users, send welcome emails).
- Compliance evidence trail (approval logs, audit trail).

**Next steps**: Implement Power Automate flows using `/flow-docs`. Set up team calendar reminders for each phase.

---

### Example 3: Incident Response

A ransomware alert fires in Defender. You need to triage, document, and respond.

**Command**:
```
/defender-triage \
  --tenant "Acme Corp" \
  --size "250 users" \
  --licenses "E5 + Defender for Identity" \
  --modules "Endpoint, Office, Cloud App Security" \
  --compliance "SOC 2, NIST" \
  --context "Ransomware detected on 3 Windows devices; potential C2 communication" \
  --siem "Sentinel"
```

**Output**:
- Incident severity assessment (Critical, High, Medium, Low).
- Triage workflow (isolate devices, analyze, remediate).
- Remediation checklist (block sender, isolate device, reset credentials, etc.).
- SIEM export format (ingest into Sentinel/Splunk).
- Compliance evidence (incident timeline, remediation trail).

**Next steps**: Follow the triage workflow. Use `/conditional-access` to add risk-based access policies to prevent lateral movement.

---

### Example 4: Records Management Compliance

Your Legal team says: "We need to prove we're managing data retention correctly for GDPR."

**Command**:
```
/retention-labels \
  --tenant "Acme Corp" \
  --size "250 users" \
  --licenses "E5, Purview Premium" \
  --compliance "GDPR, HIPAA" \
  --data-types "Email, documents, Teams messages, OneDrive files" \
  --workloads "Exchange, SharePoint, OneDrive, Teams" \
  --records-mgmt "true"
```

**Output**:
- Retention label taxonomy (personal data, transactional, records, sensitive).
- Auto-application rules (e.g., "Auto-label email as transient if subject contains 'out of office'").
- Compliance mapping (labels → GDPR Article 5 controls).
- Purview portal steps to configure and deploy.
- eDiscovery integration (how legal holds override retention).

**Next steps**: Create labels in Purview (following portal steps). Communicate to users about retention impact. Monitor compliance dashboard quarterly.

---

### Example 5: Device Security Hardening

You're deploying Windows devices to 100 new users and need secure baseline policies.

**Command**:
```
/intune-policy \
  --tenant "Acme Corp" \
  --size "100 users" \
  --licenses "E3" \
  --compliance "NIST SP 800-53" \
  --platforms "Windows 10, Windows 11" \
  --focus "Device encryption, app control, malware protection" \
  --deployment "Pilot with 10 devices, then phased by department"
```

**Output**:
- 4–6 Windows compliance policies (encryption, password, app restrictions, malware).
- Portal navigation (Intune admin center > Devices > Compliance > Create).
- Configuration details (BitLocker algorithm, NIST alignment).
- Pilot rollout plan (timeline, validation, success metrics).
- Device compliance dashboard (monitor real-time compliance rates).

**Next steps**: Pilot with 10 devices. Verify zero false positives. Roll out to full department. Monitor compliance rates in Intune dashboard.

---

## Tips & Best Practices

### 1. Customize Variables for Your Context

Each command generates output tailored to your variables. More specificity = better output.

**Good**:
```
/intune-policy \
  --tenant "Acme Corp Finance" \
  --size "50 users" \
  --licenses "E5" \
  --compliance "HIPAA, SOX" \
  --platforms "Windows, iOS" \
  --focus "Encryption and DLP on financial documents"
```

**Less specific** (generic):
```
/intune-policy --tenant "Company" --licenses "E3"
```

### 2. Iterate on Outputs

The first run gives you a solid baseline. Run again with refined inputs to drill deeper.

**First run**: Get the full strategy and roadmap.
**Second run**: Focus on one component (e.g., `--focus "MFA adoption"` for Conditional Access).
**Third run**: Build deployment runbooks or compliance evidence.

### 3. Use Portal Navigation Steps Verbatim

Each command includes step-by-step portal navigation (e.g., "Intune admin center > Devices > Compliance > Create"). Copy these exactly; Microsoft portals can change paths occasionally.

### 4. Validate Before Full Rollout

Always pilot before production:
- Intune policies: Test with 10–25 device pilot group first.
- Conditional Access: Use "Report-Only" mode before enforcement.
- Flow changes: Test in sandbox/test tenant before production.
- Retention labels: Pilot with one department before org-wide.

### 5. Align Compliance Frameworks

Different frameworks require different controls. The commands map controls to frameworks, but verify with your compliance team:
- **SOC 2 Type II**: Annual audit, focus on controls maturity.
- **HIPAA**: Data encryption, access logs, breach notification.
- **GDPR**: Data minimization, retention, user rights (access, deletion).
- **ISO 27001**: Risk management, asset control, incident response.
- **NIST CSF**: Identify, Protect, Detect, Respond, Recover.

### 6. Document Everything

Auditors want evidence:
- Who approved what change?
- When was it deployed?
- What was the rationale?
- Did it achieve the intended security outcome?

Use the "Compliance & Audit Evidence" sections in each command's output to build your evidence trail.

### 7. Sync HR + IT Processes

Onboarding/offboarding only works if HR and IT are aligned:
- Establish clear communication (email, shared form, ticketing system).
- Define SLAs (e.g., "Account provisioned within 4 hours of hire approval").
- Test the end-to-end process before scaling.

### 8. Monitor Continuously

After deployment, monitor key metrics:
- **Intune**: Device compliance rates, policy failures, remediation success.
- **Conditional Access**: Sign-in failures, MFA adoption, risky sign-ins blocked.
- **Defender**: Alert volume, incident response time, false positive rate.
- **Purview**: Label application rates, retention compliance, audit log hits.

Use the dashboards in Security.microsoft.com, Intune admin center, Azure AD, and Purview Compliance to track these metrics.

---

## Troubleshooting

### Q: My output is generic or missing specifics.

**A**: Provide more detailed variables. Example:
- Instead of `--compliance "Compliance"`, specify `--compliance "SOC 2 Type II, HIPAA".
- Instead of `--focus "Security"`, specify `--focus "Encryption and device restrictions on BYOD devices"`.

### Q: I got an output, but it doesn't match my environment.

**A**: This is expected. The output is a template:
1. Copy the relevant sections.
2. Update tenant names, usernames, group names to match your environment.
3. Adjust timelines and effort estimates for your team's capacity.
4. Verify portal paths (Microsoft sometimes changes menu structure).

### Q: Can I combine multiple commands?

**A**: Yes! For a comprehensive M365 security program:
1. Start with `/security-posture` (understand current state).
2. Run `/intune-policy`, `/conditional-access`, `/defender-triage`, `/retention-labels` (address specific gaps).
3. Use `/flow-docs` to automate repetitive tasks.
4. Use `/onboard-offboard` to ensure consistent user lifecycle management.

### Q: Do I need to run these locally or can I use Claude.ai?

**A**: You can use either:
- **Claude.ai** (free, no API key): Paste command syntax, get output.
- **Claude Code**: Install as a plugin, run commands directly.
- **Claude API**: Invoke via API calls for automation.

For best experience, install as a Claude Code plugin.

### Q: How do I customize the templates further?

**A**: Each output is markdown. You can:
- Copy sections to Word, Google Docs, or your wiki.
- Replace placeholders (e.g., `[Tenant Name]`) with your values.
- Remove sections that don't apply.
- Add your organization's specific policies (e.g., "All policies must be approved by CISO").
- Version control in Git (recommended for audit trail).

### Q: How do I know if the output is production-ready?

**A**: Use this checklist:
- [ ] All placeholders customized to your environment.
- [ ] Portal steps verified (tested in your tenant).
- [ ] Compliance mappings reviewed by Legal/Compliance.
- [ ] Stakeholders (manager, CISO, compliance officer) approved.
- [ ] Pilot testing completed successfully.
- [ ] Rollback plan documented.
- [ ] Monitoring and alerting configured.

Once you check all boxes, you can deploy.

---

## Author & License

**Author**: Donte Wong
- M365 IT Director managing 100+ user enterprise tenant (Intune, Defender, Entra ID, Purview).
- USAF veteran, CompTIA Security+, Project Management Professional (PMP).
- 10+ years hands-on M365 infrastructure and security experience.

**Built**: These templates are the exact documents I build for my own environment, templatized for reuse.

**License**: MIT

You may use, modify, and distribute these templates freely. Attribution appreciated but not required.

---

## Support & Feedback

For questions, issues, or feature requests:

- **Gumroad**: https://dontewong.gumroad.com/l/m365-it-admin-library
- **Email**: donte@example.com (hypothetical contact)
- **Community**: Share your use cases and improvements!

---

## What's Included

This plugin contains:

1. **`.claude-plugin/plugin.json`** — Plugin metadata.
2. **`skills/m365-admin.md`** — Core M365 architect persona and guidance.
3. **`commands/intune-policy.md`** — Intune Compliance Policy Builder.
4. **`commands/conditional-access.md`** — Conditional Access Explainer & Builder.
5. **`commands/defender-triage.md`** — Defender Triage Template.
6. **`commands/retention-labels.md`** — Purview Retention Label Strategy.
7. **`commands/flow-docs.md`** — Power Automate Flow Documentation.
8. **`commands/security-posture.md`** — Security Posture Assessment Report.
9. **`commands/onboard-offboard.md`** — IT Onboarding & Offboarding Checklists.
10. **`README.md`** — This file.

---

**Ready to save time on M365 documentation?**

Start with `/security-posture` to understand your current state, then run other commands to address gaps.

Good luck! The templates are battle-tested in enterprise environments and ready for production use.
