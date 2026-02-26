# WildCrickets06C_DominanceSenescence Description of content

## Overview
- Describes a dataset capturing success per fight for individual male wild crickets.
- Key attributes include temporal context, individual identity, and fight outcomes.

## Data fields and definitions
- Year: Year of the fight.
- Year when the cricket was alive: Year in which the cricket was alive (temporal context for the individual).
- ID: Unique identifier for each cricket.
- Age: Age of the cricket at the time of the fight, in days.
- AgeDiff: Difference in age relative to the opponent, in days.
- SizeDiff: Difference in size relative to the opponent, in grams.
- Won: Fight outcome for the cricket (1 = won, 0 = did not win).

## Data quality and metadata considerations
- Clear definitions needed for each field (e.g., confirm unit consistency for Age, AgeDiff, SizeDiff).
- Verify interpretation of “Year when the cricket was alive” and its relation to fight year.
- Ensure consistent coding of Won (binary) and handling of missing values.
- Documentation should specify data collection methods, sources of measurements (age, size), and any data transformations.

## Potential uses for data leaders
- Analyze how age and age difference with opponents relate to fight outcomes.
- Explore the influence of size difference on dominance and success.
- Model dominance senescence by tracking success across years and ages.
- Inform studies of animal behavior, aging processes, and competitive strategies.

## Governance, usability, and implementation notes
- Ensure metadata standards for units, definitions, and data lineage to support discoverability.
- Consider adding or clarifying fields about opponent ID, fight date, location, and additional context to improve interpretability.
- Promote data reuse through clear data licensing and provenance, enabling cross-study comparisons.