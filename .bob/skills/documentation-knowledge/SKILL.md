---
name: documentation-knowledge
description: Build reusable context and institutional knowledge with 5 systematic approaches for documenting metrics, analyses, data catalogs, SQL logic, and assumptions. Use to create semantic layers, analysis documentation, catalog entries, business logic translations, and assumption logs.
allowed-tools: Read Write Edit Bash
license: MIT license
metadata:
  version: "1.0"
  skill-author: Wisu Suntoyo
  adapted-from: data-analytics-skills by Nimrod Fisher
  category: "02-documentation-knowledge"
---

# Documentation & Knowledge

## Overview

This skill provides 5 systematic approaches to build reusable context so you never explain the same thing twice:

1. **Semantic Model Builder** - Create shared semantic layer for key metrics and dimensions
2. **Analysis Documentation** - Document findings with reproducible methodology
3. **Data Catalog Entry** - Standardized metadata and descriptions for data assets
4. **SQL to Business Logic** - Translate complex SQL into plain business language
5. **Analysis Assumptions Log** - Track every assumption and decision in an analysis

**Core Philosophy**: Document once, reuse forever. Build institutional knowledge that survives team changes.

---

## When to Use This Skill

Use this skill when:
- **Defining metrics**: Create canonical definitions that everyone uses
- **Documenting analyses**: Make your work reproducible and understandable
- **Building data catalogs**: Provide clear metadata for data assets
- **Explaining SQL**: Translate technical queries into business language
- **Tracking assumptions**: Document decisions and assumptions for transparency
- **Onboarding teams**: Create reference documentation for new team members

---

## Activity 1: Semantic Model Builder

**Purpose**: Build structured semantic layer documentation for metrics, dimensions, and entities.

### When to use
- A stakeholder asks "how is [metric] calculated?" and no canonical definition exists
- You're setting up dbt Semantic Layer and need YAML metric/dimension/entity definitions
- Multiple teams are using different SQL queries for the same metric - you need to codify the one true definition
- You're building a data catalog entry for a core model and need structured metadata

### Process
1. **Identify the object type** - Decide whether you're documenting a metric, dimension, or entity.
2. **Gather definition inputs** - Collect: calculation logic (SQL or formula), business context, data source(s), grain, edge cases, and known gotchas.
3. **Generate the YAML template** - Scaffold the initial YAML structure for the object type.
4. **Validate the YAML** - Check required fields, type constraints, and reference integrity.
5. **Add framework context** - If deploying to dbt Semantic Layer or similar, add framework-specific fields.
6. **Save final definitions** - Save metrics, dimensions, and entities to structured files.

### Inputs needed
- **Required**: Metric name or model name to document
- **Required**: Calculation logic - SQL snippet, formula, or plain-English steps
- **Required**: Business context - who uses it, what decision it informs, what a "good" value looks like
- **Optional**: Data source table(s) and column names
- **Optional**: Target semantic layer framework (dbt Semantic Layer, Cube.js, LookML, etc.)
- **Optional**: Existing YAML to validate

### Output
- Metric YAML definition(s)
- Dimension YAML definition(s)
- Entity YAML definition(s)
- Validation report

---

## Activity 2: Analysis Documentation

**Purpose**: Document findings with reproducible methodology.

### When to use
- You've completed an analysis and need to document it for future reference
- A stakeholder asks "how did you calculate this?" weeks after you delivered results
- You need to hand off an analysis to another analyst
- You want to create a template for similar future analyses

### Process
1. **Document the question** - State the business question or problem being solved.
2. **Describe the approach** - Explain the methodology, data sources, and analytical techniques used.
3. **List assumptions** - Document all assumptions made during the analysis.
4. **Show the results** - Present findings with visualizations and key metrics.
5. **Explain limitations** - Note data quality issues, sample size concerns, or other caveats.
6. **Provide recommendations** - Suggest actions based on the findings.
7. **Include reproducibility info** - Add SQL queries, code snippets, or step-by-step instructions.

### Inputs needed
- **Required**: The business question or problem
- **Required**: Analysis results and findings
- **Required**: Methodology and data sources used
- **Optional**: Code/SQL used in the analysis
- **Optional**: Visualizations or charts
- **Optional**: Stakeholder feedback or questions

### Output
- Complete analysis documentation
- Reproducible methodology
- Code/SQL snippets
- Recommendations and next steps

---

## Activity 3: Data Catalog Entry

**Purpose**: Standardized metadata and descriptions for data assets.

### When to use
- You're building a data catalog and need consistent documentation format
- A new team member asks "what's in this table?"
- You need to document a data asset for compliance or governance
- You want to make a dataset discoverable and understandable

### Process
1. **Identify the asset** - Determine what you're documenting (table, view, dataset, report).
2. **Gather basic metadata** - Collect: name, description, owner, update frequency, row count.
3. **Document schema** - List columns with data types, descriptions, and sample values.
4. **Describe grain** - Define what one row represents.
5. **List dependencies** - Note upstream sources and downstream consumers.
6. **Add usage guidance** - Explain common use cases and known limitations.
7. **Include quality info** - Document data quality metrics and known issues.

### Inputs needed
- **Required**: Asset name and type (table, view, dataset, etc.)
- **Required**: Schema information (columns, data types)
- **Required**: Business purpose and use cases
- **Optional**: Data owner and contact information
- **Optional**: Update frequency and freshness SLA
- **Optional**: Known data quality issues

### Output
- Standardized catalog entry
- Schema documentation
- Usage guidance
- Quality metrics

---

## Activity 4: SQL to Business Logic

**Purpose**: Translate complex SQL into plain business language.

### When to use
- A stakeholder asks "what does this query do?" and needs a non-technical explanation
- You need to document a complex query for future reference
- You're reviewing someone else's SQL and need to understand the business logic
- You want to validate that SQL matches the intended business logic

### Process
1. **Parse the query** - Break down the SQL into logical components (CTEs, joins, filters, aggregations).
2. **Identify business entities** - Map table names to business concepts (customers, orders, products).
3. **Translate filters** - Convert WHERE clauses into business rules ("active customers in the last 90 days").
4. **Explain joins** - Describe relationships ("match each order to its customer").
5. **Interpret aggregations** - Translate GROUP BY and aggregations into business metrics.
6. **Describe the output** - Explain what the final result set represents.
7. **Document edge cases** - Note how the query handles NULLs, duplicates, or special conditions.

### Inputs needed
- **Required**: SQL query text
- **Required**: Database schema context
- **Optional**: Business context for the query's purpose
- **Optional**: Sample output to validate understanding

### Output
- Plain-language explanation of the query
- Business logic description
- Edge case documentation
- Validation that SQL matches intent

---

## Activity 5: Analysis Assumptions Log

**Purpose**: Track every assumption and decision in an analysis.

### When to use
- You're starting a complex analysis and want to document decisions as you go
- A stakeholder questions your results and you need to explain your assumptions
- You want to create transparency about what you assumed vs. what you validated
- You're handing off an analysis and need to document decision rationale

### Process
1. **List data assumptions** - Document assumptions about data quality, completeness, and accuracy.
2. **Document business assumptions** - Note assumptions about business rules, definitions, and context.
3. **Record methodological choices** - Explain why you chose specific analytical techniques.
4. **Note exclusions** - Document what data or scenarios you excluded and why.
5. **Track validation status** - Mark which assumptions were validated vs. unvalidated.
6. **Document impact** - Assess how each assumption affects the results.
7. **Create action items** - List assumptions that should be validated in future work.

### Inputs needed
- **Required**: The analysis being documented
- **Required**: Key decisions made during the analysis
- **Optional**: Stakeholder requirements or constraints
- **Optional**: Known data quality issues

### Output
- Comprehensive assumptions log
- Validation status for each assumption
- Impact assessment
- Action items for future validation

---

## Common Workflows

### Metric Definition
```
1. Semantic Model Builder → create canonical definition
2. Analysis Documentation → document how to use the metric
3. Share with team for alignment
```

### Analysis Delivery
```
1. Analysis Assumptions Log → track decisions during analysis
2. Analysis Documentation → document complete methodology
3. SQL to Business Logic → explain queries to stakeholders
4. Deliver with full documentation
```

### Data Asset Onboarding
```
1. Data Catalog Entry → document the asset
2. Semantic Model Builder → define key metrics from the asset
3. SQL to Business Logic → document common queries
4. Share with team
```

### Knowledge Transfer
```
1. Semantic Model Builder → document all key metrics
2. Data Catalog Entry → document all data assets
3. Analysis Documentation → document past analyses
4. Create onboarding guide
```

---

## Key Principles

1. **Document once, reuse forever** - Invest time in good documentation to save time later
2. **Make it searchable** - Use consistent formats and naming conventions
3. **Keep it current** - Update documentation when definitions or logic change
4. **Be explicit** - Don't assume knowledge; document everything
5. **Show your work** - Include SQL, formulas, and step-by-step logic
6. **Track assumptions** - Be transparent about what you assumed vs. validated

---

## References

For detailed implementation guidance, see the original data-analytics-skills repository:
- Category: `02-documentation-knowledge/`
- Skills: `semantic-model-builder/`, `analysis-documentation/`, `data-catalog-entry/`, `sql-to-business-logic/`, `analysis-assumptions-log/`

Each skill includes:
- Detailed SKILL.md with process steps
- Python scripts for automation (where applicable)
- Reference documentation for frameworks and patterns
- Output templates (Markdown, YAML, HTML)

---

## Integration with Other Skills

**Pairs well with:**
- **Data Quality & Validation** - Document quality findings and thresholds
- **Data Analysis & Investigation** - Document analysis methodology and results
- **Stakeholder Communication** - Use documentation to explain work to stakeholders

**Best practices:**
- Create Semantic Model Builder definitions before starting analysis
- Use Analysis Assumptions Log during complex analyses
- Create Data Catalog Entries for all key data assets
- Use SQL to Business Logic when sharing queries with non-technical stakeholders