# Glastir Monitoring & Evaluation Programme

- The Welsh Government’s GMEP (Glastir Monitoring and Evaluation Programme) collects biodiversity-related data to monitor landscape features and the condition/management of woody features, supporting Wales’ biodiversity obligations under international frameworks.
- The programme operates on a 4-year rolling survey cycle (2013–2016) to maximise site coverage and detect year-on-year changes, with two integrated components: Wider Wales (baseline estimation and national trends) and Targeted (priority Glastir areas).
- A single spatial unit (1 km grid squares) is used across both components to enable data integration and future cross-analysis.

- Survey design and sampling
  - 300 1 km squares are sampled over the cycle; half randomly within strata defined by the ITE Land Classification (Bunce et al., 2007) and half targeted at Glastir priority areas.
  - Exclusions: squares with more than 75% urban land or more than 90% sea.
  - Sampling methodology mirrors the Countryside Survey of Great Britain to support national and sub-national indicators and potential future integration.

- Data collection methods
  - In each 1 km square, linear, areal, and point features are mapped onto base maps using predetermined coded options.
  - Field data collection uses electronic methods (CS Surveyor) with Esri GIS integration for accuracy and efficiency.
  - Linear features: landscape elements less than 5 m wide, including hedges (woody linear features), walls, fences, streams, etc. Recording includes length and condition, with a minimum feature length of 20 m and gaps up to 20 m.
  - Woody linear features (hedges, lines of trees) are classified with a standardized key (Maskell et al., 2016).

- Datasets and data schema
  - GMEP_LANDSCAPE_LINEAR_FEATURES_2013_16.csv: contains landscape linear features across up to 300 squares, with identifiers, 10 km grid coordinates, event/feature IDs, feature geometry, thematic and descriptive attributes (theme, habitat name, management indicators, species-related fields, verge widths, etc.), and various physical measurements (length, margins, width, height, etc.).
  - GMEP_LANDSCAPE_LINEAR_FEATURE_SP_2013_16.csv: holds woody linear feature species data, including species identifiers, vegetation type, species name, and proportional cover.
  - Data are aligned with definitions and classifications in the GMEP Field Mapping Handbooks (Maskell et al., 2016a, 2016b).

- Quality Assurance and data quality
  - Surveys conducted by trained botanical surveyors; field teams receive intensive training to ensure consistency with field handbooks.
  - Electronic data capture (CS Surveyor) reduces transcription errors and ensures all mapped components are visited.
  - Mandatory data entry fields and prompts improve data completeness and consistency; rapid data transfer enables timely quality checks.
  - A QC process involves a second team re-surveying all or part of a square; findings feed back to field teams to improve recording.

- Data integration and spatial context
  - A common 1 km sampling unit enables integration across Wider Wales and Targeted components, and future integration with the Countryside Survey GB dataset.
  - Spatial confidentiality is considered by plotting location data at 10 km resolution for public-facing outputs.
  - The methodology and data structure support national trend analysis and regional decision-making.

- References and documentation
  - Field mapping handbooks (Maskell et al., 2016) and related methodological guidance.
  - ITE Land Classification of Great Britain 2007 (Bunce et al.; stratification basis).
  - GMEP project reports and website (gmep.wales) for methodologies, results, and supplementary materials.
  - Relevant habitat and biodiversity classification references (e.g., Stace 1997; JNCC/DEFRA materials).

- Roles and team structure (context for GIS work)
  - Designated roles for database management, field teams, lead scientists, vegetation experts, statistics and sampling design specialists, and project management.
  - Field survey teams comprise numerous personnel across Wales with explicit responsibilities for data collection, validation, and coordination.