# Bob Skills Library

This directory contains 7 reusable skills for Bob, organized by purpose. All skills are portable and can be copied to other projects.

## Available Skills

### 1. Enterprise Design Thinking
**Location**: `enterprise-design-thinking/`  
**Author**: Wisu Suntoyo  
**Source**: IBM Enterprise Design Thinking

IBM's framework for solving users' problems at enterprise speed and scale.

- **The Loop**: Observe → Reflect → Make
- **The Keys**: Hills, Playbacks, Sponsor Users
- **The Principles**: User Outcomes, Restless Reinvention, Diverse Teams
- **29 Activities**: Complete toolkit for research, planning, ideation, testing, and alignment

### 2. Data Quality & Validation
**Location**: `data-quality-validation/`  
**Author**: Wisu Suntoyo (adapted from Nimrod Fisher)  
**Category**: 01-data-quality-validation

Ensure data reliability and correctness with 5 systematic approaches:

1. **programmatic-eda** - Systematic exploratory data analysis
   - 5 Python scripts, 3 reference docs, 2 templates
2. **data-quality-audit** - Comprehensive quality assessment
   - 5 Python scripts, 2 reference docs, 2 templates
3. **query-validation** - SQL review for correctness and performance
   - 3 Python scripts, 3 reference docs, 2 templates
4. **schema-mapper** - Understand database relationships
   - 1 SKILL.md
5. **metric-reconciliation** - Investigate metric discrepancies
   - 1 SKILL.md

**Total**: 13 Python scripts, 8 reference docs, 6 templates

### 3. Documentation & Knowledge
**Location**: `documentation-knowledge/`  
**Author**: Wisu Suntoyo (adapted from Nimrod Fisher)  
**Category**: 02-documentation-knowledge

Build reusable context with 5 systematic approaches:

1. **semantic-model-builder** - Create shared semantic layer
   - 2 Python scripts, 2 reference docs, 3 YAML templates
2. **analysis-documentation** - Document findings with methodology
   - 1 reference doc, 1 template
3. **data-catalog-entry** - Standardized metadata for data assets
   - 1 Python script, 2 reference docs, 2 templates
4. **sql-to-business-logic** - Translate SQL to plain language
   - 1 Python script, 1 reference doc, 1 template
5. **analysis-assumptions-log** - Track assumptions and decisions
   - 1 Python script, 1 reference doc, 1 template

**Total**: 6 Python scripts, 7 reference docs, 8 templates

### 4. Data Analysis & Investigation
**Location**: `data-analysis-investigation/`  
**Author**: Wisu Suntoyo (adapted from Nimrod Fisher)  
**Category**: 03-data-analysis-investigation

Core analytical workflows with 7 systematic approaches:

1. **cohort-analysis** - Time-based cohort tracking
   - 2 Python scripts, 2 reference docs, 2 templates
2. **segmentation-analysis** - Customer/user segmentation
   - 2 Python scripts, 2 reference docs, 2 templates
3. **funnel-analysis** - Conversion funnel analysis
   - 2 Python scripts, 2 reference docs, 2 templates
4. **time-series-analysis** - Trend detection and forecasting
   - 2 Python scripts, 2 reference docs, 2 templates
5. **root-cause-investigation** - Diagnose metric changes
   - 2 Python scripts, 2 reference docs, 2 templates
6. **ab-test-analysis** - Rigorous experiment analysis
   - 2 Python scripts, 2 reference docs, 2 templates
7. **business-metrics-calculator** - Standard business metrics
   - 2 Python scripts, 2 reference docs, 2 templates

**Total**: 14 Python scripts, 14 reference docs, 14 templates

### 5. Data Storytelling & Visualization
**Location**: `data-storytelling-visualization/`  
**Author**: Wisu Suntoyo (adapted from Nimrod Fisher)  
**Category**: 04-data-storytelling-visualization

Transform analysis into compelling narratives with 5 approaches:

1. **insight-synthesis** - Structure outputs into insights
   - 1 reference doc, 1 template
2. **visualization-builder** - Chart type selection and design
   - 1 Python script, 2 reference docs, 2 templates
3. **executive-summary-generator** - Concise executive summaries
   - 1 reference doc, 1 template
4. **dashboard-specification** - Full dashboard requirements
   - 1 reference doc, 1 template
5. **data-narrative-builder** - Craft compelling story arcs
   - 1 reference doc, 1 template

**Total**: 1 Python script, 7 reference docs, 7 templates

### 6. Stakeholder Communication
**Location**: `stakeholder-communication/`  
**Author**: Wisu Suntoyo (adapted from Nimrod Fisher)  
**Category**: 05-stakeholder-communication

Bridge technical and business audiences with 5 approaches:

1. **technical-to-business-translator** - Reframe technical findings
   - 1 Python script, 1 reference doc, 1 template
2. **stakeholder-requirements-gathering** - Clarify needs
   - 1 reference doc, 1 template
3. **analysis-qa-checklist** - Pre-delivery quality gate
   - 1 Python script, 2 reference docs, 1 template
4. **methodology-explainer** - Explain analysis approach
   - 1 reference doc, 1 template
5. **impact-quantification** - Estimate business impact
   - 1 Python script, 2 reference docs, 1 template

**Total**: 4 Python scripts, 7 reference docs, 5 templates

### 7. Workflow Optimization
**Location**: `workflow-optimization/`  
**Author**: Wisu Suntoyo (adapted from Nimrod Fisher)  
**Category**: 06-workflow-optimization

Streamline analytical processes with 4 approaches:

1. **analysis-planning** - Structure approach before diving in
   - 1 reference doc, 1 template
2. **context-packager** - Package context efficiently
   - 1 Python script, 1 reference doc, 1 template
3. **peer-review-template** - Structured peer review
   - 1 reference doc, 1 template
4. **analysis-retrospective** - Post-analysis learning
   - 1 reference doc, 1 template

**Total**: 1 Python script, 4 reference docs, 4 templates

---

## Summary Statistics

| Category | Skills | Sub-skills | Python Scripts | Reference Docs | Templates |
|----------|--------|------------|----------------|----------------|-----------|
| Enterprise Design Thinking | 1 | 29 activities | 0 | 31 docs | 0 |
| Data Quality & Validation | 1 | 5 | 13 | 8 | 6 |
| Documentation & Knowledge | 1 | 5 | 6 | 7 | 8 |
| Data Analysis & Investigation | 1 | 7 | 14 | 14 | 14 |
| Data Storytelling & Visualization | 1 | 5 | 1 | 7 | 7 |
| Stakeholder Communication | 1 | 5 | 4 | 7 | 5 |
| Workflow Optimization | 1 | 4 | 1 | 4 | 4 |
| **TOTAL** | **7** | **60** | **39** | **78** | **44** |

---

## Skill Structure

Each skill follows this pattern:

```
skill-name/
├── SKILL.md                    # Main skill definition with YAML frontmatter
├── sub-skill-1/
│   ├── SKILL.md               # Sub-skill definition
│   ├── scripts/               # Python utilities (optional)
│   ├── references/            # Documentation and guides (optional)
│   └── assets/                # Templates and outputs (optional)
├── sub-skill-2/
│   └── ...
└── README.md                  # Skill overview (optional)
```

---

## Using Skills

### In This Project
Skills are automatically available to Bob when working in this repository.

### In Other Projects
Copy the entire `.bob/skills/` directory to your project:

```bash
cp -r /path/to/design-thinking/.bob/skills /path/to/your-project/.bob/
```

Or copy individual skills:

```bash
cp -r /path/to/design-thinking/.bob/skills/data-quality-validation /path/to/your-project/.bob/skills/
```

---

## Python Scripts

All Python scripts follow these conventions:

- **Standalone CLI tools** using `argparse`
- **Dependencies**: Only `pandas`, `numpy`, and stdlib
- **Pattern**: Core function(s) + `main()` with demo data
- **Input**: CSV/Parquet/Excel
- **Output**: Formatted stdout + optional file save

### Running Scripts

```bash
# With your data
python .bob/skills/data-quality-validation/programmatic-eda/scripts/data_overview.py --input data.csv

# With demo data (no args)
python .bob/skills/data-quality-validation/programmatic-eda/scripts/data_overview.py
```

---

## References

### Original Sources
- **IBM Enterprise Design Thinking**: https://www.ibm.com/training/enterprise-design-thinking
- **Data Analytics Skills**: https://github.com/nimrodfisher/data-analytics-skills (by Nimrod Fisher)

### Documentation
- **AGENTS.md**: Project-level guidance for AI agents
- **Individual SKILL.md files**: Detailed process steps for each skill/sub-skill
- **Reference docs**: Frameworks, patterns, and best practices
- **Templates**: Reusable output formats

---

## License

- **Enterprise Design Thinking**: Content adapted from IBM's publicly available materials
- **Data Analytics Skills**: Adapted from Nimrod Fisher's work (check original repository for license)
- **This compilation**: MIT License

---

## Maintenance

**Last Updated**: June 9, 2026  
**Maintainer**: Wisu Suntoyo

To update skills:
1. Modify SKILL.md files as needed
2. Update scripts, references, or templates
3. Update this README if structure changes
4. Update AGENTS.md if non-obvious patterns emerge