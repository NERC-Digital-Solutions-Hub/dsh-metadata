# Headwater stream water chemistry data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes the headwater stream water chemistry data collected in 2007 as part of the Countryside Survey.
- Chemical analyses include conductivity and pH (field measurements); soluble reactive phosphorus (SRP), total oxidisable nitrogen (TON), and alkalinity (from 50 ml filtered samples).
- Data table provides site-level identifiers, timing, chemical determinands, units, and classification metadata.

## Data Content and Structure
- Data Table: STREAM_CHEMISTRY_2007.csv
- Key fields and descriptions:
  - CS_SURVEY: Year of Survey
  - SQUARE: 1 km square sampling site code
  - SITE_ID: Stream site identifier (within square)
  - SAMPLE_DATE: Date sample taken
  - DETERMINAND_NAME: Chemical determinand (analyte)
  - DETERMINAND_UNITS: Units of the determinand
  - VALUE: Measured value
  - LC07: Land class 2007 (text)
  - LC07_NUM: Land class 2007 (numeric code)
  - EZ_DESC_07: Environmental zone
  - COUNTY07: County (England & Wales) or Council (Scotland)
  - COUNTRY: England, Scotland, or Wales
- Data types explicitly noted (e.g., CS_SURVEY and SQUARE as text; SITE_ID as numeric; SAMPLE_DATE as date; VALUE as numeric).

## Data Provenance and References
- Data originate from Countryside Survey (Headwater Streams, 2007).
- Related materials:
  - Murphy, J.; Weatherby, A. 2008. Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010. Countryside Survey: Headwater Streams Report from 2007.
  - Land Classification: Bunce et al. 2007 (ITE Land Classification of Great Britain 2007).
  - Environmental zone reference: link provided in documentation.
- Acknowledgement requirements link to data usage (see Licensing).

## Licensing and Acknowledgement
- All use of Countryside Survey data must include acknowledgement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Acknowledgement and copyright apply to copies, publications, presentations, and derivatives.

## Governance and Stewardship Considerations for Data Leaders
- Data are supplied with metadata describing variables, units, and provenance; emphasize discoverability and consistent metadata standards.
- Classification metadata (LC07, EZ_DESC_07, COUNTY07, COUNTRY) supports cross-dataset analyses (e.g., linking chemistry with land classification and environmental zones).
- Ensure proper attribution in all outputs; manage licensing compliance across platforms and partners.
- Be aware of historical scope (2007 data) and provenance when integrating with newer datasets or time-series analyses.

## Related Documentation and Supporting Materials
- Freshwater Manual (2008) and Headwater Streams Report (2010) for methodological context and interpretation.
- Land classification and environmental zone references to support data integration and analysis.
- Primary data excluded in this excerpt are provided in accompanying documents and the CS data portal.

## Practical Applications
- Supports assessment of headwater stream chemistry and its relation to land use and environmental zones.
- Useful for researchers, policymakers, and partner networks requiring standardized, attributed chemical determinand data with geographic context.