# Glastir Monitoring and Evaluation Programme (GMEP)

## Overview and aims
- Wales-based monitoring programme for agri-environment schemes (AES) since the early 1990s, with the Glastir scheme and its monitoring through GMEP starting in 2013.
- Collects biodiversity data and information on woodland creation/management to support evidence for reversing native biodiversity decline and meeting biodiversity obligations.
- Provides independent estimates of semi-natural habitat change and supports the Well-Being of Future Generations Act indicator for Area of Healthy Ecosystems in Wales.
- Uses a 4-year rolling survey cycle (first cycle: 2013–2016) to maximize site coverage and detect year-on-year trends cost-effectively.

## Data strategy and system design
- Two integrated components:
  - Wider Wales Component: baseline estimation, national trends, and national reporting for Glastir.
  - Targeted Component: links directly to Glastir priority areas.
- Common spatial unit: 1 km square to enable cross-scale integration and future analysis with other surveys.
- Sampling plan: 300 1 km squares over four years; half randomly sampled within strata (based on the ITE Land Classification of Great Britain) to maximize environmental heterogeneity and provide robust national indicators; half targeted at Glastir priority areas.
- Exclusions: squares with more than 75% urban land or more than 90% sea are removed.
- Methodological alignment with the Countryside Survey of Great Britain to enable integration and future joint analyses.
- Outputs focus on broad habitat extent and change in semi-natural land as indicators for biodiversity and ecosystem health.

## Data collection methods and standards
- Within each 1 km square, areal, line, and point features are mapped on base maps using predetermined coded options per GMEP Field Mapping Handbooks.
- Data capture method: electronic data collection with CS Surveyor software (CEH/Esri) to minimize post-collection digitising errors.
- Fields collected include biodiversity broad/priority habitat codes and descriptions, land use and management, dominant vegetation, woodland structure, sward characteristics, road verge widths, and other land-use descriptors.
- Detailed data schemas:
  - LANDSCAPE_AND_HABITAT_AREA_FEATURE_2013_16.csv: core polygon areas (square, polygon IDs, habitat codes, areas, coordinates, year, land class).
  - LANDSCAPE_AND_HABITAT_AREA_FEATURE_ATT_2013_16.csv: additional attributes per polygon (themes, habitat names, mosaic attributes, vegetation specifics, DBH, sward metrics, road verge attributes, year, etc.).
- Species nomenclature references and standard field terminology (e.g., Stace 1997; Jackson 2000; Maddock 2008) are used for consistency.

## Data quality assurance and governance
- Surveys conducted by experienced botanical teams with extensive pre-survey training to ensure consistency with field handbooks.
- Use of electronic data capture reduces illegible records and enables immediate data checks; mandatory fields and prompts help maintain data integrity.
- Field-level quality control (QC): a second team re-surveys all or part of a square; results fed back to improve recording practices.
- Documentation and references provided for methodologies, sampling design, and QA processes; ongoing governance through GMEP leadership and field coordinators.

## Data products, metadata, and accessibility
- Outputs include detailed 2013–2016 data for 300 survey squares, with structured attribute tables for landscape and habitat areas and their characteristics.
- Metadata documentation covers variable definitions, habitat codes, coordinates (EASTING/NORTHING), year, and sampling framework classifications.
- Public-facing references include field handbooks, methodology reports, and the GMEP website (gmep.wales) to support transparency and reuse.
- Methodological compatibility with the GB Countryside Survey enables data integration and future joint analyses.

## Appendix: roles and teams
- Roles include GMEP Lead Scientist, Habitats Work Package Leader, Field Team Managers, Database Management, GIS expertise, and statistical specialists.
- Field survey teams comprise a wide list of named personnel supporting data collection and field operations.