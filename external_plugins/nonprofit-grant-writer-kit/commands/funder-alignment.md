# Funder Alignment Summary Generator

## Description

Generates a 1-page alignment assessment that analyzes your nonprofit against a specific funder's stated priorities. Identifies alignment gaps *before* you submit, so you know whether to apply, what to emphasize, and what to avoid.

**Output:** Actionable alignment summary with strength/weakness analysis and strategic recommendations.

**Time:** 5 minutes input (funder info + org summary), 1 minute to generate, 5–10 minutes to read and strategize.

## Required Variables

Provide the following information in XML format:

```xml
<organization>
  <name></name>
  <mission></mission>
  <annual_budget></annual_budget>
  <staff_count></staff_count>
  <primary_programs></primary_programs>
  <target_population></target_population>
  <geographic_service_area></geographic_service_area>
  <organizational_type>nonprofit | nonprofit consortium | fiscal sponsor | community organization</organizational_type>
</organization>

<program_seeking_funding>
  <name></name>
  <description></description>
  <requested_amount></requested_amount>
  <project_period></project_period>
  <primary_outcome></primary_outcome>
</program_seeking_funding>

<funder>
  <name></name>
  <funder_type>foundation | government | corporate | individual donor</funder_type>
  <stated_priorities></stated_priorities>
  <geographic_focus></geographic_focus>
  <funding_range></funding_range>
  <typical_grant_size></typical_grant_size>
  <funding_restrictions></funding_restrictions>
  <grantee_requirements></grantee_requirements>
  <funding_timeline></funding_timeline>
  <has_given_to_you_before>yes | no</has_given_to_you_before>
  <prior_grants></prior_grants>
</funder>
```

## How to Use

1. **Research the funder:**
   - Gather their 990-PF or recent grantee list
   - Read their stated priorities, funding guidelines, and grantee requirements
   - Note funding range and typical grant size
   - Identify geographic focus and any restrictions

2. **Describe your organization and program:**
   - Mission and programs
   - Target population
   - Service area
   - Ask amount and timeline

3. **Format the XML** with funder and organizational data

4. **Invoke the grant-writer skill** with the funder alignment instructions below

5. **Use the assessment strategically:**
   - Strong alignment: Apply confidently; emphasize aligned areas
   - Moderate alignment: Apply if other funding is limited; be strategic about emphasis
   - Weak alignment: Consider whether to apply; if you do, identify ways to strengthen connection

## Command Invocation

**Invoke the grant-writer skill with these instructions:**

---

You are analyzing **Funder Alignment** for {org_name} seeking support from {funder_name}.

Create a 1-page alignment assessment that helps {org_name} decide whether to pursue {funder_name}, and if pursuing, where to emphasize and what to avoid.

### Structure

**FUNDER PROFILE** (3–4 sentences)
[Summarize {funder_name}'s funding approach: type of funder, general priorities, funding range, geographic focus, any relevant grantee requirements or restrictions]

**ALIGNMENT ANALYSIS** (organized by priority area)

For each stated priority of {funder_name}, assess:

**[Priority Area]**
- **Your strength here:** How does {org_name} align with this priority? Cite specific programs, outcomes, or positioning
- **Strength rating:** Strong | Moderate | Weak (based on program fit and demonstrated track record)
- **Strategic emphasis:** If pursuing this funder, where in your narrative should you emphasize this alignment?
- **Gaps:** Are there misalignments or areas where your program doesn't fit their priorities?

[Repeat for each stated priority]

**STRUCTURAL FIT** (2–3 sentences)
- Does your funding ask align with their typical grant range? (e.g., "You're requesting $75K; their average grant is $35K—this is on the high end but potentially fundable if impact is strong")
- Are there geographic, organizational, or grantee requirements you meet or don't meet?
- Is your timeline compatible with their funding cycle?

**TRACK RECORD** (if applicable)
[If {funder_name} has given to {org_name} before, note: prior grants, amounts, outcomes. This is a strong signal for reapplication.]

**OVERALL ALIGNMENT RATING**

Rate as: **Strong** | **Moderate** | **Weak**

[Provide 2–3 sentence rationale for the rating]

**STRATEGIC RECOMMENDATION**

Based on alignment analysis:

- **If Strong alignment:** "We recommend applying. In your narrative, lead with [specific alignment area]. Emphasize [program outcome] as it directly addresses [funder's priority]. Ensure you address any gaps in [area]."

- **If Moderate alignment:** "Alignment is strong in [area] but weak in [area]. Consider applying if: (1) this funder is a significant funding source, (2) you can credibly emphasize strong areas, and (3) you can address gaps without distorting your program. If applying, be strategic: lead with [strong area], but authentically address [weak area] by [specific strategy]."

- **If Weak alignment:** "This funder appears to be a poor fit for [program]. Consider: (1) Is there a different program within {org_name} that aligns better? (2) Are there other funders whose priorities align more closely? (3) If you pursue this funder despite weak alignment, you'll need to make a compelling case for [area]. Proceed only if you have limited alternatives."

**NEXT STEPS**

If you decide to pursue {funder_name}:
1. Obtain their full LOI/proposal template and grantee guidelines
2. Use Grant Narrative, Logic Model, and LOI generators to create aligned documents
3. In your narrative, lead with [recommended priority area]
4. Address any gaps in [area] by emphasizing [specific strength]
5. Before submission, do a final alignment check against the full RFP

**DATA SOURCES FOR ALIGNMENT ASSESSMENT**

[Note: This assessment is based on publicly available information: {funder_name}'s website, 990-PF, recent grantee list. For more current information, contact their program officer directly.]

---

## Output Expectations

You will receive:

1. **Funder profile summary** (how they fund, what they prioritize, what they require)
2. **Alignment analysis by priority area** with strength ratings and strategic emphasis guidance
3. **Structural fit assessment** (funding range, timeline, requirements)
4. **Overall alignment rating** (Strong/Moderate/Weak) with rationale
5. **Strategic recommendation** tailored to your alignment level
6. **Next steps** if you decide to pursue this funder
7. **Standard disclaimer** (see grant-writer skill)

## How to Interpret Ratings

**STRONG ALIGNMENT**
- Your program directly addresses funder's stated priorities
- Your target population matches theirs
- Your service area aligns with their geographic focus
- Your funding ask is within their typical range
- You have demonstrated track record in this area
- **Action:** Apply with confidence; emphasize aligned areas

**MODERATE ALIGNMENT**
- Your program partially addresses funder's priorities
- Some strong alignment, some gaps
- Funding ask may be slightly outside typical range but potentially fundable
- Track record exists but may need strengthening in certain areas
- **Action:** Apply strategically; lead with strongest alignment; address gaps authentically

**WEAK ALIGNMENT**
- Your program does not directly address funder's stated priorities
- Limited connection between your work and their funding focus
- Significant gaps in organizational type, geographic focus, or grantee requirements
- **Action:** Consider applying only if: (1) limited alternatives, (2) you can make a compelling case for connection, (3) you have other programs with better alignment

## Tips for Success

- **Use publicly available data:** 990-PF forms, grantee lists, website priorities
- **Look for patterns in grantee list:** Which organizations do they fund repeatedly? Which sectors? What grant sizes?
- **Contact program officers:** If moderate or weak alignment, call the program officer and ask directly: "Does this funder consider applications from [your org type] doing [your work]?"
- **Be honest about fit:** Strong alignment = better funding likelihood. Weak alignment = long odds regardless of proposal quality
- **Look for secondary opportunities:** If weak alignment with primary program, consider whether you have other programs that align better
- **Leverage strong alignment:** If strong alignment, emphasize it relentlessly in your narrative
- **Address gaps directly:** Don't ignore misalignments; address them head-on with honest explanation of why you're applying despite gaps
