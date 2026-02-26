# Glastir Monitoring & Evaluation Programme (GMEP)

- Welsh Government monitoring programme (GMEP) established to track Glastir scheme effects on biodiversity and woody landscape features, supporting evidence for CBD 2020 obligations.
- Data focus: landscape linear features, woody features, habitat attributes, and biodiversity indicators across Wales.
- Data products enable national baseline estimation, trends, and targeted analysis for Glastir priority areas; designed for integration with cross-border GB data in the future.

## Survey Design and Sampling

- 4-year rolling survey cycle (first cycle 2013–2016) to maximize site coverage while monitoring year-on-year changes.
- Two components:
  - Wider Wales: baseline estimation and national reporting.
  - Targeted Component: links specifically to Glastir priority areas.
- Common spatial unit: 1 km square for all sampling and analysis.
- Sampling scheme: 300 one-km squares across Wales.
  - Half randomly sampled within strata defined by the ITE Land Classification (Bunce et al., 2007) to maximize environmental heterogeneity between strata and minimize within-stratum variability.
  - Half targeted to Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea (per LCM2007 and census data).
- Methodological alignment: follows Countryside Survey of Great Britain procedures to enable future data integration.

## Data Collection Methods

- Within each 1 km survey square, map linear (and areal/point) features onto base maps using predefined coded options.
- Field tools: electronic data capture (CS Surveyor) and GIS (Esri UK) for real-time mapping and data validation.
- Feature types:
  - Linear features: often <5 m wide; include hedges (woody), unmanaged lines of trees, walls, fences, streams, etc.
  - Recording: feature length, condition, and other descriptive attributes.
  - Woody linear features: hedges, remnant hedges, lines of trees; classified via a standardized key (Maskell et al., 2016).
- Feature sampling: minimum feature length of 20 m; gaps up to 20 m allowed; curtilage or within woodland canopy excluded.
- Data files and structure:
  - LANDSCAPE_LINEAR_FEATURES_2013_16.csv: core landscape linear feature data across up to 300 squares; includes spatial identifiers (SQ_ID, EASTING/NORTHING), feature length, theme, habitat name, historic management, species composition, and various attribute fields.
  - LANDSCAPE_LINEAR_FEATURE_SP_2013_16.csv: woody linear feature species data linked to features in the above file; includes species, vegetation type, proportion, and related identifiers.
  - Field definitions refer to GMEP Field Mapping Handbooks for detailed codes and categories.
- Data capture workflow minimizes post-survey digitizing and speeds QA.

## Data Quality Assurance (QA)

- Survey teams: experienced botanical surveyors; extensive pre-survey training to ensure consistency with handbooks (Maskell et al., 2016a/b).
- Data capture: digital system with mandatory fields and prompts; reduces illegible records and ensures complete coverage of mapped components.
- Data transfer: rapid transfer to office for timely checks; facilitates early issue resolution.
- Quality Control (QC): a second team re-surveys all or part of a square; results fed back to field teams to improve data quality and recording practices.

## Data Integration, Outputs, and Use

- Integrated approach across multiple scales and data types within a single 1 km framework to support holistic ecosystem assessments.
- Outputs designed to:
  - Provide robust national indicators of landscape features and biodiversity trends.
  - Support baseline estimation, national trends, and targeted regional analyses for Glastir.
  - Enable future integration with the Countryside Survey GB data for broader analyses.
- Outputs contribute to the evidence base for biodiversity conservation policy and reporting obligations (CBD 2020).

## Publications, References, and Documentation

- Methodology and sampling design referenced to:
  - ITE Land Classification of Great Britain (Bunce et al., 2007)
  - Field Mapping Handbooks (Maskell et al., 2016a, 2016b)
  - GMEP annual/final reports and associated CEH/NERC documentation (Emmett et al., 2014; 2017)
  - Supporting sources such as Jackson (2000), Maddock (2008), and UK BAP habitat guidance
- GMEP website provides overview and links to methodologies, results, and documentation: https://gmep.wales/

## Appendix: Roles, Tasks, and Field Teams

- Roles include database management, field team management, sampling design and statistics, vegetation expertise, GIS, and project management (examples: Astbury, Burden, Emmett, Maskell, Jarvis, Norton, Owen, Sharps, Smart, Williams, Wood, Wright, etc.).
- Field Survey Teams: extensive list of named team members contributing to data collection and fieldwork across Wales.