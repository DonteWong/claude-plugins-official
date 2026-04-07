# Termination Package Generator

Generate a comprehensive termination package including checklist, termination letter, and final paycheck instructions.

## Description

Creates a complete termination package that includes: a step-by-step termination checklist (before, during, and after the termination meeting), a professionally drafted termination letter, and a final paycheck calculation guide compliant with your state's wage and hour laws. This package protects the company by ensuring proper procedures and documentation.

## Command

`/termination`

## Required Variables

- `company_name` — Your company's legal name
- `company_address` — Full company address
- `state` — State where employee works (e.g., TX, CA, NY)
- `employee_name` — Full name of employee
- `employee_title` — Job title
- `employee_hire_date` — Original hire date (MM/DD/YYYY)
- `termination_date` — Final day of employment (MM/DD/YYYY)
- `termination_reason` — Category of termination (e.g., "At-Will Termination for Performance", "Redundancy/Layoff", "Resignation Acceptance", "Conduct Violation", "Retirement")
- `employment_type` — Full-Time, Part-Time, or Contractor
- `salary_or_hourly` — Either "Salary: $X/year" or "Hourly: $X/hr"
- `compensation_amount` — Annual salary or hourly rate
- `accrued_pto_days` — Number of unused PTO days at termination
- `benefits_offered` — List of benefits the employee had (e.g., Health Insurance, 401k)
- `manager_name` — Name of direct manager or person conducting termination meeting

## Optional Variables

- `severance_offered` — If applicable (e.g., "2 weeks salary", "1 month salary plus extended benefits")
- `final_check_details` — Any special circumstances affecting final paycheck (pending commissions, bonuses, etc.)
- `reference_policy` — Your company's reference policy (e.g., "Name, Dates, Title Only" or "Full References Available")

## Invokes

**Skill:** `hr-document-generator`

**Instructions:**

Generate a comprehensive termination package for [EMPLOYEE_NAME] ([EMPLOYEE_TITLE]) at [COMPANY_NAME] in [STATE], with termination date of [TERMINATION_DATE]. The package must include three components:

---

## COMPONENT 1: TERMINATION CHECKLIST

Create a detailed, step-by-step checklist covering:

**Pre-Termination (Before Meeting):**
- [ ] Verify final employment status and dates in HR system
- [ ] Calculate final paycheck (salary, hourly wages, overtime, bonuses, accrued PTO payout per [STATE] law)
- [ ] Coordinate with payroll: confirm final pay date and delivery method
- [ ] Prepare termination letter (personalized with employee details)
- [ ] Prepare COBRA notice (if applicable, per federal law)
- [ ] Prepare final paycheck documentation
- [ ] Prepare exit survey (optional)
- [ ] Brief manager on termination meeting procedure and talking points
- [ ] Review employee's email and file access (prepare deactivation list)
- [ ] Coordinate with IT: schedule time to disable access after termination meeting
- [ ] Gather all company property: laptop, badge, keys, credit cards, equipment (prepare list)
- [ ] Document any pending work assignments or transition notes
- [ ] Coordinate coverage: brief team about work transitions
- [ ] Notify relevant departments (Payroll, Benefits, IT, Operations)
- [ ] Schedule and prepare private meeting space
- [ ] If layoff, coordinate with any other affected employees
- [ ] Have HR and/or manager present at termination meeting
- [ ] Prepare any separation agreements or confidentiality reminders (if applicable)

**During Termination Meeting:**
- [ ] Conduct meeting in private location
- [ ] Have HR and/or witness present
- [ ] Deliver termination letter in person
- [ ] Explain:
     - Final day of employment
     - Final paycheck (date, amount, what is included)
     - Benefit continuation options (COBRA, etc.)
     - Return of company property
     - Reference policy
     - Non-disparagement expectations (if applicable)
- [ ] Provide written documentation to employee
- [ ] Do NOT engage in extended discussion about the decision (it is final)
- [ ] Collect company property (laptop, badge, keys, equipment)
- [ ] Explain transition procedures (if any handoff needed)
- [ ] Answer questions about final paycheck and benefits only
- [ ] Obtain employee signature on termination letter and any required acknowledgments
- [ ] Inform employee when they can expect final paycheck
- [ ] Escort employee from premises or arrange departure
- [ ] Document meeting in personnel file

**Immediately After Termination:**
- [ ] Deactivate email access (coordinate with IT)
- [ ] Deactivate system access (badge, VPN, software licenses, etc.)
- [ ] Deactivate phone (if company phone)
- [ ] Deactivate benefits (health insurance, 401k, etc., per plan rules)
- [ ] Send COBRA notice to employee's address (if applicable)
- [ ] Process final paycheck with all required deductions
- [ ] Verify final paycheck was delivered by required date ([STATE]-specific rules)
- [ ] Secure employee records in personnel file
- [ ] Document all property returned or not returned
- [ ] If property not returned, document non-return in file
- [ ] Notify payroll of benefits termination date
- [ ] File unemployment documentation (if required by [STATE] or company policy)
- [ ] Arrange reference protocol (if employee requests references)
- [ ] Complete exit interview notes (if conducted)
- [ ] Archive all employee digital files securely

**Post-Termination (After Final Paycheck):**
- [ ] Confirm final paycheck was received by employee
- [ ] Send benefits continuation paperwork (COBRA, etc.) if not already sent
- [ ] Update employee records to reflect termination
- [ ] Flag employee record: "Terminated [DATE]" — reason: [TERMINATION_REASON]
- [ ] Ensure all company information is secured or deleted from employee accounts
- [ ] If applicable, send separation/reference agreement (if company offers)
- [ ] Verify all property has been accounted for
- [ ] If severance was offered, confirm acceptance and documentation
- [ ] Notify relevant external parties if needed (insurance, vendors, etc.)
- [ ] Conduct team communication regarding coverage and transitions

---

## COMPONENT 2: TERMINATION LETTER

Create a professional termination letter that includes:

**Header:**
- Company name and address
- Date
- Employee name and address (on file)

**Body:**

Opening Paragraph:
- Clear statement: "Your employment with [COMPANY_NAME] is terminated effective [TERMINATION_DATE]."

Reason Paragraph (tailored to termination type):
- At-will termination language (reaffirm at-will status)
- If performance-based: reference prior feedback or PIP (if applicable)
- If conduct-based: brief description (avoid extended narrative)
- If layoff: note that position is being eliminated, not a reflection on performance
- If resignation acceptance: acknowledge the employee's notice and termination date

Final Paycheck Information:
- Final paycheck amount (gross)
- Final paycheck date (compliant with [STATE] law—typically same day or within [X] days)
- What is included: wages through [DATE], accrued and unused PTO payout per [STATE] law, any applicable bonuses or commissions
- Deductions: taxes, insurance, 401k, and any other required/authorized deductions
- Delivery method (direct deposit, check, etc.)

Benefits Information:
- Health insurance termination date
- COBRA eligibility notice (if applicable)
- 401k/retirement plan payout or continuation options
- Other benefits status (life insurance, FSA, etc.)

Final Responsibilities:
- Return of all company property (laptop, badge, keys, equipment, etc.) on [TERMINATION_DATE]
- Transfer or transition of ongoing work assignments
- Confidentiality obligations remain in effect
- Non-disparagement expectation (if applicable)
- Final timesheet or expense report submission deadline

Reference and Post-Employment:
- Company's reference policy ([specify: name and dates only, full references, etc.])
- How to request references ([contact person])
- Employee's right to receive explanation of unemployment benefits eligibility

Closing Statement:
- Professional closing
- Non-retaliation statement (employee may pursue legal remedies if applicable)
- Contact information for HR or payroll questions

**Signature Block:**
- Signature line for authorized company representative
- Date
- Typed name and title
- Employee signature (acknowledgment of receipt and understanding)
- Employee signature date

**Tone:** Professional, direct, and respectful. Avoid inflammatory language or extended justifications.

---

## COMPONENT 3: FINAL PAYCHECK CALCULATION GUIDE

Create a detailed guide showing:

**Calculation Worksheet:**

1. **Wages Earned (through [TERMINATION_DATE]):**
   - If salaried: (Annual Salary / 12) × (# months worked in final month, or daily calculation)
   - If hourly: Hourly Rate × Hours Worked (through final day)
   - Regular hours vs. overtime (per [STATE] rules for determining overtime)

2. **Accrued and Unused PTO Payout:**
   - [STATE] law requirement: Is PTO payout required on termination? (Yes/No)
   - Calculation: (Daily PTO Rate or # accrued days) × Day rate
   - Note: [STATE]-specific rules on use-it-or-lose-it vs. mandatory payout

3. **Bonuses and Commissions (if applicable):**
   - Are any bonuses earned but unpaid as of termination date?
   - Are any commissions earned but unpaid? Calculation and timing per employment agreement
   - Note: [STATE]-specific timing requirements for commission/bonus payout

4. **Severance (if offered):**
   - Severance amount (if applicable)
   - Conditions or contingencies (e.g., confidentiality agreement)
   - Timing of severance payout

5. **Deductions (Required and Authorized):**
   - Federal income tax withholding (amount, reference to W-4)
   - Social Security (FICA) — 6.2% (employee portion)
   - Medicare (FICA) — 1.45% (employee portion)
   - State income tax (if applicable in [STATE])
   - Employee health insurance contributions (if any)
   - 401k contributions (if any)
   - Court-ordered garnishments (if any)
   - Other authorized deductions (loan repayments, uniform costs, etc. — verify [STATE] rules)

6. **Gross vs. Net:**
   - Total gross pay (wages + bonuses + commissions + severance)
   - Total deductions
   - Net amount to employee

7. **Special [STATE] Considerations:**
   - [STATE] wage and hour law: Final paycheck timing (same day vs. within [X] days?)
   - [STATE] PTO payout requirements (mandatory payout, carryover rules, etc.)
   - [STATE] reporting requirements (wage statement details, etc.)
   - [STATE] restrictions on deductions (what can/cannot be deducted)

8. **Paycheck Delivery:**
   - Method: Direct deposit, check, etc.
   - Timing: [STATE]-compliant date
   - Confirmation: Document date and method of delivery to employee

**Example Calculation (for reference):**
```
Gross Wages (through 06/30/2026):     $3,461.50
Accrued PTO Payout (12 days):         $1,200.00
                                      -----------
Subtotal:                             $4,661.50

Deductions:
Federal Income Tax:                     ($559.00)
Social Security (6.2%):                 ($289.01)
Medicare (1.45%):                       ($67.59)
State Income Tax:                       ($186.46)
Health Insurance:                       ($250.00)
401k Contribution:                      ($350.00)
                                      -----------
Total Deductions:                     ($1,702.06)

NET FINAL PAYCHECK:                   $2,959.44
```

**Compliance Note:**
- Verify [STATE] law on timing: Does final paycheck need to be issued immediately, same day, or within [X] business days?
- Ensure all required deductions are withheld
- Ensure no impermissible deductions are made (verify [STATE] law)
- Document the calculation for payroll records

---

## State-Specific Alerts

Include alerts for [STATE]-specific termination rules:

```
⚠️ [STATE] Compliance Alert: [Specific requirement]
Example: ⚠️ California Compliance Alert: California requires final paycheck within 24 hours. Accrued and unused PTO must be paid out at the employee's regular rate of pay.
```

---

## Example Usage

```
/termination

company_name: Growth Marketing Group
company_address: 234 Market Street, Denver, CO 80202
state: CO
employee_name: David Thompson
employee_title: Marketing Manager
employee_hire_date: 03/15/2022
termination_date: 06/30/2026
termination_reason: At-Will Termination for Performance
employment_type: Full-Time
salary_or_hourly: Salary
compensation_amount: 85000
accrued_pto_days: 12
benefits_offered: Health Insurance, 401k, Dental, Vision
manager_name: Sarah Johnson
severance_offered: 2 weeks salary
reference_policy: Name, Title, Dates Only
```

**Expected Output:**
- Comprehensive termination checklist (3-4 pages)
- Professional termination letter with final paycheck details
- Final paycheck calculation worksheet with Colorado wage/hour compliance
- COBRA notice template
- Ready to execute the termination procedure
