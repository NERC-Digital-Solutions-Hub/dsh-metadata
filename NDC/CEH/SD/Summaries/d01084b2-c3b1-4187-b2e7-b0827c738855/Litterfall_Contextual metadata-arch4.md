# Litterfall in human-modified forests of Eastern Amazonia

## Overview
- Dataset of litterfall measurements from 20 Amazonian forest plots across a gradient of prior human disturbance.
- Plots categorized as undisturbed primary, logged primary, logged-and-burned primary, and secondary forests.
- Data collected from January 2015 to October 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF).

## Data collection and methods
- Six litterfall traps per plot (0.25 m2 each; 50 x 50 cm), placed 1.20 m above ground and spaced 50 m apart.
- Traps collected every two weeks from February 2015 to October 2018.
- Samples field-lab processed by separating into six components: leaves, flowers, fruits, seeds, wood, and rest (non-identifiable material).
- Samples oven-dried at 80°C for 3 days and weighed to the nearest 0.01 g.
- Data include whether plots burned during the 2015-16 El Niño.

## Data structure and variables
- Data file: Litterfall.csv (comma-separated values), attached.
- Core columns:
  - Catchment (microcatchment, ~5,000 ha)
  - Transect (plot number within catchment)
  - Plot (unique plot code combining catchment and transect)
  - Forest_pre_El_nino (disturbance class before El Niño)
  - El_Nino_fire (binary: 1 = fire occurred, 0 = no fire)
  - Litter (trap number 1–6)
  - Day (date of data collection)
  - Team (data-collection team)
  - Leaf (g): dry weight of leaves
  - Wood (g): dry weight of woody material
  - Flower (g): dry weight of flowers
  - Seed (g): dry weight of seeds
  - Fruit (g): dry weight of fruits
  - Rest (g): dry weight of other material
  - Total (g): total dry weight for the trap contents
  - Notes (field notes)
- Disturbance classes: undisturbed primary, logged primary, logged-and-burned primary, secondary.
- Spatial and temporal scope:
  - 20 plots across multiple coordinates (latitude/longitude listed for each plot)
  - Sampling window: Feb 2015 – Oct 2018

## Spatial and temporal coverage
- Coordinates provided for each plot (latitude and longitude).
- Sampling period spans February 2015 through October 2018, with data collected biweekly.

## Data quality and governance
- Data captured with standardized trap method and consistent drying/weighing protocol.
- Metadata captures forest disturbance history, El Niño fire events, sampling date, and trap identity to support traceability and re-analysis.
- Dataset designed for cross-site comparison of litter production across disturbance regimes and under climatic events.

## Potential uses and considerations for data leaders
- Uses:
  - Assess impact of human modification on litter production across forest types.
  - Compare litter inputs before/after El Niño fire events.
  - Integrate with carbon cycle models and nutrient cycling studies.
  - Cross-plot analyses of litter components (leaves, wood, flowers, fruits, seeds, rest).
- Considerations:
  - Ensure alignment of date formats and trap numbers when merging with other datasets.
  - Leverage El_Nino_fire and Forest_pre_El_nino fields for stratified analyses by disturbance and fire history.
  - Manage metadata to maintain discoverability and assist future updates (e.g., plot-level metadata beyond provided fields).
  - Be mindful of the geographic scope (20 plots in Eastern Amazonia) when generalizing findings.
  - Use Total (g) alongside component masses to validate data integrity and gap filling strategies.