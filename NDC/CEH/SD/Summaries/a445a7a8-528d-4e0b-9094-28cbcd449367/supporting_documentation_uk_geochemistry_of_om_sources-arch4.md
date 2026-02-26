# Supporting documentation for data resource UK_geochemistry_of_OM_sources.csv

- Overview
  - Documents a dataset of bulk elemental and stable isotope composition of organic matter from terrestrial, intertidal, and marine environments in the UK, collected between 2016 and 2021.
  - Aims to support constraining organic carbon sources (terrestrial vs marine) when used with isotope mixing models.

- Datasets Covered
  - UK_geochemistry_of_OM_sources.csv
    - Samples: 491
    - Environments: terrestrial (soil, peat, living/dead biomass), intertidal (saltmarsh vegetation, saltmarsh roots, seagrass biomass, mudflat, faecal matter), marine (macroalgae, microalgae, zooplankton, finfish aquaculture waste)
    - Analytes: bulk organic carbon (OC) and nitrogen (N), stable isotopes δ13C_org and δ15N
    - Locations: United Kingdom with specified observation coordinates
    - Purpose: support isotope-based source apportionment
  - Aboveground_Biomass_Carbon_UK.csv
    - Metadata-style resource describing sample_id and sample_class for various biotic/abiotic components
    - Classes include Terrestrial Vegetation, Soil, Wetland Vegetation, Zooplankton, Seagrass (vegetation/soil), Saltmarsh (vegetation/roots), Phytoplankton, Mudflat, Microalgae, Macroalgae, Faecal Matter, Aquaculture, Analytical Standard
    - Includes geographic/national context (Nation: Scotland, England, Wales) and NVC (National Vegetation Classification)

- Data Content and Variables
  - δ13C_org (‰), δ15N (‰)
  - OC (%) and N (%)
  - C/N and N/C ratios
  - Sample identifiers and descriptive metadata (sample_class, detailed sample descriptions)
  - Additional metadata fields: National vegetation classification (NVC), location descriptions, nation

- Geographic and Temporal Coverage
  - Geographic scope: United Kingdom
  - Temporal scope: sampling conducted 2016–2021
  - Location details include explicit coordinates for observations and descriptive location notes

- Data Collection, Processing, and Quality Assurance
  - Sampling: coastal catchments around the UK; field descriptions provided by expert knowledge
  - Sample handling: stored at -20°C; oven-dried at 40°C for 72 hours; milled to fine powder
  - Stable isotope analysis: ~12 mg processed sediment placed into tin capsules and 12 mg into silver capsules; acid fumigation (to remove carbonates) performed prior to analysis
  - Analysis platform: EA-IRMS (elemental analyzer coupled to isotope ratio mass spectrometer)
  - Calibration/QA: isotopic values quality-controlled via repeat analysis of high OC sediment standard (B2151) with reference values for C and N; equipment calibration per University of St Andrews practices
  - Data checks: laboratory practices outlined; some statistical treatment fields noted as NA

- File Formats and Metadata
  - Primary data format: .csv for UK_geochemistry_of_OM_sources.csv
  - Metadata table: Aboveground_Biomass_Carbon_UK.csv with descriptive fields (Sample_id, Sample_class, Description, Nation, NVC, etc.)
  - Some fields use NA to indicate missing data

- Data Governance, Discoverability, and Updates
  - Documentation provides method-level transparency (sampling, preparation, analysis, QA)
  - Clear description of variables and processing steps to aid data discovery and reuse
  - The documentation implies ongoing use in conjunction with isotope mixing models; however explicit update cadence is not specified

- Use Cases and Implications for Data Leaders
  - Enables quantification of terrestrial vs marine contributions to UK organic carbon via isotope mixing models
  - Supports cross-environment comparisons (terrestrial, intertidal, marine) and integration with aboveground biomass data
  - Provides a structured, well-documented dataset with robust QA procedures suitable for policy and scientific analyses requiring traceable metadata and replicable methods

- Limitations and Gaps
  - Some data fields are NA (unknowns in statistical treatment and certain metadata)
  - Detailed metadata for Aboveground_Biomass_Carbon_UK.csv is descriptive but may require linkage to raw data or downstream datasets for full reproducibility
  - Temporal coverage is limited to 2016–2021; future updates beyond this range not specified

- References
  - Harris, D., Horwáth, W.R. and Van Kessel, C., 2001. Acid fumigation of soils to remove carbonates prior to total organic carbon or carbon-13 isotopic analysis. Soil Science Society of America Journal, 65(6), pp.1853-1856.
  - Rodwell, J.S., 2000. Maritime communities and vegetation of open habitats.