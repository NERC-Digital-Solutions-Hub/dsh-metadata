# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

## Overview
- Describes the transcribed Scottish portion of the Snow Survey of Great Britain (SSGB), covering daily snowline observations at 140 Scottish locations from 1945 to 2007.
- SSGB records the lowest snow cover level as snowline elevations above sea level, typically reported in 150 m bands.
- Dataset storage and access are through the Environmental Information Data Centre, with raw transcriptions also linked to the Met Office/MIDAS and the British Atmospheric Data Centre (BACDC).

## Data collection (what was observed)
- Observers (volunteers) recorded the snowline level and, when snow was lying, the elevation bands where lying snow covered more than half the ground.
- Observations typically occurred daily during winter (usually October–May) at about 09:00 GMT; fog or cloud obscuration was also noted.
- Elevations were grouped into 150 m bands from 0 to 1200 m ASL (earlier records used 500 ft increments).
- Nine days of non-observation at a station were common, highlighting a lack of standardization across times and observers.

## Transcription process and metadata
- For each station, metadata collected: site name, elevation (m ASL), easting, northing, hills visible, and observer_comments (data quality notes).
- Missing values were transcribed when observations were obscured or the observer was absent; such missing data can be indistinguishable from times with no snow.
- Transcription converted paper returns into a spreadsheet format: each column is a station, each row is a day; roughly 16,750 station-month sheets were entered over ~3 months.
- Post-transcription QA focused on typographical errors; no additional statistical or consistency checks reported.
- Transcribed data were uploaded to MIDAS (Met Office Integrated Data Archive System); raw transcriptions are accessible via BACDC.
- Dataset variant notes: differences from BACDC due to station metadata and alterations (e.g., station name changes and potential station mergers). Some station identity remains ambiguous (e.g., Dykecrofts vs Newcastleton).

## Dataset structure and variables
- Three file groups:
  - Station_details.txt: station metadata (identifier, name, easting, northing, hills visible, comments).
  - SSGB_year_xxxx.txt: data by year.
  - SSGB_st_yyyy.txt: data by station.
- Variables (described in accompanying tables):
  - Date (yyyy-mm-dd)
  - KeyName (station identifier)
  - Snowline (observed elevation in metres)
  - SnowlineElev (same as Snowline; 'st' replaced with station elevation when applicable)
  - HillsVisible, Comments (metadata and observation notes)
- Snowline values include:
  - 0, 150, 300, ..., 1200 (snowline elevations in metres)
  - n = No snow observed
  - st = Snow at the station elevation (in Snowline column)
  - 99 = Missing observation
- In this dataset, observations originally marked as 'st' in the SSGB papers were converted to the nearest corresponding 150 m elevation band.

## Data quality, limitations, and harmonisation
- Non-standardized observations across years and observers; observational notes sometimes reflect data quality concerns.
- Ambiguities exist where missing data could indicate either no snow or observer absence.
- Station changes and name changes complicate longitudinal continuity; some stations may correspond to the same site under different names.
- Harmonisation efforts attempted to combine nearby or renamed stations, but uncertainty remains for some site pairings (e.g., Dykecrofts vs Newcastleton).

## Storage, access, and provenance
- Source data originally paper copies stored in Met Office archives; transcribed to electronic format for inclusion in MIDAS.
- Raw transcribed data available via BACDC; dataset described here adds station metadata and explicit alterations to station identity.
- Historical context and transcription methodology are documented to support reuse and reproducibility.

## Relevance for environmental monitoring and analysis
- Provides a long-term, standardized-like time series of snowline elevations across Scottish uplands, enabling assessment of snow cover conditions and potential climatic trends over six decades.
- Useful for calibrating or validating regional snow models, plus cross-referencing with other meteorological observations.
- Benefits from the standardized file structure and explicit metadata, while requiring careful handling of non-standard observations, missing data, and station harmonisation when integrating with other datasets.

## References
- Anon. Snow survey of the British Isles. Journal of Glaciology, 1947.
- Spencer, M., Essery, R., Chambers, L., and Hogg, S. The historical snow survey of Great Britain: Digitised data for Scotland. Scottish Geographical Journal, 130(4):252-265, 2014.