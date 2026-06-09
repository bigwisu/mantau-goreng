---
name: stakeholder-communication
description: Bridge technical analysis and business audiences with 5 systematic approaches for translating technical findings, gathering requirements, quality assurance, methodology explanation, and impact quantification. Use to communicate effectively with stakeholders.
allowed-tools: Read Write Edit Bash
license: MIT license
metadata:
  version: "1.0"
  skill-author: Wisu Suntoyo
  adapted-from: data-analytics-skills by Nimrod Fisher
  category: "05-stakeholder-communication"
---

# Stakeholder Communication

## Overview

This skill provides 5 systematic approaches to bridge the gap between technical depth and business understanding:

1. **Technical to Business Translator** - Reframe technical findings for a business audience
2. **Stakeholder Requirements Gathering** - Structured elicitation to clarify what stakeholders actually need
3. **Analysis QA Checklist** - Pre-delivery quality gate before sharing results
4. **Methodology Explainer** - Explain analysis approach to any audience level
5. **Impact Quantification** - Estimate and frame the business impact of findings

**Core Philosophy**: Great analysis is worthless if stakeholders don't understand or trust it.

---

## When to Use This Skill

Use this skill when:
- **Translating technical work**: Make technical findings accessible to business audiences
- **Gathering requirements**: Understand what stakeholders really need
- **Quality assurance**: Check analysis before delivery
- **Explaining methods**: Build trust by explaining your approach
- **Quantifying impact**: Show business value of findings
- **Building alignment**: Ensure stakeholders understand and support recommendations

---

## Activity 1: Technical to Business Translator

**Purpose**: Reframe technical findings for a business audience.

### When to use
- You need to present technical analysis to non-technical stakeholders
- A business leader asks "can you explain this in plain English?"
- You want to make findings accessible without losing accuracy
- You're writing a report for a mixed technical/business audience

### Process
1. **Identify technical elements** - List all technical terms, methods, and concepts in your analysis.
2. **Map to business concepts** - Translate each technical element into business language.
3. **Replace jargon** - Substitute technical terms with plain language equivalents.
4. **Add business context** - Explain why technical details matter for business decisions.
5. **Use analogies** - Create relatable comparisons for complex concepts.
6. **Test understanding** - Verify that non-technical readers can follow the explanation.
7. **Preserve accuracy** - Ensure simplification doesn't introduce errors or misleading statements.

### Inputs needed
- **Required**: Technical analysis or findings to translate
- **Required**: Target audience description
- **Optional**: Specific technical terms that need translation
- **Optional**: Business context or goals

### Output
- Business-friendly version of technical content
- Glossary of translated terms
- Analogies for complex concepts
- Preserved technical accuracy

---

## Activity 2: Stakeholder Requirements Gathering

**Purpose**: Structured elicitation to clarify what stakeholders actually need.

### When to use
- A stakeholder makes a vague request ("can you analyze our customer data?")
- You want to avoid building the wrong analysis
- You need to clarify scope and priorities before starting work
- Multiple stakeholders have conflicting requirements

### Process
1. **Understand the business problem** - Ask: What decision are you trying to make? What's not working?
2. **Clarify success criteria** - Ask: How will you know if this analysis is successful?
3. **Identify constraints** - Ask: What's the timeline? What data is available? What's the budget?
4. **Explore use cases** - Ask: How will you use these insights? Who else needs to see this?
5. **Prioritize requirements** - Separate must-haves from nice-to-haves.
6. **Document assumptions** - Confirm what you're assuming about the problem and data.
7. **Get sign-off** - Ensure stakeholders agree on scope before you start.

### Inputs needed
- **Required**: Initial stakeholder request or problem statement
- **Optional**: Previous analysis or context
- **Optional**: Known constraints (time, data, resources)

### Output
- Clarified requirements document
- Success criteria
- Prioritized scope
- Documented assumptions
- Stakeholder sign-off

---

## Activity 3: Analysis QA Checklist

**Purpose**: Pre-delivery quality gate before sharing results.

### When to use
- You've completed an analysis and want to check quality before delivery
- You want to avoid embarrassing errors or misinterpretations
- You're reviewing a colleague's analysis
- You need a structured checklist for consistent quality

### Process
1. **Verify data quality** - Check for data issues, outliers, or anomalies that might affect results.
2. **Validate calculations** - Confirm formulas, aggregations, and statistical tests are correct.
3. **Check assumptions** - Review all assumptions and verify they're documented and reasonable.
4. **Test edge cases** - Ensure analysis handles nulls, zeros, and boundary conditions correctly.
5. **Review visualizations** - Check that charts are accurate, clear, and not misleading.
6. **Validate business logic** - Confirm analysis aligns with business definitions and rules.
7. **Proofread deliverables** - Check for typos, formatting issues, and clarity.

### Inputs needed
- **Required**: Completed analysis to review
- **Optional**: Business rules or requirements to validate against
- **Optional**: Previous similar analyses for comparison

### Output
- QA checklist with pass/fail for each item
- List of issues found
- Recommendations for fixes
- Approval to deliver (or not)

---

## Activity 4: Methodology Explainer

**Purpose**: Explain analysis approach to any audience level.

### When to use
- Stakeholders ask "how did you calculate this?"
- You need to build trust in your analysis
- You want to make your work reproducible
- You're training others on analytical methods

### Process
1. **Identify the audience** - Determine their technical level and what they need to know.
2. **Explain the question** - Start with the business question you're answering.
3. **Describe the approach** - Outline your analytical method at appropriate detail level.
4. **Justify choices** - Explain why you chose this method over alternatives.
5. **Acknowledge limitations** - Be transparent about what your method can and can't do.
6. **Provide examples** - Use simple examples to illustrate the method.
7. **Offer resources** - Point to documentation or references for those who want to learn more.

### Inputs needed
- **Required**: Analysis methodology to explain
- **Required**: Target audience description
- **Optional**: Alternative methods considered
- **Optional**: Known limitations or caveats

### Output
- Methodology explanation tailored to audience
- Justification for approach
- Limitations and caveats
- Examples and references

---

## Activity 5: Impact Quantification

**Purpose**: Estimate and frame the business impact of findings.

### When to use
- Stakeholders ask "so what?" or "why does this matter?"
- You need to prioritize recommendations by business value
- You want to justify investment in implementing recommendations
- You're building a business case for action

### Process
1. **Identify the metric** - Choose the business metric affected (revenue, cost, time, satisfaction, etc.).
2. **Estimate the magnitude** - Calculate or estimate the size of the impact.
3. **Add time dimension** - Specify if impact is one-time, annual, or ongoing.
4. **Calculate confidence** - Assess certainty level (high/medium/low confidence).
5. **Compare to benchmarks** - Put impact in context (% of revenue, industry standards, etc.).
6. **Account for costs** - Consider implementation costs and effort required.
7. **Frame the impact** - Present in terms that resonate with stakeholders (ROI, payback period, etc.).

### Inputs needed
- **Required**: Finding or recommendation to quantify
- **Required**: Relevant business metrics
- **Optional**: Historical data for estimation
- **Optional**: Implementation cost estimates

### Output
- Quantified business impact
- Confidence level
- Comparison to benchmarks
- ROI or cost-benefit analysis
- Framing for stakeholder presentation

---

## Common Workflows

### Analysis Delivery
```
1. Analysis QA Checklist → verify quality
2. Technical to Business Translator → make findings accessible
3. Impact Quantification → show business value
4. Deliver to stakeholders
```

### New Analysis Request
```
1. Stakeholder Requirements Gathering → clarify needs
2. Methodology Explainer → explain proposed approach
3. Get approval to proceed
4. Execute analysis
```

### Building Trust
```
1. Methodology Explainer → explain your approach
2. Analysis QA Checklist → demonstrate rigor
3. Technical to Business Translator → make it accessible
4. Impact Quantification → show business value
```

### Prioritizing Work
```
1. Stakeholder Requirements Gathering → understand all requests
2. Impact Quantification → estimate value of each
3. Prioritize by impact and effort
4. Communicate priorities to stakeholders
```

---

## Key Principles

1. **Know your audience** - Tailor communication to their technical level and interests
2. **Be transparent** - Explain methods, assumptions, and limitations clearly
3. **Show business value** - Always connect findings to business impact
4. **Build trust** - Demonstrate rigor through quality checks and clear explanations
5. **Clarify upfront** - Gather requirements before starting work
6. **Make it actionable** - Ensure stakeholders know what to do with your findings

---

## Communication Best Practices

### For Technical Audiences
- Include methodology details
- Show statistical rigor
- Provide code or SQL
- Discuss alternative approaches
- Be precise with terminology

### For Business Audiences
- Start with business impact
- Use plain language
- Focus on actionable insights
- Use analogies and examples
- Minimize technical jargon

### For Mixed Audiences
- Layer information (executive summary + technical appendix)
- Define technical terms when first used
- Use visualizations to bridge technical and business
- Provide both "what" and "how"
- Offer to dive deeper on technical details

---

## Common Pitfalls to Avoid

1. **Assuming knowledge** - Don't assume stakeholders understand technical concepts
2. **Oversimplifying** - Don't lose accuracy in pursuit of simplicity
3. **Skipping validation** - Don't deliver without quality checks
4. **Ignoring constraints** - Don't propose solutions that ignore business realities
5. **Burying the lead** - Don't make stakeholders hunt for key findings
6. **Missing the "so what"** - Don't present findings without business implications

---

## References

For detailed implementation guidance, see the original data-analytics-skills repository:
- Category: `05-stakeholder-communication/`
- Skills: `technical-to-business-translator/`, `stakeholder-requirements-gathering/`, `analysis-qa-checklist/`, `methodology-explainer/`, `impact-quantification/`

Each skill includes:
- Detailed SKILL.md with process steps
- Reference documentation for communication frameworks
- Output templates (checklists, requirement docs)
- Examples of effective communication

---

## Integration with Other Skills

**Pairs well with:**
- **Data Storytelling & Visualization** - Communicate findings visually
- **Documentation & Knowledge** - Document for future reference
- **Data Analysis & Investigation** - Explain analytical methods

**Best practices:**
- Use Stakeholder Requirements Gathering before starting analysis
- Run Analysis QA Checklist before delivery
- Use Technical to Business Translator for all stakeholder communications
- Apply Impact Quantification to prioritize recommendations