# WildCrickets06B_SearchingActivitySenescence Description of content

## Overview
- Dataset describing wild crickets focused on searching activity and senescence.
- Observations are structured as periods per individual male adult cricket, classified as short (≤ 77 minutes) or long (> 77 minutes).

## Key variables
- Year: Year of the observation period.
- YearAlive: Year when the cricket was alive.
- ID: Unique identifier for each individual cricket.
- Temp: Temperature during the observation period (°C).
- Age: Age of the cricket in days at the time of sampling.
- Short: Binary indicator for short duration (1 = short period, 0 = not short).

## Data structure and format
- One row per observation period for each individual.
- Fields included: Year, YearAlive, ID, Temp, Age, Short.
- Duration classification used to separate short vs. long observation periods (short defined as ≤ 77 minutes).

## Potential analyses for environmental monitoring
- Track the proportion of short observation periods by Year to assess temporal patterns.
- Examine relationships between temperature (Temp) and activity duration (Short).
- Investigate age-related changes in activity and potential senescence signals.
- Integrate with life-history data (YearAlive) for survival or longevity analyses.

## Data quality, access, and management
- Data undergo verification, quality assurance, cleaning, and transformation.
- Outputs delivered in clear formats (reports, maps, charts).
- Datasets stored and uploaded to appropriate data portals.
- Emphasis on enabling access to underlying data to support reuse beyond final outputs.