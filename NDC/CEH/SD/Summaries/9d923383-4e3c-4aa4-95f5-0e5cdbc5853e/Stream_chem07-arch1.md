# Headwater stream water chemistry data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes the STREAM_CHEMISTRY_2007.csv dataset from the Countryside Survey (2007), managed by NERC - Centre for Ecology & Hydrology.
- Contains chemical analysis data from headwater streams sampled in 2007 across Great Britain.
- Includes field measurements (conductivity, pH) and laboratory-derived parameters (SRP, TON, alkalinity) from filtered samples.

## Data contents
- Measured determinands include:
  - Conductivity and pH (field measurements)
  - Soluble reactive phosphorus (SRP)
  - Total oxidisable nitrogen (TON)
  - Alkalinity (from 50 ml filtered samples)

## Dataset structure and key variables
- CS_SURVEY: Year of Survey (text)
- SQUARE: 1 km square sampling site code (text)
- SITE_ID: Stream site identifier (numeric)
- SAMPLE_DATE: Date sample taken (date)
- DETERMINAND_NAME: Chemical determinand (text)
- DETERMINAND_UNITS: Units of chemical determinand (text)
- VALUE: Value of chemical determinand (numeric)
- LC07: Land class 2007 (text)
- LC07_NUM: Land class 2007 (numeric code)
- EZ_DESC_07: Environmental zone (text)
- COUNTY07: County (England & Wales) or Council (Scotland) (text)
- COUNTRY: England (Eng), Scotland (Sco) or Wales (Wal) (text)

## Classification and geographic context
- LC07 and LC07_NUM reference the ITE Land Classification of Great Britain 2007.
- EZ_DESC_07 provides environmental zoning information.
- COUNTY07 and COUNTRY give geographic context at county and country level.

## Usage and attribution
- All use of Countryside Survey data must be acknowledged with:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## References / related documents
- Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual. NERC/Centre for Ecology & Hydrology.
- Dunbar, M.; Murphy, J.; Clarke, R.; Baker, R.; Davies, C.; Scarlett, P. 2010. Countryside Survey: Headwater Streams Report from 2007. NERC/Centre for Ecology & Hydrology.