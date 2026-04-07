# Budget Narrative Generator

## Description

Generates a funder-ready budget narrative (500–800 words) that justifies every line item in your grant budget. Translates your nonprofit's actual budget into language that explains *why* you're spending money the way you do—connecting budget to program delivery and funder priorities.

**Output:** Budget narrative section ready to paste into grant proposals. Organizes budget by major category with justification for each.

**Time:** 10–15 minutes to organize budget data, 2–3 minutes to generate, 20–30 minutes to review.

## Required Variables

Provide the following information in XML format:

```xml
<organization>
  <name></name>
  <mission></mission>
  <annual_budget></annual_budget>
  <staff_count></staff_count>
</organization>

<program>
  <name></name>
  <requested_amount></requested_amount>
  <project_period></project_period>
  <participants_served></participants_served>
</program>

<budget_details>
  <personnel>
    <item name="position_title" ftes="number" annual_salary="amount">Role description and responsibilities</item>
  </personnel>
  <fringe_benefits>
    <percentage>percentage of personnel costs</percentage>
    <components>List components: FICA, health insurance, workers comp, unemployment, retirement</components>
  </fringe_benefits>
  <direct_program_costs>
    <item name="category" cost="amount">Description and justification</item>
  </direct_program_costs>
  <evaluation>
    <cost></cost>
    <description>What you're measuring and how</description>
  </evaluation>
  <indirect_costs>
    <rate_or_amount></rate_or_amount>
    <components>Shared overhead: admin, utilities, insurance, accounting, HR, facility</components>
  </indirect_costs>
</budget_details>

<funder>
  <name></name>
  <budget_requirements></budget_requirements>
  <indirect_cost_cap></indirect_cost_cap>
</funder>
```

## How to Use

1. **Organize your budget:**
   - Personnel: List each position, FTE, and annual salary
   - Fringe benefits: Calculate as % of personnel (typically 25–35%)
   - Direct program costs: Curriculum, materials, supplies, equipment, participant support, training
   - Evaluation: What you'll measure and what that costs
   - Indirect costs: Your organization's overhead rate (if you have one) or requested % of direct costs

2. **Gather context:**
   - How many people will you serve with this grant?
   - What materials or services does your program require?
   - Are there any special program costs (scholarships, travel, equipment)?
   - What evaluation are you conducting?

3. **Format the XML** with your budget data

4. **Invoke the grant-writer skill** with the budget narrative instructions below

5. **Refine and verify:**
   - Does each line item make sense for serving this population?
   - Are fringe benefits realistic for your region?
   - Is the per-participant cost reasonable?
   - Does evaluation spending align with funder expectations?

## Command Invocation

**Invoke the grant-writer skill with these instructions:**

---

You are generating a **Budget Narrative** for {org_name}'s {program_name} program.

Using the provided budget details, create a 500–800 word budget narrative organized by major budget category. This narrative should justify each category of spending in terms of program delivery and impact.

### Structure

Organize the narrative by these sections:

**PERSONNEL** (if applicable)
[Justify each position by role and program contribution. Example: "The Program Director (1.0 FTE) will oversee daily operations, manage staff, coordinate with partner organizations, and ensure fidelity to program model." Include percentages if staff is shared across multiple programs.]

**FRINGE BENEFITS**
[Explain your fringe rate and major components. Example: "Fringe benefits are calculated at 32% of personnel costs and include FICA taxes (7.65%), health insurance ($12,000/employee), workers compensation, unemployment insurance, and TIAA retirement contributions."]

**DIRECT PROGRAM COSTS**
[Justify each major expense category. Examples:]
- Curriculum & Materials: Describe what you're purchasing, why, and per-unit cost if applicable
- Participant Support: Explain any stipends, transportation, meals, or incentives and why they're essential to program participation
- Equipment: Justify any purchases over $5,000 as program-essential
- Technology: Explain software, hardware, or platform costs and what program use they enable
- Facilities/Supplies: Describe facility needs and ongoing supply costs

**EVALUATION**
[Explain evaluation activities and associated costs. Address: What will you measure? How? Who will collect data? What tools or systems will you use? Why is this evaluation essential to understanding program impact?]

**INDIRECT COSTS**
[If claiming indirect costs, explain your cost allocation methodology and major components: administration, facilities, utilities, insurance, accounting, HR, IT support. Include your indirect cost rate or requested percentage.]

### Key Requirements

1. **Connect budget to program:** For every line item, explain how it serves program delivery and participant outcomes.

2. **Per-participant cost clarity:** If requesting funding for a specific number of participants, calculate per-participant cost for major categories. This helps funders quickly assess reasonableness.

3. **Funder alignment:** If the funder has specific budget guidelines or priorities (e.g., emphasis on direct services vs. overhead), align your narrative to those preferences.

4. **Transparency:** If you're requesting overhead or administrative costs, justify them explicitly. Program officers respect transparent budgets more than inflated program cost percentages.

5. **Realism:** Are your salary assumptions realistic for your region? Does equipment cost what you claim? Do materials quantities match participant numbers?

### Assumptions to Flag

- Are salaries market-rate for your region and nonprofit sector?
- Is fringe realistic? (Government expects ~25–35%, some nonprofits claim higher)
- Are program costs reasonable? (Cost per participant should pass the reasonableness test)
- Did you account for inflation or cost increases over the grant period?
- Are you leveraging any in-kind contributions or partner support that reduces costs?

### Tone Guidance

- Professional and transparent
- Justify, don't apologize (funders expect nonprofits to spend on operations)
- Specific and concrete (not "administrative costs" but "Executive Director oversight at 10% of time = $8,000")
- Aligned to funder priorities (if funder emphasizes direct services, lead with program staff and participant costs)

Generate this budget narrative now.

---

## Output Expectations

You will receive:

1. **Complete budget narrative** (500–800 words) organized by major category
2. **Per-participant cost calculation** for your program
3. **Reasonableness check:** Flagged line items that may raise funder questions
4. **Funder alignment notes:** How well your budget aligns with stated funder expectations
5. **Embedded assumptions** flagged for your review
6. **Standard disclaimer** (see grant-writer skill)

## Next Steps

1. **Verify all numbers:** Is your salary data accurate? Do participant numbers match your program plan?
2. **Check reasonableness:** What is your per-participant cost? How does it compare to similar programs?
3. **Review for transparency:** Have you explained fringe, overhead, and indirect costs clearly?
4. **Align to funder:** If the funder emphasizes direct services, ensure that's where most funding goes
5. **Prepare budget table:** Use this narrative to complete the funder's required budget table/form
6. **Include in proposal:** Paste this narrative into your full proposal or as a standalone budget justification section

## Tips for Success

- **Lead with program staff:** Funders understand that good programs require good people. Lead with personnel justification.
- **Justify overhead openly:** "15% for administrative overhead to provide HR, accounting, and IT support" is stronger than hiding admin costs in program lines
- **Use per-participant metrics:** "Cost per participant is $2,400" is memorable and easily comparable to similar programs
- **Account for all costs:** Don't omit fringe or assume funders will accept artificially low program costs. Budget realistically.
- **Be specific:** "$15,000 for participant transportation" is better than "program costs"; even better: "48 participants × 2 trips/month × 12 months × average fuel cost = $11,520 transportation"
- **Acknowledge constraints:** If your budget is lean, say so ("We are operating this program at 60% of standard costs due to volunteer support and in-kind facilities donation from School District X")
