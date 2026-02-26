# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017.

## Overview
- Compiles flow statistics at gauging stations matched to fish survey sites across England (1975–2017).
- Data extracted for NRFA gauging stations with daily flow records; includes 12 months of flow data prior to each fish survey.
- Regional data stored as CP_Fish_HydrologyStats_Region.csv, with one file per English region.

## Data Providers, Access, and Usage
- Authors: Virginie Keller (CEH) and Rachel Ainsworth (University of Hull); collaboration with UKCEH.
- Geographic scope: England.
- Funding: NERC grant NE/S000100/2.
- Access/licensing: © UKCEH; OS data and public sector information licensed under OGL v3.0; datasets discoverable via nrfa.ceh.ac.uk/data/search.
- Data citation: Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. DOI provided.
- Data relationship: Fish_SiteID in region CSVs matches IDs in other dataset tables (DataTable, SiteTable, chemical determinands).

## Methods: Data Collection and Matching
- Spatial matching: Gauging stations snapped to river network lines; small buffer added to convert to polygons for network splitting; nearest gauging station to each fish survey site determined along the river network.
- Source flow data: NRFA (National River Flow Archive) stations with sufficient daily records; time series aligned to fish sites.
- Temporal scope: Data extracted for 12 months prior to each fish survey; full period of interest defined as earliest sample date minus largest preceding period to most recent sample date.

## Data Processing and Statistics
- Period-of-record statistics (full period of interest):
  - Metrics computed at each gauging station: mean, median (q50), standard deviation (sd), coefficient of variation (cov), q5/mean, q95/mean.
- Threshold statistics (3-, 6-, 12-month preceding periods):
  - For 5%, 25%, 75%, 95% quantiles: threshold (discharge quantile), duration_exceeded (days threshold exceeded divided by total days in preceding period), n_exceedences (number of exceedance events divided by total days), avg_patch_length (average length of exceedance events).
  - Terminology: precper refers to the preceding period; POI refers to periods relative to the full period of interest.
- Tools: ArcGIS (map/Pro) for visualization; Python 3 (os, shapely, pandas, geopandas, matplotlib, numpy, network) for network matching and data extraction.
- Quality assurance: Manual verification of site matching due to errors in automated matching; some scripts required manual intervention.

## Data Structure and Content
- File: CP_Fish_HydrologyStats_Region.csv (region-specific)
- Variables: 100 total; region-dependent rows.
- Key columns:
  - Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate, RF_Matched_Feature_ID.
  - Period-of-record statistics: mean, q50, sd, cov, q5.mean, q95.mean.
  - Threshold statistics: columns named as {n}_{period}_{P}_{stat} describing 3M/6M/12M periods, precper/POI, 5%/25%/75%/95%, and stat (threshold, duration_exceeded, n_exceedences, avg_patch_length).
- Interpretation: threshold = estimated flow quantile; duration_exceeded and n_exceedences are normalised by total days in the preceding period; avg_patch_length is days per exceedance event.

## Data Details and Definitions
- Threshold exceedance: defined as periods of consecutive days where the threshold is exceeded; for quantiles > 0.5, exceedence means flow > threshold; for quantiles < 0.5, exceedence means flow < threshold.
- Missing data: NA.
- Administrative notes: 12 months preceding the survey and the full period of interest span roughly 1974/05/20 to 2019/03/29 (as described in the dataset methods).

## Practical Implications for Analysis
- Enables correlation and predictive analyses between fish survey metrics and hydrological conditions (flow variability, extreme events, thresholds) across English rivers.
- Facilitates region-specific and cross-region comparisons of flow regimes relative to fish habitat metrics.
- Data are suitable for building models linking river flow characteristics to fish abundance and habitat quality, with explicit quantification of thresholds and event durations.