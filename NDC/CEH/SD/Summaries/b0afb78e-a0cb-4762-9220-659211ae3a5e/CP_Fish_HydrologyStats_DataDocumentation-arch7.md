# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

- Overview
  - A dataset of extracted flow statistics and related hydrology metrics linked to fish survey sites in English rivers (1975-2017).
  - Data are aligned to gauging stations with daily flow records that meet the period-of-interest criteria.

- Geographic and temporal scope
  - Geographic location: England.
  - Time period: 1974/05/20 to 2017/11/02 (full period used for statistics); individual survey dates fall within 1975-2017.
  - Regions covered: Anglian, Midlands, North East, North West, Thames, Southern and South West (files are region-specific).

- Data content and structure
  - File format: Region-specific CSV files (one file per region) with CP_Fish_HydrologyStats_Region.csv naming.
  - Variables (example core fields):
    - Fish_SiteID: unique fish site identifier (maps to site tables in related datasets).
    - Fish_Easting, Fish_Northing: coordinates of fish sites.
    - Fish_SurveyDate: date of fish survey.
    - RF_Matched_Feature_ID: gauging station number matched to the site.
    - Period of record statistics: mean, q50, sd, cov, q5.mean, q95.mean.
    - Threshold statistics: 3M/6M/12M preceding-period metrics for precper or POI, including:
      - threshold (flow quantile for P%), duration_exceeded, n_exceedences, avg_patch_length.
  - Column naming convention for thresholds: {n}_{period}_{P}_{stat} where
    - n = 3M, 6M, 12M
    - period = precper or POI
    - P = 5%, 25%, 75%, 95%
    - stat = threshold, duration_exceeded, n_exceedences, avg_patch_length
  - Data completeness: Missing data coded as NA.
  - Data scale: 100 variables per region file; number of rows varies by region.

- Methods and data processing
  - Data linkage and matching
    - NRFA gauging stations snapped to river network lines using Euclidean distance; a small buffer converted stations to polygons for network splitting.
    - The river line was split, and distances along the network between survey sites and connected gauging stations were calculated; nearest station assigned to each site.
    - NRFA flow stations were matched to fish sites using ArcGIS (ArcGIS Desktop/Pro, v10.8+).
  - Data extraction and statistics
    - Data extracted for NRFA stations with daily flow records exceeding the period of interest.
    - Time series from appropriate NRFA stations extracted for 12 months prior to each fish survey.
    - Period-of-record statistics calculated across the full period (earliest date minus largest preceding period to most recent date).
    - Threshold statistics calculated for 3-, 6-, and 12-month periods preceding each survey (5/25/75/95 percentiles).
  - Software and tools
    - ArcGIS for visualization; Python 3 for network matching and data extraction (modules: os, shapely, pandas, geopandas, matplotlib, numpy, network, warnings).
  - QA and validation
    - Site matching was manually checked due to errors encountered in automated Python matching; manual verification ensured data integrity.

- Data quality and provenance
  - Quality assurance: manual verification of site-to-station matches; some automated matching issues required human review.
  - Source and authorship: dataset produced by Virginie Keller (CEH) and Rachel Ainsworth (University of Hull) with contributions from additional authors; data cited as Ainsworth et al. 2024 (NERC EDS EIDC).
  - Licensing and access: © UKCEH; Waterbodies in Great Britain contain OS data and public sector information licensed under the Open Government Licence v3.0. Crown copyright and database rights EMOU206.
  - Public access: data and related materials available via https://nrfa.ceh.ac.uk/data/search.

- Relationships and related data
  - Fish_SiteID in this dataset matches Fish_SiteID in other data tables (DataTable, SiteTable, chemical determinands).
  - No new data beyond the region CSVs described; no multiple versions reported.

- Usage and integration for GIS workflows
  - Suitable for creating map-based data products that show spatial patterns in fish abundance, habitat, water quality, and flow context.
  - Data designed to be visualized in GIS (ArcGIS) with accompanying network-based analyses to interpret hydrological context around fish survey sites.
  - Regions and matching enable integration with other site-level tables and chemical determinands for comprehensive spatial analysis.