# Stem respiration in human-modified forests of Eastern Amazonia

## Overview
- A dataset (StemRespirationData.csv) of stem respiration measurements from 20 Amazonian forest plots (250 x 10 m each) spanning a gradient of prior human disturbance.
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (n = 5 plots per class).
- Disturbance classification based on canopy disturbance from a satellite-based chronosequence (1988–2010) and field assessments (fire scars, charcoal, logging debris).
- Data collected from June 2015 to July 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF; grant NE/K016431/1).

## Data collection design and methods
- At least 13 trees per plot fitted with stem collars installed ~20 cm above dendrometers; trees selected across five DBH classes: 10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, ≥50 cm.
- Collars: PVC, ~5 cm tall, 10 cm diameter; connected to an infrared gas analyzer (EGM5) to measure stem CO2 efflux (stem respiration).
- Measurements taken every 3 months; if a tree died, its collar was removed and a new collar installed on a tree in the same size class (preferably with a dendrometer).
- N/A entries indicate missing measurements; the notes column contains reasons for missing data.
- Coordinates (lat/long) are provided for plots, enabling spatial context.

## Data structure and key fields
- Data file: StemRespirationData.csv (comma-separated)
- Core columns and descriptions:
  - Date: Date of data collection
  - Catchment: Microcatchment (~5,000 ha) containing the plot
  - Transect: Plot number within each catchment
  - Plot code: Unique code combining catchment and transect
  - Forest: Disturbance class before the 2015–16 El Niño
  - Fire: Whether the plot burned during the 2015–16 El Niño (1 = yes, 0 = no)
  - Tree TAG: Identifier for the individual with the collar
  - Time: Exact sampling time
  - Collar height: Height of the collar at measurement
  - CO2 initial: CO2 concentration at start of measurement
  - CO2 final: CO2 concentration at end of measurement
  - Flux: Measured stem respiration flux
  - Field notes: Field processing notes
- Data are structured to support repeated measures per tree across time, nested within plots and catchments.

## Spatial information
- Coordinates are provided for multiple plots (e.g., 112_12, 112_8, 129_10, 129_11, 129_5, 260_1, 260_4, 260_5, 261_10, 261_9, 357_2, 357_3, 357_4, 357_6, 357_9, 363_3, 363_6, 363_7, 69_11, 69_8) with corresponding latitudes and longitudes.
- Geographic placement supports analyses by microcatchment and spatial gradients of disturbance.

## Data provenance, quality, and notes
- Collected under the NERC HMTF program; dataset linked to Grant NE/K016431/1.
- Data quality considerations:
  - Missing values indicated as N/A; reasons documented in Field notes.
  - Field notes may contain processing details affecting interpretation of Flux values.
- The dataset provides explicit metadata and a clear structure to enable traceability, reproducibility, and discovery (e.g., plot codes, catchments, disturbance classifications).

## Potential uses and analysis considerations for analysts
- Research questions:
  - How does stem respiration flux vary across disturbance classes (undisturbed, logged, burned, secondary)?
  - How do flux patterns change over time (seasonal or by sampling date) within and across plots?
  - How do stem respiration flux relate to tree size (DBH class) and collar height?
- Analytical approaches:
  - Use mixed-effects models with Flux as the response, disturbance class, time, DBH class, and collar height as predictors; include random effects for trees nested within plots and plots within catchments to account for repeated measures and spatial structure.
  - Explore interactions between disturbance class and time to capture temporal responses to disturbance.
  - Validate whether Flux correlates with CO2 initial/final concentrations and whether any derived metrics (e.g., instantaneous flux changes) provide additional insight.
- Data preparation tips:
  - Handle missing data with appropriate missingness assumptions; consult Field notes for context on N/A entries.
  - Leverage the Plot code, Transect, Catchment, and Forest columns to align datasets and enable hierarchical modeling.
  - Consider using the coordinates for spatial modeling or covariate analyses of geographic patterns.
- Limitations to keep in mind:
  - Observational design across disturbance classes; potential confounders not controlled experimentally.
  - Units of Flux are not explicitly stated in the excerpt; confirm units from the original dataset before quantitative comparisons.