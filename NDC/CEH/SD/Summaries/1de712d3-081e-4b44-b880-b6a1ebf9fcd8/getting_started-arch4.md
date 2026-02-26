# State tagging application for environmental data quality assurance

- Overview
  - An implementation of a state tagging approach to improve quality assurance for environmental data.
  - The app returns state-dependent prediction intervals for daily time-series observations.
  - States are determined by clustering auxiliary data (e.g., same-day Met data).
  - Applicable to any point-based daily time series; suitable for enhancing data quality assessment and contextual interpretation.

- How it works
  - Users upload two CSV files: one with state variables and one with observations.
  - The tagging provides contextual quality information to assess observational data quality across daily states.
  - Outputs support data governance by adding interpretable QA context to data streams.

- Running the app
  - Requires R and the necessary R packages.
  - Run by pasting the app.R contents into R or using RStudio's Run App.
  - Optional online hosting via Shiny deployment; testing information available in session_info.txt.

- Data inputs and formats
  - Acceptable CSV formats:
    - One observation per line: columns DATE, FIELDNAME, VALUE (other columns ignored).
    - Tidy/Panel/Tabular: DATE column plus other columns treated as fieldnames.
  - Dates should be specified in a non-trivial format (e.g., YYYY-MM-DD).
  - After uploading, click Analyze to proceed.

- Example data sources
  - Example state data: MIDAS data at Carlisle (Met Office, 2012). Download link provided.
  - Example observation data: Data from automatic water monitoring buoy at Blelham Tarn, 2008–2011 (Jones & Feuchtmayr, 2017). Access links provided.
  - Data sample format includes: DATE, FIELDNAME, VALUE, sign_if_LT_LOD, flag.

- Deployment and usage
  - Illustration deployment available: https://statetag-generic.datalabs.ceh.ac.uk/ (as of 2020-04-22).
  - Screenshots describe the UI for using the app’s elements and running state tagging.

- Licensing and citation
  - Code is released under the Open Government Licence; no warranty.
  - Please cite:
    - Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance. Environmental Information Data Centre. https://doi.org/10.5285/1de712d3-081e-4b44-b880-b6a1ebf9fcd8
    - Tso, C.-H. M.; Henrys, P; Rennie, S.; Watkins, J. (2020) State tagging for improved earth and environmental data quality assurance. Frontiers in Environmental Science. https://doi.org/10.3389/fenvs.2020.00046
  - Data sources referenced in the app (datasets) are also cited in the document.

- References
  - Jones, I.; Feuchtmayr, H. (2017). Data from automatic water monitoring buoy from Blelham Tarn, 2008 to 2011. NERC Environmental Information Data Centre. https://doi.org/10.5285/38f382d6-e39e-4e6d-9951-1f5aa04a1a8c
  - Met Office (2012): Met Office Integrated Data Archive System (MIDAS) Land and Marine Surface Stations Data (1853-current). NCAS British Atmospheric Data Centre. http://catalogue.ceda.ac.uk/uuid/220a65615218d5c9cc9e4785a3234bd0
  - Tso, C.-H. M.; Henrys, P.; Rennie, S.; Watkins, J. (2020). State tagging for improved earth and environmental data quality assurance. Frontiers in Environmental Science. https://doi.org/10.3389/fenvs.2020.00046