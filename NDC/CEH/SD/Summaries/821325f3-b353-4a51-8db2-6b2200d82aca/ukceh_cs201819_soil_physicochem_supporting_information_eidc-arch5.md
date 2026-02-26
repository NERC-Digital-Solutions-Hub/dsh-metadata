# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC
Topsoil physico-chemical data 2018/2019

- Purpose and scope
  - Document QA metadata and analytical data for topsoil (0–15 cm) from the UKCEH Countryside Survey (CS) for 2018/2019, as part of a rolling national soil-monitoring program.
  - Supports long-term assessment of soil condition and function across Great Britain, with emphasis on traceable change over time and integration with vegetation data.
  - Data are prepared for publication and archiving within the UKCEH data infrastructure (Soil Bank) and the Environmental Information Data Centre (EIDC).

- Study design and rolling program
  - Countryside Survey is a national audit of countryside resources, conducted since 1978, now operating as a rolling program to monitor soil and vegetation changes.
  - Rolling cycle: 500 1-km2 squares sampled per cycle, completed over five years; 100 squares visited annually.
  - Sampling frames are stratified by Land Classification (ITE LC07) and environmental zones; urban (>75% urban) or sea (>90% sea) exclusions apply.
  - Rolling design buffers against climate variability and aims to maximize site coverage while enabling year-on-year trend detection.

- Sample collection methods
  - Within each 1-km2 square, five topsoil samples are collected from defined locations aligned with vegetation X-Plots, using a 15 cm long core.
  - Sampling locations and plots are linked to historical CS plots with relocation verification (maps, GPS, photos).
  - Core samples are refrigerated and shipped to UKCEH laboratories for processing; soil sampling year recorded for each square and plot.

- Metrics, laboratory protocols and analytical methods
  - Fields captured in the dataset include: SQUARE (1-km square ID), PLOT (soil sampling location), YEAR, PH (soil pH in water), LOI (loss on ignition), C_CONC_LOI (soil carbon concentration from LOI), C_STOCK_LOI (carbon stock per area), SOIL_GROUP, BULK_DENSITY, MOISTURE, MOISTURE_DRY, N_PERCENT, N_STOCK, PO4_OLSEN, LC07, COUNTRY, EZ_DESC_07.
  - LOI-derived metrics enable calculation of soil organic matter and carbon stocks; carbon stock calculations consider depth, bulk density, and area per hectare.
  - Measurements include:
    - Soil pH (in deionized water) with internal standards and duplicates for QA.
    - LOI measured by ThermoGravimetric Analysis (TGA701) with a four-step heating protocol to quantify organic matter and derive C_CONC_LOI and N_STOCK.
    - Bulk density and porosity calculations using the 15 cm core, accounting for stones.
    - Gravimetric moisture content (MOISTURE and MOISTURE_DRY).
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils; colorimetric analysis with quality controls.
    - Total nitrogen (N_PERCENT) via an elemental analyzer (oxidative combustion) with calibration against in-house references.
  - Units and conversions are documented (e.g., 0.15 m sampling depth, 1 ha = 10,000 m2, density conversions, LOI to carbon factors).

- Quality assurance and data governance
  - Robust QA workflow developed by UKCEH laboratory staff and data scientists, implemented via R-based processes and guidance documents.
  - QA measures include:
    - Internal standards and duplicates for pH and LOI runs; batch acceptance criteria based on standard deviations.
    - LOI quality control using internal standards and calcite checks; 2 standard deviations tolerance.
    - Two in-house reference materials per batch for nitrogen analyses; calibration checks with a known standard (Acetanilide).
    - Regular instrument calibration and blank/duplicate checks for Olsen-P analyses.
  - Data are stored and curated within UKCEH’s Soil Bank; data processing pipelines ensure consistency across years and rolling cycles.
  - Documentation and references provide methodological context (Soils Manual and associated CS reports).

- Data structure, completeness and access
  - Dataset structure: 18 columns, 562 rows; missing samples denoted by -9999.
  - Core metadata fields include: SQUARE (1-km square ID), PLOT (soil sampling location), YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN, BULK_DENSITY, MOISTURE, MOISTURE_DRY, LC07, LC07_NUM, COUNTRY, EZ_DESC_07, SOIL_GROUP.
  - Environmental classifications:
    - EZ_DESC_07 (UKCEH Countryside Survey Environmental Zone descriptions) derived from ITE Land Classification (2007).
    - Soil_GROUP categorizes soils by LOI-based carbon content into Mineral, Humus Mineral, Organo-mineral, and Organic groups.
  - Data accessibility and contact:
    - QA metadata and data are appropriate for archiving in EIDC; contact CEH or UKCEH Soil Bank for access (uksoilbank@ceh.ac.uk) and inquiries.
    - Supporting references and external documentation are available (Soil Bank, Countryside Survey methodological documents, and related CEH/NERC resources).

- Environmental classifications and data products
  - ITE Land Classification (LC07) and related numeric codes used to stratify sampling and enable habitat- or vegetation-class-based analyses.
  - Environmental Zones (EZ_DESC_07) summarize environmental contexts across GB and support cross-scenario comparisons.
  - Carbon groups (SOIL_GROUP) provide a framework for comparing soil carbon stocks across sampled sites.

- Practical implications for data stewardship
  - Rolling program design improves temporal sensitivity but requires ongoing standardization of sampling, relocation verification, and QA across years.
  - Integration with vegetation data and cross-dataset compatibility (land classes, environmental zones) is essential for multi-metric ecosystem assessments.
  - Data management should maintain clear provenance (sampling year, plot, location, laboratory methods) and robust metadata to support reuse and reproducibility.
  - Timely data sharing and documentation updates are needed to reflect rolling-cycle progress and methodological updates (e.g., COVID-19 disruptions mentioned in the design section).

- References and further reading (contextual)
  - Soils Manual and CS technical reports underpin QA protocols and laboratory methods.
  - Key sources include Emmett et al. (2008, 2010), Reynolds et al. (2013), Bunce et al. (2007), and related CS datasets and methodological documentation.