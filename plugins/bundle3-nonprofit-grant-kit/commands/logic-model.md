# Logic Model Generator

## Description

Generates a funder-ready logic model: the structured framework that shows inputs → activities → outputs → outcomes → impact. Program officers use logic models to quickly understand your program theory and verify that your activities actually connect to your intended outcomes.

**Output:** Narrative logic model (1–2 pages) with visual structure reference and alignment explanation.

**Time:** 5–10 minutes input, 2–3 minutes to generate, 15–20 minutes to refine.

## Required Variables

Provide the following information in XML format:

```xml
<organization>
  <name></name>
  <mission></mission>
  <target_population></target_population>
  <annual_budget></annual_budget>
  <staff_count></staff_count>
</organization>

<program>
  <name></name>
  <inputs>
    <!-- What you need to run this program: staff, funding, facilities, partnerships, materials -->
  </inputs>
  <activities>
    <!-- What you actually do: workshops, one-on-one coaching, case management, etc -->
  </activities>
  <outputs>
    <!-- Direct results of activities: # of participants served, # of sessions delivered, # of materials distributed -->
  </outputs>
  <short_term_outcomes>
    <!-- Changes in participants in first 0–12 months: knowledge, skills, attitudes, behaviors -->
  </short_term_outcomes>
  <long_term_outcomes>
    <!-- Changes in participants after 12+ months: employment, educational attainment, health, housing, income -->
  </long_term_outcomes>
  <impact>
    <!-- Ultimate change in target population or community: systemic change, policy change, community-wide shifts -->
  </impact>
  <success_metrics>
    <!-- How you measure each outcome: specific data points, frequency, tools -->
  </success_metrics>
</program>

<funder>
  <name></name>
  <priority_areas></priority_areas>
</funder>
```

## How to Use

1. **Gather your program data:**
   - What do you invest in this program? (staff, space, curriculum, technology, partnerships)
   - What do you actually do? (be specific about activities)
   - What directly results from your activities? (participants served, sessions held, material produced)
   - What changes do participants experience in the short term? (0–12 months)
   - What longer-term changes do you see? (12+ months)
   - What is the ultimate impact you're trying to achieve?
   - How do you measure each of these?

2. **Format the XML** with your program's actual structure

3. **Invoke the logic-model skill** with the logic model instructions below

4. **Refine to reflect reality:**
   - Verify the causal chain makes sense
   - Add specific metrics and measurement methods
   - Simplify overly complex logic models
   - Ensure outcomes are measurable, not aspirational

## Command Invocation

**Invoke the grant-writer skill with these instructions:**

---

You are generating a **Logic Model** for {org_name}'s {program_name} program.

Using the provided program data, create a narrative logic model that clearly shows:
- How inputs lead to activities
- How activities produce outputs
- How outputs create short-term outcomes
- How short-term outcomes lead to long-term outcomes
- How outcomes contribute to ultimate impact

### Structure

Format the logic model as follows:

**INPUTS**
[List and describe the human, financial, and material resources needed to run this program]

**ACTIVITIES**
[Describe what the program actually does; be specific about methods, frequency, and duration]

**OUTPUTS**
[Specify the direct, countable results of activities: number served, deliverables produced, sessions held]

**SHORT-TERM OUTCOMES** (0–12 months)
[Describe what changes participants experience in the short term: knowledge gained, skills developed, attitudes shifted, behaviors changed]

**LONG-TERM OUTCOMES** (12+ months)
[Describe what changes participants experience over time: educational attainment, employment, income, health, housing, relationships]

**IMPACT**
[Describe the ultimate change in the target population or community: systemic change, policy shifts, community-wide improvements]

**MEASUREMENT STRATEGY**
[For each outcome level, specify: metric, data collection method, frequency, responsible party]

### Key Requirements

1. **Causal clarity:** Each arrow should be logical. Why would activities lead to these outputs? Why would outputs lead to these outcomes?

2. **Specificity:** Replace "improved" with "increased by 25%" or "moved from 45% to 70%"

3. **Measurability:** Every outcome should be measurable. If it's not, reframe it.

4. **Funder alignment:** Ensure the logic model connects to {funder_name}'s stated priorities: {funder_priority_areas}

5. **Realism:** Is this what actually happens, or what you hope happens? Ground it in real data or reasonable assumptions.

### Assumptions to Flag

- What are you assuming about participant motivation, program fidelity, external conditions?
- What could go wrong with this logic? (External factors, implementation challenges)
- Are there missing evaluation data that would strengthen this model?

Generate this logic model now.

---

## Output Expectations

You will receive:

1. **Narrative logic model** with all five component sections clearly labeled
2. **Measurement strategy** for each outcome level
3. **Embedded assumptions** flagged for your review
4. **Visual structure guidance** (text description of a visual logic model layout)
5. **Refinement suggestions** for strengthening causal clarity
6. **Standard disclaimer** (see grant-writer skill)

## Next Steps

1. **Verify causal logic:** Does each arrow make sense? Would a program officer understand why activities lead to outcomes?
2. **Check measurement feasibility:** Can you actually measure what you've claimed?
3. **Identify missing data:** What evaluation data would strengthen this model?
4. **Create visual version:** Use the structure guidance to create a visual logic model for your proposal
5. **Share with program staff:** Ensure your team agrees this reflects how the program actually works
6. **Include in proposal:** Paste the narrative version into your grant narrative or proposal narrative section

## Tips for Success

- **Short-term outcomes are about participants; long-term outcomes are about systems:** Don't confuse knowledge gained (short-term) with policy change (long-term)
- **Outputs are countable; outcomes are changes:** "500 participants served" is output; "85% of participants increase job search skills" is outcome
- **Assumptions are not outcomes:** "We assume participants are motivated" is helpful context, not an outcome claim
- **External validity matters:** Be clear about what external factors influence your logic (economic conditions, school policies, community readiness)
- **Use your actual language:** "Increased from 2.5 to 3.2 GPA" is stronger than "improved academic performance"
