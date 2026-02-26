# Methods

## Overview
- Describes the Concentration Based Estimated Deposition (CBED) method to generate 5x5 km resolution gridded deposition data for wet and dry deposition of sulfur, oxidised and reduced nitrogen, and base cations.
- Data come from measured concentrations in the UK Eutrophying and Acidifying Pollutants (UKEAP) network and precipitation ion concentrations.
- Outputs include both wet and dry deposition estimates, mapped and aggregated to land-cover categories.

## How deposition is estimated
- Site measurements are interpolated to create UK concentration maps.
- Wet deposition: combine precipitation concentration maps with an annual precipitation map; include occult (cloud) deposition to vegetation; separate anthropogenic from total components for sulfur and calcium using sea-salt ratios; apply an orographic enhancement factor for upland precipitation.
- Dry deposition: combine gas/particle concentration maps with deposition velocities, distributed by habitat type (five land-cover categories: forest, moorland, grassland, arable, urban).
- Critical loads: apply moorland deposition to non-woodland habitats and forest deposition to woodland habitats.

## Land-cover and grid aggregation
- Deposition to five land-cover categories is weighted by the relative proportions within each 5x5 km grid square.
- For ecosystem-specific assessments, provide two sets of values: moorland everywhere and forest everywhere; plus a grid-average.

## Temporal aspect
- Deposition values can vary yearly due to weather and emissions.
- Calculations are averaged over a three-year period to smooth inter-annual variability; CBED data are produced as rolling 3-year means.
- Data are calculated annually but provided as rolling 3-year means.

## Inputs and data sources
- Sulfur dioxide (SO2) concentrations: from rural measurements with an urban enhancement factor.
- Oxidised nitrogen (NOx, NO2/NO3) deposition: interpolation of measurements from ~30 sites plus PCM model data (points/lines sources).
- Ammonia (NH3/NH4): from FRAME atmospheric model plus annual measurements from UKEAP (captures local variability).
- Wet deposition components: sulphate, ammonium, nitrate, calcium, magnesium, acidity (H+).

## Outputs and file structure
- Three main 2014–2016 CSV files:
  - CBED-deposition-moorland-2014-2016.csv
  - CBED-deposition-forest-2014-2016.csv
  - CBED-deposition-gridaverage-2014-2016.csv
- Common fields include:
  - easting, northing (centre of 5x5 km grid square in OS Great Britain grid)
  - deposition components in keq ha-1 year-1 (nox_m, nhx_m, nms_m, nm_ca_mg_m for moorland; nox_f, nhx_f, nms_f, nm_ca_mg_f for forest; nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga for grid average)
- Units: all deposition values are keq ha-1 year-1; conversion factors to kg per ha per year are provided (S, N, Ca equivalents).

## Data quality, provenance, and governance
- Methods aligned with QA procedures for government analytical models; peer reviewed; part of Defra model inter-comparison exercises.
- Documented version control, mass-balance checks, and comparison to previous years.
- Data are published in peer-reviewed literature; method developments are approved by senior responsible officers.

## Data accessibility and references
- Resource locators:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
- Supporting information and field/lab details available via the above links.
- Key references cited for model components and validation (e.g., Stedman et al. 2007; Singles et al. 1998; Dore et al. 2007; Fowler et al. 1988; RoTAP 2012).