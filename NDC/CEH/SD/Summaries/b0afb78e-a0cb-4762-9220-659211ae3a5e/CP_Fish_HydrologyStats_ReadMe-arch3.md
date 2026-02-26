# CP_Fish_HydrologyStats_Region.csv

- Purpose: Contains extracted flow statistics for gauging stations matched to fish survey sites to assess hydrology in relation to environmental health; based on 12 months of flow data prior to each fish survey.

- Regions covered: Anglian, Midlands, North East, North West, Thames, Southern, and South West (one file per region).

- Data origin and matching: NRFA (National River Flow Archive) flow data matched to fish sites using ArcGIS by identifying the nearest gauging station along the river network; matches were manually checked due to prior automation errors.

- Sampling frame and period: Gauging stations selected with daily flow records covering the period of interest; period of interest spans 1974-05-20 to 2019-03-29; statistics are derived from 12 months prior to each fish survey date.

- Variables and data structure:
  - Approximately 100 variables per region-file; key identifiers include Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate, RF_Matched_Feature_ID.
  - Data are organized per region in CP_Fish_HydrologyStats_Region.csv with links to related datasets (DataTable, SiteTable, chemical determinand).

- Derived statistics (full period):
  - mean, q50 (median), sd, cov (coefficient of variation), q5.mean, q95.mean.

- Threshold statistics (3-, 6-, and 12-month periods prior to each survey):
  - For each period and percentile (5%, 25%, 75%, 95%): 
    - threshold (discharge quantile)
    - duration_exceeded (proportion of days threshold exceeded)
    - n_exceedences (proportion of exceedance events)
    - avg_patch_length (average duration of exceedance events)

- Data processing details:
  - Time series extracted from NRFA stations for relevant fish-site periods.
  - Periods defined as earliest sample date minus largest preceding period to most recent sample date.
  - Distances along the river network calculated; nearest station assigned to each fish site.
  - Manual verification performed for site matches due to previous automation issues.
  - Processing tools: Arc GIS (Map/Pro) and Python 3 (with os, shapely, pandas, geopandas, matplotlib, numpy, network modules).

- Data quality and limitations:
  - Very low missing data in the matching period (NA as missing data code used).
  - Matching issues previously required manual QA to ensure accurate site-station linkage.
  - Metadata and transformation steps were necessary to render data usable for analysis and policy reporting.

- Licensing and copyright:
  - © UKCEH; data includes OS and public sector information licensed under OGL v3.0; Crown copyright and EMOU206.

- Use and governance considerations:
  - Data are linked to and support environmental monitoring frameworks for evaluating hydrology-health relationships.
  - Emphasizes data provenance, quality assurance, and sharing of underlying data within governance and reporting outputs.