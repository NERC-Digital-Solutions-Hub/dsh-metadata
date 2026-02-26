# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Dataset from an ammonia (NH3) enhancement experiment conducted in a tropical sub-montane forest at Queensberry Estate, central Sri Lanka (coordinates 6.9693°, 80.5911°, altitude 1645 m).
- Objective: study effects of high NH3 in air on forest vegetation, bryophytes, lichens, and soil.
- Data collection period: 13 March 2022 to 31 December 2022; time recorded in Sri Lanka Standard Time (SLST).
- Data product intended for analysis of NH3 deposition/deposition-related ecological responses; detailed methodology and findings described in Deshpande et al. (2024).

## Experimental setup and data collection
- NH3 release system triggered only under specific below-canopy wind conditions to ensure directional exposure toward monitoring quadrats (wind direction sectors and threshold speeds specified).
- Release hardware: three horizontal PVC tubes (20 m long, 110 mm diameter) arranged parallel at heights 0.5, 1.35, and 2.2 m.
- NH3 is released through six evenly spaced holes along each tube via a central manifold fed by a cylinder of pure NH3.
- Control: a solenoid valve and mass flow controller (MFC) regulate NH3 flow; release occurs only when wind conditions are met.
- Measurement: below-canopy wind data from a WXT536 weather station; NH3 volume released recorded every 20 seconds and averaged over 15-minute intervals.
- Data format: 15-minute interval measurements; all data reported in SLST.

## Data structure and variables
- Total observations: 28,257 measurements.
- Primary data columns (CSV): 
  - Timestamp (15-minute intervals, format dd/mm/yyyy hh:mm)
  - NH3_status (0 = OFF, >0 = ON)
  - NH3_flow_set (NH3 flow set point for wind conditions; slpm)
  - NH3_flow (NH3 flow through the MFC into the release manifold; slpm)
  - Wind_speed (below-canopy wind speed; ms^-1)
  - Wind_direction (below-canopy wind direction; degrees)
- Metadata fields accompany each parameter (instrument, manufacturer, and descriptive notes), detailing the measurement context and units.

## Quality control and limitations
- Visual quality checks performed; obvious instrument, datalogger, and power issues removed.
- Some data gaps occurred during replacement of faulty gas-control components.
- Described as part of data provenance, with related methodological details in the cited and accompanying publication.

## Temporal and spatial scope
- Location: Queensberry experimental site, Sri Lanka (forest environment; tropical sub-montane context).
- Timeframe: 13 March 2022 – 31 December 2022.
- Spatial scale: measurements tied to below-canopy conditions at the study site; NH3 release system designed to target exposure toward monitoring quadrats.

## Data format, access, and usage notes
- Data provided as a CSV file with 15-minute resolution.
- Time recorded in Sri Lanka Standard Time (SLST).
- Comprehensive metadata included for each column (instrumentation and descriptions) to aid reuse and integration with other datasets.

## Funding
- Funded by the UKRI GCRF South Asian Nitrogen Hub.

## References
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.

## How this data supports data use and discovery
- Provides a clearly described, wind-controlled NH3 exposure dataset with synchronized NH3 release and below-canopy meteorology, enabling analysis of NH3 exposure effects and deposition estimates.
- Structured with standardized 15-minute intervals and detailed instrument metadata to facilitate data integration, quality assessment, and re-use in dashboards or self-serve analyses.
- Related publication (Deshpande et al., 2024) offers complete methodology, analysis, and findings to contextualize the data and support reproducibility.