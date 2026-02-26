# Concentration Based Estimated Deposition (CBED) methodology

- Purpose: Produces 5x5 km resolution gridded estimates of wet and dry deposition of sulphur, oxidised nitrogen, reduced nitrogen, and base cations across the UK, derived from measured gases/particulates in air and ions in precipitation via the UKEAP network.
- Coverage: UK-wide deposition maps derived from site measurements and interpolations, with deposition values allocated to three ecosystem representations (moorland, forest/woodland) and a grid-average scenario.

## How CBED works

- Data inputs: Site-based measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network; precipitation data from the UK Met Office.
- Wet deposition: Combines ion concentrations in precipitation with annual precipitation to estimate wet deposition; accounts for occult deposition (direct deposition of cloud droplets to vegetation) and separates anthropogenic vs total components using sea-salt proxies.
- Dry deposition: Uses gas/particulate concentrations plus habitat-specific deposition velocities to estimate dry deposition for five land cover categories (forest, moorland, grassland, arable, urban).
- Spatial application: Deposition values are allocated to grid squares based on land cover proportions and applied to moorland or forest categories for critical load calculations.
- Temporal treatment: Annual calculations, but provided as rolling 3-year means to smooth inter-annual variability.

## Temporal and ecosystem specifics

- 3-year means: Outputs are averaged over three years, with ecosystem-specific values in two modes (moorland or forest/woodland) and grid-average values.
- Ecosystem representations: 
  - Moorland deposition (nox_m, nhx_m, nms_m, nm_ca_mg_m)
  - Forest deposition (nox_f, nhx_f, nms_f, nm_ca_mg_f)
  - Grid-average deposition (nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga)

## Data products and structure

- Files (2015–2017 3-year means):
  - CBED-deposition-moorland-2015-2017.csv
  - CBED-deposition-forest-2015-2017.csv
  - CBED-deposition-gridaverage-2015-2017.csv
- Common fields:
  - easting, northing: centre coordinates of the 5x5 km grid square (metres)
  - Deposition fields (keq ha-1 year-1): specific to each ecosystem category (oxidised nitrogen, reduced nitrogen, non-marine sulphur, non-marine base cations)
- Deposition units and conversion:
  - All values are expressed as keq ha-1 year-1
  - Conversions to kg per hectare per year:
    - SO2/SO4 (sulfur): keq × 16
    - Oxidised/reduced nitrogen: keq × 14
    - Base cations (Ca+Mg): keq × 20
- Metadata and provenance:
  - Methods designed to align with government QA practices
  - Extensive peer review and involvement in Defra model inter-comparison
  - Documentation, version control, and mass-balance checks are standard

## Quality, governance and references

- Quality assurance:
  - Peer-reviewed methodology and participation in model inter-comparison exercises
  - Documented method developments with central version control
  - Mass-balance checks and comparisons to prior years
- Documentation and citations:
  - Numerous referenced studies on atmospheric transport, deposition modelling, and site-specific analyses
- Data accessibility:
  - Primary information page: UK pollutant deposition site (pollutantdeposition.ceh.ac.uk)
  - Supporting information and networks: UK Air Defra network pages

## Relevance for data leadership and use

- Data system considerations:
  - Demonstrates end-to-end data lifecycle: collection (UKEAP), processing (interpolation and deposition modelling), product generation (ecosystem-specific and grid-average outputs), and quality governance.
- User needs and dissemination:
  - Produces ready-to-use deposition products with clear spatial (5x5 km) and ecological (moorland/forest/grid-average) contexts
  - Provides standardized units and conversion factors for integration with policy, ecological risk, and critical load assessment workflows
- Discoverability and updates:
  - Data are organized with explicit file naming, clear coordinate references, and metadata; rolling 3-year means indicate ongoing update potential as new years are added
- Potential challenges:
  - Inter-annual variability and dependence on multiple input data sources (measurements, models, and regional factors) require ongoing validation and versioned updates
  - Spatial allocation relies on land-cover composition within grid cells, which may affect granularity for highly heterogenous landscapes