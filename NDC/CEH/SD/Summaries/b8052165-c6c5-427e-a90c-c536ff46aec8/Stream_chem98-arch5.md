# Headwater stream water chemistry data 1998 [Countryside Survey] Data Table Descriptions

- Overview
  - Describes the Freshwater Stream - Water chemistry data from headwater sites sampled in 1998 as part of the Countryside Survey.
  - Measurements include field data (conductivity, pH) and laboratory-derived values (soluble reactive phosphorus SRP, alkalinity) from 50 mL filtered samples.
  - Data are organized to support spatially explicit analyses, with 1 km square site coding and site-level identifiers.

- Data content and structure
  - Table: STREAM_CHEMISTRY_98.csv
  - Key fields:
    - YEAR: Text; year of survey
    - SQUARE: Text; 1 km square sampling site code
    - SITE_ID: Number; site identifier within the 1 km square
    - SAMPLE_DATE: Date; date sample taken
    - SAMPLE_TYPE: Text; type of sample
    - DETERMINAND_NAME: Text; chemical determinand
    - DETERMINAND_UNITS: Text; units of determinand
    - VALUE: Number; measured value of determinand
    - LC07: Text; Land class 2007 name/code reference
    - LC07_NUM: Number; numeric land class code (2007)
    - EZ_DESC_07: Text; Environmental zone description
    - COUNTY07: Text; county or equivalent
    - COUNTRY: Text; England, Scotland, or Wales
  - Additional context:
    - Conductivity and pH are field measurements; SRP and alkalinity are from 50 mL filtered samples.
    - Data use is subject to the specified attribution and copyright.

- Provenance and governance
  - Data owned by NERC - Centre for Ecology & Hydrology (CEH); Countryside Survey copyright and database rights apply.
  - Associated with Countryside Survey modules and reports (e.g., Field handbook, Freshwater Manual, Headwater Streams Report from 2007).
  - Supporting documents provide broader methodological context and are linked for provenance.

- Access, use, and attribution
  - All use of Countryside Survey data must be acknowledged.
  - Acknowledgement wording to be used on copies, publications, and presentations:
    - “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
    - “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Data are part of CEH/NERC data holdings; guidance and citations anchor usage.

- Quality and metadata considerations
  - Metadata includes measurement methods, units, and affixed 2007 land classification (LC07) and environmental zone descriptors.
  - Data model supports traceability to source documents and related Countryside Survey materials.
  - Note potential stewardship concerns typical for historical datasets: older formats, need for harmonization with modern schemes, and reliance on supporting documentation for full context.

- Related resources and references
  - Field handbook and freshwater manuals from Countryside Survey (modules and reports listed as supporting documents).
  - Land classification reference: ITE Land Classification of Great Britain 2007 (LC07), with numeric code LC07_NUM.
  - Environmental zone description (EZ_DESC_07) and location metadata (COUNTY07, COUNTRY) linked to country-specific classifications.

- Practical stewardship implications
  - Ensure metadata alignment with current data governance practices (accurate provenance, licensing, and attribution in all distributions).
  - Maintain links to supporting documents and classification schemes to support data reuse and discoverability.
  - Prepare for potential data updates or reformatting to improve interoperability while preserving original values.