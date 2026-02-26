# Supporting documentation for Kampala Hourly Precipitation 2019-2020

- Time period and purpose: Hourly precipitation (mm) recorded around Kampala from April 2019 to March 2020 using Davis Vantage VUE Sensor Suites, installed by Makerere University and Newcastle University as part of the Science for Humanitarian Emergencies and Resilience project “Towards resilience to pluvial flood events.”
- Coverage and records: 8094 records in total with no missing values; only timestamps where data were available from all sensors are included.
- Data quality notes: No quality control procedures were applied and no calibration was carried out.
- Timestamps: Recorded as YYYY-MM-DD hh:mm:ss.

## Data content and structure

- Sensor network: Locations around Kampala (stations include ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse).
- Files provided:
  - station_locations.geojson: geographic coordinates of sensors; IDs correspond to the CSV data.
  - shear_rain.csv: hourly precipitation data per station.
- CSV schema (shear_rain.csv):
  - Timestamp (unnamed): time of observation, units = YYYY-MM-DD hh:mm:ss.
  - ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse: hourly precipitation at each station, units = mm.
- GeoJSON schema (station_locations.geojson):
  - id: station ID (string), used to join with shear_rain.csv.
  - name: station name (string).

## Access, provenance, and references

- Web interface for viewing the data: http://shear.ncl.ac.uk/weather
- Source code and data package download: https://doi.org/10.5281/zenodo.3949902
- Figure: Location map of sensors around Kampala district (Figure 1).

## How to use in GIS

- Join shear_rain.csv to station_locations.geojson on the id field to map hourly precipitation by station.
- Create map-based visualizations of spatial precipitation patterns, trends over time, and identify hotspots or temporal spikes.
- Be mindful of data quality limitations (no calibration or QC performed) when interpreting results or comparing sensors.

## Metadata details

- Table 1 (station_locations.geojson): 
  - Name (Description = station name; Type = String)
  - id (Description = weather station ID; Type = String)
- Table 2 (shear_rain.csv):
  - Timestamp (unnamed) (Description = observation time; Units = YYYY-MM-DD hh:mm:ss)
  - ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse (Description = hourly precipitation at each station; Units = mm)