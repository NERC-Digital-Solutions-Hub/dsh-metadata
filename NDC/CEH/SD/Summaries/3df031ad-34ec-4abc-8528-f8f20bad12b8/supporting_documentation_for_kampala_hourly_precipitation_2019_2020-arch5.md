# Supporting documentation for Kampala Hourly Precipitation 2019-2020

## Overview
- Hourly precipitation (mm) recorded around Kampala from April 2019 to March 2020 using Davis Vantage VUE Sensor Suites.
- Collected by Makerere University and Newcastle University as part of the Science for Humanitarian Emergencies and Resilience (SHER) project “Towards resilience to pluvial flood events.”
- 8094 records in total; no missing values; no quality control procedures or calibration performed.
- Timestamps are recorded as YYYY-MM-DD hh:mm:ss.
- Geographic sensor coordinates provided in GeoJSON; CSV column names correspond to the GeoJSON id field.
- Web interface for viewing the data: http://shear.ncl.ac.uk/weather
- Source code/data portal available via https://doi.org/10.5281/zenodo.3949902.

## Data content and structure
- Sensors: Davis Vantage VUE Sensor Suites installed at multiple locations around Kampala (locations shown in Figure 1).
- Data file formats:
  - shear_rain.csv: hourly precipitation (mm) per station; columns include ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse.
  - station_locations.geojson: metadata for sensor locations; includes station name and id.
- Timestamp format: YYYY-MM-DD hh:mm:ss.
- Unit of measurement: millimeters (mm).
- Mapping: CSV columns align with the id field in the GeoJSON locations file.

## Provenance and access
- Data collected as part of a humanitarian resilience project.
- Access points:
  - Web viewer: http://shear.ncl.ac.uk/weather
  - Source code and data hosting: Zenodo DOI provided (https://doi.org/10.5281/zenodo.3949902)

## Quality, standards, and limitations
- No quality control (QC) procedures applied.
- No calibration performed on sensors.
- Only include timestamps when data from all sensors was available; potential data loss due to sensor outages not represented in the dataset.
- No explicit uncertainty metrics or calibration status documented.
- Metadata includes basic station and measurement descriptors, but additional quality metadata is not described.

## Metadata, provenance, and governance considerations
- Clear linkage between sensor locations (station_locations.geojson) and measurements (shear_rain.csv) via the id field.
- Timestamp standardization and per-station precipitation values provided with explicit units (mm).
- Data are hosted with a web interface and an openly accessible repository, supporting discoverability and reuse.

## Implications for data reuse and sharing
- Usable for temporal analyses of rainfall patterns across Kampala on an hourly scale.
- Suitable for integration into portals or catalogs; references to a public web interface and code repository support reproducibility.
- Stewardship considerations include documenting QC/calibration, uncertainties, and data collection workflows to improve reliability for future reuse.

## Practical considerations for Data Stewards
- Timeliness: dataset represents a specific period (Apr 2019–Mar 2020) with complete sensor data only; future updates or ongoing collection would require governance around update protocols.
- Metadata completeness: basic metadata present; may need expanded quality and provenance metadata for broader user communities.
- Interoperability: data in CSV/GeoJSON formats with IDs aligned to locations facilitates integration but requires consistent schema during sharing and cataloging.
- Scalability: dataset is of modest size (8094 records) but involves multiple sensors and formats, illustrating challenges around multi-system interoperability.