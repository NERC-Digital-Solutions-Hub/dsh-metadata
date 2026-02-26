# Supporting documentation for Kampala Hourly Precipitation 2019-2020

## Overview
- Hourly precipitation (mm) recorded at distributed sensors around Kampala from April 2019 to March 2020.
- Data collected using Davis Vantage VUE Sensor Suites.
- Collected by researchers from Makerere University and Newcastle University as part of the Science for Humanitarian Emergencies and Resilience project “Towards resilience to pluvial flood events.”
- 8094 records in total; no missing values reported in the dataset.
- No quality control procedures or calibration performed prior to release.

## Data structure and content
- Timestamps are recorded as YYYY-MM-DD hh:mm:ss.
- Geographic sensor coordinates provided in GeoJSON format.
- CSV file shear_rain.csv contains:
  - Timestamp (unnamed) column
  - Hourly precipitation at each station: ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse
  - Units for precipitation: mm
- Metadata for stations is in station_locations.geojson (name and id mapping).

## Access and provenance
- Web interface to view the data: http://shear.ncl.ac.uk/weather
- Source code available for download: https://doi.org/10.5281/zenodo.3949902

## Data structure details
- The CSV column names for stations correspond to the id field in the GeoJSON station metadata.
- Station metadata includes: Name, id (string).
- Timestamp column is aligned across all sensors, with records included only when data existed for all sensors.

## Usage guidance and considerations
- Useful for analysing rainfall patterns and flood risk at multiple points around Kampala.
- Can be combined with other data sources to create data products (e.g., dashboards, reports) for end users or stakeholders.
- Given no QC or calibration, users should perform their own validation and quality checks for critical analyses.

## Limitations and caveats
- No quality control procedures applied; no calibration performed.
- Only timestamps where all sensors had data are included, which may affect coverage.
- Timezone information is not specified; users should verify time reference when integrating with other datasets.

## Metadata and replication notes
- Data product includes both raw observations and machine-readable metadata (GeoJSON for locations; CSV for observations).
- Availability of web interface and downloadable source code facilitates exploration, replication, and extension of the dataset.