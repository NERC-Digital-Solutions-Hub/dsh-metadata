# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

## Overview
- Daily snowline observations from 140 Scottish locations, 1945–2007, stored as txt files.
- Observations are snowline elevations (metres above sea level) recorded in 150 m bands (0–1200 m).
- Data are transcribed from paper records and stored within the Environmental Information Data Centre.
- The dataset supports historical climate and hydrological research and is available via MIDAS (Met Office Integrated Data Archive System) and the British Atmospheric Data Centre.

## Data collection
- Observers, largely volunteers (estates, water authorities, Nature Conservancy/Scottish Natural Heritage, energy companies, Forestry Commission, etc.), recorded snowline each winter (typically Oct–May) from 1937–2007.
- Observations were made at 09:00 GMT (or thereabouts) and included:
  - Whether snow was lying at station level and its depth.
  - Snow lying at visible elevations when coverage exceeded half the ground.
  - Fog or cloud obscuration notes.
- Noted that observations were not always standardized (e.g., some days with no observations).

## Data transcription
- For each station, metadata captured: site name, elevation (m ASL), easting, northing, hills visible, comments (data quality notes).
- Comments used to record data quality and observations (e.g., misinterpretations or partial snow patches).
- Missing values recorded when obscured or observer absent, but may be indistinguishable from no snow.
- Transcription took ~3 months, involving ~16,750 return sheets (one per station per month).
- Data uploaded to the Met Office MIDAS database; raw transcribed data available via the British Atmospheric Data Centre.
- Dataset described here differs from BADCentre in including station metadata and specific alterations to station identities.

## Data structure
- Three file groups (delimited by pipe to avoid comma confusion):
  - Station_details.txt
  - SSGB_year_xxxx.txt
  - SSGB_st_yyyy.txt
- Station_details.txt columns (Table 2):
  - KeyName: Unique station identifier
  - Place: Station name
  - Easting: British National Grid easting (m)
  - Northing: British National Grid northing (m)
  - HillsVisible: Visible hills listed by the observer
  - Comments: Transcription notes
- SSGB_year_xxxx.txt and SSGB_st_yyyy.txt columns (Table 3):
  - Date: Observation date (yyyy-mm-dd)
  - KeyName: Station identifier
  - Snowline: Snowline elevation as observed (m)
  - SnowlineElev: Snowline elevation with station elevation substituted for 'st' notation
- Snowline and SnowlineElev values (Table 4):
  - 0, 150, 300, 450, 600, 750, 900, 1050, 1200 (snowline bands)
  - n: No snow observed
  - st: Snow at the station elevation (in Snowline only)
  - 99: Missing observation

## Variables and values
- Snowline: Either a band value (0–1200), or n/missing indicators; st indicates station-elevation snow in Snowline column.
- SnowlineElev: Equivalent numeric value as Snowline with 'st' resolved to station elevation; 99 retained as missing when appropriate.

## Data quality and limitations
- Non-standardized observations across days and stations; some days missing due to observer absence or poor visibility.
- Qualitative notes in Comments reveal data quality issues and interpretation nuances.
- Some stations underwent name changes or possible mergers/duplications (e.g., Shin -> Cassley Power Station; Ardclach -> Glenferness; Tarfside -> Glen Esk); potential station identity ambiguities (e.g., Dykecrofts and Newcastleton).
- After transcription, quality assurance checked for typographical errors, but no deeper data validation beyond that.
- Differences from BADCentre arise from added station metadata and alterations to station identities.

## Access and provenance
- Paper records archived at Met Office; transcribed into electronic format.
- Transcribed data uploaded to MIDAS; raw transcribed data accessible via MIDAS and the British Atmospheric Data Centre.
- The present dataset includes station metadata and record alterations, and reflects changes in station identities over time.

## Governance and stewardship implications for data leaders
- Demonstrates the value of robust metadata (Station_details) for station identification, location, visibility, and quality notes.
- Highlights challenges in harmonizing long-running, volunteer-collected datasets (name changes, station mergers, observational inconsistencies).
- Underlines the importance of clear provenance, data lineage, and notes on data quality to enable trustworthy reuse.
- Supports data discoverability and reuse through standardized file structures, explicit variable definitions, and availability in established data archives (MIDAS, BADCentre).
- Suggests potential benefits of ongoing data stewardship practices: standardizing station identities, documenting observation protocols, and maintaining metadata describing data quality and limitations for future users.

## References
- Anon. Snow survey of the British Isles. Journal of Glaciology, 1947.
- Spencer, M., Essery, R., Chambers, L., and Hogg, S. The historical snow survey of Great Britain: Digitised data for Scotland. Scottish Geographical Journal, 130(4):252-265, December 2014.