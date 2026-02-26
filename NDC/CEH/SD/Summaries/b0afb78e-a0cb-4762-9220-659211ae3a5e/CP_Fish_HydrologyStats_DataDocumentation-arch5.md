# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Scope and provenance
- Dataset of extracted flow statistics for gauging stations matched to fish survey sites across England.
- Time period covered: 1975-2017 (full period of interest used for statistics spans 1974/05/20 – 2019/03/29; region files pertain to 1975-2017).
- Geographic location: England.
- Source data: National River Flow Archive (NRFA) flow records matched to fish sites via river network distance; daily flow records used where available.
- Funding: NERC grant NE/S000100/2.
- Authors: Virginie Keller (CEH) and Rachel Ainsworth (University of Hull), with additional coauthors.
- Publication/see also: Data cited in Ainsworth et al. 2024 (NERC EDS Environmental Information Data Centre); DOI provided.

## Data content and structure
- File organization: One file per region (Anglian, Midlands, North East, North West, Thames, Southern, South West) named CP_Fish_HydrologyStats_Region.csv.
- Number of variables: 100 per region (structure varies by region due to row counts).
- Key identifiers:
  - Fish_SiteID: unique fish site code (Chempop project).
  - Fish_Easting / Fish_Northing: site coordinates.
  - Fish_SurveyDate: date of fish survey.
  - RF_Matched_Feature_ID: NRFA gauging station ID matched to the site.
- Data relationships: Fish_SiteID links to other dataset tables (DataTable, SiteTable, chemical determinands).
- Time-series statistics (Period of record statistics):
  - mean, q50 (median), sd (standard deviation), cov (coefficient of variation), q5.mean, q95.mean over the full period of interest.
- Threshold statistics (3M, 6M, 12M preceding periods):
  - For each period, both precper and POI variants.
  - Percentiles: 5%, 25%, 75%, 95%.
  - Statistics: threshold (flow quantile), duration_exceeded, n_exceedences, avg_patch_length.
- Data codes and notes:
  - Missing data coded as NA.
  - Period definitions: 3M/6M/12M preceding sample date; POI uses corresponding days/months from full period of interest.
- Data characteristics:
  - 100 variables per region; exact row counts depend on region.
  - Threshold definitions: exceedence refers to values above (for quantiles > 0.5) or below (for quantiles < 0.5) the threshold; exceedence events defined as consecutive-day periods exceeding the threshold.

## Methods and processing
- Data collection and alignment:
  - Gauging stations snapped to nearest river network line using Euclidean distance; a 1e-4 m buffer converted to polygon for network splitting; lines split into 3 sections; distance along network calculated; nearest NRFA station assigned to each fish site.
  - NRFA flow series extracted for matched stations; only stations with daily flow records covering the period of interest used.
  - Data for 12 months prior to each fish survey extracted; statistics computed per station.
- Processing steps:
  - Calculated full-period statistics: mean, median (q50), sd, cov, q5.mean, q95.mean.
  - Calculated threshold statistics for 3M, 6M, 12M preceding periods and for POI vs precper:
    - threshold values at 5%, 25%, 75%, 95% percentiles.
    - duration_exceeded (days threshold exceeded divided by total days in preceding period).
    - n_exceedences (number of exceedance events divided by total days in preceding period).
    - avg_patch_length (average duration of exceedance events).
- Tools and environment:
  - ArcGIS (map/Pro) used for visualisation and network matching.
  - Python 3 (libraries: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings) used for data extraction and network matching.
- Quality assurance:
  - Site matching was manually checked due to errors in automated matching scripts; manual verification performed to ensure correct NRFA linkage.

## Licensing, access, and related data
- Licensing:
  - Data © UK Centre for Ecology & Hydrology (UKCEH).
  - Waterbodies in Great Britain contain OS data and public sector information licensed under the OGL v3.0.
  - Crown copyright and database rights EMOU206.
- Public access:
  - Data publicly accessible via https://nrfa.ceh.ac.uk/data/search.
- Related data:
  - Fish_SiteID links to site tables, data tables, and chemical determinands in other datasets.
  - No additional data sources cited as used beyond NRFA matching.
- Versioning:
  - No multiple versions of the dataset reported.

## Quality assurance and data quality notes
- Manual verification conducted for site matching due to automated matching errors.
- Data completeness: less than 1% missing data in the matching period.
- Data notes:
  - Threshold definitions and calculations explicitly documented.
  - Documentation includes detailed column naming conventions and interpretation of threshold-based metrics.

## Data governance and stewardship implications
- Metadata completeness supports discoverability and reuse by data stewards and researchers.
- Clear provenance: explicit data sources (NRFA), matching methodology, and processing steps aid reproducibility and governance.
- Licensing constraints and OS data attribution should be observed when sharing or distributing derived products.
- No update/version history indicated; current dataset version is static.

## Relationships and integration
- Data are designed for integration with other datasets through Fish_SiteID, enabling linkage to:
  - Site tables
  - Data tables
  - Chemical determinands
- Regional CSVs can be combined to form a national view, with care taken to maintain consistent NRFA matching and time-period framing.

## Contacts and citation
- Dataset authors and contributors listed; full citation provided:
  Ainsworth, R.F.; Keller, V.; Bachiller-Jareno, N.; Jürgens, M. D.; Eastman, M.; Sadykova, D; Rizzo, C.; Scarlett, P.; Peirson, G.; Eley, F.; Antoniou, V.; Cowx, I.G.; Johnson, A.C.; Nunn, A. D. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e