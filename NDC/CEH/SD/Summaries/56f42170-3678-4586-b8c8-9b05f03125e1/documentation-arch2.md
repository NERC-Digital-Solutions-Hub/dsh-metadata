# Documentation

## Overview
- Description of data files and creation process for the dataset "Hydro-epidemiological datasets for a selection of place studies."
- Combines geo-spatial place studies with hydrometeorological indicators and leptospirosis case data to enable temporal and spatial monitoring of environmental health.

## Data components

- Places
  - Collection of geojson files; each feature is a place study as a spatial polygon.
  - Hydrometeorological indicators are averaged over the polygon; leptospirosis cases are registered within the polygon.
  - Vertex coordinates are in degrees (longitude/latitude).
  - Polygons for China provinces provided from official data store; smaller areas in China and other countries sourced from OpenStreetMap.

- Cases
  - Collection of csv files with weekly or monthly leptospirosis case counts for each place study.
  - For many Chinese provinces, two files exist: total cases per month and cases by age group (filename format [province name]_casesByAge.csv).
  - Some areas have no data ( Ningxia, Qinghai, Shanghai, Tianjin) due to zero cases 2004-2017.
  - Case data sources include health statistics (official) and peer-reviewed literature; years and aggregation vary by study.
  - Data definitions: first column is the date; subsequent columns are counts (one column or multiple by age bracket, labeled by age range).

- Hydrometeorological variables
  - Raster-derived variables converted to area-weighted daily averages per place study.
  - Precipitation: daily rainfall in mm (CHIRPS data, 0.05° resolution).
  - Discharge: daily average discharge in m^3/s (GloFAS-ERA5 reanalysis, 0.1° resolution).
  - Soil moisture: daily relative volumetric soil moisture content (ESA CCI Soil Moisture v05.2, 0.25° resolution).
  - Each variable has its own directory; file names begin with the place name; first column 'datum' is the date; second column is the value; NA indicates missing data.

- Data structure
  - Standard geojson format for places.
  - For hydrometeorological data, each file corresponds to a place and variable; time-series data are organized with a single data column per file.

## Collection and generation methods

- Places
  - Chinese provinces polygons from an official data store via a collaborating MSc student.
  - Smaller Chinese areas (2 counties) and other countries’ polygons sourced from OpenStreetMap using relevant search results.

- Cases
  - Chinese provincial data derived from official statistics (Chinese language only); some years or provinces partially digitised.
  - For non-Chinese places, data collection details are summarized in a multi-place table (includes duration, resolution, diagnosis type, digitisation, area, remarks, and references).

- Hydrometeorological variables
  - Source rasters converted to area-weighted daily averages for each place study.
  - Precipitation from CHIRPS; discharge from GloFAS-ERA5; soil moisture from ESA CCI.
  - Key references provided for each data source.

## Quality control and provenance

- Geospatial data are open source or from official sources.
- Hydrometeorological and case data come from widely used, peer-reviewed data products or official statistics.
- Data are organized to enable traceability from source to place study outputs.

## Details of data structure and organization

- Places
  - Directory per variable; file names begin with the place name.
  - Each file's first column is 'datum' (date); subsequent columns contain the averaged indicators.

- Cases
  - Files contain date in the first column and case counts in subsequent columns (by total or by age bracket).
  - Age-bracket columns are labeled with the corresponding age range (e.g., a_5_14).

- NA handling
  - NA values indicate missing data for a given place and time in a dataset.

## Place studies (examples)

- Salvador, Brazil; Negeri Sembilan, Malaysia; Manila, Philippines; Florianópolis, Brazil; Parana/Rosario/Santa Fe/Gualeguaychú, Argentina; Yilong/Mengla, China; Anuradhapura/Nuwara Eliya/Ratnapura/Galle, Sri Lanka.
- Studies vary in length, resolution, diagnosis type (clinical/confirmed), digitisation status, area, and remarks. Some provide possible and confirmed cases; others rely on hospital or surveillance data.
- The table outlines study-specific details such as duration, spatial resolution, data digitisation, and references.

## Relevance for Analysts Monitoring the Environment

- Supports standardized, time-resolved monitoring of environmental health by linking geospatial regions with hydrometeorological context and disease outcomes.
- Enables cross-site comparisons and trend analysis over multiple time scales (weekly to monthly, depending on the place study).
- Provides clear data provenance (source references, collection methods) and quality indicators (open/official data, peer-reviewed sources).
- Facilitates data integration by using uniform formats (geojson for places, csv for cases, daily time series for hydrometeorology) and explicit handling of missing data.
- Aligns with aims to verify, quality-assure, and transform data into outputs usable for policy performance assessment and environmental health scrutiny over time.