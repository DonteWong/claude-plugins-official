# Generate Data Classification Policy

## Command Description
Generates a comprehensive Data Classification Policy for your organization. This policy establishes a standardized framework for categorizing organizational data based on sensitivity and value, and defines appropriate security controls, handling procedures, and retention schedules for each classification level.

A clear data classification scheme is foundational to effective information security—it drives access controls, encryption requirements, storage locations, and compliance obligations across your organization.

The generated policy covers:
- 4-tier data classification scheme (Public, Internal, Confidential, Restricted)
- Clear criteria and examples for each tier
- Mandatory handling requirements per tier (access controls, encryption, storage)
- User responsibilities and training needs
- System and technology requirements for each tier
- Data retention and destruction procedures
- Incident procedures specific to each classification level
- NIST CSF 2.0 alignment (GV-1, ID-1, PR-1, PR-2)
- Implementation checklist with data inventory tasks
- Compliance monitoring and audit procedures

## Required Variables
Before generating your policy, you must provide the following information in XML format:

```xml
<company_name>Your Legal Company Name</company_name>
<industry>Technology | Healthcare | Finance | Retail | Manufacturing | Education | Non-profit | Other</industry>
<employee_count>Number of employees (10-500)</employee_count>
<primary_systems>List of key systems (e.g., "Microsoft 365, Salesforce, SharePoint, on-premises file servers, AWS")</primary_systems>
<current_challenges>Existing gaps (e.g., "No clear data classification today", "sensitive data in insecure locations", "inadequate encryption", "unclear retention requirements")</current_challenges>
<risk_profile>Low | Medium | High</risk_profile>
<geographic_scope>Jurisdictions (e.g., "United States only" or "US + EU")</geographic_scope>
<budget_tier>Lean | Standard | Comprehensive</budget_tier>
```

## 4-Tier Classification Scheme
Your policy will establish four clear data tiers with specific security requirements:

### Tier 1: Public
- **Definition**: Information that can be shared externally without security impact
- **Examples**: Marketing materials, public website content, published press releases, annual reports
- **Access**: Unrestricted; anyone inside/outside organization can access
- **Security**: Minimal (standard malware protection)
- **Encryption**: Not required
- **Storage**: Any system (cloud, on-premises)
- **Retention**: Per business/legal requirements
- **Incident Impact**: Low

### Tier 2: Internal
- **Definition**: Information for internal use only; not sensitive but not public
- **Examples**: Internal policies, organizational charts, general business plans, employee directories
- **Access**: All employees; restricted from external parties
- **Security**: Standard controls (user authentication, basic network security)
- **Encryption**: Recommended in transit and at rest
- **Storage**: Company-controlled systems only; no personal devices
- **Retention**: Typically 3-7 years
- **Incident Impact**: Medium (reputational, operational impact)

### Tier 3: Confidential
- **Definition**: Sensitive business information; significant risk if compromised
- **Examples**: Financial records, customer data, product designs, strategic plans, HR records (salaries, reviews)
- **Access**: Need-to-know basis; documented approval required
- **Security**: Strong controls (MFA required, encryption mandatory, access logging)
- **Encryption**: Required in transit and at rest
- **Storage**: Approved secure systems only (Microsoft 365, Salesforce, encrypted databases)
- **Retention**: Per legal/regulatory requirements (3-7 years typical)
- **Incident Impact**: High (financial loss, competitive damage, customer impact)
- **Special Handling**: Regular access reviews, classification labeling

### Tier 4: Restricted
- **Definition**: Highly sensitive information; critical to protect under law/regulation
- **Examples**: Payment card data (PCI-DSS), healthcare records (HIPAA), trade secrets, executive-level information
- **Access**: Executive-only or minimal; formal approval and audit trail required
- **Security**: Maximum controls (encryption, MFA, endpoint protection, comprehensive logging)
- **Encryption**: Required with strong algorithms (AES-256 or equivalent)
- **Storage**: Specialized secure systems only; no cloud unless specifically approved and encrypted
- **Retention**: Per regulatory requirements (often 7+ years)
- **Incident Impact**: Critical (regulatory penalties, legal liability, breach notification requirements)
- **Special Handling**: Enhanced logging, quarterly access reviews, DLP monitoring

## How to Use This Command
1. Provide the 8 required XML variables with your organization's details
2. Specify data types unique to your industry (e.g., "healthcare: patient records, insurance data")
3. Indicate current classification challenges (e.g., "everything is mixed together", "unclear sensitivity levels")
4. Invoke the policy-generator skill with data classification-specific instructions
5. Receive a complete data classification framework

## Policy Generation
The policy-generator skill will be invoked with the following instructions:

**You are generating a Data Classification Policy. Use the expert persona, 8 provided XML variables, and standard output format from the policy-generator skill definition. Apply NIST CSF 2.0 alignment (emphasizing GV-1, ID-1, PR-1, PR-2). Include:**

- **4-Tier Scheme**: Detailed definitions of Public, Internal, Confidential, Restricted with clear criteria
- **Classification Criteria**: Specific factors for assigning data to each tier
- **Data Examples**: Industry-specific examples of each classification tier
- **Handling Requirements**: Access controls, encryption, storage location rules per tier
- **User Responsibilities**: Who classifies data, how often, documentation required
- **System Mapping**: Which systems/tools are appropriate for each tier
- **Data Inventory**: Procedures for cataloging and classifying existing data
- **Retention Schedules**: How long each tier must be retained before destruction
- **Incident Procedures**: Specific incident response steps for each classification level
- **Training**: Employee awareness and responsibility communication
- **Exceptions & Approvals**: Process for justified exceptions with audit trail
- **Industry-Specific Data**: Special handling for [INDUSTRY]-specific sensitive data (healthcare: PHI, Finance: PCI data, etc.)

**Generate the policy in a professional tone suitable for employee handbooks and IT procedures. Ensure practical implementability for a [BUDGET_TIER] resource environment with [EMPLOYEE_COUNT] employees. Include role-specific responsibilities (employees, managers, IT staff, Security Officer).**

## Expected Deliverables
You will receive:
1. **Data Classification Policy Document** - Complete policy with 4-tier scheme and handling requirements
2. **Classification Matrix** - Quick-reference table showing requirements per tier
3. **Data Inventory Template** - Spreadsheet/checklist for cataloging organizational data
4. **User Training Guide** - How to identify and classify sensitive data
5. **NIST CSF Alignment** - Mapping to asset management and data protection controls
6. **Implementation Checklist** - Steps for data discovery, classification, and ongoing management
7. **Storage/System Approval Matrix** - Which systems are approved for each data tier
8. **Compliance Monitoring** - Audit procedures and classification accuracy metrics

## Next Steps
After generation:
1. Review with legal and compliance teams (especially for industry-specific requirements)
2. Obtain executive and departmental leadership sign-off
3. Conduct data discovery and inventory (identify what data you have and where)
4. Classify existing data using the 4-tier scheme
5. Conduct awareness training for all employees
6. Implement technical controls (encryption, access controls, DLP)
7. Review and classify new data as it's created
8. Audit data classification annually and update as data types evolve
9. Review and update policy as regulatory requirements change

## Critical Considerations
- Data often contains multiple classification levels (e.g., a spreadsheet with both internal and restricted data)
- Data can be re-classified upward if sensitivity increases (e.g., internal data about a pending acquisition becomes restricted)
- Retention periods often conflict; err on the side of longer retention to ensure legal/regulatory compliance
- Consider industry-specific regulations (GDPR, HIPAA, PCI-DSS, SOC 2) when determining requirements
- Encrypted data in transit and at rest should use industry-standard algorithms (AES-256, TLS 1.2+)
