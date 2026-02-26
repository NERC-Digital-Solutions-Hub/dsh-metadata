# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022.

## Purpose and project context
- Part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, aiming to reduce plastic leakage and support sustainable plastics management.
- Data collected to monitor river hydrological conditions alongside measurements of anthropogenic litter using the Azure System developed by Ichthion Limited.

## Data coverage and scope
- Location: Portoviejo River, Ecuador (coordinates provided).
- Timeframe:
  - River flow velocity and river depth: January 2021 – December 2022.
  - River discharge and river width: January 2021 – March 2022.
- Data coverage aligns with operative days of the Azure System (excludes weekends and bank holidays).

## Experimental design
- Daily collection regime for the specified hydrological parameters.
- Data structured to reflect calendar date with geographic coordinates and measured variables.

## Collection methods
- River flow velocity:
  - Calculated as distance travelled by a reference buoy divided by travel time (s).
  - Three replicates; final velocity is the average of replicates.
- River discharge:
  - Calculated as velocity multiplied by river cross-section area.
- River depth:
  - Measured twice daily (8:00 and 16:30) using a fixed limnimeter.
- River width:
  - Measured daily with a measuring tape at 90° to the margins across five equidistant points; average taken for daily report.

## Quality control and data provenance
- Data collection supervised by expert lead engineer during fieldwork.
- Field officers from Ichthion collected data; lead field engineer Desiree G. Hidalgo supervised data assembly, revision, and reporting.
- Data interpretation and analysis handled by Dr. Lara Pinheiro (University of Exeter).

## Data structure and file details
- File: HydrologicalData_PortoviejoRiver.csv
- Columns (10): Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity, River_Discharge, River_Depth, River_Width
- Data gaps:
  - Cells marked as N/A indicate days with no data collection.
- Units and formats:
  - Latitude/Longitude: degrees with 3 decimals (positive/negative for hemispheres).
  - River_Flow_Velocity: meters per second (m/s).
  - River_Discharge: cubic meters per second (m3/s).
  - River_Depth: centimeters (cm).
  - River_Width: meters (m).