# Ozone flux POD1 IAM dataset for grasslands, UK and USA, 2018

## Overview
- A GIS-ready dataset describing daily POD1 IAM ozone flux values summed over the 90-day grassland growing season (mid-April to mid-July) for 2018 in the UK and USA.
- Generated from the EMEP-WRF global model (v4.45) driven by hourly meteorology, using DO3SE stomatal flux parameterisations and CLRTAP guidelines.
- Data are provided as a shapefile on a 1° × 1° grid, suitable for integration with other geospatial datasets and GIS analyses (e.g., impacts on crop yield, tree biomass, or flowering).

## Data collection and modeling context
- Based on EMEP-WRF (global model) with 1° × 1° horizontal resolution and 21 vertical layers; driven by WRF (v4.2.2) using GFS-FNL data for initialization and nudging.
- Emissions input from IIASA ECLIPSE v6a GAINS for 2015.
- Ozone flux (POD1 IAM) computed using the DO3SE model, with input data including hourly ozone concentration, temperature, vapor pressure deficit, irradiance, and soil moisture.
- POD1 IAM values are intended for semi-natural vegetation; ISO-specific parameterisations adapt for vegetation type and phenology.

## Time frame, scope, and spatial extent
- Temporal aggregation: POD1 IAM values accumulated daily and summed over the 90-day grassland growing season (mid-April to mid-July) for 2018.
- Spatial extent: Global model output aggregated to 1° × 1° grid cells, with a focus on the UK and USA in this dataset.
- Projection and coordinates: Geographic Coordinate System WGS84; outputs provided in decimal degrees.

## Data structure and GIS compatibility
- Shapefile structure: 1° × 1° gridded data with 5 attributes
  - FID: Unique grid cell identifier
  - Lon: Longitude of the grid cell center
  - Lat: Latitude of the grid cell center
  - NAME: Country (USA or UK)
  - POD1: Accumulated POD1 IAM for the grassland season, in mmol m^-2
- Units: POD1 IAM values in millimoles per square meter (mmol m^-2)
- Practical use: Suitable for spatial analyses linking ozone flux to crop/yield impacts, biomass, or phenology using CLRTAP response functions.

## Parameterisation and methodological notes
- POD1 IAM parameterisation follows CLRTAP Mapping Manual (2017) for semi-natural vegetation; Table 1 in the dataset documentation outlines the specific parameter values (vegetation-type specific, including factors like stomatal conductance, VPD thresholds, and seasonal windows).
- The recommended season window is selected per local conditions to maximize flux relevance.
- For smaller-scale, species-specific studies, POD1 IAM is complemented by POD1 SPEC or alternate IAM formulations as appropriate.

## Quality control and validation
- Model outputs undergo QA/QC prior to use; validation includes comparison with Global Atmosphere Watch (GAW) site measurements to assess spatial and temporal ozone variations.
- A key validation finding: strong correlation (r^2 ≈ 0.63) between AET/PET proxy and model-estimated POD3 IAM divided by the 7-hour mean ozone, indicating the model reasonably estimates stomatal ozone uptake.
- Visual validation referenced from Mills et al. (2018) and supplementary materials; model performance generally captures seasonal ozone patterns.

## Data usage and applications
- The ozone flux dataset can be used to:
  - Assess potential crop yield impacts and flowering reductions using CLRTAP-derived response functions.
  - Inform vegetation and crop models or integrated assessments that hinge on stomatal ozone uptake.
  - Support regional risk assessments for ozone-related stresses on semi-natural vegetation, particularly grasslands.
- Background resources and data provenance links:
  - EMEP/ICP Vegetation CLRTAP, and CLRTAP Mapping Manual (2017)
  - Mills et al. (2018) validation study
  - Emberson et al. (2000) stomatal flux modelling
  - Simpson et al. (2012) EMEP MSC-W model description
  - Vieno et al. (2016) EMEP-WRF context and emissions considerations

## References
- CLRTAP (2017) Mapping critical levels for vegetation. CLRTAP Mapping Manual.
- Emberson et al. (2000) Modelling stomatal ozone flux across Europe.
- Hayes et al. (2021) Ozone critical levels for (semi-) natural vegetation dominated by perennial grassland species.
- Mills et al. (2018) Ozone pollution will compromise efforts to increase global wheat production.
- Simpson et al. (2012) The EMEP MSC-W chemical transport model – technical description.
- Vieno et al. (2016) The sensitivities of emissions reductions for PM2.5 mitigation in the UK.