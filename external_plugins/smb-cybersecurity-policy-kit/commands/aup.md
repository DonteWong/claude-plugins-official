# Generate Acceptable Use Policy

## Command Description
Generates a comprehensive Acceptable Use Policy (AUP) for your organization. This policy defines appropriate use of company IT resources, systems, and data by employees and contractors. It establishes boundaries between business and personal use while protecting organizational security and reputation.

The generated AUP covers:
- Appropriate use of company computers, networks, and applications
- Personal use allowances and restrictions
- Social media and external communications guidance
- Prohibited activities and content
- Consequences for policy violations
- NIST CSF 2.0 alignment (GV-3, PR-1, PR-2)
- Implementation checklist with role assignments
- Compliance monitoring and audit procedures

## Required Variables
Before generating your AUP, you must provide the following information in XML format:

```xml
<company_name>Your Legal Company Name</company_name>
<industry>Technology | Healthcare | Finance | Retail | Manufacturing | Education | Non-profit | Other</industry>
<employee_count>Number of employees (10-500)</employee_count>
<primary_systems>List of key systems (e.g., "Microsoft 365, on-premises Windows servers, Salesforce")</primary_systems>
<current_challenges>Existing gaps you want addressed (e.g., "Shadow IT adoption, unclear BYOD policies")</current_challenges>
<risk_profile>Low | Medium | High</risk_profile>
<geographic_scope>Jurisdictions (e.g., "United States only")</geographic_scope>
<budget_tier>Lean | Standard | Comprehensive</budget_tier>
```

## How to Use This Command
1. Provide the 8 required XML variables with your organization's details
2. Specify any additional customization needs (e.g., "strong emphasis on social media policy", "include BYOD guidance")
3. Invoke the policy-generator skill with AUP-specific instructions
4. Receive a complete, ready-to-customize policy document

## Policy Generation
The policy-generator skill will be invoked with the following instructions:

**You are generating an Acceptable Use Policy. Use the expert persona, 8 provided XML variables, and standard output format from the policy-generator skill definition. Apply NIST CSF 2.0 alignment (emphasizing GV-3, PR-1, PR-2). Include:**

- Clear definitions of "company resources," "business use," and "personal use"
- Specific examples of prohibited activities (e.g., illegal activity, harassment, competitive intelligence gathering)
- Social media guidance for employees representing the company online
- Consequences framework (coaching, warnings, suspension, termination)
- When primary_systems includes Microsoft 365: explicitly reference Sentinel/Defender XDR correlation rules and DLP alert review procedures in the compliance monitoring section. When primary_systems includes AWS: reference CloudTrail and Security Hub. When primary_systems includes Salesforce: reference Shield Event Monitoring. Make these tool-specific callouts concrete, not generic.
- In the social media section (typically §4.x), add a prominent inline callout: "[LEGAL REVIEW REQUIRED — This section may implicate NLRA §7 protected concerted activity. Have employment counsel review before distribution.]"
- Acknowledgment/sign-off requirement for all employees
- Implementation checklist with distribution, training, and monitoring steps
- Compliance verification procedures

**Generate the policy in a professional tone suitable for employee handbooks. Ensure practical implementability for a [BUDGET_TIER] resource environment with [EMPLOYEE_COUNT] employees.**

## Expected Deliverables
You will receive:
1. **Acceptable Use Policy Document** - Full policy ready for customization and legal review
2. **NIST CSF Alignment Summary** - Mapping of policy sections to framework categories
3. **Implementation Checklist** - Step-by-step deployment plan
4. **Compliance Monitoring Framework** — Tool-specific audit procedures tied to the organization's actual systems (e.g., Sentinel/Defender XDR, CloudTrail, Shield Event Monitoring), with KPI baselines to be established at Day 0 discovery, not left as directional trends
5. **Legal Disclaimer** - Required disclaimer for your organization

## Next Steps
After generation:
1. Review the policy with your legal counsel
2. Customize role names and system names as needed
3. Set review/approval cycle (typically annual)
4. Distribute with acknowledgment requirement
5. Implement compliance monitoring per the checklist
6. Track acknowledgments and conduct refresher training annually
