---
name: data-quality-validation
description: Comprehensive data quality and validation toolkit with 5 systematic approaches for ensuring data reliability, correctness, and fitness for analysis. Use for exploratory data analysis, quality audits, SQL validation, schema mapping, and metric reconciliation.
allowed-tools: Read Write Edit Bash
license: MIT license
metadata:
  version: "1.0"
  skill-author: Wisu Suntoyo
  adapted-from: data-analytics-skills by Nimrod Fisher
  category: "01-data-quality-validation"
---

# Data Quality & Validation

## Overview

This skill provides 5 systematic approaches to ensure data reliability and correctness before analysis:

1. **Programmatic EDA** - Systematic exploratory data analysis with automated sanity checks
2. **Data Quality Audit** - Comprehensive quality assessment against business rules and schema
3. **Query Validation** - SQL review for correctness, performance, and edge cases
4. **Schema Mapper** - Understand database relationships and table structures
5. **Metric Reconciliation** - Investigate discrepancies between metric sources

**Core Philosophy**: Validate data quality early and systematically to prevent downstream analysis errors.

---

## When to Use This Skill

Use this skill when:
- **Exploring new datasets**: Need to understand structure, quality, and patterns
- **Validating data pipelines**: Ensure pipeline outputs meet quality standards
- **Reviewing SQL queries**: Check for correctness, performance issues, and edge cases
- **Understanding schemas**: Map database relationships and dependencies
- **Investigating metric discrepancies**: Reconcile differences between data sources
- **Quality assurance**: Produce formal quality scorecards for data assets

---

## Activity 1: Programmatic EDA

**Purpose**: Systematic exploratory data analysis with automated sanity checks.

### When to use
- You receive a new dataset and need to understand its shape and quality before analysis
- An analysis produces surprising numbers and you want to verify the underlying data first
- A stakeholder asks "is this data reliable?" or "what's in this table?"
- You're about to run a model or statistical test and need data-quality assurance

### Process
1. **Load and overview** - Get row count, dtypes, memory usage, and sample. Confirm grain (what one row represents).
2. **Null profile** - Analyze null patterns; compare against quality thresholds and flag columns above limits.
3. **Outlier detection** - Use IQR + z-score on numeric columns; document flagged values and decide: real signal or data error?
4. **Distribution summary** - Generate descriptive stats and univariate histograms for each numeric column.
5. **Correlation exploration** - Calculate correlations; flag pairs with |r| > 0.8 as potential multicollinearity or redundancy.
6. **EDA checklist sign-off** - Confirm each quality checkpoint before declaring the dataset profiled.
7. **Write findings** - Document full profiling output; distill top issues into summary.

### Inputs needed
- **Required**: Dataset path (CSV/Parquet/Excel) or DataFrame
- **Required**: Business context - what does one row represent?
- **Optional**: Quality threshold overrides
- **Optional**: Columns to skip (PII, binary blobs, high-cardinality IDs)

### Output
- Full profiling report with per-column statistics
- Summary of top 3-5 quality issues and recommended next steps
- Console output/plots for interactive inspection

---

## Activity 2: Data Quality Audit

**Purpose**: Comprehensive quality assessment against business rules, schema constraints, and freshness expectations.

### When to use
- A data pipeline has just loaded new data and needs validation before downstream reports consume it
- A stakeholder has flagged data quality concerns (wrong totals, unexpected nulls, stale data)
- You need to produce a formal data quality scorecard for a data asset
- You are onboarding a new data source and need to understand its quality profile

### Process
1. **Null and completeness audit** - Generate column-by-column null profile. Flag columns above acceptable thresholds.
2. **Duplicate detection** - Identify full-row and key-level duplicates. Determine if duplicates are intentional or errors.
3. **Referential integrity check** - Validate that foreign key values in child tables exist in parent tables. Report orphan rate.
4. **Value range validation** - Check values against business rules. Flag values outside acceptable ranges.
5. **Freshness check** - Verify dataset is up to date - compare latest record timestamp against expected lag.
6. **Score and classify findings** - Map each finding to quality dimension. Assign severity (CRITICAL/HIGH/MEDIUM/LOW).
7. **Produce deliverables** - Create shareable audit report and concise quality scorecard.

### Inputs needed
- **Required**: Dataset (CSV/Parquet/database table reference)
- **Required**: Schema relationships - primary keys, foreign keys
- **Required**: Business rules - acceptable value ranges, expected value sets, freshness SLA
- **Optional**: Acceptable error rates - thresholds for CRITICAL vs. HIGH
- **Optional**: Pipeline schedule - to assess freshness relative to expected update frequency

### Output
- Full quality audit report, shareable with stakeholders
- One-page quality scorecard with dimension scores
- Per-check pass/fail counts for each validation

---

## Activity 3: Query Validation

**Purpose**: SQL review for correctness, performance, and edge cases.

### When to use
- You've written a complex SQL query and want to catch logic errors before running it on production
- A query is running slowly and you need to identify performance bottlenecks
- You're reviewing a colleague's SQL and need a structured checklist
- A query produced unexpected results and you need to debug the logic

### Process
1. **Parse and understand intent** - Read the query; identify what business question it's answering.
2. **Logic validation** - Check JOIN conditions, WHERE filters, GROUP BY logic, and aggregation correctness.
3. **Edge case review** - Test for NULL handling, division by zero, empty result sets, and date boundary issues.
4. **Performance analysis** - Identify missing indexes, unnecessary subqueries, Cartesian products, and inefficient patterns.
5. **Best practices check** - Verify consistent formatting, meaningful aliases, and proper use of CTEs vs subqueries.
6. **Generate test cases** - Create sample data scenarios that exercise edge cases.
7. **Document findings** - Provide annotated query with issues flagged and suggested fixes.

### Inputs needed
- **Required**: SQL query text
- **Required**: Database type (PostgreSQL, MySQL, SQL Server, etc.)
- **Required**: Business context - what question is this query answering?
- **Optional**: Schema information (table structures, indexes)
- **Optional**: Expected result set characteristics
- **Optional**: Performance requirements (query should complete in X seconds)

### Output
- Annotated query with issues highlighted
- List of logic errors, edge cases, and performance concerns
- Suggested fixes with explanations
- Test cases to validate the query

---

## Activity 4: Schema Mapper

**Purpose**: Understand database relationships and table structures.

### When to use
- You're new to a database and need to understand how tables relate to each other
- You need to document the schema for a data catalog or onboarding guide
- You're planning a complex query and need to identify the join path between tables
- You're investigating a data quality issue and need to trace data lineage

### Process
1. **Catalog tables** - List all tables in the schema with row counts and descriptions.
2. **Identify relationships** - Map primary keys, foreign keys, and join patterns.
3. **Document grain** - For each table, define what one row represents.
4. **Map dependencies** - Identify which tables depend on which (parent-child relationships).
5. **Visualize structure** - Create entity-relationship diagram or text-based schema map.
6. **Document patterns** - Note common join patterns, bridge tables, and denormalized structures.
7. **Create reference** - Generate schema documentation for future use.

### Inputs needed
- **Required**: Database connection details or schema export
- **Required**: Database type
- **Optional**: Specific tables to focus on
- **Optional**: Business context for table purposes

### Output
- Schema map showing table relationships
- Documentation of primary/foreign keys
- Common join patterns
- Table grain definitions

---

## Activity 5: Metric Reconciliation

**Purpose**: Investigate discrepancies between metric sources.

### When to use
- Two reports show different numbers for the same metric
- A dashboard doesn't match the source system
- Stakeholders question why metrics changed after a data migration
- You need to validate that a new calculation matches the legacy one

### Process
1. **Define the discrepancy** - Document the two (or more) metric values and their sources.
2. **Identify calculation differences** - Compare SQL queries, formulas, or business logic between sources.
3. **Check data sources** - Verify both calculations use the same underlying tables and time ranges.
4. **Analyze filters and joins** - Look for differences in WHERE clauses, JOIN conditions, or aggregation levels.
5. **Test with sample data** - Run both calculations on a small, controlled dataset to isolate the difference.
6. **Document root cause** - Explain why the metrics differ (different filters, different grain, different time zones, etc.).
7. **Recommend resolution** - Propose which calculation is correct and how to align the other source.

### Inputs needed
- **Required**: The two (or more) metric values that don't match
- **Required**: Source of each metric (query, report, dashboard, etc.)
- **Required**: Business definition of the metric
- **Optional**: Access to underlying data sources
- **Optional**: Historical context (when did the discrepancy start?)

### Output
- Root cause analysis of the discrepancy
- Side-by-side comparison of calculation logic
- Recommendation for which source is correct
- Action plan to align metrics

---

## Common Workflows

### New Dataset Investigation
```
1. Programmatic EDA → understand structure and quality
2. Schema Mapper → understand relationships (if database)
3. Data Quality Audit → formal quality assessment
4. Proceed with analysis using appropriate skills
```

### SQL Development
```
1. Schema Mapper → understand available tables
2. Write query
3. Query Validation → review before running
4. Execute and validate results
```

### Metric Discrepancy Investigation
```
1. Metric Reconciliation → identify root cause
2. Query Validation → review both calculations
3. Data Quality Audit → check underlying data quality
4. Document resolution
```

### Data Pipeline Validation
```
1. Data Quality Audit → comprehensive quality check
2. Metric Reconciliation → validate against source system
3. Document quality scorecard
```

---

## Key Principles

1. **Validate early** - Check data quality before investing time in analysis
2. **Be systematic** - Follow structured checklists to avoid missing issues
3. **Document findings** - Create reusable quality reports and scorecards
4. **Test edge cases** - Don't just check happy path scenarios
5. **Understand context** - Quality thresholds depend on business requirements
6. **Automate when possible** - Use scripts for repeatable validation tasks

---

## References

For detailed implementation guidance, see the original data-analytics-skills repository:
- Category: `01-data-quality-validation/`
- Skills: `programmatic-eda/`, `data-quality-audit/`, `query-validation/`, `schema-mapper/`, `metric-reconciliation/`

Each skill includes:
- Detailed SKILL.md with process steps
- Python scripts for automation (where applicable)
- Reference documentation for frameworks and patterns
- Output templates for reports and scorecards

---

## Integration with Other Skills

**Pairs well with:**
- **Documentation & Knowledge** - Document quality findings and metric definitions
- **Data Analysis & Investigation** - Use validated data for analysis
- **Stakeholder Communication** - Present quality scorecards to stakeholders

**Quality gates:**
- Run Programmatic EDA before any analysis
- Run Data Quality Audit before production deployment
- Run Query Validation before executing complex queries