# Methods

## Overview
- Describes the Concentration Based Estimated Deposition (CBED) methodology for generating 5x5 km gridded deposition data in the UK.
- Outputs wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations from gas/PM concentrations and precipitation measurements (UKEAP network) and habitat-specific deposition velocities.
- Data are provided as rolling 3-year means to smooth inter-annual variability; includes ecosystem-specific scenarios (moorland vs forest) and a grid-average dataset.

## Data resolution and coverage
- Gridded data at 5x5 km resolution across the UK (OS Great Britain grid centers in each square).
- Annual deposition values averaged over rolling 3-year periods; ecosystem-specific (moorland or forest/woodland) plus grid-average datasets.

## Deposition components and calculations
- Wet deposition:
  - Derived from precipitation data and direct cloud (occult) deposition to vegetation.
  - Includes sulphate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion).
  - Anthropogenic and total components separated for sulphur and calcium using sea-salt ion ratios.
  - Orographic enhancement factor adjusts precipitation concentration in upland regions (seeder-feeder effect).
- Dry deposition:
  - Based on gas and PM concentration maps plus habitat-specific deposition velocities.
  - Five land cover categories: forest, moorland, grassland, arable, urban.
  - Deposition values are combined across land-cover proportions within each 5x5 km grid cell.
  - For critical load calculations, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.

## Data content and structure
- Three 2015–2017 CSV data files:
  - CBED-deposition-moorland-2015-2017.csv
    - Columns: easting, northing (metres); nox_m (oxidised nitrogen to moorland); nhx_m (reduced nitrogen to moorland); nms_m (non-marine sulphur to moorland); nm_ca_mg_m (non-marine base cations to moorland).
  - CBED-deposition-forest-2015-2017.csv
    - Columns: easting, northing (metres); nox_f (oxidised nitrogen to forest); nhx_f (reduced nitrogen to forest); nms_f (non-marine sulphur to forest); nm_ca_mg_f (non-marine base cations to forest).
  - CBED-deposition-gridaverage-2015-2017.csv
    - Columns: easting, northing (metres); nox_ga (oxidised nitrogen grid average); nhx_ga (reduced nitrogen grid average); nms_ga (non-marine sulphur grid average); nm_ca_mg_ga (non-marine base cations grid average).
- All deposition values are expressed as keq ha^-1 year^-1.
- Coordinates represent the centre of each 5x5 km grid square.

## Units and conversions
- keq ha^-1 year^-1 for all deposition values.
- Conversions to kg units:
  - Sulphur deposition: keq ha^-1 year^-1 × 16 = kg S ha^-1 year^-1
  - Oxidised/reduced nitrogen deposition: keq ha^-1 year^-1 × 14 = kg N ha^-1 year^-1
  - Base cations (Ca+Mg): keq ha^-1 year^-1 × 20 = kg Ca ha^-1 year^-1

## Quality control and provenance
- Methods align with QA procedures from Government analytical models; extensive peer review and participation in Defra model inter-comparison (Carslaw 2011).
- Documented versioning, central storage of code, and mass balance checks against previous years.
- Data and methodologies published in peer-reviewed literature; responsible officers oversee method developments.

## Access, references, and related information
- Data and supporting information cited via:
  - UK Monitoring and Assessment of Pollutants (CEH) pollutant deposition pages
  - UK-AIR Defra network information pages
  - References including Carrslaw et al. and related modelling studies on ammonia, deposition, and atmospheric transport
- Fieldwork and calibration: not applicable (N/A) for this dataset.

## Practical GIS considerations
- Suitable for integration into GIS workflows as 5x5 km grid layers with precise easting/northing coordinates.
- Use moorland vs forest datasets to assess habitat-specific deposition; combine with land-cover maps to compute grid-level totals.
- Ideal for assessing spatial patterns, identifying hotspots, and supporting critical load exceedance analyses with standardized 3-year mean values.