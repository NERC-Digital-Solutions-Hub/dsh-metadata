# State tagging application for environmental data quality assurance

## Aim
- Implement a state tagging approach to improve quality assurance for environmental data.
- Provide state-dependent prediction intervals; states are determined by clustering auxiliary data from the same day (e.g., meteorological data).
- Applicable to any point-based daily time series observational data.
- Users upload two separate CSV files: one for state variables and one for observations.

## How it helps analysts
- Adds contextual information to assess observational data quality beyond single outputs.
- Facilitates improved data reliability for monitoring and policy evaluation.
- Encourages re-use and potential combination with other relevant datasets.

## Running the app
- Requires R and the necessary R packages.
- Run by copying app.R into R or using RStudio and clicking Run App.
- Optional online hosting via Shiny deployment; refer to Shiny docs for deployment.

## Data upload requirements
- Acceptable CSV formats:
  - One observation per line: columns DATE, FIELDNAME, VALUE; other columns ignored.
  - Tidy/Panel/Tabular: DATE column plus other columns treated as fieldnames.
- Dates should be in non-trivial formats (e.g., YYYY-MM-DD).
- After uploading, click Analyze to proceed to the next tab.

## Example data
- State data example: MIDAS data at Carlisle (Met Office, 2012).
  - Source: Met Office MIDAS dataset.
- Observation data example: Automatic water monitoring buoy data from Blelham Tarn, 2008–2011 (Jones & Feuchtmayr, 2017).
  - Source: CEH Environmental Information Data Centre.
- Example data snippet includes columns such as DATE, FIELDNAME, VALUE, sign_if_LT_LOD, flag.

## State tagging in practice
- The app provides an interface (screenshots referenced) to perform state tagging and visualize state-based QA outputs.

## Deployment and access
- A deployment of the application is available at: https://statetag-generic.datalabs.ceh.ac.uk/ (as of 2020-04-22).

## Licensing, citation, and references
- Code is available under the Open Government Licence at the provided DOI.
- No warranty; citation recommended: Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance. Environmental Information Data Centre. https://doi.org/10.5285/1de712d3-081e-4b44-b880-b6a1ebf9fcd8
- Primary related publications:
  - Tso, C.-H. M.; Henrys, P.; Rennie, S.; Watkins, J. (2020). State tagging for improved earth and environmental data quality assurance. Frontiers in Environmental Science. https://doi.org/10.3389/fenvs.2020.00046
  - Data sources: Met Office MIDAS (Met Office Integrated Data Archive System) and CEH data centre datasets referenced in the document.