---
name: workflow-optimization
description: Streamline and improve analytical processes with 4 systematic approaches for analysis planning, context packaging, peer review, and retrospectives. Use to work smarter across every project and continuously improve analytical workflows.
allowed-tools: Read Write Edit Bash
license: MIT license
metadata:
  version: "1.0"
  skill-author: Wisu Suntoyo
  adapted-from: data-analytics-skills by Nimrod Fisher
  category: "06-workflow-optimization"
---

# Workflow Optimization

## Overview

This skill provides 4 systematic approaches to work smarter across every project:

1. **Analysis Planning** - Structure the approach before diving in
2. **Context Packager** - Package context efficiently for AI-assisted analysis
3. **Peer Review Template** - Structured peer review checklist for analytical work
4. **Analysis Retrospective** - Post-analysis learning and process improvement

**Core Philosophy**: Invest time in planning and reflection to work faster and better over time.

---

## When to Use This Skill

Use this skill when:
- **Starting new analysis**: Plan approach before diving into data
- **Working with AI assistants**: Package context efficiently
- **Reviewing work**: Conduct structured peer reviews
- **Learning from experience**: Reflect on what worked and what didn't
- **Improving processes**: Identify and fix workflow bottlenecks
- **Building team capabilities**: Share learnings across the team

---

## Activity 1: Analysis Planning

**Purpose**: Structure the approach before diving in.

### When to use
- You're starting a new analysis and want to avoid false starts
- A stakeholder makes a complex request and you need to break it down
- You want to estimate effort and timeline before committing
- You need to identify data and resource requirements upfront

### Process
1. **Clarify the question** - Restate the business question in clear, specific terms.
2. **Define success criteria** - Determine what a successful answer looks like.
3. **Identify data needs** - List all data sources, tables, and metrics required.
4. **Choose analytical approach** - Select appropriate methods and techniques.
5. **Break down tasks** - Decompose the analysis into discrete steps.
6. **Estimate effort** - Assess time required for each step.
7. **Identify risks** - Note potential blockers (data quality, access, complexity).

### Inputs needed
- **Required**: Business question or problem statement
- **Required**: Available data sources
- **Optional**: Timeline or deadline
- **Optional**: Resource constraints

### Output
- Analysis plan with clear steps
- Data requirements
- Effort estimate
- Risk assessment
- Success criteria

---

## Activity 2: Context Packager

**Purpose**: Package context efficiently for AI-assisted analysis.

### When to use
- You're working with an AI assistant and want to provide efficient context
- You need to onboard someone quickly to a project
- You want to create reusable context for similar future analyses
- You're documenting a project for handoff

### Process
1. **Identify essential context** - Determine what information is truly necessary.
2. **Structure the context** - Organize into logical sections (business context, data schema, metrics, etc.).
3. **Create schema documentation** - Document table structures, relationships, and key columns.
4. **Define metrics** - Provide canonical definitions for key metrics.
5. **Document business rules** - Capture important business logic and edge cases.
6. **Add examples** - Include sample queries or previous analyses.
7. **Package for reuse** - Save in a format that's easy to reference in future conversations.

### Inputs needed
- **Required**: Project or analysis context to package
- **Optional**: Database schema
- **Optional**: Metric definitions
- **Optional**: Business rules

### Output
- Structured context document
- Schema documentation
- Metric definitions
- Business rules
- Example queries or analyses

---

## Activity 3: Peer Review Template

**Purpose**: Structured peer review checklist for analytical work.

### When to use
- You want feedback on your analysis before delivery
- You're reviewing a colleague's work
- You want to ensure consistent quality across the team
- You're training junior analysts on quality standards

### Process
1. **Review the question** - Verify the analysis addresses the right business question.
2. **Check data quality** - Assess if data sources are appropriate and reliable.
3. **Validate methodology** - Confirm analytical approach is sound and appropriate.
4. **Verify calculations** - Check formulas, aggregations, and statistical tests.
5. **Assess assumptions** - Review documented assumptions for reasonableness.
6. **Evaluate insights** - Determine if conclusions are supported by data.
7. **Check deliverables** - Review clarity, accuracy, and completeness of outputs.

### Inputs needed
- **Required**: Analysis to review
- **Optional**: Original requirements or business question
- **Optional**: Quality standards or guidelines

### Output
- Peer review checklist with ratings
- Specific feedback and suggestions
- Approval status (approved, needs revision, rejected)
- Action items for improvement

---

## Activity 4: Analysis Retrospective

**Purpose**: Post-analysis learning and process improvement.

### When to use
- You've completed a significant analysis and want to capture learnings
- You want to identify process improvements for future work
- You're building team knowledge about what works and what doesn't
- You need to document lessons learned for similar future projects

### Process
1. **Review the outcome** - Assess if the analysis achieved its goals.
2. **Identify what worked well** - Document successful approaches and techniques.
3. **Identify what didn't work** - Note challenges, blockers, and inefficiencies.
4. **Analyze root causes** - Understand why things went well or poorly.
5. **Generate improvements** - Propose specific changes to process or approach.
6. **Document learnings** - Capture insights for future reference.
7. **Create action items** - Define concrete steps to implement improvements.

### Inputs needed
- **Required**: Completed analysis to reflect on
- **Optional**: Original plan or timeline for comparison
- **Optional**: Stakeholder feedback

### Output
- Retrospective document
- What worked well
- What didn't work
- Root cause analysis
- Improvement recommendations
- Action items

---

## Common Workflows

### Starting New Analysis
```
1. Analysis Planning → structure approach
2. Context Packager → document context
3. Execute analysis
4. Peer Review Template → get feedback
5. Analysis Retrospective → capture learnings
```

### Team Knowledge Building
```
1. Analysis Retrospective → after each project
2. Context Packager → document reusable context
3. Share learnings with team
4. Update standards and templates
```

### Quality Assurance
```
1. Analysis Planning → plan before starting
2. Execute analysis
3. Peer Review Template → structured review
4. Revise based on feedback
5. Deliver
```

### Continuous Improvement
```
1. Analysis Retrospective → identify improvements
2. Update Analysis Planning templates
3. Refine Peer Review Template
4. Share with team
5. Implement in next project
```

---

## Key Principles

1. **Plan before executing** - Time spent planning saves time in execution
2. **Document for reuse** - Capture context and learnings for future projects
3. **Review systematically** - Use structured checklists for consistent quality
4. **Reflect regularly** - Learn from every project to improve over time
5. **Share knowledge** - Build team capabilities through documentation
6. **Iterate on process** - Continuously refine workflows based on experience

---

## Planning Best Practices

### Good Analysis Plans Include
- Clear business question
- Specific success criteria
- Detailed data requirements
- Step-by-step approach
- Effort estimates
- Risk assessment
- Stakeholder alignment

### Common Planning Mistakes
- Starting analysis before clarifying the question
- Underestimating data quality issues
- Not identifying data access requirements early
- Skipping effort estimation
- Not documenting assumptions upfront
- Failing to align with stakeholders on scope

---

## Context Packaging Best Practices

### Essential Context Elements
- Business problem and goals
- Data schema (tables, columns, relationships)
- Metric definitions and calculations
- Business rules and edge cases
- Known data quality issues
- Example queries or analyses

### Context Organization
- Use consistent structure across projects
- Keep it concise but complete
- Update as you learn more
- Make it searchable
- Version control for changes

---

## Peer Review Best Practices

### Effective Reviews
- Use structured checklists
- Be specific in feedback
- Focus on high-impact issues first
- Suggest improvements, not just problems
- Check both technical and business aspects
- Document review findings

### Review Focus Areas
- Business question alignment
- Data quality and appropriateness
- Methodology soundness
- Calculation accuracy
- Assumption reasonableness
- Insight validity
- Deliverable clarity

---

## Retrospective Best Practices

### Effective Retrospectives
- Conduct soon after project completion
- Include all team members involved
- Focus on process, not people
- Be specific about what to improve
- Create actionable next steps
- Document and share learnings

### Key Questions
- Did we answer the right question?
- What took longer than expected? Why?
- What data issues did we encounter?
- What would we do differently next time?
- What should we standardize or automate?
- What knowledge should we capture?

---

## References

For detailed implementation guidance, see the original data-analytics-skills repository:
- Category: `06-workflow-optimization/`
- Skills: `analysis-planning/`, `context-packager/`, `peer-review-template/`, `analysis-retrospective/`

Each skill includes:
- Detailed SKILL.md with process steps
- Reference documentation for frameworks
- Output templates (plans, checklists, retrospectives)
- Examples of effective workflows

---

## Integration with Other Skills

**Pairs well with:**
- **All other skills** - Workflow optimization improves every analytical activity
- **Documentation & Knowledge** - Document learnings for reuse
- **Stakeholder Communication** - Plan communication strategy upfront

**Best practices:**
- Use Analysis Planning before starting any significant analysis
- Create Context Packager documents for complex projects
- Run Peer Review Template before delivering results
- Conduct Analysis Retrospective after major projects
- Share learnings across the team

---

## Measuring Workflow Improvement

### Key Metrics
- Time from request to delivery
- Number of revision cycles
- Stakeholder satisfaction
- Analysis reuse rate
- Team knowledge sharing

### Improvement Indicators
- Faster project completion
- Fewer errors and revisions
- Better stakeholder alignment
- More reusable components
- Stronger team capabilities

---

## Building a Learning Culture

1. **Make retrospectives routine** - After every significant project
2. **Document learnings** - Capture insights in accessible format
3. **Share across team** - Regular knowledge sharing sessions
4. **Update standards** - Evolve templates and processes based on learnings
5. **Celebrate improvements** - Recognize process innovations
6. **Invest in planning** - Allocate time for upfront planning and reflection