# Nonprofit Grant Writer Kit

Generate foundation-ready grant documents for nonprofits. 5 production-ready generators for grant narratives, logic models, budget narratives, letters of inquiry, and funder alignment assessments.

**Built by [Donte Wong](https://dontewong.gumroad.com)** — practitioner, not prompt engineer.

---

## Installation

Install from the official marketplace:

```
/plugin install nonprofit-grant-writer-kit@claude-plugins-official
```

Or browse for "Nonprofit Grant Writer Kit" in `/plugin > Discover` inside Claude Code.

## Quick Start

1. **Install the plugin** (see above)
2. **Gather your data** (organization basics, program details, funder info)
3. **Use the generators** to create foundation-ready documents
4. **Refine and submit** through your funder's portal

---

## The 5 Generators

### 1. Grant Narrative Generator
Creates 2–3 page grant narratives that funders actually read.

**What it generates:**
- Problem statement (grounded in data, aligned to funder priorities)
- Program description and strategy
- Program theory & evaluation approach
- Organizational capacity
- Sustainability plan

**Time:** 5–15 min input + 2–5 min generation + 30–45 min refinement

**Best for:** Full grant proposals, RFP responses, comprehensive program descriptions

---

### 2. Logic Model Generator
Generates funder-ready logic models that show inputs → activities → outputs → outcomes → impact.

**What it generates:**
- Structured logic model with all five components
- Measurement strategy for each outcome level
- Assumptions and external factors
- Visual structure guidance

**Time:** 5–10 min input + 2–3 min generation + 15–20 min refinement

**Best for:** Program design clarity, evaluation planning, RFP responses

---

### 3. Budget Narrative Generator
Translates your nonprofit budget into funder-ready budget narratives that justify spending.

**What it generates:**
- Personnel justification (by position and FTE)
- Fringe benefits explanation
- Direct program cost justification
- Evaluation cost explanation
- Indirect cost justification
- Per-participant cost calculation

**Time:** 10–15 min data prep + 2–3 min generation + 20–30 min review

**Best for:** Grant proposals, budget justification, funding requests

---

### 4. Letter of Inquiry (LOI) Generator
Creates 1–2 page LOIs that get you to the full proposal stage.

**What it generates:**
- Foundation-ready LOI in business letter format
- Opening hook tied to funder priorities
- Problem statement with data
- Program overview
- Impact & outcomes
- Organizational capacity
- Request and timeline
- Call to action

**Time:** 5–10 min input + 1–2 min generation + 10–15 min editing

**Best for:** Foundation pre-screening, quick foundation inquiries, initial outreach

---

### 5. Funder Alignment Summary Generator
Analyzes your nonprofit against a funder's stated priorities *before* you apply.

**What it generates:**
- Funder profile summary
- Alignment analysis by priority area (with strength ratings)
- Structural fit assessment
- Overall alignment rating (Strong/Moderate/Weak)
- Strategic recommendation (apply or reconsider)
- Next steps if you pursue the funder

**Time:** 5 min input + 1 min generation + 5–10 min review

**Best for:** Strategic funding decisions, pre-proposal planning, funder research

---

## Installation & Usage

### Install the Plugin

1. Copy the plugin directory to your Claude Code plugins folder
2. Reference in Claude Code: `/plugin nonprofit-grant-writer-kit`
3. Use the generators as commands

### Basic Workflow

```
1. Research funder (website, 990-PF, grantee list)
2. Run Funder Alignment Summary → decide whether to apply
3. Gather organization & program data
4. Generate Grant Narrative, Logic Model, Budget Narrative
5. Generate LOI for pre-screening
6. Refine all documents
7. Paste into funder's RFP template
8. Submit
```

### Example: Full Grant Application in 3 Hours

```
0:00–0:15  Gather data: org basics, program details, funder info, budget
0:15–0:20  Run Funder Alignment Summary
0:20–0:25  If alignment is strong, continue; if weak, reconsider
0:25–0:35  Generate Grant Narrative
0:35–0:45  Generate Logic Model
0:45–1:00  Generate Budget Narrative
1:00–1:30  Generate LOI (for pre-screening if needed)
1:30–3:00  Refine all documents, verify accuracy, customize
3:00+      Submit
```

---

## Data Reference: Required Variables

Each generator needs data organized into three categories: organization, program, and funder.

### Organization Variables

```
- name: Your nonprofit's legal name
- ein: Employer Identification Number (required for some proposals)
- mission: Your mission statement (1–2 sentences)
- annual_budget: Total annual operating budget
- staff_count: Number of FTE staff
- founded_year: Year organization was established
- target_population: Demographics/characteristics you serve
- address: Street address
- phone: Contact phone
- email: Contact email
- website: Organization website
```

### Program Variables

```
- name: Program or initiative name
- description: What the program does (2–3 sentences)
- problem_statement: The problem your program solves (with data if available)
- target_population: Who participates (specific demographics/numbers)
- target_participants: Number of annual participants
- measurable_outcomes: What you measure (specific metrics)
- requested_amount: Dollar amount of grant request
- project_period: Timeline (e.g., "January 2026–December 2026")
- participants_served: Annual or projected participant numbers
- primary_outcome: Your most important outcome to achieve
```

### Funder Variables

```
- name: Foundation or funder name
- funder_type: Foundation | Government | Corporate | Individual
- stated_priorities: Their funding focus areas
- priority_areas: Specific program areas they fund
- geographic_focus: Geographic areas they fund in
- funding_range: Minimum and maximum grant amounts
- typical_grant_size: Average grant size
- funding_restrictions: What they will NOT fund
- grantee_requirements: 501(c)(3) status, geographic requirements, etc.
- funding_timeline: When they accept applications, when they announce
- has_given_to_you_before: Yes | No
- prior_grants: If yes, describe prior grants received
```

### Budget Variables (for Budget Narrative)

```
- personnel: List of positions, FTE, annual salary
- fringe_benefits: Percentage and components (FICA, health, workers comp, etc.)
- direct_program_costs: Curriculum, materials, participant support, equipment, facilities
- evaluation: Cost and description of evaluation activities
- indirect_costs: Overhead rate or requested percentage
```

---

## Workflow: Grant Narrative

### Input Required
- Organization basics (mission, budget, staff, founding)
- Program details (name, description, problem solved, target population, outcomes)
- Budget information (if including sustainability section)
- Funder information (name, stated priorities)

### Output
- 2–3 page grant narrative with:
  - Opening & problem statement
  - Program description & strategy
  - Program theory & evaluation
  - Organizational capacity
  - Sustainability plan

### Refinement Checklist
- [ ] Problem statement uses real data
- [ ] Program description is specific (not generic)
- [ ] Outcomes are measurable (not aspirational)
- [ ] Funder priorities are directly addressed
- [ ] Organizational capacity section demonstrates capability
- [ ] Sustainability plan is credible
- [ ] Word count fits RFP requirements
- [ ] Language is your nonprofit's voice (not generic grant-speak)

---

## Workflow: Logic Model

### Input Required
- Program name and description
- Inputs: Resources needed (staff, funding, facilities, partnerships, materials)
- Activities: What you actually do (workshops, coaching, case management, etc.)
- Outputs: Direct results (# served, # sessions, # materials)
- Short-term outcomes: Changes in 0–12 months (knowledge, skills, attitudes, behaviors)
- Long-term outcomes: Changes after 12+ months (employment, education, health, housing, income)
- Impact: Ultimate community-level change
- Success metrics: How you measure each level

### Output
- Narrative logic model showing clear causal chain
- Measurement strategy by outcome level
- Visual structure guidance
- Flagged assumptions and external factors

### Refinement Checklist
- [ ] Causal chain is logical (why would activities lead to outcomes?)
- [ ] Outcomes are specific and measurable
- [ ] Short-term vs. long-term outcomes are clearly distinguished
- [ ] Measurement strategy is feasible (can you actually collect this data?)
- [ ] External assumptions are flagged (What external factors matter?)
- [ ] Logic model is realistic (what actually happens, not aspiration)

---

## Workflow: Budget Narrative

### Input Required
- Program name and funding request
- Personnel: positions, FTE, salaries (include % allocation if shared across programs)
- Fringe benefits: percentage and components
- Direct program costs: broken down by category (curriculum, equipment, participant support, etc.)
- Evaluation: costs and measurement approach
- Indirect costs: overhead rate or requested percentage
- Participant numbers (for per-participant cost calculation)

### Output
- 500–800 word budget narrative organized by category
- Per-participant cost calculation
- Reasonableness assessment
- Funder alignment notes

### Refinement Checklist
- [ ] All numbers are accurate (salaries, participant counts, costs)
- [ ] Fringe benefits are realistic for your region
- [ ] Per-participant cost passes "reasonableness" test
- [ ] Every line item connects to program delivery
- [ ] Overhead and administrative costs are justified (not hidden)
- [ ] Budget aligns with funder's priorities (emphasis on direct services vs. overhead)
- [ ] Word count fits RFP requirements

---

## Workflow: Letter of Inquiry (LOI)

### Input Required
- Organization contact info (address, phone, email, website)
- Organization basics (mission, budget, staff, founding, relevant experience)
- Program name and description
- Problem you solve (with data)
- Solution approach (what you do, who you serve, how many)
- Primary outcome and supporting metrics
- Funding request (amount and timeline)
- What makes your organization uniquely positioned
- Funder name and priorities

### Output
- 1–2 page LOI in business letter format ready for submission
- Funder alignment callouts
- Customization guidance for funder-specific LOI formats

### Refinement Checklist
- [ ] Opening hook is compelling (gets them to read the next sentence)
- [ ] Problem statement includes specific data
- [ ] Program description is concrete (not abstract)
- [ ] Outcomes are quantified ("increased from X to Y" not "improved")
- [ ] Funder priorities are directly addressed
- [ ] Organizational capacity is demonstrated (track record, staff, partnerships)
- [ ] Request is clear (amount, timeline, use)
- [ ] Tone is professional and warm (not cold bureaucratic)
- [ ] Length fits funder requirements (verify in their guidelines)

---

## Workflow: Funder Alignment Summary

### Input Required
- Organization basics (mission, budget, staff, programs, target population, service area)
- Program seeking funding (name, description, request, timeline, outcomes)
- Funder information:
  - Name and type (foundation, government, corporate, individual)
  - Stated priorities
  - Geographic focus
  - Funding range and typical grant size
  - Any restrictions or requirements
  - Prior grants (if you've received from them before)

### Output
- 1-page alignment assessment including:
  - Funder profile summary
  - Alignment analysis by priority area (with strength ratings)
  - Structural fit assessment
  - Overall alignment rating (Strong/Moderate/Weak)
  - Strategic recommendation
  - Next steps

### How to Use Results

**Strong Alignment:** Apply confidently. Lead with aligned areas. Emphasize directly.

**Moderate Alignment:** Apply strategically if you have limited alternatives. Lead with strongest alignment. Address gaps authentically.

**Weak Alignment:** Reconsider. Only apply if (1) limited alternatives, (2) you can make compelling case for connection, (3) you have other programs that align better.

### Refinement Checklist
- [ ] Alignment assessment reflects actual funder priorities (not assumptions)
- [ ] Strength ratings (Strong/Moderate/Weak) are justified
- [ ] Gaps are clearly identified
- [ ] Strategic recommendation is actionable
- [ ] If applying, next steps are clear

---

## Tips for Success

### General Best Practices

1. **Be specific:** Funders remember "We served 156 first-grade readers from 8 schools" not "We serve young children"

2. **Use your nonprofit's language:** Don't adopt generic grant-speak. Use your actual program terms, outcome language, and organizational voice.

3. **Lead with outcomes:** Program officers read first paragraphs first. Lead with impact, not program features.

4. **Ground everything in data:** Use actual numbers—participant counts, outcomes, costs. Projections are fine, but ground them in realistic assumptions.

5. **Connect to funder priorities:** Every paragraph should connect to the funder's stated interests. If you don't see a connection, either find one or reconsider the funder.

6. **Demonstrate capacity:** Show you can actually deliver. Reference relevant past successes, staff expertise, partnerships, and track record.

7. **Be transparent about constraints:** Nonprofits operate with resource constraints. Funders respect honesty about what you can and can't do.

8. **Get stakeholder review:** Have your ED, board, and program staff review drafts. These generators are starting points, not finished products.

### Red Flags to Avoid

- Generic language: "We serve underserved communities" (Specific: "We serve 48 unhoused families with children in District X")
- Unsupported claims: "Our program changes lives" (Support: "Participants increased income by average of $8,400 in year following program completion")
- Unclear logic: Outcomes not connected to activities (If you teach job search skills, measure job search and employment, not general well-being)
- Weak organizational capacity: "We are a small nonprofit with big dreams" (Show: "Our ED has 15 years of program leadership experience; our board includes X expertise")
- Misaligned asks: Requesting $500K from a foundation that gives $25K average grants (Do funder research first)
- Sustainability that's vague: "We will pursue diversified funding" (Be specific: "30% government contracts, 40% foundation grants, 20% individual donations, 10% earned revenue")

---

## About the Author

**Donte Wong** has sat on both sides of the grant-making table:

- **As a grantee:** Led nonprofits through multiple grant cycles. Learned what actually works.
- **As a program officer:** Sat in foundation meetings, read hundreds of grant applications, saw what gets funded.
- **As a practitioner:** USAF veteran. Director of IT & Cybersecurity. Understands nonprofit operations and constraints.

"I've seen hundreds of grant applications. I know what program officers actually read first. I know what makes them stop reading. And I know what gets funded. This kit is built from that experience—to give you the same advantage."

[Learn more: dontewong.gumroad.com](https://dontewong.gumroad.com)

---

## Licensing

MIT License. Use freely. Build on this. Share improvements.

---

## Support

Questions? Issues? Suggestions?

Email: [support email if provided]

---

## Updates & Roadmap

**Current version:** 1.0.0

**Planned generators (coming soon):**
- Impact Report Generator (Q3 2026)
- Multi-Year Strategy Generator (Q4 2026)
- Sustainability Plan Generator (Q1 2027)

**How to stay updated:**
- Purchase includes free updates as new generators are added
- No subscription. No recurring charges.

---

**Built by a practitioner, not a prompt engineer. For nonprofits that deserve to spend more time on mission, and less time on paperwork.**
