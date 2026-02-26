# Headwater stream macrophyte data 2007 [Countryside Survey] Dataset description

- Source and purpose
  - Countryside Survey data for headwater streams (macrophytes) from 2007.
  - Uses the Mean Trophic Rank (MTR) protocol to assess presence and extent of macrophytes within a 100 m stream reach.
  - More extensive plant species checklist used than required by standard MTR; data collected with tablet-based custom software.
  - Data supported by related Countryside Survey reports and manuals.

- Data and metadata at a glance
  - Version: 1 (dated 19/10/2016)
  - Data ownership: Countryside Survey © NERC - Centre for Ecology & Hydrology
  - Related documentation: Murphy & Weatherby (2008) Freshwater Manual; Dunbar et al. (2010) Headwater Streams Report; Holmes et al. (1999) Mean Trophic Rank manual
  - Access and use: Acknowledgement required on all copies, publications, and presentations

- Data collection method
  - Field survey of headwater streams using the standard MTR protocol.
  - Observations include occurrence and abundance of macrophytes within a 100 m reach.
  - Data recorded on tablet computers using custom software.

- Dataset structure and content
  - Table: STREAM_MACROPHYTES_07.csv
  - Key fields:
    - SQUARE: 1 km square sampling site code (Text)
    - YEAR: Year of Survey (Text)
    - SITE_ID: Site identifier (Number)
    - SURVEY_DATE: Date of survey (Date)
    - PLANT_NAME: Scientific name of plant (Text)
    - PROPORTION: Proportion (%) of the 100 m reach covered by the plant (Text)
    - LC07: Land class 2007 (Text)
    - LC07_NUM: Land class 2007 (numeric code)
    - EZ_DESC_07: Environmental zone description (Text)
    - COUNTY07: County (Eng/Wal) or Council (Sco) (Text)
    - COUNTRY: England, Scotland, or Wales (Text)
  - Data types per field are provided in the dataset specification; ranges and codes follow the ITE Land Classification of Great Britain 2007 for LC07.

- Scope and scale
  - Sampling is conducted within Countryside Survey 2007 headwater streams.
  - Each 1 km square contains site-level observations; proportion data reflect the 100 m survey stretch.

- Related classifications and references
  - LC07 and LC07_NUM correspond to the ITE Land Classification of Great Britain 2007.
  - EZ_DESC_07 provides environmental zone descriptors (see associated CEH catalog/document for details).

- Usage notes and rights
  - All uses require acknowledgement of Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Data is rights-reserved; proper citation and licensing needed for redistribution or publication.

- Practical considerations for analysts
  - The dataset combines presence/abundance data with land classification and environmental zone descriptors, enabling analyses of macrophyte distributions across land classes and environmental zones at headwater scales.
  - The expanded species checklist allows richer ecological analyses beyond the core MTR requirements.
  - Integrating with other Countryside Survey datasets (e.g., hydrology, land cover) may require careful standardization due to scale and naming conventions.