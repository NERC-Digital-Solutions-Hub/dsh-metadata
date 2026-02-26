# Headwater stream water chemistry data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes the STREAM_CHEMISTRY_2007.csv data table for headwater streams, capturing water chemistry analysed in 2007.
- Part of the Countryside Survey data collection; references the Freshwater Manual (Murphy & Weatherby 2008) and Headwater Streams Report (2010).
- Data are intended to be used with appropriate acknowledgement and within the governance and metadata context provided by CEH/NERC.

## Data Scope and Measurements
- Measured elements (at each headwater site):
  - Conductivity and pH: field measurements.
  - Soluble reactive phosphorus (SRP), total oxidisable nitrogen (TON), and alkalinity: measured from 50 ml filtered samples.
- Data table records are linked to site and survey context (year, location, and sampling details).

## Data Structure and Variables
- STREAM_CHEMISTRY_2007.csv: main data table for chemical determinands and values.
- Key fields:
  - CS_SURVEY: Year of Survey (text)
  - SQUARE: 1 km square sampling site code (text)
  - SITE_ID: Stream site identifier (numeric)
  - SAMPLE_DATE: Date sample taken (date)
  - DETERMINAND_NAME: Chemical determinand (text)
  - DETERMINAND_UNITS: Units of chemical determinand (text)
  - VALUE: Value of chemical determinand (numeric)
  - LC07: Land class 2007 (text)
  - LC07_NUM: Land class 2007 (numeric code) (numeric)
  - EZ_DESC_07: Environmental zone (text)
  - COUNTY07: County (Eng & Wal) or Council (Sco) (text)
  - COUNTRY: England, Scotland, or Wales (text)

- Data types span Text, Date, and Number as described above.

## Standards, Documentation, and Related Resources
- Related guidance and context:
  - Countryside Survey Freshwater Manual (Murphy & Weatherby, 2008)
  - Countryside Survey: Headwater Streams Report from 2007 (Dunbar et al., 2010)
- LC07 land classification reference: ITE Land Classification of Great Britain 2007 (CEH/NEC). DOI provided in documentation.
- Environmental zone descriptor reference linked in EZ_DESC_07.

## Data Use, Acknowledgement, and Rights
- All uses of CS data must include acknowledgement:
  - “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
  - “Countryside Survey ©” and note of Data rights restrictions (All rights reserved).
- Acknowledgement and copyright notice must be present in all copies, publications, reports, and presentations.

## Data Stewardship Considerations
- Metadata completeness: ensure year, location, site identifiers, and determinand units are recorded consistently for interoperability.
- Data quality: maintain clarity on field vs laboratory measurements (e.g., SRP, TON, alkalinity from filtered samples).
- Versioning and provenance: align with related manuals and reports; track connection between STREAM_CHEMISTRY_2007.csv and broader Countryside Survey datasets.
- Access and sharing: preserve the requirement for proper acknowledgement when sharing or publishing derived datasets.
- Interoperability: maintain consistent naming, codes (LC07, LC07_NUM), and geographic descriptors to facilitate cross-dataset analyses.

## Related Documentation and References
- Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual. NERC/CEH.
- Dunbar, M.; Murphy, J.; Clarke, R.; Baker, R.; Davies, C.; Scarlett, P. 2010. Countryside Survey: Headwater Streams Report from 2007.
- ITE Land Classification of Great Britain 2007 (linked within LC07 and LC07_NUM).

## Publisher and Rights
- Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- All rights reserved; data sharing should preserve the stated acknowledgments.