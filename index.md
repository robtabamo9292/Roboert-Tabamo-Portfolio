---
layout: default
title: Hospital Readmissions and Unplanned Visits Analysis
---

# Hospital Readmissions and Unplanned Visits Analysis

## Description

I built this project out of curiosity to see what I could learn from open public healthcare data.

What interested me most was the chance to see how these quality measures vary across hospitals and whether factors like state, hospital type, and overall hospital rating seemed to be associated with different outcomes.

## Purpose

My goal with this project was to better understand how hospitals differ on selected unplanned visit and readmission-related measures using open public CMS data, while also practicing the full data analysis process from start to finish.

## Data Sources

- Unplanned Hospital Visits
- https://data.cms.gov/provider-data/dataset/632h-zaca?utm_source

## Tools Used

- Tableau
- CMS.gov Provider Data

## Key Questions

- How much variation exists across hospitals on readmission-related measures?
- Do some states appear to perform differently on average?
- Are certain hospital types associated with better or worse results?
- Is there any visible relationship between overall hospital rating and the selected quality measures?

## Dashboard

I built an interactive Tableau dashboard using open source hospital quality data to explore patterns in unplanned hospital visits and readmission-related performance across hospitals, states, and measures.

The dashboard includes:
- average score by measure
- average score by state
- compared-to-national breakdown by measure
- hospital-level drilldown for a selected measure

### Dashboard Overview

![Hospital Dashboard Overview](Main%20Dashboard.png)

### Avg Score by Measure

![Avg Score by Measure](Avg%20Score%20by%20Measure.png)

### Avg Score by State

![Avg Score by State](Avg%20Score%20by%20State.png)

### Hospital Drilldown

![Hospital Drilldown](Hospital%20Drilldown.png)

### Compared Group by Measure

![Compared Group by Measure](Compared%20Group%20by%20Measure.png)

## Methodology

I used CMS Unplanned Hospital Visits hospital-level data to build an interactive Tableau dashboard. I cleaned score fields, filtered invalid values, grouped CMS comparison labels into broader categories, and created views at the measure, state, and hospital level.

The dashboard is structured to show:
- broad measure-level comparisons
- state-level average comparisons
- compared-to-national category distributions
- hospital-level rankings for a selected measure

## Key Findings

- The dataset contains 67,046 hospital-measure records across 14 CMS measures and 4,789 hospitals. The score scales vary substantially by measure, so raw averages are not directly comparable across measures. For example, average measure scores range from 1.01 for the Ratio of unplanned hospital visits after hospital outpatient surgery to 19.71 for the Heart failure (HF) 30-Day Readmission Rate. The measure comparison view is therefore best read as a within-measure overview, not as a single cross-measure ranking.

- Data completeness varies sharply by measure. Overall, 35,280 records (52.6%) have valid numeric scores and 31,766 (47.4%) do not. The most complete measure is Hybrid Hospital-Wide All-Cause Readmission (HWR), with 4,217 valid scores and an 88.1% valid-score rate. The sparsest is CABG readmission, with only 878 valid scores and an 18.3% valid-score rate. Measures with high invalid-score rates are much less reliable for hospital-level comparison.

- Across records that received a benchmark category, most observations fall into No Different rather than Better or Worse. Among rated records, 84.4% are No Different, 9.4% are Worse, and 6.3% are Better. This indicates a modest skew toward underperformance relative to the benchmark, but the dominant pattern is still that most hospital-measure observations are classified as not materially different from the national benchmark.
  
- The most differentiated measures are the three hospital return days metrics. These show the clearest spread between relative outperformers and underperformers:
  * _Hospital return days for pneumonia patients: 767 Better, 1,284 Worse, 1,587 No Different_
  * _Hospital return days for heart failure patients: 748 Better, 1,007 Worse, 1,400 No Different_
  * _Hospital return days for heart attack patients: 276 Better, 546 Worse, 733 No Different_
  * _These measures provide the strongest separation between hospitals in the comparison categories_
 
- The Avg Score by State view should be interpreted cautiously because it averages valid scores across measures with very different scales. This makes it more useful as a descriptive overview than as a strict state ranking. Small territories with very few valid records appear at the top of the view, for example, VI has 12 valid scores and MP has 8, which further limits comparability at the geography level.

- For a more apples-to-apples geographic comparison, a single high-coverage measure is more defensible. On HWR, among geographies with at least 20 valid hospitals, the lowest average readmission rates are in Maryland (14.43), Washington (14.45), and Oregon (14.48), while the highest are in Puerto Rico (15.70), Massachusetts (15.64), and Florida (15.50). These differences are informative, but they should still be interpreted in the context of hospital mix and reporting volume.
  
- The Hospital Drilldown view is most meaningful when used exactly as designed in the workbook: one selected measure at a time. It is useful for identifying relative leaders within a specific metric, but it should not be interpreted as an overall hospital ranking across all CMS quality measures.


## How to Read the Dashboard

- **Avg Score by Measure** shows average reported scores across CMS measures.
- **Avg Score by State** compares average scores across states and territories.
- **Compared Group by Measure** shows how hospitals are distributed across CMS comparison categories.
- **Hospital Drilldown** updates based on the selected measure and helps identify relative leaders for that metric.

## Limitations

This project purely descriptive and exploratory. It is intended to surface patterns in publicly available CMS data, not make causal claims about hospital quality. Results should be interpreted within the context of each selected CMS measure rather than as a single overall ranking of hospitals.
