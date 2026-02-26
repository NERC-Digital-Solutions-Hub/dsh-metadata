# State tagging application for environmental data quality assurance

## Overview
- An implementation of the state tagging approach to improve quality assurance for environmental data.
- Returns state-dependent prediction intervals on data (e.g., moth data).
- States are determined by clustering auxiliary data (e.g., meteorological data) from the same day.
- Applicable to any point-based daily time series observational data.
- Users upload two CSV files: one for state variables and one for observations.

## How to run
- Requires R and the necessary R packages.
- Run as a Shiny app: copy/app.R into the R terminal and run, or open app.R in RStudio and click Run App.
- Optional online hosting available; reference deployment resources for Shiny apps.
- For testing, refer to session_info.txt.

## Data inputs
- Acceptable CSV formats:
  - One observation per line: columns DATE, FIELDNAME, VALUE (other columns ignored).
  - Tidy/panel/tabular: DATE is required; other columns treated as field names.
- Dates should be in a non-trivial format, e.g., YYYY-MM-DD.
- After uploading, press Analyze to proceed to the next tab.

## Example data
- Example state data: MIDAS data at Carlisle (Met Office, 2012).
  - Access: Met Office MIDAS data catalog.
- Example observation data: Data from an automatic water monitoring buoy (Blelham Tarn, 2008–2011).
  - Access: CEH data catalogue.
- Sample format:
  - Columns: DATE, FIELDNAME, VALUE, sign_if_LT_LOD, flag
  - Example rows provided in the documentation.

## State tagging workflow
- Upload two CSV files (state variables and observations).
- Use the Analyze function to generate state tags and contextual QA information.
- The interface includes steps and visual elements to guide the tagging process (as illustrated in the documentation).

## Deployment
- A live deployment of the application is available at:
  - https://statetag-generic.datalabs.ceh.ac.uk/

## Access, licensing, and citation
- Code is accessible at: https://doi.org/10.5285/1de712d3-081e-4b44-b880-b6a1ebf9fcd8
- Licensed under the Open Government Licence.
- Please cite: Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance. Environmental Information Data Centre. https://doi.org/10.5285/1de712d3-081e-4b44-b880b6a1ebf9fcd8

## References
- Jones, I.; Feuchtmayr, H. (2017). Data from automatic water monitoring buoy from Blelham Tarn, 2008 to 2011. NERC Environmental Information Data Centre.
- Met Office (2012): Met Office Integrated Data Archive System (MIDAS) Land and Marine Surface Stations Data (1853-current).
- Tso, C.-H. M.; Henrys, P.; Rennie, S.; Watkins, J. (2020). State tagging for improved earth and environmental data quality assurance. Frontiers in Environmental Science.