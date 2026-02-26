# Glastir Monitoring & Evaluation Programme (GMEP) Pollinators Data and Methodology (2013-2016)

- Context and aims
  - In Wales, agri-environment schemes (AES) have funded activities since the 1990s; Glastir is a current focus.
  - GMEP was established by the Welsh Government in 2013 to monitor Glastir’s effects on biodiversity, woodland creation/management, and to support evidence toward reversing native biodiversity decline.
  - Data contribute to the CBD 2020 commitments and align with Wales’ Well-Being of Future Generations Act indicators, notably the Area of Healthy Ecosystems in Wales.

- Survey design and sampling framework
  - Adopted a 4-year rolling survey (2013–2016) to balance site coverage with year-to-year monitoring.
  - Two main components:
    - Wider Wales Component: baseline estimation, national trends, and national reporting for Glastir.
    - Targeted Component: links to Glastir priority areas.
  - Common unit of analysis: 1 km square; 300 squares sampled over the cycle.
  - Sampling method aligned with the Countryside Survey of Great Britain to enable future data integration; stratified sampling across Land Classification units to maximise environmental heterogeneity between strata.
  - Exclusions/replacements: squares with >75% urban land or >90% sea were replaced.
  - Data visualization: distribution of 1 km squares plotted at a high level to protect confidentiality.

- Data collection methods and protocols
  - Each square was visited twice in the year (July and August) by Butterfly Conservation (BC) ecologists; one region covered by a BC employee.
  - Pollinators targeted: butterflies (species-level for Lepidoptera), bees, and hoverflies (group-level for bees/hoverflies).
  - Data capture included:
    - Transect route: standardised 2 km transect following Pollard walk method, split into ten 200 m sections; records for each insect group within a 5 m2 recording box.
    - Timed searches: a 150 m2 flower-rich area within the square; 20-minute counts of pollinators visiting flowers.
    - Flower abundance: DAFOR-X scale (Dominant to Not seen) for key flowering plant groups.
  - Schedule and conditions:
    - Surveys conducted between 10:00–16:00 (or up to 16:30 if shading allows) with suitable weather (temperature and sunshine criteria; low wind).
    - Weather and time of day recorded; transects divided into sections with linked flowering plant observations.
  - Data collection documentation: Appendices detail recording forms and field handbooks.

- Data structure and schema
  - Two main data components per square: transect counts and timed observations.
  - Each component uses two linked tables:
    - VISIT table: metadata about each visit (time, conditions, weather, etc.).
    - COUNT table: counts for insects and flower observations linked to VISIT via VISITID.
  - Lookup and coding:
    - GMEP_POLLINATOR_GROUP_CODES.csv provides codes for insects and plant groups; used to interpret GROUP_CODE, FLOWER_GROUP_CODE, and INSECT_GROUP_CODE in COUNT tables.
    - Anonymised square IDs (SQ_ID) and recorder codes to protect privacy.
  - Specific data files (examples):
    - GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv: transect visit metadata (SQ_ID, VISITID, date, weather, etc.).
    - GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv: counts per transect section (SECTION, GROUP_CODE, COUNT, etc.).
    - GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv: timed observation visit metadata (SQ_ID, VISITID, date, weather, etc.).
    - GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv: counts of plant–insect interactions (FLOWER_GROUP_CODE, INSECT_GROUP_CODE, NUM_VISITS, etc.).
    - GMEP_POLLINATOR_GROUP_CODES.csv: taxonomy and metadata for GROUP_CODE entries (RECORDED_SPECIES_NAME, COMMON_NAME, TAXON, etc.).
  - Data relationships:
    - VISIT records connect to COUNT records via VISITID.
    - SQ_ID links across transect and observation datasets; LOOKUP tables provide taxonomic and group details.

- Quality assurance and governance
  - Training and validation:
    - A dedicated training workshop trained all surveyors in pollinator group identification; basic guides provided; expert support available via email.
    - Photos submitted for ID verification; expert review of photographs for quality control.
  - QC and ongoing QA:
    - QA visits to seven 1 km squares to replicate surveys; online assessments for surveyors after each survey year.
    - DEFRA Joint Codes of Practice (JCoPR) followed to ensure robust, auditable science and data processes.
  - Data provenance and reproducibility:
    - Detailed field handbooks and appendices support repeatability and methodological transparency.
    - Data and methodologies are supported by a suite of publications and a project website (GMEP).

- Publications, references, and documentation
  - References include land classification methodologies, the Pollard method for butterflies, and annual/final reports to Welsh Government.
  - Field handbooks and project website provide access to methodologies, results, and supplementary material.

- Roles and project teams
  - UKCEH staff: data management, QA, statistics, project coordination, field operations.
  - Consultant entomologist: training and QA support.
  - Butterfly Conservation (BC): field survey coordination and delivery.
  - Field survey team: listed individuals across multiple roles and regions.

- Appendices and forms (overview)
  - Appendix 2: Survey recording form for transect walks (structure for recording species/groups, environmental variables, and transect sections).
  - Appendix 3: Survey recording form for timed observations (start/end times, photography, DAFOR-X, and plant/insect group observations).
  - Appendix 4: Hoverfly ID key groups and typical/atypical species examples.

- Data stewardship considerations for reuse
  - Standardised 1 km grid unit framework enables integration with GB-wide datasets (e.g., Countryside Survey) and potential cross-program analyses.
  - Anonymisation and controlled access (SQ_ID and RECORDER codes) help protect sensitive information while preserving linkages for analysis.
  - Comprehensive metadata and lookup tables support accurate interpretation of GROUP_CODEs and taxonomic classifications.

- Key takeaways for data stewards
  - Robust, standardized data model with linked VISIT and COUNT tables supports multi-scale analysis of pollinator activity and plant–insect interactions.
  - Clear QA processes, training, and adherence to JCoPR enhance data quality, reproducibility, and trust.
  - The dataset is designed for interoperability with related GB-wide surveys and programmatic reporting requirements, while maintaining appropriate confidentiality.