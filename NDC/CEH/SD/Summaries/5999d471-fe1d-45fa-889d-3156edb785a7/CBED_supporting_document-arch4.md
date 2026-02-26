# Concentration Based Estimated Deposition (CBED) methodology

## Overview
- Generates 5x5 km gridded deposition data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
- Uses measured air concentrations and precipitation ion concentrations from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Produces dataset variants for moorland, forest, and grid-wide averages; suitable for critical load exceedance calculations and ecosystem assessments.

## Data content and scope
- Wet deposition derived from precipitation ion concentrations and annual precipitation data.
- Dry deposition produced by combining gas/PM concentration maps with habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
- Deposition to land cover categories is weighted by their proportions within each 5x5 km grid cell.
- Critical load calculations apply moorland values to non-woodland habitats and forest values to woodland habitats.
- Nitric acid concentrations interpolated from ~30 sites; NO2 and SO2 from PCM model; ammonia from FRAME model plus UKEAP measurements (2017 emissions used in FRAME).

## Processing pipeline and methodology
- Site measurements interpolated to UK concentration maps.
- Ion concentrations in precipitation combined with annual precipitation to produce wet deposition.
- Dry deposition uses habitat-specific velocities; aggregated to grid cells by land-cover proportions.
- Orographic enhancement applied to wet deposition in upland regions; occult deposition (direct cloud droplet deposition) included.
- Inter-annual variability acknowledged; three-year rolling means used to smooth fluctuations.

## Temporal and spatial resolution
- Annual deposition values generated but provided as rolling 3-year means.
- Spatial resolution: 5x5 km grid cells across the UK.
- Ecosystem-specific deposition data available for moorland and forest; grid-average deposition provided as a separate dataset.

## Data structure and files
- Three main CSV data files (for 2016–2018):
  - CBED-deposition-moorland-2016-2018.csv
  - CBED-deposition-forest-2016-2018.csv
  - CBED-deposition-gridaverage-2016-2018.csv
- Common columns:
  - easting; northing (centre of 5x5 km square, OS Great Britain grid) in metres.
  - Deposition values in keq ha-1 year-1:
    - Moorland: nox_m (oxidised N), nhx_m (reduced N), nms_m (non-marine S), ca_mg_m (base cations).
    - Forest: nox_f, nhx_f, nms_f, ca_m_f.
    - Grid average: nox_ga, nhx_ga, nms_ga, ca_mga.
- Grid-average file has fewer rows (10678) than the forest/moorland files (11172) because it requires all nitrogen forms to be present.

## Units and conversions
- All deposition values are expressed as keq ha-1 year-1.
- Conversions to kg ha-1 year-1:
  - Sulphur: keq × 16
  - Nitrogen (oxidised and reduced): keq × 14
  - Base cations (Ca+Mg): keq × 20

## Quality assurance and provenance
- Methods aligned with Government analytical model QA practices; extensive peer review.
- Part of Defra model inter-comparison exercises.
- Documented versioning, central code storage, and mass-balance checks for numerical consistency.
- Data and method developments are overseen by senior responsible officers; widely published in peer-reviewed literature.

## Access, references, and metadata
- Resource locators:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap (UK Acidifying and Eutrophying Atmospheric Pollutants)
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap (UK Air Defra network information)
- Included references and supporting information related to data sources and modelling approaches.

## Data governance considerations for Data Leaders
- Data lineage: multi-source inputs (measurements, PCM model, FRAME model) and spatial-temporal aggregation.
- Metadata and discoverability: dataset naming, grid definitions, and unit conventions clearly defined; three-year rolling means documentation essential.
- Versioning and updates: annual data generation with rolling 3-year means; ensure downstream systems handle rolling window semantics.
- Data quality and stewardship: QA procedures, mass-balance checks, and cross-validation with literature; clear handling of missing data (grid-average limitations).
- Usage considerations: explicit conversion factors provided; suitability for critical load exceedance assessments and ecosystem impact analyses.
- Gaps and limitations: inter-annual variability reduced by smoothing; potential data gaps in grid-average due to missing forms; reliance on model components (PCM, FRAME) for some species/locations.
- Data access and licensing: ensure clear licensing and citation requirements when integrated into broader data systems or policy analyses.