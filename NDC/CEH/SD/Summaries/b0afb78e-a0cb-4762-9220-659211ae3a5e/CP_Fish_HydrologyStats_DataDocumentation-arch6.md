# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017.

## Overview
- A dataset of flow statistics and related metrics for gauging stations near fish survey sites across England, covering 1975–2017.
- Data were extracted for NRFA gauging stations with daily flow records during the period of interest and linked to fish survey sites to enable analysis of relationships between hydrology and fish metrics.
- Regional splits are provided (Anglian, Midlands, North East, North West, Thames, Southern, South West) with one file per region.

## Provenance and access
- Authors: Virginie Keller (CEH) and Rachel Ainsworth (University of Hull), with contributions from others.
- Date range for data collection: 2022-07-21 to 2022-10-11.
- Geographic scope: England.
- Funding: NERC grant NE/S000100/2.
- Licensing: © UKCEH; Waterbodies in Great Britain contain OS data and public sector information licensed under the OGL v3.0; Crown copyright and database rights EMOU206 .2.
- Public access: Data available via https://nrfa.ceh.ac.uk/data/search.
- Related dataset relationships: Fish_SiteID links to Fish_SiteID in other tables (DataTable, SiteTable, chemical determinands).
- Citation: Ainsworth et al. 2024. Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.

## Data content and structure
- File organization: One CSV per region named CP_Fish_HydrologyStats_Region.csv.
- Variables: Approximately 100 per region; primary identifiers include:
  - Fish_SiteID: unique fish site identifier (Chempop project).
  - Fish_Easting / Fish_Northing: coordinates of fish sites.
  - Fish_SurveyDate: date of survey.
  - RF_Matched_Feature_ID: gauging station identifier matched to the site.
- Period-of-record statistics (for the full period of interest):
  - mean, q50 (median), sd, cov (coefficient of variation), q5.mean, q95.mean.
- Threshold statistics (for 3-, 6-, 12-month periods preceding each survey):
  - For each of 5%, 25%, 75%, 95% thresholds, four statistic types:
    - threshold: estimated flow quantile.
    - duration_exceeded: proportion of days threshold was exceeded in the preceding period.
    - n_exceedences: proportion of exceedence events in the preceding period.
    - avg_patch_length: average duration of exceedence events (days per event).
- Naming convention for threshold statistics: {n}_{period}_{P}_{stat}, where:
  - n = 3M, 6M, 12M (preceding period length in months)
  - period = precper or POI (precise preceding period vs. period of interest)
  - P = 5%, 25%, 75%, 95%
  - stat = threshold, duration_exceeded, n_exceedences, avg_patch_length
- Data relationships: Fish_SiteID aligns with site records in DataTable, SiteTable, and chemical determinands.

## Methods and processing
- Data collection and matching:
  - NRFA flow stations snapped to river-network lines by nearest distance; a 1e-4 m buffer converts the point to a polygon to enable network splitting.
  - River line split into three sections using the polygon; distance along the network between each fish survey site and the connected gauging station is calculated; nearest station assigned.
  - NRFA gauges with daily records exceeding the period of interest were used; time series for those stations extracted for the fish sites.
  - 12 months of data prior to each fish survey were collected.
- Data processing:
  - Computed full-period statistics (mean, q50, sd, cov, q5.mean, q95.mean) over 1974/05/20 to 2019/03/29.
  - Computed 3-, 6-, 12-month preceding-period statistics for threshold analyses (POI or precper as applicable).
- Tools:
  - Geographic: ArcGIS (Map or Pro) for visualization and network matching.
  - Programming: Python 3 with modules including os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings.
- Quality assurance:
  - Site matches were manually checked; automated matching originally produced errors requiring manual verification.
- Personnel involved: Virginie Keller, Michael Eastman, Rachel Ainsworth, Nuria Bachiller-Jareno.

## Data quality and limitations
- Only gauging stations with daily records exceeding the period of interest and with less than 1% missing data were included in matches.
- Manual verification was necessary due to prior automation errors in site matching.
- Threshold statistics rely on quantile-based definitions; interpretation varies by whether the quantile is above or below 0.5 (exceedence direction accordingly).

## Access, licensing, and use
- Data license and rights: © UKCEH; OS data and public sector information under OGL v3.0; Crown copyright and database rights EMOU206 .2.
- Public availability: nrfa.ceh.ac.uk data search portal; dataset specifically linked through Fish_SiteID relationships across multiple data tables.
- Versions: No multiple versions indicated for this dataset.
- Citation guidance: Use the provided dataset citation to acknowledge data provenance.

## Practical relevance for Data Support
- Provides a ready-made, regionally organized data product that combines fish survey site data with hydrological context, enabling dashboards, reports, and self-serve exploration of relationships between fish metrics and river flow dynamics.
- The explicit matching methodology and QA notes help ensure reproducibility and transparency for data-consuming stakeholders.
- The structured 100-variable region CSVs facilitate integration with other data layers (site tables, chemical determinands) for broader analyses.

## Contact and governance
- Primary authors listed; data stewardship and licensing indicate ongoing governance through UKCEH and the NERC Data Centre.