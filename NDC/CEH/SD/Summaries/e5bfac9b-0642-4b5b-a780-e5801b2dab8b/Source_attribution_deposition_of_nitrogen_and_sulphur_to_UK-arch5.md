# Frame Modelling

- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to assess the annual mean deposition of reduced and oxidised nitrogen and sulphur over the United Kingdom.
- Domain and resolution: British Isles, 5 km grid, 172 x 144 grid cells.
- Emissions inputs: UK National Atmospheric Emissions Inventory (NAEI) with 160 sub-sector categories, including 22 point sources and background area emissions; emissions broken down by SNAP sectors, international shipping, and European imports.
- Ammonia inputs: derived from NARSES model split into five sectors (livestock, fertiliser, non-agricultural abatable/non-abatable sources, waste sector).
- Spatial masking: regional masks by England, Scotland, Wales, Northern Ireland to inform regulators about source locations.

- Major outputs: deposition footprints for dry and wet deposition of SOx, NOy, and NHx, plus detailed species breakdown and ecosystem-specific deposition.

- Point sources and runs: Largest point sources (power stations, refineries, steel works, etc.) are identified; model runs created for a baseline (all sources) and for each source abated individually, using a 25% reduction per run to minimise non-linearities; final footprints are scaled (multiplied) to maintain comparability.

- Footprint calculation: footprints for each source are computed as the difference between the baseline deposition and the deposition with the source abated:
  FP(id=n) = DEP(id=0) - DEP(id=n).

- Short/long-range attribution: deposition components are split to estimate short- and long-range inputs for each pollutant and species, across multiple deposition pathways (wet/dry, NHx species, NOx, SO2/SO4, etc.).

- Habitat-specific deposition: outputs distinguished for three ecosystem types—forest, moorland, and grid average (arable, grassland, urban, etc.) to reflect surface roughness effects on deposition rates; dry NH3 deposition is higher to forests and moorland.

- Post-processing and calibration:
  - Normalisation: individual source footprints are normalised so their sum matches the baseline total to account for non-linearities.
  - Budget validation: national total deposition budgets are checked against previous years.
  - Calibration to CBED: FRAME outputs are calibrated to the Consolidation Based Estimated Deposition (CBED) 2011–2013 dataset to provide robust annual estimates (e.g., CBED for 2011–2013 averaged).
  - Calibration equations:
    - DEP(CAL, 2012) = DEP(UNC, 2012) × [DEP(CBED, 2011–2013) / DEP(UNC, 2012)]
    - FP(CAL, 2012, id=n) = FP(UNC, 2012, id=n) × [DEP(CAL, 2012) / Σ FP(UNC, 2012, id=1..160)]
  - Calibrated footprints are designed to reproduce official CBED totals for 2012 when aggregated.

- Data outputs and structure:
  - FRAME produces 160 files per footprint type per pollutant; deposition data for SOx, NOy, NHx across 5 km grid cells.
  - 160 footprint files are aggregated to 90 footprint files to improve processing efficiency.
  - 90 footprint datasets are ecosystem- and source-specific, with fields including:
    - Spatial coordinates (EASTING, NORTHING)
    - FOOTPRINT_ID and FOOTPRINT_NAME
    - SOURCE LOCATION (country/region)
    - Deposition values for grid average, forest, and moorland, for both short-range and long-range pathways
    - Pollutant-specific components (SOx, NOy, NHx) and sub-species (e.g., NH3, NH4+, NO2, HNO3, SO2, SO4)
  - Output includes separate data streams for:
    - Short-range vs long-range deposition
    - Grid-average vs ecosystem-specific deposition (forest, moorland)
  - Data delivery and QC artifacts:
    - Each footprint output is also produced as a jpg to facilitate error detection
    - National budgets of total deposition are checked against prior years

- Spatial mapping and data products:
  - FRAME outputs 160 files per footprint type; these are aggregated to 90 footprint files for processing
  - Data are distributed as 5 x 5 km grid-square components, with ecosystem-specific attribution (moorland, forest/woodland) and grid-average deposition
  - Post-processed and calibrated footprints are designed to align with official CBED totals for 2012

- Resource and access:
  - Data and methodology references available at the given web resource (URL provided in the document)

- Quality control and governance considerations for data stewards:
  - Provenance: traceable from emissions (NAEI, SNAP, NARSES) through to calibrated deposition footprints
  - Metadata and standards: structured footprint identifiers, source locations, and deposition components support consistent cataloguing
  - Reproducibility: baseline plus abatement approach with a defined 25% reduction and a scaling step ensures reproducible footprints
 Calibration: CBED-based calibration ensures alignment with national deposition budgets
  - Data quality checks: normalisation to baseline, budget checks, and per-footprint JPG QC images
  - Update and maintenance: workflows tied to annual deposition calibration (CBED 2011–2013) and 2012 calibration, enabling updates with new CBED-like references
  - Data sharing considerations: detailed footprint and deposition data, with ecosystem-specific and short/long-range breakdowns, facilitate policy-relevant analyses while preserving traceability to source categories

- Overall aim alignment for Data Stewards:
  - Ensures transparent data lineage from emission inventories to deposition footprints
  - Supports governance of large, complex multi-source, multi-species deposition datasets
  - Provides metadata-rich, calibrated datasets suitable for policy analysis, environmental assessments, and regulatory reporting
  - Includes quality control, versioning cues (calibration steps), and accessible documentation via the resource URL