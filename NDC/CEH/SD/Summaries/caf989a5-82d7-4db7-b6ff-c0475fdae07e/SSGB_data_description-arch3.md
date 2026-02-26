# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

## Overview
- Describes the transcribed Scottish component of the Snow Survey of Great Britain (SSGB) data, covering 1945–2007.
- Original SSGB: daily snowline observations at 140 Scottish locations, collected by volunteers and used for regional snow assessments and annual reports (1947–1992).
- Data now stored with station metadata and accessible through archival data centers.

## Data scope and collection
- Observations: snowline height above sea level, recorded daily (autumn to spring, typically Oct–May) at 09:00 GMT, with depth when snow is lying.
- Elevation bands: 150 m steps from 0 to 1200 m (earlier data used 500 ft increments).
- Observers included volunteers from estates, water authorities, energy companies, Forestry Commission, and others.
- Instructions aimed to capture representative snow occurrence across upland districts; observations outside standard times or missing days noted as data quality remarks.
- Some records indicate non-standard observations (e.g., patchy snow, observer absence) and variable visibility.

## Transcription and metadata
- Paper SSGB sheets were transcribed into electronic form, including:
  - Station name, elevation (m ASL), easting, northing, hills visible, and transcription comments.
  - Missing values noted where observations were obscured or observers absent.
- Transcription duration approx. three months for ~16,750 sheets.
- Post-transcription, data were uploaded to the Met Office MIDAS database and are publicly accessible via the British Atmospheric Data Centre.
- This dataset differs from the BA BDC version by including station metadata and altered formatting to reflect transcription decisions (e.g., station name changes over years).

## Data structure and files
- Three file groups:
  - Station_details.txt: station metadata (station ID, place name, easting, northing, hills visible, comments).
  - SSGB_year_xxxx.txt: data split by year.
  - SSGB_st_yyyy.txt: data split by station.
- Files are pipe-delimited to avoid comma-related confusion.
- Key variables:
  - Date (YYYY-MM-DD)
  - KeyName (station identifier)
  - Snowline (observed elevation of snow lying)
  - SnowlineElev (same, with 'st' replaced by station elevation)
- Potential values for Snowline/SnowlineElev:
  - 0, 150, 300, 450, 600, 750, 900, 1050, 1200 (snowline at those bands)
  - n = No snow observed
  - st = Snow at the station elevation (in Snowline column)
  - 99 = Missing observation
- Spatial and temporal data coverage visuals are provided in the documentation (station distribution and record length).

## Data quality, limitations, and notes
- Quality checks conducted: typographical QA; deeper data quality checks were not performed.
- Challenges include:
  - Some stations effectively represent multiple historical names; consolidation required.
  - Some stations may be the same physical location under different names.
  - Observations on days with obscured visibility or observer absence may be indistinguishable from no snow.
  - Observations are not fully standardized across all years and stations.
- Metadata and observational notes (Comments) used to assess data quality and context.

## Provenance, access, and governance
- Primary source: Met Office (data c Crown copyright and database rights).
- Raw transcription preserved and hosted; transcribed data accessible via the British Atmospheric Data Centre.
- Data governance includes documenting metadata, ensuring openness, and acknowledging changes in station naming and data formats over time.

## Relevance for monitoring frameworks
- Demonstrates the lifecycle of a long-running environmental monitoring dataset:
  - Establishing observation protocols, volunteer-based data collection, and historical continuity.
  - Challenges of data standardization, metadata completeness, and data accessibility.
  - Importance of structured metadata, data provenance, and transparent data transformations for re-use.
- Highlights practical considerations for monitoring programs:
  - Managing data gaps, non-standard observations, and evolving station identities.
  - Balancing openness with provenance and data governance obligations.
  - Providing multiple data views (year- and station-based) to support analysis and cross-study comparability.