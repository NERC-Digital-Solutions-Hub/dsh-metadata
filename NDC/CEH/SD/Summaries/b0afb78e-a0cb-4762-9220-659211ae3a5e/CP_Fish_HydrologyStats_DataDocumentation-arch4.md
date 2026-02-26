# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- Compilation of flow statistics for gauging stations matched to fish survey sites across England.
- Focuses on relationships between fish abundance, habitat, water quality, flow, and climate from 1975 to 2017.
- Data are extracted from NRFA gauging stations with sufficient daily flow records and are linked to fish sites via network-based matching.

## Data Scope and Structure
- Geographic coverage: England.
- File structure: One region-specific file per region, named CP_Fish_HydrologyStats_Region.csv (Regions: Anglian, Midlands, North East, North West, Thames, Southern and South West).
- Key identifiers: Fish_SiteID (unique for fish sites; matches across data tables), Fish_Easting, Fish_Northing, Fish_SurveyDate, RF_Matched_Feature_ID (gauging station).
- Data licensing: © UKCEH; includes OS data licensed under OGL v3.0; Crown copyright and database rights (EMOU206).
- Data access: Publicly available via https://nrfa.ceh.ac.uk/data/search; dataset cited with DOI in the related publication.
- Data versioning: Single version; no multiple versions reported.
- Data linkage: Fish_SiteID links to site tables, data tables, and chemical determinands in related datasets.

## Methodology
- Matching approach: Gauging stations are snapped to the nearest river line by Euclidean distance; a small buffer is added to convert to a polygon for network splitting; the river line is segmented, and sites are assigned to the nearest gauging station along the network.
- Data sources: NRFA (National River Flow Archive) gauging stations matched to fish sites using shortest network distance; only stations with sufficient daily records were used.
- Time series: Data extracted for 12 months prior to each fish survey; appropriate NRFA time series were then compiled.
- Statistics calculated:
  - Period-of-record statistics across the full period of interest (earliest date minus largest preceding period to most recent date): mean, median (q50), sd, cov, q5/mean, q95/mean (full period; dates cited ~1974/05/20 to 2019/03/29).
  - Threshold statistics for 3-, 6-, and 12-month preceding periods: threshold (flow quantile), duration_exceeded (days threshold exceeded divided by days in preceding period), n_exceedences (number of exceedance events divided by days in preceding period), and avg_patch_length (average duration of exceedance events).
  - Thresholds are calculated for 5%, 25%, 75%, and 95% quantiles (denoted as 5%, 25%, 75%, 95% in column names).
- Tools and software:
  - ArcGIS (map or Pro) for visualization and matching.
  - Python 3 with modules: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings for data extraction and processing.
- Quality assurance: Manual verification of site matching due to errors in automated matching; some previously automated scripts required human review.
- Data provenance and collaborators: Virginie Keller, Michael Eastman, Rachel Ainsworth, Nuria Bachiller-Jareno.

## Data Content and Metadata
- Dataset per region: CP_Fish_HydrologyStats_Region.csv containing approximately 100 variables; region-dependent row counts.
- Core variables:
  - Fish_SiteID, Fish_Easting, Fish_Northing, Fish_SurveyDate, RF_Matched_Feature_ID.
  - Period-of-record statistics: mean, q50 (median), sd, cov, q5.mean, q95.mean.
  - Threshold statistics: columns named as {n}_{period}_{P}_{stat}, where:
    - {n}: 3M, 6M, 12M (preceding period length in months).
    - {period}: precper (preceding period) or POI (period of interest, i.e., full period of interest).
    - {P}: 5%, 25%, 75%, 95% (percentile used to define the threshold).
    - {stat}: threshold, duration_exceeded, n_exceedences, avg_patch_length.
- Missing data: NA.
- Exceedance definitions: For quantiles > 0.5, exceedance means values above the threshold; for quantiles < 0.5, exceedance means values below the threshold. An exceedance event is a consecutive sequence of days exceeding the threshold.
- Time frame notes: Full period of interest cited as 1974/05/20 – 2019/03/29 in one section, with ancillary notes indicating data extracted for 12 months prior to each fish survey and reference to 1974/05/20 – 2017/11/02 in another description; the dataset consistently anchors to the long historical window and aligns 12-month preceding periods to survey dates.

## Access, Licensing and Citations
- Licensing: © UKCEH; publicly licensed data elements under OGL v3.0; Crown copyright and database rights (EMOU206).
- Public location for data: https://nrfa.ceh.ac.uk/data/search.
- Related publication and citation: Ainsworth et al. 2024. Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.

## Quality Assurance and Limitations
- Data have been filtered to include only NRFA stations with sufficient daily flow records for the period of interest.
- Manual QA performed for site matching due to issues with automated matching scripts.
- Data integration relies on cross-dataset linkage via Fish_SiteID and RF_Matched_Feature_ID across site, data, and chemical determinand tables.