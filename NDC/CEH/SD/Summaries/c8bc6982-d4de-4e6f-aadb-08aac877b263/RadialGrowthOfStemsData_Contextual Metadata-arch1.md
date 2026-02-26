# Radial growth in stems in human-modified forests of Eastern Amazonia

- A dataset describing radial growth of stems in 20 Amazonian forest plots arranged across a disturbance gradient prior to the 2015-16 El Niño.
- Disturbance classes included: undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).

## Data overview and scope

- Timeframe: radial growth measurements collected from December 2014 to September 2018.
- Context: part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).
- Plot layout: 20 plots of 250 x 10 m each, with a mix of life forms (trees, lianas, palms) across five DBH size classes.
- Purpose for analysts: enables analysis of how prior human disturbance affects stem radial growth and how growth responds over time, potentially in relation to El Niño events and fire.

## Data collection design and methods

- Dendrometer setup:
  - At least 50 dendrometer bands per plot, distributed across five DBH classes and all lianas ≥10 cm DBH.
  - Bands installed 10 cm above DBH; a one-month settling period before marking the zero line; first measurement 5 months after marking; monthly measurements thereafter.
  - If bands were damaged, replacements were installed; dead stems had bands removed and reinstalled on another tree in the same size class.
- Growth measurement details:
  - Negative values (stem shrinkage) occur due to water loss and are not corrected, as some positive growth is due to water accumulation.
- Data values:
  - Growth reported in millimeters (mm) per month for each individual tree or liana.
- Plot disturbance assessment:
  - Disturbance status determined from satellite imagery (1988–2010) and field assessments of fire scars, charcoal, and logging debris.
- Location data:
  - Each plot has precise coordinates (latitude and longitude) provided for spatial analysis.

## Data structure and key fields

- Core identifiers:
  - Catchment, Transect, Plot (unique plot code combining bacia and transect)
  - Rainfor (ForestPlots database code)
  - Forest (pre-2015-16 El Niño disturbance class)
  - Fire_ElNino (whether the plot burned during the El Niño)
  - Tree_tag (individual dendrometer identifier)
  - Tree_code (unique code for each individual)
- Biological and measurement attributes:
  - DBH (diameter at breast height, 2014 measurement)
  - Life form (A = tree, C = liana, P = palm)
  - Re-installed (whether dendrometer was re-installed during the study)
- Temporal data (monthly series):
  - Data-Dec14, Data-Jan15, etc. (month-year of measurement date)
  - mm-Dec14, mm-Jan15, etc. (radial growth in mm for that month)
  - OBS-Dec14, OBS-Jan15, etc. (field notes for that month)
- Spatial scope:
  - A set of plot coordinates covering the study area, enabling spatial analyses of growth patterns relative to location.

## Data quality, caveats, and handling

- Data gaps and accessibility:
  - Data is organized monthly with field notes; some months may have missing observations due to field conditions or instrument issues.
- Measurement considerations:
  - Negative monthly growth values reflect trunk water loss and are not corrected; the dataset preserves natural variability in growth measurements.
- Scale and generalizability:
  - Focuses on 20 plots within a defined gradient of human modification in Eastern Amazonia, which may limit broad generalizations beyond similar forest types and disturbance histories.
- Data provenance and reproducibility:
  - Collected under a formal program (HMTF) with explicit disturbance classifications and monthly dendrometer measurements, enabling traceability and replication of analyses.

## Provenance and usage notes for analysts

- Data file: RadialGrowthOfStemsData.csv contains the monthly radial growth measurements and associated plot/individual metadata.
- Intended analyses:
  - Investigate correlations between disturbance class and radial growth trajectories.
  - Model growth as a function of DBH class, life form, and disturbance history.
  - Assess temporal responses to El Niño-related events and fire history at the plot level.
  - Integrate with spatial data using plot coordinates to explore geographic patterns of growth.
- Data preparation tips:
  - Align monthly mm values with corresponding Data and OBS fields; handle potential missing months via standard time-series imputation or exclusion depending on analysis.
  - Consider normalizing growth by DBH class or life form to compare across size classes.
  - Ensure traceability of data sources and field notes when reporting results.

## Summary of potential insights

- The dataset enables assessment of how prior human disturbance influences stem radial growth dynamics over multiple years.
- It supports exploration of how growth responds to climate-related events (El Niño) and fire history within a managed forest mosaic.
- With careful QA and transformation, the data can yield robust correlations and predictive models relating disturbance, growth, and temporal trends across forest types and size classes.