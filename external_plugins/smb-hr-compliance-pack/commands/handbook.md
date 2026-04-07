# Employee Handbook Generator

Generate a comprehensive, state-compliant employee handbook customized to your company, state, and industry.

## Description

Creates a complete employee handbook (typically 20-40 pages) that covers everything from company culture and policies to state-required compliance provisions. The handbook is a foundational HR document that protects both the company and employees by setting clear expectations and procedures.

## Command

`/handbook`

## Required Variables

- `company_name` — Your company's legal name
- `company_address` — Full company address
- `state` — State where the company operates (e.g., TX, CA, NY)
- `industry` — Industry or business type (e.g., Technology, Retail, Professional Services, Manufacturing)
- `employee_count` — Approximate number of employees (e.g., 25, 50, 100)
- `employment_type` — Employment classifications (e.g., Full-Time, Part-Time, Contractors)
- `work_arrangement` — Primary work setup (e.g., In-Office, Remote, Hybrid)
- `benefits_offered` — Comma-separated list (e.g., Health Insurance, 401k, PTO, Parental Leave, Tuition Reimbursement)
- `at_will_state` — true or false (determines at-will language requirements)

## Optional Variables

- `company_mission` — Your company's mission statement (if you want it included)
- `company_values` — Comma-separated list of core values (e.g., Integrity, Innovation, Collaboration)

## Invokes

**Skill:** `hr-document-generator`

**Instructions:**

Generate a comprehensive employee handbook for [COMPANY_NAME] in [STATE]. The handbook must address all required sections below and be tailored to the company's industry ([INDUSTRY]) and current size ([EMPLOYEE_COUNT] employees).

**Core Sections (Required):**

1. **Welcome and Company Overview**
   - Welcome message from leadership
   - Company mission and values (if provided)
   - Company history (brief)
   - Company culture and commitment to diversity

2. **Employment Relationship**
   - At-will employment statement (state-specific language for [STATE])
   - Employment classification (full-time, part-time, contractor)
   - Right to modify policies
   - Acknowledgment of handbook receipt (must include signature line)

3. **Compensation and Benefits**
   - Pay frequency and pay periods
   - Overtime rules (federal FLSA + [STATE]-specific rules)
   - Benefits overview ([BENEFITS_OFFERED])
   - Health insurance enrollment
   - 401k/retirement plan (if offered)
   - PTO policy (state-required minimums for [STATE])
   - Paid sick leave (state requirements)
   - Other leave policies (bereavement, jury duty, military, etc. per [STATE])

4. **Work Hours and Scheduling**
   - Standard work hours
   - Work arrangement expectations ([WORK_ARRANGEMENT])
   - Flexibility policies (if applicable)
   - Remote work procedures (if applicable)
   - Scheduling practices
   - Meal and break requirements ([STATE]-specific rules)

5. **Time Off and Leave**
   - PTO accrual and usage
   - Sick leave policy
   - Vacation/personal days
   - Holidays (list standard company holidays)
   - Bereavement leave
   - Jury duty
   - Military leave
   - Family and Medical Leave Act (FMLA) notice (if applicable to company size)
   - State-specific leave requirements (e.g., California paid family leave, Texas domestic violence leave)
   - Final paycheck and PTO payout upon termination ([STATE] rules)

6. **Performance and Development**
   - Performance expectations
   - Performance reviews (frequency and process)
   - Performance Improvement Plans (PIP) overview
   - Career development opportunities
   - Training and professional development

7. **Workplace Conduct and Policies**
   - Professional conduct expectations
   - Attendance and punctuality
   - Dress code (if applicable)
   - Confidentiality and proprietary information
   - Social media policy
   - Conflict of interest
   - Technology use (email, internet, devices)
   - Mobile device and bring-your-own-device policy
   - Data security and privacy

8. **Workplace Safety and Health**
   - Workplace safety commitment
   - Injury reporting procedures
   - Workers' compensation (state-required notice)
   - Substance abuse policy
   - Workplace violence prevention
   - Smoking policy
   - Emergency procedures
   - COVID-19 or pandemic protocols (if relevant)

9. **Discrimination, Harassment, and Retaliation**
   - Zero-tolerance discrimination and harassment policy (federal + [STATE] requirements)
   - Protected classes ([STATE]-specific protected statuses)
   - Definition of harassment (sexual and non-sexual)
   - Reporting procedures (multiple reporting channels)
   - Investigation procedures
   - Confidentiality and non-retaliation statement
   - Resources and support

10. **Complaint and Grievance Procedures**
    - How to report concerns or complaints
    - Informal resolution process
    - Formal complaint procedure
    - Investigation timeline
    - Non-retaliation assurance
    - Right to external complaints (EEOC, state labor board, etc.)

11. **Disciplinary Action and Termination**
    - Disciplinary process (may include warnings, suspension, termination)
    - At-will employment reiteration
    - Grounds for termination
    - Termination procedure (if at-will)
    - Final paycheck and benefits continuation (state-specific rules for [STATE])
    - Severance (if company offers)
    - References and exit interviews

12. **Benefits Upon Separation**
    - Final paycheck timing ([STATE] requirements)
    - PTO payout upon termination ([STATE]-specific rules)
    - Health insurance continuation (COBRA notice)
    - 401k/retirement plan distribution
    - Return of company property

13. **State-Specific Compliance Sections**
    - Wage statement/pay stub rights
    - Minimum wage notice
    - Paid leave laws (state-specific)
    - Right to inspect personnel files (if required by [STATE])
    - Any other mandatory disclosures for [STATE]

14. **Acknowledgment and Agreement**
    - Employee acknowledgment of handbook receipt
    - Agreement to follow policies
    - Signature block with date line
    - Confirmation that handbook is not a contract of employment (at-will reaffirmation)

**Format Requirements:**

- Professional document (ready for distribution and printing)
- Clear table of contents with page numbers
- Section headers with consistent formatting
- Plain language (avoid legal jargon where possible, but maintain legal accuracy)
- Readable font and spacing
- Total length: 20-40 pages (typical for company of [EMPLOYEE_COUNT] employees)

**State-Specific Flags:**

Include alert boxes (prefixed with ⚠️) for:
- Any state-specific employment law variations
- Common compliance gaps in [STATE]
- Mandatory provisions required by [STATE] law
- Any industry-specific regulations relevant to [INDUSTRY]

**Tone:**
Professional, welcoming, and clear. The handbook should reflect company culture while maintaining legal rigor.

---

## Example Usage

```
/handbook

company_name: Innovation Labs, Inc.
company_address: 789 Creative Drive, San Francisco, CA 94105
state: CA
industry: Technology / Software Development
employee_count: 35
employment_type: Full-Time, Part-Time
work_arrangement: Remote
benefits_offered: Health Insurance, 401k, 25 days PTO, Parental Leave, Professional Development Budget, Home Office Equipment
at_will_state: true
company_mission: "Empowering teams through innovative software solutions"
company_values: "Innovation, Transparency, Inclusion, Excellence"
```

**Expected Output:**
- Comprehensive employee handbook (25-35 pages typical for 35-person company)
- California-compliant language and disclosures
- Remote work procedures
- State-specific PTO and benefits rules
- Clear at-will employment language
- Discrimination and harassment policy with state-required provisions
- Ready to distribute to employees
