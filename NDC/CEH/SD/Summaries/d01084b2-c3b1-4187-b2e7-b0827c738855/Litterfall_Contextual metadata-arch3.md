# Litterfall in human-modified forests of Eastern Amazonia

## Overview
- Dataset of litterfall measurements in 20 Amazonian forest plots across a gradient of prior human disturbance.
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (n = 5 per class).
- Collected from January 2015 to October 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).
- Disturbance classification based on canopy disturbance analysis from satellite imagery (1988–2010) and field assessments (fire scars, charcoal, logging debris).

## Study design and disturbance gradient
- Each plot is 250 x 10 m, with six plots per disturbance class.
- Designed to compare litterfall production across varying levels of prior disturbance.

## Data collection methods
- Six litter traps per plot (50 x 50 cm; 0.25 m²), placed 1.2 m above ground, spaced 50 m apart.
- Contents collected every two weeks from February 2015 to October 2018.
- Samples were divided into six components (leaves, flowers, fruits, seeds, wood, and rest), oven-dried at 80°C for 3 days, and weighed to the nearest 0.01 g.

## Spatial and temporal coverage
- Plot coordinates provided (20 plots with unique codes such as 112_12, 112_8, 129_10, etc.), including latitude and longitude for each plot.
- Temporal scope covers field data collection in 2015–2018, with El Niño relevant to the study period (El Niño of 2015–16 noted).

## Data structure and content
- Data file: Litterfall.csv (comma-separated values).
- Key columns:
  - Catchment, Transect, Plot (unique identifiers for microcatchments, transects, and plots)
  - Forest_pre_El_nino (disturbance class before El Niño)
  - El_Nino_fire (binary: 1 = fire, 0 = no fire)
  - Litter (plot-level litterfall)
  - Day (date of data collection)
  - Team (data collection team)
  - Leaf (g), Wood (g), Flower (g), Seed (g), Fruit (g), Rest (g), Total (g) (mass by component and total)
  - Notes (field notes)

## Provenance and data governance
- Data collected under the NERC HMTF programme, ensuring data provenance and alignment with program objectives.

## Access and format
- A CSV file containing the dataset is attached, including detailed column definitions and coordinates for each plot.