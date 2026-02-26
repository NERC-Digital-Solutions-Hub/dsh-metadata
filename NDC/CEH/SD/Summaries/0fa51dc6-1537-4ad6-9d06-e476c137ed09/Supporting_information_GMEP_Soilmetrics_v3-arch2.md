# Glastir Monitoring & Evaluation Programme

## Overview for Analysts Monitoring the Environment
- Purpose: Monitor the effects of the Glastir agri-environment scheme on the environment and provide evidence on soil quality outcomes related to climate, biodiversity, soil and water quality, and woodland expansion.
- Scope: Quantify both scheme-specific impacts and general soil status/trends, identifying drivers of change beyond Glastir (land use, climate, pollution).
- Data handling: Data are collected, quality assured, cleaned, and transformed into standardized outputs (e.g., reports, maps, charts) and stored/uploaded to appropriate data portals.
- Collaboration and standards: Uses established sampling methodologies to enable integration with national surveys and future cross-survey analyses.

## Study design and scope
- Monitoring framework: Glastir Monitoring and Evaluation Programme (GMEP) with a 4-year rolling survey cycle (2013–2016 as the initial cycle).
- Components:
  - Wider Wales Component: Baseline estimation, national trends, and national reporting for Glastir.
  - Targeted Component: Links directly to Glastir priority areas.
- Sampling unit: Common spatial unit of 1 km square to enable integration across scales.
- Sample size: 300 x 1 km squares over the four-year cycle; half are Wider Wales squares, half are targeted at Glastir priority areas.
- Site selection and exclusions: Square selection follows Countryside Survey GB methodology; excludes squares with >75% urban land or >90% sea.
- Confidentiality: Distribution of squares mapped at 10 km for data protection.

## Field survey methods
- Within each square: 5 randomly dispersed locations for soil sampling (where possible).
- Soil sampling: 15 cm C-core from a vegetation-survey coincident location; samples refrigerated and shipped to laboratories within a few days.
- Vegetation alignment: Sampling occurs in tandem with vegetation surveys for integrated ecosystem assessment.

## Laboratory protocols and metrics
- Primary soil metrics:
  - Soil organic matter and Loss on Ignition (LOI) with derived soil carbon concentration (C_FE_LOI and C_FE_CARBO_CONC_GPERKG).
  - Total soil carbon (SOC), nitrogen (TOTAL N), and related measurements (C_FE_CTOTAL, C_FE_NTOTAL).
  - Total phosphorus (C_FE_PTOTAL) and Olsen phosphorus (C_FE_POLSEN).
  - Soil pH (in deionised water and in CaCl2) and soil solution electrical conductivity (C_B_EC).
  - Soil bulk density (C_FE_BULK_DENSITYGPERCM3) and volumetric water content (C_FE_VWC).
  - Soil water repellency (C_FE_SWRMEDIAN) via water drop penetration time.
- Derived units and processing rationale: LOI converted to carbon concentration (multiplier 5.5) for compatibility with legacy Countryside Survey data emphasis on LOI; inorganic carbon removal prior to SOC measurement.
- Instruments and labs: CEH Lancaster (lab protocols, LOI, SOC, N, P) and CEH Bangor; individual sample weights typically ~15 mg (peat) to 15–60 mg (mineral soil).
- Data file: GMEP_SOIL_METRICS_2013_16.csv documenting 1 km square identifiers, sampling plots, grid coordinates, year, and all measured/derived metrics.

## Quality control and data integrity
- Internal standards: Two in-house soil standards per batch; repeat analyses if LOI deviates >2 standard deviations from historical means.
- Total soil carbon and nitrogen: Analyzed with accredited SOP3102 method; quality control with in-house references.
- Phosphorus: Duplicates and two matrix-matched blanks every 25 samples; results corrected via calibration curves.
- Olsen P and other measures: Similar QA/QC with duplicates and blanks every 25 samples; moisture corrections applied where relevant.
- pH and EC: Internal standards and repeats if QC criteria fail.
- Sampling and processing QA: Fixed-volume sampling sleeves; extensive field training; rigorous tracking of samples.

## Data integration, outputs, and governance
- Data integration: Design supports multi-scale ecosystem assessment; aligns with Countryside Survey GB methodology to enable future data integration across GB and constituent countries.
- Outputs: Standardised datasets, reports, maps, and charts for national and sub-national reporting; supports monitoring of Glastir outcomes and baseline trends.
- Data storage and access: Datasets stored and uploaded to appropriate data portals; QA/QC processes documented to ensure traceability and reuse.
- Teams and roles:
  - CEH staff lead and QA: GMEP Lead Scientist, QA/Database managers, laboratory managers, field coordinators.
  - Bangor University: Biodiversity science lead and work package co-supervisor.
  - Field survey teams: Multiple regional field personnel for sampling and data collection.

## Key considerations for analysts (challenges and opportunities)
- Challenge: Increase the value of monitoring datasets by integrating them with other relevant data sources beyond Glastir outputs (avoiding single-use datasets).
- Challenge: Improve access to underlying data used to create final outputs to enable broader reuse, verification, and secondary analyses.

## References and context
- Methodological foundations and supporting literature include: Land Classification of Great Britain (Bunce et al., 2007); Countryside Survey soil reports (Emmett et al., 2010); Glastir Monitoring & Evaluation Programme (First Year Annual Report, 2014); and UK soil strategies (Defra, 2009).
- Key outputs and data products are designed to be compatible with legacy datasets to facilitate long-term trend analysis and cross-survey integration.