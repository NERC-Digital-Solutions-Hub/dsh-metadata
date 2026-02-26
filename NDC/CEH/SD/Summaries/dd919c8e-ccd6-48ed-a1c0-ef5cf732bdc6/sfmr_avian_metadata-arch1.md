# Avian data from the South Fork McKenzie River in Oregon, USA.

- Purpose: Monitoring avian response to wildfire in restored and unrestored sites; data collected to assess how bird communities vary with restoration status after wildfire.
- Size and scope: 12.9 KB dataset comprising four separate CSV files; 41 five-minute surveys across 20 restored and 21 unrestored sites.
- Interpreted by: All authors.

## Datasets included

- SFMR_PointCoordinates.csv
  - Columns: Point, Restored_Status, Long, Lat
- SFMR_SpeciesCodes.csv
  - Columns: CODE, Species
- SFMR_RawPointCounts.csv
  - Columns: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date
  - Values: number of observations per species per distance band and time window
- SFMR_TotalPointCounts.csv
  - Columns: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover
  - Values: number of observations for all birds across all species by distance band and time window, per survey

## Sampling design and collection protocol

- Methodology: Point counts of bird species
  - Initial observation period: 3 minutes, followed by an additional 2 minutes (total 5 minutes)
  - Distance categories: closer than 50 m, further than 50 m, and flying over
- Sampling intensity: 41 five-minute surveys total
  - Restored sites: 20 surveys
  - Unrestored sites: 21 surveys
- Field conditions: Each site intended to be sampled twice; five points could not be sampled twice due to field conditions (Points 5, 17, 21, 22, 23)

## Collection dates and site details

- Unrestored reaches: June 16, 2021 and June 23, 2021
- Restored reaches: June 17, 2021 and June 24, 2021
- Location context: Avian monitoring in the South Fork McKenzie River area, Oregon (wildfire context)

## Data structure and codes

- Point-level coordinates: SFMR_PointCoordinates.csv (Point, Restored_Status, Long, Lat)
- Species identifiers: SFMR_SpeciesCodes.csv (CODE, Species)
- Per-point, per-species counts: SFMR_RawPointCounts.csv (Point, Species, counts by time window and distance)
- Aggregated per-point totals: SFMR_TotalPointCounts.csv (Point, Restoration_status, FirstSurvey and SecondSurvey totals by time window and distance)

## Data quality and provenance

- Protocol adherence: Data collected using standardized field procedures by trained fieldworkers
- Quality assurance: Data digitized from field sheets and double-checked prior to upload
- Documentation: Species codes linked via SFMR_SpeciesCodes.csv

## Considerations and potential analyses

- Comparative analyses: Assess effects of restoration status on avian abundance, using both raw (per species) and total counts
- Temporal aspects: Analyze first vs. second surveys; account for repeated sampling and potential temporal autocorrelation
- Effort and scaling: Normalize by survey effort (3-minute vs 5-minute) or combine with per-minute rates
- Data gaps: Handle points not sampled twice (missing data) and points with limited sampling due to field conditions
- Species mapping: Use SFMR_SpeciesCodes.csv to translate codes to species names for interpretation
- Spatial context: Incorporate coordinates (Long, Lat) for spatial analyses or mapping of restored vs unrestored sites
- Contextual caveats: Data collected in a post-wildfire context; results reflect avian response under these specific conditions and dates (June 2021) and may not generalize beyond this period

## Access and metadata

- Data provenance: Collected via established field methods (Ralph et al. 1993; Stephens et al. 2010)
- Metadata references: Field protocols and study design described in the dataset files and their accompanying notes
- Reusability: Datasets structured to support site-level and species-level analyses; relationships between point coordinates, species codes, and counts are explicit for reproducible analyses