# WildCrickets04_Pheromones Description of content

## Overview
- The file contains the pheromonal profile of cuticular hydrocarbons (CHC) collected from the thorax of adult crickets.
- It covers a total of 32 CHC compounds.

## Data structure and fields
- Year: the year when the cricket was alive.
- Tag: a two-character code identifying the cricket in video recordings; read from a plastic tag on the pronotum.
- Sex: male (M) or female (F).
- Peak1 to Peak40: columns representing CHC peaks/compounds; each column holds the score for a specific compound.
- Note: There is a discrepancy in the description—the dataset is stated as having 32 compounds, yet the columns are labeled Peak1 to Peak40. The final statement claims these 32 columns correspond to 32 CHC peaks, indicating potential schema inconsistency that should be clarified.

## Potential analyses and uses for data leaders
- Understand CHC profiles across individual crickets and by sex or year.
- Compare profiles to identify which hydrocarbons differentiate crickets or cohorts.
- Prepare data for statistical analyses (e.g., multivariate analyses, clustering, PCA) to explore patterns in CHC composition.

## Data governance and quality considerations
- Metadata completeness and standardization (Year, Tag, Sex) to enable reliable filtering and grouping.
- Clarify and standardize the peak naming convention (32 vs 40 peaks) to ensure consistency and reproducibility.
- Check for missing values and outliers in Peak columns; assess data quality and suitability for downstream analyses.
- Ensure documentation matches the actual data structure; update metadata if discrepancies remain.
- Improve discoverability and maintainability by cataloging the dataset with explicit variable definitions and units.