# Glastir Monitoring &Evaluation Programme

- Purpose and context
  - Welsh Government AES-funded biodiversity monitoring program (GMEP) established to track effects of Glastir on biodiversity and woodland management.
  - Data support evidence base for reversing native biodiversity decline and fulfilling Convention on Biological Diversity 2020 obligations; informs Welsh Well-Being Act 2015 indicator on Area of Healthy Ecosystems.

- Study design and sampling
  - 4-year rolling survey cycle (2013–2016 first cycle) to capture spatial and temporal trends cost-effectively.
  - Two components: Wider Wales baseline/trends and Targeted component focusing on Glastir priority areas; both use a common 1 km grid unit.
  - Sampling: 300 1 km squares over cycle; Half randomly selected within Land Classification strata; Half targeted at Glastir priority areas.
  - Exclusions: urban >75% or sea >90% squares excluded and replaced.

- Data collection methods
  - Bird surveys coordinated by British Trust for Ornithology (BTO) using a robust protocol to estimate breeding pairs and habitat associations.
  - Fieldwork intensity: 4 visits per square (reduced to 3 visits from 2015–16); visits mid-March to mid-July; each visit up to 5 hours, starting around 06:00.
  - Survey design ensures detailed habitat and local abundance data, enabling finer-scale inference than broader national surveys.
  - Route coverage: surveyors walked within 50 m of all accessible parts of the square; routes varied by visit to ensure full coverage and minimize double-counting.

- Data specifications, dictionaries, and formats
  - Primary dataset: GMEP_BIRD_COUNTS_2013_16.csv
  - Supporting dictionaries: GMEP_BTO_SPECIES_CODES.csv (lookup for BTO two-letter codes with English and Latin names and status)
  - Variables include: visit number/date, species code, activity, count, notes, observer (anonymised), Ind_ID and ProB_ID identifiers, Year, SQ_ID, Easting/Northing (10 km grid), and Land Classification (LC)
  - Spatial scope: 1 km survey squares; coordinates in OSGB 1936 system (E/N in metres)
  - Anonymisation: observer IDs anonymised to four-letter codes

- Data collection standards and metadata
  - Data collection aligned with BTO Common Birds Census lineage; standardised field maps and CBC notation for species and behaviours.
  - Metadata and data dictionaries provide interpretation of fields, including what constitutes separate records for individuals and probable recaptures.
  - Use of BTO field handbook and codes to ensure consistency across years and teams.
  - Data dictionaries reference crosswalks to English/Latin names and species status for clarity.

- Quality assurance and governance
  - Surveys conducted by experienced ornithological teams; QA via training, field protocols, and ongoing support from a designated survey coordinator.
  - Data digitisation conducted at BTO offices (Bangor, then head office) with ArcMap GIS processing.
  - QA checks include verification of uncertain counts and species codes, cross-checks with surveyors, and subsequent checks for unrecognized codes or improbable counts during processing.
  - Compliance with DEFRA Joint Codes of Practice (JCoPR) to ensure robust, auditable scientific standards.

- Data storage, access, and sharing
  - Primary data management and storage within BTO Wales and UK offices; field forms and maps collated locally before digital input.
  - Digitised data provide precise, mapped bird locations; field data supervised by a lead scientist and QA personnel.
  - Public-facing references and project website ( gmep.wales ) provide methodological and results information, supporting transparency and potential data reuse.

- Data integration, interoperability, and reuse
  - 1 km spatial unit adopted to enable integration with national surveys (e.g., Countryside Survey of Great Britain) and future cross-project analyses.
  - Metadata supports cross-study reuse through standardized 1 km grids, OSGB coordinates, and consistent species coding.
  - Data dictionaries and accompanying publications facilitate reproducibility and secondary analyses.

- Key considerations and challenges for data stewards
  - Ensuring complete alignment between user needs and data collected across Wider Wales and Targeted components.
  - Timely receipt and standardisation of data from field teams; maintaining consistent metadata across years.
  - Handling multiple data formats and systems (field forms, maps, GIS data) and maintaining interoperability as the dataset grows.
  - Managing large volumes of spatially explicit data (3–4 visits per square across 300 squares per cycle) with careful QA to preserve data quality.
  - Ongoing governance to maintain anonymisation of observers and consistency with ethical/privacy standards.

- Related outputs and references
  - Field handbooks and methodological references (e.g., GMEP Birds Field Handbook, O'Connor 1990 CBC methods, Harris et al. 2019 BBS methodology).
  - Supporting datasets and code lists (GMEP_BIRD_COUNTS_2013_16.csv; GMEP_BTO_SPECIES_CODES.csv).
  - Documentation and project resources via the Glastir Monitoring & Evaluation Programme website and annual/final reports.