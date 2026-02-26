# Automatic Weather Station recordings from Moor House and Helbeck, Cumbria, 1974 - 1987

## Purpose and scope
- Historic Automatic Weather Station (AWS) dataset from Moor House and Helbeck, Cumbria, UK.
- Collected by Ken Taylor and stored in a database described by Cuthbertson (1993).
- Related to ongoing monitoring at Moor House by the UK Environmental Change Network (ECN) (Rennie et al., 2017).

## Site locations and temporal coverage
- Helbeck AWS: located in a wood near Brough, Cumbria (grid reference 378900 516000).
- Moor House AWS: grid reference 375100 533400.
- Recorded time periods include multiple series with hourly and daily readings:
  - Helbeck: hourly readings (1974–1978; 01-Jan-1978 to 18-Oct-1983 elsewhere).
  - Moor House: daily and hourly readings (1974–1979; 1979–1987 for Moor House series).

## Recording variables and data structure
- Core variables (per DATID entries):
  - REC_TIME: recording date (DD-MM-YYYY)
  - REC_HOUR: hour of recording (0–23)
  - SOL_RAD: Solar radiation (W/m^2)
  - AIR_TEMP: Air temperature (°C)
  - DEP_TEMP: Depression temperature (°C) – difference between dry and wet bulb temperatures
  - WIND_VEL: Wind velocity (km/h or km/day depending on series)
  - WIND_DIR: Wind direction
  - RAINFALL: Rainfall (mm)
- Additional identifiers:
  - DATID: dataset identification record number
  - NO_REC: number of recordings used to establish the record
- Data presentation includes both site-specific descriptions and earliest/latest dates for each series.

## Data quality, metadata, and gaps
- Notable missing values present; reasons for missing data unknown (historic dataset).
- Quality assurance procedures for the data are unknown due to its age.
- Metadata completeness and standardization may be limited, posing challenges for integration and verification.
- Transformation may be required to harmonize units and formats across series.

## Data governance and accessibility considerations
- Historical nature and potential lack of QA and metadata complicate public sharing and reuse.
- For monitoring frameworks: would require contacting originators or custodians to verify provenance and to obtain any available metadata.
- Potential for linkage with ECN data (post-1991) to extend temporal coverage and support continuity, subject to compatibility.

## Implications for environmental health monitoring frameworks
- Provides two-site, multi-year meteorological data useful for context in environmental health assessments (e.g., temperature, solar radiation, wind, precipitation).
- Useful as a case study for data discovery, provenance verification, and integration challenges in monitoring programs.
- Highlights common barriers: data gaps, limited QA information, inconsistent metadata, and the need for data governance to enable reuse.

## Recommendations for leveraging in monitoring work
- Initiate provenance verification by consulting dataset originators and Cuthbertson (1993) description.
- Assess and document metadata completeness; standardize variable names, units, and temporal resolutions.
- Implement data quality checks where possible; annotate missing values and uncertainties.
- Consider digitizing and harmonizing data into a modern data model; create a clear data lineage and governance plan.
- Explore linkage with ECN Moor House data (1991–2015) for extended trend analyses, ensuring methodological compatibility.
- Proactively address data sharing barriers by defining access controls and metadata publishing practices to meet openness requirements.