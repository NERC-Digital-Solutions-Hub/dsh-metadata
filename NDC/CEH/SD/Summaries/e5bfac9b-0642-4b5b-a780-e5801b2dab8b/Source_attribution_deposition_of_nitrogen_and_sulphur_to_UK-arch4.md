# Frame Modelling

- Frame (Fine Resolution Multi-pollutant Exchange) is a 5 km grid, 172 x 144 domain covering the British Isles, using a Lagrangian atmospheric transport model to estimate annual mean deposition of reduced and oxidised nitrogen and sulphur in the UK.
- The model uses emissions inputs from the UK National Atmospheric Emissions Inventory (NAEI) with 160 sub-sector categories, including 22 point sources and background emissions split into SNAP sectors, plus international shipping and European emissions.
- Ammonia inputs come from the National Ammonia Reduction Strategy Evaluation System (NARSES) and are divided into five sectors. Regional land masks separate sources by England, Scotland, Wales, and Northern Ireland.

- Data inputs and structure
  - Emissions sources are categorized by sector, point sources, offshore, international shipping, and European imports, with detailed breakdowns (e.g., energy production, transport, agriculture, industry).
  - Outputs include deposition for sulphur (SOx), oxidised nitrogen (NOy), and reduced nitrogen (NHx) across 5 km grid cells, plus breakdown by ecosystem types (forest, moorland, grid average) to reflect surface roughness effects on deposition.
  - A total of 160 footprint files are produced for each footprint type and pollutant, with aggregation down to 90 footprint files to ease processing.

- Model runs and footprint calculation
  - The base FRAME run (all sources) is repeated with each emission source abated individually. To reduce non-linear chemical interactions, a 25% emission reduction is used for each abated source, and the final footprints are scaled by a factor of 4.
  - Source footprints are calculated as the difference between the baseline deposition and the deposition with a specific source abated: FP(id=n) = DEP(id=0) - DEP(id=n).
  - Outputs include deposition data for SOx, NOy, and NHx, further disaggregated into short-range and long-range components, across 11 detailed species/compounds (e.g., wet/dry NH3, NH4+, HNO3, NO2, SO2, SO4) and across ecosystem types.

- Post-processing, calibration, and quality control
  - Deposition footprints are normalised so their sum matches the baseline simulation, mitigating model non-linearities (average discrepancy around 4%).
  - Calibration is applied to align FRAME outputs with the official CBED (Concentration Based Estimated Deposition) deposition totals for 2012, using CBED data from 2011–2013. Calibration equations adjust both bulk deposition and footprints to ensure consistency with CBED totals.
  - All outputs are validated against national budgets and previous years to detect discrepancies, and each footprint file is also produced as a JPG for quick error identification.

- Output data structure and accessibility
  - FRAME outputs are provided as 160 files per footprint type for each pollutant, later aggregated to 90 footprint files, with data for S, NOx, and NHx deposition across the 5 km UK grid.
  - Datasets include ecosystem-specific deposition data for moorland, forest/woodland, and grid average, capturing differences in deposition velocity and surface roughness.
  - Metadata and data dictionaries accompany the outputs, including coordinates (Easting/Northing), footprint IDs, source locations, and a wide set of deposition variables broken down by local grid, forest, and moorland rasters and long-range vs short-range components.

- Data products, interpretation, and uses
  - Outputs support attribution of deposition to specific source groups (e.g., energy, transport, agriculture, shipping) and help regulators understand spatial distributions of impacts.
  - Calibrated footprints enable more robust calculations of Critical Loads exceedance and other policy-relevant assessments by aligning model results with observed CBED-derived deposition.

- Resources and references
  - Primary data source for emissions: NAEI; ammonia sources: NARSES; calibration reference: CBED (APIS 2015) using 2011–2013 data.
  - Related methodologies and policy context include European-scale approaches (EMEP) and deposition calibration practices.
  - Practical access: http://www.pollutantdeposition.ceh.ac.uk/node/319
  - Quality assurance notes: national budgets checked against previous years; footprint outputs include error-detection aids (jpg files) to identify anomalous runs.

- Implications for data leadership and governance
  - Emphasizes integration of diverse emission datasets (160 sub-sectors, point sources, international inputs) and the need for careful calibration to official deposition datasets (CBED).
  - Highlights importance of metadata standardization (footprint IDs, source locations, ecosystem classifications) to maintain discoverability and reusability of 90 footprint datasets.
  - Demonstrates a rigorous post-processing workflow (normalisation, calibration, quality checks) to ensure reliable, policy-relevant data products and traceable data lineage.