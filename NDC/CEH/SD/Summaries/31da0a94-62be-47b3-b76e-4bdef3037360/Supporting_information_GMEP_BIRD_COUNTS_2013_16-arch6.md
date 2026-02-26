# Glastir Monitoring & Evaluation Programme (GMEP) Bird Survey Data and Methodology

- Purpose and scope
  - Welsh Government-backed programme to monitor biodiversity and habitat change as part of Glastir and to support evidence for biodiversity targets and Well-Being goals.
  - Focuses on landscape-scale biodiversity indicators, including semi-natural habitat changes and habitat use.

- Survey design and sampling framework
  - 4-year rolling cycle (2013–2016) to capture spatial and temporal variation cost-effectively.
  - Two components:
    - Wider Wales Component: baseline estimation and national trends.
    - Targeted Component: links to Glastir priority areas.
  - Common spatial unit: 1 km grid squares.
  - Sampling plan: 300 1 km squares over four years; half randomly sampled within Land Classification strata (ITE framework) and half targeted at Glastir priorities.
  - Exclusions: squares with >75% urban land or >90% sea replaced with alternatives.

- Data collection methods (bird surveys)
  - Coordinated by British Trust for Ornithology (BTO).
  - Objective: robust counts of breeding pairs per species within each square and habitat use data.
  - Survey cadence:
    - Four visits per square (reduced to three in 2015–16) between mid-March and mid-July.
    - Surveys started around 06:00, up to 5 hours per visit; routes designed to cover all accessible parts within 50 m of boundaries.
  - Field protocol details:
    - Record all birds seen or heard with location, behavior, and habitat context.
    - Use standard BTO two-letter species codes and CBC notation; include birds just outside boundaries when relevant for territory analyses.
    - Map routes with start points varied across visits; document poorly covered areas to assess data completeness.
  - Data capture and storage:
    - Data collected on standard forms and field maps; later digitized in ArcMap (up to v10.5) for precise, mapped bird locations.
    - Quality control during transcription: cross-check counts and species identifications with surveyors as needed.

- Data structure and files (data products)
  - GMEP_BIRD_COUNTS_2013_16.csv: core sightings data for 300 squares across Wales, including visit number, date, species code, counts, observer, location, and habitat context.
  - GMEP_BTO_SPECIES_CODES.csv: lookup for BTO two-letter species codes to English and Latin names, and status notes.
  - Availability of anonymized observer IDs and 10 km grid coordinates (E/N) for spatial analyses.
  - SQ_ID: unique 1 km square identifier; LC: sampling framework code (ITE Land Classification).

- Quality assurance and data governance
  - Experienced ornithological teams with standardized training and QC checks prior to each survey period.
  - Field coordinators provide ongoing support; data input via BTO Wales office and head office, with digitization and mapping by qualified personnel.
  - QC checks include:
    - Verification of uncertain counts and species codes with surveyors.
    - Post-processing checks for unrecognized codes and improbable counts.
  - Adherence to DEFRA Joint Codes of Practice (JCoPR) to ensure quality, robustness, and auditability of scientific methods.

- Data access, reuse, and integration
  - Data designed for integration with other GB surveys (e.g., Countryside Survey) and future cross-analysis.
  - Spatially explicit at 1 km resolution, enabling national and sub-national trend analyses.
  - Outputs support biodiversity indicators linked to Well-Being Act commitments and habitat management assessments.

- References and supporting materials
  - Field handbooks and methodology documents (e.g., GMEP Birds Handbook, v4, 2014).
  - Related publications on land classification and survey design.
  - Glastir Monitoring & Evaluation Programme website (gmep.wales) for documentation and results.
  - Notable foundational works: Common Birds Census methodology and BBS-related guidelines.

- People and organizational roles
  - UKCEH (UK Centre for Ecology & Hydrology) staff handling data management, QA, field coordination, and statistical support.
  - BTO staff leading scientific direction, field coordination, and spatial data processing.
  - Field survey team comprising multiple surveyors contributing to annual data collection.

- Practical implications for data users
  - Rich, standardized bird survey data across Wales suitable for trend analyses, habitat association studies, and integration with other landscape-scale indicators.
  - Clear documentation of sampling design, data collection procedures, and QA processes enhances reliability and reproducibility.
  - Anonymized observer identifiers and precise 1 km square geolocations facilitate geographically explicit insights while maintaining confidentiality.