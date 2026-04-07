# Generate Password & MFA Policy

## Command Description
Generates a comprehensive Password and Multi-Factor Authentication (MFA) Policy for your organization. This policy establishes standards for credential management and implements modern authentication controls to prevent unauthorized account access—one of the most common attack vectors in cybersecurity incidents.

The generated policy covers:
- Password complexity and strength requirements
- Password rotation and expiration rules
- MFA mandate and applicability rules
- Password manager recommendations and requirements
- Single Sign-On (SSO) integration guidance
- Account lockout and recovery procedures
- Tool-specific implementation (Microsoft 365, Google Workspace, AWS, etc.)
- Legacy system workarounds
- NIST CSF 2.0 alignment (PR-1, PR-3)
- Implementation checklist with deployment timelines
- Compliance monitoring and audit procedures

## Required Variables
Before generating your policy, you must provide the following information in XML format:

```xml
<company_name>Your Legal Company Name</company_name>
<industry>Technology | Healthcare | Finance | Retail | Manufacturing | Education | Non-profit | Other</industry>
<employee_count>Number of employees (10-500)</employee_count>
<primary_systems>List of key systems (e.g., "Microsoft 365, Google Workspace, AWS, Okta, on-premises Active Directory")</primary_systems>
<current_challenges>Existing gaps (e.g., "Users struggling with password complexity", "MFA adoption is low", "legacy systems don't support MFA")</current_challenges>
<risk_profile>Low | Medium | High</risk_profile>
<geographic_scope>Jurisdictions (e.g., "United States only")</geographic_scope>
<budget_tier>Lean | Standard | Comprehensive</budget_tier>
```

## Tool-Specific Implementation Guidance
Your policy will include specific configuration steps for your primary authentication systems:

### Microsoft 365
- Azure AD password policies and complexity settings
- MFA enforcement via Microsoft Authenticator or hardware keys
- Conditional Access policies for risky sign-ins
- Legacy authentication blocking recommendations
- Password reset and self-service procedures

### Google Workspace
- Google Cloud Identity password complexity settings
- Authenticator app and hardware security keys
- 2-Step Verification enforcement
- Recovery phone/email procedures
- Advanced security event audit configuration

### AWS (for technical/developer users)
- IAM password policies
- MFA device management
- Hardware security key support (FIDO2)
- Root account protection requirements
- Access key rotation procedures

### On-Premises Active Directory
- Group Policy Object (GPO) configuration
- Fine-grained password policies
- Account lockout thresholds
- VPN/remote access authentication requirements
- Multi-Factor Authentication server integration

### Password Managers
- Organizational password manager recommendation (Bitwarden, 1Password, LastPass, etc.)
- Shared credential vault procedures
- Emergency access protocols
- Master password requirements and backup procedures

## How to Use This Command
1. Provide the 8 required XML variables with your organization's details
2. List all primary authentication systems/platforms you use
3. Specify pain points (e.g., "Users forgetting MFA devices", "legacy systems blocking MFA adoption")
4. Invoke the policy-generator skill with password policy-specific instructions
5. Receive a complete, implementable password policy

## Policy Generation
The policy-generator skill will be invoked with the following instructions:

**You are generating a Password & MFA Policy. Use the expert persona, 8 provided XML variables, and standard output format from the policy-generator skill definition. Apply NIST CSF 2.0 alignment (emphasizing PR-1, PR-3). Include:**

- **Password Standards**: Complexity requirements, length minimums, character diversity rules
- **Rotation Rules**: Expiration periods (or rationale for passwordless approach), prohibited password reuse
- **MFA Mandate**: Which systems require MFA, which user groups, phased rollout plan
- **Tool-Specific Guidance**: Implementation steps for [PRIMARY_SYSTEMS]
- **Password Manager**: Recommendation and organizational policies for shared credential storage
- **Recovery Procedures**: Account lockout, password reset, emergency access protocols
- **Legacy System Workarounds**: How to handle systems that don't support MFA or modern passwords
- **Common Use Cases**: Developers, system accounts, shared accounts (where applicable and justified)
- **Training Requirements**: Employee education on strong passwords and MFA adoption
- **Exceptions & Approvals**: Process for documented exceptions with audit trail
- **Industry-Specific Requirements**: Healthcare (HIPAA), Finance (PCI-DSS), etc.

**Generate the policy in a professional tone suitable for employee handbooks and IT procedures. Ensure practical implementability for a [BUDGET_TIER] resource environment with [EMPLOYEE_COUNT] employees. Prioritize phased MFA adoption to avoid adoption resistance.**

## Expected Deliverables
You will receive:
1. **Password & MFA Policy Document** - Complete policy with tool-specific guidance
2. **Implementation Checklist** - Step-by-step deployment for each platform
3. **Configuration Templates** - Specific settings for M365, Google Workspace, AWS, AD, etc.
4. **User Communication** - Templates for announcing policy and training employees
5. **NIST CSF Alignment** - Mapping to access control and authentication controls
6. **Phased Rollout Plan** - Timeline for MFA adoption by user group
7. **Compliance Monitoring** - Audit procedures and reporting metrics
8. **Recovery Procedures** - Step-by-step account recovery and emergency access

## Next Steps
After generation:
1. Review with IT leadership and legal counsel
2. Customize tool-specific sections with your actual system names and configurations
3. Define phased rollout (e.g., IT staff first, then management, then general employees)
4. Obtain executive sign-off
5. Deploy tool-specific configurations (MFA enforcement, password policies)
6. Conduct employee training and awareness campaigns
7. Implement monitoring and compliance reporting
8. Plan annual policy review and technology updates
9. Document exceptions with audit trail and expiration dates

## Recommended Implementation Order
1. **Week 1-2**: Tool-specific MFA configuration
2. **Week 2-3**: Executive and IT staff MFA adoption (lead by example)
3. **Week 3-4**: All-hands training and communication campaign
4. **Week 4-8**: Phased MFA rollout by department
5. **Week 8-12**: Legacy system workarounds and accommodations
6. **Week 12+**: Monitoring and enforcement
