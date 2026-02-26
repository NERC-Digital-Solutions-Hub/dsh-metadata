# National Plant Monitoring Scheme (NPMS) Data Resources and Evidence Quality Assurance

- Purpose and scope
  - NPMS is a habitat-based plant monitoring scheme designed to track annual changes in plant abundance and diversity.
  - Aims include detecting change in priority habitats, understanding drivers of change, and contributing to the UK Biodiversity Indicator C7 (plants of the wider countryside).
  - Data are collected from volunteer recorders across the UK, Isle of Man, and Channel Islands using a structured, plot-based approach.

- Data files and structure
  - locations_2015to2022.csv
    - Links location_id to location_type and identifies survey plots (square or linear) by habitat type.
  - sampleInfoWithLatLong_2015to2022.csv
    - Contains sampling events per location_id with fields: id (sample_id), survey_id (type of NPMS survey), date_start, entered_sref and system, coordinates (LATITUDE/LONGITUDE), monad (1 km grid), monadCRS, country, and audit fields (created_on, created_by_id).
  - sampleAttributes_2015to2022.csv
    - Extra data about samples; links to sampleInfo via sample_id; includes caption and text_value describing attributes (e.g., habitat category).
  - occurrences_2015to2022.csv
    - Species observations per sample; fields include id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), and sensitivity_precision (spatial blur flag).
  - npmsHabitatLookup.csv
    - Maps NPMS fine-scale habitats to NPMS broad habitat categories.
  - dominScores.csv
    - Harmonises multiple Domin score formats from different survey levels; provides dominIndex and midPoint for comparable abundance estimates.
  - Relationships and linking
    - location_id in locations_2015to2022.csv links to sampleInfoWithLatLong_2015to2022.csv.
    - sample_id (id) in sampleInfoWithLatLong_2015to2022 links to sampleAttributes_2015to2022.csv and to occurrences_2015to2022.csv.
    - Occurrences include verification status via iRecord and, if applicable, spatial sensitivity controls.

- Examples of accessing and joining habitat information
  - In R: merge sampleInfoWithLatLong with sampleAttributes filtered to NPMS Habitat attributes:
    - samples <- read.csv('sampleInfoWithLatLong_2015to2022.csv')
    - sampleAtts <- read.csv('sampleAttributes_2015to2022.csv')
    - sampleHabAtts <- subset(sampleAtts, caption == 'NPMS Habitat')
    - samplesWithHabs <- merge(samples, sampleHabAtts, by.x = 'id', by.y = 'sample_id')
  - Similar operations can be performed in SQL or other databases.

- Survey types and data coding
  - survey_id values include:
    - 87: Wildflower survey
    - 154: Inventory survey
    - 155: Indicator survey
  - Spatial referencing: OSGB (British National Grid), Irish National Grid, or WGS84 (EPSG:4326).
  - monad concept refers to 1 km grid squares; monadCRS indicates the CRS used for monads.
  - Country labels include Britain, Channel_Islands, Northern_Ireland.
  - Domin scores may be NULL (presence with no abundance) or reflect abundance categories; record_status indicates verification status (C, V, R).
  - Some records may be spatially blurred (sensitivity_precision = 10000).

- How to access and use the data
  - Data are organized to enable join-based analyses across locations, samples, and species occurrences.
  - The NPMS emphasizes transparent data handling, with guidance documents and a pathway to publish data for independent review.

- Evidence Quality Assurance (EQA) framework
  - Publications supporting EQA:
    - Journal articles on design, implementation, and modeling of NPMS and citizen-science monitoring.
    - Additional articles and reports detailing NPMS development, cross-scheme comparisons, and Bayesian modeling approaches.
  - QA governance and processes
    - Project Steering Group oversees work; external peer review pursued when risk warrants it (e.g., survey design).
    - Uncertainty and limitations are communicated through outputs (newsletters, reports) reviewed by scientists to ensure claims are evidence-based.
    - Robust statistical design supports estimation of uncertainty; data-driven analyses performed by quantitative ecologists using R scripts.
    - Document tracking and version control follow a Data Management Plan aligned with PRINCE2 standards; all outputs are archived and backed up off-site.
  - Data access, transparency, and publication
    - Data from NPMS are publicly available to enable independent review of results.
    - Ongoing engagement with the Monitoring science community for critique and improvement.

- Quality assurance of field recording and data collection
  - Field recording is volunteer-based with three levels of contributor expertise; training and guidance are provided.
  - Online data capture ensures structured data entry; a species dictionary, calendar dates, and controlled terms reduce errors.
  - Verification through iRecord (for botanist experts) handles exceptions requiring higher expertise.
  - Formal, scheme-wide quality assessment of field recording is not currently part of NPMS but is planned for the future.
  - Data input and verification include geographic range checks and other automated quality checks.

- Aims, scope, and outputs
  - NPMS aims to deliver annual snapshots of plant communities across key habitats and to support understanding of ecological drivers and pressures.
  - Outputs include newsletters, reports, and peer-reviewed publications; results are designed for researchers, volunteers, policymakers, and the public.

- Practical considerations for analysts
  - The dataset supports estimating habitat change, species occurrences, and abundance patterns across time and space.
  - Recognize potential limitations:
    - Presence-only records with domin values; possible gaps at local scales or in certain habitats.
    - Verification status and potential data sensitivity (blurred locations) affecting precision.
  - Harmonization via dominScores and the use of standardized habitat mappings aids cross-scheme comparisons.

- References and resources
  - Multiple peer-reviewed articles, newsletters, and internal/external reports underpinning design, QA, and methodological approaches.
  - Official NPMS resources and survey guidance documents available for deeper context and methodological details.