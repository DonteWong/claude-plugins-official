# 90-Day Onboarding Checklist Generator

Generate comprehensive 90-day onboarding checklists for both employees and managers.

## Description

Creates two parallel checklists that guide the first 90 days of a new hire's integration into the company. The employee checklist ensures they understand role expectations, complete required training, and meet success milestones. The manager checklist ensures the hiring manager provides structure, feedback, and support to set the employee up for success.

## Command

`/onboarding`

## Required Variables

- `company_name` — Your company's legal name
- `state` — State where employee works (e.g., TX, CA, NY)
- `employee_name` — Full name of new hire
- `employee_title` — Job title
- `start_date` — First day of employment (MM/DD/YYYY)
- `manager_name` — Name of direct manager
- `manager_title` — Manager's job title
- `employment_type` — Full-Time, Part-Time, or Contractor
- `work_arrangement` — In-Office, Remote, or Hybrid
- `department` — Department or team (e.g., Engineering, Sales, Operations)
- `industry` — Industry/business type (e.g., Technology, Healthcare, Retail)
- `team_size` — Number of people on the employee's team
- `primary_responsibilities` — 3-4 main areas of responsibility (e.g., "Customer support, ticket triage, knowledge base management")

## Optional Variables

- `key_projects` — Ongoing projects the employee will work on (if applicable)
- `mentorship_assigned` — Name of assigned mentor or buddy (if applicable)
- `travel_required` — Yes/No; if yes, frequency and expectations
- `direct_reports` — Number of direct reports (if manager role)

## Invokes

**Skill:** `hr-document-generator`

**Instructions:**

Generate comprehensive 90-day onboarding checklists for [EMPLOYEE_NAME] ([EMPLOYEE_TITLE]) at [COMPANY_NAME] starting [START_DATE]. Create two checklists:

---

## DOCUMENT 1: EMPLOYEE ONBOARDING CHECKLIST

**Purpose:** Guide the new hire through their first 90 days with clear milestones, training requirements, and success criteria.

**Structure (organized by week and phase):**

### WEEK 1: ORIENTATION & FOUNDATIONAL SETUP

**Day 1 (First Day):**
- [ ] Welcome and company overview with HR or manager
- [ ] Office/facility tour (if in-office) or virtual walkthrough (if remote)
- [ ] IT setup:
  - [ ] Computer/laptop issued and configured
  - [ ] Email account created and tested
  - [ ] Phone (if applicable) issued
  - [ ] System access and login credentials provided
  - [ ] VPN access (if remote) tested
  - [ ] Required software installed and access verified
  - [ ] Passwords securely stored in password manager
- [ ] Building access (badge, keys, parking, etc. if in-office)
- [ ] Workspace setup (desk, phone, equipment, etc.)
- [ ] Introduction to manager and direct team
- [ ] Emergency contact information updated
- [ ] Benefits enrollment meeting (health insurance, 401k, etc.)
- [ ] Employee handbook review and acknowledgment signed
- [ ] I-9 and tax withholding (W-4) completed
- [ ] Direct deposit setup (if not already completed)
- [ ] Company orientation materials provided (org chart, contact list, policies, etc.)

**Days 2-5:**
- [ ] Attend company orientation or onboarding training (if structured program exists)
- [ ] Meet with HR to review:
  - [ ] Benefits overview (health insurance, retirement, PTO, etc.)
  - [ ] Payroll and pay schedule
  - [ ] Time tracking/timekeeping system (if applicable)
  - [ ] Leave request process
  - [ ] Company policies and code of conduct review
- [ ] Role-specific training begins (tools, systems, processes)
- [ ] Initial 1:1 with manager
  - [ ] Role expectations and primary responsibilities reviewed
  - [ ] Goals for first 90 days discussed
  - [ ] Mentor/buddy assignment introduced (if applicable)
  - [ ] Calendar of check-ins scheduled
- [ ] Mentor/buddy introduction and kick-off
- [ ] Access to training materials, documentation, and knowledge base
- [ ] Internal communication channels joined (Slack, Teams, mailing lists, etc.)
- [ ] Team introductions (video calls or in-person meetings)

### WEEK 2-3: SYSTEM & PROCESS TRAINING

- [ ] Complete product/service training:
  - [ ] Core product/service overview
  - [ ] Customer base and market positioning
  - [ ] Competitive landscape
- [ ] Complete department-specific training:
  - [ ] Key processes and workflows
  - [ ] Tools and systems used in department
  - [ ] Documentation and knowledge base review
  - [ ] Standard operating procedures (SOPs) overview
- [ ] Role-specific training continues
  - [ ] Hands-on training in primary tools
  - [ ] Shadow experienced team member(s)
  - [ ] Practice scenarios or low-stakes tasks
- [ ] Begin small, guided tasks or projects
  - [ ] First task assigned (low complexity, clear success criteria)
  - [ ] Questions documented and discussed with mentor/manager
- [ ] Weekly 1:1 with manager
  - [ ] Progress review
  - [ ] Questions answered
  - [ ] Adjustment to pace or training if needed

### WEEK 4: INDEPENDENT WORK & GOAL SETTING

**30-Day Check-in:**
- [ ] Formal 30-day check-in meeting with manager
  - [ ] Progress review against onboarding plan
  - [ ] Early feedback on performance and fit
  - [ ] Adjustment of goals or expectations if needed
  - [ ] Identification of gaps in training or understanding
- [ ] Begin assigned projects/work independently
  - [ ] First solo project started (manager-approved scope)
  - [ ] Regular check-ins during execution
  - [ ] Manager available for questions
- [ ] Complete any remaining role-specific training
- [ ] Establish regular 1:1 cadence and feedback routine
- [ ] Meet with key cross-functional partners
- [ ] Review and clarification of responsibilities, authorities, and reporting lines

### WEEK 5-8: BUILDING COMPETENCE & INDEPENDENCE

- [ ] Primary project work underway
  - [ ] Increased scope and complexity of tasks
  - [ ] Manager oversight decreases, employee autonomy increases
  - [ ] Quality and speed benchmarks tracking
- [ ] Skill development focus areas
  - [ ] Specific skills identified for growth (per role requirements)
  - [ ] Training or resources provided
  - [ ] Progress tracked
- [ ] Relationship building
  - [ ] Regular interaction with team members
  - [ ] Cross-functional collaboration initiated
  - [ ] Understanding of broader organizational dynamics
- [ ] Process and system mastery
  - [ ] Tools/systems used competently and independently
  - [ ] Troubleshooting basic issues independently
  - [ ] Knowledge of escalation paths for complex issues
- [ ] Bi-weekly 1:1 check-ins continuing
  - [ ] Performance feedback
  - [ ] Growth opportunities identified
  - [ ] Roadblocks addressed

### WEEK 9-12: PROFICIENCY & 90-DAY ASSESSMENT

**60-Day Check-in (Week 8-9):**
- [ ] Formal 60-day feedback conversation with manager
  - [ ] Progress against 30/60/90-day goals
  - [ ] Performance relative to role expectations
  - [ ] Feedback on strengths and areas for development
  - [ ] Plan for final 30 days if needed
- [ ] Independent work continued and expanded
  - [ ] Employee confidently managing assigned responsibilities
  - [ ] Quality of work meets or exceeds standards
  - [ ] Minimal manager oversight needed

**90-Day Final Assessment (Week 12):**
- [ ] Formal 90-day review meeting with manager and HR
  - [ ] Comprehensive review of 90-day performance
  - [ ] Assessment against position requirements and company expectations
  - [ ] Decision: successful completion of onboarding or continuation plan
  - [ ] Long-term development plan and next goals
  - [ ] Benefits/compensation review (if applicable)
- [ ] Documentation of performance assessment in personnel file
- [ ] Celebration of successful onboarding (if applicable)
- [ ] Transition to standard performance management (annual reviews, regular 1:1s)
- [ ] Career development discussion
  - [ ] Long-term growth opportunities
  - [ ] Training or development goals
  - [ ] Career path within company

**Throughout Full 90 Days:**
- [ ] Regular feedback from manager (weekly or bi-weekly)
- [ ] Open communication with mentor/buddy
- [ ] Participation in team meetings and company events
- [ ] Contribution to team projects and deliverables
- [ ] Demonstration of company values and culture fit
- [ ] Questions and concerns addressed promptly
- [ ] Documentation of progress and key milestones

**Success Criteria by 90 Days:**
- [ ] Employee demonstrates understanding of role responsibilities
- [ ] Employee independently completes assigned tasks with acceptable quality
- [ ] Employee integrates with team and culture
- [ ] Employee has met or is on track to meet initial 90-day goals
- [ ] Manager recommends successful completion of onboarding period

---

## DOCUMENT 2: MANAGER ONBOARDING CHECKLIST

**Purpose:** Ensure the hiring manager provides consistent structure, feedback, training, and support to set the new hire up for success.

**Manager Responsibilities:**

### BEFORE FIRST DAY

- [ ] Workspace preparation (desk, phone, computer, supplies)
- [ ] IT setup coordination (hardware, software, system access)
- [ ] Payroll and HR setup complete (tax forms, benefits elections)
- [ ] Building access arranged (badge, keys, parking, etc. if in-office)
- [ ] Team notification (communicate new hire start to team)
- [ ] First week schedule planned:
  - [ ] Your availability confirmed for orientation and check-ins
  - [ ] Team introductions scheduled
  - [ ] Training materials prepared
  - [ ] Mentor/buddy assigned and briefed
- [ ] Onboarding plan documented and ready to share
- [ ] Welcome package or materials prepared (optional)
- [ ] Direct reports (if applicable) prepped for new peer/subordinate

### DAY 1: FIRST DAY ORIENTATION

**Morning:**
- [ ] Greet employee warmly; first impression matters
- [ ] Welcome to the team and role
- [ ] Brief office/facility tour (or virtual if remote)
  - [ ] Restrooms, break room, parking, emergency exits
  - [ ] IT support location (if in-office)
  - [ ] Other relevant facilities
- [ ] Walk to desk/workspace; confirm setup is acceptable
- [ ] IT contact info and support process provided
- [ ] 15-30 minute 1:1 orientation conversation
  - [ ] Outline first day/week schedule
  - [ ] Ask how they're feeling, if they have immediate needs
  - [ ] Explain your management style and 1:1 meeting cadence
  - [ ] Answer immediate questions

**First Week:**
- [ ] Introduce employee to direct team members (group meeting and individual intros)
  - [ ] Each team member: brief conversation, role overview
  - [ ] Team lunch or casual get-together (if in-office)
- [ ] Conduct 1:1 at end of first day or next day
  - [ ] Debrief on first day
  - [ ] Check in on comfort level, IT setup, any issues
  - [ ] Address immediate needs
  - [ ] Confirm schedule and expectations for week 1
- [ ] Provide employee handbook and review key policies
  - [ ] Confirm employee understanding of at-will employment status
  - [ ] Review PTO, benefits, and leave policies
  - [ ] Clarify any questions about company policies

### WEEK 1-2: ORIENTATION & RELATIONSHIP BUILDING

**Manager Actions:**
- [ ] Conduct role expectations conversation
  - [ ] Role responsibilities clearly outlined
  - [ ] Reporting structure and key relationships explained
  - [ ] Authorities and decision-making boundaries defined
  - [ ] Success metrics and performance expectations discussed
- [ ] Provide department overview
  - [ ] Department mission and current priorities
  - [ ] Introduce to key cross-functional partners
  - [ ] Org chart and team structure review
- [ ] Assign mentor/buddy (if applicable)
  - [ ] Confirm mentor is briefed and available
  - [ ] Clarify mentor responsibilities (daily support, questions, system training)
  - [ ] Establish regular buddy meetings (daily first week, then as needed)
- [ ] Conduct first weekly 1:1 (schedule ongoing meetings)
  - [ ] What went well in first few days?
  - [ ] What's confusing or challenging?
  - [ ] What training/info is most urgent?
  - [ ] Confirm understanding of role and expectations
  - [ ] Schedule 1:1s: same time each week, calendared
- [ ] Introduce broader team and cross-functional partners
  - [ ] Key stakeholders identified
  - [ ] Introductory meetings arranged
  - [ ] Relationships facilitated

**Training Coordination:**
- [ ] Identify training needs and create training plan
  - [ ] Product/service training (who delivers, timeline)
  - [ ] Role-specific training (tools, processes, SOPs)
  - [ ] Compliance training (if required)
  - [ ] Department-specific training
- [ ] Coordinate with HR or relevant departments
  - [ ] Benefits orientation scheduled
  - [ ] Payroll and timekeeping process explained
  - [ ] System access and login instructions provided
- [ ] Provide documentation and knowledge base
  - [ ] Department wiki, docs, shared drives access
  - [ ] Process documentation and SOPs
  - [ ] Department contact list and communication channels
  - [ ] Customer/client information (if applicable)

### WEEK 3-4: SKILL BUILDING & FIRST PROJECTS

**30-Day Check-In Meeting (by end of Week 4):**
- [ ] Formal 30-day check-in scheduled with employee
  - [ ] Prepare feedback on first month:
    - [ ] Strengths observed
    - [ ] Areas requiring development or additional training
    - [ ] Pace of onboarding (too fast, too slow, just right?)
    - [ ] Cultural fit and team integration
    - [ ] Early performance against expectations
  - [ ] Solicit feedback from employee
    - [ ] How are they feeling about the role and company?
    - [ ] Any concerns or challenges?
    - [ ] Any gaps in training or support?
  - [ ] Adjust plan if needed (additional training, different pace, role adjustments)
  - [ ] Confirm 30-day goals are on track
  - [ ] Document check-in in personnel file

**Work Assignment & Support:**
- [ ] Assign first meaningful project/task (manager-scoped, clear success criteria)
  - [ ] Task complexity appropriate for new hire (not too simple, not overwhelming)
  - [ ] Clear deliverable and timeline
  - [ ] Success criteria defined
  - [ ] Resources and support identified
- [ ] Provide regular support and feedback
  - [ ] Check in on project at least once during execution (mid-point)
  - [ ] Available to answer questions (don't wait for formal 1:1)
  - [ ] Correct course early if going off track
  - [ ] Provide constructive feedback when complete
- [ ] Increase complexity of assignments as competence increases
  - [ ] Task 2 slightly more complex than Task 1
  - [ ] More autonomy as confidence increases
  - [ ] Manager oversight decreases gradually

### WEEK 5-8: COMPETENCE BUILDING & INDEPENDENCE

**Manager Focus:**
- [ ] Continue 1:1 meetings (weekly or bi-weekly)
  - [ ] Ongoing feedback on performance and progress
  - [ ] Recognition of achievements and milestones
  - [ ] Discussion of challenges and development areas
  - [ ] Career expectations and interests explored
- [ ] Increase work autonomy as employee demonstrates readiness
  - [ ] Assign larger or more complex projects
  - [ ] Reduce frequency of check-ins if appropriate
  - [ ] Let employee take ownership of deliverables
  - [ ] Support without micromanaging
- [ ] Build employee relationships
  - [ ] Facilitate introductions to cross-functional partners
  - [ ] Include in team meetings and group projects
  - [ ] Help navigate organizational dynamics and politics
  - [ ] Support team integration
- [ ] Identify skill development opportunities
  - [ ] Areas where additional training would help
  - [ ] Stretch projects that develop capabilities
  - [ ] Training resources or courses (if available)
  - [ ] Coaching and mentoring on soft skills
- [ ] Observe performance and behavior
  - [ ] Quality of work output
  - [ ] Work habits and productivity
  - [ ] Collaboration and team fit
  - [ ] Problem-solving approach
  - [ ] Communication style
  - [ ] Alignment with company values

### WEEK 9-12: PROFICIENCY ASSESSMENT & FINAL PHASE

**60-Day Check-In (Week 8-9):**
- [ ] Conduct 60-day feedback conversation with employee
  - [ ] Progress against goals and expectations to date
  - [ ] Performance review relative to position requirements
  - [ ] Feedback on strengths and continued development areas
  - [ ] Plan for final 30 days
  - [ ] Any significant concerns identified?
  - [ ] Is completion of onboarding on track?
- [ ] Document 60-day assessment in personnel file

**Final Push (Weeks 9-12):**
- [ ] Maintain regular 1:1 cadence
  - [ ] Ongoing feedback and support
  - [ ] Recognition of progress and achievement
  - [ ] Discussion of development goals and long-term plans
- [ ] Assess readiness for full independence
  - [ ] Can employee perform role independently and competently?
  - [ ] Are performance standards being met or exceeded?
  - [ ] Is team fit and cultural integration solid?
  - [ ] Is employee confident in role?
- [ ] Prepare for 90-day review

**90-Day Final Review (Week 12):**
- [ ] Schedule formal 90-day review meeting with employee and HR
  - [ ] Comprehensive review of 90-day performance
  - [ ] Overall assessment: successful onboarding or continuation plan?
  - [ ] Feedback on strengths, areas for continued growth, and achievements
  - [ ] Long-term development plan and next goals
  - [ ] Career path discussion and growth opportunities
  - [ ] Benefits review or compensation adjustment (if applicable)
- [ ] Document assessment thoroughly in personnel file
  - [ ] Detailed feedback on performance
  - [ ] Copy of assessment provided to employee
  - [ ] Employee signature acknowledging receipt
- [ ] Transition to standard performance management
  - [ ] Regular 1:1 cadence (monthly, quarterly, or as standard for company)
  - [ ] Annual performance reviews
  - [ ] Ongoing feedback and development

### ONGOING THROUGHOUT 90 DAYS: BEST PRACTICES

- [ ] Regular, consistent 1:1 meetings (weekly or bi-weekly, same time)
  - [ ] Safe space for questions, concerns, and feedback
  - [ ] Listen actively and empathetically
  - [ ] Provide clear, constructive feedback (both positive and developmental)
- [ ] Clear communication of expectations
  - [ ] What does good performance look like?
  - [ ] What are priorities vs. nice-to-haves?
  - [ ] How will success be measured?
  - [ ] What's the timeline for full competence?
- [ ] Prompt feedback and course correction
  - [ ] Don't wait for formal reviews to provide feedback
  - [ ] Correct course early if performance is off track
  - [ ] Celebrate wins and progress
  - [ ] Address concerns directly and promptly
- [ ] Support without micromanaging
  - [ ] Be available for questions
  - [ ] Provide resources and training
  - [ ] Let employee make decisions and own work
  - [ ] Intervene only when necessary
- [ ] Cultural integration and team fit
  - [ ] Include in team meetings, social events, projects
  - [ ] Help understand team dynamics and norms
  - [ ] Facilitate peer relationships
  - [ ] Model company values and expected behaviors
- [ ] Continuous documentation
  - [ ] Keep notes of check-ins and feedback
  - [ ] Document key milestones and achievements
  - [ ] Record any performance concerns or gaps
  - [ ] Prepare for 30/60/90-day formal assessments

---

## Example Usage

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
industry: Software/SaaS
team_size: 8
primary_responsibilities: "Customer onboarding, relationship management, account health monitoring, renewal management"
mentorship_assigned: Alex Chen (Senior CSM)
```

**Expected Output:**
- 15-20 page employee onboarding checklist (Week 1-12 activities)
- 10-15 page manager onboarding checklist (30/60/90-day roadmap)
- Clear milestones at 30, 60, and 90 days
- Specific activities and success criteria
- Integration with company handbook and policies
- Ready to execute and track 90-day integration
