# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset description

## Overview
- RHS is a standardized assessment of the physical structure of freshwater streams and rivers using a 500 m sample unit.
- Surveys require accredited surveyors and follow published protocols to ensure consistency.
- Data are collected for Countryside Survey and held by NERC - Centre for Ecology & Hydrology (CEH); data owners emphasize governance and usability.

## Data collection and provenance
- Field data collected in 2007 on tablet computers and uploaded to a central CEH database.
- A comprehensive audit and checking process follows data entry.
- Primary documentation and context are provided by:
  - Murphy, J. & Weatherby, A. 2008 Freshwater Manual (Countryside Survey)
  - Dunbar et al. 2010 Headwater Streams Report (2007 data)
  - River Habitat Survey official website

## Data structure and contents
- Data are stored in multiple CSV tables:
  - STREAM_RHS_SURVEY_main_07.csv: site-level details and sections A–Q for each 1 km square; key fields include SQUARE (site code), SITE_ID, CS_SURVEY (year), COUNTRY, COUNTY07, LC07 (land classification), environmental zones, hydrological unit (HYDRO_UNIT), survey date, flow category, catchment area, Strahler order, geology, and extensive channel morphology and vegetation metrics.
  - STREAM_RHS_SURVEY_spotcheck_07.csv: spot-check data for Sections E–G (year, square, land class, bank/spot-check specific attributes).
  - STREAM_RHS_SURVEY_bank_07.csv: Sections H and I (bank-related attributes, land use near banks, channel features, and habitat/vegetation observations).
- Fields cover a wide range of data types: textual descriptors, numeric measurements (e.g., banktop height, water width/depth), categorical codes (e.g., CH_REALIGN, WAT_IMP_DAM), and qualitative observations (habitat features, vegetation types, nuisance species).
- Data include documented definitions and coding (e.g., land class codes, flow categories, habitat feature descriptors) and reference to standard classification schemes (ITE land classification, hydrological units).

## Data quality and provenance
- Data collection requires accredited surveyors and strict adherence to standardized RHS protocols to ensure comparability.
- Data entry and quality control performed by CEH, with an explicit audit process.
- Documentation and supporting materials exist to enable proper interpretation and reuse.
- Clear copyright and usage notes accompany the data.

## Access, reuse, and governance
- Data are provided with clear provenance and are intended to be discoverable and usable for researchers and practitioners.
- Access is accompanied by formal acknowledgements:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Rights/Copyright NERC-Centre for Ecology & Hydrology; all rights reserved.
- All use of Countryside Survey data must be acknowledged in publications, presentations, and other outputs.
- Supporting documents and the RHS official website offer additional context and guidance for reuse and interpretation.

## Challenges and considerations for Data Stewards
- The dataset encompasses a large, multi-table structure with many specialized fields across different survey components, which can complicate interoperability and metadata alignment.
- Ensuring timely updates and maintaining consistency across tables (main, spot-check, bank) is essential for discoverability and reuse.
- Users have diverse needs (e.g., geomorphology, hydrology, vegetation, land use), so clear metadata and documentation are critical for usability.
- Given the 2007 scope, stewardship should consider long-term preservation, versioning, and the need to link to related reports (e.g., Freshwater Manual, Headwater Streams Report).

## Acknowledgement and rights
- All CS data usage must include the specified acknowledgement statement.
- The dataset is copyright and rights reserved by NERC - CEH; access and reuse should comply with the accompanying licensing language.