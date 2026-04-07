# Conditional Access Explainer & Builder

## Description

Generates a comprehensive Conditional Access (CA) policy inventory with plain-English explanations, risk-based access flow diagrams, and policy gap analysis. Output includes policy recommendations, deployment strategy, and audit-ready documentation for stakeholders and compliance teams.

**Use this command when**:
- Building or hardening Conditional Access policies from scratch.
- Documenting existing CA policies for audits and stakeholder handoffs.
- Implementing Zero Trust or risk-based access controls.
- Preparing for a security assessment or compliance review.
- Creating a CA policy gap analysis (what's missing, what needs adjustment).

---

## Required Variables

```xml
<tenant_name>Organization name (e.g., "Acme Corp IT")</tenant_name>

<tenant_size>User count (e.g., "100–250 users", "500–1000 users")</tenant_size>

<licensed_skus>Licensing tier(s) (e.g., "E5, Premium P2")</licensed_skus>

<compliance_frameworks>Applicable regulations (e.g., "SOC 2 Type II, Zero Trust")</compliance_frameworks>

<primary_risk_focus>Primary access control concern (e.g., "External user access", "Unmanaged devices", "Legacy authentication", "High-risk sign-ins")</primary_risk_focus>

<target_apps>Apps to protect (e.g., "Exchange Online, SharePoint Online, Teams, Power BI")</target_apps>

<existing_ca_count>Current CA policy count (e.g., "None", "5–10 existing policies")</existing_ca_count>
```

---

## Command Invocation

```
/conditional-access --tenant "Acme Corp" --size "250 users" --licenses "E5, Premium P2" --compliance "SOC 2, Zero Trust" --risk-focus "External user access" --apps "Exchange, SharePoint, Teams" --existing "3 policies"
```

---

## Skill Binding

This command invokes the **M365 IT Admin Architect** skill with these instructions:

**Task**: Generate a Conditional Access policy inventory and gap analysis document.

**Context**:
- Tenant: <tenant_name>, <tenant_size>
- Licenses: <licensed_skus>
- Compliance: <compliance_frameworks>
- Risk focus: <primary_risk_focus>
- Protected apps: <target_apps>
- Current state: <existing_ca_count>

**Output Structure**:

1. **Executive Summary**
   - Current access control posture (high-level).
   - Key risks and mitigation strategies.
   - Recommended CA policy count and deployment timeline.

2. **Conditional Access Baseline**
   - List 5–8 recommended CA policies, prioritized by risk.
   - Each policy includes:
     - **Policy Name**: Descriptive (e.g., "Block Legacy Authentication").
     - **Objective**: Security goal (e.g., "Prevent sign-in via basic auth protocols").
     - **Conditions**: User/group, location, device state, app, sign-in risk, etc.
     - **Controls**: Require MFA, device compliance, session timeout, block, etc.
     - **License Requirement**: Which licenses enable this (CA is E5/Premium P1+).
     - **Plain English Explanation**: Non-technical summary for stakeholders.

3. **Policy Flow Diagram (ASCII)**
   - Visualize decision logic (e.g., "If user signs in from outside US AND device is unmanaged AND app is Exchange, THEN require MFA").
   - Show policy precedence and stacking effects.

4. **Gap Analysis**
   - Current policies inventory (if <existing_ca_count> > 0).
   - Missing policies (e.g., "Legacy auth block", "Unmanaged device restrictions").
   - Overly complex policies that can be simplified.
   - Conflicting or redundant policies.

5. **Implementation Roadmap**
   - Phase 1: Pilot (1–2 foundational policies, small user group).
   - Phase 2: Core policies (expand to all cloud apps).
   - Phase 3: Advanced policies (risk-based, session controls).
   - Effort estimates, testing requirements, rollback procedures.

6. **Portal Navigation & Steps**
   - Detailed instructions for each policy in Azure AD > Conditional Access.
   - Condition and control configurations (condition matching logic, operator precedence).

7. **Stakeholder Communication**
   - Non-technical summary of what's changing (user impact, MFA prompts, etc.).
   - FAQ (Why this policy? What happens if I don't comply?).

8. **Audit & Compliance**
   - Policy versioning and change history recommendations.
   - Monitoring (sign-in logs, risk detections, policy violations).
   - Regulatory alignment (SOC 2, NIST, Zero Trust framework).

**Tone**: Pragmatic, stakeholder-friendly, audit-ready.

---

## Sample Output (Teaser)

**Document Title**: Conditional Access Policy Inventory & Gap Analysis — Acme Corp

**Policy 1: Block Legacy Authentication**
- **Objective**: Prevent sign-in using IMAP, POP, SMTP, and other basic auth protocols.
- **Conditions**:
  - Client apps: Exchange Online (IMAP, POP), Outlook legacy, other legacy clients
  - All cloud apps
  - All users
- **Controls**: Block access
- **License**: E5 or Premium P1
- **Plain English**: "We don't allow email to log in with just a username and password. Legacy email clients have to use Modern Auth with MFA."
- **Impact**: Users on old Outlook/Thunderbird versions must update; mobile apps must switch to modern OAuth.

**Policy 2: Require MFA for External Users**
- **Objective**: Require multi-factor authentication for any user signing in from outside the organization's IP range.
- **Conditions**:
  - User: Guest users (external) + synchronized users from partner orgs
  - Location: Named locations (exclude internal IPs)
  - All cloud apps
- **Controls**: Require MFA
- **License**: E5 or Premium P1
- **Plain English**: "External partners and contractors must use a second verification method (phone, authenticator app, or security key) when accessing our apps."

---

## Related Commands

- `/intune-policy` — Layer in device compliance requirements via Intune.
- `/security-posture` — Measure risk detection and CA effectiveness.
- `/defender-triage` — Correlate CA blocks with incident response.

---

## Tips

- **Test in Report-Only mode first**: CA supports a "Report-Only" state that logs what would be blocked without actually blocking. Use this to validate policies before enforcement.
- **MFA method options**: Offer users multiple MFA options (Microsoft Authenticator, phone, FIDO2 security keys) to maximize adoption.
- **Location-based policies**: Use named locations (on-prem office IP ranges) to reduce friction for internal users while protecting against external threats.
- **License requirement**: Conditional Access requires M365 E5, Azure AD Premium P1+, or EMS E5. Some features (risk-based) require P2.
- **Session controls**: Use session controls (app enforced restrictions, sign-in frequency) to add an additional layer of risk-based access.
