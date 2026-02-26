# Bore Hole monitoring

## Overview
- Field study at Tyn y Bryn farm documenting groundwater via five boreholes from 03/08/2005 to 03/03/2008.
- Instruments used: barodiver and divers to measure water levels; data include time-stamped readings, diver status, and measurement corrections.
- Purpose for GIS use: produce time-series, map-based visualization of groundwater fluctuations across multiple boreholes, with attention to data quality and measurement protocols.

## Borehole details (summary)
- Borehole 1 (total depth 11.6 m)
  - Water levels recorded throughout 2005–2007, with readings adjusted for measurement point offset and diver presence.
- Borehole 2 (total depth 5.5 m)
  - Regular water level measurements; similar corrections for measuring point above ground and diver status; periodic notes on diver condition.
- Borehole 3 (Bowl, total depth 5.89 m)
  - Extensive time-series data; barodiver installed 03/03/08; multiple diver placements and readings (in/out) with corresponding adjustments.
- Borehole 4 (Above shelterbelt, total depth 1208.5 cm)
  - Readings often not possible when diver in hole; frequent diver deployments/removals; barodiver activity documented with later installation (periodic logging and adjustments).
- Borehole 5 (Below shelterbelt, depth ~775 cm)
  - Long-running as-reading series; diver reliability issues noted (07–08/2007), diver moved to Bowl borehole; multiple data corrections for measuring point offset and diver status.

## Instrumentation and measurement methods
- Barodiver and divers used to obtain water-level readings.
- Measuring point offsets applied to derive actual water levels (e.g., 15 cm or 30–31 cm above ground depending on borehole).
- Readings include timestamp, water depth, and notes on diver in/out, diver condition, and manual readings.
- Some measurements include sampling frequency (e.g., every 30 minutes) and occasional manual dips.

## Data quality and challenges
- Readings sometimes unavailable or unreliable when divers were in the borehole.
- Occasional jumps or anomalies between downloads (e.g., ~10 cm differences).
- Diver-related issues: dirtiness, reliability concerns, and hardware changes (replacements, reinstallation, wire handling).
- Data management notes: occasional “diver downloaded and removed,” “wire left in hole,” and reconfiguration of diverts/divers.
- Files reference multiple corrections to readings to account for measurement point offsets and the diver’s presence.

## Notable events and timeline highlights
- 03/08/2005: Divers installed in boreholes; initial data collection begins.
- 09/08/2005: Barodiver moved from Bowl borehole to borehole above shelterbelt to improve measurement stability.
- 03/03/2008: Baro diver installed in Bowl borehole (Borehole 3); ongoing data integrity checks and reconfigurations across boreholes.
- 2006–2007: Repeated adjustments of divers, readings, and data corrections; several notes on reading reliability and equipment changes.
- 2007–2008: Diver reliability concerns lead to reassignments and eventual removal/reinstallation activities.

## GIS-related considerations for data products
- Time-series construction: store per-borehole readings with accurate timestamps, including diver status and measurement corrections.
- Data harmonization: apply standardized corrections to convert raw readings into actual water levels (accounting for measuring-point offset and diver in/out).
- Quality flags: annotate records with data quality indicators (e.g., diver in, reading not possible, dirty diver, jump between downloads).
- Spatial layer design: create separate layers for each borehole (with precise coordinates) and a temporal layer or animation for time-based visualization.
- Uncertainty handling: flag readings with known reliability issues and consider incorporating measurement uncertainty related to diver positions.
- Data gaps: document and visualize periods with no data due to reading infeasibility or equipment issues.
- Metadata needs: preserve instrument type, installation/removal dates, and notes on divergences (e.g., barodiver moved, diver relocated) to aid interpretation.