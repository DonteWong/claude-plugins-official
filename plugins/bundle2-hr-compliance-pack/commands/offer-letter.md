# Offer Letter Generator

Generate a state-compliant employment offer letter customized to your company and hire.

## Description

Creates a professional, legally defensible employment offer letter that includes all required disclosures, at-will employment language, and state-specific compliance provisions. The letter is ready to send immediately.

## Command

`/offer-letter`

## Required Variables

- `company_name` — Your company's legal name
- `company_address` — Full company address
- `state` — State where employee will work (e.g., TX, CA, NY)
- `employee_name` — Full name of the employee
- `job_title` — Position title (e.g., Senior Developer, Account Manager)
- `start_date` — First day of employment (date format: MM/DD/YYYY)
- `salary_or_hourly` — Either "Salary: $X" or "Hourly: $X/hr"
- `compensation_amount` — Annual salary or hourly rate (numeric)
- `employment_type` — Full-Time, Part-Time, or Contractor
- `work_arrangement` — In-Office, Remote, or Hybrid (specify days if hybrid)
- `benefits_offered` — Comma-separated list (e.g., Health Insurance, 401k, PTO, Dental, Vision)
- `at_will_state` — true or false (determines at-will language requirements)

## Invokes

**Skill:** `hr-document-generator`

**Instructions:**

Generate a state-compliant offer letter for a new hire in [STATE]. The letter must:

1. Include all required information:
   - Company name and address
   - Employee name, position, start date
   - Compensation (salary or hourly rate) and payment frequency
   - Employment classification (full-time, part-time, contractor)
   - Work arrangement (in-office, remote, hybrid)
   - Benefits (list all provided)
   - Position responsibilities (brief summary)

2. Include state-required disclosures:
   - At-will employment language (required in [STATE] per applicable case law)
   - Wage statement/pay stub disclosure
   - State-specific tax withholding notice (as required)

3. Include compliance sections:
   - Confidentiality and intellectual property assignment (if standard for the company)
   - At-will employment confirmation
   - Acknowledgment of handbook receipt (if handbook exists)
   - Reference to state wage and hour laws

4. Add state-specific flags:
   - Alert for any state-specific employment requirements not mentioned
   - Alert for any non-compete or non-solicitation restrictions (state-specific enforceability)
   - Any mandatory disclosures for [STATE]

5. Format for execution:
   - Professional business letter format
   - Clear signature block for employee and authorized company representative
   - Date line
   - Reference to handbook and company policies

**Output Requirements:**
- Length: 1-2 pages (professional and concise)
- Tone: Professional, warm, welcoming
- Format: Ready to print and sign
- Disclaimers: Minimal (included if state-required)

---

## Example Usage

```
/offer-letter

company_name: Acme Software, Inc.
company_address: 456 Tech Way, Austin, TX 78701
state: TX
employee_name: Sarah Johnson
job_title: Senior Software Engineer
start_date: 06/15/2026
salary_or_hourly: Salary
compensation_amount: 145000
employment_type: Full-Time
work_arrangement: Hybrid (3 days in office)
benefits_offered: Health Insurance, 401k, 20 days PTO, Home Office Equipment
at_will_state: true
```

**Expected Output:**
- Professional offer letter addressed to Sarah Johnson
- Texas at-will employment language
- Clear compensation terms
- Benefits summary
- State-specific compliance flags (if applicable)
- Signature block for both employee and hiring manager
