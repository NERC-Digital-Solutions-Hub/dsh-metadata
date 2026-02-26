# README for dataset: 'Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018' From submitted manuscript: 'High inter-individual variability in habitat selection and functional habitat relationships in European nightjars over a period of habitat change' Authors: Mitchell, Lucy J.; Kohler, Tim; White, Piran C .L.; Arnold, Kathryn E.

## Overview
- Dataset contains 39 European nightjars tracked at Humberhead Peatlands NNR (South Yorkshire) from 2015–2018.
- Main data include 95% home range sizes (hectares), habitat availability within those home ranges, and habitat selection ratios (Manly's Selection Ratios) per individual.
- GPS tracking data accompany the habitat data, enabling construction of foraging tracks and assessment of habitat use relative to availability.

## Data Files and Structure
- Two primary CSV files:
  - Home Range and Habitat Availability: for each individual bird, includes home range size and habitat availability within the 95% home range, plus selection ratios for various habitat types.
  - GPS Tracking Data: latitude/longitude points with date/time for each bird, used to map foraging tracks and link locations to habitat types.
- Columns in Home Range and Habitat Availability CSV:
  - Individual: unique bird identifier
  - Size_HR: home range size (ha) at the 95% utilization level
  - Year: fixed-effect covariate
  - Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water: percentage availability (1–100) of each habitat within the 95% home range
  - SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site: Manly's Selection Ratios for each habitat type
- Columns in GPS Tracking Data CSV:
  - ID: bird identifier (matching Individual)
  - Date: date (DD/MM/YYYY)
  - Year: fixed-effect covariate
  - Time: time (24-hour clock; 21:30–04:30 range)
  - Lat, Long: latitude/longitude (WGS84)
- Data are provided for two sites: Thorne and Hatfield Moors (Humberhead Peatlands NNR)

## Data Collection and Tracking Methods
- Nightjars captured by mist nets between 21:00–01:00 at Thorne or Hatfield Moors.
- Tagged with nanoFix mini GPS tags (Pathtrack, Otley, UK) preprogrammed for 3/5 minute sampling schedules.
- Tags archival (not transmitting); birds recaptured after 7–16 days.
- GPS data used to construct foraging tracks, estimate home range sizes, and assess habitat selection and responses to landscape change.

## Data Processing and Quality Assurance
- GPS data manually checked for missing points; points with fewer than 3 satellites removed (poor fix).
- Data plotted in ArcMap to verify points within plausible foraging ranges and to identify outliers.
- 95% home range sizes derived from GPS metadata; habitat availability derived from an independent habitat map overlaid on 95% home range outlines.
- Habitat selection ratios calculated using Manly’s equation, integrating availability values with GPS point locations.

## Habitat and Selection Details
- Habitat types covered in selection analyses include:
  - Water, Bare peat, Woodland, Wetland, Cottongrass, Bracken, Heather, Scrub, Cleared (and Cleared+1, Cleared+2 to reflect different clearing years), Grass, Building, Off_Site.
- Availability values reflect the proportion of each habitat type within the bird’s 95% home range.
- Selection ratios indicate relative use vs. availability:
  - Values >1 indicate positive selection for a habitat type.
  - Values <1 indicate avoidance of a habitat type.

## Temporal and Spatial Context
- Data collected June–August, across 2015–2018.
- GPS fixes at 3-minute intervals in 2015–2016 and 5-minute intervals in 2017–2018.
- Calibration of tags suggested location error between ~5–25 meters, depending on habitat type.

## Purpose and Use
- Data intended to monitor behavioral responses of nightjars to landscape change by linking foraging behavior and habitat use to habitat availability.
- Enables analyses of inter-individual variability in habitat selection and the functional relationships between habitat change and nightjar behavior.

## Collection Site Details
- Humberhead Peatlands National Nature Reserve (Thorne and Hatfield Moors), coordinates ~53.6°N, -0.9°E.
- Study focused on the foraging range and habitat selection of 39 individuals within this landscape.