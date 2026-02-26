# Glastir Monitoring & Evaluation Programme

- Aim
  - Collect data to measure biodiversity and the condition/management of woody landscape features in Wales.
  - Build an evidence base to track progress in reversing the decline of native biodiversity and meet obligations under the Convention on Biological Diversity (CBD) 2020.

- Survey design and cycle
  - Rolling 4-year survey cycle (2013–2016) to maximise site coverage while monitoring year-on-year changes.
  - Two components:
    - Wider Wales Component: baseline estimation, national trends, and national reporting for Glastir.
    - Targeted Component: links to Glastir priority areas.
  - Common spatial unit: 1 km square.
  - Sampling: 300 1 km squares over the cycle; half randomly sampled from strata within the Land Classification of Great Britain (ITE framework) to maximize heterogeneity, half targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea.
  - Rationale: enables integration across metrics and with GB data; mirrors Countryside Survey GB methodology for future data integration.

- Data collection methods
  - Within each 1 km square, map linear features (primarily lines <5 m wide) using pre-determined coded options.
  - Features recorded include boundaries, hedges (woody), unmanaged lines, walls, fences, streams, etc.; minimum length 20 m with up to 20 m gaps.
  - Woody linear features (hedges, lines of trees) classified using a standardized key.
  - Data capture: electronic field mapping with CS Surveyor software and Esri GIS; mandatory fields and prompts to ensure consistent data collection.
  - Objects and metrics collected are designed to support an ecosystem-based assessment of landscape features.

- Data structure and formats
  - Landscape linear features data (up to 300 1 km squares, 2013–2016):
    - Key fields include: EVENTDATA_GUID, LINEARDATA_GUID, SQ_ID, LC (Land Classification), EASTING_10km, NORTHING_10km, EVENT_FROM, EVENT_TO, LENGTH_M, THEME, HABITAT_NAME, HISTORIC_MANAGEMENT, etc.
    - Links to a companion dataset via GUIDs for feature location and attribution.
  - Landscape linear features – woody species data (2013–16):
    - Fields include: SEVENTDATA_ID, SEVENTDATA_GUID, SPECIES, VEGETATION_TYPE, PROPORTION.
  - Definitions and codes are provided in the GMEP Field Mapping Handbooks.

- Quality assurance and data quality
  - Surveys conducted by experienced botanical survey teams; extensive pre-survey training to ensure consistency with handbooks.
  - Digital capture (CS Surveyor) reduces transcription errors; mandatory fields and prompts improve data completeness.
  - Data transfer to the office soon after fieldwork allows prompt data checks.
  - Quality control (QC) involves a second team re-surveying all or part of a square; QC findings fed back to improve recording.

- Rationale and integration considerations
  - Uses the same sampling framework and methodologies as the Countryside Survey of Great Britain to enable future integration and comparability across GB.
  - Produces standardized, shareable data to support national and regional biodiversity monitoring.

- Outputs, publications, and references
  - Methodological and results references include publications from Bunce et al. (ITE Land Classification), Emmett et al. (GMEP annual and final reports), and the GMEP Field Mapping Handbooks.
  - Documentation and project website provide access to methodologies, results, and data handling practices.

- Appendices: roles and field teams
  - Roles and responsibilities listed for key personnel (database management, field management, science leadership, vegetation expertise, sampling design, statistics, project management, GIS, etc.).
  - Field Survey Teams comprise a large list of named personnel, illustrating the collaborative field effort underpinning the monitoring programme.

- Key takeaways for analysts
  - A standardized, multi-metric, ecosystem-based monitoring framework implemented over a 4-year rolling cycle across 300 1 km squares in Wales.
  - Primary focus on linear woody landscape features and their condition, with accompanying vegetation data to support biodiversity assessments.
  - Data collected in structured CSV formats with robust QA processes and clear links between feature locations and attribute data.
  - Designed for long-term trend analysis and integration with GB-wide biodiversity monitoring efforts.