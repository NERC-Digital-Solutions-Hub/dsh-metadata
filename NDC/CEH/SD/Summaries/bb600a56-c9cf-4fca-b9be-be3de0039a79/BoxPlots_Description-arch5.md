# LOCAR BASELINE DATASETS LOCAR

## Overview
- Box and whisker plots assess data quality by visualising range, median, and quartiles.
- They help interpret distribution and identify how much data falls within the central box and the presence of outliers.

## Plot structure
- Y-axis: number line corresponding to the units of the determinand.
- X-axis: different sites; site IDs label each position.
- Red line: median of the determinand at each site.
- Box edges: Q1 (25th percentile) and Q3 (75th percentile).

## Calculations
- Interquartile range (IQR) = Q3 − Q1.
- Lower whisker = Q1 − 1.5 × IQR; upper whisker = Q3 + 1.5 × IQR.
- Data points outside whiskers are classified as outliers.

## Relevance for Data Stewards
- Used as a visual quality check across sites to ensure consistent data distribution and detect anomalies.
- Supports metadata and documentation by clarifying axis units, determinand, and site-specific measurements.
- Aids in identifying data that may require cleaning, transformation, or special handling due to outliers or non-standard distributions.
- Provides a basis for communicating data quality to data creators and users, and for justifying data curation or embargo decisions if present.