# Headwater stream water chemistry data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Dataset from Countryside Survey 1998 documenting freshwater headwater stream water chemistry.
- Measurements include field conductivity and pH; soluble reactive phosphorus (SRP) and alkalinity from 50 ml filtered samples.

## Data Table and Key Fields
- Table: STREAM_CHEMISTRY_98.csv
- Core fields and descriptions:
  - YEAR: Year of survey (text)
  - SQUARE: 1 km square sampling site code (text)
  - SITE_ID: Site identifier within the 1 km square (numeric)
  - SAMPLE_DATE: Date sample taken (date)
  - SAMPLE_TYPE: Sample type (text)
  - DETERMINAND_NAME: Chemical determinand (text)
  - DETERMINAND_UNITS: Units of the determinand (text)
  - VALUE: Value of chemical determinand (numeric)
  - LC07: Land class 2007 (text)
  - LC07_NUM: Land class 2007 (numeric code)
  - EZ_DESC_07: Environmental zone (text)
  - COUNTY07: County/region (text)
  - COUNTRY: England, Scotland, or Wales (text)
- Additional contextual fields provide location, date, and metadata for robust analysis and cross-referencing with land classifications and environmental zones.

## Data provenance and references
- Data linked to Countryside Survey modules and supporting manuals:
  - Field handbook and freshwater studies from Countryside Survey 2000/1998 editions
  - Freshwater Manual (Murphy & Weatherby, 2008)
  - Headwater Streams Report (2007)
  - ITE Land Classification (2007) referenced for LC07
- Supporting documents and project reports cited for methodological context and data lineage.

## Usage rights and attribution
- All Countryside Survey data must be acknowledged.
- Acknowledgement statement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © database rights © CEH. All rights reserved.
- Attribution and copyright considerations must accompany copies, publications, presentations, and derived products.

## Relevance for Data Leaders
- Demonstrates structured data governance:
  - Clear schema with field-level definitions and units.
  - Links to standardized classifications (LC07, environmental zones) and geographic identifiers (SQUARE, COUNTY07, COUNTRY) to enable interoperability.
  - Explicit data provenance and supporting references for traceability.
- Supports discovery and re-use across networks by providing:
  - Metadata-rich descriptions (measurement types, sampling details, dates).
  - Fixed data types and consistent naming conventions.
- Helps address common leadership challenges:
  - Understanding data scope and availability across landscapes (headwater streams, 1998 snapshot).
  - Assessing data quality, granularity, and compatibility with other datasets (land class, environmental zones).
  - Establishing clear attribution, discoverability, and licensing terms for data products. 

## Considerations for action
- Ensure discoverability of STREAM_CHEMISTRY_98.csv within broader data catalogs and links to related CS datasets and reports.
- Maintain and communicate data standards (naming, units, determinand definitions) to support integration with other data assets.
- Plan for coordination with external users through clear citations, usage guidance, and acknowledgement requirements.