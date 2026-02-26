# README for dataset: 'GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018'

## Overview
- GPS location data (latitude/longitude in WGS84) for 32 European nightjars.
- Collected at Thorne and Hatfield Moors, Humberhead Peatlands NNR, South Yorkshire.
- Timeframe: June–August, 2015–2018.
- Purpose: construct foraging tracks, estimate home range sizes, and assess habitat selection; evaluate behavioural responses to landscape change.

## Data collection and scope
- Locations: Thorne (53.636, -0.89682) and Hatfield Moors (53.545, -0.93493).
- Tags: nanoFix mini GPS tags (Pathtrack, Otley, UK); archival (not transmitting).
- Tracking schedule: fixes every 3 minutes (2015–2016) or every 5 minutes (2017–2018).
- Capture method: mist nets, 21:00–01:00.
- Tags were preprogrammed; birds were recaptured after 7–10 days for data retrieval.
- Calibration: brief calibration to estimate positional error (about 5–25 metres, depending on habitat).

## Methods and data processing
- Data used to monitor behavioural responses to landscape change via foraging tracks and home-range estimates.
- Data quality checks:
  - Manual verification for missing points.
  - Excluded fixes with fewer than 3 satellites (considered poor quality).
  - Visual checks in ArcMap to ensure points fall within plausible foraging ranges.

## Data content and structure
- Data format: GPS fixes collected as latitude and longitude (WGS84).
- Temporal coverage: June–August each year, 2015–2018.
- Fix interval: 3 minutes (2015–2016) or 5 minutes (2017–2018); some fixes may be spurious or missing.
- Status: fixes are regular with some exceptions; data are tied to individual birds.

## Dataset fields (CSV columns)
- ID: unique identifier for each bird.
- Date: date of fix (DD/MM/YYYY).
- Year: factorial covariate used as a fixed effect.
- Time: time of fix (24-hour clock; 21:30–04:30, to the nearest minute).
- Lat: latitude (degrees north).
- Long: longitude (degrees east).
- Site: two-level factor indicating the part of the nature reserve where data were collected.
- Fix_int: interval between fixes; 3 or 5 minutes; used as a fixed effect in models.
- Day: day number for tracking duration subsets.
- Days: days run for collection periods (21:30–04:30); used as a fixed effect and random slope in models.

## Associated publication and authors
- From submitted manuscript: "THE TRADE-OFF BETWEEN FIX RATE AND TRACKING DURATION ON ESTIMATES OF HOME RANGE SIZE AND HABITAT SELECTION FOR SMALL VERTEBRATES."
- Authors: Mitchell, Lucy J.; White, Piran C.L.; Arnold, Kathryn E. (dataset context referenced).