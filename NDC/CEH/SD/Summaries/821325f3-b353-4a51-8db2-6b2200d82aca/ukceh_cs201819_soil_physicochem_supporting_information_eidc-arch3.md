# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC

- Purpose and scope
  - Documents UKCEH Countryside Survey as a national, rolling monitoring program to assess topsoil condition and function and how multiple pressures interact.
  - Supports policy scrutiny, evaluation, and informing future decisions on soil health, climate interactions, and land management.
  - Emphasizes co-located vegetation data and a framework designed for national- and sub-national indicators across GB.

- Monitoring design and rolling program
  - Rolling survey implemented in 2019 to repeat every five years or after 500 squares completed.
  - Aims to detect change over time while buffering against extreme climate years; prioritizes broad site coverage and year-on-year monitoring.
  - Sampling framework: 500 x 1-km² squares over the five-year cycle; 100 squares visited annually.
  - Stratified by Land Classification (ITE LC07) to ensure robust national and sub-national estimates.
  - Exclusion criteria: squares with >75% urban land or >90% sea excluded.

- Sample collection and field procedures
  - Within each 1-km² square, up to five sampling locations (PLOTs) with vegetation X-Plots are sampled.
  - Topsoil cores collected to 15 cm depth using a 15 cm-long core, co-located with vegetation surveys.
  - Historical sampling points tracked (1978 baseline; markers placed in 1990; resampling in 1998/2007; relocation checks in 2019).
  - Collected cores refrigerated, then shipped to UKCEH laboratories for processing and storage in the UKCEH Soil Bank.

- Metrics, laboratory protocols and analytical methods
  - Field methods and general procedures documented in the Soils Manual; five soil samples per square analyzed.
  - Key measured metrics and methods:
    - Soil pH (in deionised water) with internal QC standards and duplicates.
    - Loss-on-Ignition (LOI) for soil organic matter and derivation of soil carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI).
    - Soil bulk density (BULK_DENSITY) and porosity considerations via stone correction.
    - Gravimetric water content (MOISTURE and MOISTURE_DRY).
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils.
    - Total nitrogen (N_PERCENT; N_STOCK) via elemental analysis.
  - Unit conversions and derived calculations are specified (e.g., stock calculations per hectare).
  - Data structure: multiple interrelated fields including SQUARE, PLOT, YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN, BULK_DENSITY, MOISTURE, MOISTURE_DRY, LC07, LC07_NUM, COUNTRY, EZ_DESC_07, SOIL_GROUP; -9999 used for missing samples.

- Data quality assurance and governance
  - Robust QA workflow developed with data scientists and laboratory staff using R scripts and guidance documents.
  - Multiple QC steps embedded in laboratory analyses:
    - Internal standards and duplicate samples for pH, LOI, Olsen-P, and nitrogen analyses.
    - LOI quality control with calcite and reference materials; calibration checks for nitrogen analyses.
  - Clear documentation of data lineage, processing, and QA checks in metadata; data stored within the UKCEH Soil Bank system.
  - Data structure transparency includes explicit column definitions and units to support reproducibility and policy use.

- Environmental and classification context
  - Environmental Zones (EZ_DESC_07) derived from repeatable multivariate analyses of ITE Land Classes to reflect integrated environmental characteristics rather than single parameters.
  - ITE Land Classification (LC07 and LC07_NUM) stratify sampling across GB’s environmental gradients (climate, relief, geology).
  - Data allow examination of soil condition changes by habitat/vegetation class and by environmental zones (EZ1–EZ9) to inform regional policy and land management.

- Implications for monitoring policy and practice
  - Demonstrates a comprehensive, standardized approach to monitoring soil health at national scales with rolling reassessments.
  - Enables assessment of interactions between pressures (deposition, management changes, climate) on topsoil condition and carbon/nitrogen dynamics.
  - Highlights the importance of metadata, data sharing readiness, and governance to ensure datasets meet openness and quality standards for policy use.

- References and context
  - Documents and related literature cited include Countryside Survey methods, soils manuals, land classification frameworks, and prior national soil-change analyses, underpinning the monitoring framework and QA procedures.