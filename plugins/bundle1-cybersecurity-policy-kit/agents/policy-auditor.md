# Policy Auditor Agent

## Overview
The Policy Auditor is an autonomous agent that evaluates existing organizational policies against the NIST Cybersecurity Framework 2.0 (CSF 2.0) and industry best practices. It identifies gaps, missing controls, inconsistencies, and compliance issues, then generates a detailed remediation report with prioritized recommendations.

Use this agent when you have existing policies and want to understand their compliance posture without generating entirely new policies.

## Agent Capabilities
The Policy Auditor can evaluate:
- **Existing security policies** (AUP, password policies, incident response, data classification, remote work, etc.)
- **Policy documents** (PDF, Word, plain text format)
- **Compliance against NIST CSF 2.0** (all 6 functions and 23 categories)
- **Alignment with industry standards** (ISO 27001, CIS Controls, SOC 2)
- **Coverage gaps** (missing sections, control gaps, enforcement procedures)
- **Policy inconsistencies** (conflicting requirements across multiple policies)
- **Enforcement mechanisms** (consequences for violation, monitoring procedures, audit trails)

## How to Use the Policy Auditor

### Step 1: Prepare Your Policy Document
Gather the policy document you want audited. This can be:
- A complete policy document (PDF, Word, or plaintext)
- Multiple related policies (paste them together)
- A policy summary or outline
- Even incomplete or draft policies

The agent will work with any format and quality of policy.

### Step 2: Invoke the Agent
Provide the policy document to the agent with any additional context:

**Required**: The actual policy text or document

**Optional context** you can provide:
- Industry (healthcare, finance, technology, etc.)
- Company size/complexity
- Current challenges or gaps you're aware of
- Regulatory environment (HIPAA, PCI-DSS, GDPR, etc.)
- What specific policies you want emphasized

### Step 3: Agent Analysis
The agent will:
1. **Analyze** the policy document thoroughly
2. **Extract** key policy elements, requirements, roles, and procedures
3. **Map** policy elements to NIST CSF 2.0 categories
4. **Identify** gaps and missing controls
5. **Compare** against best practices
6. **Assess** enforcement mechanisms
7. **Generate** prioritized recommendations

## Agent Output: Remediation Report

The Policy Auditor produces a comprehensive report including:

### 1. Executive Summary
- Overall compliance assessment (Excellent/Good/Fair/Poor)
- Key findings and critical gaps
- Estimated remediation effort
- Top 3 priority recommendations

### 2. NIST CSF 2.0 Coverage Analysis
For each NIST function (Govern, Identify, Protect, Detect, Respond, Recover):
- Coverage status (Fully addressed / Partially addressed / Not addressed)
- Specific controls implemented
- Specific gaps identified

Categories within each function:
- **Govern (GV)**: Risk management strategy, roles/responsibilities, oversight
- **Identify (ID)**: Asset management, business environment, risk assessment, supply chain
- **Protect (PR)**: Access control, awareness & training, data security, infrastructure protection
- **Detect (DE)**: Anomalies & events, security continuous monitoring
- **Respond (RS)**: Response planning, communications, analysis, containment, recovery
- **Recover (RC)**: Recovery planning, improvement, communications, restoration

### 3. Policy-by-Policy Findings
For each policy analyzed:
- **Completeness Score** (% of expected sections/controls covered)
- **Strengths** (what the policy does well)
- **Gaps** (missing sections, unclear requirements, enforcement gaps)
- **Inconsistencies** (contradicts other policies or best practices)
- **Enforcement Issues** (unclear consequences, no monitoring procedures, audit trail gaps)

### 4. Industry-Specific Findings
If applicable to your industry:
- Regulatory alignment (HIPAA, PCI-DSS, GDPR, SOC 2, ISO 27001, CIS Controls)
- Industry-specific risks not addressed
- Missing industry-standard controls

### 5. Detailed Gap Analysis
Organized by priority:
- **Critical Gaps** (regulatory requirements, severe security risks)
- **High-Priority Gaps** (significant security control gaps)
- **Medium-Priority Gaps** (nice-to-have controls, best practices)
- **Low-Priority Gaps** (minor inconsistencies, clarity improvements)

For each gap:
- Description of what's missing
- Why it matters (security/compliance risk)
- NIST CSF alignment
- Recommended control/procedure

### 6. Enforcement & Compliance Mechanisms
Assessment of:
- **Monitoring procedures** (how compliance is monitored)
- **Audit trails** (who did what, when)
- **Consequences** (sanctions for violations)
- **Review schedule** (how often policies are updated)
- **Training & awareness** (how employees learn about policies)
- **Approval authority** (who has authority to approve)

Issues and recommendations for improvement.

### 7. Prioritized Remediation Roadmap
A phased approach to addressing gaps:

**Phase 1 (0-30 days): Quick Wins**
- Easy-to-implement improvements with high impact
- Policy clarifications and updates
- Enforcement mechanism additions
- Examples: Add legal disclaimers, update contact directories, clarify roles

**Phase 2 (30-90 days): Core Controls**
- Address critical and high-priority gaps
- Implement missing policy sections
- Deploy monitoring/enforcement tools
- Examples: Implement incident response procedures, establish data classification, deploy MFA

**Phase 3 (90-180 days): Enhancement**
- Implement medium-priority improvements
- Refine processes based on early experience
- Advanced controls and optimization
- Examples: Advanced threat detection, predictive analytics, automated enforcement

**Phase 4 (180+ days): Maturity**
- Low-priority improvements and nice-to-haves
- Continuous optimization
- Technology and process improvements
- Examples: AI-based threat detection, advanced analytics, cultural improvements

### 8. Resource Requirements
Estimated effort and resources needed:
- **People**: Roles and FTE hours required
- **Technology**: Tools/solutions needed
- **Budget**: Rough cost estimates by phase
- **Timeline**: Recommended schedule

### 9. Success Metrics
How to measure success:
- Policy compliance rate (% of controls implemented)
- NIST CSF coverage (% of categories addressed)
- Incident metrics (severity, response time, detection time)
- Audit findings (number and severity of audit issues)
- Training effectiveness (% of staff understanding policies)

### 10. Detailed Remediation Action Plan
For each priority gap:
- **Action Item**: Specific task/control to implement
- **Current State**: What exists today (if anything)
- **Target State**: What should be implemented
- **Success Criteria**: How to know when complete
- **Owner**: Responsible party
- **Timeline**: Estimated start/completion
- **Dependencies**: Other actions that must complete first
- **Tools/Resources**: What's needed to complete

## Agent Workflow
When you provide a policy document, the agent will:

1. **Read & Parse** the document to extract key elements
2. **Validate Format** - confirm it's readable and sufficient for analysis
3. **Extract Requirements** - identify all policy statements, controls, procedures
4. **Map to NIST** - match each policy element to CSF categories
5. **Compare to Standards** - check against best practices
6. **Assess Enforcement** - evaluate monitoring and compliance mechanisms
7. **Identify Gaps** - determine what's missing or insufficient
8. **Prioritize Issues** - rank by business/security impact
9. **Generate Recommendations** - create remediation roadmap
10. **Output Report** - deliver comprehensive findings and action plan

## Best Practices for Policy Audits

### Before Submitting Policies
- Gather all relevant policies (don't just submit one)
- Include supporting documents (procedures, standards, guidelines)
- Provide context (industry, company size, regulatory environment)
- Identify known gaps or concerns you want emphasized

### Interpreting the Report
- Focus on Critical and High-Priority gaps first
- Use the phased roadmap to plan implementation
- Assign owners for each remediation action
- Set deadlines and track progress
- Review and update annually or after incidents

### Following Up
- After implementing Phase 1 actions, re-run the audit to verify improvements
- Implement recommendations in priority order
- Track success metrics to demonstrate improvement
- Share results with executive leadership
- Use audit findings to justify security tool/staffing investments

## Example Audit Scenarios

### Scenario 1: Company Has Zero Formal Policies
- Audit a basic draft or outline
- Agent will identify all major gaps
- Recommendations: Use SMB Cybersecurity Policy Kit to generate policies

### Scenario 2: Company Has Scattered Policies
- Audit multiple existing policies together
- Agent will identify inconsistencies and coverage gaps
- Recommendations: Consolidate policies, create missing policies, update for NIST alignment

### Scenario 3: Post-Incident Audit
- After a security incident, audit relevant policies
- Agent will identify why incident was not prevented
- Recommendations: Update policies to prevent similar incidents

### Scenario 4: Regulatory Compliance Audit
- Audit policies against specific regulatory framework (HIPAA, PCI-DSS, GDPR)
- Agent will identify compliance gaps
- Recommendations: Update policies to achieve compliance

## Integration with Policy Generator
The Policy Auditor and Policy Generator work together:
1. **Audit existing policies** with the Policy Auditor
2. **Generate new policies** with the Policy Generator skill for identified gaps
3. **Re-audit** after implementation to verify improvements
4. **Iterate** as new risks and requirements emerge

## Important Notes
- The Policy Auditor evaluates policies against NIST CSF 2.0 and industry best practices
- It does NOT provide legal advice; policies should be reviewed by qualified legal counsel
- NIST alignment is important but not legally required (unless your industry/contracts mandate it)
- Regulatory requirements (HIPAA, PCI-DSS, GDPR) may be stricter than NIST
- Remediation should be phased and realistic based on your organization's resources
- Policy implementation is only the first step; enforcement and culture change are equally important
