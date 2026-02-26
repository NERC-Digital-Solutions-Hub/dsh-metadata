# Methods

## Overview
- Concentration Based Estimated Deposition (CBED) generates 5x5 km resolution gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Data are derived from measured concentrations (gas, PM) in air and ions in precipitation collected by the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Outputs include ecosystem-specific deposition maps for UK, with separate treatment for moorland and forest, and grid-average deposition.

## How CBED Works (Data Generation)
- Site measurements are interpolated to create UK-wide concentration maps.
- Wet deposition:
  - From precipitation plus direct deposition of cloud droplets (occult deposition).
  - Anthropogenic vs total components separated using sea-salt ratios.
  - Orographic enhancement factor applied for upland precipitation concentration.
- Dry deposition:
  - Gas and PM deposition estimated using concentration maps and deposition velocities, across five land cover categories: forest, moorland, grassland, arable, urban.
  - Grid-square deposition combined according to local land cover proportions.
  - Critical load calculations apply moorland deposition to non-woodland habitats and forest deposition to woodland habitats.
- Gas/deposition components:
  - SO2, HNO3, NO2 for oxidised nitrogen; NH3/NH4 for reduced nitrogen.
  - Ammonia concentrations blend FRAME model results with UKEAP observations.
- Temporal considerations:
  - Inter-annual variability exists due to weather; CBED values for deposition are averaged over a 3-year period.
  - Data are produced as rolling 3-year means and are annual in calculation.

## Data Products and Structure
- Ecosystem-specific data (3-year means):
  - Moorland (m) deposition: nox_m, nhx_m, nms_m, nm_ca_mg_m.
  - Forest/woodland (f) deposition: nox_f, nhx_f, nms_f, nm_ca_mg_f.
- Grid-average data (ga) for each component: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga.
- Units:
  - All deposition values in keq ha^-1 year^-1.
  - Convert to kg N ha^-1 year^-1 or kg S ha^-1 year^-1 using provided factors when needed.
- Data files (example structure for 2013–2015):
  - CBED-deposition-moorland-2013-2015.csv
  - CBED-deposition-forest-2013-2015.csv
  - CBED-deposition-gridaverage-2013-2015.csv
- Common fields in all files:
  - easting, northing (centre of 5x5 km grid square, OS GB grid, in metres).
  - deposition values for each component (e.g., nox_m, nhx_m, nms_m, nm_ca_mg_m for moorland; corresponding f or ga suffix for other categories).

## Data Provenance and Method Details
- Data sources:
  - Gas concentrations, precipitation, and site measurements from UKEAP network.
  - Precipitation maps from the UK Meteorological Office.
- Modelling choices:
  - Oxidised nitrogen dry deposition from interpolated nitric acid measurements and NO2 concentrations from PCM model.
  - Ammonia concentrations from FRAME model plus UKEAP data.
  - Wet deposition separated into anthropogenic vs sea-salt components using sodium ratios.
  - Occult deposition accounted for in wet deposition mapping.
- Deposition to habitats:
  - Moorland vs forest deposition values applied to respective non-woodland/woodland habitats in the calculation of grid-square totals.

## Quality Control and Data Governance
- Quality assurance:
  - CBED methodology has undergone extensive peer review and participated in Defra model inter-comparison exercises.
  - Version control, documented method developments, and central storage of code.
  - Mass balance checks to ensure numerical consistency; comparisons with previous years.
- Documentation and reproducibility:
  - Method developments reviewed by senior responsible officers.
  - Results published in peer-reviewed literature.

## Access, Documentation, and Metadata
- Data are accompanied by supporting information and documentation (online resources provided in the dataset description).
- Data structure documentation includes detailed field names, units, and descriptions for each of the 3 CSV files (moorland, forest, grid average) across 2013–2015.

## Practical Considerations for Data Leaders
- System-level view: CBED provides end-to-end deposition estimates by ecosystem type and grid, enabling assessment of data coverage and gaps across the UK.
- Data availability and usability:
  - Data are standardized to keq ha^-1 year^-1 with clear conversion factors to kg units.
  - Rolling 3-year means help smooth inter-annual variability but limit detection of short-term trends.
- Governance and reusability:
  - Strong provenance, versioning, and QA support reliable reuse across analyses and policy contexts.
- Considerations for broader data strategy:
  - Interoperability with other deposition and atmospheric datasets (e.g., coatings for metadata and formats).
  - Clear metadata and documentation to support cross-team collaboration and co-ownership of data products.