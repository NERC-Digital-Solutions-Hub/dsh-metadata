# National Plant Monitoring Scheme survey data (2015-2017)

- Purpose: A habitat-based plant monitoring scheme designed to provide annual indications of changes in plant abundance and diversity, detect habitat-quality change, understand pressures/drivers, and contribute data for the UK Biodiversity Indicator C7. It focuses on volunteer-recorded plant data and habitat attributes across 28 fine NPMS habitats (11 broad categories) in the UK, Isle of Man, and Channel Islands. Data are held in CEH Wallingford and are updated annually with field guidance and QA processes.

- Partnership and outputs: Run by BSBI, CEH, JNCC, and Plantlife; aims to publish data for independent review and provide feedback to volunteers. Analysis is conducted by experienced quantitative ecologists using R; results disseminated via newsletters and peer-reviewed publications.

- Data scope and structure: The document describes the provided data files, the evidence quality assurance (EQA) process, and the field recording guidance issued to surveyors. It also includes the field methodology, data recording procedures, and how the data feed into habitat change assessments over time.

- Access and usage mindset for analysts: Data are organized for linkage across sampling locations, samples, and species occurrences, enabling analyses of change over time, habitat indicators, and drivers. Emphasis is placed on data provenance, metadata, validation, uncertainty, and the ability to reproduce results from standardized data dictionaries and verification systems.

- Evidence quality assurance (EQA) emphasis: NPMS data are supported by peer-reviewed and other published literature; the project uses a project Steering Group, external expert reviews as warranted, and explicit documentation of uncertainty and limitations. Data management plans and version control (PRINCE2 framework) underpin design and outputs, with transparent reporting of methods and results.

- Data accessibility and sharing: Data from NPMS will be publicly available to allow independent review. Users are encouraged to enter data online via the NPMS website; alternative submission by post is possible. Support contacts are provided for data submission and access issues.

- Data types and linkage (high-level): Four main CSV files:
  - locations_2015to2017.csv: unique location_id and location_type; links to sampling events in sampleInfo.
  - sampleInfo_2015to2017.csv: sampling events with id, survey_id, date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id.
  - sampleAttributes_2015to2017.csv: additional attributes linked to samples via sample_id (text_value with descriptive captions).
  - occurrences_2015to2017.csv: species observations linked to samples via sample_id; includes taxonversionkey, preferred_taxon, domin (abundance), record_status, sensitivity_precision.

- Data collection and field methods (analytical relevance):
  - NPMS habitats: 28 fine habitats, grouped into 11 broad NPMS categories.
  - Survey levels: Wildflower, Indicator, and Inventory (with increasing taxon lists and detail).
  - Plot design: 5x5 m square plots (10x10 m in woodlands) and 1x25 m linear plots; plots allocated within kilometre squares; aim for diverse habitat representation across plots.
  - Plot selection: Prefers pre-selected plots; Protocol A allows self-selected plots to represent average habitat conditions, with relocation features to aid future re-surveys.
  - Ponds, flushes, arable margins, hedgerows, road verges, standing water, and other habitats have specific plotting guidelines to maximize habitat representation and accessibility.
  - Data collection protocol: Record species presence and percent cover using the Domin scale; optional attributes include vegetation height, woodedness, aspect, slope, and management. Recording forms and guidance accompany fieldwork; participants can upload photographs and sketch plots to aid relocation.

- Data recording specifics (for modeling and QA):
  - Species data are captured using habitat-specific species lists; abundance is percent cover, with a standardized Domin scale.
  - Additional fields capture bare ground, litter, moss/lichen, and rock/gravel cover.
  - Optional site attributes (e.g., aspect, slope, management, grazing intensity) provide contextual covariates for ecological modeling.
  - Verification and quality checks include online data entry with controlled terms, calendar dates, geographic range checks, and iRecord-based expert review for incorrect or sensitive records.

- Data usage and outputs (analytic considerations):
  - Data are designed to support analyses of habitat quality changes, plant community shifts, and indicators across time.
  - Public release allows independent review; researchers can replicate analyses using the provided data structure and metadata.
  - Limitations and uncertainties are addressed through robust experimental design, model-based uncertainty estimation, and explicit communication of assumptions in outputs.

- Access, rights, and safety (operational notes):
  - Volunteers are instructed to respect land access rights and safety considerations; certain plots may be inaccessible due to safety or biosecurity concerns.
  - The project provides guidelines and a support channel for access and submission issues.
  - Data collection emphasizes relocation, field safety, and ethical engagement with landowners and other users.

- Appendix highlights: Habitat types and Domin scale details
  - Appendix 1 presents the 28 fine NPMS habitats and 11 broad categories (with descriptive definitions and example species/characteristics).
  - Domin scale: 10-point percentage cover scale (with guidance for translating observations into percent cover; examples provided for 1% increments on different plot sizes).
  - Guidance includes practical field tips for estimating cover, handling multi-layer vegetation, and translating visual observations into standardized scores.

- Summary for analysts:
  - The NPMS 2015-2017 dataset provides a linked, multi-level data structure (locations, samples, attributes, and species occurrences) designed for robust assessment of habitat quality and plant community change over time.
  - Data quality is underpinned by a formal EQA framework, external reviews, transparent documentation, and version-controlled data management.
  - The design supports modeling of spatially and temporally aligned changes, incorporating habitat indicators, sampling effort, and optional environmental covariates.
  - Public data access and clear metadata enable reproducible analyses, with explicit acknowledgment of uncertainties and limitations in outputs.