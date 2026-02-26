# Glastir Monitoring & Evaluation Programme (GMEP) – Bird Survey Data 2013-2016

- Overview
  - Welsh Government programme (GMEP) to monitor biodiversity, woodland creation, and habitat management under Glastir.
  - Data support evidence for reversing native biodiversity decline and tracking Well-Being of Future Generations indicators (Area of Healthy Ecosystems in Wales).
  - Spatial unit: 1 km squares; data collection designed for integration across scales and metrics; outputs suitable for map-based analyses and policy / public audiences.

- Sampling design and scope
  - 4-year rolling survey cycle (2013–2016) to maximize site coverage and detect year-to-year changes.
  - Two components:
    - Wider Wales Component: baseline estimation and national trends.
    - Targeted Component: focuses on Glastir priority areas.
  - 300 x 1 km squares sampled across Wales; half randomly selected within stratified Land Classification (ITE) areas, half targeted to Glastir priorities.
  - Exclusions: squares with >75% urban land or >90% sea replaced with alternatives.
  - Common spatial unit for integration: 1 km square; planning aligned with Countryside Survey GB to enable future integration.
  - Plot confidentiality: maps published at 10 km resolution.

- Data collection methods (Bird surveys)
  - Led by British Trust for Ornithology (BTO); robust estimates of breeding pairs and habitat associations.
  - Survey design mirrors national BBS scale but is more intensive to improve local accuracy:
    - 60–90 squares surveyed per year (smaller sample vs. BBS).
    - Each square: 4 visits (reduced to 3 visits from 2015–16), mid-March to mid-July.
  - Field protocol:
    - Four visits (three in later years), starting around 06:00, up to 5 hours per visit.
    - Route passes within 50 m of all accessible parts of the square; routes rotated between visits.
    - Record all birds seen/heard with BTO activity codes; note not only counts but behavior (territorial, nesting, etc.).
    - Include birds just outside the boundary if necessary to identify territorial overlaps.
    - Record weather and route coverage; mark areas poorly covered or not covered.
  - Data capture:
    - Use A3 field maps per visit; standard CBC notation and two-letter BTO codes.
    - Anonymized observer identifiers; routes and observations mapped for spatial analysis.
  - Data collection documentation:
    - See GMEP Birds Field Handbook (GMEP_Birds_Handbook_v4_2014.pdf) for full details.

- Data files and structure (GIS-ready)
  - GMEP_BIRD_COUNTS_2013_16.csv
    - Core fields: Visit number, Date, Species (BTO codes), Activity, Count, Notes, Ind_ID, Year, ProB_ID, Sex, Observer (anon. 4-letter code), EASTING_10km, NORTHING_10km, SQ_ID (anon. 6-letter), LC (ITE Land Classification), plus derived fields for analysis.
    - Spatial coordinates provided at 10 km resolution (OSGB) to support GIS mapping while preserving confidentiality.
  - GMEP_BTO_SPECIES_CODES.csv
    - Lookup for BTO two-letter species codes with English and Latin names and status.
  - Data context
    - Records cover 300 1 km squares across 2013–2016; linked to field methods and sampling framework.
  - Data storage and access
    - Anonymized observer codes; data digitized in ArcMap (up to v10.5) for precise mapping.

- Quality assurance and data management
  - Field teams vetted for survey ability via interviews and audio-visual QC tests; ongoing training before each survey period.
  - Data recorded on standard forms and field maps; collated in BTO Wales office and digitized at BTO head office.
  - QC checks:
    - Verification of counts, species codes, and identifications with surveyors.
    - Automated and manual checks for unrecognized species codes and implausible counts during processing.
  - Standards and governance:
    - Adheres to DEFRA Joint Codes of Practice (JCoPR) for scientific quality and repeatability.
    - Documented in field handbooks and project reports; data are auditable and robust for trend analysis.

- GIS and analytical implications
  - Spatial unit integrity (1 km squares) enables national and sub-national trend analyses and integration with GB-level surveys.
  - 10 km plotting for confidentiality; 1 km grid allows detailed habitat–species associations and habitat management impact assessments.
  - Data suitable for mapping breeding bird distributions, habitat preferences (e.g., Glastir habitat management areas), and monitoring changes over time.
  - Links to broader biodiversity indicators and biodiversity-related policy reporting (e.g., Well-Being Act indicators).

- Key references and resources
  - ITE Land Classification of Great Britain (Bunce et al., 2007) – sampling framework.
  - O’Connor (1990) – Common Birds Census design and methods.
  - Harris et al. (2019) – The Breeding Bird Survey 2018 methodologies.
  - Siriwardena & Taylor (2014) – GMEP Bird Survey Field Handbook.
  - GMEP project website and annual/final reports (UKCEH/BTO collaboration).

- People and teams involved (high-level)
  - UK Centre for Ecology & Hydrology (UKCEH) staff: project lead, data management, QA, field coordination.
  - British Trust for Ornithology (BTO) staff: lead scientists, field coordination, spatial data processing.
  - Field survey teams: qualified ornithological surveyors executing the standardized protocol.

- Practical notes for GIS users
  - Expect output data to support spatial analyses of breeding birds at 1 km resolution, integrated with habitat management and Land Classification layers.
  - Use 10 km anonymized coordinates for display where necessary; refer to SQ_ID for square-level aggregation.
  - Cross-reference with BTO species codes and GMEP field handbook for coding and interpretation of observations.