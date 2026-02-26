# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016 L. A. Ashton , H. M. Griffiths, C. L. Parr, T. A. Evans and P. Eggleton

## Overview
- Large-scale, field-based study in lowland, old-growth dipterocarp rainforest in Sabah, Malaysia (Maliau Basin Conservation Area).
- Timeframe: 2014–2017, with core data collection during 2015–2016, including drought and non-drought periods.
- Experimental design: eight 50×50 m plots within a 42-ha area; four termite-suppressed plots (80×80 m treated area with 15 m buffers) and four control plots, separated by at least 100 m.
- Objective: assess the role of termites in ecosystem processes and their interaction with drought, using a combination of termite suppression, decomposition assays, soil/leaf litter measurements, invertebrate surveys, seedling survival, and rainfall/climate indices.

## Datasets included
Twelve CSV data files are provided, covering:
- Termite encounter data (termite_hits_on_T_and_C_plots.csv)
- Leaf litter depth measurements (Leaf_litter_depth.csv)
- Leaf litter invertebrate abundances (Leaf_litter_invertebrates.csv)
- Leaf litter mass loss in decomposition bags (Litter_mass_loss.csv)
- Non-target invertebrates across years (Non_target_invertebrates_all_years.csv)
- Seedling survival under nondrought and drought conditions (Seedling_survival_nondrought.csv; Seedling_survival_drought.csv)
- Soil moisture measurements (Soil_moisture.csv)
- Soil nutrient measurements via resin probes (Soil_nutrients.csv)
- Termite cumulative attack scores (Termite_cumulative_attack.csv)
- Termite hits on control plots with rainfall index (Termite_hits_on_C_plots_SPI.csv)
- Plot location data (Locations_of_plots.csv)

## Experimental design and sampling regime
- Study area coordinates and environmental context described; eight plots established in Oct 2014 within a 42-ha area.
- Plot layout: four termite-suppressed plots and four controls; core sampling occurs within central 50×50 m sections to avoid edge effects.
- Termite suppression method: removal of mounds followed by soil treatment with imidacloprid; TPRs and tea bags with fipronil used for ongoing suppression, deployed in a staggered, integrated pest management approach.
- Sampling periods and methods include transect-based termite sampling, leaf litter depth and decomposition assays, Winkler extraction for invertebrates, seedling transplant experiments, soil moisture and nutrient probes, and rainfall-derived climate indices.

## Data collection methods (highlights)
- Termite abundance and community composition: transect sampling in June 2015 and Oct 2016 using Jones and Eggleton protocol.
- Leaf litter depth: in situ measurements across multiple transects during drought (Mar 2016) and non-drought (Oct 2016) periods.
- Leaf litter invertebrates: 15 one-square-meter samples per plot collected in 2016, extracted and identified to order.
- Decomposition: 112-day litter bag experiments (drought and non-drought) with macroinvertebrate exclusion vs access treatments.
- Non-target invertebrates: 1 m² leaf litter samples across 2014–2016, with Winkler extraction and taxonomic grouping.
- Seedling survival: transplant experiments from Agelaea borneensis with survival tracked through drought and non-drought periods.
- Soil measurements: soil moisture at 25 grid points per plot (March and Oct 2016); plant-available nutrients measured with PRS resin probes (two-week and full-grid deployments in drought and non-drought periods).
- Termite feeding activity: untreated termite paper rolls (TPRs) scored for consumption on a 0–5 scale; monthly re-sampling to generate cumulative attack metrics.
- Rainfall context: control plots’ termite activity linked to rainfall via SPI (Standardised Precipitation Index) calculated from Danum Valley rainfall data.
- Plot geolocation: GPS coordinates for plot corners to enable spatial mapping and GIS analyses.

## Geospatial context and mapping potential
- Location data provided for each plot, including corner coordinates and elevation, enabling precise spatial mapping of termite suppression effects.
- Data structure supports joins with climate indices (SPI) and soil/leaf litter variables to produce map-based visuals of spatial and temporal patterns.
- Suitable for GIS workflows to explore edge effects, spatial autocorrelation, and relationships between termite activity, soil resources, and ecosystem processes.

## Data structure and key fields
- Twelve CSVs with detailed column definitions per dataset (e.g., Plot, Treatment, date, and variable-specific fields such as genus of termites, depth_cm, abundance groups, mass_loss, Alive_2016/Alive_2017, soil_moisture, SPI, etc.).
- Each dataset is designed for integration in GIS and statistical environments, enabling cross-dataset analyses by plot, treatment, date, and environmental condition (drought vs non-drought).

## Potential GIS analyses and applications
- Spatial comparison of termite suppression effects across the four plots over time.
- Correlation of termite activity with drought intensity (SPI) and rainfall patterns.
- Integration of soil moisture and nutrient data with biological responses (seedling survival, decomposition rates, invertebrate communities).
- Mapping of leaf litter depth, decomposition rates, and non-target invertebrate distributions to understand ecosystem processes under termite suppression.
- Visualization of sampling transects, plots, and plot-level attributes (e.g., proximity to buffers, edge effects).

## Quality notes and context
- Multi-year, multi-dataset design with parallel control and treatment plots, enabling robust comparisons.
- Data collection methods span termites, soil, litter, and plant responses, providing a holistic view of termite roles in ecosystem processes.
- Data are tied to established references for termite sampling and drought indices.

## References
- Jones, D.T. and Eggleton, P. (2000). Sampling termite assemblages in tropical forests: testing a rapid biodiversity assessment protocol. J Appl Ecol 37(1), 191-203.
- Vicente-Serrano, S.M. et al. (2010). A multiscalar drought index sensitive to global warming: the standardized precipitation evapotranspiration index. J Clim 23(7), 1696-1718.