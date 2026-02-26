# CP_Fish_HydrologyStats

## Overview
- Contains extracted flow statistics for NRFA gauging stations matched to fish survey sites.
- Only includes gauging stations with daily flow records exceeding the period of interest and with less than 1% missing data.
- Timeframe for extracted data: 12 months prior to each fish survey; full period of record spans 1974/05/20–2019/03/29.
- Generated for regional files, intended to support fish-habitat analyses by providing hydrology context.

## Data Structure and Scope
- One region-specific file per region: CP_Fish_HydrologyStats_Region.csv.
- Region list: Anglian, Midlands, North East, North West, Thames, Southern, South West.
- Primary linking key: Fish_SiteID (matches Fish_SiteID in other datasets like DataTable, SiteTable, chemical determinand).
- Contents include:
  - Fish site location: Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate.
  - Matched NRFA gauging station: RF_Matched_Feature_ID.
  - Period-of-record statistics for the full period: mean, q50, sd, cov, q5.mean, q95.mean.
  - Threshold statistics for 3M, 6M, and 12M periods preceding surveys: threshold, duration_exceeded, n_exceedences, avg_patch_length (with 5%, 25%, 75%, 95% thresholds).
- Data model notes: variable names follow a {n}_{period}_{P}_{stat} scheme (n = 3M/6M/12M; period = precper or POI; P = 5%/25%/75%/95%; stat = threshold/duration_exceeded/n_exceedences/avg_patch_length).

## Provenance and Data Source
- Derived from NRFA flow archive (National River Flow Archive) via CEH.
- Method: match NRFA stations to fish sites along the river network using network-distance in ArcGIS; convert points to polygons for network splitting; compute nearest network distance to assign gauging stations to survey sites.
- Time series extracted for 12 months before each fish survey; only NRFA stations with adequate daily records were used.

## Methodology and Processing
- Software and tools:
  - ArcGIS (version 10.8+ or Pro) for network matching and spatial processing.
  - Python 3 with modules: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings for data extraction and calculations.
- Calculations:
  - Full-period statistics from the entire matching window: mean, median (q50), standard deviation (sd), coefficient of variation (cov), and Q5/mean, Q95/mean.
  - 3-, 6-, and 12-month preceding-period statistics for thresholds:
    - Threshold = estimated discharge quantile (5%, 25%, 75%, 95%).
    - duration_exceeded = proportion of days threshold was exceeded in the preceding period.
    - n_exceedences = number of exceedance events per total days in the preceding period.
    - avg_patch_length = average duration of exceedance events (days exceeded divided by number of exceedances).
- QA and validation:
  - Site matching was manually checked due to errors in automated matching; previously automated scripts were insufficient.
  - Missing data handling: NA used for missing values; only regions with <1% missing in the period were included.

## Data Quality and Interpretation Notes
- 100 variables per region file; primary identifiers and coordinates enable discovery and linkage to related datasets.
- Exceedance definitions: apply to both above-threshold and below-threshold scenarios depending on quantile (>0.5 vs <0.5).
- Threshold statistics provide insight into flow variability and extremity around fish survey dates.

## Licensing, Access, and Versioning
- Licensing: Data and OS/OpenData components licensed under OGL v3.0; Crown copyright and database rights.
- Versioning: No multiple versions indicated for this dataset (single regional file per region).
- Authorship: Generated 2022-01-11 by Rachel Ainsworth; contributors include Virginie Keller.

## Data Linkages and Governance
- Strong linkage to fish site data via Fish_SiteID; interoperable with related datasets (DataTable, SiteTable, chemical determinand).
- Designed to support data discovery, sharing, and reuse by data stewards and users needing hydrological context for fish survey analyses.
- Emphasizes data provenance from NRFA with explicit processing steps to enhance traceability and reproducibility.

## Challenges for Data Stewards
- Incomplete picture of user needs and priorities; potential misalignment with downstream analyses.
- Timely data acquisition from data creators and ensure metadata completeness.
- Heterogeneous data sources and formats across river networks; interoperability considerations.
- Handling large regional datasets and older, non-interoperable database structures.

## Author and Contact
- Authors: Rachel Ainsworth (r.ainsworth@hull.ac.uk); Virginie Keller (vke@ceh.ac.uk).