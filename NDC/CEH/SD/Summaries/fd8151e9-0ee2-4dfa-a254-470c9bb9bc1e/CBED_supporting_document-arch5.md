# The Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Generates 5x5 km resolution gridded data for wet and dry deposition of sulfur, oxidised and reduced nitrogen, and base cations.
- Based on measured concentrations of gases, particulates in air, and ions in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Outputs deposition values across five land cover categories (forest, moorland, grassland, arable, urban) and provides grid-square averages; includes ecosystem-specific scenarios (moorland everywhere; forest everywhere).

## Methodology and data sources
- Site measurements are interpolated to UK concentration maps; precipitation map used to convert ion concentrations to wet deposition.
- Dry deposition combines gas/PM concentration maps with habitat-specific deposition velocities; applied to land cover categories to produce grid-square deposition.
- Wet deposition includes direct deposition of cloud droplets (occult deposition) and separates anthropogenic vs total components using sea-salt proxies; includes orographic enhancement for upland precipitation.
- Gas and particulate species included: SO2, HNO3, NO2, NH3, sulfate, nitrate, ammonium, calcium, magnesium.
- Critical load calculations apply deposition values for non-woodland vs woodland habitats.
- Ammonia and oxidised nitrogen pathways incorporate FRAME model and PCM data; NO2 interpolation from rural sites and point/line source modelling.
- Wet deposition accounts for occult deposition and uses an annual precipitation map; separation of sea-salt and non-sea-salt components via ion ratios.

## Temporal and spatial aspects
- Calculations are annual but published as rolling 3-year means to smooth inter-annual variability.
- Deposition data are provided as ecosystem-specific (moorland, forest/woodland) and as grid averages.
- Two ecosystem assumptions per grid square: moorland everywhere or forest everywhere.

## Data products (3-year means for 2013–2015)
- CBED-deposition-moorland-2013-2015.csv: easting, northing, and deposition components for moorland (nox_m, nhx_m, nms_m, nm_ca_mg_m).
- CBED-deposition-forest-2013-2015.csv: easting, northing, and deposition components for forest (nox_f, nhx_f, nms_f, nm_ca_mg_f).
- CBED-deposition-gridaverage-2013-2015.csv: easting, northing, and grid-average deposition components (nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga).

## Units and data conversion
- All deposition values are in kilo-equivalents per hectare per year (keq ha-1 year-1).
- Conversions to kilograms per hectare per year:
  - Sulfur (SO4, SO2): keq ha-1 year-1 × 16 → kg S ha-1 year-1
  - Oxidised/reduced nitrogen: keq ha-1 year-1 × 14 → kg N ha-1 year-1
  - Base cations (Ca+Mg): keq ha-1 year-1 × 20 → kg Ca ha-1 year-1

## Quality assurance and provenance
- CBED methodology adheres to government QA practices; extensive peer review and participation in Defra model inter-comparison (Carslaw 2011).
- Documented version control, method development approvals, and central code storage.
- Mass-balance checks performed to ensure numerical consistency and comparability with previous years.
- Results widely published in peer-reviewed literature.

## Data structure and metadata
- Data are provided as 3-year means with the following structure:
  - Moorland: CBED-deposition-moorland-2013-2015.csv
  - Forest: CBED-deposition-forest-2013-2015.csv
  - Grid-average: CBED-deposition-gridaverage-2013-2015.csv
- Each file includes:
  - easting and northing (centre of 5x5 km grid square in OS Great Britain grid; units: metres)
  - Deposition components per grid square (nox, nhx, nms, nm_ca) with ecosystem-specific suffixes or ga for grid-average
- Documentation also includes references and links to data portals:
  - http://wwwpollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap

## Limitations and considerations for data stewards
- Inter-annual variability in deposition due to weather; values are smoothed via 3-year means.
- Temporal resolution is annual; spatial resolution is fixed at 5x5 km grids with ecosystem-specific or grid-average outputs.
- Some components rely on modelling/remote-sensing inputs (e.g., FRAME, PCM) and sea-salt fraction assumptions; users should consider model-derived uncertainties in analyses.
- Updates and archival practices are in place to ensure traceability across model versions.