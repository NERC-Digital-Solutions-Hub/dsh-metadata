# Headwater stream water chemistry data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Dataset description for the Freshwater Stream - Water chemistry data collected in headwater sites during 1998 the Countryside Survey (CS).
- Part of Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; supports analyses of freshwater chemistry in headwaters.
- References to accompanying manuals and reports provide context for field methods and data packaging.

## Data table and fields
- Table name: STREAM_CHEMISTRY_98.csv
- Brief purpose: Chemical analysis from headwater stream waters sampled in 1998.
- Core measurement variables (field and lab):
  - Conductivity (field measurement)
  - pH (field measurement)
  - Soluble reactive phosphorus (SRP)
  - Alkalinity
- Core row-level fields:
  - YEAR: Year of survey (text)
  - SQUARE: 1 km square sampling site code (text)
  - SITE_ID: Site identifier within the 1 km square (numeric)
  - SAMPLE_DATE: Date sample taken (date)
  - SAMPLE_TYPE: Type of sample (text)
  - DETERMINAND_NAME: Chemical determinand (text)
  - DETERMINAND_UNITS: Units of the determinand (text)
  - VALUE: Value of the chemical determinand (numeric)
- Additional fields for geographic and classification context:
  - LC07: Land class 2007 (text)
  - LC07_NUM: Land class 2007 (numeric code)
  - EZ_DESC_07: Environmental zone (text)
  - COUNTY07: County (Eng & Wal) or Council (Sco) (text)
  - COUNTRY: England, Scotland, or Wales (text)

## Measurement details
- Each headwater site yields measurements for multiple chemical determinands across the 1998 survey.
- Sample handling: SRP and alkalinity measured from 50 ml filtered samples.
- Field measurements: Conductivity and pH recorded in-field.

## Geographic and classification fields
- SQUARE: 1 km grid reference for site localization.
- SITE_ID: Unique site identifier within the square.
- LC07 / LC07_NUM: 2007 land classification codes and descriptions associated with the site.
- EZ_DESC_07: Environmental zone descriptor.
- COUNTY07 / COUNTRY: Administrative geographic context for the site.

## Data usage and attribution
- All use of Countryside Survey data must include the specified acknowledgement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data are part of CS data compilations and are subject to copyright and usage terms.
- This description references supplementary materials for methods and background:
  - Countryside Survey 2000 modules and freshwater studies
  - Freshwater Manual and Headwater Streams reports
  - Environment Agency technical reports and related CEH documents

## Related documentation and sources
- Supporting documents and manuals:
  - Furse et al., 1998 and 2002–2000 CS modules (field handbook and freshwater studies)
  - Murphy & Weatherby, 2008 Countryside Survey: Freshwater Manual
  - Dunbar et al., 2010 Countryside Survey: Headwater Streams Report from 2007
  - ITE Land Classification of Great Britain 2007 (for LC07)
- Data access and provenance:
  - CEH / NERC Environmental Information Data Centre
  - Nora/NERC repository links provided in the data description for related materials

## Notes for analysts
- The dataset is suitable for analyzing headwater stream chemistry, linking chemical determinants to land use/classification and environmental zones.
- Consider the single-year scope (1998) for temporal analyses; combine with other CS years for trend insights if available.
- Ensure proper data provenance and acknowledgement in any outputs; cross-reference related CS reports for methodological context.