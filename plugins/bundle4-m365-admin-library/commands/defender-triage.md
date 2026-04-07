# Defender Triage Template

## Description

Systematically assesses Microsoft Defender alerts, incidents, and endpoint health across your M365 environment. Output includes incident severity matrix, remediation tracking, threat summary, and compliance correlation. Perfect for incident response runbooks, SIEM handoffs, and compliance reporting.

**Use this command when**:
- Responding to Defender alerts and building a triage process.
- Preparing an incident response runbook aligned with your environment.
- Integrating Defender data with SIEM or ticketing systems.
- Compiling a threat and incident summary for compliance auditors.
- Conducting a quarterly security health review.

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<tenant_size>User count (e.g., "100–250 users", "500–1000 users")</tenant_size>

<licensed_skus>Licensing (e.g., "E5 + Defender for Identity", "E3 + Defender for Office standalone")</licensed_skus>

<defender_modules>Active Defender modules (e.g., "Defender for Endpoint, Defender for Office, Cloud App Security")</defender_modules>

<compliance_frameworks>Applicable regulations (e.g., "SOC 2 Type II, HIPAA, NIST CSF")</compliance_frameworks>

<incident_context>Specific incident or threat (e.g., "Phishing campaign with malware attachment", "Ransomware detection", "Unusual sign-in activity", "General quarterly review")</incident_context>

<siem_integration>SIEM platform if integrated (e.g., "Splunk", "Sentinel", "None")</siem_integration>
```

---

## Command Invocation

```
/defender-triage --tenant "Acme Corp" --size "250 users" --licenses "E5 + Defender for Identity" --modules "Endpoint, Office, Cloud App Security" --compliance "SOC 2, NIST" --context "Phishing with attachment campaign" --siem "Sentinel"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate a Defender triage and incident assessment document.

**Context**:
- Tenant: <tenant_name>, <tenant_size>
- Licenses: <licensed_skus>
- Defender coverage: <defender_modules>
- Compliance: <compliance_frameworks>
- Incident type: <incident_context>
- SIEM: <siem_integration>

**Output Structure**:

1. **Incident Summary**
   - High-level overview (what happened, scope, timeline).
   - Affected assets (users, devices, data).
   - Current status (ongoing, contained, resolved).

2. **Severity & Risk Assessment**
   - Severity level (Critical, High, Medium, Low) with justification.
   - Risk matrix (likelihood × impact).
   - Alignment with compliance frameworks (e.g., "If this data was PII, it's a HIPAA breach").

3. **Defender Detection & Alerts**
   - Alerts triggered by module (Defender for Endpoint, Office, Identity, etc.).
   - Alert timeline (first detection, escalation, resolution).
   - Confidence scores and detection logic.

4. **Triage Workflow**
   - Step-by-step incident response process.
   - Portal navigation (Security.microsoft.com > Incidents, Device Timeline, Email Threat Explorer).
   - Decision points (escalate? isolate? remediate?).
   - Evidence collection (logs, email metadata, file hashes).

5. **Remediation Tracking**
   - Recommended actions (block sender, isolate device, revoke tokens, etc.).
   - Action status (pending, in-progress, completed).
   - Rollback/contingency plans.

6. **SIEM/Ticketing Integration** (if applicable)
   - Format for log export to SIEM.
   - Recommended alert severity mapping (Defender → SIEM severity scale).
   - Automation opportunities (e.g., "Auto-create Jira ticket on Critical alert").

7. **Compliance & Audit Trail**
   - Incident timeline for auditors.
   - Evidence preservation (email quarantine, device forensics).
   - Regulatory reporting requirements (breach notification, incident disclosure).
   - Defender logging alignment (Advanced Hunting queries, audit logs).

8. **Post-Incident Actions**
   - Preventive controls to reduce recurrence (CA policy, Defender tuning, user training).
   - Monitoring recommendations.
   - Lessons learned & playbook refinement.

**Tone**: Structured, evidence-focused, forensic-ready.

---

## Sample Output (Teaser)

**Document Title**: Defender Triage & Incident Response — Phishing Campaign with Malware

**Incident Summary**:
- Type: Phishing email with malicious attachment (suspected trojan).
- Scope: 35 users received email; 8 opened attachment; 3 devices executed payload.
- Timeline: First detection 2026-04-01 14:22 UTC; contained by 15:45 UTC.
- Status: Contained; remediation in-progress.

**Severity**: High
- Reasoning: Malware detected on 3 devices; payload attempts lateral movement.
- Impact: Potential data exfiltration, credential compromise, lateral spread.
- Compliance: HIPAA reportable if PII was accessed; SOC 2 incident logging required.

**Defender Alerts**:
1. Defender for Office 365: Malicious email detected in Transport (phishing + malware).
2. Defender for Endpoint: Suspicious behavior (process creation, network connection to C2).
3. Defender for Identity: Impossible travel alert (sign-in from unexpected geography post-compromise).

**Triage Workflow**:
1. Quarantine email in Exchange (remove from all inboxes).
2. Isolate 3 affected devices from network.
3. Run forensic scan in Defender (gather file hash, parent process, network connections).
4. Check Azure AD sign-in logs for token theft (unexpected locations, apps).
5. Escalate to IR team if C2 communication confirmed.

**Remediation**:
- Email quarantined: Yes
- Devices isolated: Yes
- Malware signature updated: Yes
- Conditional Access policy updated (block high-risk sign-ins): In-progress

---

## Related Commands

- `/conditional-access` — Layer in risk-based access to limit lateral movement.
- `/intune-policy` — Ensure device compliance and threat remediation.
- `/security-posture` — Measure overall Defender coverage and effectiveness post-incident.

---

## Tips

- **Alert tuning**: Microsoft Defender generates many alerts. Tune exclusions and auto-remediation to reduce noise while catching real threats.
- **Email threat explorer**: Use Threat Explorer in Security.microsoft.com to pivot on phishing campaigns (sender, attachment hash, affected users).
- **Advanced Hunting**: Write KQL (Kusto Query Language) queries to hunt for related IOCs (Indicators of Compromise) across your environment.
- **Device timeline**: Defender for Endpoint's device timeline shows process execution, network connections, file activity—invaluable for forensics.
- **Incident graph**: The Incidents page in Security.microsoft.com correlates alerts across Defender modules into a unified incident view.
- **SIEM correlation**: If you have Sentinel or Splunk, configure connector to ingest Defender logs; correlate with other data sources for richer context.
