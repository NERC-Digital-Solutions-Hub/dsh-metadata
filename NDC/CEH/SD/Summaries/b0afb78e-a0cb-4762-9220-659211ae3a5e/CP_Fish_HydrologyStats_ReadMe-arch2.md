# CP_Fish_HydrologyStats

- This file contains extracted flow statistics for gauging stations selected to be nearest to fish survey sites, using data only from stations with daily flow records spanning the period of interest (12 months prior to each fish survey).
- Generated per region, with one file named CP_Fish_HydrologyStats_Region.csv for each region (Anglian, Midlands, North East, North West, Thames, Southern and South West).

## Purpose and scope

- Align NRFA gauging stations with fish survey sites by minimal distance along the river network.
- Focus on stations with adequate daily flow records for the period of interest.
- Provides statistics for the full period and for 3-, 6-, and 12-month windows preceding each fish survey.

## Data structure and linkage

- Key linkage: Fish_SiteID in this dataset matches Fish_SiteID in other CHEMPop-related data tables (DataTable, SiteTable, chemical determinand).
- Main fields include:
  - Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate
  - RF_Matched_Feature_ID (gauge station identifier)
- Contents include:
  - Period-of-record statistics (mean, q50, sd, cov, q5.mean, q95.mean)
  - Threshold statistics for 3-, 6-, and 12-month periods (threshold, duration_exceeded, n_exceedences, avg_patch_length)
- Column naming for threshold statistics follows the pattern {n}_{period}_{P}_{stat}, with detailed definitions provided.

## Time frame and statistics

- Full period: 1974/05/20 to 2019/03/29 (earliest sample date minus largest preceding period to most recent sample date).
- Threshold statistics computed for 3-, 6-, and 12-month periods prior to each survey:
  - 5%, 25%, 75%, 95% quantiles used to define thresholds
  - For each threshold: days exceeded, number of exceedance events, and average patch length (average duration of exceedance events)

## Methodology

- Spatial matching:
  - NRFA gauging stations snapped to the nearest river network line via Euclidean distance.
  - A 1e-4 m buffer converts the point to a polygon to enable network splitting.
  - The river line is split; the distance along the network between each fish site and connected gauging station is calculated; the nearest station is assigned to the site.
  - NRFA stations with insufficient daily records are excluded.
- Time series extraction:
  - Time series for the 12 months prior to each fish survey is extracted from the NRFA stations.
- Computations:
  - Full-period statistics: mean, median (q50), sd, cov, q5.mean, q95.mean.
  - Threshold statistics for 3-, 6-, 12-month windows: threshold (quantile), duration_exceeded, n_exceedences, avg_patch_length.
- Software and tools:
  - ArcGIS (version 10.8 or later) for mapping and network operations
  - Python 3 with modules: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings
- Quality assurance:
  - Site matching was manually verified due to errors in automated matching that occurred earlier in the workflow.
  - Data quality note: less than 1% missing data in the period of interest.

## Data specifics

- File: CP_Fish_HydrologyStats_Region.csv
- Rows/columns: region-dependent; total around 100 variables per region
- Key data captured per row:
  - Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate, RF_Matched_Feature_ID
  - Period-of-record statistics: mean, q50, sd, cov, q5.mean, q95.mean
  - Threshold statistics for 3M/6M/12M: {n}_{period}_{P}_{stat} (threshold, duration_exceeded, n_exceedences, avg_patch_length)
- Missing data: coded as NA
- Data coverage note: only gauging stations with adequate daily flow records were included; data period covers 1974/05/20 to 2019/03/29

## Licensing and provenance

- Licensing: © UKCEH; waterbodies include OS data and public sector information licensed under the OGL v3.0; Crown copyright and database rights EMOU206
- Provenance: Derived from the National River Flow Archive (NRFA) flow archive; region-specific files compiled for CHEMPop project
- Generation date and authors: Generated on 2022-01-11 by Rachel Ainsworth; authors listed as Rachel Ainsworth and Virginie Keller

## Considerations for analysts

- The dataset is designed for standardized cross-region comparisons of hydrology adjacent to fish survey sites, enabling assessment of environmental health and policy performance over time.
- Potential for data integration:
  - Link fish-site statistics with underlying NRFA time series and other environmental data to enrich analyses (aligns with the archetype’s aim to increase dataset value by combining data and facilitating access to underlying data).
- Data accessibility:
  - Region files can be correlated with other CHEMPOP datasets via Fish_SiteID; underlying NRFA time series may be leveraged for deeper analyses but requires access to the NRFA data sources.