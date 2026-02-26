# Glastir Monitoring and Evaluation Programme (GMEP)

- Wales-wide agri-environment schemes and the GMEP
  - AES funding since the early 1990s; GMEP monitors Glastir effects on environment, biodiversity, woodland creation and management.
  - Aims to contribute to evidence for reversing native biodiversity decline and meeting biodiversity obligations; aligns with Well-Being of Future Generations Act indicators (Area of Healthy Ecosystems in Wales).

- Survey design and sampling framework
  - 4-year rolling cycle (first cycle 2013–2016) to maximise site coverage and detect temporal trends cost-effectively.
  - Two components: Wider Wales (baseline estimates and national trends) and Targeted Component (priority Glastir areas).
  - Common spatial unit: 1 km x 1 km squares; total of 300 squares sampled over the cycle.
  - Sampling approach mirrors Countryside Survey of Great Britain to enable future data integration.
  - Stratified random sampling within Land Classification strata; half the squares are Wider Wales (random within strata) and half are targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea replaced.
  - Anonymisation: square identifiers de-identified to protect confidentiality.

- Data collection methods and scope
  - Each square visited twice in a year (July and August) within 2013–2016; pollinator surveys conducted by Butterfly Conservation (BC) ecologists and staff.
  - Target groups: butterflies (species-level), bees and hoverflies (grouped by ecological difference); training and quality assurance emphasized; ID verified via photos and expert review.
  - Plant flowering abundance recorded using DAFOR-X scale (Dominant to not seen) for key flowering groups.
  - Two survey components per square:
    - Transect route: standardized 2 km path (Pollard Walks) through the square, divided into ten 200 m sections; record counts of butterflies and bee/hoverfly groups within 5 m² recording boxes; record DAFOR-X around transect sections; capture weather data (temperature, sunshine, wind).
    - Timed search: 150 m² flower-rich area within the square; 20-minute count of pollinators visiting flowers and visiting plant groups.
  - Timing and weather constraints: surveys conducted 10:00–16:00 (or 9:30–16:30 if shaded) with appropriate conditions (temperature 11–17°C with sun or >17°C with light wind).
  - Data and methodology references provided in field handbooks (GMEP Pollinators Handbooks, 2014/2017).

- Data structure and management
  - Two core data components per square: transect counts and timed observations.
  - For each component, two linked tables: VISIT (visit-level metadata) and COUNT (taxa/flower counts).
  - Linkage: VISITID in COUNT tables; SQ_ID (square) and date connect transect and timed observation datasets.
  - Lookup table GMEP_POLLINATOR_GROUP_CODES.csv maps GROUP_CODE to taxa groups, enabling interpretation of insect and plant group codes used in COUNT tables.
  - File-level details:
    - GMEP_POLLINATOR_TRAN_VISIT_2013_16.csv: transect visit metadata (SQ_ID, VISITID, date, recorder, weather, etc.).
    - GMEP_POLLINATOR_TRAN_COUNT_2013_16.csv: transect counts by section, group codes, and counts.
    - GMEP_POLLINATOR_OBSV_VISIT_2013_16.csv: timed observation metadata (SQ_ID, VISITID, date, recorder, weather).
    - GMEP_POLLINATOR_OBSV_COUNT_2013_16.csv: counts of pollinators interacting with flowering groups during timed observations.
    - GMEP_POLLINATOR_GROUP_CODES.csv: taxonomy and coding for groups, including names, taxonomic levels, and life-history details (esp. for butterflies and hoverflies).
  - Data structure supports integration across scales and future analyses with national datasets; anonymisation applied to site and recorder identifiers.

- Quality assurance, standards and governance
  - Training workshops for surveyors; ID guides provided; expert support via email; ID verification via photos reviewed by experts.
  - Quality control (QC): field QC in seven 1 km squares by an experienced UKCEH surveyor, repeating surveys in August with similar timing to participants’ second visit.
  - Online QA: after the first year, surveyors completed an image-based online assessment (randomized image sets, single attempt per surveyor).
  - Adherence to DEFRA Joint Codes of Practice (JCoPR) to ensure robust, repeatable, auditable science and processes.

- Relevance, outputs and potential for integration
  - Produces biodiversity indicators for semi-natural habitat change and contributes to national and regional biodiversity baselines.
  - Provides a framework to track progress toward Well-Being Act indicators via changes in healthy ecosystems in Wales.
  - Designed for potential integration with the Countryside Survey of Great Britain data streams due to shared sampling framework and 1 km spatial unit.
  - Results and methodologies are documented in annual/final reports, field handbooks, and the GMEP website; multiple publications and appendices support transparency and reproducibility.

- References, publications and resources
  - Key methodological references: Bunce et al. 2007 (ITE Land Classification), Pollard 1977 (Pollard Walk method).
  - GMEP project reports: Emmett et al. 2014 (First Year Annual Report), Emmett et al. 2017 (Final Report – Executive Summary).
  - Field handbooks and project website: GMEP Birds and Pollinators handbooks; GMEP website (gmep.wales).
  - Data governance and standards referenced via DEFRA JCoPR.

- Appendices and data capture instruments
  - Appendix 2: Transect recording forms for multiple butterfly species and pollinator groups; weather and site details.
  - Appendix 3: Timed observation recording forms, including start/end times, wind, temperature, % sun, and pollinator group interactions.
  - Appendix 4: Hoverfly ID – key groups and atypical groupings (for training and identification support).