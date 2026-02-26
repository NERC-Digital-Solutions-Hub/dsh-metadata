# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Dataset of daily hydrological measurements for the Portoviejo River, Ecuador, covering 2021 and 2022.
- Variables: river flow velocity (m/s), river discharge (m3/s), river depth (cm), and river width (m).
- Generated as part of the NERC-funded project “Reducing the impacts of plastic waste in the Eastern Pacific Ocean,” which aims to reduce plastic leakage and support sustainable plastics resource flows.
- Data collected alongside anthropogenic litter data using the Azure System (Ichthion Limited).

## Experimental design / Sampling regime
- Location: Portoviejo River, Ecuador (coordinates provided).
- Timeframe:
  - River flow velocity and river depth: January 2021 – December 2022.
  - River discharge and river width: January 2021 – March 2022.
- Data coverage aligned with operative days of the Azure System, excluding weekends and bank holidays.

## Data collection methods
- River flow velocity: calculated from distance traveled by a reference buoy divided by travel time, with three replicates and an average.
- River discharge: velocity multiplied by river cross-section area.
- River depth: measured twice daily (8:00 and 16:30) using a fixed limnimeter.
- River width: measured daily at 90° to river margins at five equidistant points; average computed for daily value.

## Quality control
- Data collection supervised by lead engineer Desiree G. Hidalgo (Ichthion).
- Data assembly and reporting handled by Ichthion team; data interpretation and analysis by Dr. Lara Pinheiro (University of Exeter).

## Data structure and metadata
- File: HydrologicalData_PortoviejoRiver.csv (Excel format).
- Columns: Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity, River_Discharge, River_Depth, River_Width.
- Data quality: 'N/A' indicates days with no data.
- Units:
  - Latitude/Longitude: decimal degrees with 3 decimal places (Latitude: +/- N/S; Longitude: +/- E/W).
  - River_Flow_Velocity: meters per second (m/s).
  - River_Discharge: cubic meters per second (m3/s).
  - River_Depth: centimeters (cm).
  - River_Width: meters (m).

## Data governance and sharing context
- Dataset is associated with a broader research program on environmental health and plastic waste, emphasizing data quality, transparency, and linkage to ancillary litter data.
- Metadata and data provenance are documented to facilitate verification and reuse.
- Public sharing considerations noted as a potential barrier in some contexts; dataset documentation provides clarity on data collection, quality control, and structure to support governance and reuse.

## Potential uses for monitoring frameworks
- Provides standardized hydrological indicators for policy evaluation and decision-making.
- Methodology supports reproducibility and comparability across monitoring sites and programs.
- Can be integrated with litter data (Azure System) to assess links between hydrology and plastic pollution dynamics.
- Supports quality assurance processes, data cleaning, and clear presentation through reports or dashboards.

## Limitations and caveats
- Data gaps indicated by N/A entries; not all days have complete measurements.
- Discharge and width data limited to January 2021 – March 2022; velocity and depth extend through 2022.
- Coverage excludes weekends and bank holidays (Azure System constraint), which may affect temporal representativeness.
- Location-specific dataset; careful extrapolation advised for broader regional assessments.