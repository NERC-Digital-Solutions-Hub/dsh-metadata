# Avian data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Data type: Monitoring; size 12.9 KB; interpreted by all authors.
- Collection purpose: To assess avian response to wildfire in restored and unrestored sites.
- Geography: Latitude 44.17, Longitude -122.30.
- Sampling design: 41 five-minute surveys (20 restored, 21 unrestored) conducted in June 2021.
- Collection dates: Unrestored reaches on 16 and 23 June 2021; restored reaches on 17 and 24 June 2021.
- Data products: Four CSV files providing coordinates, species codes, raw counts, and total counts.

## Datasets and structure
- SFMR_PointCoordinates.csv
  - Columns: Point, Restored_Status, Long, Lat
  - Purpose: Geographic location and restoration status of each sampling point.
- SFMR_SpeciesCodes.csv
  - Columns: CODE, Species
  - Purpose: Mapping of species codes to full species names.
- SFMR_RawPointCounts.csv
  - Columns: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date
  - Purpose: Observations by species at each point by distance band and time window (3 or 5 minutes).
  - Notes: Values are counts of observations within each category for the specified date.
- SFMR_TotalPointCounts.csv
  - Columns: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover
  - Purpose: Aggregated counts of all birds across all species by point, restoration status, and survey occasion (First and Second) within 3- and 5-minute windows.

## Sampling methods and protocols
- Method: Point count surveys of birds.
- Observation windows: Initial 3 minutes, followed by an additional 2 minutes (total 5 minutes).
- Distance bands: Birds recorded as closer than 50 m, further than 50 m, or flying over.
- Sites and effort: 41 five-minute surveys (20 restored, 21 unrestored).
- Protocol references: Based on Ralph et al. 1993 and Stephens et al. 2010 field methods for landbird monitoring.
- Dates and conditions: Some points could not be sampled twice due to field conditions (Points 5, 17, 21, 22, 23).

## Data quality, provenance, and usability
- Quality control: Data collected following standardized procedures by trained fieldworkers; field survey sheets were digitised and double-checked prior to upload.
- Metadata support: Includes a species code dictionary and explicit restoration status to enable comparisons between restored and unrestored sites.
- Self-serve readiness: Provides raw counts by species and consolidated totals by survey occasion, facilitating flexible analysis and visualization.

## Usage considerations and caveats
- Restoration comparison: Designed to assess avian response to wildfire by contrasting restored versus unrestored reaches.
- Incomplete duplication: Five points could not be re-sampled twice due to field conditions; account for potential sampling gaps in analyses.
- Timeframe: Data reflect two sets of surveys within a short window in June 2021; temporal scope is limited to these dates.