# Generate Incident Response Plan

## Command Description
Generates a comprehensive Incident Response Plan (IRP) tailored to your organization. This plan establishes procedures for detecting, analyzing, containing, and recovering from security incidents. A well-defined incident response capability minimizes damage, accelerates recovery, and demonstrates regulatory compliance.

The generated IRP covers:
- Incident severity classification (Critical, High, Medium, Low)
- Escalation matrix and contact procedures
- Response team roles and clear responsibilities
- Investigation and forensics procedures
- Evidence preservation and chain of custody
- Internal and external communications protocols
- Regulatory reporting requirements
- Post-incident review and improvement
- NIST CSF 2.0 alignment (DE-1, DE-3, RS-1, RS-2, RS-3)
- Implementation checklist with playbooks
- Testing and drill procedures

## Required Variables
Before generating your IRP, you must provide the following information in XML format:

```xml
<company_name>Your Legal Company Name</company_name>
<industry>Technology | Healthcare | Finance | Retail | Manufacturing | Education | Non-profit | Other</industry>
<employee_count>Number of employees (10-500)</employee_count>
<primary_systems>List of key systems (e.g., "Microsoft 365, on-premises Windows servers, Salesforce, AWS")</primary_systems>
<current_challenges>Existing gaps (e.g., "No incident response team defined", "unclear communication protocols", "poor evidence preservation")</current_challenges>
<risk_profile>Low | Medium | High</risk_profile>
<geographic_scope>Jurisdictions (e.g., "United States only" or "US + EU")</geographic_scope>
<budget_tier>Lean | Standard | Comprehensive</budget_tier>
```

## Severity Tiers & Escalation Matrix
Your plan will define incident severity with specific escalation rules:

### Severity Levels
- **Critical**: Widespread system compromise, data breach, active attacks, regulatory notification required
- **High**: Significant system impact, potential data loss, limited affected systems
- **Medium**: Isolated system issues, suspicious activity, contained impact
- **Low**: Minor suspicious events, potential false positives, minimal impact

### Escalation Matrix
The plan includes a role-based escalation matrix specifying:
- **Detection Level**: Who first identifies the incident (NOC staff, email alerts, users)
- **Triage Level**: Who validates and classifies severity (IT Support, Security Officer)
- **Incident Commander**: Who coordinates response (Security Lead, IT Manager)
- **Stakeholder Notification**: Who informs affected parties (Communications, Legal, Executive)
- **Executive Escalation**: When C-level involvement is required (for Critical incidents)
- **External Escalation**: When law enforcement/regulators are involved (for data breaches, illegal activity)

## How to Use This Command
1. Provide the 8 required XML variables with your organization's details
2. Specify industry-specific incident types to emphasize (e.g., "healthcare: focus on patient privacy breaches")
3. Invoke the policy-generator skill with IRP-specific instructions
4. Receive a complete incident response framework

## Policy Generation
The policy-generator skill will be invoked with the following instructions:

**You are generating an Incident Response Plan. Use the expert persona, 8 provided XML variables, and standard output format from the policy-generator skill definition. Apply NIST CSF 2.0 alignment (emphasizing DE-1, DE-3, RS-1, RS-2, RS-3). Include:**

- **Severity Tiers**: Define Critical, High, Medium, Low with specific criteria
- **Escalation Matrix**: Clear role-based escalation showing who decides what at each level
- **Response Procedures**: Step-by-step incident handling (detection, triage, containment, investigation, recovery)
- Include tool-specific detection callouts based on primary_systems: Microsoft 365 → Sentinel/Defender XDR incident queues; AWS → CloudTrail anomaly detection + Security Hub findings; Salesforce → Shield Event Monitoring and Real-Time Event Log. Do not leave detection procedures generic.
- **Investigation Protocols**: Evidence preservation, forensics procedures, chain of custody
- **Communication Plans**: Internal (employee notification), external (customers/partners), regulatory (law enforcement, regulators)
- **Contact Directory**: Key personnel, external contacts, escalation procedures
- **Industry-Specific Scenarios**: Tailored incident types for [INDUSTRY]
- **Post-Incident Review**: Root cause analysis, lessons learned, improvement recommendations
- **Testing & Drills**: Tabletop exercises, incident simulations, annual testing schedule
- **Playbooks**: Specific response procedures for top 5 likely incident types

**Generate the plan in a professional tone suitable for internal security operations. Ensure practical implementability for a [BUDGET_TIER] resource environment with [EMPLOYEE_COUNT] employees.**

## Expected Deliverables
You will receive:
1. **Incident Response Plan Document** - Complete IRP with severity tiers and escalation procedures
2. **Escalation Matrix** - Role-based decision table for incident severity classification
3. **Response Playbooks** - Step-by-step procedures for top 5 incident types
4. **Contact Directory Template** - Roles, names, and contact procedures
5. **NIST CSF Alignment** - Mapping to incident detection, response, and recovery controls
6. **Testing Schedule** - Annual drill and tabletop exercise plan
7. **Implementation Checklist** - Team definition, training, and tool deployment

## Next Steps
After generation:
1. Customize escalation matrix with actual roles and contact information
2. Define incident categories specific to your environment (malware, data breach, denial of service, etc.)
3. Develop detailed playbooks for top 3 likely incident types
4. Conduct incident response team training
5. Execute tabletop exercises quarterly
6. Test incident communications annually
7. Review and update plan after every incident and annually
8. Ensure legal compliance for breach notification requirements in your jurisdiction
