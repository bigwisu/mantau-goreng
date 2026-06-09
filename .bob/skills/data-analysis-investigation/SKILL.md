---
name: data-analysis-investigation
description: Core analytical workflows with 7 systematic approaches for discovering insights through cohort analysis, segmentation, funnels, time series, root cause investigation, A/B testing, and business metrics calculation. Use for deep-dive analysis and investigation.
allowed-tools: Read Write Edit Bash
license: MIT license
metadata:
  version: "1.0"
  skill-author: Wisu Suntoyo
  adapted-from: data-analytics-skills by Nimrod Fisher
  category: "03-data-analysis-investigation"
---

# Data Analysis & Investigation

## Overview

This skill provides 7 core analytical workflows for discovering insights:

1. **Cohort Analysis** - Time-based cohort tracking with retention curves
2. **Segmentation Analysis** - Customer/user segmentation with actionable profiles
3. **Funnel Analysis** - Conversion funnel with drop-off root-cause
4. **Time Series Analysis** - Trend detection, seasonality, and forecasting
5. **Root Cause Investigation** - Structured diagnosis of unexpected metric changes
6. **A/B Test Analysis** - Rigorous experiment analysis with significance testing
7. **Business Metrics Calculator** - Standard business metric calculation with benchmarks

**Core Philosophy**: Use structured analytical frameworks to discover insights systematically.

---

## When to Use This Skill

Use this skill when:
- **Analyzing retention**: Track how cohorts behave over time
- **Understanding segments**: Identify distinct user or customer groups
- **Optimizing conversions**: Analyze funnel drop-offs and improvements
- **Detecting trends**: Identify patterns, seasonality, and anomalies
- **Investigating changes**: Diagnose unexpected metric movements
- **Evaluating experiments**: Analyze A/B test results rigorously
- **Calculating KPIs**: Compute standard business metrics consistently

---

## Activity 1: Cohort Analysis

**Purpose**: Time-based cohort tracking with retention curves.

### When to use
- You want to understand user retention by signup month or first purchase date
- You need to compare retention across different acquisition channels
- You're evaluating the impact of a product change on long-term engagement
- You want to forecast future revenue based on cohort behavior

### Process
1. **Define the cohort** - Choose the cohort dimension (signup month, first purchase date, etc.).
2. **Define the retention metric** - Decide what "retained" means (active user, repeat purchase, etc.).
3. **Set the time window** - Choose the analysis period (weeks, months, quarters).
4. **Build the cohort table** - Create a matrix showing retention rates by cohort and time period.
5. **Calculate retention curves** - Plot retention over time for each cohort.
6. **Identify patterns** - Look for improving/declining retention, seasonal effects, or channel differences.
7. **Generate insights** - Explain what's driving retention patterns and recommend actions.

### Inputs needed
- **Required**: User/customer activity data with timestamps
- **Required**: Cohort definition (what groups users into cohorts)
- **Required**: Retention definition (what counts as "retained")
- **Optional**: Segmentation dimensions (channel, product, geography)
- **Optional**: Benchmark retention rates

### Output
- Cohort retention matrix
- Retention curves by cohort
- Pattern analysis and insights
- Recommendations for improving retention

---

## Activity 2: Segmentation Analysis

**Purpose**: Customer/user segmentation with actionable profiles.

### When to use
- You want to identify distinct customer groups for targeted marketing
- You need to understand which user segments are most valuable
- You're designing personalized experiences for different user types
- You want to allocate resources based on segment potential

### Process
1. **Choose segmentation variables** - Select dimensions for segmentation (behavior, demographics, value).
2. **Prepare the data** - Aggregate user-level metrics and features.
3. **Apply segmentation method** - Use clustering, RFM analysis, or rule-based segmentation.
4. **Profile each segment** - Describe characteristics, behaviors, and value of each segment.
5. **Validate segments** - Check that segments are distinct, stable, and actionable.
6. **Size and prioritize** - Calculate segment sizes and prioritize by business value.
7. **Create action plan** - Recommend strategies for each segment.

### Inputs needed
- **Required**: User/customer data with behavioral and demographic attributes
- **Required**: Business context - what decisions will segmentation inform?
- **Optional**: Existing segmentation to compare against
- **Optional**: Minimum segment size requirements

### Output
- Segment definitions and profiles
- Segment sizes and characteristics
- Value analysis by segment
- Actionable recommendations per segment

---

## Activity 3: Funnel Analysis

**Purpose**: Conversion funnel with drop-off root-cause analysis.

### When to use
- You want to optimize a multi-step conversion process (signup, checkout, onboarding)
- You need to identify where users are dropping off in a flow
- You're comparing funnel performance across segments or time periods
- You want to estimate the impact of improving specific funnel steps

### Process
1. **Define funnel steps** - List the sequential steps in the conversion process.
2. **Calculate step conversion rates** - Measure what % of users complete each step.
3. **Identify drop-off points** - Find steps with the highest abandonment rates.
4. **Segment the funnel** - Compare funnel performance across user segments, channels, or time periods.
5. **Investigate drop-offs** - Analyze why users abandon at specific steps (UX issues, friction, confusion).
6. **Estimate impact** - Calculate potential lift from improving each step.
7. **Prioritize improvements** - Recommend which steps to optimize first.

### Inputs needed
- **Required**: Event data showing user progression through funnel steps
- **Required**: Funnel step definitions
- **Optional**: Segmentation dimensions (device, channel, user type)
- **Optional**: Benchmark conversion rates

### Output
- Funnel visualization with conversion rates
- Drop-off analysis by step
- Segment comparison
- Prioritized improvement recommendations

---

## Activity 4: Time Series Analysis

**Purpose**: Trend detection, seasonality, and forecasting.

### When to use
- You want to understand if a metric is trending up or down
- You need to detect seasonal patterns in your data
- You want to forecast future values of a metric
- You need to identify anomalies or unusual spikes/drops

### Process
1. **Prepare time series data** - Aggregate data at appropriate time granularity (daily, weekly, monthly).
2. **Visualize the series** - Plot the metric over time to identify obvious patterns.
3. **Decompose components** - Separate trend, seasonality, and residuals.
4. **Test for stationarity** - Check if the series has a stable mean and variance.
5. **Identify patterns** - Detect trends, cycles, seasonality, and anomalies.
6. **Build forecast** - Use appropriate method (moving average, exponential smoothing, ARIMA).
7. **Validate and interpret** - Check forecast accuracy and explain findings.

### Inputs needed
- **Required**: Time series data (metric values with timestamps)
- **Required**: Business context - what drives this metric?
- **Optional**: External factors that might influence the metric
- **Optional**: Forecast horizon (how far into the future)

### Output
- Time series visualization
- Trend and seasonality analysis
- Anomaly detection
- Forecast with confidence intervals

---

## Activity 5: Root Cause Investigation

**Purpose**: Structured diagnosis of unexpected metric changes.

### When to use
- A key metric suddenly increased or decreased and you need to know why
- Stakeholders are asking "what happened?" and you need a systematic answer
- You want to rule out data quality issues before investigating business causes
- You need to prioritize which factors to investigate first

### Process
1. **Quantify the change** - Measure the magnitude and timing of the metric change.
2. **Rule out data issues** - Check for pipeline failures, schema changes, or data quality problems.
3. **Segment the metric** - Break down the change by dimensions (product, channel, geography, user segment).
4. **Identify contributing factors** - Find which segments or dimensions drove the change.
5. **Form hypotheses** - Generate possible explanations based on business context.
6. **Test hypotheses** - Validate each hypothesis with data.
7. **Document findings** - Explain the root cause and recommend actions.

### Inputs needed
- **Required**: Metric data showing the change
- **Required**: Historical baseline for comparison
- **Required**: Segmentation dimensions to investigate
- **Optional**: Timeline of recent changes (product launches, marketing campaigns, etc.)
- **Optional**: Related metrics that might provide context

### Output
- Quantified impact of the change
- Segment-level breakdown
- Root cause explanation
- Recommendations to address or capitalize on the change

---

## Activity 6: A/B Test Analysis

**Purpose**: Rigorous experiment analysis with significance testing.

### When to use
- You've run an A/B test and need to determine if results are statistically significant
- You want to calculate the required sample size before launching an experiment
- You need to analyze multiple metrics from an experiment
- You want to understand if results vary across user segments

### Process
1. **Define the experiment** - Document control, treatment, randomization method, and success metrics.
2. **Check experiment validity** - Verify randomization worked and sample sizes are balanced.
3. **Calculate sample statistics** - Compute means, conversion rates, and standard errors for each variant.
4. **Run significance tests** - Perform appropriate statistical tests (t-test, chi-square, etc.).
5. **Calculate effect size** - Measure the practical significance (% lift, absolute difference).
6. **Analyze by segment** - Check if results vary across user segments.
7. **Make recommendation** - Decide whether to ship, iterate, or abandon based on results.

### Inputs needed
- **Required**: Experiment data with user assignments and outcomes
- **Required**: Success metric definition
- **Required**: Significance level (typically 0.05)
- **Optional**: Minimum detectable effect
- **Optional**: Segmentation dimensions for subgroup analysis

### Output
- Statistical significance results
- Effect size and confidence intervals
- Segment-level analysis
- Ship/no-ship recommendation

---

## Activity 7: Business Metrics Calculator

**Purpose**: Standard business metric calculation with benchmarks.

### When to use
- You need to calculate standard business metrics (CAC, LTV, churn rate, etc.)
- You want to ensure metrics are calculated consistently across the organization
- You need to compare your metrics against industry benchmarks
- You're building a metrics dashboard and need canonical definitions

### Process
1. **Identify the metric** - Choose which business metric to calculate (CAC, LTV, MRR, etc.).
2. **Gather inputs** - Collect the data needed for the calculation.
3. **Apply the formula** - Calculate the metric using the standard formula.
4. **Validate the result** - Check if the result makes sense given business context.
5. **Compare to benchmarks** - See how your metric compares to industry standards.
6. **Trend over time** - Calculate the metric for multiple time periods to identify trends.
7. **Document the calculation** - Record the formula, data sources, and assumptions.

### Inputs needed
- **Required**: Metric name to calculate
- **Required**: Data needed for the calculation
- **Optional**: Industry or company benchmarks
- **Optional**: Historical data for trend analysis

### Output
- Calculated metric value
- Benchmark comparison
- Trend analysis
- Documentation of calculation method

---

## Common Workflows

### User Retention Analysis
```
1. Cohort Analysis → understand retention patterns
2. Segmentation Analysis → identify high/low retention segments
3. Root Cause Investigation → diagnose retention issues
4. Recommend improvements
```

### Conversion Optimization
```
1. Funnel Analysis → identify drop-off points
2. Segmentation Analysis → find high-converting segments
3. A/B Test Analysis → validate improvements
4. Business Metrics Calculator → measure impact on KPIs
```

### Metric Investigation
```
1. Time Series Analysis → detect when change occurred
2. Root Cause Investigation → diagnose why it changed
3. Segmentation Analysis → understand which segments drove change
4. Document findings
```

### Experiment Evaluation
```
1. A/B Test Analysis → determine statistical significance
2. Segmentation Analysis → check for segment-level effects
3. Business Metrics Calculator → measure impact on KPIs
4. Make ship/no-ship decision
```

---

## Key Principles

1. **Be systematic** - Follow structured frameworks to avoid missing insights
2. **Segment everything** - Always break down metrics by relevant dimensions
3. **Test rigorously** - Use proper statistical methods for experiments
4. **Validate assumptions** - Check data quality and business logic
5. **Tell the story** - Explain not just what happened, but why it matters
6. **Recommend actions** - Analysis should lead to decisions

---

## References

For detailed implementation guidance, see the original data-analytics-skills repository:
- Category: `03-data-analysis-investigation/`
- Skills: `cohort-analysis/`, `segmentation-analysis/`, `funnel-analysis/`, `time-series-analysis/`, `root-cause-investigation/`, `ab-test-analysis/`, `business-metrics-calculator/`

Each skill includes:
- Detailed SKILL.md with process steps
- Python scripts for calculations and visualizations
- Reference documentation for statistical methods
- Output templates for reports

---

## Integration with Other Skills

**Pairs well with:**
- **Data Quality & Validation** - Validate data before analysis
- **Documentation & Knowledge** - Document methodology and assumptions
- **Data Storytelling & Visualization** - Present findings effectively
- **Stakeholder Communication** - Explain results to business audiences

**Best practices:**
- Run Data Quality Audit before starting analysis
- Use Analysis Assumptions Log to track decisions
- Create visualizations to communicate findings
- Document methodology for reproducibility