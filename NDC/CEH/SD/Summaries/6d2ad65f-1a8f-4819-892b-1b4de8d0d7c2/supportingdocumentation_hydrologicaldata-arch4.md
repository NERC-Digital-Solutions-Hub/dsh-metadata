# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Dataset of daily hydrological measurements from the Portoviejo River, Ecuador, covering 2021 and 2022.
- Variables: River Flow Velocity (m/s), River Discharge (m3/s), River Depth (cm), River Width (m).
- Generated as part of the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, aiming to reduce plastic leakage and support sustainable plastics flow.
- Data collected to monitor river hydrological conditions alongside anthropogenic litter data using the Azure System developed by Ichthion Limited.

## Experimental design / Sampling regime
- Location: Portoviejo River, Ecuador (approx. 1°01'23.9"S, 80°29'35.6"W).
- Timeframe:
  - River Flow Velocity and River Depth: January 2021 – December 2022.
  - River Discharge and River Width: January 2021 – March 2022.
- Data coverage aligned with operative days of the Azure System; excludes weekends and bank holidays.

## Collection methods
- River Flow Velocity: calculated from distance travelled by a reference buoy divided by travel time; three replicates per measurement; averaged.
- River Discharge: velocity multiplied by river cross-section area.
- River Depth: measured twice daily (8:00 and 16:30) using a fixed limnimeter.
- River Width: measured daily at 90° from river margins across 5 equidistant points; average taken for daily report.

## Quality control
- Data collection supervised by lead engineer Desiree G. Hidalgo (Ichthion); field officers collected data.
- Data assembly and reporting performed by Desiree G. Hidalgo; data interpretation and analysis by Dr. Lara Pinheiro (University of Exeter).

## Data structure & metadata
- File: HydrologicalData_PortoviejoRiver.csv (Excel format).
- Columns: Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity, River_Discharge, River_Depth, River_Width.
- N/A values indicate days with no data recorded.

## Data coverage & availability
- Continuous daily data for River Flow Velocity and River Depth (2021–2022).
- River Discharge and River Width available for Jan 2021–Mar 2022.
- Data aligned with Azure System operation; gaps indicated by N/A markers.

## File details & units
- Latitude/Longitude: decimal degrees with N/S and E/W indicators; 3 decimals.
- River_Flow_Velocity: meters per second (m/s).
- River_Discharge: cubic meters per second (m3/s).
- River_Depth: centimeters (cm).
- River_Width: meters (m).