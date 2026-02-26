# CP_Fish_HydrologyStats

## Overview
- Contains extracted flow statistics for gauging stations matched to fish survey sites.
- Includes data only for stations with daily flow records covering the period of interest (12 months prior to fish surveys).

## Data organization
- One file per region: CP_Fish_HydrologyStats_Region.csv (regions: Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Key linkage: Fish_SiteID matches with other dataset files (DataTable, SiteTable, chemical determinand).
- Each region file contains up to ~100 variables related to fish site hydrology statistics.

## Data sources and provenance
- Derived from NRFA (National River Flow Archive) flow archive managed by CEH.
- Matching of NRFA stations to fish sites performed using river-network distance within Arc GIS.

## Methods

- Spatial matching and data extraction
  - Gauging stations snapped to nearest line on river network using Euclidean distance; converted to polygons to enable network splitting; distance along the network calculated to assign the nearest NRFA station to each fish site.
  - Only NRFA stations with daily flow records exceeding the period of interest were used.

- Time window and data extraction
  - Time series from selected NRFA stations extracted for 12 months prior to each fish survey.
  - Period of record for statistics: 1974/05/20 – 2019/03/29 (earliest sample date minus largest preceding period to most recent sample date).

- Statistics computed
  - Period of record statistics (full period of record):
    - mean, q50 (median), sd (standard deviation), cov (coefficient of variation), q5.mean, q95.mean.
  - Threshold statistics for 3-, 6-, and 12-month preceding periods:
    - Threshold values at 5%, 25%, 75%, 95% percentiles (P).
    - duration_exceeded: proportion of days the threshold was exceeded during the preceding period.
    - n_exceedences: proportion of exceedance events during the preceding period.
    - avg_patch_length: average duration of exceedance events (days exceeded divided by number of exceedances).

- Definitions and interpretations
  - Exceedance is defined relative to each percentile; for quantiles > 0.5, exceedance means values above the threshold; for quantiles < 0.5, exceedance means values below the threshold.
  - POI vs precper distinctions in column naming indicate whether thresholds were estimated on the preceding period (precper) or on the full period of interest (POI).

## Software and reproducibility
- Arc GIS (Map or Pro) used for visualization.
- Python 3 used for data matching along the river network (modules: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings).

## Quality assurance
- Site matching was manually checked due to errors in automated matching; manual verification ensured correct NRFA-to-fish-site associations.

## Data schema and key columns

- Fish_SiteID: unique fish site identifier.
- Fish_Easting, Fish_Northing: site coordinates.
- Fish_SurveyDate: date of fish survey.
- RF_Matched_Feature_ID: matched NRFA gauging station ID.
- Period of record statistics: mean, q50, sd, cov, q5.mean, q95.mean.
- Threshold statistics: columns named as {n}_{period}_{P}_{stat}, where:
  - n = 3M, 6M, 12M (preceding period length)
  - period = precper or POI
  - P = 5%, 25%, 75%, 95%
  - stat = threshold, duration_exceeded, n_exceedences, avg_patch_length
- Missing data: coded as NA.
- Notes: fewer than 1% missing data in the period; only gauging stations meeting this criterion are included.

## Additional notes and permissions
- Data/licensing: © UKCEH; Waterbodies in Great Britain include OS data and public sector information licensed under OGL v3.0; Crown copyright and database rights, EMOU206 .2. Publication date around 2022-01-11 (generator: Rachel Ainsworth).