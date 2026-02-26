# Supporting documentation for Kampala Hourly Precipitation 2019-2020

## Overview
- Hourly precipitation (mm) data collected around Kampala from April 2019 to March 2020.
- Collected using Davis Vantage VUE Sensor Suites installed by researchers from Makerere University and Newcastle University.
- Part of the Science for Humanitarian Emergencies and Resilience (SHEAR) project: "Towards resilience to pluvial flood events."
- Only timestamps with data from all sensors are included (8094 records in total).

## Data collection and sensors
- Distributed rain gauges at multiple points around Kampala (Figure 1).
- Sensors: Davis Vantage VUE Sensor Suites.
- Installation led by Makerere University and Newcastle University.
- Time period: April 2019 – March 2020.
- No quality control procedures or calibration performed.
- Timestamps recorded as YYYY-MM-DD hh:mm:ss.

## Data structure and content
- Data stored in shear_rain.csv; timestamps and hourly precipitation values.
- Geographic coordinates provided in GeoJSON (station_locations.geojson).
- CSV column names correspond to the 'id' field in the GeoJSON file.
- Stations included: ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse.
- Data description:
  - Timestamp (YYYY-MM-DD hh:mm:ss)
  - Hourly precipitation at each station (mm)

## Metadata and access
- Figure 1 shows sensor locations around Kampala district.
- Table 1: Metadata for station_locations.geojson (station name and id).
- Table 2: Metadata for shear_rain.csv (timestamp and hourly precipitation per station).
- Web interface to view the data: http://shear.ncl.ac.uk/weather
- Source code available: https://doi.org/10.5281/zenodo.3949902

## Quality, limitations, and caveats
- No quality control (QC) procedures applied.
- No calibration performed on sensors.
- All records are included only when data from all sensors are available.
- 8094 records with no missing values reported, but underlying sensor issues may affect accuracy due to lack of QC/calibration.

## Relevance for environmental monitoring (Analysts Monitoring the Environment)
- Provides a consistent, standardized dataset of hourly rainfall across multiple Kampala points for environmental health and flood risk monitoring.
- Data can be analyzed to assess precipitation patterns and inform resilience to pluvial flood events.
- Outputs can be generated as reports, maps, and charts; datasets are suitable for storage and portal uploads.
- Encourages integrating this rainfall dataset with other environmental datasets to enhance usefulness and scope.
- Highlights the need for data transparency and access to underlying data to support broader analysis and policy scrutiny.