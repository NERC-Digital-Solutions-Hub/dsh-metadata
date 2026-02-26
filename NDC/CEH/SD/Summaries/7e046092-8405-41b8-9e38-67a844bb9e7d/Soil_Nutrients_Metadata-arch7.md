# Dataset Description (Soil_Nutrients)

## Overview
- Describes soil nutrient availability across three land-use types (unlogged tropical forest, logged tropical forest, and oil palm plantation) in Sabah, Malaysia.
- Data collected March–April 2016 as part of the NERC-funded BALI project.
- Primary data file: Soil_Nutrients.csv with 21 measured variables plus identifiers and descriptors.
- Results represent supply rates of nutrients per 10 cm2 over a 14-day burial period using ion exchange membranes.

## Sampling Design and Spatial Coverage
- 9 1-hectare plots across 3 sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified sampling: each 1 Ha plot subdivided into 25 subplots (20 m x 20 m); 3 subplots sampled per plot.
- Within each subplot: 3 sampling locations, with four PRS ion exchange membrane probe pairs buried to ~10 cm depth.
- Probes left in situ for 2 weeks, pooled per location, eluted, and analyzed.

## Data Content and Structure
- Soil_Nutrients.csv contains 21 numeric/text columns plus an Identifier and descriptive fields.
- Columns include:
  - Identifier, Site, Land_Use, Plot_Name, Subplot
  - Nutrient concentrations: NO3_N, NH4_N, Total_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd
  - Each concentration reported as µg/10cm2/14 days (per 10 cm2 membrane area).
- Total_N is the sum of NO3_N and NH4_N.
- Data are compiled from pooled ion exchange membranes across four probe pairs per location.

## Measurements, Units, and Detection Limits
- Measurements: concentration or supply rate per 10 cm2 per 14 days.
- Units: micrograms per 10 cm2 per 14 days (µg/10cm2/14 days).
- MDL (Method Detection Limits) provided per element; zeros indicate non-detectable values.
  - Examples: NO3_N MDL = 2; NH4_N MDL = 2; Ca MDL = 2; K MDL = 4; P MDL = 0.2, etc.

## Metadata
- Key fields: Identifier (unique sample identifier), Site (geographic area), Land_Use (forest type vs. oil palm), Plot_Name (1 Ha plot), Subplot (0–24 within plot).
- Descriptions and units provided for each metadata field to support data understanding and GIS integration.

## Data Quality and Considerations
- Data are reported as measured values even if below MDL (zeros indicate non-detectable).
- Acknowledges potential data challenges common in GIS-focused datasets:
  - Data scattered across multiple locations and formats.
  - Need for data cleaning and harmonization when integrating with other layers.
  - Potential gaps or resolutions mismatches across datasets.

## Geographic and Temporal Coverage
- Temporal: Sampling conducted in March–April 2016.
- Geographic scope: Sabah, Malaysia, encompassing three sites and three land-use categories (unlogged forest, logged forest, oil palm plantation).

## Applications for GIS and Data Use
- Map-based visualization of soil nutrient supply rates across land-use types and sites.
- Comparisons of nutrient availability between unlogged forest, logging-disturbed forests, and oil palm plantations.
- Integration with other spatial datasets (soil, vegetation, topography) for landscape-level nutrient cycling analyses.
- Support for policy, conservation planning, and land management decisions by illustrating spatial patterns in nutrient availability.

## References
- Qian, P. & J. J. Schoenau (2002) on ion exchange resins in soil research.
- Riutta et al. (2018) on logging disturbance effects in tropical forests.
- Source for data collection tools: www.westernag.ca (PRS ion exchange membranes).