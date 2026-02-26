# Supporting documentation for Kampala Hourly Precipitation 2019-2020

## Overview
- Hourly precipitation (mm) recorded at distributed points around Kampala from April 2019 to March 2020.
- Data collection using Davis Vantage VUE Sensor Suites by researchers from Makerere University and Newcastle University as part of the Science for Humanitarian Emergencies and Resilience project “Towards resilience to pluvial flood events.”
- 8094 records in total with no missing values; no quality control procedures or calibration applied.
- Timestamps are formatted as YYYY-MM-DD hh:mm:ss.
- Sensor geographic coordinates provided in GeoJSON; CSV column names correspond to the ‘id’ field in the GeoJSON.
- A web interface for viewing the data is available at http://shear.ncl.ac.uk/weather; source code is accessible via a DOI: https://doi.org/10.5281/zenodo.3949902.
- Figure 1 illustrates sensor locations; Tables 1 and 2 provide metadata for station locations and precipitation data per station.

## Data structure and contents
- station_locations.geojson contains station metadata (name and id).
- shear_rain.csv contains hourly precipitation measurements with columns: ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse; units are millimetres.
- Timestamp column records the observation time (unnamed in the CSV).
- Each station column corresponds to a station ID defined in the GeoJSON, enabling traceability between measurements and locations.
- Stations named: ACTogether-HQ, Makerere, MengoSS, RC-ClimateCentre, RC-Warehouse.

## Data quality and cautions
- No quality control or calibration has been performed on the data.
- Data are included only for timestamps where all sensors recorded data (i.e., synchronized observations).
- Although there are no missing values in the 8094 records, the lack of QC and calibration means careful validation is required before use in critical analyses.
- Metadata is limited to basic station IDs and names; detailed sensor maintenance or siting information is not provided.
- Data accessibility is straightforward (web interface and downloadable source), but standardization and provenance documentation could be enhanced for broader reuse.

## Access and reuse
- Web viewing interface: http://shear.ncl.ac.uk/weather
- Source code and data provenance available via DOI: https://doi.org/10.5281/zenodo.3949902
- Geographic and tabular data are aligned to support spatial analysis (GeoJSON coordinates linked to CSV station IDs).

## Relevance for data strategy (Data Leaders perspective)
- Demonstrates end-to-end data lifecycle: collection, storage in structured CSV, spatial linkage via GeoJSON, and public-facing access tooling.
- Emphasizes the importance of robust metadata alignment between data files and spatial definitions to ensure discoverability and traceability.
- Highlights a key data quality gap (absence of QC/calibration) that requires explicit consideration and remediation for reliable decision-making.
- Provides a potential data product with co-ownership opportunities for policy and technical teams, through transparent data gathering and open access.
- Illustrates the need for ongoing data quality assurance, documentation of provenance, and standardization to reduce data gaps and improve reuse across networks.