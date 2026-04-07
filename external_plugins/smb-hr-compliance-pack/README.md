# SMB HR Compliance Document Pack

A comprehensive Claude Code plugin that generates state-compliant HR documents for small and mid-size businesses. Create professional, legally defensible employment documents in minutes.

**5 Production-Ready Generators:**
- Offer Letters
- Employee Handbooks
- Performance Improvement Plans (PIPs)
- Termination Packages (Checklist + Letter + Paycheck Guide)
- 90-Day Onboarding Checklists

---

## Installation

### Install from the official marketplace

```
/plugin install smb-hr-compliance-pack@claude-plugins-official
```

Or browse for "SMB HR Compliance Pack" in `/plugin > Discover` inside Claude Code.

### Plugin structure

```
smb-hr-compliance-pack/
  .claude-plugin/
    plugin.json
  skills/
    hr-document-generator.md
  commands/
    offer-letter.md
    handbook.md
    pip.md
    termination.md
    onboarding.md
  README.md
```

---

## Quick Start

### 1. Generate an Offer Letter

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

**Output:** Professional, state-compliant offer letter ready to send.

---

### 2. Generate an Employee Handbook

```
/handbook

company_name: Innovation Labs, Inc.
company_address: 789 Creative Drive, San Francisco, CA 94105
state: CA
industry: Technology / Software Development
employee_count: 35
employment_type: Full-Time, Part-Time
work_arrangement: Remote
benefits_offered: Health Insurance, 401k, 25 days PTO, Parental Leave, Professional Development Budget
at_will_state: true
company_mission: "Empowering teams through innovative software solutions"
company_values: "Innovation, Transparency, Inclusion, Excellence"
```

**Output:** Complete employee handbook (20-40 pages) ready to distribute.

---

### 3. Generate a Performance Improvement Plan

```
/pip

company_name: Operations Pro, LLC
state: NY
employee_name: Michael Chen
employee_title: Sales Associate
start_date: 06/01/2026
pip_length: 60 days
performance_concerns: "Missed sales quota 3 of 4 months. May sales: $45,000 vs. $70,000 target. Slow customer response times."
improvement_goals: "1) Achieve 90% of monthly sales quota. 2) Respond to customer emails within 24 hours 95% of time. 3) Complete daily follow-up calls. 4) Attend weekly coaching sessions."
support_provided: "Sales coaching (weekly), CRM training, mentoring from top performer, flexible schedule, daily progress check-ins"
check_in_frequency: Weekly
manager_name: Jennifer Martinez
manager_title: Sales Director
```

**Output:** Legally defensible PIP document with clear goals and outcomes.

---

### 4. Generate a Termination Package

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
```

**Output:**
- Comprehensive termination checklist (before, during, after)
- Professional termination letter
- Final paycheck calculation guide

---

### 5. Generate 90-Day Onboarding Checklists

```
/onboarding

company_name: Tech Solutions Inc.
state: WA
employee_name: Jessica Lee
employee_title: Customer Success Manager
start_date: 07/01/2026
manager_name: Robert Martinez
manager_title: VP of Customer Success
employment_type: Full-Time
work_arrangement: Hybrid
department: Customer Success
team_size: 8
primary_responsibilities: "Customer onboarding, relationship management, account health monitoring, renewal management"
mentorship_assigned: Alex Chen (Senior CSM)
```

**Output:**
- Employee onboarding checklist (Week 1-12)
- Manager onboarding checklist (30/60/90-day roadmap)

---

## Variable Reference

### Universal Variables (Used in All Commands)

| Variable | Type | Example | Required |
|----------|------|---------|----------|
| `company_name` | String | Acme Software, Inc. | Yes |
| `state` | String (US state abbrev.) | TX, CA, NY | Yes |
| `employment_type` | String | Full-Time, Part-Time, Contractor | Yes |

### Offer Letter Variables

| Variable | Type | Example | Required |
|----------|------|---------|----------|
| `company_address` | String | 456 Tech Way, Austin, TX 78701 | Yes |
| `employee_name` | String | Sarah Johnson | Yes |
| `job_title` | String | Senior Software Engineer | Yes |
| `start_date` | Date (MM/DD/YYYY) | 06/15/2026 | Yes |
| `salary_or_hourly` | String | "Salary" or "Hourly" | Yes |
| `compensation_amount` | Number | 145000 (salary) or 35 (hourly) | Yes |
| `work_arrangement` | String | In-Office, Remote, Hybrid | Yes |
| `benefits_offered` | String (comma-separated) | Health Insurance, 401k, PTO | Yes |
| `at_will_state` | Boolean | true or false | Yes |

### Handbook Variables

| Variable | Type | Example | Required |
|----------|------|---------|----------|
| `company_address` | String | 789 Creative Drive, San Francisco, CA | Yes |
| `industry` | String | Technology, Retail, Professional Services | Yes |
| `employee_count` | Number | 35 | Yes |
| `work_arrangement` | String | In-Office, Remote, Hybrid | Yes |
| `benefits_offered` | String (comma-separated) | Health Insurance, 401k, PTO, Parental Leave | Yes |
| `at_will_state` | Boolean | true or false | Yes |
| `company_mission` | String | Our mission statement | No |
| `company_values` | String (comma-separated) | Innovation, Transparency, Inclusion | No |

### PIP Variables

| Variable | Type | Example | Required |
|----------|------|---------|----------|
| `employee_name` | String | Michael Chen | Yes |
| `employee_title` | String | Sales Associate | Yes |
| `start_date` | Date (MM/DD/YYYY) | 06/01/2026 | Yes |
| `pip_length` | String | 30 days, 60 days, 90 days | Yes |
| `performance_concerns` | String | Description of specific issues | Yes |
| `improvement_goals` | String | List of 3-5 specific goals | Yes |
| `support_provided` | String | Resources and support offered | Yes |
| `check_in_frequency` | String | Weekly, Bi-weekly | Yes |
| `manager_name` | String | Jennifer Martinez | Yes |
| `manager_title` | String | Sales Director | Yes |
| `performance_context` | String | Background or context (optional) | No |

### Termination Variables

| Variable | Type | Example | Required |
|----------|------|---------|----------|
| `company_address` | String | 234 Market Street, Denver, CO 80202 | Yes |
| `employee_name` | String | David Thompson | Yes |
| `employee_title` | String | Marketing Manager | Yes |
| `employee_hire_date` | Date (MM/DD/YYYY) | 03/15/2022 | Yes |
| `termination_date` | Date (MM/DD/YYYY) | 06/30/2026 | Yes |
| `termination_reason` | String | At-Will, Layoff, Conduct Violation, Resignation | Yes |
| `salary_or_hourly` | String | "Salary" or "Hourly" | Yes |
| `compensation_amount` | Number | 85000 (salary) or 25 (hourly) | Yes |
| `accrued_pto_days` | Number | 12 | Yes |
| `benefits_offered` | String (comma-separated) | Health Insurance, 401k, Dental | Yes |
| `manager_name` | String | Sarah Johnson | Yes |
| `severance_offered` | String | 2 weeks salary, 1 month + extended benefits | No |

### Onboarding Variables

| Variable | Type | Example | Required |
|----------|------|---------|----------|
| `employee_name` | String | Jessica Lee | Yes |
| `employee_title` | String | Customer Success Manager | Yes |
| `start_date` | Date (MM/DD/YYYY) | 07/01/2026 | Yes |
| `manager_name` | String | Robert Martinez | Yes |
| `manager_title` | String | VP of Customer Success | Yes |
| `work_arrangement` | String | In-Office, Remote, Hybrid | Yes |
| `department` | String | Sales, Engineering, Operations | Yes |
| `industry` | String | Technology, Healthcare, Retail | Yes |
| `team_size` | Number | 8 | Yes |
| `primary_responsibilities` | String | 3-4 main job responsibilities | Yes |
| `mentorship_assigned` | String | Name of assigned mentor | No |
| `key_projects` | String | Ongoing projects employee will work on | No |

---

## Output Specifications

### Offer Letter
- **Length:** 1-2 pages
- **Format:** Professional business letter
- **Includes:** Compensation, benefits, at-will language, state-specific disclosures, signature blocks
- **Ready for:** Immediate printing and signing

### Employee Handbook
- **Length:** 20-40 pages (varies by company size and complexity)
- **Format:** Professional document with table of contents
- **Includes:** Company overview, policies, benefits, compliance sections, state-specific alerts
- **Ready for:** Employee distribution

### Performance Improvement Plan
- **Length:** 2-4 pages
- **Format:** Professional business document
- **Includes:** Performance concerns, improvement goals, support resources, check-in schedule, outcomes
- **Ready for:** Employee presentation and signature

### Termination Package
- **Length:** 6-12 pages (3 components)
- **Format:**
  1. Termination Checklist (pre, during, post)
  2. Termination Letter
  3. Final Paycheck Calculation Guide
- **Includes:** Step-by-step procedures, legal protections, state-specific wage/hour rules
- **Ready for:** Immediate execution

### 90-Day Onboarding Checklists
- **Length:** 20-30 pages (2 checklists)
- **Format:**
  1. Employee Onboarding Checklist (Weeks 1-12)
  2. Manager Onboarding Checklist (Leadership guide)
- **Includes:** Day-by-day activities, 30/60/90-day milestones, success criteria
- **Ready for:** Immediate use with new hire

---

## State-Specific Compliance

All documents include state-specific compliance flags and language for:

- **At-Will Employment:** State-specific at-will language and exceptions
- **Wage and Hour:** Overtime rules, minimum wage, break requirements, final paycheck timing
- **Leave Requirements:** PTO, sick leave, FMLA, state-specific leave mandates
- **Harassment and Discrimination:** State-specific protected classes and reporting requirements
- **Termination Procedures:** Advance notice, final paycheck timing, COBRA requirements
- **Industry-Specific Rules:** Variations based on industry type (healthcare, retail, tech, etc.)

---

## Legal Disclaimer

These documents are templates designed to comply with employment laws in your state. They are not a substitute for professional legal counsel.

**Always consult an employment attorney before:**
- Terminating an employee (especially for performance or conduct)
- Implementing significant policy changes
- Handling disability or health-related accommodations
- Addressing discrimination or harassment concerns
- Making changes affecting employee classification

This plugin provides educational templates. The responsibility for legal compliance rests with the employer.

---

## FAQ

### Is this legal advice?
No. This plugin generates templates based on employment law frameworks. It is not a substitute for qualified legal counsel. Always have an attorney review critical documents before use, especially terminations.

### What AI powers this?
Claude (Anthropic). The plugin uses advanced language models to generate professional, legally accurate HR documents tailored to your state and company.

### Do I need technical skills?
No. You fill in a simple form with company details. The system handles the rest. No coding or prompt engineering required.

### How do I update documents if laws change?
Templates are regularly updated to reflect new employment laws and compliance requirements. Updates are made available to all customers at no additional cost.

### Can I customize the output?
Yes. All generated documents are fully editable. Customize to match your company's culture, branding, and specific needs.

### What if I have state-specific questions?
The plugin flags state-specific compliance areas and alerts you when to consult an attorney. When you see a "⚠️ [STATE] Compliance Alert," review that section carefully and consult an attorney if uncertain.

---

## Support

For questions or issues:
- Email: donte@dontewong.com
- Gumroad: https://dontewong.gumroad.com/l/smb-hr-compliance-pack

---

## Author

**Donte Wong**

USAF veteran. Director of IT & Cybersecurity at a $1B+ philanthropic foundation. 15+ years of HR experience across multiple states and industries. Built by a practitioner, not a prompt engineer.

---

## License

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this plugin to use, modify, and distribute it for personal or commercial purposes, provided that proper attribution is given.

---

## Version History

**v1.0.0** (April 2026)
- Initial release
- 5 document generators (Offer Letter, Handbook, PIP, Termination, Onboarding)
- State-specific compliance for all 50 US states
- Legal disclaimers and audit trails

---

## Changelog & Updates

Check this section for updates and new features as they're released.

---

Thank you for using the SMB HR Compliance Document Pack. Built for small businesses by someone who's been there.
