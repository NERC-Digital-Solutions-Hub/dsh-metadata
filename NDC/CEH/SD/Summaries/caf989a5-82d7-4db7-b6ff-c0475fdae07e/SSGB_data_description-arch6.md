# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

## Overview
- Daily observations of snowline from the Snow Survey of Great Britain (SSGB) at 140 Scottish locations, 1945–2007.
- Observations record the lowest snow cover in 150 m elevation bands, stored in the Environmental Information Data Centre.
- dataset derived from paper records transcribed to electronic format; volunteers contributed data; used for annual Snow Survey reports (1947–1992).

## Data collection
- Observers noted snowline in metres above sea level, typically October–May; elevations grouped into 150 m bands (0–1200 m).
- Observations aimed to be at 09:00 GMT; recorded when snow was lying at station level and its depth; sometimes noted visibility and fog.
- Observations were not fully standardised across stations; gaps occurred (e.g., days with no observations).

## Data transcription
- For each station: metadata captured (site name, elevation, easting, northing, hills visible, transcription notes).
- Comments recorded data quality, e.g., distinguishing isolated patches from continuous snow; missing values logged when obscured or absent, though could be indistinguishable from “no snow.”
- Transcription converted returned data (paper) into a spreadsheet: rows = days, columns = stations (about 16,750 return sheets).
- Quality assurance focused on typographical errors; no comprehensive data consistency checks beyond that.
- Data uploaded to Met Office MIDAS; the transcribed dataset differs from the British Atmospheric Data Centre (Badc) version by including station metadata and alterations (e.g., station name changes, consolidation of stations).

## Data structure and contents
- Three file groups:
  - Station_details.txt: metadata for each station (unique station identifier, name, coordinates, hills visible, comments).
  - SSGB_year_xxxx.txt: data split by year.
  - SSGB_st_yyyy.txt: data split by station.
- Key variables:
  - Date (yyyy-mm-dd), KeyName (station identifier), Snowline (observed snowline in metres), SnowlineElev (same but with ‘st’ replaced by station elevation).
- Snowline values: 0–1200 m in 150 m steps; “n” = no snow observed; “st” = snow at station elevation; “99” = missing observation.
- Observers’ comments and station details help identify data context and potential issues (e.g., visibility, station visibility changes).

## Data quality, limitations, and considerations
- Observations not fully standardised across all stations and years; some stations share or swap names.
- Distinguishing between “no snow” and missing data can be challenging.
- Conversions (e.g., original ‘st’ markers) and station consolidations may affect comparability across time.
- Data quality control referenced but limited to typographical checks; no extensive cross-validation described.

## Access and availability
- Original transcription stored in MIDAS (Met Office Integrated Data Archive System).
- The published dataset version includes station metadata and documented alterations; available via the British Atmospheric Data Centre as part of the SSGB Scottish data digitisation project.
- File coverage: Station_details (1 file), SSGB_year_xxxx (62 files), SSGB_st_yyyy (140 files).

## Uses and context
- Facilitates historical analysis of snowline and altitude-dependent snow cover in Scotland.
- Supports climate and hydrological research by providing long-term, station-based snow observations from 1945–2007.
- Useful for understanding data collection challenges, station changes, and transcription-based data preservation.

## References
- Anon. Snow survey of the British Isles. Journal of Glaciology, 1947.
- Spencer, M., Essery, R., Chambers, L., and Hogg, S. The historical snow survey of Great Britain: Digitised data for Scotland. Scottish Geographical Journal, 2014.