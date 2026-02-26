# WildCrickets06H_EarlyDominanceVsSurvival

## Overview
- Dataset describing individual male crickets with lifespan and early-life dominance classification.
- Early Dominance is categorized as High (H) or Low (L) based on whether it is above or below the population median.

## Data Content
- Year: Year when the cricket was alive.
- Lifespan: Lifespan in days.
- EarlyDominance: High (H) or Low (L) dominance in early life.

## Variable Details
- Year: Temporal context for each record.
- Lifespan: Numeric value representing days lived.
- EarlyDominance: Categorical marker indicating early-life social status using a median-based threshold.

## Classification Rule
- EarlyDominance is determined by comparing early-life dominance to the population median::
  - High (H) if above median
  - Low (L) if below median

## Potential Analyses for Data Leaders
- Examine the relationship between early-life dominance and survival duration.
- Cohort or year-based comparisons to identify patterns across time.
- Descriptive summaries of Lifespan by EarlyDominance category.

## Data Governance and Metadata Considerations
- Need clear definitions for Year and Lifespan units, and documentation of how the population median is computed.
- Ensure metadata includes method of data collection, scope, and any handling of missing values.
- Establish naming conventions and discoverability to support integration with related datasets (e.g., broader cricket behavior or survival studies).