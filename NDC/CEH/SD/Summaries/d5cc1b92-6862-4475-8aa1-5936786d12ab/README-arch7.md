# Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- Dataset linking nightjar space use with habitat availability to monitor behavioural responses to landscape change.
- Main data: 95% home range sizes (ha), habitat availability within those home ranges (%), and habitat selection ratios (Manly's Selection Ratios) for each individual.
- GPS data accompany the dataset to construct foraging tracks and derive home ranges and habitat selection.

## Datasets included
- Home Range and Habitat Availability CSV
  - Contains per-individual metrics:
    - Individual: unique bird ID
    - Size_HR: 95% home range size (ha)
    - Year: year of tracking
    - Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water: habitat availability within the 95% home range (percent, 1-100)
    - SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site: Manly's Selection Ratios for respective habitat types
- GPS tracking data CSV
  - Contains per-record GPS fixes:
    - ID: bird identifier
    - Date: in DD/MM/YYYY
    - Year: fixed effect covariate
    - Time: HH:MM (24h)
    - Lat, Long: coordinates (WGS84)

## Data fields and interpretations
- Habitat availability fields (Av_...):
  - Percentage of each habitat type within the bird’s 95% home range
- Selection ratios (SR_...):
  - Values >1 indicate selection for a habitat type
  - Values <1 indicate avoidance
  - Includes habitat categories such as water, bare peat, woodland, wetland, cottongrass, bracken, heather, scrub, cleared (1-2 years prior and current year), grass, buildings, and off-site areas
- GPS data fields:
  - ID, Date, Year, Time, Lat, Long
  - Coordinates are latitude/longitude (WGS84), collected June–August 2015–2018

## Methods
- Field collection
  - Nightjars captured by mist nets from 21:00 to 01:00 at Thorne or Hatfield Moors
  - Fitted with nanoFix mini GPS tags (Pathtrack, Otley, UK) programmed for 3-minute (2015/16) or 5-minute (2017/18) intervals
  - Tags archival; birds recaptured after 7–16 days
- Data processing
  - GPS data used to construct foraging tracks and estimate home range sizes and habitat selection
  - Data quality checks:
    - Manually checked for missing points
    - Removed fixes with <3 satellites (poor fix)
    - Plotted in ArcMap to verify points within plausible foraging ranges
  - Habitat availability maps used are independent and aligned with 95% home range outlines
- Data quality and error
  - GPS fix calibration performed; typical location error estimated at 5–25 meters depending on habitat

## Location and scope
- Study area: Humberhead Peatlands NNR, South Yorkshire
- Sampling sites: Thorne (approx. 53.636, -0.89682) and Hatfield Moors (approx. 53.545, -0.93493)
- Timeframe: 2015–2018; 39 individual nightjars studied

## Use and interpretation
- Data supports analysis of functional habitat relationships and inter-individual variability in habitat selection under landscape change
- Useful for GIS-based analyses of space use, habitat availability, and selection across individuals and years
- References the accompanying manuscript: High inter-individual variability in habitat selection and functional habitat relationships in European nightjars over a period of habitat change

## Access and provenance
- Data derived from GPS-tracked nightjars, with habitat maps and 95% home range outlines used to compute availability
- Primary data described in the README accompanying the dataset and associated manuscript