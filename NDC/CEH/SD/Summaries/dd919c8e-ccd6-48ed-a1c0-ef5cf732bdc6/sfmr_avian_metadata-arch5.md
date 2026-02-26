# Avian data from the South Fork McKenzie River in Oregon, USA

## Overview
- Data type: Monitoring
- Size: 12.9 KB
- Collection purpose: Assess avian response to wildfire in restored and unrestored sites
- Interpreted by: All authors

## Data Content and Structure
- Four CSV files:
  - SFMR_PointCoordinates.csv: Point, Restored_Status, Long, Lat
  - SFMR_SpeciesCodes.csv: CODE, Species
  - SFMR_RawPointCounts.csv: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date
  - SFMR_TotalPointCounts.csv: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover
- Content focus:
  - Counts of avian observations by site, species, distance band (<50m, >50m, flying) and time window (3 or 5 minutes)
  - Metadata linking points to coordinates and restoration status
  - Species codes mapping to species names
- Note: Values reflect observations of birds within each category; some sites may have limited sampling data due to field conditions.

## Collection Methodology
- Method: Point counts of bird species
- Observation windows: 3 minutes initially, followed by an additional 2 minutes (total 5 minutes)
- Distance categories: closer than 50m, further than 50m, or flying over
- Site repeats: Each site intended to be sampled twice; exceptions at points 5, 17, 21, 22, and 23 due to field conditions
- Protocols referenced:
  - Ralph et al. 1993 Handbook of field methods for monitoring landbirds
  - Klamath Network Landbird Monitoring Protocol (2010)
- Sampling scope: 41 five-minute surveys total
  - 20 restored sites, 21 unrestored sites
- Collection dates:
  - Unrestored reaches: June 16 and June 23, 2021
  - Restored reaches: June 17 and June 24, 2021

## Quality Control and Provenance
- Procedures: Data collected following standardised field protocols by trained fieldworkers
- Digitization: Field survey sheets digitised and double-checked prior to upload

## Governance and Stewardship Considerations
- Data provenance: Clear linkage between coordinates, restoration status, surveys, and species counts
- Metadata implications:
  - Coordinate system and units implied by Long/Lat fields; ensure explicit CRS in metadata
  - Inconsistent naming across files (Restored_Status vs Restoration_status) may affect data integration and requires harmonization for governance and reuse
- Data completeness:
  - Some points were not sampled twice due to field conditions, affecting comparability across sites
- Usage guidance for data stewards:
  - Maintain clear documentation of sampling effort, site statuses, and any deviations from the protocol
  - Preserve the linkage between SFMR_PointCoordinates, SFMR_SpeciesCodes, SFMR_RawPointCounts, and SFMR_TotalPointCounts to support traceability and reproducibility