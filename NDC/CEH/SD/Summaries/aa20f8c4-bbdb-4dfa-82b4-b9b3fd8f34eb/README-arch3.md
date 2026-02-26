# GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- GPS location data (latitude/longitude in WGS84) for 32 European nightjars.
- Collected at Thorne and Hatfield Moors, Humberhead Peatlands NNR, South Yorkshire.
- Timeframe: June–August, 2015–2018.
- Fix intervals: every 3 minutes (2015–2016) or 5 minutes (2017–2018).
- Tags calibrated to estimate location error (approximately 5–25 metres, depending on habitat).
- Tags were archival (not transmitting) and birds were recaptured after 7–10 days.

## Data collection and tagging methods
- Nightjars captured by mist nets between 21:00 and 01:00 on Thorne or Hatfield Moors.
- Tags: nanoFix mini GPS tags (Pathtrack, UK) preprogrammed with 3/5 minute schedules.
- Data collection ended when birds were recaptured after a short tagging period.

## Data content and quality
- Used to construct foraging tracks, estimate home range sizes, and assess habitat selection.
- Data checked for quality: points with fewer than 3 satellites excluded; problematic fixes identified and removed.
- Visual plausibility checks performed in ArcMap to ensure points were within plausible foraging ranges.
- Calibration information: fixed error estimates (5–25 m) noted, varying by habitat.

## Data structure (CSV columns)
- ID: unique bird identifier.
- Date: date of fix (DD/MM/YYYY).
- Year: factor used as a fixed effect in models.
- Time: fix timestamp (HH:MM in 24-hour format).
- Lat: latitude (degrees North).
- Long: longitude (degrees East).
- Site: two-level factor indicating which part of the nature reserve data were collected.
- Fix_int: interval between fixes (3 or 5 minutes).
- Day: tracking day number for the period.
- Days: total days of collection within the subset.

## Use of the data
- To analyze foraging paths, home range size, and habitat selection of nightjars.
- To monitor behavioural responses to landscape changes within the Humberhead Peatlands.

## Processing and governance considerations
- Data are manually cleaned and filtered for quality prior to analysis.
- Output relies on a CSV format with clearly defined fields for traceability.
- Metadata present includes capture methods, tagging schedule, and calibration notes; broader data governance and sharing considerations (e.g., openness of underlying datasets) are not explicit in the document.