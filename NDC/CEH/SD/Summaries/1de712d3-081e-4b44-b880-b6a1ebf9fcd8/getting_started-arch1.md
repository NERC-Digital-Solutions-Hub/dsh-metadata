# State tagging application for environmental data quality assurance

- Purpose: An implementation of state tagging to improve quality assurance for environmental data. The app provides state-dependent prediction intervals for observations (e.g., moth data) by determining states through clustering of auxiliary data (e.g., same-day meteorological data). Applicable to any point-based daily time series. Users upload two CSV files: one with state variables and one with observations.

- Code access and citation:
  - Code available at https://doi.org/10.5285/1de712d3-081e-4b44-b880-b6a1ebf9fcd8
  - Licensed under the Open Government Licence; no warranty or fitness implied.
  - Cite: Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance.

- Running the app:
  - Requires R and specified packages; run as a Shiny app (paste app.R in R terminal or use RStudio’s Run App).
  - Options to host online; guidance available via Shiny ecosystem.
  - For testing, reference session_info.txt.

- Data upload (4.1):
  - Acceptable CSV formats:
    - One observation per line: columns DATE, FIELDNAME, VALUE (other columns ignored).
    - Tidy/Panel/Tabular: DATE column plus other columns as fieldnames.
  - Dates should be in non-trivial formats (e.g., YYYY-MM-DD).
  - After uploading, press Analyze to proceed.

- Example data (4.2):
  - State data: MIDAS data at Carlisle (Met Office, 2012).
  - Observation data: Data from automatic water monitoring buoy at Blelham Tarn (2008–2011).
  - Example data include sample rows with DATE, FIELDNAME, VALUE, sign_if_LT_LOD, flag.
  - Access to example datasets and related metadata via provided URLs.

- Perform state tagging (4.3):
  - The app provides a guided UI to perform state tagging, including interaction with uploaded data and interpretation of results (screenshots describe the workflow).

- Illustration deployment (4.4):
  - Deployment of the application accessible at https://statetag-generic.datalabs.ceh.ac.uk/ (as of the referenced date).

- References and data sources:
  - Data sources include MIDAS (Met Office), and the Blelham Tarn buoy dataset.
  - Related methodological reference: Tso, C.-H. M.; Henrys, P; Rennie, S.; Watkins, J. (2020) State tagging for improved earth and environmental data quality assurance. Frontiers in Environmental Science.