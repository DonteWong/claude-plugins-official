# Generate Remote Work Security Policy

## Command Description
Generates a comprehensive Remote Work Security Policy for your organization. This policy establishes security standards and procedures for employees working outside traditional office environments, including home offices, coffee shops, client sites, and other remote locations.

A well-designed remote work security policy balances employee flexibility with organizational security needs—ensuring sensitive data is protected while maintaining reasonable productivity and work-life boundaries.

The generated policy covers:
- Remote work eligibility and approval process
- Device management and security requirements
- BYOD (Bring Your Own Device) provisions and restrictions
- VPN and secure network access requirements
- Data handling and storage rules for remote environments
- Home office setup recommendations and security controls
- Incident reporting specific to remote work
- Privacy considerations for home-based work
- Communication security and web conferencing protocols
- Compliance with data residency and regulatory requirements
- NIST CSF 2.0 alignment (PR-1, PR-2, PR-3, DE-1)
- Implementation checklist with device onboarding procedures
- Compliance monitoring and audit procedures

## Required Variables
Before generating your policy, you must provide the following information in XML format:

```xml
<company_name>Your Legal Company Name</company_name>
<industry>Technology | Healthcare | Finance | Retail | Manufacturing | Education | Non-profit | Other</industry>
<employee_count>Number of employees (10-500)</employee_count>
<primary_systems>List of key systems (e.g., "Microsoft 365, VPN, Okta, Salesforce, company-issued laptops")</primary_systems>
<current_challenges>Existing gaps (e.g., "Employees using personal devices", "no VPN enforcement", "shadow IT adoption", "unclear data handling on home networks")</current_challenges>
<risk_profile>Low | Medium | High</risk_profile>
<geographic_scope>Jurisdictions (e.g., "United States only" or "US + EU")</geographic_scope>
<budget_tier>Lean | Standard | Comprehensive</budget_tier>
```

## BYOD Section Requirements
Your policy will include a dedicated section addressing Bring Your Own Device (BYOD) usage:

### BYOD Policy Components
- **Eligibility**: Which job roles can use personal devices for work
- **Approved Devices**: OS versions and hardware requirements (iOS 15+, Android 12+, Windows 11, macOS 12+, etc.)
- **Access Restrictions**: Which systems/data can be accessed from BYOD (usually excluding Restricted tier data)
- **Security Requirements**: Password protection, device encryption, latest OS updates, antivirus/malware protection
- **Data Segregation**: Use of mobile device management (MDM) containerization or VPN-only access
- **Compliance**: Data residency requirements, GDPR/CCPA considerations
- **Wipe Procedures**: Remote wipe capability for lost/stolen devices
- **Liability**: Clear statement that personal devices are employee's responsibility
- **Opt-In Process**: Formal agreement required with security acknowledgment
- **Monitoring Limits**: What the organization can/cannot monitor on personal devices

### BYOD Restrictions
- Access limitations for employees handling Protected tier data
- Requirement for company-issued devices in sensitive roles
- Restrictions based on industry requirements (healthcare, finance, etc.)
- Clear approval process for exceptions

## How to Use This Command
1. Provide the 8 required XML variables with your organization's details
2. Specify your remote work status (temporary post-pandemic, permanent hybrid, on-demand, etc.)
3. Indicate BYOD allowances/restrictions you want emphasized
4. Specify any regulatory considerations (healthcare, finance, government contracting, etc.)
5. Invoke the policy-generator skill with remote work policy-specific instructions
6. Receive a complete, implementable remote work security framework

## Policy Generation
The policy-generator skill will be invoked with the following instructions:

**You are generating a Remote Work Security Policy. Use the expert persona, 8 provided XML variables, and standard output format from the policy-generator skill definition. Apply NIST CSF 2.0 alignment (emphasizing PR-1, PR-2, PR-3, DE-1). Include:**

- **Work Arrangement Types**: Full-time remote, hybrid, temporary remote, travel/client sites
- **Eligibility & Approval**: Job roles eligible for remote work, approval authority, documentation
- **Device Management**: Company-issued device requirements, encryption, endpoint protection, mobile device management (MDM)
- **BYOD Section**: Clear policy on personal device usage including:
  - Approved device types and OS versions
  - Access restrictions (which data/systems allowed)
  - Security requirements (device encryption, password, malware protection)
  - Enrollment in MDM or VPN-only restrictions
  - Liability and wipe procedures
  - Opt-in agreement with audit trail
- **Network Access**: VPN requirements, multi-factor authentication, split tunneling restrictions
- **Home Office Setup**: Recommendations for physical security (secure workspace, screen privacy), internet quality, network security
- **Data Handling**: Rules for accessing, storing, and transmitting company data from home/remote locations
- **Web Conferencing & Communications**: Secure video conferencing practices, background selection, screen sharing restrictions
- **Incident Reporting**: How to report lost devices, suspicious activity, security concerns from remote locations
- **Privacy & Monitoring**: Balance between security monitoring and employee privacy expectations; notice requirements
- **Data Residency & Regulatory**: Compliance with GDPR, CCPA, HIPAA, PCI-DSS for remote work
- **Communication Channels**: Use of personal email/messaging apps, restrictions on unapproved platforms
- **Work-Life Boundaries**: Reasonable expectations for off-hours availability while protecting privacy

**Generate the policy in a professional tone suitable for employee handbooks and remote-specific procedures. Ensure practical implementability for a [BUDGET_TIER] resource environment with [EMPLOYEE_COUNT] employees. Balance security requirements with employee autonomy and flexibility.**

## Expected Deliverables
You will receive:
1. **Remote Work Security Policy Document** - Complete policy with BYOD section and work arrangement types
2. **BYOD Agreement Template** - Formal agreement for employees using personal devices
3. **Device Approval Checklist** - Technical requirements for approved devices
4. **Home Office Setup Guide** - Best practices for secure remote workspace
5. **VPN & Network Configuration** - Technical guidance for secure remote access
6. **Web Conferencing Guidelines** - Security practices for Zoom, Teams, Google Meet, etc.
7. **NIST CSF Alignment** - Mapping to access control and endpoint protection
8. **Implementation Checklist** - MDM enrollment, VPN setup, employee training, monitoring procedures
9. **Incident Response for Remote Work** - Special procedures for remote-specific incidents

## Next Steps
After generation:
1. Review with legal counsel and HR regarding employment/privacy laws in your jurisdiction
2. Customize for your specific work arrangement (full remote, hybrid, on-demand)
3. Define approved device types and OS version requirements
4. Obtain executive sign-off
5. Select and deploy Mobile Device Management (MDM) solution if BYOD allowed
6. Configure VPN and multi-factor authentication
7. Conduct employee training emphasizing home office security and data handling
8. Implement monitoring for policy compliance
9. Review and update annually or after significant security incidents

## Critical Considerations
- BYOD raises privacy concerns; ensure BYOD agreement is explicit and legally compliant
- Remote work increases phishing/social engineering risk; emphasize awareness
- Home internet quality varies; consider bandwidth requirements for your business
- Data residency laws (GDPR, CCPA) may restrict cloud storage for certain data types
- Remote workers may have less visibility from IT security team; implement monitoring and alerting
- Time zone differences and always-on culture can impact work-life balance; establish clear boundaries
- Consider industry-specific risks (healthcare: PHI in home office, Finance: customer data on home network)

## Regulatory Considerations by Industry
- **Healthcare (HIPAA)**: Restricted tier data generally NOT allowed on personal devices; secure home office required
- **Finance (PCI-DSS)**: Payment card data restricted to company-issued encrypted devices; bank-grade encryption required
- **Legal**: Client confidential data handling restricted; secure storage requirements
- **Government Contracting**: May require government-approved devices or facilities; review FedRAMP requirements
- **EU Operations (GDPR)**: Data residency may require EU-only storage; Standard Contractual Clauses needed for cloud
