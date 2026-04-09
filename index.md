---
layout: default
title: Hospital Readmissions and Unplanned Visits Analysis
---

# Hospital Readmissions and Unplanned Visits Analysis

## Description

I built this project out of curiosity to see what I could learn from open public healthcare data. Instead of using a synthetic dataset, I wanted to work with something real, so I used publicly available CMS data to explore patterns in unplanned hospital visits and readmission-related performance across U.S. hospitals.

What interested me most was the chance to see how these quality measures vary across hospitals and whether factors like state, hospital type, and overall hospital rating seemed to be associated with different outcomes.

## Purpose

My goal with this project was to better understand how hospitals differ on selected unplanned visit and readmission-related measures using open public CMS data, while also practicing the full data analysis process from start to finish.

I approached the project using the **Ask → Prepare → Process → Analyze → Share → Act** framework.

## Data Sources

- Unplanned Hospital Visits - Hospital
- https://data.cms.gov/provider-data/dataset/632h-zaca?utm_source=chatgpt.com

## Tools Used

- Tableau
- CMS Provider Data

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

![Compared Group by Measure](Compared%20Goub%20by%20Measure.png)

## Methodology

I used CMS Unplanned Hospital Visits hospital-level data to build an interactive Tableau dashboard. I cleaned score fields, filtered invalid values, grouped CMS comparison labels into broader categories, and created views at the measure, state, and hospital level.

The dashboard is structured to show:
- broad measure-level comparisons
- state-level average comparisons
- compared-to-national category distributions
- hospital-level rankings for a selected measure

## Key Findings

- Average reported CMS scores vary meaningfully across measures, which suggests that different quality metrics operate on very different baseline levels.
- State-level averages show visible variation, though interpretation should be cautious because reporting mix differs across states and territories.
- Compared-to-national categories are not evenly distributed across measures, with some measures clustering more heavily in “No Different” style categories and others showing wider spread.
- The hospital drilldown is most useful when interpreted within a single selected measure rather than as an overall hospital ranking.

## How to Read the Dashboard

- **Avg Score by Measure** shows average reported scores across CMS measures.
- **Avg Score by State** compares average scores across states and territories.
- **Compared Group by Measure** shows how hospitals are distributed across CMS comparison categories.
- **Hospital Drilldown** updates based on the selected measure and helps identify relative leaders for that metric.

## Limitations

This dashboard is descriptive and exploratory. It is intended to surface patterns in publicly available CMS data, not make causal claims about hospital quality. Results should be interpreted within the context of each selected CMS measure rather than as a single overall ranking of hospitals.
