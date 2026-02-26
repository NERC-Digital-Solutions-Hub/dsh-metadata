# Introduction The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC.

- Purpose and scope
  - A volunteer-based plant monitoring scheme across the UK, Isle of Man and Channel Islands to provide annual indicators of changes in plant abundance and diversity.
  - Objectives include detecting changes in key habitats, understanding drivers of change, and contributing to the UK Biodiversity Indicator on plants.

- Data product and current dataset
  - An annually updated dataset representing the NPMS database held at UKCEH Wallingford.
  - The document describes the files provided (2015–2020) and the evidence quality assurance (EQA) process.

- Data files provided (GIS-relevant structure and fields)
  - locationTypes_2015to2020.csv
    - location_id: unique location identifier
    - location_type: survey plot type (e.g., square, linear)
  - sampleInfoWithLatLong_2015to2020.csv
    - id: sample identifier
    - survey_id: NPMS survey type (87 Wildflower, 154 Inventory, 155 Indicator)
    - date_start: sampling date
    - location_id: links to locationTypes_2015to2020
    - entered_sref and entered_sref_system: spatial reference and CRS
    - LATITUDE, LONGITUDE: precise sample coordinates
    - monad and monadCRS: 1 km grid unit and its CRS (OSGB, OSIE, UTM30)
    - country: territory context
    - additional metadata: created_on, created_by_id
  - sampleAttributes_2015to2020.csv
    - sample_attribute_id, sample_id (links to sampleInfoWithLatLong), caption, text_value
  - occurrences_2015to2020.csv
    - id: unique occurrence ID
    - sample_id: links to sampleInfoWithLatLong
    - taxonversionkey, preferred_taxon: taxon identifiers/names
    - domin: Domin cover score
    - record_status: verification status (C, V, R)
    - sensitivity_precision: 10000 indicates privacy-blurred records
  - npmsHabitatLookup.csv
    - NPMS_broad_habitat, NPMS_fine-scale_habitat: mapping between habitat levels
  - dominScores.csv
    - domin: original Domin score
    - dominIndex: harmonised Domin category
    - midPoint: interpreted mid-points for Domin categories

- Working with habitat information
  - Example workflow (R): merging sampleInfoWithLatLong with sampleAttributes to extract habitat data where caption == 'NPMS Habitat'.
  - SQL or other databases can perform a LEFT JOIN between sampleInfoWithLatLong and sampleAttributes using sample_id.

- Evidence Quality Assurance (EQA) framework
  - EQA materials and publications support data quality considerations and usage.
  - Key thematic areas include study design, data input/verification, data publishing, analysis, and reporting.
  - Outputs are reviewed to ensure claims are evidence-supported; data are openly available for independent review.

- QA and governance details (Q&A highlights)
  - Q1: Methods and publications were peer-reviewed; design and monitoring components involved statistical and botanical experts.
  - Q2: Steering Group oversight with external peer review for higher-risk outputs; design workshops inform robust QA.
  - Q3: Uncertainty and limitations are communicated through reviewed outputs (newsletters, reports).
  - Q4: Bias reduction through robust statistical design enabling uncertainty estimation.
  - Q5: Document tracking and version control via a Data Management Plan and PRINCE2 standards; off-site backups.

- Spatial and data quality considerations for GIS
  - Spatial references and coordinate systems are explicitly documented (OSGB, Irish Grid, UTM, EPSG:27700/29902/32630, and 4326).
  - Monads (1 km squares) provide a consistent spatial unit for aggregation and mapping.
  - Sensitive records may be blurred to 10 km, controlling precision in published data.
  - Data are collected across multiple plot types and habitats, enabling multi-scale map visualizations.

- Implications for GIS product development
  - Rich geospatial dataset enabling map-based analyses of habitat change and plant community dynamics.
  - Supports integration with other biodiversity datasets through standardized habitat classifications and harmonised Domin scores.
  - Data quality processes, documentation, and versioning facilitate reproducible mapping and time-series analyses.