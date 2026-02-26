# Clocaenog_supporting documentation_Fortnightly measurements.rft

## Purpose of the document
- Provides a supplement to the supporting documentation for data series describing Fortnightly measurements at Clocaenog (2015-2016).
- Details the data structure for two datasets and how they were collected together.

## Datasets described
- Data were collected together and comprise two related datasets:
  1) Fortnightly measurements_Clocaenog_2015-2016_site.csv
  2) Fortnightly measurements_Clocaenog_2015-2016_soil respiration.csv

## Dataset 1: Fortnightly measurements_Clocaenog_2015-2016_site.csv
- Structure: 20 columns, 32 rows
- Content:
  - Date (fortnightly time points; Day/Month/Year)
  - Rainfall (mm) – site level
  - Throughfall measurements across plots (Plot1–Plot9) with different treatments (Warming, Control, Drought)
  - Water table depth measurements for plots (labels indicate different treatment plots)
- Notes on units and labeling:
  - Rainfall and Throughfall are listed with mm units
  - Water table depth entries are described with both cm and mm units across different columns, indicating potential inconsistencies in unit labeling that may require clarification in metadata
- Data purpose:
  - Captures site-level hydrology and moisture inputs across multiple treatment plots over time

## Dataset 2: Fortnightly measurements_Clocaenog_2015-2016_soil respiration.csv
- Structure: 38 columns, 32 rows
- Content:
  - Date (fortnightly time points)
  - Soil respiration measurements (Plot1–Plot9) associated with treatments (Warming, Control, Drought)
  - Soil temperature measurements (Plot1–Plot9) in degrees Celsius
  - Soil moisture measurements (Plot1–Plot9) in Vol%
  - Photosynthetic active radiation (PAR) measurements (Plot1–Plot9) in µmol m⁻² s⁻¹
- Notes on organization:
  - Variables are grouped by measurement type (soil respiration, soil temperature, soil moisture, PAR) and by plot with treatment labels
- Data purpose:
  - Provides a multivariate view of below-ground respiratory activity and associated environmental drivers across treatments and plots over time

## Metadata and data quality considerations
- Metadata richness:
  - The headers describe variable names, units, and descriptions for each column, aiding interpretability
- Potential data quality issues to address in a monitoring framework:
  - Inconsistent or unclear unit labeling for water table depth (cm vs. mm) in Dataset 1
  - Need for standardized metadata to ensure consistent interpretation across datasets
  - Fortnightly cadence and 32 rows imply a defined time span; confirm exact date range and alignment between datasets
- Data governance implications:
  - The document underscores the importance of metadata and data sharing, which can be barriers if datasets are not openly accessible or properly documented
  - Ensuring data are quality assured, cleaned, transformed, and accompanied by clear documentation will support reuse in monitoring frameworks

## Relevance for monitoring frameworks
- The datasets exemplify structured, plot-level long-term environmental monitoring with experimental treatments (Warming, Drought, Control)
- Key measures captured align with environmental health monitoring needs:
  - Hydrology: rainfall, throughfall, water table depth
  - Soil processes: soil respiration
  - Soil environment: soil temperature, soil moisture
  - Light environment: photosynthetically active radiation
- The integrated structure supports analysis of treatment effects over time and across environmental conditions

## Implications for future data handling
- Prioritize consistent units and clear metadata to facilitate data sharing and interoperability
- Maintain explicit documentation of treatment plots and their assignments to support reproducibility
- Ensure datasets are linked to supporting documentation and data governance protocols to ease use in monitoring frameworks and decision-making contexts