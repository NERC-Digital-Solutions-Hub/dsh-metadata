# WildCrickets06C_DominanceSenescence Description of content

## Overview
- A dataset focusing on success per fight and individual male crickets, capturing longitudinal fight data.

## Variables (content description)
- Year: year when the cricket was alive
- ID: individual identification
- Age: age at fight in days
- AgeDiff: age difference relative to opponent in days
- SizeDiff: size difference relative to opponent in grams
- Won: 1 if the cricket won the fight, 0 otherwise

## Analytical opportunities for data support
- Compute win rates by age, age difference, and size difference
- Investigate dominance and senescence patterns across years
- Compare individuals (by ID) for consistency in outcomes
- Integrate with additional data (environment, other fights) to analyze drivers

## Data preparation and quality considerations
- Check for missing values and correct data types
- Ensure consistent units (grams, days)
- Validate ID consistency across fights and deduplicate as needed

## Outputs and dissemination
- Self-serve analyses via dashboards, pivot tables, and charts
- Reports with guidance on interpreting fight outcomes
- Early prototypes to solicit stakeholder feedback