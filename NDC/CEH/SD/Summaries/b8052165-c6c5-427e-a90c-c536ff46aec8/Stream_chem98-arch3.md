# Headwater stream water chemistry data 1998 [Countryside Survey] Data Table Descriptions

- Overview
  - Data table STREAM_CHEMISTRY_98.csv contains freshwater stream water chemistry measurements from headwater sites sampled in 1998 as part of Countryside Survey.
  - Measured parameters include conductivity and pH (field), soluble reactive phosphorus (SRP), and alkalinity (50 ml filtered).
  - Context and supporting documents are linked to Countryside Survey 1998 and related freshwater studies and manuals.

- Data Content and Structure
  - Core dataset describes chemical determinands measured at headwater stream sites.
  - Fields include year, location, sampling details, determinand name and units, and measured values.
  - Location and classification fields provided to enable spatial and environmental context:
    - LC07 (land class 2007) and LC07_NUM
    - EZ_DESC_07 (environmental zone)
    - COUNTY07 (county)
    - COUNTRY (England, Scotland, or Wales)

- Key Fields (selected)
  - YEAR: Year of survey (CS +Yr)
  - SQUARE: 1 km square sampling site code
  - SITE_ID: Site identifier within the square
  - SAMPLE_DATE: Date sample taken
  - SAMPLE_TYPE: Type of sample
  - DETERMINAND_NAME: Name of chemical determinand
  - DETERMINAND_UNITS: Units of the determinand
  - VALUE: Measured value
  - LC07, LC07_NUM: Land class (2007)
  - EZ_DESC_07: Environmental zone
  - COUNTY07: County
  - COUNTRY: Country designation

- Data Usage, Quality, and Governance
  - Data handling emphasizes metadata quality and traceability; notes that metadata may require augmentation for usability.
  - Acknowledgement and copyright obligations apply to all copies and presentations:
    - “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
    - “Countryside Survey ©” with all rights reserved
  - Data sharing practices and governance are important considerations for data usability and openness.

- Related Documentation and References
  - Countryside Survey 2000 Module 2: Freshwater Studies (field handbook and reports)
  - Countryside Survey: Headwater Streams Report from 2007
  - ITE Land Classification of Great Britain 2007 (for LC07)
  - Freshwater Manual and other Countryside Survey technical reports

- Relevance for Monitoring Frameworks
  - Provides a structured example of environmental health monitoring data, including field measurements, temporal and spatial identifiers, land use/classification context, and governance/acknowledgement requirements.
  - Highlights common barriers and considerations for authors of monitoring frameworks: data availability/quality, metadata completeness, data sharing constraints, and the necessity of clear data governance and provenance.