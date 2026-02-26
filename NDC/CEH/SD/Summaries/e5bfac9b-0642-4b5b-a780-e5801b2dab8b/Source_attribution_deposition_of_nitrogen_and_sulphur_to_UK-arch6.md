# Frame Modelling

- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to estimate annual mean deposition of reduced and oxidised nitrogen and sulphur over the UK.
- Domain and resolution: British Isles with a 5 km grid (172 x 144).

- Emissions input and sources
  - UK National Atmospheric Emissions Inventory (NAEI) providing 160 sub-sector emission categories, including 22 point sources and background area emissions split into 11 SNAP sectors.
  - Ammonia inputs from the National Ammonia Reduction Strategy Evaluation System (NARSES) split into 5 sectors.
  - Regional land masks applied to separate sources by country (England, Scotland, Wales, Northern Ireland).

- Running the model and footprint calculation
  - Base scenario run (all sources) vs runs with each source abated (25% reductions to avoid non-linearities).
  - Final footprints scaled by a factor of 4.
  - Footprint for a given id (n) calculated as FP(id=n) = DEP(id=0) - DEP(id=n) for each 5 km grid cell and pollutant (SOx, NOy, NHx).
  - Outputs include detailed species splits to distinguish short vs long-range inputs.

- Short/long-range deposition splits
  - 11 categories of deposition split into short vs long range, including wet/dry NH3, NH4+, HNO3, NO3-, NO2, SO2, SO4, for both grid averages and habitats (forest and moorland).

- Ecosystem and habitat differentiation
  - Deposition data output for three ecosystem types: forest, moorland (representing short semi-natural vegetation), and grid average (arable, grassland, urban, forest, moorland).
  - Deposition varies by habitat due to surface roughness (forests/moorland have higher dry deposition rates for ammonia).

- Post-processing and calibration
  - Normalisation: individual source footprints are normalised so their sum matches the baseline deposition to account for model non-linearities.
  - Calibration to CBED data (Concentration Based Estimated Deposition) for 2011–2013 to obtain a robust annual deposition estimate.
  - Calibration equations:
    - DEP(CAL, 2012) = DEP(UNC, 2012) * ( DEP(CBED, 2011-2013) / DEP(UNC, 2012) )
    - FP(CAL, 2012, id=n) = FP(UNC, 2012, id=n) * ( DEP(CAL, 2012) / sum FP(UNC, 2012, id=1..160) )
  - This ensures calibrated footprints align with CBED totals for 2012 when combined.

- Spatial mapping and data outputs
  - FRAME outputs 160 files per footprint type for each pollutant; aggregated to 90 footprint files to optimize processing.
  - Outputs cover deposition for SOx, NOy, NHx, including grid-average and ecosystem-specific (forest, moorland) components, at 5 x 5 km resolution.
  - Data products include ecosystem-specific source attribution and deposition data for nitrogen and sulfur, with metadata such as footprint ID, footprint name, source location (by country), and grid coordinates (Easting/Northing).

- Data formats and quality control
  - Each footprint dataset includes fields such as GRID/SOD/SOW, NOD/NOW, NHD/NHW, etc., across local (grid, forest, moorland) and long-range components.
  - Outputs include 90 footprint datasets, plus a set of 160 input/output files, with additional metadata for traceability.
  - Quality control measures:
    - Normalisation ensures sums match baseline.
    - National budgets for total deposition are checked against previous years.
    - Every footprint output is also produced as a JPG to facilitate error detection.

- Access, references, and resources
  - Primary data/resource location: http://www.pollutantdeposition.ceh.ac.uk/node/319
  - The output includes a comprehensive set of 5x5 km deposition data and footprint-level data suitable for policy analysis and further data exploration.

- Summary of purpose for data support
  - Provides a transparent, calibrated, and well-documented framework to attribute deposition to emission sources.
  - Delivers multiple data products (base footprints, calibrated footprints, ecosystem-specific and short/long-range components) to enable end-user exploration, analysis, and integration with other datasets.