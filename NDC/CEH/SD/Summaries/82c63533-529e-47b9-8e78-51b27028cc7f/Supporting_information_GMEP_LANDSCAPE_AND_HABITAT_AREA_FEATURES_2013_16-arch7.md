# GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURES_2013_16.csv

- Overview
  - Welsh Government Glastir Monitoring and Evaluation Programme (GMEP) monitors agri-environment scheme (AES) effects on biodiversity, woodland creation/management, and landscape features to support evidence for biodiversity targets and Well-Being of Future Generations indicators.
  - Uses a 4-year rolling survey (2013–2016) with two components: Wider Wales (baseline/national trends) and Targeted (Glastir priority areas), employing a common spatial unit of 1 km square.

- Sampling design and spatial unit
  - 300 x 1 km squares sampled over the four-year cycle.
  - Half randomly selected from within strata defined by the ITE Land Classification of Great Britain; half targeted at Glastir priority areas.
  - Exclusions: squares with more than 75% urban land or more than 90% sea.
  - Sampling framework aligns with Countryside Survey of GB to enable future data integration.

- Data collection and mapping
  - Within each 1 km square, areal, line, and point features mapped onto base maps using predetermined codes.
  - Field methods follow GMEP Field Mapping Handbooks; data captured electronically with CS Surveyor (CEH/Esri UK).
  - Attributes recorded include Biodiversity Broad/Priority Habitats, land use/management, dominant vegetation, and a range of land-use descriptors (e.g., road verge widths, tree DBH, woodland structure, sward descriptions).

- Data files and key fields
  - GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURES_2013_16.csv
    - Core polygon-level data for areas of Broad/Priority Habitats across 300 squares.
    - Important fields: SQ_ID (1 km square code), POLY_ID, POLY_GUID (polygon unique ID), BHCODE (habitat code), BHDESC (habitat description), AREA (m2), EASTING_10km, NORTHING_10km, YEAR, LC (land classification).
  - GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURE_ATT_2013_16.csv
    - Additional attributes for areas; links via POLY_GUID.
    - Key fields: THEME, HABITAT_NAME, MOSAIC_PC_AREA, PRIMARY_QUALIFIER, plus vegetation-related attributes (SPECIES, SPECIES_COVER, SWARD_COVER, SWARD_HEIGHT, etc.), YEAR, LC.
  - Species and vegetation nomenclature follow established references (e.g., Stace 1997).

- Quality Assurance and data integrity
  - Surveys conducted by experienced botanical surveyors; rigorous training and standardization per field handbooks.
  - Electronic data capture reduces transcription errors; mandatory fields and prompts to ensure complete recording.
  - Data transferred promptly to the office for timely checks; QC exercises involve a second survey team to validate or identify issues, with feedback loops to field teams.

- Data standards, integration, and confidentiality
  - Uses a common 1 km spatial unit and OSGB 1936 coordinates; alignment with GB Countryside Survey methodologies to enable future integration.
  - Figure distributions (e.g., 10 km plotting) protect data confidentiality.

- Applications and relevance
  - Enables estimation of extent for Broad/Priority Habitats and semi-natural habitat change.
  - Supports monitoring progress toward reversing native biodiversity decline and contributes to indicators under the Well-Being of Future Generations Act (Healthy Ecosystems in Wales).

- References and documentation
  - Field handbooks (2016) and related methodology documents.
  - GMEP website (gmep.wales) for additional resources, methodologies, and results.
  - Supporting publications and datasets detailing sampling design, land classification, and habitat descriptions.

- Appendix: roles and teams (highlights)
  - Roles include GMEP Lead Scientist, Habitats Work Package Leader, Field Team Managers, GIS/Database Management, Vegetation specialists, and Project Manager.
  - Field survey teams comprise multiple named members across Wales, with designated field coordination and data management responsibilities.