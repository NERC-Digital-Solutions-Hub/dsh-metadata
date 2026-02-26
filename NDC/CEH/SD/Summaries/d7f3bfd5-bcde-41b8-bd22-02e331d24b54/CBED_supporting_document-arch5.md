# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Generates 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Data come from the UK Eutrophying and Acidifying Pollutants (UKEAP) network and are interpolated to UK-wide maps.
- Wet deposition combines ion concentrations in precipitation with a UK precipitation map; includes occult (cloud) deposition.
- Dry deposition uses gas/PM concentration maps with habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
- Deposition in each grid square is weighted by the proportions of land-cover types in that square.
- For critical load exceedance, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.
- Separation of anthropogenic vs total deposition is performed for sulphur and calcium using sea-salt fraction methods.
- Orographic enhancement factors account for upland precipitation variations (e.g., Great Dun Fell, Holme Moss).
- Inter-annual variability exists due to weather; CBED values are averaged over a three-year period.
- Outputs are annual but provided as rolling 3-year means; ecosystem-specific outputs exist in two forms and grid-average values are also provided.

## Data sources and processing
- Gas and PM concentration maps used to estimate dry deposition; ion concentrations in precipitation used to estimate wet deposition.
- Sulphur concentration map derived from rural SO2 measurements with an urban enhancement factor.
- Oxidised nitrogen deposition (NOx and related species) derived via interpolation plus PCM model data.
- Ammonia concentrations from FRAME model and UKEAP measurements to capture local variability.
- Wet deposition includes direct cloud-deposition to vegetation (occult deposition) and uses ion-ratio methods to separate non-marine vs total components.
- Orographic enhancement factors are based on observed altitude effects on precipitation.
- Inter-annual variability acknowledged; 3-year mean used to smooth natural variability.

## Data structure and fields
- Data provided as 3-year mean deposition values on the UK 5x5 km grid, with ecosystem-specific and grid-average options.
- Fields (examples for forest, moorland, and grid-average):
  - easting: centre of 5x5 km grid (metres)
  - northing: centre of 5x5 km grid (metres)
  - nox_f: oxidised nitrogen deposition to forest (keq ha-1 year-1)
  - nhx_f: reduced nitrogen deposition to forest (keq ha-1 year-1)
  - nms_f: non-marine sulphur deposition to forest (keq ha-1 year-1)
  - nm_ca_mg_f: non-marine base cations deposition to forest (keq ha-1 year-1)
  - nox_m, nhx_m, nms_m, nm_ca_mg_m: analogous values for moorland
  - nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga: analogous values for grid average
- Units: keq ha-1 year-1
- Outputs cover both ecosystem-specific (moorland and forest) and grid-average scenarios.

## Quality control and governance
- Methods align with government QA standards for analytical models; subjected to extensive peer review and participation in Defra model inter-comparison exercises.
- Version-controlled documentation and storage in a central file system.
- Results have been published in peer-reviewed literature; method developments approved by senior officers.
- Mass-balance checks and cross-year comparisons ensure numerical consistency and consistency with previous years.

## Data access and practical considerations for Data Stewards
- Primary sources:
  - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) information: http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - UK-AIR Defra network information: https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
- Data are expressed in keq ha-1 year-1 and can be converted to kilograms per hectare per year using provided multipliers (e.g., for oxidised/reduced nitrogen and sulphur; base cations have separate conversion).
- Suitable for ingestion into large-scale environmental data holdings with consistent 5x5 km gridding; metadata should capture:
  - grid reference and projection
  - ecosystem-specific vs grid-average context
  - rolling 3-year mean basis and time window
  - land-cover assumptions used for deposition weighting
  - any model components (FRAME, PCM) and their role in the inputs
- caveats on use:
  - inter-annual variability remains, though smoothed by 3-year means
  - deposition values differ by habitat assumptions (moorland vs forest) and may require alignment with local land-cover maps
  - dependent on external models and datasets (e.g., FRAME, PCM) whose uncertainties should be considered

## Summary of relevance to data governance
- Provides a well-documented, QA-anchored deposition dataset with clearly defined units, grid structure, and habitat-specific decomposition.
- Facilitates interoperability through explicit data structures and conversion guidance.
- Highlights the need for clear metadata around time averaging, habitat assumptions, and processing steps to ensure discoverability and reusability by data users.