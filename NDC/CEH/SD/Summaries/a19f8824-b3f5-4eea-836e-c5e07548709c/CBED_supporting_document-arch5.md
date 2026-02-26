# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Generates 5x5 km resolution gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Uses measured concentrations of gases/particulate matter in air and ions in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Produces wet deposition (from precipitation and occult deposition) and dry deposition (gas and PM to vegetation) across five land cover categories.
- Provides annual values as rolling 3-year means; outputs include ecosystem-specific (moorland; forest/woodland) and grid-average deposition for each grid square.

## Methodology
- Site measurements are interpolated to create UK concentration maps; precipitation maps are used to derive wet deposition.
- Dry deposition combines gas and PM concentration maps with habitat-specific deposition velocities; applied to land cover categories: forest, moorland, grassland, arable, urban.
- For critical load exceedance, deposition values are assigned regionally (moorland to non-woodland habitats; forest to woodland habitats).
- SO2 concentration uses rural measurements with an urban enhancement factor; oxidised nitrogen dry deposition interpolates rural measurements with point/line-source modelling (NO2 from PCM model); ammonia uses FRAME model plus annual network measurements.
- Wet deposition accounts for direct cloud deposition (occult deposition) and separates anthropogenic vs total components via sea-salt ion ratios; includes orographic enhancement in upland regions (seeder-feeder effect).

## Temporal and spatial specifics
- Deposition values are calculated annually but provided as rolling 3-year means to smooth inter-annual variability.
- Outputs are ecosystem-specific (moorland vs forest/woodland) and also provided as grid-average values for each 5x5 km grid square.

## Data products and structure
- Files (2015–2017):
  - CBED-deposition-moorland-2015-2017.csv
    - Fields include easting, northing (metres); deposition for oxidised nitrogen (nox_m), reduced nitrogen (nhx_m), non-marine sulphur (nms_m), non-marine base cations (nm_ca_mg_m).
  - CBED-deposition-forest-2015-2017.csv
    - Fields include easting, northing (metres); deposition for oxidised nitrogen (nox_f), reduced nitrogen (nhx_f), non-marine sulphur (nms_f), non-marine base cations (nm_ca_mg_f).
  - CBED-deposition-gridaverage-2015-2017.csv
    - Fields include easting, northing (metres); grid-average deposition for oxidised nitrogen (nox_ga), reduced nitrogen (nhx_ga), non-marine sulphur (nms_ga), non-marine base cations (nm_ca_mg_ga).
- Each deposition value is expressed as keq ha^-1 y^-1; conversion to kg S ha^-1 y^-1 or kg N ha^-1 y^-1 is provided (multipliers: S = 16; N = 14; Ca+Mg = 20).

## Units and conversions
- Deposition values: keq ha^-1 year^-1.
- Conversions:
  - Sulphur deposition to kg S ha^-1 y^-1: keq ha^-1 y^-1 × 16
  - Oxidised/reduced nitrogen deposition to kg N ha^-1 y^-1: keq ha^-1 y^-1 × 14
  - Base cation deposition to kg Ca ha^-1 y^-1: keq ha^-1 y^-1 × 20

## Quality control and governance
- Methods aligned with quality assurance practices for government analytical models; extensive peer review and participation in Defra model inter-comparison (Carslaw 2011).
- Documented method developments, versioning, and central code storage; results widely published in peer-reviewed literature.
- Mass balance checks performed to ensure numerical consistency and comparability with previous years.

## Data provenance and access
- Data derive from UK EAU/EPA network measurements (UKEAP) and supporting modelling components (PCM, FRAME).
- Supporting information and network details available via the following:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap

## Data Stewardship implications
- Provenance: clearly traceable from UKEAP measurements and modelling components; ensure proper citation of sources.
- Metadata and standards: consistent naming, units, and field definitions; maintain comprehensive metadata for future reuse.
- Versioning and updates: rolling 3-year means imply updates; track dataset versions and maintain documentation of changes.
- Storage and interoperability: multiple CSV files per dataset; ensure centralized, accessible repository and compatibility with other UK air pollution datasets.
- Access and licensing: confirm and communicate data licensing; provide stable access points (URLs) and, where possible, programmatic access.