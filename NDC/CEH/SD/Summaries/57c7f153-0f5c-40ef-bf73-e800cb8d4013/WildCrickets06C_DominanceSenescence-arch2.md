# WildCrickets06C_DominanceSenescence

## Overview
- A dataset describing success per fight and individual male crickets.
- For each encounter, records include Year (year the cricket was alive), ID (individual identifier), Age (age at fight in days), AgeDiff (age difference vs. opponent in days), SizeDiff (size difference vs. opponent in grams), and Won (1 if the fight was won, 0 otherwise).

## Data fields and definitions
- Year: Year when the cricket was alive.
- ID: Individual identification.
- Age: Age at fight in days.
- AgeDiff: Age difference relative to opponent in days.
- SizeDiff: Size difference relative to opponent in grams.
- Won: Fight outcome (1 = won, 0 = not won).

## How analysts can use this data
- Assess how aging relates to fighting success (dominance senescence) across individuals.
- Explore effects of opponent differences: AgeDiff and SizeDiff as predictors of win probability.
- Track individual-level patterns over time by linking Age and Won across fights for each ID.
- Compare outcomes across different Years to identify temporal trends in dominance or aging.

## Data quality, standardization, and access considerations
- Ensure consistent units (days for Age/AgeDiff, grams for SizeDiff) and clear definition of each field.
- Validate and clean IDs and outcomes to support reliable cross-fight comparisons.
- Store the dataset in a standard repository and upload to appropriate portals to enable reuse and interoperability.
- Consider data quality steps such as handling missing values and potential multiple fights per individual.