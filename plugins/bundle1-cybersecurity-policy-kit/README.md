# SMB Cybersecurity Policy Kit

Generate NIST CSF 2.0-aligned cybersecurity policies for small and mid-size businesses. Production-ready policy generators covering Acceptable Use Policy, Incident Response Plan, Password & MFA Policy, Data Classification Policy, and Remote Work Security Policy.

**Created by:** Donte Wong, USAF veteran, Director of IT & Cybersecurity
**Version:** 1.0.0
**License:** MIT

## Overview

The SMB Cybersecurity Policy Kit is a comprehensive policy generation toolkit designed for organizations with 10-500 employees. It combines security expertise with practical SMB constraints to generate customized, legally-sound cybersecurity policies aligned with NIST Cybersecurity Framework 2.0.

### Key Features
- **5 Production-Ready Policies**: AUP, IRP, Password/MFA, Data Classification, Remote Work Security
- **NIST CSF 2.0 Aligned**: All policies map explicitly to NIST functions and categories
- **SMB-Optimized**: Practical, implementable policies for organizations with limited security staff
- **Customizable**: Templates use 8 XML variables to tailor policies to your organization
- **Implementation-Focused**: Includes checklists, playbooks, and step-by-step deployment guides
- **Policy Auditor**: Evaluate existing policies against NIST CSF 2.0 and identify gaps

## Installation

### Requirements
- Claude Code (latest version)
- Access to Claude API

### Install as Claude Code Plugin

1. **Download the plugin directory**
   ```
   bundle1-cybersecurity-policy-kit/plugin/
   ```

2. **Install in Claude Code**
   - Open Claude Code on your system
   - Navigate to Plugins section
   - Click "Add Plugin"
   - Select the plugin directory
   - The plugin will automatically load all skills, commands, and agents

3. **Verify Installation**
   - Check that 5 commands are available: `aup`, `irp`, `password-policy`, `data-classify`, `remote-work-policy`
   - Check that `policy-generator` skill is loaded
   - Check that `policy-auditor` agent is available

## Quick Start

### Generate Your First Policy

1. **Gather your organization's information**:
   - Company name
   - Industry (Technology, Healthcare, Finance, etc.)
   - Employee count
   - Primary systems/tools used (Microsoft 365, AWS, Salesforce, etc.)
   - Current security challenges
   - Risk profile (Low, Medium, High)
   - Geographic scope (US, US+EU, etc.)
   - Budget tier (Lean, Standard, Comprehensive)

2. **Choose a policy to generate**:
   ```
   /aup                    # Acceptable Use Policy
   /irp                    # Incident Response Plan
   /password-policy        # Password & MFA Policy
   /data-classify          # Data Classification Policy
   /remote-work-policy     # Remote Work Security Policy
   ```

3. **Provide your information in XML format** when prompted:
   ```xml
   <company_name>Acme Corp</company_name>
   <industry>Technology</industry>
   <employee_count>150</employee_count>
   <primary_systems>Microsoft 365, AWS, Salesforce</primary_systems>
   <current_challenges>Shadow IT adoption, unclear password standards</current_challenges>
   <risk_profile>Medium</risk_profile>
   <geographic_scope>United States only</geographic_scope>
   <budget_tier>Standard</budget_tier>
   ```

4. **Claude will generate** a complete policy document with:
   - Policy statements and procedures
   - NIST CSF 2.0 alignment mapping
   - Implementation checklist with roles and timelines
   - Compliance monitoring procedures
   - Legal disclaimer

5. **Review and customize**:
   - Replace generic language with your organization-specific details
   - Customize role names and responsibilities
   - Set specific dates and review schedules
   - Have legal counsel review before implementation

## Commands Reference

### /aup - Acceptable Use Policy
Generates a policy defining appropriate use of company IT resources, systems, and data.

**Covers:**
- Personal vs. business use boundaries
- Social media and external communications guidance
- Prohibited activities
- Consequences for violations
- Employee acknowledgment procedures

**Output includes:**
- AUP policy document
- NIST CSF alignment (GV-3, PR-1, PR-2)
- Implementation checklist
- Employee training materials

**Use when:** You need to establish clear expectations for employee behavior on company systems and enforce consequences for misuse.

---

### /irp - Incident Response Plan
Generates a comprehensive incident response plan with severity tiers and escalation procedures.

**Covers:**
- Incident severity classification (Critical, High, Medium, Low)
- Escalation matrix and contact procedures
- Response team roles and responsibilities
- Investigation and forensics procedures
- Evidence preservation and chain of custody
- Internal and external communications
- Regulatory reporting requirements
- Post-incident review and improvement

**Output includes:**
- IRP policy document
- Escalation matrix with roles and triggers
- Response playbooks for top 5 incident types
- Contact directory template
- Tabletop exercise guide
- NIST CSF alignment (DE-1, DE-3, RS-1, RS-2, RS-3)

**Use when:** You want to establish formal incident response procedures, define clear escalation paths, and prepare your team for rapid, coordinated response to security incidents.

---

### /password-policy - Password & MFA Policy
Generates a password and multi-factor authentication policy with tool-specific implementation guidance.

**Covers:**
- Password complexity and strength requirements
- Password rotation and expiration rules
- MFA mandate and applicability
- Password manager recommendations
- Tool-specific guidance (M365, Google Workspace, AWS, Active Directory)
- Account lockout and recovery procedures
- Legacy system workarounds
- Phased MFA rollout strategy

**Output includes:**
- Password/MFA policy document
- Tool-specific configuration steps
- MFA deployment timeline
- User communication templates
- Compliance monitoring procedures
- NIST CSF alignment (PR-1, PR-3)

**Use when:** You want to strengthen authentication controls, enforce modern password practices, and roll out MFA across your organization in phases.

---

### /data-classify - Data Classification Policy
Generates a 4-tier data classification scheme with handling requirements for each tier.

**Covers:**
- Public tier (unrestricted external sharing)
- Internal tier (employee-only, non-sensitive)
- Confidential tier (need-to-know access, sensitive business data)
- Restricted tier (highly sensitive, regulatory data)
- Handling requirements per tier (access, encryption, storage)
- Data retention and destruction schedules
- User responsibilities and training
- Incident procedures by classification level

**Output includes:**
- Data Classification Policy document
- 4-tier classification matrix
- Data inventory and discovery checklist
- Storage/system approval matrix
- User training guide
- Classification accuracy audit procedures
- NIST CSF alignment (GV-1, ID-1, PR-1, PR-2)

**Use when:** You want to establish a common language for data sensitivity, ensure appropriate security controls for each data type, and enable consistent data handling across your organization.

---

### /remote-work-policy - Remote Work Security Policy
Generates a remote work security policy with BYOD section and work arrangement specifics.

**Covers:**
- Remote work arrangement types (full-time, hybrid, temporary, travel)
- Device management and security requirements
- BYOD policy and restrictions
- VPN and secure network access
- Home office setup recommendations
- Data handling and storage procedures
- Web conferencing security practices
- Incident reporting for remote work
- Privacy considerations
- Work-life boundary expectations

**Output includes:**
- Remote Work Security Policy document
- BYOD agreement template
- Device approval checklist
- Home office setup guide
- VPN configuration procedures
- Web conferencing guidelines
- NIST CSF alignment (PR-1, PR-2, PR-3, DE-1)

**Use when:** You need to establish security standards for remote workers, define BYOD rules, and balance employee flexibility with organizational security requirements.

## Skills Reference

### policy-generator (Core Skill)
The production-ready policy generation engine behind all policy commands.

**What it does:**
- Generates complete, customizable policy documents
- Ensures NIST CSF 2.0 alignment
- Creates implementation checklists and role matrices
- Provides tool-specific guidance for common platforms
- Includes legal disclaimers and enforcement procedures

**Invoked by:** All policy commands (aup, irp, password-policy, data-classify, remote-work-policy)

**You don't call this directly;** it's used by the policy commands automatically.

## Agents Reference

### policy-auditor (Policy Audit Agent)
Evaluates existing policies against NIST CSF 2.0 and best practices.

**What it does:**
- Analyzes your existing policies
- Maps coverage to NIST CSF 2.0 categories
- Identifies critical gaps and compliance issues
- Generates prioritized remediation recommendations
- Creates implementation roadmap with timelines

**How to use:**
1. Provide your existing policy document(s)
2. Agent analyzes and identifies gaps
3. Receive detailed audit report with findings and recommendations
4. Use recommendations to prioritize policy updates

**Output includes:**
- NIST CSF 2.0 coverage analysis
- Gap analysis by policy type
- Industry-specific findings
- Prioritized remediation roadmap
- Action plan with owners, timelines, and success metrics

**Use when:** You have existing policies and want to understand compliance gaps, identify improvement priorities, or prepare for audits.

## Variables Reference

All policies use 8 XML variables for customization. Provide these values when generating policies:

| Variable | Purpose | Example |
|----------|---------|---------|
| **company_name** | Legal organization name | "Acme Corporation" |
| **industry** | Industry classification | Technology, Healthcare, Finance, etc. |
| **employee_count** | Total FT/PT employees | 50, 150, 300, etc. |
| **primary_systems** | Key systems/platforms | "M365, AWS, Salesforce, on-prem servers" |
| **current_challenges** | Known security gaps | "Shadow IT, unclear password standards" |
| **risk_profile** | Organizational risk appetite | Low, Medium, High |
| **geographic_scope** | Operating jurisdictions | "US only" or "US + EU + Canada" |
| **budget_tier** | Implementation resource level | Lean, Standard, Comprehensive |

## Usage Examples

### Example 1: Generate AUP for Tech Startup
```
Command: /aup

Variables:
<company_name>TechStart Innovations Inc.</company_name>
<industry>Technology</industry>
<employee_count>45</employee_count>
<primary_systems>Microsoft 365, GitHub, AWS</primary_systems>
<current_challenges>Rapid growth, new employees unfamiliar with policies, social media risks</current_challenges>
<risk_profile>Medium</risk_profile>
<geographic_scope>United States only</geographic_scope>
<budget_tier>Standard</budget_tier>

Result: Complete AUP ready for customization, including implementation checklist and training materials
```

### Example 2: Generate IRP for Healthcare Practice
```
Command: /irp

Variables:
<company_name>Healthy Valley Medical Associates</company_name>
<industry>Healthcare</industry>
<employee_count>35</employee_count>
<primary_systems>Epic EHR, Microsoft 365, RingCentral, encrypted file servers</primary_systems>
<current_challenges>No formal incident response team, unclear HIPAA breach notification process, limited IT staff</current_challenges>
<risk_profile>High</risk_profile>
<geographic_scope>United States only</geographic_scope>
<budget_tier>Lean</budget_tier>

Result: IRP with healthcare-specific incident types, HIPAA breach notification procedures, escalation matrix with clinical leadership
```

### Example 3: Generate Password Policy for Finance Company
```
Command: /password-policy

Variables:
<company_name>Secure Finance Partners LLC</company_name>
<industry>Finance</industry>
<employee_count>120</employee_count>
<primary_systems>Microsoft 365, Okta SSO, on-premises Active Directory, custom banking systems</primary_systems>
<current_challenges>Legacy systems don't support MFA, users struggling with password complexity, inconsistent across departments</current_challenges>
<risk_profile>High</risk_profile>
<geographic_scope>United States only</geographic_scope>
<budget_tier>Comprehensive</budget_tier>

Result: Password policy with M365/AD-specific MFA deployment, legacy system workarounds, phased rollout timeline
```

### Example 4: Audit Existing Policies
```
Command: /policy-auditor

Provide: Your existing policy document(s)

Result: Comprehensive audit report showing:
- NIST CSF 2.0 coverage gaps
- Missing policy sections
- Inconsistencies and enforcement issues
- Prioritized remediation roadmap with timelines
```

## NIST CSF 2.0 Alignment

All policies align with NIST Cybersecurity Framework 2.0. The framework has 6 functions:

- **Govern (GV)**: Risk management strategy and oversight
- **Identify (ID)**: Asset management and risk assessment
- **Protect (PR)**: Access control and data protection
- **Detect (DE)**: Anomaly detection and monitoring
- **Respond (RS)**: Incident response and recovery
- **Recover (RC)**: Business continuity and restoration

Each policy maps specific sections to relevant CSF categories. See individual policy commands for specific NIST alignments.

## Compliance & Legal Considerations

### Important Disclaimers
- **Not Legal Advice**: Policies should be reviewed by qualified legal counsel
- **Industry-Specific Rules**: Some industries (healthcare, finance, etc.) have additional legal requirements
- **Geographic Variations**: Laws differ by jurisdiction; ensure compliance with local regulations
- **Regulatory Mandates**: Some regulations (HIPAA, PCI-DSS, GDPR) may impose stricter requirements than NIST
- **Regular Updates**: Policies should be reviewed and updated annually or after significant incidents

### Legal Review Checklist
Before implementing any policy:
- [ ] Have legal counsel review for compliance with applicable laws
- [ ] Verify industry-specific regulatory requirements (HIPAA, PCI-DSS, GDPR, etc.)
- [ ] Check geographic jurisdiction-specific requirements
- [ ] Ensure employment law compliance (at-will employment, progressive discipline, etc.)
- [ ] Confirm union/collective bargaining agreement compliance if applicable
- [ ] Get executive/board approval per your governance requirements
- [ ] Ensure consistent implementation across the organization

## Complete Kit & Additional Resources

This plugin provides the core policy generation engine. For the **complete kit** including:
- Sample policy outputs (PDF format)
- Implementation guides and case studies
- Policy customization templates
- Incident response playbooks and checklists
- Compliance audit checklist
- Training presentation decks
- Email templates for policy rollout

**Visit:** [Gumroad - SMB Cybersecurity Policy Kit](https://dontewong.gumroad.com/l/smb-cybersecurity-policy-kit)

The paid bundle includes production-ready outputs, detailed implementation guides, and professional templates to accelerate your policy program.

## Support & Feedback

### Getting Help
- Review the individual command documentation (aup, irp, password-policy, data-classify, remote-work-policy)
- Check the policy-auditor agent for gap analysis
- Consult with qualified legal counsel on compliance questions
- Review NIST CSF 2.0 documentation for framework details

### Providing Feedback
- Found a bug or have suggestions? Reach out through the Gumroad page
- Share your policy implementation experience
- Suggest enhancements or additional policy types

## About the Author

**Donte Wong** is a USAF veteran and Director of IT & Cybersecurity with 15+ years of experience in enterprise security, SMB compliance, and security operations. He has helped hundreds of organizations implement practical, cost-effective security programs aligned with industry frameworks.

This kit represents years of experience helping SMBs build mature security programs without the overhead of enterprise-scale solutions.

## License

MIT License - This plugin and associated materials are provided under the MIT License. See LICENSE file for details.

---

**Version:** 1.0.0
**Last Updated:** April 2026
**Support:** [Gumroad](https://dontewong.gumroad.com/l/smb-cybersecurity-policy-kit)
