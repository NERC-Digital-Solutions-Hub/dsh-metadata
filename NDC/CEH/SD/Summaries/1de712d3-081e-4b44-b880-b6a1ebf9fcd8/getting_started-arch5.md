# State tagging application for environmental data quality assurance

- Code access and licensing
  - Code available at https://doi.org/10.5285/1de712d3-081e-4b44-b880-b6a1ebf9fcd8
  - Licensed under the Open Government Licence; no warranty or guarantee of fitness for a particular purpose
  - Please cite: Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance

- Purpose
  - Implements a state tagging approach to improve quality assurance for environmental data
  - Produces state-dependent prediction intervals for observations (e.g., moth data)
  - States are determined by clustering auxiliary data from the same day (e.g., met data)
  - Applicable to any point-based daily time series observational data
  - Users upload two CSV files: one with state variables and one with observations

- Running the app
  - Requires R and required R packages
  - Run options: paste app.R into R terminal, or open in RStudio and click Run App
  - can be hosted online; deployment guidance available via Shiny documentation
  - For testing, a session_info file is provided

- Data upload
  - Accepted CSV formats:
    - One observation per line: columns DATE, FIELDNAME, VALUE (others ignored)
    - Tidy/Panel/Tabular: DATE column; other columns treated as fieldnames
  - Dates must be in non-trivial formats (e.g., YYYY-MM-DD)
  - After uploading, press Analyze to proceed to the next tab

- Example data
  - Example state data source: MIDAS data at Carlisle (Met Office, 2012)
  - Example observation data source: automatic water monitoring buoy data (Blelham Tarn, 2008–2011)
  - Example data snippets include DATE, TEMP, VALUE and related quality/flag fields

- Perform state tagging
  - Screenshots illustrate how to use the app’s UI elements to perform tagging
  - Workflow is guided by the app’s interface after data upload

- Illustration deployment
  - Deployment of the application available at https://statetag-generic.datalabs.ceh.ac.uk/ (as of 2020)

- References and data sources
  - Jones, I.; Feuchtmayr, H. (2017) Data from automatic water monitoring buoy from Blelham Tarn, 2008 to 2011
  - Met Office (2012) MIDAS data archive
  - Tso, C.-H. M.; Henrys, P.; Rennie, S.; Watkins, J. (2020) State tagging for improved earth and environmental data quality assurance