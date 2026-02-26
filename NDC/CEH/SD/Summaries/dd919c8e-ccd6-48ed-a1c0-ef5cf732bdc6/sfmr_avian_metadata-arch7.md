# Avian data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: monitor avian response to wildfire in restored and unrestored sites.
- Data type: monitoring; four CSV files containing sampling coordinates, species codes, raw point counts, and total point counts.
- Geography: sampling points with longitude and latitude; restoration status at each point.
- Temporal scope: surveys conducted in June 2021 (two dates for unrestored reaches and two dates for restored reaches).
- Survey effort: 41 five-minute surveys (20 in restored sites, 21 in unrestored sites).

## Data Structure and Content
- SFMR_PointCoordinates.csv
  - Columns: Point, Restored_Status, Long, Lat.
- SFMR_SpeciesCodes.csv
  - Columns: CODE, Species.
- SFMR_RawPointCounts.csv
  - Columns: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date.
  - Values are counts of observed birds by species, distance band, and time window.
- SFMR_TotalPointCounts.csv
  - Columns: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover.
  - Values are counts of all birds (across species) by distance band and time window.
- Sampling detail: 41 surveys total (3-minute counts and 5-minute counts), with 2 surveys at most points; five points (5, 17, 21, 22, 23) could not be sampled twice due to field conditions.
- Data collection cadence: two survey dates per site, aligned with restored vs unrestored status.

## Collection Methodology
- Method: point counts of bird species.
- Observation windows: 3-minute and 5-minute periods.
- Distance categorization: birds recorded as closer than 50 m, further than 50 m, or flying over.
- Protocol basis: Ralph et al. 1993 and Klamath Network Landbird Monitoring Protocol; field methods standardized and documented.
- Personnel: collected by trained fieldworkers; data digitized from survey sheets and double-checked prior to upload.

## Data Quality and Provenance
- Standardized procedures followed for data collection.
- Data digitized from field sheets and subjected to double-checks before upload.
- Metadata includes sampling dates, site restoration status, and coordinate accuracy to enable GIS joining.

## GIS Applications and How to Use
- Map-based analyses: join SFMR_PointCoordinates with count data to visualize spatial patterns of avian abundance.
- Compare restored vs unrestored sites: assess differences in species counts and overall abundance across time windows.
- Temporal analysis: evaluate changes between FirstSurvey and SecondSurvey within each site.
- Data integration: combine with the species codes to convert codes to species names for readable maps; transform raw counts to per-point summaries or densities as needed.
- Potential data prep: convert to long format for GIS software; ensure alignment of point identifiers across all four CSVs.

## Additional Notes
- Data size is modest (approximately 12.9 KB) but structured for GIS-friendly integration.
- The dataset provides explicit coordinates, restoration status, and detailed count breakdowns by species, distance band, and observation window, enabling detailed spatial and temporal analyses of avian response to wildfire in the study area.