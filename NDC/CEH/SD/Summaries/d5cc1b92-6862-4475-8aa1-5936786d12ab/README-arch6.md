# Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- Dataset of home range sizes (95% use level, hectares), habitat availability within those ranges, and habitat selection ratios (Manly’s Selection Ratios) for 39 European nightjars.
- 95% home ranges derived from GPS data; habitat availability estimated from an independent habitat map aligned with the 95% home range outlines.
- Habitat selection ratios indicate avoidance (<1) or selection (>1) of habitat types by each individual.

## Data contents
- Main data file includes:
  - Home range size (Size_HR) in hectares.
  - Habitat availability within the 95% home range for habitat categories (Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water) as percentages (1–100).
  - Habitat selection ratios for each habitat type (e.g., SR_Water, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site).
- Separate field list:
  - Individual: unique bird identifier.
  - Other habitat-specific SR fields: SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared variants, SR_Grass, SR_Building, SR_Off_Site.
- Associated GPS tracking data file:
  - ID, Date, Year, Time, Lat, Long (WGS84).

## Methods
- Nightjars captured by mist net between 21:00–01:00 at Thorne or Hatfield Moors.
- Tagged with nanoFix mini GPS tags (Pathtrack, Otley, UK) preprogrammed for 3/5 minute tracking.
- Tags archival (non-transmitting); birds recaptured after 7–16 days.

## Data collection and processing
- GPS data used to construct foraging tracks, estimate home ranges, and assess habitat selection to monitor responses to landscape change.
- Data quality steps:
  - Manual checks for missing points.
  - Excluded points with poor GPS fixes (less than 3 satellites).
  - Potential spurious fixes identified and removed; data visualized in ArcMap to confirm points within plausible foraging range.

## Data formats and key fields
- Home Range and Habitat Availability CSV:
  - Individual
  - Size_HR (ha)
  - Year
  - Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water (habitat availability percentages)
  - SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub
  - SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site
- GPS Tracking Data CSV:
  - ID
  - Date (DD/MM/YYYY)
  - Year
  - Time (HH:MM, 24-hour)
  - Lat, Long (WGS84)

## Study scope and timing
- Location: Humberhead Peatlands NNR, South Yorkshire (Thorne: 53.636, -0.89682; Hatfield Moors: 53.545, -0.93493).
- Data collection period: June–August, 2015–2018.
- GPS fix interval: 3 minutes (2015–2016) or 5 minutes (2017–2018).
- GPS fixes generally regular with some exceptions (spurious or missing fixes); calibration-indicated error estimated at 5–25 metres depending on habitat type.

## Use of the dataset
- Supports analyses of foraging behavior, habitat selection, and responses of nightjars to landscape changes through 2015–2018.
- Enables comparison of inter-individual habitat use and selection across a changing habitat mosaic.