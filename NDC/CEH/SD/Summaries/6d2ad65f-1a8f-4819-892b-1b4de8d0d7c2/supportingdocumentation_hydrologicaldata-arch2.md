# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022.

- Overview
  - Daily hydrological measurements for Portoviejo River, Ecuador, 2021–2022.
  - Variables: river flow velocity (m/s), river discharge (m³/s), river depth (cm), river width (m).
  - Collected to monitor hydrological conditions alongside anthropogenic litter data collected with the Azure System (Ichthion Limited).

- Study location and timeframe
  - Location coordinates: 1° 01' 23.9" S, 80° 29' 35.6" W.
  - Temporal coverage:
    - River flow velocity and river depth: January 2021 – December 2022.
    - River discharge and river width: January 2021 – March 2022.
  - Data coverage aligns with operative days of the Azure System (excludes weekends and bank holidays).

- Data collected (variables and units)
  - River_Flow_Velocity: meters per second (m/s).
  - River_Discharge: cubic meters per second (m³/s).
  - River_Depth: centimeters (cm).
  - River_Width: meters (m).
  - Spatial data: Latitude and Longitude for site positioning.
  - Format: single Excel file HydrologicalData_PortoviejoRiver.csv with 10 columns.

- Sampling regime and collection methods
  - River flow velocity:
    - Calculated as distance traveled (m) divided by travel time (s) of a reference buoy.
    - Measurements taken three times as replicates; final velocity is the average.
  - River discharge:
    - Calculated as velocity multiplied by river cross-sectional area.
  - River depth:
    - Measured twice daily (8:00 a.m. and 4:30 p.m.) using a fixed limnimeter.
  - River width:
    - Measured daily with a measuring tape at 5 equidistant points; average computed for daily report.

- Quality control and governance
  - Data collection supervised by lead engineer (Ichthion) Desiree G. Hidalgo.
  - Data assembly, revision, and reporting managed by Desiree G. Hidalgo (Ichthion).
  - Data interpretation and analysis performed by Dr. Lara Pinheiro (University of Exeter).

- Data structure and accessibility
  - File: HydrologicalData_PortoviejoRiver.csv (Excel format).
  - Columns: Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity, River_Discharge, River_Depth, River_Width.
  - Data completeness indicated by N/A for days without data collection.
  - Latitude/Longitude format: decimal degrees with ±N/±S and ±E/±W to three decimal places.
  - Notes on data provenance: part of a broader project addressing plastic waste reduction in the Eastern Pacific; data integration with litter observations via the Azure System.

- Project context and contributors
  - Project: Reducing the impacts of plastic waste in the Eastern Pacific Ocean (NERC-funded).
  - Aim alignment: supports environmental monitoring through standardized hydrological data to assess ecosystem health and inform policy/performance over time.
  - Key teams: Ichthion Limited (Azure System data collection) and University of Exeter (data analysis).