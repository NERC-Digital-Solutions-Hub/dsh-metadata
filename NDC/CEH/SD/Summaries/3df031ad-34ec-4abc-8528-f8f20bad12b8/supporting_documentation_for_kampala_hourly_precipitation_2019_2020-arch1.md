# Supporting documentation for Kampala Hourly Precipitation 2019-2020

- Data collection and scope
  - Hourly precipitation (mm) recorded at distributed points around Kampala from April 2019 to March 2020.
  - Sensors: Davis Vantage VUE Sensor Suites installed by researchers from Makerere University and Newcastle University.
  - Project context: Science for Humanitarian Emergencies and Resilience, focusing on resilience to pluvial flood events.
  - Only timestamps with data from all sensors are included (complete-case approach).

- Data volume and completeness
  - Total records: 8,094
  - Missing values: none reported
  - No quality control procedures or calibration; dataset comprises raw observations.

- Data format and structure
  - station_locations.geojson: metadata for sensor locations (station name, id, and geographic coordinates).
  - shear_rain.csv: hourly precipitation per station with columns corresponding to station IDs (ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse) and a timestamp column.
  - Timestamp format: YYYY-MM-DD hh:mm:ss.
  - Units: precipitation in millimeters (mm) per station.

- Data relationship and accessibility
  - Station IDs in the CSV correspond to the IDs in the GeoJSON metadata, enabling spatial joins.
  - Web interface to view the data: http://shear.ncl.ac.uk/weather
  - Source code and data access: https://doi.org/10.5281/zenodo.3949902

- Considerations for analysts
  - Analyses can explore spatial and temporal rainfall patterns across Kampala at hourly resolution.
  - The absence of quality control and calibration means results should consider potential sensor biases and unvalidated observations.
  - Complete-case requirement (only times with all sensors) may affect temporal coverage and analyses of missingness.
  - Spatial scope is limited to the included sensor locations; extrapolation beyond these points should be approached with caution.
  - Data can be joined with the GeoJSON metadata via station IDs for mapping and regional analyses.