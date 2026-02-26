# Temperature data from Labfacility platinum resistant thermometers (PRTs) - Campbell Scientific CR10X

## Overview
- Sensor dataset of temperature measurements from 10 Labfacility PRTs embedded at multiple depths (1 m to 19 m, at 2 m intervals: 1, 3, 5, 7, 9, 11, 13, 15, 17, 19 m).
- Temperature range for thermometers: -5 to +40 °C.
- Date range covered: 03/11/2006 00:00 to 15/12/2008 14:00.
- Location metadata provided (grid reference, lat/long, elevation) and instrument specifics.

## Spatial and Temporal Scope
- Location: Latitude 53.001555, Longitude -3.8200267, Elevation 460 m.
- Grid reference: SH 77961 46465.
- Temporal coverage: from 03/11/2006 to 15/12/2008 (times in GMT as indicated by field headings).

## Instrumentation and Measurements
- Temperature measurements from 10 Labfacility platinum resistance thermometers (PRTs) housed in stainless steel sheaths.
- Data logger: Campbell Scientific CR10X.
- Depth-structured measurements with temperature recorded at 1 m, 3 m, 5 m, 7 m, 9 m, 11 m, 13 m, 15 m, 17 m, and 19 m.
- Each depth is represented as a separate temperature measurement (e.g., “1m, GMT = °C at 1 metre” through to “19m, GMT = °C at 19 metre”).

## Data Structure and Metadata
- Temperature measurements are organized by depth (multiple depths per time point) and timestamp (GMT).
- Temperature values are in degrees Celsius.
- The dataset includes geographic coordinates and elevation for spatial context.

## Data Quality and Processing Considerations
- Data may require quality assurance, cleaning, and harmonization across depths and time steps.
- Potential data gaps or inconsistencies due to the multi-depth setup and the long time span.
- Standardization of metadata (coordinate reference system, time zone, and sensor calibration details) is advisable for GIS integration.

## GIS Use and Visualization Opportunities
- Create depth-profile maps or cross-sections showing temperature distribution by depth at given times.
- Develop time-enabled (temporal) maps to visualize how subsurface temperatures change over the study period.
- Integrate with other spatial datasets using the provided coordinates for site-specific analyses (e.g., renewable energy, hydrology, or soil temperature studies).

## Practical Recommendations for GIS Specialists
- Verify and document coordinate reference system (likely WGS84) and ensure timestamps are consistently in GMT.
- Align depth fields into a clean, tabular structure suitable for GIS time-series visualization (one row per timestamp with depth columns or a long-form representation).
- Assess data quality flags or calibration notes from the data logger and sensor metadata before analysis.
- Consider grouping by depth or creating stacked visualizations to convey vertical temperature structure effectively.