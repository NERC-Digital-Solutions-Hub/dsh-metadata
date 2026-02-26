# Details of data structure to 'Digestate_NF_SoilTemperature_WFPS.csv'

- Overview
  - Supplement to supporting documentation for data series referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
  - Dataset from a digestate-treated wheat trial (2017) conducted at North Wyke Research station, with Rothamsted Research involvement.
  - Focuses on soil conditions: soil temperature and water-filled pore space (WFPS) at a shallow depth (2.5 cm).
  - Contains data for ten plots collected across blocks, enabling temporal soil moisture and temperature monitoring.

- Dataset contents
  - Rows: 31,778
  - Columns: 4
  - Time coverage: Date and time of day
  - Block: Categorical indicator values 1 to 5
  - Soil_Temperature_degrees_celcius: numeric, Celsius
  - WFPS_percent: numeric, percent

- Data structure details
  - Time: Date and time of day specifying when measurements were taken
  - Block: Indicates a grouping of measurements (Blocks 1–5)
  - Soil_Temperature_degrees_celcius: Soil temperature at 2.5 cm depth
  - WFPS_percent: Water-filled pore space at 2.5 cm soil depth

- Provenance and collection context
  - Origin: Digestate experiment data from the wheat trial conducted in 2017
  - Location: North Wyke Research station (and collaboration with Rothamsted Research)
  - Purpose within the data lineage: Part of a broader set of data series with supporting documentation; the current file provides structural details for the Digestate_NF_SoilTemperature_WFPS.csv dataset

- Relevance for monitoring frameworks
  - Provides key environmental health indicators (soil temperature and soil moisture) at a shallow soil depth, useful for monitoring soil health, agronomic conditions, and the effects of digestate treatments.
  - Enables cross-sectional and temporal analyses across multiple blocks/plots for policy and management decision support.

- Data quality, metadata, and governance considerations
  - Metadata completeness is not fully described in this supplement; it may require review against the broader supporting documentation.
  - Data may require cleaning or transformation to ensure consistent units and formats across time points and blocks.
  - Public sharing of underlying data is a potential governance consideration; ensure provenance, versioning, and access controls align with data governance standards.

- Access and dissemination notes
  - Supplementary to the main documentation; full interpretation benefits from consulting Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
  - This file provides the structural schema (column headers, units, and meanings) needed to integrate the dataset into monitoring dashboards or reports.