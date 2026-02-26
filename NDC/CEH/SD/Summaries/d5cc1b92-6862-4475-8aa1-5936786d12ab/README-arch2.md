# Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Aim and use
- Provide standardized data to monitor how European nightjars respond to landscape change in the Humberhead Peatlands NNR.
- Support analysis of home range size, habitat availability within home ranges, and habitat selection by individuals using GPS data.
- Enable comparison over time and integration with other environmental datasets to assess environmental health and policy-relevant habitat use.

## Data content

- Main data file
  - Home range sizes (95% use level, in hectares)
  - Habitat availability within the 95% home range (percentage availability per habitat category)
  - Habitat selection ratios (Manly's Selection Ratios; values >1 indicate selection, <1 indicate avoidance)
  - 95% home range outlines used to derive habitat availability
- Habitat selection calculations
  - Based on Manly's equation using habitat availability values and GPS points
- GPS tracking data file
  - Latitude/longitude (WGS84) from GPS tags for 39 individuals
  - ID, Date, Year, Time, Lat, Long
- Habitat categories included in availability and selection
  - Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water
  - Selection ratios: SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site

## Methods

- Field collection
  - Nightjars captured by mist net between 21:00 and 01:00 at Thorne or Hatfield Moors
  - Tagged with a nanoFix mini GPS tag (Pathtrack, UK) preprogrammed for 3- or 5-minute tracking
  - Tags archival (no real-time transmission); recaptured after 7–16 days
- GPS data processing
  - GPS fixes used to construct foraging tracks and estimate home range and habitat selection
  - Manual data checks for missing points; exclude fixes with fewer than 3 satellites (poor fix)
  - Points plotted in ArcMap to verify they fall within plausible foraging ranges
- Habitat and range calculations
  - 95% home ranges derived from GPS data
  - Habitat availability calculated using an independent habitat map and the 95% home range outlines
  - Habitat selection ratios calculated using Manly’s equation with availability and GPS points
- Data quality considerations
  - GPS error calibrated per habitat type (estimated 5–25 m)

## Data structure and definitions

- Home Range and Habitat Availability CSV
  - Individual: unique identifier for each bird
  - Size_HR: home range area (ha)
  - Year: fixed effect in analyses
- Habitat availability variables (Av_*)
  - Percent availability of each habitat category within the 95% home range
- Habitat selection variables (SR_*)
  - Selection ratio values for each habitat type per individual
  - Interpretation: SR > 1 indicates selection; SR < 1 indicates avoidance
- GPS data CSV
  - ID: unique bird identifier
  - Date, Time: date and time of GPS fix
  - Year: fixed effect in analyses
  - Lat, Long: latitude and longitude (WGS84)

## Location and timeframe

- Study site: Humberhead Peatlands NNR, South Yorkshire, UK (Thorne and Hatfield Moors)
- Sampling period: June–August, 2015–2018
- Sample size: 39 European nightjars

## Use cases and purpose

- Supports monitoring of behavioural responses to landscape change through quantitative measures of home range, habitat availability, and habitat selection
- Provides standardized outputs that can be used for trend analysis, policy assessment, and integration with other environmental datasets
- Data quality-conscious preprocessing and explicit metadata facilitate reuse in comparative analyses

## Notes on data provenance

- Derived from a submitted manuscript: High inter-individual variability in habitat selection and functional habitat relationships in European nightjars over a period of habitat change
- Authors: Mitchell, Lucy J.; Kohler, Tim; White, Piran C. L.; Arnold, Kathryn E.