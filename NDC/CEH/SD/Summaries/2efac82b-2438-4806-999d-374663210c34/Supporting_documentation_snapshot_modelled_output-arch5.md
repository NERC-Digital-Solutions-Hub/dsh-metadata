# Supporting documentation

## Overview
- Dataset contains model outputs for Great Britain from two models: JULES (land surface model) and ECO-AG (econometric agricultural land use model).
- Eight scenarios examine the effects of climate, CO2 concentrations, and irrigation under unmitigated climate change (RCP8.5).

## Data content
- JULES outputs: 1.5 km x 1.5 km grid, variables include net primary productivity (npp), runoff, and irrigation water demand (irrig_water).
- ECO-AG outputs: 2 km x 2 km grid, arable land area per grid cell.
- Additional grid coordinate data: ECO_AG_grid_2km.csv provides easting/northing, corners, and grid cell identifiers.

## Data structure and files
- JULES_output directory:
  - Tar files, each for one scenario and one variable (npp, runoff, irrig_water).
  - Each tar contains 132 files (11 years of monthly data per year) with data for all grid cells plus longitude/latitude.
  - File naming: {scenario run}_{variable}_yyyymm.nc.
  - Present-climate data labeled normally; future-climate data labeled 100 years later in the date portion of filenames.
- ECO-AG outputs:
  - ECO_AG_output directory with files named ECO_AG_{scenario run}.csv containing arable land area (hectares, up to 400 ha) per grid cell.
  - ECO_AG_grid_2km.csv provides grid cell coordinates and mapping to grid cell identifiers.

## Spatial and temporal resolution
- JULES: 1.5 km x 1.5 km grid; daily temporal resolution aggregated to monthly means for 11-year periods.
- ECO-AG: 2 km x 2 km grid covering Great Britain; uses census-based land-use inputs (sixteen-year window spanning 1972–2010 in the dataset construction).

## Scenarios and drivers
- Eight scenarios explore combinations of climate, CO2, and irrigation:
  - ECO-AG Baseline states (Climate present, CO2 No, Irrigation No)
  - JULES Baseline states (Climate present, CO2 Present, Irrigation No)
  - Climate-only, Irrigation-only, Climate & Irrigation, and Climate & CO2 combinations
  - Distinctions between ECO-AG and JULES configurations (e.g., ECO-AG cannot model CO2 effects)
- Climate forcing uses high-resolution Regional Climate Model (RCM) data:
  - 1998–2008 present-day climate for northern GB and southern GB data combined via a piecewise linear weighting function.
  - Future climate with a 11-year period at end-of-century; CO2 concentration 936 ppm (RCP8.5).
  - Present-day CO2 around 386.5 ppm (approximate 2009 levels) for present data.
- Data sources and methods:
  - JULES outputs (vn4.9) produced with Rose suite u-ao645; community-led model with UK Met Office/Centre for Ecology and Hydrology backing.
  - ECO-AG outputs built on Fezzi & Bateman (2011) methods, UK NEA context, using June Agricultural Census land-use data.

## Quality control and provenance
- JULES is a community-developed model; access requires registration to the JULES repository (code.metoffice.gov.uk/trac/jules).
- Data provenance:
  - JULES configuration: Rose suite u-ao645, branch full_UK; file versions and structure documented.
  - ECO-AG methodology and underpinning studies cited (Fezzi & Bateman; UK NEA follow-on; related climate studies).
- Data have been peer-reviewed and come with established references for reproducibility and validation.

## Access, licensing, and reuse
- JULES data are accessible via the JULES repository; registration required for download.
- ECO-AG data are provided as CSV and grid coordinate files; direct access implied by dataset documentation.
- File naming conventions and units are specified to support reproducibility and integration with other data sources.

## Metadata and governance considerations for Data Stewards
- Clearly documented data structures and variable definitions (npp, runoff, irrig_water; grid mappings; unit conventions) support metadata completeness.
- Consistent grid definitions (1.5 km for JULES, 2 km for ECO-AG) require careful alignment when merging datasets.
- Time labeling of future data uses a 100-year offset in file names, which should be captured in metadata to avoid misinterpretation.
- Access controls and registration requirements should be reflected in data catalogs; provenance and version information should be maintained for future updates.
- Potential data governance challenges include handling multiple systems and formats, ensuring timely data access from model outputs, and maintaining metadata accuracy across model versions and scenario updates.

## References
- Bateman, I. et al., 2014. UK National Ecosystem Assessment Follow-on. Work Package Report 3: Economic value of ecosystem services.
- Bateman, I. J. et al., 2013. Bringing ecosystem services into economic decision-making: land use in the United Kingdom. Science.
- Chan, S. C., et al., 2018. Projected changes in extreme precipitation over Scotland and Northern England using a high-resolution regional climate model. Climate Dynamics.
- Fezzi, C. et al., 2014. Valuing provisioning ecosystem services in agriculture: the impact of climate change on food production in the United Kingdom. Environmental and Resource Economics.
- Fezzi, C. & Bateman, I. J., 2011. Structural agricultural land use modeling for spatial agroenvironmental policy analysis. American Journal of Agricultural Economics.
- Fezzi, C. et al., 2015. The environmental impact of climate change adaptation on land use and water quality. Nature Climate Change.
- Kendon, E. J. et al., 2014. Heavier summer downpours with climate change revealed by weather forecast resolution model. Nature Climate Change.
- Kendon, E. J. et al., 2012. Realism of rainfall in a very high-resolution regional climate model. Journal of Climate.
- NEA, U., 2011. The UK national ecosystem assessment technical report. UNEP-WCMC.