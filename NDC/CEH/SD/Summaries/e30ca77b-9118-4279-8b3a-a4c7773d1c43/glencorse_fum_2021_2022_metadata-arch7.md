# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022) Deshpande, A.G., Jones, M.R., Mullinger, N. J., Harvey, D. and Nicoll, R.

## Overview
- Dataset from a controlled NH3 enhancement experiment in the Glencorse woodland near Edinburgh to study ammonia effects on forest vegetation, bryophytes, lichens, and soil.
- Data collected under wind-controlled release conditions between 16 September 2021 and 5 January 2023.
- Aims to support spatial and environmental analyses of ammonia exposure and deposition when integrated with GIS workflows.

## Experimental design and data collection
- NH3 release system: three 20 m long tubes placed horizontally at 0.5, 1.35, and 2.2 m above ground; NH3 delivered via a manifold fed by a mass flow controller and solenoid valve.
- Activation conditions: release occurs when wind is from 275–345 degrees at threshold speeds (0.3–10 m/s) as measured below the canopy.
- Monitoring and control: a WXT536 weather station provides wind data; mass flow controller records NH3 release volume every 20 seconds; 15-minute intervals are averaged.
- Location specifics: Glencorse woodland, coordinates 55.8539°N, -3.2151°W; altitude ~200 m.

## Data structure and variables
- Format: CSV with 45,538 measurements covering five primary parameters.
- Key variables (with typical data types):
  - Timestamp (GMT) for 15-minute intervals
  - NH3_status: release status (0 = OFF, >0 = ON)
  - NH3_flow_set: NH3 flow set point (slpm)
  - NH3_flow: NH3 flow through the MFC (slpm)
  - Wind_speed: below-canopy wind speed (m/s)
  - Wind_direction: wind direction (degrees)
- Additional metadata fields capture instrument, manufacturer, and description details for traceability.

## Data quality and preprocessing
- Visual quality checks performed; obvious instrument malfunctions, datalogger issues, and power cuts corrected or removed.
- Some data gaps remained due to replacement of faulty gas control components.

## Temporal and spatial scope
- Timeframe: 16 September 2021 to 5 January 2023 (GMT timestamps).
- Spatial scope tied to a single experimental site (Glencorse woodland) with wind-directed NH3 release affecting measurements at monitoring quadrats.

## Usage notes for GIS and data integration
- Suitable for mapping NH3 exposure potential, release events, and deposition modelling when combined with wind fields and other environmental layers.
- Data can be joined with other GIS datasets at the site level; be mindful of the five primary variables and the 20-second/15-minute temporal resolutions.
- Consider aligning with the monitoring quadrat locations and canopy structure for spatial analyses.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- References: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. (2024). Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.