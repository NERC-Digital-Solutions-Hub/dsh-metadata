# Documentation

## Overview
- Describes the dataset "Hydro-epidemiological datasets for a selection of place studies".
- Combines geospatial place studies (polygons) with time-series leptospirosis cases (CSV) and hydrometeorological variables (precipitation, discharge, soil moisture).
- Geographic scope includes Chinese provinces (with some provinces omitted due to zero cases) and multiple international place studies, with varying temporal resolutions (weeks to months).

## Data Components
- Places
  - GeoJSON collection of place-study polygons; polygons represent spatial extents where hydrometeorological indicators are averaged and leptospirosis cases are recorded.
  - Polygons have vertices in degrees latitude/longitude.
- Cases
  - CSV files with weekly or monthly leptospirosis case counts per place study.
  - For many Chinese provinces, two CSVs exist: total monthly cases and optional age-stratified data in [province name]_casesByAge.csv.
  - Some provinces (Ningxia, Qinghai, Shanghai, Tianjin) have no files because zero cases were reported 2004–2017.
  - Sources: official Chinese statistics (in Chinese) for Chinese provinces; for other places, various sources summarized in a detailed table (diagnosis type, digitisation status, area, remarks, references).
- Hydrometeorological variables
  - Precipitation (daily, mm) from CHIRPS (0.05° resolution).
  - Discharge (daily, m³/s) from GloFAS-ERA5 reanalysis (0.1° resolution).
  - Soil moisture (daily, relative volumetric content) from ESA CCI Soil Moisture v05.2 (0.25° resolution).
  - Each variable has its own directory; file names start with the place name; first column is 'datum' (date), second column is the value; missing data indicated as NA.

## Data Collection and Generation
- Polygons
  - Chinese provinces: provided by a collaborating MSc student from official Chinese data stores.
  - Other areas (two Chinese counties and international sites): sourced from OpenStreetMap.
- Case data
  - Chinese provincial data: from official statistics (Chinese language only).
  - Other places: details summarized in a table (length/resolution, diagnosis type, digitised, area, remarks, references).
  - Notes: no data for certain provinces due to zero cases during the covered period.
- Hydrometeorological data
  - Derived by converting raster data to area-weighted daily averages per place study.
  - Precipitation: CHIRPS dataset; Discharge: GloFAS-ERA5; Soil moisture: ESA CCI Soil Moisture.
  - References provided for each data source.

## Units and Data Structure
- Place polygons
  - Polygons with vertices in degrees (lat/long).
- Cases
  - Time series with the first column named 'datum' (date); subsequent columns contain case counts (one column or multiple columns by age bracket, age brackets denoted with lowest_highest age, separated by an underscore).
- Hydrometeorological variables
  - Precipitation: daily rainfall in mm.
  - Discharge: daily average discharge in m³/s.
  - Soil moisture: daily relative volumetric content.
- File organization
  - Hydrometeorological data: separate directories for each variable; file names begin with the place name.
  - Case data: per-place CSVs; age-stratified files named [place]_casesByAge.csv where applicable.
  - NA entries indicate missing data for that place and time.

## Quality Control and Provenance
- Geospatial data are open source or from official sources.
- Case data quality: derived from health department statistics or peer-reviewed literature.
- Hydrometeorological data quality: widely used, peer-reviewed datasets; specific references cited for CHIRPS, GloFAS-ERA5, and ESA CCI Soil Moisture.

## Temporal and Geographic Coverage
- China: multiple provinces with time-series data; Ningxia, Qinghai, Shanghai, and Tianjin not included due to zero reported cases in the period.
- Other sites: Salvador (Brazil), Negeri Sembilan (Malaysia), Manila (Philippines), Florianópolis (Brazil), Parana/ Rosario/Santa Fe/Gualeguaychú (Argentina), Yilong/Mengla (China), Anuradhapura/Nuwara Eliya/Ratnapura/Galle (Sri Lanka), and others; each site has varying temporal resolution (weeks to months) and geographic area.

## Governance and Stewardship Considerations
- Metadata and provenance: dataset includes sourcing details (official statistics, OpenStreetMap, peer-reviewed sources) and references for hydrometeorological inputs.
- Standards and interoperability: uses standard formats (GeoJSON for spatial data, CSV for time series) with consistent date column ('datum') and explicit age-bracket conventions.
- Updates and maintenance: data are drawn from diverse sources with potentially different update cadences; maintainers should document versioning and update schedules.
- Licensing and access: sources are labeled as open data or official; ensure ongoing compliance with licensing when reusing or redistributing.
- Handling of limitations: dataset acknowledges incomplete user-need picture, data timeliness, standardization across many systems, large size, and the need for bespoke solutions where data are older or non-interoperable.

## References and Data Sources
- Hydrometeorological datasets and DOIs:
  - CHIRPS precipitation: Funk et al., 2015; Scientific Data; DOI provided.
  - GloFAS-ERA5 discharge: Harrigan et al., 2020; Earth System Science Data Discussions; DOI provided.
  - ESA CCI Soil Moisture: Dorigo et al., 2017; Gruber et al., 2017/2019; DOIs provided.
- Case data sources: health department statistics or peer-reviewed literature; specific place references listed in the detailed table within the document.
- Chinese provincial data: official statistics (Chinese language).