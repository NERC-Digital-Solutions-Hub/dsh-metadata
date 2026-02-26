# Supporting documentation for data resource UK_geochemistry_of_OM_sources.csv

- Overview
  - Bulk elemental (organic carbon and nitrogen) and stable isotope composition (δ13C_org and δ15N) of organic matter from terrestrial, intertidal, and marine environments in the UK (2016–2021).
  - Aims to constrain organic carbon sources (terrestrial vs marine) when used with isotope mixing models.
  - Sample set: 491 samples from diverse substrates (soil, peat, living/dead biomass; saltmarsh vegetation and roots; seagrass; mudflat; faecal matter; macroalgae; zooplankton; finfish aquaculture waste).
  - Geographic coverage: United Kingdom with coordinates provided for observation locations.

- Data resource: UK_geochemistry_of_OM_sources.csv
  - Observed variables (examples)
    - δ13C_org (‰), δ15N (‰), OC content (%), N content (%), C/N ratio, N/C ratio.
  - Sampling and storage
    - Coastal catchments across the UK; samples stored at -20°C prior to analysis.
  - Sample preparation and analysis
    - Oven drying (40°C, 72 h) and milling to a fine powder.
    - Isotopic analysis: ~12 mg processed sediment in tin capsules; ~12 mg in silver capsules; acid fumigation to remove carbonate; EA-IRMS analysis.
  - Quality control and calibration
    - Isotopic values quality-checked via repeat analysis of high OC sediment standard (B2151) with reference values for C and N.
    - Laboratory equipment calibrated per University of St Andrews practices.
  - Data handling and format
    - File format: .csv.
    - Metadata fields include: location descriptions, nation (Scotland, England, Wales), NVC (National Vegetation Classification), delta_13Corg_per_mil, delta_15N_per_mil, OC_perc, N_perc, CN, NC.
  - Notes and references
    - Calibration/analysis references: Harris et al. (2001) on acid fumigation; Rodwell (2000) for vegetation classification.

- Data resource: Aboveground_Biomass_Carbon_UK.csv
  - Description
    - Detailed sample descriptions for aboveground biomass carbon across UK datasets.
  - Sample_id and Sample_class
    - Classifications include Terrestrial Vegetation, Soil, Wetland Vegetation, Zooplankton, Seagrass Vegetation, Seagrass Soil, Saltmarsh Vegetation, Saltmarsh Roots, Phytoplankton, Mudflat, Mix, Microalgae, Macroalgae, Faecal Matter, Aquaculture, Analytical Standard.
  - Metadata fields
    - NVC (National Vegetation Classification), Nation (England, Scotland, Wales).
    - delta_13Corg (‰), delta_15N (‰), OC_perc, N_perc, CN, NC.
  - Data formatting
    - Structure largely consists of Sample_id, Sample_class, Description fields with text values indicating sample category and description of location and material.
  - Notes
    - Provides a structured scheme for describing biomass carbon across diverse UK habitats, complementing the geochemistry dataset.

- Data quality, governance and use in monitoring
  - The documentation highlights rigorous sampling, storage, preparation, and isotopic analysis protocols, with quality control steps (standards, calibration) to ensure data reliability for policy-relevant monitoring.
  - Metadata breadth (locations, nation, habitat/classification, isotopic and elemental measurements) supports reproducibility, data discovery, and integration into monitoring dashboards and reports.
  - Public sharing of underlying data is intended, though metadata completeness and transformations required for use may pose practical barriers, aligning with common monitoring framework challenges.
  - References provided for methodological choices (acid fumigation, isotope analysis) to support traceability and methodological scrutiny.

- Relevance for monitoring frameworks
  - Establishes UK-wide baselines of organic matter sources and elemental/isotopic composition across terrestrial, intertidal, and marine environments.
  - Enables policy-relevant assessment of carbon sources and trophic/biogeochemical processes when combined with mixing models.
  - The structured metadata and QA practices support transparent data governance, data integration, and evidence-based decision making in environmental health monitoring.