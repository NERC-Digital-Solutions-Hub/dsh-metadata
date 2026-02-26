# UKCEH Countryside Survey QA metadata and analysis report CS 2020 - EIDC Topsoil physico-chemical data 2020

- Purpose and context
  - Countryside Survey is a long-running national audit of UK countryside resources, enabling trend detection in soil condition and function since 1978.
  - The 2019 rollout introduces a rolling monitoring program to quantify direction and magnitude of soil changes and to assess interactions between multiple pressures.
  - Focus of this dataset: topsoil (0–15 cm) condition and related vegetation context, with data intended to inform policy and scientific understanding of soil health, carbon dynamics, nutrients, and management impacts.

- Survey design and rolling program
  - Rolling survey: 500 1-km squares sampled over a five-year cycle, with 100 squares visited each year.
  - Squares stratified within Land Classification (ITE) 2007 framework; excludes urban-dominated or sea-dominated squares.
  - Sampling framework supports national and sub-national indicators with repeatable estimates across GB.
  - 2020 disruption due to Covid-19; 50 England-only squares were added to mitigate access issues.

- Sampling and field methods
  - Within each square: up to five sampling locations (X-Plots) for soils and vegetation.
  - Topsoil cores collected at ~15 cm depth using a 15 cm long core from predefined locations, co-located with vegetation plots.
  - Soil samples are refrigerated and sent to UKCEH laboratories; soil cores stored in the UKCEH Soil Bank.

- Metrics, laboratory protocols and analyses
  - Core soil metrics (0–15 cm fine earth fraction) include:
    - pH in deionized water (PH)
    - Loss-on-Ignition (LOI) to derive soil organic matter and carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
    - Bulk density (BULK_DENSITY) and moisture contents (MOISTURE, MOISTURE_DRY)
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland lands
    - Total nitrogen (N_PERCENT) and nitrogen stock (N_STOCK)
    - Derived soil carbon and nitrogen stocks per hectare
  - Land classification and environmental zone metadata accompany soil measurements (LC07, LC07_NUM; EZ_DESC_07)
  - Soil groupings based on LOI (SOIL_GROUP) categorize soils into Mineral, Humus mineral, Organo-mineral, and Organic.
  - Units and conversions are defined (e.g., 0.15 m depth for representative core; 1 ha = 10,000 m2).

- Quality assurance and quality control
  - QA framework implemented via a robust data workflow with R scripts and guidance documents to ensure high data quality.
  - pH QA: internal standards and duplicates; acceptance within ±2 SD of batch mean.
  - LOI QA: internal LOI standards and calcite checks; batch-level QC with ≤2 SD deviation for internal standards.
  - N (%), PO4, and other measurements include in-house reference materials and blanks for routine QC.
  - Emphasis on traceability, calibration checks, and data corrections against standards.

- Data structure and metadata
  - Dataset comprises 18 columns and 194 rows; missing values denoted by -9999.
  - Key fields include SQUARE (1-km square ID), PLOT (soil sampling location within square), YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN, BULK_DENSITY, MOISTURE, MOISTURE_DRY, SOIL_GROUP, LC07, LC07_NUM, COUNTRY, EZ_DESC_07.
  - Data quality and provenance are documented, with mapping to Land Classification (2007) and Environmental Zones for interpretability across scales.

- Data access and governance
  - Data stored in the UKCEH Soil Bank; intended for use in soil monitoring and policy-relevant analyses.
  - Contact information and institutional channels provided for data inquiries and access permissions.
  - Document cites standard soil analysis methodologies and previously published Countryside Survey reports and manuals to support methodological transparency.

- References and context
  - Aligns with foundational Countryside Survey methodologies (Soils Manual; 2007 CS reports), and related soil science procedures for LOI, pH, bulk density, and nutrient analyses.
  - Supported by CEH/NERC programs and prior national soil-change research linking soil metrics to ecosystem services and policy-relevant indicators.