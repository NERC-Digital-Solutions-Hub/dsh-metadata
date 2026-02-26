# Headwater stream water chemistry data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes STREAM_CHEMISTRY_2007.csv, which contains headwater stream water chemistry data collected in 2007 as part of Countryside Survey.
- Measured chemical parameters include field measurements of conductivity and pH, plus filtered measurements of soluble reactive phosphorus (SRP), total oxidisable nitrogen (TON), and alkalinity.
- Data intended for GIS-based visualization and analysis of spatial patterns in stream chemistry.

## Data table structure
- Data types and columns:
  - CS_SURVEY: Text (Year of Survey)
  - SQUARE: Text (1km square sampling site code)
  - SITE_ID: Number (Stream site identifier within the 1km square)
  - SAMPLE_DATE: Date (Date sample taken)
  - DETERMINAND_NAME: Text (Chemical determinand)
  - DETERMINAND_UNITS: Text (Units of determinand)
  - VALUE: Number (Value of chemical determinand)
  - LC07: Text (Land class 2007)
  - LC07_NUM: Number (Numeric land class code)
  - EZ_DESC_07: Text (Environmental zone)
  - COUNTY07: Text (County or council area)
  - COUNTRY: Text (England, Scotland, or Wales)

## Variables and meanings
- CS_SURVEY: Year of survey (e.g., 2007)
- SQUARE: 1km square sampling site code
- SITE_ID: Stream site identifier within the square
- SAMPLE_DATE: Date the sample was collected
- DETERMINAND_NAME: Chemical determinand (e.g., SRP, TON, alkalinity, conductivity, pH)
- DETERMINAND_UNITS: Units for the determinand
- VALUE: Measured value of the determinand
- LC07 / LC07_NUM: Land classification (text and numeric code) as per ITE Land Classification of Great Britain 2007
- EZ_DESC_07: Environmental zone description
- COUNTY07: County or council area
- COUNTRY: England, Scotland, or Wales

## Measurement details
- Conductivity and pH measured in the field.
- SRP, TON, and alkalinity measured from 50 ml filtered samples.

## Spatial and reporting context
- 1km square coding (SQUARE) links chemistry data to spatial units for mapping.
- Land classification (LC07) and environmental zone (EZ_DESC_07) provide geographic/ecosystem context.

## Data provenance and references
- Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data rights apply.
- Supporting documents:
  - Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010 Countryside Survey: Headwater Streams Report from 2007.
- Land classification reference: ITE Land Classification of Great Britain 2007 (LC07).

## Usage and acknowledgement
- All CS data usage must include acknowledgements:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.