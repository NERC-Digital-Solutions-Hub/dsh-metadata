# Methods

## Overview
- Describes the Concentration Based Estimated Deposition (CBED) methodology for generating 5x5 km resolution gridded data of wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Data are derived from measured air concentrations of gases/particulate matter and ions in precipitation, collected within the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Outputs are intended to support assessment of critical load exceedances and inform environmental health monitoring.

## How CBED is calculated
- Site measurements are interpolated to create UK-wide concentration maps.
- For wet deposition, precipitation concentrations are combined with an annual precipitation map from the UK Met Office.
- Dry deposition is calculated by combining gas/PM concentration maps with habitat-specific deposition velocities across five land cover categories: forest, moorland, grassland, arable, and urban.
- Critical load exceedances distinguish moorland vs forest deposition; moorland values apply to non-woodland habitats and forest values to woodland habitats.

## Gas/particle and precursor data sources
- NOx concentrations (NO2/NO3) interpolated from ~30 sites.
- NO2 and SO2 concentrations from the PCM model, mixing rural measurements with point/line source modelling.
- NH3 concentrations from FRAME atmospheric transport model plus local UKEAP measurements (emissions year used: 2017).
- Wet deposition includes direct deposition of cloud droplets (occult deposition) and an orographic enhancement factor for uplands (seeded by elevation-related precipitation observations).

## Temporal aspects
- Inter-annual weather variability influences deposition estimates.
- CBED deposition values are averaged over a three-year period to smooth natural variability.
- Calculations are annual but presented as rolling 3-year means, with ecosystem-specific outputs and a grid-averaged set.

## Outputs and ecosystem-specific sets
- Three ecosystem-specific deposition datasets (moorland, forest/woodland, grid average) for each 5x5 km grid square.
- Grid average file contains fewer mapped squares due to the requirement that all nitrogen forms be present to compute the average.

## Data structure and format
- Files include:
  - CBED-deposition-moorland-2016-2018.csv (easting, northing, and moorland deposition for NOx, NHx, NMS, and Ca_mg)
  - CBED-deposition-forest-2016-2018.csv (forest deposition values for NOx, NHx, NMS, and Ca_mg)
  - CBED-deposition-gridaverage-2016-2018.csv (grid-average deposition for NOx, NHx, NMS, and Ca_mg)
- Columns include easting (metres), northing (metres), and deposition terms expressed as keq ha-1 year-1:
  - Moorland: nox_m, nhx_m, nms_m, ca_mg_m
  - Forest: nox_f, nhx_f, nms_f, ca_mg_f
  - Grid average: nox_ga, nhx_ga, nms_ga, ca_mg_ga
- Grid-average files have 10,678 rows vs 11,172 for forest/moorland due to completeness requirements.

## Units and conversions
- All deposition values are in keq ha-1 year-1.
- Conversions to kilograms per hectare per year (kg ha-1 year-1):
  - Sulphur deposition: keq ha-1 year-1 × 16 → kg S ha-1 year-1
  - Oxidised/reduced nitrogen deposition: keq ha-1 year-1 × 14 → kg N ha-1 year-1
  - Base cation deposition (Ca+Mg): keq ha-1 year-1 × 20 → kg Ca ha-1 year-1

## Quality control and governance
- CBED methods have undergone extensive peer review and participated in Defra model inter-comparison (e.g., Carslaw 2011).
- Procedures cover method documentation, version control, and central code storage.
- CBED results are widely published; method developments are overseen by senior responsible officers.
- Mass balance checks are routinely performed to ensure numerical consistency and checks against previous years.

## Data provenance and references
- Data sources for NOx, NO2, NO3, NH3, and wet/dry deposition are documented with supporting models and observations.
- Includes a set of key publications and project reports (e.g., Holme Moss measurements, Great Dun Fell observations, RoTAP, and related atmospheric modelling literature).

## Data access and metadata
- Data are linked to supporting information and networks:
  - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP)
  - UK Air Defra network information
- URLs provided for additional information and data access:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap

## Context for monitoring frameworks
- The CBED methodology exemplifies a structured approach to environmental health monitoring:
  - Clear data sources and interpolation methods
  - Habitat-specific deposition modelling and aggregation
  - Transparent temporal averaging to reduce inter-annual noise
  - Rigorous quality control and documentation
  - Open dissemination of data with defined units and conversion factors