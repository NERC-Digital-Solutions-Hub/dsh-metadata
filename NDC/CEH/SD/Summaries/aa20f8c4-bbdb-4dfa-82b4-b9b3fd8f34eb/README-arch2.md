# GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- Dataset of latitude/longitude (WGS84) GPS fixes for 32 European nightjars.
- Collected to construct foraging tracks, estimate home range sizes, and assess habitat selection to monitor behavioural responses to landscape change.
- Data curated to support environmental monitoring and policy-relevant analyses.

## Data Collected
- Location: Humberhead Peatlands NNR, South Yorkshire (Thorne: 53.636, -0.89682; Hatfield Moors: 53.545, -0.93493).
- Timeframe: June–August, 2015–2018.
- Sampling: GPS fixes every 3 minutes (2015–2016) or 5 minutes (2017–2018).
- Tagging: NanoFix mini GPS tags (archival, preprogrammed; not transmitting) attached to birds and recaptured after 7–10 days.
- Calibration: Brief calibration to estimate location error (5–25 m depending on habitat).

## Methods and Calibration
- Capture: Nightjars trapped with mist nets between 21:00–01:00 at Thorne or Hatfield Moors.
- Data quality: Manual checks for missing points; removal of fixes with fewer than 3 satellites.
- Validation: Visual inspection in ArcMap to ensure points fall within plausible foraging ranges.

## Data Quality Assurance
- Fixes screened for reliability (sufficient satellites; plausible spatial extent).
- Spurious fixes and missing data noted and excluded from analyses.
- Regular QA steps aligned with standardised environmental monitoring practices.

## Dataset Structure (CSV Columns)
- ID: unique identifier for each bird.
- Date: DD/MM/YYYY.
- Year: factorial covariate (as fixed effect in models).
- Time: 24-hour clock to the nearest full minute (21:30–04:30 range).
- Lat: latitude (degrees north).
- Long: longitude (degrees east).
- Site: two-level factor indicating part of the nature reserve.
- Fix_int: interval between fixes (3 or 5 minutes) used as fixed effect.
- Day: tracking day number; used for duration subsets and as fixed effect/random slope in models.

## Uses and Analysis
- Produces foraging tracks, estimates of home range, and habitat selection.
- Data intended to support analyses of behavioural responses to landscape change.
- Data quality checks inform model inputs and interpretation.

## Geographic and Temporal Coverage
- Location: Humberhead Peatlands NNR, Thorne and Hatfield Moors, South Yorkshire, UK.
- Periods: 2015–2018 (summer months within each year).

## Related Publication and Collectors
- Related manuscript: The Trade-Off Between Fix Rate and Tracking Duration on Estimates of Home Range Size and Habitat Selection for Small Vertebrates.
- Authors: Mitchell, Lucy J.; White, Piran C.L.; Arnold, Kathryn E.
- Collected by: Lucy Mitchell (PhD student) and colleagues (Paul Shawcroft, Colin Neale, George Day, Tim Jones, Vivien Hartwell, Stephen Mosely).