# LOCAR BASELINE DATASETS LOCAR

## Purpose
- Use box and whisker plots to visually check the quality of LOCAR data.
- Help interpret the distribution of the data (central tendency, spread) and identify outliers.
- Assess how much data falls within the central box and the length of the whiskers.

## Plot Components and Layout
- Y-axis: number line corresponding to the units of the determinand.
- X-axis: different sites where the determinand was measured; site IDs label sites.
- Median: red line inside the box.
- Box edges: Q1 (25th percentile) and Q3 (75th percentile).
- Whiskers: lower = Q1 − 1.5 × IQR, upper = Q3 + 1.5 × IQR.
- IQR: interquartile range = Q3 − Q1.
- Outliers: points outside the whiskers.

## Data Governance and Metadata Implications
- Ensure clear definitions in metadata for determinand, units, and site IDs.
- Standardize how Q1, Q3, IQR, and whiskers are calculated across datasets.
- Document any data transformations or reductions applied before plotting.
- Capture and communicate any data limitations or potential embargoes impacting visibility of certain data points.

## Quality Assurance and Data Sharing Practices
- Compare distributions across sites to detect site-specific data quality issues.
- Use outliers and whisker lengths as signals for further review or data cleaning.
- Use the plots to confirm data completeness and the representativeness of the central distribution prior to uploading to portals or catalogues.

## Documentation and Reproducibility
- Include the box and whisker figure with a caption describing axes, median, quartiles, and whisker rules.
- Record observed data quality issues and any corrective actions taken (e.g., metadata updates, re-measurement requests).