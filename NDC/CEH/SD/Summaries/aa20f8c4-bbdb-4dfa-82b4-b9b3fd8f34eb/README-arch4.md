# README for dataset: 'GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018' Collected by: Lucy Mitchell (PhD student), Paul Shawcroft, Colin Neale, George Day, Tim Jones, Viven Hartwell, Stephen Mosely

## Overview
- Dataset of GPS tracking data for 32 European nightjars.
- Collected at Humberhead Peatlands NNR (Thorne and Hatfield Moors), South Yorkshire.
- Time frame: June–August 2015–2018.
- GPS fixes at 3-minute intervals (2015–2016) or 5-minute intervals (2017–2018); fixes regular with a few spurious or missing points.
- Tags were archival (not transmitting) and required recapture after 7–10 days.
- Tags were briefly calibrated to estimate location error (5–25 metres, depending on habitat).

## Data collection and methods
- Nightjars captured by mist nets between 21:00 and 01:00 at Thorne or Hatfield Moors.
- Each bird equipped with a nanoFix mini GPS tag (Pathtrack, UK) preprogrammed for 3 or 5 minute tracking.
- Data collection relied on recapture (tags did not transmit).

## Data content and structure
- Data format: latitude and longitude (WGS84) coordinates.
- Variables/columns in the CSV:
  - ID: unique identifier for each bird.
  - Date: date in DD/MM/YYYY.
  - Year: factorial covariate used as a fixed effect.
  - Time: time of point (24-hour clock), nearest minute; range 21:30–04:30.
  - Lat: latitude in degrees north.
  - Long: longitude in degrees east.
  - Site: two-level factor indicating part of the nature reserve.
  - Fix_int: interval between fixes (3 or 5 minutes).
  - Day: day number for tracking subsets.
  - Days: duration of tracking periods (21:30–04:30).
- Use in analyses: construct foraging tracks, estimate home range sizes, and habitat selection; monitor behavioural responses to landscape change.

## Data quality and preprocessing
- Data manually checked for missing points.
- Points with fewer than 3 satellites excluded as poor fixes.
- Visual checks performed in ArcMap to ensure points fall within plausible foraging ranges.
- Location error estimated via calibration: 5–25 metres depending on habitat type.

## Use cases and applications
- Supports analyses of home range size and habitat selection for nightjars.
- Useful for understanding behavioural responses to landscape change and for validating movement models.

## Data governance and stewardship considerations (Data Leaders perspective)
- Ensure comprehensive metadata: IDs, dates, times, coordinates, site, fix interval, and tracking window.
- Maintain and communicate data quality criteria (e.g., minimum satellites, post-processing steps).
- Document GPS error estimates and calibration method to inform model uncertainty.
- Preserve dataset structure (CSV with clear column definitions) for discoverability and reuse.
- Consider linking this dataset with broader networks to support cross-site comparisons and collaborative data sharing.