# Snow Survey of Great Britain: transcribed Scottish data (1945 to 2007)

- What the dataset is
  - Daily observations of snowline from the Snow Survey of Great Britain (SSGB) for Scotland, 140 locations, 1945–2007.
  - Contains the lowest snow cover levels (as observed) recorded in 150 m elevation bands up to 1200 m ASL, with notes on visibility and observer remarks.
  - Described as the transcribed version of paper records, stored in the Environmental Information Data Centre (EIDC).

- Data collection approach
  - Voluntary observers stationed at estates, water authorities, nature conservation bodies, energy companies, forestry, etc.
  - Observations typically made at 09:00 GMT, noting snow lying at station level and its depth.
  - Elevation bands used: 0–1200 m in 150 m increments (earlier in the record, bands were 500 ft).
  - Observers recorded hills visible from the site and any weather conditions affecting observation (e.g., fog, cloud).
  - Observations were not always standardised; some days/entries reflect variations in reporting.

- Data transcription and quality assurance
  - Paper SSGB returns were transcribed into electronic format, including station metadata and daily observations.
  - Metadata captured per station: site name, elevation (m ASL), easting, northing, hills visible, and transcription comments (data quality notes).
  - Missing values were transcribed when observations were obscured or a sampler was absent; however, it can be difficult to distinguish from true “no snow.”
  - Transcription took about three months and involved roughly 16,750 return sheets (one sheet per station per month).
  - Quality checks focused on typographical errors; broader data validation against other sources was not performed in this transcription.

- Data structure and file organization
  - Three file groups, delimited by pipes (|) to avoid comma-related confusion:
    - Station_details.txt: station metadata
      - KeyName (station identifier), Place (station name), Easting, Northing, HillsVisible, Comments
    - SSGB_year_xxxx.txt: data by year (62 files)
      - Date (yyyy-mm-dd), KeyName, Snowline, SnowlineElev
      - Snowline: observed snowline elevation in metres; SnowlineElev: Snowline with “st” replaced by the station elevation when relevant
    - SSGB_st_yyyy.txt: data by station (140 files)
      - Same variables as SSGB_year_xxxx.txt
  - Potential Snowline values
    - 0, 150, 300, 450, 600, 750, 900, 1050, 1200 (snowline elevations in metres)
    - n = no snow observed
    - st = snow at the station elevation (only in Snowline column)
    - 99 = missing observation (e.g., observer absence, cloud)
  - Station coordinates are in the British National Grid (easting/northing)

- Data availability and provenance
  - Raw transcribed data are available via the Met Office MIDAS database, and the British Atmospheric Data Centre (BADC).
  - The released dataset differs from the BADC version by including station metadata and specific alterations described in the transcription process.
  - Station naming has been harmonised where possible, but some inconsistencies remain due to historical name changes and potential station duplication (e.g., name changes over time, or ambiguous station identity).

- Limitations and considerations for analysis
  - Observations are not fully standardised across time and sites; some entries reflect observer notes and irregular reporting.
  - Some stations may be the same site under different names or may have moved within a village; careful station reconciliation is needed.
  - Missing data and ambiguous entries (e.g., distinguishing “no snow” from days with no observation) can affect time-series analyses.
  - Data at local scales (individual stations) may present challenges for broad-scale trend analyses without careful harmonisation and QA.
  - The dataset emphasizes snowline altitude rather than snowfall depth, which is valuable for altitude-dependent snowpack studies and climate relationships.

- References
  - Anon. Snow survey of the British Isles. Journal of Glaciology, 1947.
  - Spencer, M., Essery, R., Chambers, L., and Hogg, S. The historical snow survey of Great Britain: Digitised data for Scotland. Scottish Geographical Journal, 130(4):252-265, December 2014.