# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- Compiles flow statistics at NRFA gauging stations nearest to fish survey sites in England.
- Focuses on stations with daily flow records covering the period of interest and within a defined network distance to fish sites.
- Aimed at enabling monitoring of environmental health and policy performance over time, with data suitable for integration with other environmental datasets.

## Data scope, provenance, and access
- Geographic scope: England.
- Time frame: main dataset reflects 1975-2017; period-of-record statistics span 1974/05/20 to 2017/11/02 (earliest sample date minus largest preceding period to most recent sample date). Some metadata references an end around 2019/03/29.
- Data origin: extracted flow statistics from National River Flow Archive (NRFA); linked to fish survey sites via Fish_SiteID.
- Licensing and access:
  - © UKCEH; OS data and public sector information licensed under the OGL v3.0; Crown copyright and database rights.
  - Public access: https://nrfa.ceh.ac.uk/data/search
  - DOI citation provided in metadata for the dataset.
- Related data: Fish_SiteID links to other dataset tables (SiteTable, DataTable, chemical determinands).

## Data structure and outputs
- File structure: one region-specific file per region (Anglian, Midlands, North East, North West, Thames, Southern and South West) named CP_Fish_HydrologyStats_Region.csv.
- Key identifiers: Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate, RF_Matched_Feature_ID (_NRFA gauging station).
- Data columns: 100 variables per region, including:
  - Period-of-record statistics: mean, q50, sd, cov, q5.mean, q95.mean.
  - Threshold statistics for 3M, 6M, and 12M periods preceding each survey date:
    - threshold (flow quantile at 5%, 25%, 75%, 95%)
    - duration_exceeded (proportion of days threshold exceeded)
    - n_exceedences (proportion of exceedence events)
    - avg_patch_length (average length of exceedence events)
- Column naming convention explained in metadata:
  - {n}_{period}_{P}_{stat} where:
    - n = 3M, 6M, 12M (preceding period length)
    - period = precper or POI (precipitation period vs. period of interest)
    - P = 5%, 25%, 75%, 95% (percentile used)
    - stat = threshold, duration_exceeded, n_exceedences, avg_patch_length
- Missing data code: NA.
- Data interpretation notes:
  - Exceedence terminology covers values above (quantiles > 0.5) or below (quantiles < 0.5) the threshold.
  - Exceedence events defined as periods of consecutive days exceeding the threshold.

## Methods and data processing
- Matching and geospatial workflow:
  - Gauging stations snapped to the nearest river network line by Euclidean distance; transformed to a polygon to enable network splitting.
  - River network distance between each fish survey site and its nearest gauging station calculated; NRFA stations matched to fish sites by shortest distance along the river network.
  - Only NRFA stations with daily flow records in the period of interest were used; data extracted for 12 months prior to each fish survey.
- Software and tools:
  - ArcGIS (version 10.8 or later) for network matching and visualization.
  - Python 3 with modules: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings for data extraction and matching.
- Data processing steps:
  - For each gauging station, compute a full period-of-record set of statistics (mean, median, sd, cov, q5.mean, q95.mean).
  - Compute threshold-based statistics for 3M, 6M, and 12M windows prior to each survey date (precper or POI) at 5%, 25%, 75%, 95% quantiles.
- Quality assurance:
  - Site matchings manually checked due to prior automated-matching errors; manual verification supplementing automated workflow.

## Usage, standards, and caveats
- Standardized metrics enable comparison across sites and times, supporting monitoring of environmental health and policy performance.
- Data are suitable for integration with other environmental datasets through the common Fish_SiteID linkage.
- Cited dataset: Ainsworth et al. (2024) with a DOI provided; dataset maintained under UKCEH/NERC stewardship.
- Limitations and considerations:
  - Period-of-record definitions and end dates vary between sections; users should align analyses with the defined windows (precper vs POI) and the stated dates in the metadata.
  - Some regions may have variable sample sizes (number of rows depends on region).

## Data provenance and citation
- Primary authors: Virginie Keller (CEH) and Rachel Ainsworth (University of Hull), with collaborators.
- Funding: NERC grant NE/S000100/2.
- Citation format: Ainsworth, R.F.; Keller, V.; Bachiller-Jareno, N.; Jürgens, M. D.; Eastman, M.; Sadykova, D; Rizzo, C.; Scarlett, P.; Peirson, G.; Eley, F.; Antoniou, V.; Cowx, I.G.; Johnson, A.C.; Nunn, A. D. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Relevance to environmental monitoring aims
- Demonstrates the condition of the environment in a consistent format, enabling scrutiny of environmental health and policy performance over time.
- Aligns with the Analysts Monitoring the Environment archetype by providing standardized, QA'd data to support broader analyses and policy assessment.
- Encourages data reuse and integration by maintaining explicit data linkages (Fish_SiteID) across datasets and by providing underlying source references and access points.