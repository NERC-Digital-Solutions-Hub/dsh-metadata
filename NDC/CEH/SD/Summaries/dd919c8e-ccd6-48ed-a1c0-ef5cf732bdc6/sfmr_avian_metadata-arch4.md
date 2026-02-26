# Avian data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Data type: Monitoring.
- Size: 12.9 KB.
- Interpreted by: All authors.
- Collection purpose: Assess avian response to wildfire in restored and unrestored sites.

## Data collection and design
- Study design: Point count surveys of birds.
- Survey duration: 3 minutes initially, then an additional 2 minutes (total 5 minutes per survey).
- Distance bands: Observations categorized as closer than 50 m, farther than 50 m, or flying over.
- Sites and replication: 41 five-minute surveys total; 20 in restored sites, 21 in unrestored sites. Five points (5, 17, 21, 22, 23) were not sampled twice due to field conditions.
- Sampling dates: Unrestored reaches on 16 and 23 June 2021; restored reaches on 17 and 24 June 2021.
- Methodology basis: Ralph et al. (1993) Handbook of Field Methods for Monitoring Landbirds; Klamath Network Landbird Monitoring Protocol (Stephens et al., 2010).
- Data collection approach: Standardized field procedures with trained fieldworkers; data digitised from field sheets and double-checked before upload.

## Data files and structure
- Four CSV files:
  - SFMR_PointCoordinates.csv: Point, Restored_Status, Long, Lat.
  - SFMR_SpeciesCodes.csv: CODE, Species.
  - SFMR_RawPointCounts.csv: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date.
  - SFMR_TotalPointCounts.csv: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover.
- Content mapping: SFMR_SpeciesCodes.csv provides CODE-to-Species mapping; RawPointCounts.csv contains per-point, per-species, per-time-window, per-distance-band counts; TotalPointCounts.csv aggregates counts by survey and time window.

## Data quality and provenance
- Adheres to standardised field protocols and training.
- Data are digitised from survey sheets and subjected to double-check validation prior to upload.

## Uses, value, and implications for data strategy
- Enables comparison of avian abundance/occurrence between restored and unrestored sites to evaluate wildfire impact and restoration effectiveness.
- Provides spatially explicit data (Point coordinates) and a detailed species coding dictionary to support reproducibility and cross-study integration.
- Supports time-window and distance-band analyses, aiding nuanced assessment of detection versus abundance across conditions.

## Limitations and considerations for data managers
- Partial replication at some points (not all points sampled twice) due to field conditions.
- Data cover specific dates in June 2021; temporal scope is limited to the recorded surveys.