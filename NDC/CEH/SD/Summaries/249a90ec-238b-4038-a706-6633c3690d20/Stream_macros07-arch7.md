# Headwater stream macrophyte data 2007 [Countryside Survey] Dataset description

## Overview
- Describes the Headwater stream macrophyte dataset from Countryside Survey 2007.
- Intended to support map-based data products and GIS analyses; data can be used with the accompanying manuals and reports.

## Data structure and content
- Primary table: STREAM_MACROPHYTES_07.csv
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of Survey (text; CS +Yr)
  - SITE_ID: Site identifier within the 1km square (numeric)
  - SURVEY_DATE: Date of survey (date)
  - PLANT_NAME: Scientific name of plant (text)
  - PROPORTION: Proportion (%) of the 100m stream reach covered by the plant (text)
  - LC07: Land class 2007 (text) with LC07_NUM as its numeric code
  - EZ_DESC_07: Environmental zone description (text)
  - COUNTY07: County (Eng/Wal) or Council (Sco) for the square (text)
  - COUNTRY: England, Scotland, or Wales (text)

- Notes:
  - Uses the standard Mean Trophic Rank (MTR) protocol for 100m stream reaches, but employed a broader plant species checklist than typical MTR use.
  - Data collected and stored via tablet computers with custom software.

## Methods and context
- Data collection follows the MTR protocol (Holmes et al. 1999) for presence and extent of macrophytes in a 100m reach.
- A more extensive plant species checklist was used than required for standard MTR.
- Data captured with tablet-based, custom software during Countryside Survey 2007.

## GIS and analysis implications
- Geospatial linkage: Each record is tied to a 1km square (SQUARE), enabling GIS joins to grid-based maps.
- Rich attributes for mapping and analysis:
  - Plant-specific abundance (PROPORTION) by site within a square
  - Land classification (LC07 and LC07_NUM)
  - Environmental zone (EZ_DESC_07)
  - Administrative geography (COUNTY07, COUNTRY)
- Suitable for examining spatial patterns of headwater macrophytes across GB, with resolution at 1km squares and 100m stream reaches.

## Usage rights and acknowledgements
- All Countryside Survey data must be acknowledged.
- Acknowledgement language: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”

## Related resources
- Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual (CS Technical Report No.5/07)
- Dunbar, M. et al. 2010 Countryside Survey: Headwater Streams Report from 2007
- Holmes N.T.H. et al. 1999 Mean Trophic Rank: A users' manual
- Access to related documents: final PDF and additional information available via CEH/NERC portals

## Data provenance and contact
- Source: Countryside Survey data (2007), CEH/NERC
- Supporting documents provide methodological details and reporting context for headwater streams.