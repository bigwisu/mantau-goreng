# Data Analytics Setup Guide

This guide explains how to set up and use the data analytics capabilities in this project.

## Quick Start

### 1. Activate Data Analytics Mode

Switch to Data Analytics mode in Bob to access all analytical capabilities.

### 2. Set Up Python Environment

When you first activate Data Analytics mode, Bob will check for required packages and offer to set up the environment:

```bash
# Bob will run this check automatically
python3 -c "import pandas; import numpy; print('✅ All packages ready')"
```

If packages are missing, Bob will offer to:
1. Copy `requirements.txt` to project root
2. Create a virtual environment
3. Install all dependencies

**Manual setup:**
```bash
# Copy requirements
cp .bob/skills/requirements.txt ./requirements.txt

# Create virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 3. Optional: Set Up Jupyter Notebook

For interactive analysis, Bob can set up Jupyter Notebook:

```bash
# Install Jupyter
pip install jupyter notebook ipykernel

# Bob will create starter notebook
mkdir -p notebooks

# Launch Jupyter
jupyter notebook notebooks/
```

## Directory Structure

The project uses a **flat, organized structure**:

```
project/
├── data/              # Data files
│   ├── raw/           # Original, unmodified data
│   ├── processed/     # Cleaned, transformed data
│   └── exports/       # Query results, analysis outputs
│
├── scripts/           # Generated Python scripts
├── notebooks/         # Jupyter notebooks
├── data-analysis/     # Analysis outputs (visualizations, reports, summaries)
├── design-thinking/   # Design thinking deliverables
├── docs/              # Other project documentation
│
├── .bob/              # Bob configuration and skills
└── requirements.txt   # Python dependencies (copied from .bob/skills/)
```

## File Naming Conventions

All analysis outputs use date-prefixed naming:

### Scripts
- **Location**: `scripts/`
- **Format**: `YYYY-MM-DD_descriptive_name.py`
- **Example**: `scripts/2026-06-09_cohort_retention.py`

### Notebooks
- **Location**: `notebooks/`
- **Format**: `YYYY-MM-DD_analysis_name.ipynb`
- **Example**: `notebooks/2026-06-09_customer_segmentation.ipynb`

### Data Analysis Outputs
- **Location**: `data-analysis/`
- **Visualizations**: `YYYY-MM-DD_chart_name.{png|svg|html}`
- **Reports**: `YYYY-MM-DD_report_name.md`
- **Examples**:
  - `data-analysis/2026-06-09_retention_curve.png`
  - `data-analysis/2026-06-09_executive_summary.md`
  - `data-analysis/2026-06-09_insights.md`

## Data Storage

### File-Based Data

Store data files in the `data/` directory:

```bash
# Raw data (original files)
data/raw/customer_data.csv
data/raw/transactions.xlsx

# Processed data (cleaned/transformed)
data/processed/customer_data_clean.parquet
data/processed/cohort_analysis.csv

# Exports (analysis results)
data/exports/2026-06-09_segment_summary.csv
```

**Supported formats**: CSV, Excel (.xlsx), Parquet, JSON

### Database Connections

For live database connections, use environment variables:

1. Create `.env` file (excluded from git):
```bash
# PostgreSQL
POSTGRES_URL=postgresql://user:password@host:port/database

# MySQL
MYSQL_URL=mysql://user:password@host:port/database

# SQLite
SQLITE_URL=sqlite:///path/to/database.db
```

2. Load in Python:
```python
import os
from dotenv import load_dotenv
import pandas as pd
from sqlalchemy import create_engine

load_dotenv()
engine = create_engine(os.getenv('POSTGRES_URL'))
df = pd.read_sql("SELECT * FROM table", engine)
```

## Available Skills

### 1. Data Quality & Validation (5 sub-skills)
- Programmatic EDA
- Data Quality Audit
- Query Validation
- Schema Mapper
- Metric Reconciliation

### 2. Documentation & Knowledge (5 sub-skills)
- Semantic Model Builder
- Analysis Documentation
- Data Catalog Entry
- SQL to Business Logic
- Analysis Assumptions Log

### 3. Data Analysis & Investigation (7 sub-skills)
- Cohort Analysis
- Segmentation Analysis
- Funnel Analysis
- Time Series Analysis
- Root Cause Investigation
- A/B Test Analysis
- Business Metrics Calculator

### 4. Data Storytelling & Visualization (5 sub-skills)
- Insight Synthesis
- Visualization Builder
- Executive Summary Generator
- Dashboard Specification
- Data Narrative Builder

### 5. Stakeholder Communication (5 sub-skills)
- Technical to Business Translator
- Stakeholder Requirements Gathering
- Analysis QA Checklist
- Methodology Explainer
- Impact Quantification

### 6. Workflow Optimization (4 sub-skills)
- Analysis Planning
- Context Packager
- Peer Review Template
- Analysis Retrospective

## Python Scripts

### Skill Scripts (39 available)

Pre-built scripts in `.bob/skills/{category}/{sub-skill}/scripts/`:

```bash
# Example: Data overview
python .bob/skills/data-quality-validation/programmatic-eda/scripts/data_overview.py \
  --input data/raw/customer_data.csv

# Example: Cohort analysis
python .bob/skills/data-analysis-investigation/cohort-analysis/scripts/cohort_builder.py \
  --input data/raw/user_events.csv \
  --cohort-col signup_date \
  --event-col activity_date

# Example: A/B test analysis
python .bob/skills/data-analysis-investigation/ab-test-analysis/scripts/ab_test_analyzer.py \
  --control-n 5000 --control-conv 480 \
  --treatment-n 5100 --treatment-conv 530
```

### Generated Scripts

Custom scripts created during analysis are saved to `scripts/`:

```bash
# Run generated script
python scripts/2026-06-09_custom_analysis.py \
  --input data/raw/data.csv \
  --output data/exports/results.csv
```

## Git Tracking

### What's Tracked
- ✅ Analysis reports (`data-analysis/*.md`)
- ✅ Project documentation
- ✅ Configuration files
- ✅ Requirements.txt

### What's Ignored
- ❌ Data files (`data/**/*`)
- ❌ Generated scripts (`scripts/*.py`)
- ❌ Jupyter notebooks (`notebooks/*.ipynb`)
- ❌ Visualizations (`data-analysis/*.png`, `*.svg`, `*.html`)
- ❌ Virtual environment (`venv/`)
- ❌ Environment variables (`.env`)

This keeps the repository clean while preserving important documentation.

## Workflow Examples

### New Dataset Investigation

```
1. Store data → data/raw/dataset.csv
2. Run Programmatic EDA → understand structure
3. Run Data Quality Audit → assess quality
4. Document findings → data-analysis/YYYY-MM-DD_data_quality.md
```

### Complete Analysis Project

```
1. Analysis Planning → structure approach
2. Execute analysis → use appropriate skills
3. Generate visualizations → save to data-analysis/
4. Create executive summary → data-analysis/YYYY-MM-DD_executive_summary.md
5. Run QA checklist → verify quality
6. Analysis Retrospective → capture learnings
```

### Interactive Analysis with Jupyter

```
1. Launch Jupyter → jupyter notebook notebooks/
2. Create notebook → YYYY-MM-DD_analysis_name.ipynb
3. Load data → from data/raw/ or database
4. Perform analysis → use pandas, numpy
5. Create visualizations → save to data-analysis/
6. Export results → to data/exports/
7. Document findings → in data-analysis/
```

## Best Practices

1. **Validate Early** - Check data quality before analysis
2. **Be Systematic** - Follow structured workflows
3. **Document Everything** - Create reusable reports
4. **Use Version Control** - Track reports, not data
5. **Organize Outputs** - Follow naming conventions
6. **Test Edge Cases** - Don't just check happy paths
7. **Communicate Clearly** - Tailor to your audience
8. **Show Business Value** - Connect findings to impact

## Troubleshooting

### Missing Packages
```bash
# Check what's installed
pip list | grep -E "pandas|numpy"

# Reinstall from requirements
pip install -r requirements.txt
```

### Jupyter Not Starting
```bash
# Install Jupyter
pip install jupyter notebook ipykernel

# Register kernel
python -m ipykernel install --user --name=venv

# Launch
jupyter notebook
```

### Import Errors in Scripts
```bash
# Activate virtual environment first
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Then run script
python scripts/script_name.py
```

## Additional Resources

- **Skills Documentation**: `.bob/skills/README.md`
- **Security Review**: `.bob/skills/SECURITY_REVIEW.md`
- **Python Requirements**: `.bob/skills/requirements.txt`
- **Individual Skills**: `.bob/skills/{category}/SKILL.md`

## Support

For questions or issues:
1. Check skill documentation in `.bob/skills/`
2. Review this setup guide
3. Consult Bob in Data Analytics mode