# Glastir Monitoring and Evaluation Programme (GMEP)

- Purpose and context
  - Welsh Government agri-environment scheme monitoring since the early 1990s (e.g., ESAs, Glastir variants) to track biodiversity and woodland management.
  - GMEP aims to provide an evidence base for reversing native biodiversity decline and meeting CBD 2020 obligations.
  - Data collection supports national biodiversity indicators, landscape features mapping, and integration with broader UK surveys.

- Survey design and sampling
  - 4-year rolling survey cycle (first cycle 2013–2016) to maximise site coverage and detect spatial and temporal trends cost-effectively.
  - Two components:
    - Wider Wales Component: baseline estimation, national trends, national reporting.
    - Targeted Component: focuses on Glastir priority areas.
  - Common spatial unit: 1 km2 squares, enabling cross-analysis and potential future integration with the Countryside Survey of Great Britain.
  - Sample: 300 1 km squares across Wales (split evenly between Wider Wales and targeted areas).
  - Stratification and exclusion:
    - Squares randomly sampled within strata defined by the ITE Land Classification of GB 2007 (Bunce et al., 2007) to balance environmental heterogeneity.
    - Exclude squares with >75% urban land or >90% sea.
  - Methodology alignment: uses the same sampling framework as GB Countryside Survey to facilitate future data integration.

- Data collection methods and dataset content
  - Within each 1 km square: mapping of point, areal, and line features onto base maps using predefined codes (field handbooks provided).
  - Electronic data capture: CS Surveyor software with ESRI GIS integration, enabling real-time data entry and reducing post-processing errors.
  - Point features: elements occupying <20 m × 20 m (e.g., trees/groups, ponds, cliffs, buildings with use codes).
  - Dataset: GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv
    - Key fields include: SQ_ID (1 km square code), PCOMPDATA_ID, PCOMPDATA_GUID (unique feature ID), THEME, HABITAT_NAME, VETERAN_TREE_TYPE, DEAD_MISSING_BARK, LIGHTNING_STRIKES, MISSING_LIMBS, HOLLOW_TRUNK, DEAD_WOOD, IVY_COVER, EPIPHYTE_COVER, CANOPY_LIVE, TREE_DEAD, VEGETATION_TYPE, MODAL_DBH, SPECIES, PROPORTION, USE, HABITAT_BOX, DISEASE_SIGNS, BUFFER, SURVEY_YEAR, and 10 km easting/northing coordinates, plus LC (Land Classification).
    - Data captured at 2013–2016 survey period, with species nomenclature following Stace (1997).

- Data quality assurance and governance
  - QA-driven field program: surveys conducted by experienced botanical surveyors; intensive pre-survey training to ensure consistent methodology and recording.
  - Electronic data capture reduces illegible records and enables prompt data checks.
  - Data quality control (QC) exercise: a second survey team re-visits all or part of a square; issues fed back to field teams for improvement.
  - Roles and teams: explicit lists of QA leads, project managers, field team managers, database managers, GIS experts, and vegetation specialists; names documented as part of governance and accountability.

- Data usage, outputs, and access
  - Designed to contribute to the evidence base for Wales’ biodiversity monitoring and to track progress toward CBD targets.
  - Data intended for national reporting and to support policy decisions; results and methodologies are disseminated through the Glastir Monitoring & Evaluation Programme website (gmep.wales) and related publications.
  - Field handbooks and reference documentation underpin reproducibility and future integration with other datasets (e.g., Countryside Survey GB).

- Supporting documentation and references
  - Field handbooks: Mapping Field Handbook Part 1 (habitat attributes) and Part 2 (using Surveyor software).
  - Key methodological references: Bunce et al. 2007 ITE Land Classification; Maskell et al. 2016 field handbooks; Emmett et al. reports (2014, 2017) on GMEP; Stace 1997 plant nomenclature; JNCC/BAP habitat guidance.
  - Websites and reports provide the general overview, detailed methodologies, and results.

- Stakeholders and team overview
  - QA and project leadership, field team managers, database and GIS specialists, and a large field survey team contributing to data collection and validation.
  - Collaboration framework supports ongoing data sharing, methodological consistency, and potential sector-wide coordination for stronger data communities of practice.