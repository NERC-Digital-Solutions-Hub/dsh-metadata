# GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- A GPS dataset of 32 European nightjars collected on Thorne and Hatfield Moors, part of Humberhead Peatlands NNR in South Yorkshire.
- Timeframe: June to August, 2015–2018.
- Data: latitude/longitude coordinates (WGS84) from nanoFix mini GPS tags; fixes every 3 minutes (2015–2016) or 5 minutes (2017–2018).
- Purpose: construct foraging tracks, estimate home range sizes, and analyze habitat selection to monitor responses to landscape change.
- Data quality: fixes are regular with occasional spurious or missing points; each tag was briefly calibrated to estimate location error (5–25 m depending on habitat).

## Data collection and methods
- Bird capture: mist nets from 21:00 to 01:00 on Thorne or Hatfield Moors.
- Equipment: nanoFix mini GPS tags (Pathtrack, Otley, UK); preprogrammed 3/5 minute tracking schedule; archival tags (non-transmitting) requiring recapture after 7–10 days.
- Data checks: manually checked for missing points; removed fixes with fewer than 3 satellites (poor fix).
- Data validation: plotted in ArcMap to ensure points fall within plausible foraging range.

## Data structure and columns
- File: CSV with the following columns:
  - ID: unique identifier for each bird
  - Date: date in DD/MM/YYYY
  - Year: factorial covariate used as a fixed effect
  - Time: time of capture point (24-hour clock), between 21:30 and 04:30 to the nearest full minute
  - Lat: latitude (degrees north)
  - Long: longitude (degrees east)
  - Site: two-level factor indicating the part of the nature reserve where data were collected
  - Fix_int: interval between fixes; 3 minutes (2015/16) or 5 minutes (2017/18)
  - Day: day number, used for tracking duration subsets
  - Days: number of days run for collection periods; 21:30–04:30 window
- Notes: Data are used as fixed effects and, in some models, as random slopes.

## Use and applications
- Enables construction of foraging tracks and quantitative analyses of home range size and habitat selection for nightjars.
- Supports analysis of behavioural responses to landscape change over multiple years and sites.
- Data can be re-plotted and re-analyzed in GIS software (e.g., ArcMap) or integrated with other environmental datasets.

## Limitations and caveats
- Some data gaps due to missing fixes or spurious points.
- Patchy data across years with changing fix intervals (3 min vs 5 min) that may affect comparability.
- Location error estimate is variable (5–25 m) depending on habitat, and this uncertainty should be considered in analyses.

## Provenance and references
- Collected by: Lucy Mitchell (PhD student), Paul Shawcroft, Colin Neale, George Day, Tim Jones, Viven Hartwell, Stephen Mosely.
- Associated manuscript: “The trade-off between fix rate and tracking duration on estimates of home range size and habitat selection for small vertebrates” by Mitchell, Lucy J.; White, Piran C.L.; Arnold, Kathryn E.