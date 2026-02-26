# Avian data from the South Fork McKenzie River in Oregon, USA

## Aim and context
- Assess avian response to wildfire in restored and unrestored sites along the South Fork McKenzie River, Oregon.
- Data collected to support environmental health monitoring and policy performance evaluations over time.
- Location coordinates included for sampling points: approx. 44.17, -122.30.

## Datasets and structure
- Four CSV files:
  - SFMR_PointCoordinates.csv: Point, Restored_Status, Long, Lat
  - SFMR_SpeciesCodes.csv: CODE, Species
  - SFMR_RawPointCounts.csv: Point, Species, 3min_closer_than_50m, 3min_further_than_50m, 3min_flyover, 5min_closer_than_50m, 5min_further_than_50m, 5min_flyover, Date
  - SFMR_TotalPointCounts.csv: Point, Restoration_status, FirstSurvey_3min_closer_than_50m, FirstSurvey_3min_further_than_50m, FirstSurvey_3min_flyover, FirstSurvey_5min_closer_than_50m, FirstSurvey_5min_further_than_50m, FirstSurvey_5min_flyover, SecondSurvey_3min_closer_than_50m, SecondSurvey_3min_further_than_50m, SecondSurvey_3min_flyover, SecondSurvey_5min_closer_than_50m, SecondSurvey_5min_further_than_50m, SecondSurvey_5min_flyover
- Data fields capture counts by species (via codes), distance bands (<50m, >50m, flyover), time windows (3 and 5 minutes), and survey order.

## Sampling and methodology
- Method: standardized point counts of bird species.
- Recording protocol: observations conducted initially for 3 minutes, then an additional 2 minutes (total 5 minutes per survey).
- Distance categorization: closer than 50m, further than 50m, or flying overhead.
- Sites and sampling effort: 41 five-minute surveys total; 20 restored sites and 21 unrestored sites.
- Sampling dates:
  - Unrestored reaches: June 16 and June 23, 2021.
  - Restored reaches: June 17 and June 24, 2021.
- Field protocols referenced: Ralph et al. 1993 Handbook of Field Methods for Monitoring Landbirds; Klamath Network Landbird Monitoring Protocol (2010).

## Data quality and provenance
- Collected by trained fieldworkers using standardized procedures.
- Data digitized from field survey sheets and double-checked prior to upload.

## Usage notes and interoperability
- Designed to enable comparisons of avian abundance across restored vs unrestored reaches and to assess responses to wildfire.
- Structured to support data sharing and potential integration with other monitoring datasets; underlying data can be accessed for broader analyses.
- Counts are provided at both raw (per species per point per date) and aggregate (per point per survey) levels, facilitating varied analyses and indexing over time.