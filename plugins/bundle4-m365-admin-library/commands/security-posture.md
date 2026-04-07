# Security Posture Assessment Report

## Description

Synthesizes Defender, Conditional Access, Intune, and Entra ID signals into a single executive summary. Output includes risk scorecard, remediation roadmap, trending insights, and compliance alignment. Perfect for board-level reporting, quarterly reviews, and audit readiness.

**Use this command when**:
- Conducting a quarterly or annual security health review.
- Preparing for a compliance audit (SOC 2, ISO 27001, HIPAA, etc.).
- Creating an executive summary for board or leadership.
- Planning a security roadmap for the next 12 months.
- Benchmarking your posture against industry standards.

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<tenant_size>User count (e.g., "100–250 users", "500–1000 users", "1000+ users")</tenant_size>

<licensed_skus>Licensing (e.g., "E3, E5, Premium P2, Defender for Identity")</licensed_skus>

<compliance_frameworks>Applicable regulations (e.g., "SOC 2 Type II, HIPAA, ISO 27001, NIST CSF")</compliance_frameworks>

<report_period>Review timeframe (e.g., "Q4 2025", "Last 12 months", "Last 90 days")</report_period>

<prior_report_date>Previous assessment date if available (e.g., "2025-10-01" for trend comparison)</prior_report_date>

<assessment_focus>Priority areas (e.g., "Overall security posture", "Incident response readiness", "Compliance gaps", "Cloud adoption")</assessment_focus>
```

---

## Command Invocation

```
/security-posture --tenant "Acme Corp" --size "250 users" --licenses "E5, Premium P2, Defender for Identity" --compliance "SOC 2, ISO 27001, HIPAA" --period "Q1 2026" --prior "2025-10-01" --focus "Overall posture, incident response, compliance gaps"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate a comprehensive security posture assessment report.

**Context**:
- Tenant: <tenant_name>, <tenant_size>
- Licenses: <licensed_skus>
- Compliance: <compliance_frameworks>
- Period: <report_period>
- Prior assessment: <prior_report_date> (if applicable)
- Focus areas: <assessment_focus>

**Output Structure**:

1. **Executive Summary**
   - Overall security posture rating (e.g., "Green", "Yellow", "Red" with 1-3 sentence justification).
   - Key highlights (improvements since last assessment).
   - Critical risks requiring immediate attention (if any).
   - Strategic recommendations for leadership.

2. **Security Scorecard**
   - Overall score (0–100) with components:
     - **Identity & Access** (Entra ID, Conditional Access, MFA adoption): Score, status, trend.
     - **Endpoint Security** (Intune compliance, Defender for Endpoint): Score, status, trend.
     - **Threat Detection** (Defender alerts, incident response): Score, status, trend.
     - **Data Protection** (Purview, DLP, encryption): Score, status, trend.
     - **Compliance Readiness** (Audit controls, logging, documentation): Score, status, trend.
   - Trend indicators (↑ improving, → stable, ↓ declining).

3. **Detailed Assessment by Domain**

   **3.1 Identity & Access**
   - Entra ID health: Directory sync, licensing, user count.
   - MFA adoption: Percentage of users, fallback authentication, FIDO2 security keys.
   - Conditional Access: Number of policies, enforcement rate, risky sign-in blocks.
   - Privileged access: PIM usage, admin role assignments, privilege elevation tracking.
   - Gaps & recommendations: e.g., "Only 60% of users have MFA; recommend user education campaign".

   **3.2 Endpoint Security**
   - Intune enrollment: Percentage of devices, platforms (Windows, macOS, iOS, Android).
   - Compliance rate: Percentage of devices compliant with policies.
   - Defender for Endpoint: Coverage, malware detection rate, remediation success.
   - Gaps & recommendations: e.g., "macOS devices not enrolled; deploy Jamf or Intune company portal".

   **3.3 Threat Detection & Response**
   - Defender alerts: Volume, severity distribution, false positive rate.
   - Incident response: Number of incidents, average response time, escalation rate.
   - Security events: Phishing blocks, malware detections, anomalous sign-ins.
   - Gaps & recommendations: e.g., "No formal IR runbooks; create incident response playbooks".

   **3.4 Data Protection**
   - Data classification: Percentage of sensitive data tagged.
   - Encryption: Email TLS, device encryption (BitLocker), at-rest encryption.
   - DLP policies: Rules in place, violations, user awareness.
   - Retention & compliance: Data retention compliance rate, eDiscovery readiness.
   - Gaps & recommendations: e.g., "No DLP policies for OneDrive; implement sensitive data classification".

   **3.5 Compliance & Audit**
   - Regulatory alignment: Mapping to SOC 2, ISO 27001, HIPAA, etc.
   - Audit logging: Enabled, retention, analysis.
   - Change control: Formal approval process, change log completeness.
   - Incident documentation: Breach notification procedures, audit trail completeness.
   - Gaps & recommendations: e.g., "Audit logs not centralized; implement Azure Monitor + Log Analytics".

4. **Risk Matrix**
   - Identified risks with:
     - **Risk description**: What could go wrong.
     - **Likelihood**: High/Medium/Low (based on current controls).
     - **Impact**: High/Medium/Low (business impact if it happens).
     - **Current mitigation**: Controls in place to reduce risk.
     - **Recommended action**: Priority (Critical, High, Medium, Low), timeline, owner.
   - Example: Risk "Unmanaged BYOD devices accessing Exchange" → Likelihood High, Impact High → Implement device compliance policy (Critical, 30 days, IT Admin).

5. **Compliance Alignment Matrix**
   - Table mapping security controls to regulatory requirements.
   - Example:
     | Control | SOC 2 CC6.1 | ISO 27001 A.9.1.1 | HIPAA §164.312(a)(1) |
     |---------|------------|-------------------|----------------------|
     | MFA enabled | ✓ | ✓ | ✓ |
     | Device encryption | ✓ | ✓ | ✓ |
     | Conditional Access | ✓ | ✓ | ✓ |

6. **Remediation Roadmap (12-Month Plan)**
   - Phase 1 (Next 90 days): Quick wins, high-impact items.
     - Example: "Enforce MFA for all users", "Publish Conditional Access policies", "Deploy Intune compliance policies".
   - Phase 2 (91–180 days): Medium-complexity improvements.
     - Example: "Implement DLP policies", "Roll out advanced Defender features", "Centralize audit logging".
   - Phase 3 (181–365 days): Strategic investments.
     - Example: "Achieve SOC 2 Type II certification", "Implement Advanced Hunting", "Deploy Privileged Identity Management".

7. **Metrics & KPIs to Monitor**
   - Dashboard indicators (Real-time or weekly):
     - MFA adoption %, Intune compliance %, Defender alert volume, incident response time, audit log completion %.
   - Targets: What should each metric be in 12 months?
   - Data source: Where to get these metrics (Intune admin center, Security.microsoft.com, Azure AD insights, etc.).

8. **Comparison to Prior Assessment** (if applicable)
   - Trends over time (improvement vs. decline).
   - Metrics that improved: Celebrate and sustain.
   - Metrics that declined: Investigate root causes and re-prioritize.
   - New risks identified: Assess and remediate.

9. **Industry Benchmarking** (if contextually relevant)
   - How does this organization compare to industry peers (e.g., mid-market SMB, healthcare, financial services)?
   - Percentile ranking on key metrics (identity, endpoint, threat detection).
   - Benchmarking data source (if available: Verizon DBIR, Gartner, internal comparison).

10. **Audit & Compliance Evidence**
    - Evidence collected for this assessment (Intune reports, Defender logs, Azure AD audit logs, etc.).
    - Retention policy for assessment artifacts.
    - How to present findings to auditors/leadership.
    - Appendices: Sample screenshots, raw metrics, detailed logs.

**Tone**: Executive-friendly, data-driven, action-oriented.

---

## Sample Output (Teaser)

**Document Title**: Security Posture Assessment Report — Acme Corp (Q1 2026)

**Overall Posture**: Yellow (79/100)

**Rationale**: Strong identity and endpoint controls (Entra ID, Intune, Conditional Access), but gaps in threat detection orchestration and compliance documentation. Significant improvement vs. Q4 2025 (68/100), trending in right direction.

**Key Highlights**:
- MFA adoption: 95% (↑ from 78% in Q4 2025)
- Intune compliance: 88% (↑ from 72%)
- Defender incident response time: 4.2 hours (↑ improved from 6.1 hours)
- Zero data breaches or security incidents in Q1

**Critical Risks**:
1. **Risk**: Unmanaged BYOD devices with no compliance enforcement → **Action**: Deploy device compliance policy (Critical, 15 days)
2. **Risk**: No formal incident response runbooks → **Action**: Publish IR playbooks (High, 30 days)

**Scorecard**:
| Domain | Score | Status | Trend |
|--------|-------|--------|-------|
| Identity & Access | 92 | Green | ↑ |
| Endpoint Security | 84 | Green | ↑ |
| Threat Detection | 68 | Yellow | → |
| Data Protection | 72 | Yellow | ↓ |
| Compliance Readiness | 77 | Yellow | ↑ |

---

## Related Commands

- `/intune-policy` — Implement or refine endpoint compliance policies.
- `/conditional-access` — Strengthen identity-based access controls.
- `/defender-triage` — Improve threat detection and incident response.
- `/retention-labels` — Strengthen data protection and compliance alignment.

---

## Tips

- **Use native dashboards**: Leverage Intune admin center, Security.microsoft.com, and Azure AD Insights for real-time metrics.
- **Trending matters**: Comparing to prior assessments shows improvement or decline; always include historical context.
- **Risk tolerance**: Not all risks require immediate remediation. Align remediation roadmap to risk tolerance and business priorities.
- **Benchmark with caution**: Industry benchmarks can be helpful for context, but your organization's risk profile is unique.
- **Executive translation**: Avoid technical jargon in the Executive Summary; use business language (revenue risk, compliance violation cost, incident response time).
- **Annual cadence**: Conduct formal assessments quarterly; interim checks (monthly dashboard reviews) inform planning.
