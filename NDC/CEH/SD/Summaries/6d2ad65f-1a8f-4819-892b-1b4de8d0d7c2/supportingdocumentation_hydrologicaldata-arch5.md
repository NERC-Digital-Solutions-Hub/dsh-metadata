# Supporting documentation to dataset: Hydrological data from the Portoviejo River, Ecuador, 2021-2022

## Overview
- Daily hydrological measurements for the Portoviejo River, Ecuador, collected in 2021 and 2022.
- Part of the NERC-funded project to reduce plastic waste in the Eastern Pacific; data collected alongside anthropogenic litter monitoring using the Azure System by Ichthion Limited.
- Purpose: monitor hydrological conditions to support environmental assessment and pollution studies, with linkage to plastic waste monitoring.

## Dataset contents and structure
- Variables included: River Flow Velocity (m/s), River Discharge (m3/s), River Depth (cm), River Width (m).
- Metadata fields: Site, Year, Month, Day, Latitude, Longitude.
- File format: single dataset file named HydrologicalData_PortoviejoRiver.csv with 10 columns:
  - Site, Year, Month, Day, Latitude, Longitude, River_Flow_Velocity, River_Discharge, River_Depth, River_Width.
- Data completeness: cells with N/A indicate days when data were not collected.

## Temporal and spatial coverage
- Location: Portoviejo River, Ecuador (approximate coordinates 1°01'23.9"S, 80°29'35.6"W).
- Time period: January 2021 – December 2022 (River Flow Velocity and River Depth data); January 2021 – March 2022 (River Discharge and River Width data).
- Data coverage aligned with operative days of the Azure System; excludes weekends and bank holidays.

## Experimental design and data collection methods
- River Flow Velocity: calculated from distance traveled by a reference buoy divided by travel time; measurements replicated three times; final velocity is the average of replicates.
- River Discharge: calculated as River Flow Velocity multiplied by river cross-sectional area.
- River Depth: measured twice daily at 08:00 and 16:30 using a fixed limnimeter.
- River Width: measured daily with a measuring tape at 90° to the river margins across five equidistant points; average computed for daily value.
- Location data is included to enable geospatial analyses.

## Quality control and provenance
- Data collection supervised by lead engineer Desiree G. Hidalgo (Ichthion); data assembly and reporting handled within Ichthion.
- Data interpretation and analysis conducted by Dr. Lara Pinheiro (University of Exeter).
- Documentation indicates collaboration across Ichthion and Exeter, supporting traceability from collection to analysis.

## Data formatting and standards
- 10-column CSV/Excel-style dataset with clearly defined units:
  - Latitude and Longitude: decimal degrees with three decimals; N/S and E/W qualifiers.
  - River_Flow_Velocity: meters per second (m/s).
  - River_Discharge: cubic meters per second (m3/s).
  - River_Depth: centimeters (cm).
  - River_Width: meters (m).
- Explicit note that N/A entries denote non-collection days.

## Considerations for data reuse and governance
- Practical gaps: non-collection days (weekends/bank holidays) result in incomplete daily series; users should account for these gaps during analysis.
- Methodology details (buoy-based velocity, cross-sectional area for discharge, dual-depth measurements) support reproducibility but require access to ancillary details (e.g., cross-sectional area) if recalculating derived metrics.
- Dataset is tied to a broader project on plastic pollution; consider any data sharing restrictions or licensing as per project governance.
- Key stewardship needs: maintain provenance, ensure ongoing metadata availability, track data updates, and document any methodological changes to preserve interoperability with other hydrological and pollution datasets.