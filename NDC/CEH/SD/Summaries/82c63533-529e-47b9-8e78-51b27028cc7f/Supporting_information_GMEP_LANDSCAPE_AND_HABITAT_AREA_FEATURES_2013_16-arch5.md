# Glastir Monitoring and Evaluation Programme

## Overview
- Welsh Government programme (GMEP) monitoring the Glastir agri-environment schemes to measure biodiversity, woodland creation/management, and progress toward reversing native biodiversity decline.
- Data support indicators for biodiversity targets and Well-Being of Future Generations Act 2015 (Area of Healthy Ecosystems).

## Survey Design and Sampling
- 4-year rolling survey cycle (2013–2016 first cycle) to maximize site coverage while detecting year-to-year changes cost-effectively.
- Two components: Wider Wales (baseline/national trends) and Targeted (Glastir priority areas); both use a common 1 km square unit.
- 300 1 km squares sampled; half randomly within strata defined by the ITE Land Classification of GB; other half targeted at Glastir priorities.
- Exclusion criteria: squares with >75% urban land or >90% sea excluded.
- Sampling framework aligns with Countryside Survey GB methodology for future integration.

## Data Collection and Dataset Structure
- Areal, line, and point features mapped on base maps using predetermined codes; data captured electronically with CS Surveyor (Esri GIS integration).
- Attributes collected per feature include Biodiversity Broad/Priority Habitat, land use/management, vegetation species, and other descriptors.
- Data files:
  - LANDSCAPE_AND_HABITAT_AREA_FEATURE_2013_16.csv: polygon areas within 300 squares; includes SQ_ID, POLY_ID, BHCODE, AREA, coordinates, YEAR, LC, etc.
  - LANDSCAPE_AREA_FEATURE_ATT_2013_16.csv: polygon attributes and detailed descriptors (THEME, HABITAT_NAME, MOSAIC_PC_AREA, etc.), including species and vegetation details where relevant.
- Species nomenclature follows Stace (1997); vegetation data include cover, sward characteristics, tussock presence, DBH, and structure descriptors.
- Spatial and thematic data tied to 1 km squares with OSGB coordinates (EASTING/NORTHING at 10 km) and Land Classification codes.

## Quality Assurance and Data Quality
- Surveys conducted by trained botanical survey teams; intensive pre-survey training to ensure consistency.
- Electronic data capture reduces transcription errors; mandatory fields and prompts improve data completeness.
- Timely data transfer to offices enables prompt QA checks; field staff and managers communicate to resolve issues.
- QC exercise: a second survey team re-measures all or part of a square to identify and address recording issues.
- Supporting documentation includes GMEP Field Mapping Handbooks (habitat attributes), and extensive references and methodological notes.

## Data Documentation and Access
- Documentation and methodologies available through the Glastir Monitoring & Evaluation Programme website (gmep.wales) and referenced field handbooks.
- Data definitions and codes drawn from established sources (Jackson 2000; Maddock 2008; Stace 1997).
- Data exclusions and structure noted (e.g., refused access areas removed from datasets).
- Appendix provides roles, responsibilities, and lists of field survey teams and management staff.

## Data Management Roles and Teams
- Roles include database management, field team management, lead scientist, field expertise, sampling design, statistics, habitat and vegetation specialists, GIS, and project management.
- Field survey teams comprised of numerous named members supporting data collection, mapping, and QA activities.

## Relevance to Biodiversity Monitoring and Policy
- Provides an independent estimate of change in semi-natural habitat extent, informing indicators for biodiversity progress.
- Supports reporting aligned with the Well-Being of Future Generations Act by quantifying the Area of Healthy Ecosystems in Wales.
- Facilitates integration with GB-level surveys for broader analyses and future data synthesis.

## Data Stewardship Considerations and Challenges
- Data volume at national scale with standardized 1 km units across a multi-year cycle; requires robust metadata, versioning, and provenance tracking.
- Integration potential with Countryside Survey GB data; harmonization of classifications and attributes essential for interoperability.
- Ensuring timely data sharing from field teams and adherence to metadata standards, including spatial references and habitat coding.
- Handling complex, multi-attribute datasets (habitats, land use, vegetation, sward metrics, and species data) and maintaining consistency across years.
- Operational challenges such as data access limitations (refused areas) and the need for ongoing data quality control.