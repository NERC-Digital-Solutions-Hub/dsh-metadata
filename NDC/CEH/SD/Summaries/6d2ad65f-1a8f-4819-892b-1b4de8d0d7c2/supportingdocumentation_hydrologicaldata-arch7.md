# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Daily measurements of river flow velocity (m/s), river discharge (m3/s), river depth (cm), and river width (m) for the Portoviejo River, Ecuador, collected in 2021 and 2022.
- Generated as part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, which monitors hydrological conditions alongside anthropogenic litter collection using the Azure System by Ichthion Limited.

## Experimental design / sampling regime
- Location: Portoviejo River, Ecuador at 1°01'23.9"S, 80°29'35.6"W.
- Timeframe: January 2021 – December 2022 for River_Flow_Velocity and River_Depth; January 2021 – March 2022 for River_Discharge and River_Width.
- Data coverage: aligned with operative days of the Azure System, excluding weekends and bank holidays.

## Collection methods
- River flow velocity: calculated from distance traveled by a reference buoy divided by travel time; three replicates; average used as final velocity.
- River discharge: velocity multiplied by river cross-sectional area.
- River depth: measured twice daily (8:00 am and 4:30 pm) using a fixed limnimeter.
- River width: measured daily with a measuring tape at 90° to river margins at five equidistant points; average of measurements used as daily width.

## Quality control
- Data collection supervised by lead engineer Desiree G. Hidalgo (Ichthion); data assembly, revision, and reporting managed within Ichthion.
- Data interpretation and analysis performed by Dr. Lara Pinheiro (University of Exeter).

## Data structure
- Single CSV file: HydrologicalData_PortoviejoRiver.csv
- Columns: Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity, River_Discharge, River_Depth, River_Width
- Data availability: N/A entries indicate days with no data.
- Units:
  - Latitude/Longitude: decimal degrees with N/S or E/W indicators, 3 decimals
  - River_Flow_Velocity: meters per second (m/s)
  - River_Discharge: cubic meters per second (m3/s)
  - River_Depth: centimeters (cm)
  - River_Width: meters (m)

## Notes and provenance
- Part of a broader effort to monitor plastic leakage impacts and litter collection alongside hydrological measurements.
- Data file formats and collection align with GIS-ready attributes suitable for spatial analyses and map-based visualisations.