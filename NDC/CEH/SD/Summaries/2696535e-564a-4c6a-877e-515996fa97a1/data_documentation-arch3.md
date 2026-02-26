# Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

- Purpose and scope
  - Investigates whether bumblebee wing morphology shows signatures of environmental stress over the past century using museum specimens from five UK institutions.
  - Focuses on five Bombus species and uses wing shape fluctuation asymmetry as a metric.

- Collection and generation methods
  - Source material: high-resolution images of bumblebee specimens and label data from Natural History Museum (London), National Museums Scotland, Oxford University Museum of Natural History, Tullie House Museum and Art Gallery, and World Museum (Liverpool).
  - Timeframe: specimens collected in Britain between the 19th and 21st centuries.
  - Data captured: for each specimen, label data (location, date) and wing images.
  - Geolocation: where possible, specimen collection locations were geocoded to latitude/longitude via Google Maps Geocoding API.
  - Morphometrics: left and right forewings were annotated with 13 landmarks per wing using tpsDig2/tpsUtil; only specimens with both wings landmarked were analyzed.
  - Alignment and analysis: wings were Procrustes-aligned to standardize scale, location, and rotation; fluctuating asymmetry (FA) was quantified as Procrustes distance using the geomorph package in R.

- Quality control and data curation
  - Inter- and intra-operator reliability: two data collectors landmarked a subset thrice; mixed-effects models showed no significant differences between collectors or repeated landmarking.
  - Measurement error: Procrustes ANOVA indicated no significant measurement error.
  - specimen filtering: retained specimens with wing shapes close to the species mean and with similar wing angles between left and right wings; filtering thresholds set at the 75th percentile for wing shape and wing-angle differential (plus IQR where specified).
  - Datasets reflect quality-controlled subsets or notes on quality status (see data files below).

- Datasets and data descriptions
  - FA_data_with_metadata_3_3.csv
    - Content: FA (ProcD), wing angles (left/right), angle difference, project ID, species, sex/caste, collection date/location, latitude/longitude, geotag accuracy, intertegular distance, climate data (from UK Met Office), and various climate/seasonal fields.
    - Quality: FA values not QC’d in this file; includes broader metadata for context.
  - 20210409_updated_dataset.csv
    - Content: QC’d dataset where specimens with wing shape or wing-angle differences beyond 0 and 1×IQR above the upper quartile were included; adds extensive climate variables (annual/seasonal temperatures, precipitation, etc.).
    - Notable additions: QueenType (early/late cohort) for some entries; geocoding details and climate region variables.
  - Subsampled_FA_Data_0_1_v3.csv
    - Content: QC’d dataset with the same core fields as 20210409_updated_dataset.csv but subsampled to ensure >20 specimens per year across 1900–2000 for even temporal coverage; excludes queens potentially eclosing before collection.
  - 20210409_updated_dataset.csv, Subsampled_FA_Data_0_1_v3.csv
    - Both contain standardized fields including ImageID, FA measure (ProcD), wing angles, location, date, species, sex/caste, climate variables, and geolocation accuracy.
  - NA handling: missing data represented as NA in CSVs.

- Data governance, accessibility, and metadata
  - Metadata richness: location, date, geocoordinates, wing angles, FA metrics, and climate context are provided to support downstream monitoring analyses.
  - Data sharing and openness: underlying data and provenance are documented; some analyses note that certain datasets have not undergone quality control (e.g., FA_data_with_metadata_3_3.csv), while others are QC’d (e.g., 20210409_updated_dataset.csv, Subsampled_FA_Data_0_1_v3.csv).
  - Data transformation: wing shapes required alignment (Procrustes) and computation of FA; multiple QC steps ensure comparability across specimens and time periods.

- Relevance to monitoring frameworks
  - Demonstrates a workflow for long-term environmental health indicators using archival biology and morphometrics.
  - Highlights key monitoring considerations:
    - Importance of standardized metadata (species, sex/caste, collection date/location, geolocation accuracy).
    - Necessity of rigorous quality control (inter-rater reliability, measurement error, and filtering criteria) to ensure data suitability for policy-relevant analyses.
    - Value of linking biological traits to climate data (regional UK Met Office climate variables) to contextualize stress signals.
    - Trade-offs between data completeness and temporal coverage (e.g., subsampling to achieve even representation across the 20th century).
    - Clear documentation of data provenance and QC status to facilitate transparent decision-making and reproducibility.
  - Indicates potential barriers for monitoring frameworks: incomplete metadata, varying data quality across datasets, and the need for consistent data governance to enable open sharing and reuse.

- Practical implications for policy and decision-making
  - Long-term museum-based morphometric data can illuminate trends in environmental stress and inform adaptive management decisions.
  - Embedding QC, metadata standards, and clear data provenance in monitoring projects enhances credibility and usability for policy evaluation.
  - Integration with climate-context variables enables policymakers to assess correlations between environmental stress signals and climatic factors, supporting evidence-based interventions.