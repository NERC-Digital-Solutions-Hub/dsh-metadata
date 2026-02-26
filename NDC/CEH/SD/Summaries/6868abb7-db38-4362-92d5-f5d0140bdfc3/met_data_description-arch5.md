# Supporting Documentation

## Overview
- Datasets described: Hampshire Avon soil temperature and water content data from three sub-catchments (two dataset entries with identical descriptions).
- Depositor: James Stockdale; Contact: james.stockdale@york.ac.uk

## Datasets included
- met_data.csv
  - Time coverage: 02 Dec 2013 to 02 Sep 2015
  - Description: Soil temperature and volumetric water content from plots at three contrasting geologies
  - Locations (OS Grid References):
    - Chalk: ST 85862 38261
    - Clay: ST 92218 27263
    - Greensand: SU 09720 57896

## Dataset structure
- datetime: date and time of measurement conclusion (format ddmmmyyyy:hh:mm:ss)
- site: two-character site code (CH = Chalk; CL = Clay; Greensand)
- plot: plot number for each measurement
- treatment: two-character code (CO = Control; warming)
- temp: soil temperature in °C
- moisture: volumetric water content in m3 m-3

## Methods
- Sampling design: Plots with lysimeters in unimproved pastures across three underlying geologies in the Hampshire Avon catchment
- Sensors:
  - Temperature: single thermistors (ST1, Delta-T Devices)
  - Moisture: theta probes (ML2, Delta-T Devices)
- Data collection: Hourly mean values recorded using data loggers (GP1 and DL2e)
- Quality control: Post-measurement QC to remove failed sensors (commonly due to animal damage)

## Data quality and governance considerations
- Metadata clarity: explicit variable descriptions, codes for site and treatment, and precise units
- Data integrity: QA step documented to exclude faulty sensor data
- Interoperability notes: codes and structured fields facilitate integration across systems; location references provided as OS grid coordinates
- Limitations: potential data gaps due to sensor failures/animal damage; historical time period (2013–2015)

## Access and custodianship
- Custodian/depositor: James Stockdale
- Contact information provided for data requests and clarifications
- Deposited data described for sharing and reuse; explicit mention of data identifiers (file name met_data.csv) and location references

## Data stewardship takeaways
- Ensure metadata remains aligned with current standards (codes, units, date-time format, site geologies)
- Maintain QA flags or notes to document any sensor-related data exclusions
- Preserve provenance: dataset provenance includes collection methods, sensor types, depths, and loggers
- Facilitate discoverability by mapping OS grid references to geographic locations and documenting geologies for each site
- Provide clear data-use guidance and potential limitations to dataset users (e.g., potential gaps from animal damage)