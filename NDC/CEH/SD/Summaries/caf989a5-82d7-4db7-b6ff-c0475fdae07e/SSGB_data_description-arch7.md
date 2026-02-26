# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

## Overview
- Daily snowline observations from 140 Scottish SSGB stations, 1945–2007, recorded in 150 m elevation bands up to 1200 m.
- Data sourced from paper records stored at the Met Office; transcribed to electronic format and described for use in GIS and data products.
- Metadata and transcription differences exist compared with the BACD version; dataset is provided with station metadata and specific alterations.

## Data collection
- Observers recorded the lowest snow cover level and, if snow lay at station level, the depth; observations typically at 09:00 GMT.
- Snow lying at visible elevations was noted when coverage exceeded half the ground at a given elevation.
- Fog or cloud obscuring observation was also recorded.
- Elevations were grouped into 150 m bands (0–1200 m ASL); metric values became common by the early 1980s.
- Observations are from volunteers affiliated with estates, water authorities, nature agencies, energy companies, etc.; not all observations are standardised.

## Data transcription
- For each station, metadata collected: site name, elevation (m ASL), easting, northing, hills visible, and transcription comments (data quality notes).
- Comments captured nuances such as isolated snow patches or continuous snow; missing values logged when obscured or absent, though sometimes indistinguishable from no snow.
- Transcription process: lowest snowline elevations transcribed into a day-by-station spreadsheet (approximately three months per station; ~16,750 sheets).
- Quality assurance focused on typographical checks; no extensive data validation beyond that.
- Post-transcription, data uploaded to the Met Office MIDAS database; raw transcribed data also accessible via the British Atmospheric Data Centre (BACD).

## Data structure and content
- Three file groups:
  - Station_details.txt: station metadata (KeyName, Place, Easting, Northing, HillsVisible, Comments).
  - SSGB_year_xxxx.txt: observations by year (Date, KeyName, Snowline, SnowlineElev).
  - SSGB_st_yyyy.txt: observations by station (same columns as year files).
- Data are pipe-delimited to avoid comma-confusion.
- Snowline values: 0, 150, 300, ..., 1200 (metres). Special codes: n = no snow observed; st = snow at the station elevation (in Snowline); 99 = missing observation.
- SnowlineElev mirrors Snowline but replaces 'st' with the station’s elevation.
- Station metadata includes station location (Easting/Northing in British National Grid) and hills visible from the site.
- Station changes: some stations have undergone name changes or amalgamations (e.g., Shin to Cassley Power Station, Ardclach to Glenferness, Tarfside to Glen Esk); some near-duplicates may represent the same location.

## Geographic and practical implications
- Coordinates (British National Grid) enable GIS-based mapping of snowline dynamics over time.
- Data suitable for time-series spatial analysis of snow cover relative to elevation bands and station location.
- Variations in observation practices and non-standard days require careful cleaning and harmonisation for GIS analyses.

## Data quality and limitations
- Observations were not always standardised; quality notes exist in the Comments field.
- Missing data may reflect observer absence, poor visibility, or genuine absence of snow; distinction not always clear.
- Some stations may represent the same location due to name changes; merging requires expert judgement.
- Limited post-transcription data validation beyond typographical checks; some inconsistencies may remain.

## Access and references
- Data availability: delivered via the Met Office MIDAS database; raw transcribed data also accessible from BACD.
- Related literature: 
  - Anon. Snow survey of the British Isles (1947).
  - Spencer, Essery, Chambers, and Hogg (2014) on digitised Scottish data.