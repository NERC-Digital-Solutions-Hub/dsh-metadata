# Glastir Monitoring & Evaluation Programme (GMEP)

- Welsh Government AES monitoring initiative (Glastir) and its biodiversity data collection to track progress toward reversing native biodiversity decline and obligations under biodiversity conventions.
- Aims to provide independent estimates of semi-natural habitat change and contribute to the Well-Being of Future Generations indicators (Area of Healthy Ecosystems in Wales).

## Survey design and scope

- Four-year rolling survey cycle (2013–2016 first cycle) to maximize site coverage and detect temporal and spatial trends cost-effectively.
- Two components:
  - Wider Wales Component: baseline estimation, national trends, and national reporting of Glastir.
  - Targeted Component: links to Glastir priority areas.
- Common spatial unit: 1 km grid squares; total of 300 squares sampled over the cycle.
- Sampling methodology aligned with the Countryside Survey of Great Britain to enable future integration.
- Exclusions: squares with >75% urban land or >90% sea excluded.

## Data collection methods

- In each 1 km square, areal, line, and point features mapped on base maps using predetermined codes.
- Electronic data capture with CS Surveyor (GIS-enabled) to reduce post-survey digitising and ensure data completeness.
- Attributes collected include:
  - Biodiversity Broad/Priority Habitats (BAP classifications)
  - Land use and management (e.g., crops, grazing, recreation, timber)
  - Dominant vegetation species and related descriptors (e.g., road verge widths, tree DBH, woodland structure)
- Field Mapping Handbooks provide detailed methodology (Habitat attributes; mapping procedures).

## Data structure and files

- Primary data cover areas of Broad and Priority Habitats across 300 1 km squares (2013–2016).
- Key data files:
  - GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURES_2013_16.csv: includes square ID, polygon IDs, habitat codes and descriptions, area (m²), coordinates, year, and Land Classification (LC).
  - GMEP_LANDSCAPE_AND_HABITAT_AREA_FEATURE_ATT_2013_16.csv: additional attributes for polygon areas, such as theme, habitat name, mosaic area details, vegetation specifics, and year.
- Notable fields: SQ_ID (1 km square code), POLY_ID/POLY_GUID (polygon identifiers), BHCODE/BHDESC (habitat codes and descriptions), AREA (polygon area), YEAR, LC (land classification).
- Species nomenclature adheres to Stace (1997).
- Supplemental vegetation data include species cover, sward metrics, tussockiness, diameter at breast height (DBH), structure use, and various physiographic and road/ verge attributes.

## Quality Assurance and data quality

- Surveys conducted by experienced botanical teams; extensive pre-survey training to ensure consistency with field handbooks.
- Electronic data capture reduces illegible records; mandatory fields and prompts improve data completeness.
- Post-survey data transfer to offices enables prompt data checks.
- Quality Control (QC) process involves a second team re-surveying all or part of a square; feedback from QC informs field team improvements.

## Access, references, and publications

- References to methodological standards and background reports (e.g., ITE Land Classification of Great Britain 2007, field handbooks by Maskell et al., 2016).
- CEH/UK sources and links to Glastir Monitoring & Evaluation Programme website (gmep.wales) for documentation, methodologies, and results.
- Cited field handbooks and related biodiversity classifications (Jackson 2000; Maddock 2008; Stace 1997).

## Roles, tasks, and teams

- Appendix 1 lists core project roles (e.g., GMEP Lead Scientist, Habitats work package leader, database management, GIS expertise, field coordinators, sampling design, statistics).
- Field survey teams comprise a large roster of surveyors and field staff, with appointed field team managers and coordinators.
- Indicates structured governance and responsibilities to maintain data quality and consistency across the 2013–2016 survey cycle.