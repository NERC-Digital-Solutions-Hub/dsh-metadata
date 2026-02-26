# UK Acidifying and Eutrophying Atmospheric Pollutants

## Overview
- Describes the Concentration Based Estimated Deposition (CBED) methodology for generating 5x5 km gridded deposition data of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations.
- Data are derived from the UK Eutrophying and Acidifying Pollutants (UKEAP) network and integrated with additional models and measurements to produce ecosystem-specific deposition estimates.
- Outputs are used to assess critical loads and support policy decisions; data are provided as rolling 3-year means to smooth inter-annual variability.
- Includes both ecosystem-specific scenarios (moorland vs forest) and a grid-average deposition dataset.

## Methodology (CBED)
- Interpolates site-based measurements to create UK-wide concentration maps; combines with precipitation data to derive wet deposition.
- Dry deposition is generated from gas and PM concentration maps combined with habitat-specific deposition velocities across five land cover categories (forest, moorland, grassland, arable, urban).
- Critical load calculations apply deposition values to appropriate habitats (moorland to non-woodland; forest to woodland).
- Gas concentrations and deposition components are sourced from a mix of rural measurements, interpolation, and models (e.g., PCM model for NO2; FRAME for ammonia).
- Wet deposition accounts for direct cloud deposition (occult deposition) and uses sea-salt ratios to separate anthropogenic from total components; includes an orographic enhancement factor for upland regions.
- Inter-annual variability is acknowledged; CBED deposition values used for exceedance calculations are averaged over a three-year period.
- Values are calculated annually but provided as rolling 3-year means; ecosystem-specific data are supplied for moorland and forest scenarios, plus a grid-average dataset.

## Data products and structure
- CBED-deposition-moorland-2015-2017.csv
  - Columns include easting (m), northing (m), nox_m (oxidised nitrogen to moorland, keq ha-1 year-1), nhx_m (reduced nitrogen to moorland, keq ha-1 year-1), nms_m (non-marine sulphur to moorland, keq ha-1 year-1), nm_ca_mg_m (non-marine base cations to moorland, keq ha-1 year-1).
- CBED-deposition-forest-2015-2017.csv
  - Columns include easting (m), northing (m), nox_f (oxidised nitrogen to forest, keq ha-1 year-1), nhx_f (reduced nitrogen to forest, keq ha-1 year-1), nms_f (non-marine sulphur to forest, keq ha-1 year-1), nm_ca_mg_f (non-marine base cations to forest, keq ha-1 year-1).
- CBED-deposition-gridaverage-2015-2017.csv
  - Columns include easting (m), northing (m), nox_ga (oxidised nitrogen to grid average, keq ha-1 year-1), nhx_ga (reduced nitrogen to grid average, keq ha-1 year-1), nms_ga (non-marine sulphur to grid average, keq ha-1 year-1), nm_ca_mg_ga (non-marine base cations to grid average, keq ha-1 year-1).

## Temporal and spatial details
- Spatial resolution: 5x5 km grid squares across the UK.
- Temporal coverage: annual values, presented as rolling 3-year means to reduce inter-annual variability.
- Ecosystem scenarios: separate datasets for moorland and forest, plus a grid-average dataset for general use.
- Data orientation: deposition values expressed per habitat type and per grid cell, aligned with habitat proportions within each 5x5 km cell.

## Units, conversion, and interpretation
- All deposition values are in kilo-equivalents per hectare per year (keq ha-1 year-1).
- Conversions to kilograms per hectare per year:
  - Sulphur deposition: keq ha-1 year-1 × 16 = kg S ha-1 year-1
  - Oxidised/reduced nitrogen deposition: keq ha-1 year-1 × 14 = kg N ha-1 year-1
  - Combined base cations (Ca+Mg): keq ha-1 year-1 × 20 = kg Ca ha-1 year-1

## Quality assurance and governance
- CBED methods have undergone extensive peer review and participated in Defra model inter-comparison exercises.
- Documentation practices include versioning, central storage of code, and comprehensive methodological records.
- Mass balance checks are routinely performed to ensure numerical consistency against previous years.
- Results are published in peer-reviewed literature; method developments are overseen by senior responsible officers.

## Data access, metadata, and provenance
- Data are linked to supporting information from the UK Acidifying and Eutrophying Atmospheric Pollutants context.
- Primary data sources include the UKEAP network, rural measurements, and atmospheric models (e.g., FRAME, PCM).
- Key references and methodological details are provided within the data documentation and associated publications.
- URLs for data and supporting information:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap

## Applicability and limitations
- Purpose: to quantify pollutant deposition for assessment of critical loads and to inform policy decisions on atmospheric pollutants.
- Limitations acknowledged include inter-annual variability due to weather, orographic effects, dataset gaps, and the need to translate deposition values into habitat-specific exceedance assessments.
- The methodology emphasizes openness and data governance, with explicit sharing of data inputs where appropriate and clear documentation of data processing steps.