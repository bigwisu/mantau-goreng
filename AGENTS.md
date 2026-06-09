# AGENTS.md

This file provides guidance to agents when working with code in this repository.

## Project Type
IBM Enterprise Design Thinking research and documentation repository.

## Key Non-Obvious Details

### Skill System
- **Skills available**: 7 reusable skills in `.bob/skills/`
- All skills use YAML frontmatter with `allowed-tools`, `description`, `skill-author`, `metadata`
- Skills are portable across projects (self-contained documentation)
- Author: Wisu Suntoyo

#### Enterprise Design Thinking Skill
- Location: `.bob/skills/enterprise-design-thinking/`
- Fully self-contained with all IBM EDT documentation
- 29 activities in `toolkit/` subdirectory
- Quick reference: `references/toolkit_quick_reference.md`

#### Data Analytics Skills (6 skills)
Adapted from data-analytics-skills by Nimrod Fisher:

1. **data-quality-validation** - 5 activities for ensuring data reliability
   - Programmatic EDA, Data Quality Audit, Query Validation, Schema Mapper, Metric Reconciliation
   
2. **documentation-knowledge** - 5 activities for building reusable context
   - Semantic Model Builder, Analysis Documentation, Data Catalog Entry, SQL to Business Logic, Analysis Assumptions Log
   
3. **data-analysis-investigation** - 7 activities for discovering insights
   - Cohort Analysis, Segmentation Analysis, Funnel Analysis, Time Series Analysis, Root Cause Investigation, A/B Test Analysis, Business Metrics Calculator
   
4. **data-storytelling-visualization** - 5 activities for communicating findings
   - Insight Synthesis, Visualization Builder, Executive Summary Generator, Dashboard Specification, Data Narrative Builder
   
5. **stakeholder-communication** - 5 activities for bridging technical and business
   - Technical to Business Translator, Stakeholder Requirements Gathering, Analysis QA Checklist, Methodology Explainer, Impact Quantification
   
6. **workflow-optimization** - 4 activities for improving processes
   - Analysis Planning, Context Packager, Peer Review Template, Analysis Retrospective

### IBM Enterprise Design Thinking Documentation
- **All documentation is in the skill directory** for portability across projects
- Framework: `.bob/skills/enterprise-design-thinking/toolkit/00_framework.md`
- Toolkit index: `.bob/skills/enterprise-design-thinking/toolkit/01_toolkit.md`
- 29 activities: `.bob/skills/enterprise-design-thinking/toolkit/02-30-toolkit-deck-*.md`
- Quick reference: `.bob/skills/enterprise-design-thinking/references/toolkit_quick_reference.md`

### Custom Mode
- **Design Thinking mode** available via `.bob/custom_modes.yaml`
- Specialized for IBM Enterprise Design Thinking facilitation
- Focuses on The Loop (Observe → Reflect → Make), The Keys (Hills, Playbacks, Sponsor Users), and The Principles
- Conversational mode for facilitating EDT activities
- Restricted to editing documentation files only (`.md`, `.txt`, `.yaml`, `.yml`)
- Access via mode switcher or `/mode design-thinking` command

### PDF Conversion
- PDFs converted to markdown using `markitdown` with PDF support
- Virtual environment setup: `python3 -m venv venv && source venv/bin/activate && pip install 'markitdown[pdf]'`
- Conversion command: `markitdown input.pdf > output.md`

### Content Organization
- Design thinking methodology content: `docs/design-thinking-methodology.md`
- IBM EDT documentation: `.bob/skills/enterprise-design-thinking/toolkit/`
- This file (AGENTS.md) is for agent instructions only