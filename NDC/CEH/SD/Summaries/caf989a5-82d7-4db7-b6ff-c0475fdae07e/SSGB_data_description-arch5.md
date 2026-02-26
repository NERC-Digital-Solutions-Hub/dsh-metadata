# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

- Long-running, volunteer-collected dataset of snowline observations (meters above sea level) at 140 Scottish stations from 1945 to 2007.
- Stored and described within the Environmental Information Data Centre; raw transcriptions uploaded to Met Office MIDAS; available via the British Atmospheric Data Centre (BADC).

## Data provenance and collection
- Observations taken during winter seasons (typically October–May) with a 09:00 GMT observation time.
- Snowline recorded in 150 m elevation bands (0–1200 m) with occasional use of feet in earlier years; observers listed visible hills and noted conditions (e.g., fog, cloud obscuring view).
- Observers were volunteers from estates, water authorities, national bodies, energy companies, and others; data used for the annual report (1947–1992).
- Instructions emphasize non-standardized practices on some days; occasional missing days noted in observer comments.
- Original data were paper returns; transcription converted to electronic format for storage and access.

## Transcription process and QA
- For each station, metadata captured: site name, elevation (m ASL), easting, northing, hills visible, and transcription comments.
- Transcription converted paper returns into a spreadsheet: rows = days, columns = stations.
- Approximately 16,750 return sheets were entered; quality assurance checked for typographical errors only; deeper data validation not performed.
- Some values were transcribed as missing when observations were obscured or the observer was absent; distinguishing missing from “no snow” was not always possible.
- Post-transcription, data were uploaded to MIDAS; the public dataset differs from BADC data by including station metadata and specific alterations described in the document.

## Data structure and schema
- Three file groups (pipe-delimited to avoid comma confusion):
  - Station_details.txt: station metadata (KeyName, Place, Easting, Northing, HillsVisible, Comments).
  - SSGB_year_xxxx.txt: yearly observations (Date, KeyName, Snowline, SnowlineElev).
  - SSGB_st_yyyy.txt: per-station observations (same columns as yearly file).
- Snowline values:
  - 0, 150, 300, 450, 600, 750, 900, 1050, 1200 (snowline elevations in metres).
  - n = no snow observed.
  - st = snow at the station elevation (replaced in this dataset by the nearest 150 m band in SnowlineElev).
  - 99 = missing observation (e.g., due to observer absence or cloud).
- Station metadata includes exact spatial coordinates (Easting/Northing in British National Grid) and descriptive fields (Place, HillsVisible, Comments).

## Data values, interpretation, and caveats
- Elevation bands standardised to 150 m increments; some stations were renamed or combined (e.g., Shin into Cassley Power Station; Ardclach into Glenferness) and may reflect station moves or name changes over time.
- Some stations may represent the same location under different names; consolidation was done where geographically close and longer-running records existed.
- Data quality notes in comments identify non-snow observations and data quality issues; not all quality checks beyond typographical validation were performed.
- Dataset scope and structure differ from the BADC version due to inclusion of station metadata and the documented alterations.

## Governance, access, and provenance
- Data held under Crown copyright; Met Office data and database rights noted.
- Original data management and hosting involve the Met Office (MIDAS) and the British Atmospheric Data Centre; the SSGB dataset described here includes station metadata and specific transcription-based alterations.
- Useful for historical climate and hydrological analyses; provenance and metadata are essential for correct interpretation and reuse.

## Data quality, limitations, and considerations for stewards
- Incomplete standardization across observations and days; potential ambiguities between “no snow” and missing data.
- Changing station identities and occasional renames require careful metadata management to maintain longitudinal continuity.
- QA focused on transcription accuracy; no extensive cross-validation with modern datasets described.
- When reusing, ensure alignment of station identifiers, elevation representations, and spatial coordinates; document any station merges or name changes.

## Data access and reuse guidance
- Data are accessible via the MIDAS archive, with the BADC hosting variations; ensure use of station metadata in conjunction with observation rows for correct interpretation.
- When integrating into new systems, preserve the three-file structure (Station_details, yearly, and per-station files) or migrate to a unified schema with explicit provenance and versioning.
- Consider documenting data lineage, transcription steps, and any alterations (e.g., “st” to SnowlineElev) for future users and governance records.

## References
- Anon. Snow survey of the British Isles. Journal of Glaciology, 1947.
- Spencer, M., Essery, R., Chambers, L., and Hogg, S. The historical snow survey of Great Britain: Digitised data for Scotland. Scottish Geographical Journal, 130(4):252-265, 2014.