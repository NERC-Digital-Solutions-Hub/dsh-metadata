# Short working title: Avian data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Data Type: Monitoring
- Size: 12.9 KB
- Interpreted by: All authors
- Collection purpose: Assess avian response to wildfire in restored and unrestored sites
- Geographic reference: South Fork McKenzie River, Oregon (lat 44.17, lon -122.30)

## Data Files and Content
- Four separate CSV files:
  - SFMR_PointCoordinates.csv: Point, Restored_Status, Long, Lat
  - SFMR_SpeciesCodes.csv: CODE, Species
  - SFMR_RawPointCounts.csv: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date
  - SFMR_TotalPointCounts.csv: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover
- Dataset structure details:
  - SFMR_PointCoordinates.csv contains: Point, Restored_Status, Long, Lat
  - SFMR_SpeciesCodes.csv contains: CODE, Species
  - SFMR_RawPointCounts.csv contains: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date
  - SFMR_TotalPointCounts.csv contains: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover

## Sampling Methodology
- Method: Point count of bird species
- Observation windows: Initial 3 minutes, then an additional 2 minutes
- Distance bands: Birds recorded as closer than 50m, further than 50m, or flying over
- Replication: Each site intended to be sampled twice; five points (5, 17, 21, 22, 23) could not be revisited due to field conditions
- Protocols referenced: Ralph et al. 1993 Handbook of Field Methods for Monitoring Land Birds; Stephens et al. 2010 Klamath Network Landbird Monitoring Protocol

## Sampling Coverage
- Surveys: 41 five-minute surveys total
  - 20 in restored sites
  - 21 in unrestored sites
- Collection dates:
  - Unrestored reaches: 16 and 23 June 2021
  - Restored reaches: 17 and 24 June 2021

## Quality Control and Metadata
- Procedures: Data collected using standardized methods by trained fieldworkers
- Data handling: Digitized from field survey sheets and double-checked prior to upload
- Metadata support: Includes a species codes dictionary to map codes to species names

## Notes and Considerations for Monitoring Use
- Field limitations: Some sites could not be sampled twice, potentially affecting temporal replication analyses
- Data richness: Combines per-site coordinates, species-level counts, and time-banded totals to enable comparative analyses between restored and unrestored sites
- Governance-friendly structure: Clearly labeled datasets and columns facilitate data validation, re-use, and integration into monitoring frameworks for policy evaluation and decision support