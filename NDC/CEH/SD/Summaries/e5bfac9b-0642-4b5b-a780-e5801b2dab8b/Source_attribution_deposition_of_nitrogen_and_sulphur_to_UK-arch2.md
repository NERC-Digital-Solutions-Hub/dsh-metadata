# Frame Modelling

- Purpose and scope
  - FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to assess the annual mean deposition of reduced and oxidised nitrogen and sulphur over the United Kingdom.
  - Domain: British Isles with a 5 km grid (172 x 144).
  - Outputs include dry and wet deposition of SOx, NOy, and NHx, at a 5 km resolution, across the UK.

- Emissions data and inputs
  - Emissions from UK National Atmospheric Emissions Inventory (NAEI), split into 160 sub-sector categories.
  - Included 22 point sources and background area emissions across 11 SNAP sectors; also includes international shipping and European emissions.
  - Ammonia (NH3) inputs derived from the National Ammonia Reduction Strategy Evaluation System (NARSES), split into five sectors (e.g., livestock, fertiliser, non-agricultural NH3 sources, waste sector).
  - Regional land masks assign sources by country (England, Scotland, Wales, Northern Ireland) to aid regulators.
  - Major inputs highlighted: largest point sources for SOx and NOx (e.g., power stations, refineries, steel works).

- Model execution and footprint generation
  - Baseline run with all sources, followed by successive runs with each source abated by 25% to reduce non-linearities; final footprints are scaled by a factor of 4.
  - Footprints are computed as the difference between the baseline deposition and the deposition when a given source is abated:
    FP(id=n) = DEP(id=0) - DEP(id=n)
  - For each 5 km grid square, deposition for SOx, NOy, and NHx is calculated across all footprints.
  - Output is further partitioned into short-range vs long-range contributions for various species (e.g., wet/dry NH3, NH4+, HNO3, NO3-, NO2, SO2, SO4) and separated by ecosystem type (forest, moorland, grid average) due to surface roughness effects on deposition velocity.

- Short/long-range attribution and ecosystem differentiation
  - Short/long-range splits are applied for multiple species and deposition modes (detailed in the document’s 1–11 categories).
  - Deposition data are provided for three ecosystem types: forest, moorland, and grid average (arable, grassland, urban, etc.), reflecting differing surface roughness and deposition velocities.

- Calibration, normalization, and quality control
  - Post-processing normalizes each footprint so its sum matches the baseline simulation to account for non-linearities.
  - A calibration procedure aligns FRAME results with the CBED (Concentration Based Estimated Deposition) dataset for 2011–2013, producing calibrated deposition for 2012 (DEP_CAL) via a ratio method.
  - Footprints can also be calibrated using the CBED-based approach to ensure footprints sum to official CBED totals for 2012.
  - Quality checks include: budget verification against previous years, generation of footprint-specific JPGs to identify errors, and normalization checks (average difference between footprint sums and baseline around 4%).

- Data outputs and structure
  - Frame outputs 160 files per footprint type per pollutant, subsequently aggregated to 90 footprint files to ease processing.
  - 90 footprint datasets with ecosystem-specific source attribution and deposition data for nitrogen and sulphur compounds, at 5 x 5 km resolution.
  - 90-footprint data fields include spatial coordinates (Easting/Northing), FOOTPRINT_ID, FOOTPRINT_NAME, SOURCE LOCATION, and deposition components for grid, forest, and moorland (local and long-range categories) across multiple species.
  - Example footprint data organization includes detailed local vs long-range deposition across SOx, NOx, NHx components for grid, forest, and moorland.

- Output records and accessibility
  - Data are organized as 90 footprint datasets with ecosystem-specific deposition and source attribution, plus 160 initial footprint files per pollutant/footprint type (reduced to 90 for processing).
  - Resource link for deposition data: http://www.pollutantdeposition.ceh.ac.uk/node/319
  - Outputs include explicit details of footprint names, source locations (England, Scotland, Wales, Northern Ireland), and a wide range of deposition metrics (e.g., GRD_SOD_LOCAL, FOR_SOW_LOCAL, MOR_NHW_LONG, etc.).

- Calibration steps and values
  - Calibration uses CBED data to adjust FRAME deposit estimates and footprint sums to align with 2012 totals, ensuring compatibility with official deposition estimates.
  - Calibration equations (2) and (3) describe the methodological approach for depositing calibration to 2012 and calibrating footprints, respectively.

- Summary of relevance for environmental analysts
  - Provides a reproducible, calibrated, high-resolution (5 km) appraisal of nitrogen and sulphur deposition from multiple emission sources across the UK.
  - Enables source-receptor analysis by abating individual sources, with clear attribution of short- vs long-range inputs and ecosystem-specific deposition.
  - Supports policy analysis and regulatory scrutiny by aligning model outputs to CBED benchmarks and delivering standardized data products suitable for critical loads and deposition budgeting.