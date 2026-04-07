# Letter of Inquiry (LOI) Generator

## Description

Generates a 1–2 page Letter of Inquiry (LOI) for foundation pre-screening. LOIs are the tightest form foundations read first—they determine whether you advance to full proposal or get a decline. This generator creates foundation-ready LOIs that capture your program, ask, timeline, and organizational strength in the most compelling format.

**Output:** Complete LOI ready to submit (or adapt to funder-specific LOI formats).

**Time:** 5–10 minutes input, 1–2 minutes to generate, 10–15 minutes to edit.

## Required Variables

Provide the following information in XML format:

```xml
<organization>
  <name></name>
  <ein></ein>
  <mission></mission>
  <annual_budget></annual_budget>
  <staff_count></staff_count>
  <founded_year></founded_year>
  <address></address>
  <phone></phone>
  <email></email>
  <website></website>
</organization>

<program>
  <name></name>
  <description></description>
  <target_population></target_population>
  <problem_statement></problem_statement>
  <solution_approach></solution_approach>
  <participants_served_annually></participants_served_annually>
  <primary_outcome></primary_outcome>
  <requested_amount></requested_amount>
  <project_period></project_period>
</program>

<organizational_strength>
  <relevant_experience></relevant_experience>
  <evaluation_approach></evaluation_approach>
  <board_size></board_size>
  <board_composition_diversity></board_composition_diversity>
  <unique_positioning></unique_positioning>
</organizational_strength>

<funder>
  <name></name>
  <priority_areas></priority_areas>
  <grant_guidelines_url></grant_guidelines_url>
</funder>
```

## How to Use

1. **Gather essential information:**
   - Organization basics (name, mission, budget, staff, founding year, contact info)
   - Program name and 2–3 sentence description
   - The problem you solve
   - Your solution approach (what you do)
   - Annual participants
   - Primary outcome you're targeting
   - Amount requested and project period
   - What makes your organization uniquely positioned for this work
   - How you evaluate success
   - Funder name and priorities

2. **Format the XML** with your data

3. **Invoke the grant-writer skill** with the LOI instructions below

4. **Adapt to funder requirements:**
   - Some foundations have specific LOI formats or word limits
   - Verify length and section requirements in funder guidelines
   - Adjust as needed while maintaining core messaging

## Command Invocation

**Invoke the grant-writer skill with these instructions:**

---

You are generating a **Letter of Inquiry (LOI)** for {org_name} to submit to {funder_name}.

Create a compelling 1–2 page LOI (approximately 500–750 words) following standard business letter format. This LOI should capture {funder_name}'s attention and position {org_name} as a strong candidate for further consideration.

### Format & Structure

**Header**
[Include organization letterhead info: name, address, phone, email, website. Include date and funder contact information if known]

**Salutation**
[Address to Program Officer or "To the Grants Committee" if officer is unknown]

**Opening Paragraph** (3–4 sentences, ~75 words)
- Hook with the problem: State the specific problem your program addresses in concrete terms (not abstract)
- Connect to funder priorities: Reference {funder_name}'s stated interest in {funder_priority_areas}
- Position your request: "We are seeking $X from [Funder] to [specific program outcome]"

**Problem Statement** (2–3 sentences, ~60 words)
- Be specific and data-driven: "In City X, 40% of third-grade readers are reading below grade level, compared to 25% statewide"
- Explain scope and urgency: Why does this problem matter now?
- Avoid doom and gloom; focus on opportunity: This is a solvable problem and we have a solution

**Program Overview** (3–4 sentences, ~100 words)
- Describe what you do in concrete, specific terms
- Include: Who you serve, what activities you offer, how many participants
- Highlight key features that align with funder priorities
- Be specific: "We provide 24 hours of intensive tutoring over 8 weeks" beats "We offer reading support"

**Impact & Outcomes** (2–3 sentences, ~75 words)
- Lead with your primary outcome: "Participants increase reading level by 1.5 grade levels on average" (actual data if available)
- Include supporting metrics: "95% of participants remain enrolled; 78% meet end-of-program reading benchmarks"
- Frame as funder-relevant: How does this outcome align with their priorities?

**Organizational Capacity** (2–3 sentences, ~75 words)
- Demonstrate you can deliver: Reference relevant program experience, staff expertise, or past successes
- Include organizational track record: "Since 2015, [Org] has served X participants and achieved Y results"
- Brief board/governance statement: "Our board provides fiscal oversight and strategic guidance" (shows stability)

**Request & Timeline** (2–3 sentences, ~60 words)
- State the amount: "We are requesting $[X] to [specific use over specific period]"
- Include timeline: "This grant would support [program] from [start date] to [end date]"
- Show sustainability: "This grant represents [X%] of our annual program budget; remaining funding comes from [revenue sources]"

**Closing** (2–3 sentences, ~50 words)
- Express enthusiasm: "We believe [Funder] is an ideal partner for this work"
- Call to action: "We would welcome the opportunity to discuss this proposal further"
- Offer next steps: "We are happy to provide a full proposal, recent evaluation results, or any additional information"

**Sign-off**
[Sincerely, Executive Director name, title, phone, email]

### Key Requirements

1. **Specificity over generality:** Use actual numbers, program names, and measurable outcomes. Avoid "serve vulnerable populations" in favor of "serve 120 first-generation college students from households earning under 200% of poverty line"

2. **Funder alignment:** Connect your program and ask directly to their stated priorities. If they fund education, lead with education impact. If they fund equity, lead with equity outcomes.

3. **Conciseness:** Every sentence should earn its place. No filler, no generic language, no nonprofit clichés.

4. **Credibility:** Ground your claims in actual experience, evaluation data, or partnership. "We've served X participants" is stronger than "We plan to serve X participants"

5. **Urgency without desperation:** Convey why this is timely without begging. "This grant would allow us to expand to 3 new schools this year" is better than "We urgently need this funding"

### Tone Guidance

- Professional and respectful
- Warm and human (not cold bureaucratic)
- Confident in your approach (not tentative)
- Specific and grounded (not aspirational)
- Brief and scannable (program officers read fast)

### Critical Notes

- **No more than 1 page if funder specifies single-page LOI**
- **Check funder LOI guidelines:** Some foundations have specific format/length requirements; verify and adapt
- **Avoid promises you can't keep:** Don't claim outcomes you haven't measured or expansion you're unsure of
- **Let the program speak:** You don't need to be clever or literary; clarity and specificity beat flowery language

Generate this LOI now.

---

## Output Expectations

You will receive:

1. **Complete LOI** (1–2 pages) in business letter format
2. **Funder alignment callouts:** Notes on how well the LOI addresses stated funder priorities
3. **Specificity check:** Flagged any remaining generic language or unsupported claims
4. **Customization guidance:** Specific suggestions for adapting to {funder_name}'s LOI format (if you have their template)
5. **Standard disclaimer** (see grant-writer skill)

## Next Steps

1. **Check funder requirements:** Does {funder_name} have specific LOI format/length requirements? Adapt if needed.
2. **Verify all claims:** Are numbers accurate? Are outcomes measured or projected?
3. **Read aloud:** Program officers scan quickly; test whether your LOI is scannable
4. **Get leadership review:** Has your ED or board president reviewed this?
5. **Adapt to template:** If funder provided LOI template, transfer content to their format
6. **Submit:** Most LOIs are emailed to program officers or submitted through grantmaker portals

## Tips for Success

- **Open strong:** Your first sentence should make program officers want to read the second sentence
- **Use data from day one:** "We serve 40% of struggling readers in 8 schools" beats generic opening
- **Show partnership:** If you work with schools, health centers, or other partners, mention them (shows you're connected)
- **Be human:** "Our participants are X demographic" is less memorable than "Our participants are [Name], a single mom working two jobs, and [Name], a recent immigrant learning to navigate school systems"
- **Quantify impact:** "Increased from 2.1 to 3.4 GPA" is memorable; "improved academic performance" is forgotten
- **Close with warmth:** End with genuine enthusiasm for partnership, not a formal request
