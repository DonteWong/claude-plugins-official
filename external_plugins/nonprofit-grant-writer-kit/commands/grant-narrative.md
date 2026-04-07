# Grant Narrative Generator

## Description

Generates a 2–3 page foundation-ready grant narrative. Converts your nonprofit's story, programs, and impact into language aligned with funder priorities. Covers problem statement, program description, program theory, evaluation approach, organizational capacity, and sustainability.

**Output:** Funder-ready narrative section ready to paste into RFP templates.

**Time:** 5–15 minutes input, 2–5 minutes to generate, 30–45 minutes to refine.

## Required Variables

Provide the following information in XML format:

```xml
<organization>
  <name></name>
  <ein></ein>
  <mission></mission>
  <target_population></target_population>
  <annual_budget></annual_budget>
  <staff_count></staff_count>
  <founded_year></founded_year>
</organization>

<program>
  <name></name>
  <description></description>
  <problem_statement></problem_statement>
  <target_participants></target_participants>
  <measurable_outcomes></measurable_outcomes>
  <requested_amount></requested_amount>
  <project_period></project_period>
</program>

<funder>
  <name></name>
  <priority_areas></priority_areas>
  <prior_grants></prior_grants>
</funder>
```

## How to Use

1. **Gather your data:**
   - Organization basics (name, mission, budget, staff size, founding year)
   - Program name and detailed description
   - The specific problem your program solves
   - Who you serve (demographics, numbers)
   - What you measure and your results to date
   - How much you're requesting and for what period
   - Funder name and stated priorities

2. **Format the XML** with your organization and program data

3. **Invoke the grant-writer skill** with the grant narrative instructions below

4. **Review and refine:**
   - Replace generic language with your nonprofit's voice
   - Add specific numbers and outcomes
   - Verify funder alignment
   - Check for gaps in program logic

## Command Invocation

**Invoke the grant-writer skill with these instructions:**

---

You are generating a **Grant Narrative** for {org_name}.

Using the provided organization, program, and funder data, create a 2–3 page grant narrative that includes:

### 1. Opening & Problem Statement (250–300 words)
- Lead with the specific problem your program solves
- Use data to demonstrate scope and urgency
- Connect the problem to the funder's stated priorities
- Make it clear why this problem matters *now*

### 2. Program Description & Strategy (400–500 words)
- Describe the program in concrete, specific terms
- Explain *how* your program addresses the problem
- Detail activities, timeline, and participant flow
- Ground everything in your program's actual approach (not generic best practices)

### 3. Program Theory & Evaluation (300–400 words)
- Explain the theory of change: what you do, what happens as a result, and what ultimately changes for beneficiaries
- Be explicit about the causal chain: activity → output → outcome → impact
- Describe how you measure success (specific metrics, frequency, data collection)
- Include evaluation findings to date if you have them

### 4. Organizational Capacity (250–300 words)
- Demonstrate your nonprofit can execute this program
- Reference relevant staff expertise and experience
- Highlight past successes similar to this program
- Mention board governance, financial management, and compliance

### 5. Sustainability (150–200 words)
- Explain how you'll sustain the program after grant funding ends
- Reference diversified revenue sources
- Show that this grant is not a one-time solution, but part of long-term strategy

### Format Requirements
- Use clear, jargon-free language (avoid nonprofit "buzz")
- Use second-level headers for each section
- Keep paragraphs to 4–5 sentences
- Front-load impact: outcomes first, then description
- Connect every claim back to funder priorities

### Critical Notes
- Flag any missing data that would strengthen the narrative
- If evaluation data is incomplete, suggest what metrics to add
- If sustainability strategy is weak, note areas that need development
- Use the nonprofit's actual language and examples; do not invent outcomes

Generate this narrative now.

---

## Output Expectations

You will receive:

1. **Complete grant narrative** (2–3 pages) with all five sections
2. **Embedded guidance notes** where assumptions were made
3. **Refinement suggestions** specific to your program and funder
4. **Standard disclaimer** (see grant-writer skill)

## Next Steps

1. **Review for accuracy** — Does this reflect your nonprofit's actual program and data?
2. **Refine language** — Replace generic language with your nonprofit's voice
3. **Verify funder alignment** — Does this speak to their stated priorities?
4. **Add specific numbers** — Are your outcomes and participant numbers accurate?
5. **Get stakeholder review** — Have program staff and leadership read this
6. **Paste into RFP template** — Insert this narrative into the funder's required format

## Tips for Success

- **Lead with specificity:** "We served 156 first-grade readers from 8 elementary schools in District 4" beats "We serve young children"
- **Show funder alignment:** If the funder prioritizes equity, mention how your program specifically advances equity
- **Demonstrate sustainability:** Vague references to "diversified funding" feel uncertain; specific revenue sources feel real
- **Use data to tell the story:** Numbers ground your narrative and make it memorable
