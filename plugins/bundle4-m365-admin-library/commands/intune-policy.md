# Intune Compliance Policy Builder

## Description

Generates a comprehensive Intune compliance policy baseline tailored to your organization's security requirements, licensing tier, and compliance frameworks. Output includes policy recommendations, portal navigation steps, device groups, and validation procedures.

**Use this command when**:
- Building a new Intune compliance baseline from scratch.
- Hardening existing policies against security benchmarks.
- Preparing for a compliance audit (SOC 2, HIPAA, CJIS, ISO 27001).
- Scaling policies across multiple device platforms (Windows, macOS, iOS, Android).

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<tenant_size>User count range (e.g., "100–250 users", "500–1000 users")</tenant_size>

<licensed_skus>Licensing tier(s) (e.g., "E3, E5, Intune standalone")</licensed_skus>

<compliance_frameworks>Applicable regulations (e.g., "SOC 2 Type II, HIPAA, NIST CSF")</compliance_frameworks>

<device_platforms>Platforms to secure (e.g., "Windows 10/11", "macOS", "iOS", "Android")</device_platforms>

<primary_focus>Policy focus area (e.g., "Encryption & data protection", "Mobile device control", "Windows hardening", "Application control")</primary_focus>

<deployment_strategy>Rollout approach (e.g., "Pilot group (25 devices)", "Phased by department", "Full tenant")</deployment_strategy>
```

---

## Command Invocation

```
/intune-policy --tenant "Acme Corp" --size "250 users" --licenses "E3, E5" --compliance "SOC 2, HIPAA" --platforms "Windows, iOS" --focus "Mobile device security" --deployment "Phased by department"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate an Intune compliance policy baseline document.

**Context**:
- Tenant: <tenant_name>, <tenant_size>
- Licenses: <licensed_skus>
- Compliance: <compliance_frameworks>
- Devices: <device_platforms>
- Focus: <primary_focus>
- Rollout: <deployment_strategy>

**Output Structure**:

1. **Policy Inventory**
   - List 3–6 recommended compliance policies by platform.
   - Align each to a specific security objective (encryption, device restrictions, app protection, etc.).

2. **Policy Definitions**
   - For each policy, provide:
     - **Platform**: Windows, macOS, iOS, Android, or multi-platform.
     - **Objective**: Security goal (e.g., "Enforce full-disk encryption").
     - **Requirements**: Licenses needed, prerequisites, dependencies.
     - **Portal Path**: Step-by-step navigation in Intune admin center.
     - **Configuration**: Key settings (encryption algorithm, password requirements, app restrictions, etc.).
     - **Device Groups**: Which groups to target (e.g., "All Windows devices", "iOS corporate devices").

3. **Compliance Alignment**
   - Map each policy to compliance framework controls (e.g., SOC 2 CC6.2 "Logical access controls", HIPAA §164.312(a)(2)(i) "Encryption and decryption").

4. **Deployment Roadmap**
   - Phase 1: Pilot (scope, timeline, success criteria).
   - Phase 2: Rollout (group sizes, communication plan).
   - Phase 3: Monitoring & optimization.

5. **Device Validation**
   - Intune compliance reports to monitor.
   - Expected compliance rates and remediation actions.
   - Common non-compliance scenarios and fixes.

6. **Audit Evidence**
   - What to document for compliance auditors.
   - Policy version tracking, deployment timestamps, compliance dashboards.

**Tone**: Pragmatic, audit-ready, copy-paste ready for deployment.

---

## Sample Output (Teaser)

**Document Title**: Intune Compliance Policy Baseline — Acme Corp

**Policy 1: Windows 10/11 Device Encryption**
- Platform: Windows
- Objective: Enforce BitLocker encryption for all corporate devices.
- License: Intune standalone or M365 E3+
- Portal Path: Intune admin center > Devices > Compliance > Create Policy > Windows 10 and later
- Key Setting: Encryption required = Yes, Encryption method = XTS-AES 128-bit (or stronger)
- Target Groups: All Windows devices (excluding DEP/COPE)
- Compliance Mapping: SOC 2 CC6.2, HIPAA §164.312(a)(2)(iv), NIST SP 800-53 SC-28

---

## Related Commands

- `/conditional-access` — Layer in risk-based access controls.
- `/security-posture` — Measure overall posture including compliance metrics.
- `/onboard-offboard` — Ensure new devices enroll and configure policies automatically.

---

## Tips

- **License variance**: If the organization has E3 only, some advanced protection features won't be available; this command will flag and provide E3-compatible alternatives.
- **Pilot first**: Always run a pilot with a small group before full rollout.
- **Remediation action**: Set policies to "remediate non-compliance" (device blocks cloud access) rather than soft warnings if security posture is critical.
- **Monitor baseline**: Use Intune's compliance dashboard (Intune > Devices > Compliance) to track real-time compliance rates.
