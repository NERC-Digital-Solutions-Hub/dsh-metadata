# Glastir Monitoring and Evaluation Programme (GMEP) – Survey Design and Data Collection

- Wales-wide AES funding since the early 1990s supported schemes like Glastir, with a monitoring programme (GMEP) established in 2013 to evaluate environmental impacts, biodiversity trends, and woody feature management.
- GMEP aims to contribute to reversing the decline of Wales’ native biodiversity and meet CBD 2020 obligations.

## Survey design and scope

- Uses a 4-year rolling cycle (2013–2016) to maximise site coverage while enabling year-to-year monitoring of spatial and temporal changes.
- Two components:
  - Wider Wales Component: baseline estimation and national trends for Glastir.
  - Targeted Component: links to Glastir priority areas.
- Unified sampling unit: 1 km square grid across Wales; 300 squares sampled over the cycle (half Wider Wales, half targeted).
- Sampling frames and stratification:
  - Wider Wales squares randomly sampled within strata defined by the ITE Land Classification of Great Britain (Bunce et al., 2007) to minimize within-stratum heterogeneity and maximize between-strata variation.
  - Exclusions: squares with >75% urban land or >90% sea (based on LCM2007 and mean high tide data).
- Methodological alignment with Countryside Survey of Great Britain to enable future data integration.

## Data collection design and variables

- Within each 1 km square, landscape features are mapped using predetermined coded options during a single snapshot visit.
- Features recorded:
  - Linear features (less than 5 m wide): boundaries, hedges (woody), lines of trees, walls, fences, streams, etc.
  - Measurements: length, condition, and related attributes; minimum length 20 m with gaps up to 20 m.
  - Woody linear features captured with a Habitats-focused classification (per Maskell et al., 2016) after consultation with UK BAP Hedgerow Steering Group.
- Data capture:
  - Electronic data capture using CS Surveyor (CEH) and Esri GIS.
  - Digital capture reduces post-survey digitising errors and ensures all mapped components are visited.
  - QA uses a field mapping handbooks framework for consistency.
- Datasets generated (examples):
  - GMEP_LANDSCAPE_LINEAR_FEATURES_2013_16.csv: landscape linear feature identifiers, square codes, location, dimensions, habitat/theme, and feature attributes.
  - GMEP_LANDSCAPE_LINEAR_FEATURE_SP_2013_16.csv: species-level data for woody linear features, including vegetation type, species, and proportional cover.
- Coordinate and spatial context:
  - Includes 10 km resolution coordinates (EASTING_10km, NORTHING_10km) for square location context.
  - Square codes (SQ_ID) link records to the 1 km survey sites.

## Data quality assurance and procedures

- Survey teams are experienced botanical surveyors; mandatory training ensures consistency with the GMEP Field Mapping Handbooks.
- Electronic data capture (CS Surveyor) minimizes illegible data and supports immediate data checks.
- Data are checked quickly after collection; QA includes a second team (QC assessors) repeating surveys in all or part of a square to identify issues and feed back to field teams.
- Documentation and methodology are supported by comprehensive Field Mapping Handbooks (2016 versions) and related references.

## Outputs and dissemination

- Methodology designed to enable integration of survey data across scales and with national frameworks.
- Public references and documentation:
  - Field Mapping Handbooks (habitat attributes and digital mapping).
  - Related annual and final reports to Welsh Government, including executive summaries and project outlines.
  - Glastir Monitoring & Evaluation Programme website offering overview, methodologies, and results.
- Data management emphasis:
  - Datasets are prepared with metadata and structured to be discoverable and reusable (consistent with QA and project governance).

## Appendices: roles, responsibilities, and field team

- Roles include GMEP Lead Scientist, sampling design/statistical experts, vegetation experts, database management, GIS expertise, project management, and field team managers.
- Field survey teams comprise named individuals across data collection and field operations, indicating a structured team-based workflow and accountability.

## Context and references

- Links to relevant methodological and classificatory sources:
  - ITE Land Classification of Great Britain 2007
  - GMEP Field Mapping Handbooks (habitat attributes and digital mapping)
  - Emmett et al. project reports (annual and final), CEH/CEH-derived outputs
  - Glastir Monitoring & Evaluation Programme website (gmep.wales)
- Purposeful alignment with GB-wide biodiversity classifications and existing survey methodologies to facilitate future data integration and cross-border analyses.