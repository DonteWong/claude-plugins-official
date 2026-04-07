# Performance Improvement Plan (PIP) Generator

Generate a legally defensible Performance Improvement Plan that clearly documents performance expectations and improvement pathways.

## Description

Creates a state-compliant Performance Improvement Plan (PIP) that outlines specific performance concerns, measurable improvement goals, required support and resources, check-in procedures, and outcomes. A well-documented PIP is essential for protecting the company in performance-based terminations and demonstrates good-faith efforts to help the employee succeed.

## Command

`/pip`

## Required Variables

- `company_name` — Your company's legal name
- `state` — State where employee works (e.g., TX, CA, NY)
- `employee_name` — Full name of employee
- `employee_title` — Job title
- `start_date` — PIP start date (MM/DD/YYYY)
- `pip_length` — Duration of plan (e.g., 30 days, 60 days, 90 days)
- `performance_concerns` — Detailed description of specific performance issues (be specific, not general)
- `improvement_goals` — List of 3-5 specific, measurable goals (e.g., "Complete monthly reports by the 5th of each month with 95% accuracy")
- `support_provided` — Resources and support the company will provide (e.g., training, mentoring, tools, schedule adjustments)
- `check_in_frequency` — How often manager and employee will meet (e.g., Weekly, Bi-weekly)
- `manager_name` — Name of direct manager
- `manager_title` — Manager's job title
- `state` — State where employee works (affects legal language around at-will employment and documentation)

## Optional Variables

- `performance_context` — Any context about circumstances affecting performance (e.g., "Recent personal challenges" or leave situation)
- `previous_feedback_date` — Date of previous informal or formal performance feedback (if applicable)

## Invokes

**Skill:** `hr-document-generator`

**Instructions:**

Generate a legally defensible Performance Improvement Plan for [EMPLOYEE_NAME] ([EMPLOYEE_TITLE]) at [COMPANY_NAME] in [STATE]. The PIP must:

1. **Document Current Performance Issues**
   - Provide specific examples of performance concerns (not vague complaints)
   - Reference previous feedback or conversations if applicable
   - Distinguish between performance deficiencies and behavior/conduct issues
   - Be objective and measurable (e.g., "missed deadlines" not "doesn't seem engaged")

2. **Define Clear, Measurable Improvement Goals**
   - List 3-5 specific goals that are achievable within the PIP timeframe
   - Each goal must include:
     - Specific behavior or outcome to improve
     - Measurable success criteria (how will we know the goal is met?)
     - Deadline for achievement (linked to PIP timeline)
   - Goals should be challenging but realistically achievable

3. **Outline Company Support**
   - Specify resources the company will provide:
     - Training programs
     - Mentoring or coaching
     - Tools or technology
     - Schedule changes (if applicable)
     - Additional oversight or feedback
   - Clarify that support does not guarantee success

4. **Establish Check-in Schedule**
   - Regular check-in meetings (weekly, bi-weekly, etc.)
   - Who will attend (manager, HR, employee)
   - What will be discussed (progress toward goals, obstacles, adjustments)
   - Documentation of each check-in

5. **Clearly State Outcomes**
   - Success outcome: "At the end of the [PIP_LENGTH] period, if all goals are met, the PIP will be lifted and normal performance management will resume."
   - Failure outcome: "If goals are not substantially met by [END_DATE], the company may proceed with additional disciplinary action, up to and including termination of employment."
   - At-will employment reminder: Reaffirm that employment is at-will and termination may occur at any time, with or without a PIP

6. **Include Legal Protections**
   - At-will employment confirmation ([STATE]-specific language)
   - Confidentiality of PIP (keep discussions private)
   - No retaliation statement
   - Opportunity for employee to respond or provide input

7. **Format for Execution**
   - Clear signature blocks for:
     - Employee (acknowledgment of receipt and understanding)
     - Manager
     - HR representative
   - Dates for each signature
   - Statement that employee received a copy

8. **State-Specific Considerations**
   - Ensure language complies with [STATE] at-will employment law
   - Include any state-specific protections (e.g., California's implied contract doctrine)
   - Flag any state-specific considerations for performance documentation

**Additional Guidance:**

- **Tone:** Professional, clear, and supportive. The PIP should feel like an opportunity to improve, not purely punitive.
- **Specificity:** The more specific the concerns and goals, the stronger the legal defensibility.
- **Documentation:** Recommend that the manager keep detailed notes of all check-ins and progress.
- **Realism:** Goals should be achievable with the support provided, but challenging enough to genuinely assess improvement.
- **Next Steps Warning:** Clarify that failure to meet goals may result in termination (be direct about consequences).

**Output Requirements:**
- Length: 2-4 pages (depends on number of goals and complexity)
- Format: Professional business document
- Tone: Firm but fair
- Ready to deliver to employee

---

## Example Usage

```
/pip

company_name: Operations Pro, LLC
state: NY
employee_name: Michael Chen
employee_title: Sales Associate
start_date: 06/01/2026
pip_length: 60 days
performance_concerns: "Michael has missed his monthly sales quota in 3 of the last 4 months. In May, he generated $45,000 in sales against a target of $70,000. Additionally, customer feedback has noted slow response times to inquiries. Email follow-up rate is below team average."
improvement_goals: "1) Achieve minimum 90% of monthly sales quota ($63,000) by July 31, 2026. 2) Respond to customer emails within 24 hours, 95% of the time. 3) Complete daily customer follow-up calls as outlined in role expectations. 4) Attend weekly sales coaching sessions with manager."
support_provided: "Sales coaching sessions (weekly), access to CRM training, mentoring from top performer on team, flexible schedule for cold-calling block, daily check-in on progress"
check_in_frequency: Weekly
manager_name: Jennifer Martinez
manager_title: Sales Director
performance_context: "Michael joined 8 months ago. Performance was strong in months 1-2, declined starting in month 3. No known personal circumstances."
```

**Expected Output:**
- Clear, detailed PIP document
- Specific performance concerns with examples
- 4 measurable improvement goals
- Support resources listed
- Weekly check-in schedule
- Clear success/failure outcomes
- New York at-will employment language
- Signature blocks for all parties
- Ready to present to employee
