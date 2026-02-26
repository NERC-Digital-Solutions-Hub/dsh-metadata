# NERC Soil Biodiversity Thematic Programme: Meteorological Data from Sourhope (1999-2002)

## Overview
- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biodiversity and the functional roles of soil organisms within key ecological processes at Sourhope, Scottish Borders.
- 24 projects funded to study soil structure, processes (e.g., carbon and nitrogen cycles), and roles of micro-, meso-, and macro-fauna.
- Meteorological data were collected from an on-site Automatic Weather Station (AWS) between February 1999 and September 2002 and regularly downloaded to support ecological analyses.

## Data Description and Structure
- Data source: On-site AWS at the Sourhope experimental plots; hourly summaries derived from 5-second samples.
- Primary data asset: CHA_Sourhope_AWS_1999_2002.csv.
- Key fields include:
  - EXPERIMENT_ID and Description (AWS)
  - AWS_DATE (date) and AWS_TIME (time)
  - RAINFALL (mm)
  - WIND_SPEED (m/s) and WIND_DIRECTION (degrees)
  - AIR_TEMP (°C)
  - SOIL_TEMP_2CM, SOIL_TEMP_MINUS_2CM, SOIL_TEMP_MINUS_5CM, SOIL_TEMP_MINUS_10CM, SOIL_TEMP_MINUS_30CM (each in °C)
  - SOIL_MOISTURE (m3/m3)
- Data governance and QA:
  - Quality control included numeric range checks, formatting checks, and logical integrity checks.
  - Data are subject to quality assurance but not guaranteed for accuracy or fitness for purpose; no liability is assumed by NERC for data use.

## Data Management and Access
- Stewardship: Managed by the Soil Biodiversity Data Manager at the Centre for Ecology & Hydrology (CEH).
- Data handling: Regular downloads and transmission to CEH for curation and dissemination.
- Context: Part of a broader programme to integrate biological soil biodiversity data with environmental (meteorological) context.

## Relevance for Data Leaders

- Data asset mapping and discoverability
  - Metadata is embedded in the dataset description (columns, units, and variable definitions), aiding discoverability and interpretation.
  - Clear dataset naming (CHA_Sourhope_AWS_1999_2002.csv) supports versioning and provenance tracking.

- Data quality and governance
  - Explicit QA processes are described, though accuracy and fitness-for-use are not warranted, highlighting the need for explicit data provenance, limitations, and risk disclosures in data products.
  - Governance by a dedicated data manager demonstrates established stewardship, suggesting a model for cross-project data stewardship and accountability.

- Data integration and interoperability
  - Rich meteorological variables (temperature, rainfall, wind, soil temperatures at multiple depths, soil moisture) provide a solid basis for integrating climate context with soil biodiversity analyses.
  - Standardized units and definitions for fields facilitate interoperability with other ecological and environmental datasets.

- Data strategy and capability for data leaders
  - Emphasizes comprehensive metadata, clear data quality practices, and explicit usage constraints as foundational elements of a robust data strategy.
  - Highlights potential challenges for data leaders: ensuring data accuracy, managing expectations about data fitness for purpose, and maintaining discoverability across dispersed geo-located datasets.

- Practical considerations and risks
  - Access and liability limitations require clear communication of data limitations to end users.
  - Temporal scope (1999-2002) may necessitate integration with newer datasets for longitudinal analyses; ongoing stewardship is essential for continuity.

## Takeaways
- The Sourhope AWS dataset exemplifies how a well-governed data asset, with defined variables, units, and quality checks, can support larger data ecosystems linking environmental context to soil biodiversity research.
- For data leadership: prioritize robust metadata, transparent quality controls and limitations, clear stewardship roles, and strategies for data integration and discoverability across networks of datasets.