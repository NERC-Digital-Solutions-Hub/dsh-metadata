# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- Dataset extracts flow statistics for gauging stations nearest to fish survey sites in English rivers, focusing on stations with daily flow records within the period of interest.
- Regional data is stored in separate files (one per region: Anglian, Midlands, North East, North West, Thames, Southern and South West) with a single file per region named CP_Fish_HydrologyStats_Region.csv.
- Timeframe considerations:
  - Period of record statistics cover 1974/05/20 to 2019/03/29.
  - Period of interest for matching and analysis is 1974/05/20 to 2017/11/02, with 12 months prior to each fish survey used for extraction.
- Data linked to fish survey sites via Fish_SiteID, matching to NRFA gauging stations (RF_Matched_Feature_ID).

## Data sources and linking
- Primary data sources:
  - National River Flow Archive (NRFA) gauging stations for daily flow records.
  - Fish survey sites within England (chempop project coordinates).
- Key linkage:
  - Fish_SiteID (fish site) is matched to a single NRFA gauging station (RF_Matched_Feature_ID) along the river network.
- Licensing and access:
  - © UKCEH; data includes OS and public sector information licensed under OGL v3.0.
  - Data accessible via the NRFA data portal: https://nrfa.ceh.ac.uk/data/search
  - Dataset published with citation: Ainsworth et al. 2024 (NERC EDS Data Centre, DOI provided in citation).

## Methods and processing
- Spatial and network methodology:
  - Gauging stations are snapped to the nearest line on the river network using Euclidean distance; a small polygon buffer is created to enable network splitting; the river line is split; distances along the network between survey sites and gauging stations are calculated to assign the nearest station to each site.
  - NRFA stations with daily records during the period of interest are used; time series for these stations are extracted for 12 months prior to fish surveys.
- Statistical processing:
  - For each gauging station, period-of-record statistics are calculated over the full period (earliest sample date minus the largest preceding period to the most recent sample date: 1974/05/20 – 2019/03/29).
  - Threshold statistics are calculated for 3-, 6-, and 12-month preceding periods prior to each survey, including:
    - Threshold values (5%, 25%, 75%, 95% quantiles, referred to as 5%, 25%, 75%, 95%).
    - Duration_exceeded (days the threshold was exceeded) divided by the total days in the preceding period.
    - N_exceedences (number of exceedance events) divided by total days in the preceding period.
    - Avg_patch_length (average duration of exceedance events) = duration_exceeded / n_exceedences.
  - Thresholds are defined as estimated discharge quantiles; exceedance can refer to values above or below the threshold depending on the percentile.
- Tools and software:
  - ArcGIS (Map or Pro) for visualization; Python 3 with modules including os, shapely, pandas, geopandas, matplotlib, numpy, network for matching along the river network.
- Quality assurance:
  - Site matching was manually checked due to errors in automated matching; manual verification complemented the automated workflow.

## Data content and structure
- File: CP_Fish_HydrologyStats_Region.csv (one per region)
- Variables:
  - Fish_SiteID: unique fish site identifier (Chempop project)
  - Fish_Easting, Fish_Northing: site coordinates
  - Fish_SurveyDate: date of fish survey
  - RF_Matched_Feature_ID: matched NRFA gauging station
  - Period of record statistics: mean, q50 (median), sd, cov (coefficient of variation), q5.mean, q95.mean
  - Threshold statistics (for 3M, 6M, 12M precedents; POI or precper):
    - {n}_{period}_{P}_{stat} columns, where:
      - n = 3M, 6M, 12M (preceding period length)
      - period = precper (preceding period) or POI (full period of interest)
      - P = 5%, 25%, 75%, 95% percentile
      - stat = threshold, duration_exceeded, n_exceedences, avg_patch_length
  - Missing data: NA
- Data relationships:
  - Fish_SiteID in CP_Fish_HydrologyStats_Region.csv matches Fish_SiteID in other related dataset tables (DataTable, SiteTable, chemical determinands).

## Practical considerations for monitoring frameworks
- Use case:
  - Provides environmental health measures linking fish site status to river flow and climate conditions, enabling monitoring of policy impacts and informing future decisions.
- Data governance and openness:
  - Requires data sharing of underlying datasets; metadata quality and provenance are emphasized to ensure traceability and reuse.
- Reusability and integration:
  - Regionally organized with a consistent structure, enabling dashboards and comparative analyses across regions.
- Limitations and barriers:
  - Some data gaps and metadata inadequacies can hinder quick verification.
  - Data transformations and standardization efforts may be needed to harmonize datasets across regions or with other datasets.

## Data quality, limitations, and governance
- Quality assurance:
  - Manual verification of site-to-station matches due to automated matching issues.
- Data gaps:
  - Data restricted to gauging stations with sufficient daily records; some missing data codes exist (NA) and require careful handling.
- Metadata and provenance:
  - Clear methodological documentation describing data sources, processing steps, and statistical definitions to support reproducibility and governance.

## Access, licensing, and citations
- Access:
  - Publicly accessible via the NRFA data portal and described in the accompanying publication (citation provided).
- Licensing:
  - Data licensed under OGL v3.0 with Crown copyright and database rights; OS data included.
- Citation:
  - Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e