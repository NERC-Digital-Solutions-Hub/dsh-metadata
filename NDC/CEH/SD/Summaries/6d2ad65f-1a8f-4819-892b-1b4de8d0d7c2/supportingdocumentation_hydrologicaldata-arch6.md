# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Dataset of daily measurements: River Flow Velocity (m/s), River Discharge (m3/s), River Depth (cm), River Width (m).
- Timeframe: 2021–2022 (velocity and depth Jan 2021–Dec 2022; discharge and width Jan 2021–Mar 2022).
- Generated under the NERC-funded project Reducing the impacts of plastic waste in the Eastern Pacific Ocean, to monitor hydrology alongside anthropogenic litter collections using the Azure System by Ichthion Limited.

## Temporal and spatial coverage
- Location: Portoviejo River, Ecuador at 1° 01' 23.9" S, 80° 29' 35.6" W.
- Operative days correspond to Azure System activity (excludes weekends and bank holidays).

## Variables and units
- Columns: Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity (m/s), River_Discharge (m3/s), River_Depth (cm), River_Width (m).
- Latitude/Longitude provided with 3 decimal places; N/A indicates days without data.
- Units: River_Flow_Velocity (m/s), River_Discharge (m3/s), River_Depth (cm), River_Width (m).

## Data collection methods
- Velocity: distance traveled by a reference buoy divided by travel time; three replicates; average used.
- Discharge: velocity multiplied by river cross-sectional area.
- Depth: measured twice daily (8:00 and 16:30) using a fixed limnimeter.
- Width: measured daily at 5 equidistant points along a perpendicular to the margins; average used for daily report.

## Data quality and governance
- Supervision by lead engineer Desiree G. Hidalgo (Ichthion); data assembly and reporting by Ichthion; data interpretation/analysis by Dr. Lara Pinheiro (University of Exeter).

## Data structure and access
- File: HydrologicalData_PortoviejoRiver.csv with 10 columns as listed above.
- Data gaps indicated by N/A; explicit units/formats provided for each variable.

## Potential uses for data support
- Build dashboards or self-serve data products enabling exploration of hydrological conditions.
- Analyze temporal trends and relationships between velocity, discharge, depth, and width.
- Integrate with Azure System litter data for environmental impact assessments.

## Limitations and considerations
- Gaps on non-collection days; partial coverage for discharge/width data (Jan 2021–Mar 2022).
- Exclusion of weekends/bank holidays may affect continuity.
- Measurements rely on specific instruments (reference buoy, limnimeter) and require cross-sectional area calculations.