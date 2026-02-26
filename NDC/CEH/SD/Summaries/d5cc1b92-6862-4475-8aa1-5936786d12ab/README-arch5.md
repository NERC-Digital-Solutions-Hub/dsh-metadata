# README for dataset: 'Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018'

## Overview
- Dataset comprises home range sizes (95% use level, in hectares), habitat availability within each 95% home range (percent of each habitat category), and habitat selection ratios (Manly's Selection Ratios) for 39 individual European nightjars.
- 95% home ranges are derived from GPS data; habitat availability is based on an independent habitat map overlaid with the 95% home range outlines.
- Habitat selection ratios are calculated with Manly's equation using availability values and GPS points.
- Data are connected to a study on inter-individual variability in habitat selection during habitat change.

## Data contents
- Main data file includes:
  - Size_HR: home range size (ha)
  - Year: fixed-effect covariate
  - Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water: habitat availability within the 95% home range (percent, 1–100)
  - SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site: selection ratios for each habitat type
- Associated CSV file contains GPS tracking data with columns:
  - ID, Date, Year, Time, Lat, Long (WGS84)
- Geographic scope: Humberhead Peatlands NNR, Thorne and Hatfield Moors (South Yorkshire, UK)

## Data collection and methods
- Subjects: 39 European nightjars captured by mist nets from 21:00 to 01:00 at Thorne or Hatfield Moors.
- Tracking devices: nanoFix mini GPS tags (Pathtrack, Otley, UK) preprogrammed for 3- or 5-minute intervals.
- Data collection window: June–August, 2015–2018.
- Tag characteristics: archival tags (not transmitting); birds recaptured after 7–16 days.
- Purpose: construct foraging tracks, estimate home ranges, and assess habitat selection in response to landscape change.

## Data processing and quality assurance
- Data cleaning:
  - Manual checks for missing points.
  - Exclusion of fixes with fewer than 3 satellites (considered poor fixes).
  - Visual screening in ArcMap to confirm points within plausible foraging ranges.
- GPS accuracy:
  - Tags calibrated to estimate error typically between 5–25 meters depending on habitat type.
- Data structure notes:
  - GPS fixes provided as latitude/longitude (WGS84) with time stamps in local format (21:30–04:30).
  - 95% home ranges calculated using the accompanying GPS metadata file.

## Data structure and column details (summary)
- Home Range and Habitat Availability CSV:
  - Individual: unique bird identifier
  - Size_HR: home range size (ha)
  - Year: fixed effect
  - Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water: habitat availability percentages
  - SR_* fields: multiple habitat-specific selection ratios (e.g., SR_Water, SR_Woodland, SR_Bare_peat, SR_Grass, SR_Building, SR_Off_Site, and several Cleared-related categories)
- GPS tracking CSV:
  - ID: bird identifier
  - Date, Year, Time, Lat, Long: timestamped location data (lat/long, WGS84)

## Temporal and geographic scope
- Temporal: data collected during June–August across 2015–2018.
- Spatial: Thorne and Hatfield Moors within the Humberhead Peatlands NNR, South Yorkshire, UK.

## Use and context
- GPS data used to map foraging paths, quantify home range sizes, and evaluate habitat selection to understand behavioural responses to landscape change.
- Metadata and quality checks enable reproducible analyses and consistent interpretation of habitat use patterns across individuals and years.

## Limitations and caveats
- archiving GPS tags do not transmit; records rely on recapture timing (7–16 days), which may constrain longitudinal comparisons per individual.
- Occasional data gaps due to missing fixes or calibration errors; 3–5 minute fix intervals may affect fine-scale movement interpretation.
- Habitat availability relies on an independent habitat map; any updates to habitat classifications could influence availability and selection interpretations.