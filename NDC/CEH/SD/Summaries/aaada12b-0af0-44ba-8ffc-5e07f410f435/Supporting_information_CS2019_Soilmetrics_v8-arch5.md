# Countryside Survey: Soils Metrics 2019

## Overview
- UK Countryside Survey provides a rolling, longitudinal assessment of soil and vegetation across Great Britain, enabling comparisons with past surveys since 1978.
- The 2019 survey marks the start of a rolling programme (UKCEH-CS) to monitor soil condition and change, supported by NERC under UK-SCAPE.
- Primary aim: quantify direction and magnitude of soil change and how multiple pressures interact to shape soil condition and function, with data intended to inform understanding of soil health, carbon dynamics, and related ecosystem services.

## Design and Rolling Program
- Rolling survey with a five-year cycle, sampling 500 1km squares in total, with 100 squares visited per year.
- Stratified sampling based on the Land Classification of Great Britain; aims to balance national and sub-national estimates.
- Exclusions: squares with more than 75% urban land or more than 90% sea are excluded.
- The sampling framework builds on the 1978, 1998, and 2007 CS designs to enable long-term trend detection.
- Within each annual square, soil samples are taken from five randomly dispersed locations, accompanied by vegetation X-Plots.

## Sampling and Sample Collection
- Annual program visits 100 x 1km squares; within each square, five soil samples are collected from 0–15 cm using a 15 cm C-core from predetermined random locations.
- Historic sampling locations are maintained via maps and markers to allow relocation across survey cycles (1978, 1990, 1998, 2007, 2019); plots were adjusted over time to maintain comparability.
- After collection, soils are refrigerated and mailed to laboratories (UKCEH, Bangor) for analysis.

## Laboratory Analyses and Metrics
- Field/Laboratory Protocols:
  - Land classification: ITE Land Classification 2007 basis for stratifying sites.
  - Soil carbon groups based on loss on ignition (LOI) with four categories (mineral, humus mineral, organo-mineral, organic soils).
  - Depth of peaty organic layers is recorded to classify peat status (peaty horizons defined up to 40 cm with broader groupings for peat).
  - Soil pH measured in deionised water and in CaCl2; EC measured in DIW extract.
- Key soil metrics measured:
  - LOI, hygroscopic water content, CaCO3; derivation of soil organic carbon (SOC) from LOI with a conversion factor aligned to legacy 2007 CS methods.
  - Bulk density, porosity, particle density, and related soil physical properties to support carbon stock calculations.
  - Olsen phosphorus, total phosphorus (TP), total soil organic carbon (SOC) and total nitrogen (TN) using standardized digestion and analysis protocols.
  - Derived indices such as CN ratio and carbon stocks per hectare (tC/ha) using bulk density and soil carbon concentration.
- Quality Control:
  - Internal standards and duplicates included in batches; acceptance criteria set around standard deviations and recovery rates.
  - CaCO3 recovery target 95–100%; LOI quality checks with internal standards; regular instrument calibration and reference materials (including Acetanilide standards) used to validate measurements.

## Data Structure and Metadata
- Core dataset: UKCEHCS_SOIL_METRICS_2019.csv with -9999 indicating missing samples.
- Key fields include:
  - SQ_ID (1km square identifier), PLOT_ID (X-plot), YEAR, LC07 (ITE Land Classification), habitat descriptors, depth measures (Average_O_depth), LOI-based groupings (SOIL_GP_LOI_CS_1_4, SOIL_GP_1_3, SOIL_GP_1_5), pH measures (C_B_PH_DIW, C_B_PH_CACL2), EC (C_B_EC), moisture and LOI (C_FE_MOISTURE_HYGRO, C_FE_LOI), calcite (C_FE_CACO3), bulk density (C_FE_BULK_DENSITYGPERCM3), porosity (C_FE_POROSITY), stone content (C_FE_MASSSTONES, C_FE_VOLSTONES), gravimetric and volumetric water contents (C_FE_GWC_D, C_FE_GWC_W, C_FE_VWC), Olsen-P (C_FE_POLSEN), total P (C_FE_PTOTAL), total C (C_FE_CTOTAL), total N (C_FE_NTOTAL), CN ratio (CN_RATIO_FE), and derived C per kg and per hectare values.
- Data are designed to support rolling, time-series analysis of soil change, enabling population-level and site-level trend assessments.

## Quality Control and Data Integrity
- Ensures data reliability through:
  - Internal standards and duplicates in each batch.
  - Calibration verifications and use of reference materials across runs.
  - Monitoring recovery, precision, and reproducibility (e.g., CaCO3, LOI, and Olsen-P checks every 25 samples).
- Data processing and conversions are aligned with legacy CS methodologies to maintain comparability with earlier surveys (e.g., LOI-based SOC conversions and units).

## Data Management, Access, and Reuse
- Data management led by UK Centre for Ecology & Hydrology (UKCEH) with dedicated staff for data management, lab processing, analysis, archiving, and field operations.
- Data are integrated into a rolling program framework and linked with accompanying vegetation data for broader ecosystem analyses.
- Outputs include the 2019 soil metrics dataset and summary figures illustrating soil organic matter trends, pH changes, and relationships among LOI, porosity, bulk density, and other properties.
- References and methodologies are documented in a wide set of CS reports and papers to facilitate reproducibility and cross-study integration.

## Implications for Data Stewards
- This dataset exemplifies long-term, standardized data governance across changing methodologies and site relocations, emphasizing:
  - Robust sampling design with clear provenance and relocation markers for comparability across cycles.
  - Comprehensive metadata and documentation of laboratory protocols, quality controls, and data derivations.
  - Alignment with legacy CS methods to ensure temporal continuity and interoperability with historical data.
  - Transparent data structure with explicit field definitions, units, and handling of missing data.
  - Ongoing data quality assurance, archival practices, and cross-dataset integration (e.g., coupling with vegetation datasets).
- Challenges highlighted (and relevant to stewardship):
  - Maintaining timeliness and consistency across decades and multiple field teams.
  - Integrating data from diverse systems and ensuring interoperability with legacy datasets.
  - Managing large, multi-metric datasets, including derived variables and unit conversions for stock assessments.