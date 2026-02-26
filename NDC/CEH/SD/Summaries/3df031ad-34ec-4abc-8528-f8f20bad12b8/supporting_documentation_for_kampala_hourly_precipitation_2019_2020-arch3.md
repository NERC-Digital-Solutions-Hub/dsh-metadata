# Supporting documentation for Kampala Hourly Precipitation 2019-2020

## Overview
- Hourly precipitation (mm) recorded around Kampala from April 2019 to March 2020 using Davis Vantage VUE Sensor Suites.
- Installations conducted by Makerere University and Newcastle University as part of the Science for Humanitarian Emergencies and Resilience (SHEAR) project, “Towards resilience to pluvial flood events.”
- Data intended to support evaluation of environmental health and resilience, with a focus on informing monitoring and decision-making.

## Data collection and methods
- Sensor network: Davis Vantage VUE sensor suites deployed at distributed points around Kampala (locations shown in Figure 1).
- Timeframe: April 2019 – March 2020.
- Inclusion rule: Only timestamps with data from all sensors are included, resulting in 8,094 records.
- Data completeness: No missing values within the included records.
- Quality control: No quality control procedures applied; no calibration carried out.
- Timestamp format: YYYY-MM-DD hh:mm:ss.
- Location data: Sensor coordinates provided in GeoJSON format.
- Data alignment: CSV column names correspond to the 'id' field in the GeoJSON locations.

## Data structure and access
- CSV file: shear_rain.csv
  - Timestamp (unnamed): time of observation (YYYY-MM-DD hh:mm:ss)
  - Per-station columns: ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse
  - Units: mm (hourly precipitation per station)
- Location metadata: station_locations.geojson
  - Columns include Name (station name) and id (station identifier)
- Web interface: http://shear.ncl.ac.uk/weather
- Source code: https://doi.org/10.5281/zenodo.3949902

## Metadata details
- Table 1: station_locations.geojson
  - Fields: Name (string), id (string)
- Table 2: shear_rain.csv
  - Fields: Timestamp (YYYY-MM-DD hh:mm:ss), ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse
  - Units: mm

## Provenance and governance
- Project context: Science for Humanitarian Emergencies and Resilience (SHEAR) project
- Data sharing: Web-accessible interface and open-source code available; underlying data and metadata structured for reuse
- Potential governance considerations for monitoring frameworks:
  - Absence of QC and calibration introduces uncertainties for policy-driven decisions
  - Data completeness is ensured only by excluding incomplete timestamps, which may affect continuity analyses
  - Metadata is provided, but the lack of explicit quality metrics suggests the need for standardized QA/QC protocols
  - Encourages openness and reproducibility but highlights challenges around data quality, timeliness, and interoperability

## Implications for monitoring frameworks
- Provides a multi-station, hourly precipitation dataset suitable for evaluating flood resilience and environmental health indicators in Kampala.
- To maximize policy utility, consider implementing:
  - Routine QC checks and calibration procedures
  - Comprehensive metadata standards and data provenance updates
  - Clear data governance to facilitate timely data sharing and avoid silos
  - Documentation of data transformation steps to ensure reproducibility and comparability over time