# UKCEH Countryside Survey QA metadata and analysis report CS 2020 - EIDC Topsoil physico-chemical data 2020

- Purpose and scope
  - QA metadata and analysis report for topsoil physico-chemical data from the UK Countryside Survey (CS) 2020.
  - Part of the rolling Countryside Survey program (soil health focus; 0–15 cm topsoil).
  - Supports national and sub-national monitoring of soil condition and function across Great Britain.

- Survey design and rolling program
  - Rolling survey adopted: repeats on a five-year cycle or after 500 squares completed.
  - Sampling unit: 1-km × 1-km squares; 500 squares sampled per cycle, with 100 visited annually.
  - Stratification: based on Land Classification of Great Britain (ITE LC07) to capture environmental gradients.
  - Environmental zones: aggregates of ITE land classes (EZ_DESC_07) used to describe broad environmental settings.
  - 2019 onward: shift toward continuous rolling monitoring to detect change while accommodating climate variability.

- Covid disruption in 2020
  - Limited field access in May–June 2020; rescheduled surveys in July–August.
  - 50 squares reselected and sampled in England only due to disruptions.

- Sample collection methods
  - Within each 1-km square: five topsoil samples collected from pre-defined random locations near vegetation X-Plots (co-located with vegetation surveys).
  - Core: 15 cm long black plastic core (0–15 cm) collected at each sampling point.
  - Relocation and accuracy: post-collection relocation verified with maps, field photos, and GPS data; permanent markers introduced in prior years to aid relocation.
  - Sample handling: cores refrigerated and mailed to UKCEH laboratories; soils stored in the UKCEH Soil Bank.

- Metrics, laboratory protocols and analytical methods
  - Core data: five locations per square; soil metrics derived from fine earth (FE) or bulk soil; calculations consider stones for volumetric estimates.
  - Key measured parameters:
    - Soil pH (PH) in deionised water.
    - Loss-on-Ignition (LOI) for soil organic matter and carbon estimation (C_CONC_LOI; C_STOCK_LOI).
    - Bulk density (BULK_DENSITY) and moisture metrics (MOISTURE, MOISTURE_DRY).
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils.
    - Total nitrogen (N_PERCENT; N_STOCK).
    - Soil carbon groups (SOIL_GROUP) based on LOI categories.
    - Land classification (LC07, LC07_NUM) and country (COUNTRY).
    - Environmental Zone description (EZ_DESC_07).
  - LOI method and carbon derivations:
    - LOI determined by heating to 1000°C in four steps; organic matter estimated between 105°C and 375°C.
    - C_CONC_LOI derived from LOI; C_STOCK_LOI converted to t C ha⁻¹ using land area and bulk density.
  - Unit conventions and conversions:
    - Depth: 0.15 m core representation.
    - Area: 1 ha = 10,000 m².
    - Bulk density to kg m⁻³ (multiply by 1000 if needed).
    - Conversion from g C to tonnes C for stocks.

- Data quality assurance (QA)
  - Established data workflow with laboratory staff and data scientists using R scripts and guidance documents.
  - Field and lab QA measures:
    - pH: internal standards in each batch; acceptance within ±2 SD of batch mean; duplicates (~10%).
    - LOI: internal standards and calcite checks; batch repeat if standards deviate by >2 SD.
    - N and other chemical analyses: use of in-house reference materials; instrument calibration checks with standards and blanks.
  - Emphasis on robust QA for the rolling survey to maintain data quality across the cycle.

- Data structure and metadata
  - Dataset characteristics: 18 columns; 194 rows (topsoil 2020).
  - Missing data: denoted by -9999.
  - Core metadata fields include:
    - SQUARE: 1-km survey square identifier.
    - PLOT: soil sampling location within the square.
    - YEAR: year of sampling.
    - PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN: soil metrics with units.
    - BULK_DENSITY, MOISTURE, MOISTURE_DRY: physical properties.
    - LC07, LC07_NUM: 2007 land classification codes.
    - COUNTRY: GB country (England, Scotland, Wales).
    - EZ_DESC_07: Countryside Survey Environmental Zone description.
    - SOIL_GROUP: LOI-based soil carbon group classification.
  - Data provenance: linked to UKCEH Soils Manual and CS methods; references to Land Classification and Environmental Zones descriptions.

- Land classification, environmental zones and carbon grouping
  - ITE Land Classification (LC07) linked to 2007 classification; numeric and textual descriptors provided.
  - Countryside Survey Environmental Zones (EZ_DESC_07) derived from multivariate analyses of environmental data across squares.
  - Soil carbon groups (SOIL_GROUP) defined by LOI-based LOI categories (Mineral, Humus mineral, Organo-mineral, Organic) for carbon stock interpretation.

- End uses and applications
  - Enables mapping and analysis of topsoil condition and change at national/sub-national scales.
  - Facilitates integration with vegetation data for ecosystem-level insights.
  - Supports policy-relevant indicators and research on soil carbon, nutrient status, pH trends, moisture, and compaction signals in relation to land use and pressures.

- References and further reading
  - Includes foundational CS methodologies (Soils Manual, 2007; 2008; 2010–2020 updates), land classification frameworks, QA practices, and related soil science literature.