# State tagging application for environmental data quality assurance

## Overview
- Purpose: Implement state tagging to provide improved quality assurance for environmental data, offering contextual information to assess observational data quality and supporting any point-based daily time series.
- Core idea: States are determined by clustering auxiliary data (e.g., meteorological data) from the same day; the app returns state-dependent prediction intervals.
- Use case: Applies to any daily time series observations; helps evaluate data quality for policy review and decision-making.
- Data governance angle: Emphasizes transparency by sharing underlying data and metadata and supporting quality assurance workflows.

## How it works
- Input: User uploads two CSV files—one for state variables (auxiliary data) and one for observations.
- State tagging: States are derived via clustering of auxiliary data by day to provide contextual QA information.
- Outputs: State-dependent prediction intervals and context to assess the reliability of observations; designed to be integrated into QA/monitoring workflows.

## Running the app
- Requirements: Install R and the required R packages; run a Shiny app (e.g., by running app.R in R or RStudio).
- Deployment: Possible to host online; guidance provided via Shiny resources.
- Access: Example deployment available for demonstration.

## Data input formats (4.1 Data upload)
- Option 1 (one observation per line): Columns should include DATE, FIELDNAME, VALUE (other columns ignored).
- Option 2 (tidy/panel/tabular): Use a DATE column and other columns as fieldnames.
- Date formatting: Use non-trivial formats, e.g., YYYY-MM-DD.
- After upload: Click Analyze to proceed.

## Example data (4.2)
- State data example: MIDAS data at Carlisle (Met Office, 2012).
- Observation data example: Data from automatic water monitoring buoy at Blelham Tarn, 2008–2011.
- Sample data snippet provided illustrating DATE, FIELDNAME, VALUE, etc.

## Illustrations and deployment (4.3–4.4)
- Screenshots illustrate app components and workflows.
- Live deployment: https://statetag-generic.datalabs.ceh.ac.uk/ (as of 2020-04-22).

## Licensing and citation
- Code license: Open Government Licence; code accessible at the provided DOI.
- Warranty: App provided without warranty; not guaranteed fit for a particular purpose.
- Citation: Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance. Environmental Information Data Centre. DOI and reference provided in the document.