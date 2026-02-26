# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Produces 5x5 km gridded data of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Derived from measured concentrations of gases/particulate matter in air and ions in precipitation, collected via the UK Eutrophying and Acidifying Pollutants (UKEAP) network.

## How the data are produced
- Site measurements are interpolated to create UK concentration maps.
- Wet deposition: combine ion concentrations in precipitation with an annual precipitation map (UK Met Office).
- Dry deposition: combine gas/PM concentration maps with habitat-specific deposition velocities to generate deposition for five land cover categories (forest, moorland, grassland, arable, urban).
- Deposition to grid squares is weighted by the proportions of land cover types within each 5x5 km square.
- For critical load exceedance, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.

## Species and data sources
- Nitric oxide/nitrogen species: NOx concentrations interpolated from ~30 sites; NO2 and SO2 from the PCM model (Stedman et al., 2007).
- Ammonia: from FRAME model plus annual UKEAP measurements; FRAME provides local-scale variability; 2017 FRAME emissions used.
- Wet deposition components include direct cloud droplet deposition (occult deposition) and an orographic enhancement factor for upland regions (based on Dun Fell and Holme Moss observations).

## Temporal and ecosystem outputs
- Inter-annual variability smoothed by three-year averaging; deposition values are provided as rolling 3-year means.
- Outputs are ecosystem-specific (two sets): moorland everywhere and forest everywhere; plus grid-average values.
- The 3-year mean data are presented for 2016–2018.

## Data structure and files
- 3-year mean deposition data for 2016–2018 in 5x5 km grid squares:
  - CBED-deposition-moorland-2016-2018.csv
    - Columns: easting, northing (metres); nox_m, nhx_m, nms_m, ca_mg_m
  - CBED-deposition-forest-2016-2018.csv
    - Columns: easting, northing (metres); nox_f, nhx_f, nms_f, ca_mg_f
  - CBED-deposition-gridaverage-2016-2018.csv
    - Columns: easting, northing (metres); nox_ga, nhx_ga, nms_ga, ca_mg_ga
- Coordinates refer to the centre of each 5x5 km OS Great Britain grid square.
- Grid-average file has fewer rows (10678) than forest/moorland (11172) because the grid-average requires all nitrogen forms to be present.

## Units and data conversions
- All deposition values are in keq ha-1 year-1.
- Conversions:
  - To kg S ha-1 year-1: multiply by 16 (for sulphur deposition).
  - To kg N ha-1 year-1: multiply by 14 (for oxidised/reduced nitrogen deposition).
  - Base cations (Ca+Mg) deposition: keq ha-1 year-1 multiplied by 20 to obtain kg Ca ha-1 year-1.

## Quality control
- Methods aligned with Government analytical model QA guidance; extensive peer review and participation in Defra model inter-comparison (Carslaw, 2011).
- Version control, central storage of code, and comprehensive documentation.
- Mass-balance checks comparing current and previous years to ensure numerical consistency.

## GIS considerations and usage
- Outputs provide map-ready 5x5 km deposition surfaces suitable for spatial analyses and policy exercises.
- Coordinates in the GB grid facilitate integration with other GB GIS layers; habitat-specific deposition informs habitat-targeted assessments.
- Grid-average limitations: missing values in any nitrogen form prevent grid-average calculation for those squares.