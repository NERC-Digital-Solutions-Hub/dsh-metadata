# Water discharge data for Trout Beck, Cumbria. 1961 - 1980

## Overview
- Dataset of water discharge data from Trout Beck, Cumbria, UK.
- Collected by various staff at Moor House Research Station for the Wear and Tees River Board and the NRA; staff names not recorded.
- Stored in a database described by Cuthbertson (1993): A database for environmental research programmes.
- Original units were Imperial and have been converted to metric (cumecs).

## Site location
- Trout Beck Weir located at grid reference 375900 533600.

## Data content and structure
- Key fields:
  - DATID: Recording location (data description varies by ID).
  - REC_TIME: The day represented by the record (date).
  - TCMD: Total Mean Daily Discharge (cumecs).
  - MEAN: The Mean discharge (cumecs).
  - HIGHEST: The highest discharge (cumecs).
  - LOWEST: The lowest discharge during the day (cumecs).
  - HGH_TIME: Hour of the greatest discharge.
  - LOW_TIME: Hour of the lowest discharge.

## Recording locations and temporal resolution
- DATID 39: Trout Beck gauging station.
  - Earliest date: 01-Oct-1961; Last date: 30-Sep-1968.
- DATID 17: TROUTBECK gauging station (recording from Northumbrian Water Authority).
  - Earliest date: 01-Oct-1968; Last date: 30-Jun-1980.
- Data originally in Imperial units, converted to cumecs for consistency.

## Temporal coverage
- Data span from 01-Oct-1961 to 30-Jun-1980, with two distinct recording sites/periods.

## Data quality, notes, and caveats
- Noted a large peak in discharge in March 1979; no accompanying notes in the database.
- Peak may be related to snowmelt after a major UK snow event.
- Metadata about data provenance and staff is limited (names not recorded).

## GIS considerations and data product guidance
- Two recording locations (DATID 39 and 17) require careful harmonization when combining datasets (different periods and possibly differing measurement practices).
- Daily discharge values (TCMD, MEAN) and event timing (HIGHEST, LOWEST with corresponding times) are suitable for map-based visualization of spatially aggregated river behavior, catchment responses, or event-based mapping.
- Ensure consistent temporal alignment when mapping time-series or generating animated/discrete-time maps.
- When integrating with other hydrological or meteorological layers, account for potential data gaps and the conversion from Imperial to metric units.
- The dataset is suitable for GIS products that illustrate discharge magnitude and timing across the Trout Beck reach, with attention to the 1961–1980 temporal window and the 1968 boundary between recording sites.