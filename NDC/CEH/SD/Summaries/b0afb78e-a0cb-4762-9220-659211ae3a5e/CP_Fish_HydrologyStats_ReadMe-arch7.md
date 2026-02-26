# CP_Fish_HydrologyStats

- A region-based collection of extracted flow statistics for gauging stations matched to fish survey sites. Each region has its own CP_Fish_HydrologyStats_Region.csv file containing 100 variables related to site metadata and flow statistics.

## Purpose and content
- Purpose: quantify hydrological context around fish survey sites by linking NRFA flow data to fish sampling locations.
- File structure: one CSV per region (Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Key linkage: Fish_SiteID from fish datasets is matched to NRFA gauging stations (RF_Matched_Feature_ID) along the river network.
- Spatial data included: Fish_Easting and Fish_Northing coordinates for each fish site; region-specific matching to NRFA stations.

## Data sources and provenance
- Primary data: NRFA (National River Flow Archive) flow records.
- Matching methodology: gauging stations snapped to the nearest river line using Euclidean distance, converted to a polygon for network splitting, then distance along the network to connect to fish sites.
- Software used: ArcGIS (10.8+ or Pro) for geospatial matching; Python 3 (with os, shapely, pandas, geopandas, matplotlib, numpy, network) for data processing and matching.
- Time frame: flow data for 12 months prior to each fish survey; full statistics cover 1974/05/20 – 2019/03/29.

## Spatial matching and data processing
- Snapping method: NRFA stations matched to fish sites by shortest distance along the river network; only stations with daily records across the period of interest were used.
- Data processing workflow: extract time series for the relevant period, compute summary and threshold statistics, and compile into region-specific CSVs.
- Quality assurance: manual checking of site matches due to earlier automation issues; overall data quality constrained by missing data.

## Variables and data structure
- Core fields:
  - Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate
  - RF_Matched_Feature_ID (NRFA gauging station ID)
- Period-of-record statistics (for the full period of interest):
  - mean, q50, sd, cov, q5.mean, q95.mean
- Threshold statistics (for 3-, 6-, and 12-month preceding periods):
  - {n}_{period}_{P}_{stat} where
    - {n} = 3M, 6M, 12M (preceding period length)
    - {period} = precper or POI (period of interest)
    - {P} = 5%, 25%, 75%, 95% (percentile for threshold)
    - {stat} = threshold, duration_exceeded, n_exceedences, avg_patch_length
  - Exceedance definitions: threshold breaches considered for both directions (above/below threshold depending on percentile); duration_exceeded is days threshold is exceeded divided by total days in the preceding period; n_exceedences is number of exceedance events divided by total days; avg_patch_length is duration_exceeded divided by n_exceedences.
- Data nuances:
  - 100 variables per region-file; number of rows varies by region.
  - Missing data coded as NA; less than 1% missing data used for matching.
- Periods and interpretation:
  - Period of interest defined as earliest sample date minus largest preceding period to most recent sample date.
  - Full period used for POI thresholds; 1974/05/20 to 2019/03/29.

## Data quality and QA
- Matching: manual verification of site-to-station matches; automated Python matching previously produced errors.
- Data completeness: less than 1% missing data within the period of interest for matching.
- Documentation clarity: column naming scheme explained to aid interpretation and GIS usage.

## Usage and GIS integration
- Recommended tools: ArcGIS (map or Pro) for visualization; Python for data preparation and network matching.
- How to use in GIS:
  - Join region CSV to fish survey layers by Fish_SiteID.
  - Map spatially the Fish_Easting/Fish_Northing coordinates and associated hydrological statistics around each fish site.
  - Use threshold statistics to identify periods of notably high or low flows near survey dates.

## Licensing and rights
- Data licenses: © UKCEH; Waterbodies in Great Britain contain OS data and public sector information licensed under the OGL v3.0. Crown copyright and database rights EMOU206.

## Authors and contact
- Generated 2022-01-11 by Rachel Ainsworth; co-authored with Virginie Keller.