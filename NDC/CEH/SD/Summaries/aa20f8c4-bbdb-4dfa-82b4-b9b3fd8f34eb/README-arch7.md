# GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- GPS fixes (latitude/longitude, WGS84) for 32 individual European nightjars.
- Collected at Thorne and Hatfield Moors, Humberhead Peatlands NNR, South Yorkshire.
- Timeframe: June–August, 2015–2018.
- Purpose: construct foraging tracks, estimate home range sizes, and assess habitat selection; monitor responses to landscape change.
- Data collected with nanoFix mini GPS tags; archival (not transmitting) and recaptured after 7–10 days.

## Data details
- Fix intervals: 3 minutes (2015–2016) and 5 minutes (2017–2018).
- Calibration: brief calibration to estimate location error (5–25 metres, depending on habitat).
- Quality controls: fixes with fewer than 3 satellites removed; manual checks for missing points; ArcMap used to verify points within plausible foraging ranges.

## Data structure (CSV columns)
- ID: unique bird identifier
- Date: DD/MM/YYYY
- Year: factorial covariate used as fixed effect
- Time: 24-hour time for each fix (between 21:30 and 04:30, to nearest full minute)
- Lat: latitude (degrees)
- Long: longitude (degrees)
- Site: two-level factor indicating part of the nature reserve
- Fix_int: interval between fixes (3 or 5)
- Day: day number for tracking duration subsets
- Days: tracking period windows (21:30–04:30)

## Data processing and quality control
- Data manually checked for missing points.
- Poor fixes removed if satellite count < 3.
- Visual validation in ArcMap to ensure spatial plausibility.
- Spurious or missing fixes addressed through standard cleaning steps.

## GIS applications and use cases
- Visualize and analyze foraging tracks and movement patterns.
- Estimate and compare home range sizes across individuals and time periods.
- Assess habitat selection by overlaying tracks with land cover and landscape change layers.
- Integrate with other GIS datasets to explore spatiotemporal responses of nightjars to environmental changes.

## Provenance and related literature
- Collected by researchers including Lucy Mitchell, Paul Shawcroft, Colin Neale, George Day, Tim Jones, Viven Hartwell, Stephen Mosely.
- Related manuscript: The Trade-Off Between Fix Rate and Tracking Duration on Estimates of Home Range Size and Habitat Selection for Small Vertebrates (Mitchell et al.).