# Methods

## Overview
- CBED (Concentration Based Estimated Deposition) produces 5x5 km gridded deposition data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Data come from measurements in the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Outputs are ecosystem-specific and used to assess critical loads and environmental health over time.

## How the data are produced
- Site-based measurements are interpolated to create UK-wide concentration maps.
- Wet deposition is derived by combining ion concentrations in precipitation with an annual precipitation map from the UK Met Office.
- Dry deposition is computed by combining gas/PM concentration maps with habitat-specific deposition velocities for five land cover types: forest, moorland, grassland, arable, and urban.
- Deposition to land covers is weighted by the proportion of each land cover in a 5x5 km grid to produce grid-square averages.
- Dry deposition includes deposition of gases (SO2, HNO3, NO2, NH3) and particulate matter (sulfate, nitrate, ammonium, calcium, magnesium) to vegetation.
- Critical loads: deposition values for moorland are applied to all non-woodland habitats, while forest deposition is applied to woodland habitats.

## Specific components and data sources
- SO2 concentrations: derived from rural measurements with an urban enhancement factor.
- Oxidised nitrogen dry deposition: nitric acid concentrations interpolated from ~30 rural sites; NO2 concentrations from the PCM model (Stedman et al., 2007).
- Ammonia concentrations: from FRAME atmospheric transport model plus annual UKEAP measurements.
- Wet deposition: accounts for direct deposition of cloud droplets to vegetation (occult deposition); mapped for sulfate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion).
- Anthropogenic vs total deposition: separation using sea-salt ion ratios relative to sodium.
- Orographic enhancement: applied using an uplift factor from observations in upland regions (Great Dun Fell, Holme Moss).

## Temporal aspects
- Inter-annual variability due to weather, air circulation, temperature, and precipitation affects emissions, chemistry, and transport.
- CBED deposition data used to calculate critical loads are averaged over a three-year period to smooth variability.
- Deposition data are calculated annually but provided as rolling three-year means.

## Outputs and data structure
- Three ecosystem-specific 3-year mean datasets:
  - Moorland deposition (nox_m, nhx_m, nms_m, nm_ca_mg_m) with easting/northing.
  - Forest deposition (nox_f, nhx_f, nms_f, nm_ca_mg_f) with easting/northing.
  - Grid-average deposition (nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga) with easting/northing.
- Data are organized per 2015-2017 in CSV files:
  - CBED-deposition-moorland-2015-2017.csv
  - CBED-deposition-forest-2015-2017.csv
  - CBED-deposition-gridaverage-2015-2017.csv
- Each row includes grid center coordinates (easting, northing) and deposition values for the relevant species/compounds in keq ha-1 year-1.

## Units and conversions
- All deposition values are in keq ha-1 year-1.
- Conversions to kilograms per hectare per year:
  - Sulphur deposition: keq × 16 = kg S ha-1 year-1
  - Oxidised/reduced nitrogen deposition: keq × 14 = kg N ha-1 year-1
  - Base cations (Ca+Mg) deposition: keq × 20 = kg Ca ha-1 year-1

## Quality control and governance
- CBED methods follow QA procedures aligned with the Review of QA of Government analytical models.
- Extensive peer review and participation in Defra model inter-comparison (e.g., Carslaw 2011).
- Documentation of method developments, version control, and central storage of code.
- Results widely published in peer-reviewed literature.
- Method developments approved by a group of senior responsible officers.
- Mass balance checks performed to ensure numerical consistency and comparability with previous years.

## Data structure details
- 3-year mean, ecosystem-specific deposition data with three modes:
  - Moorland: deposition to moorland.
  - Forest/woody: deposition to forest.
  - Grid average: deposition across the entire grid square.
- Each CSV file includes:
  - Easting (metres) and Northing (metres) for the grid cell center.
  - Deposition fields for the relevant ecosystem category (e.g., nox_m, nhx_m, nms_m, nm_ca_mg_m for moorland).
- Example fields per dataset:
  - Moorland: nox_m, nhx_m, nms_m, nm_ca_mg_m
  - Forest: nox_f, nhx_f, nms_f, nm_ca_mg_f
  - Grid average: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga

## Relevance to environmental monitoring
- Provides standardized, grid-based deposition estimates suitable for trend analysis, policy evaluation, and informing critical load assessments.
- Facilitates data sharing and broader access by structuring outputs in consistent, machine-readable formats aligned with monitoring responsibilities.