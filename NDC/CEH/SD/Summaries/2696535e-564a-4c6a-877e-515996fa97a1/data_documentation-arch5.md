# Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

## Overview
- A data-backed study using high-resolution images of bumblebee specimens from five UK museums to assess wing shape fluctuating asymmetry (FA) as an indicator of environmental stress across the 19th–21st centuries.
- Targets five Bombus species: B. hortorum, B. muscorum, B. lapidarius, B. pascuorum, B. sylvarum; all from Britain.
- Data include specimen labels, geolocated collection sites, wing landmark coordinates, and climate context, enabling analyses of temporal and spatial stress signals.

## Collection and generation methods
- Specimens and images were collected from five museums: Natural History Museum (London), National Museums Scotland, Oxford University Museum of Natural History, Tullie House Museum and Art Gallery, and World Museum (Liverpool).
- For each specimen, left and right forewings were annotated with 13 landmarks using tpsDig2 and tpsUtil; only specimens with both wings landmarked were used.
- Wing shapes were Procrustes-aligned to standardize scale, position, and rotation; FA was estimated as Procrustes distance between left and right wings.
- Location data were enhanced by geocoding collection sites to latitude/longitude where possible. Climate context was derived from UK Met Office historic region data.

## Data processing and quality control
- Data collectors independently landmarked a subset (20 B. hortorum drones) three times to assess repeatability; mixed-effects models showed no significant differences between collectors or repeats.
- Measurement error assessed via Procrustes ANOVA; no significant error detected.
- Quality filtering to include only high-quality wings:
  - Filter based on similarity to mean wing shape (75th percentile cutoff).
  - Filter based on wing angle alignment between left and right wings (75th percentile plus IQR).
- QC notes are documented in the accompanying scripts: 01_Filtering_specimens_generating_FA.R and 03_Repeatability_analysis.R.

## Data contents and file descriptions
- Orientation data (Orientation_species_sex): per-specimen CSVs with ImageID, Wing (left/right), Species, Sex/Caste, Orientation (horizontal/vertical), and Flipped (Y/N).
- FA data with metadata (FA_data_with_metadata_3_3.csv): FA (ProcD) values for five species; includes ImageID, FA, wing angles, coordinates, projID, species ID, sex, caste, decade, collection year/month, latitude/longitude, geotag accuracy, ITD, climate region, and climate-derived variables (temp and rain measures).
- QC-filtered FA data (20210409_updated_dataset.csv): same columns as FA_data_with_metadata_3_3.csv plus additional UK Met Office climate variables (e.g., Raindays1mm_ANN, WinMaxTemp, SprMeanTemp, etc.). Includes queen-cohort labeling (QueenType: early/late) and filtered to higher-quality specimens (no wing shape/angle outliers beyond specified thresholds).
- Subsampled time-series data (Subsampled_FA_Data_0_1_v3.csv): QC-filtered FA data with an aim for even 20th-century temporal coverage; identical column structure to 20210409_updated_dataset.csv with queen exclusions (eclosed prior to collection).
- Data NA convention: missing values indicated as NA in CSVs.

## Metadata, provenance, and ecosystem context
- Provenance data include:
  - Specimen image IDs, wing side, species identity, sex/caste, and collection date/month.
  - Precise crawlable location data (lat/long) and geotagging accuracy.
  - Climate context derived from UK Met Office historic region data across annual and seasonal windows.
  - Anatomical measurements (13 landmarks per wing; Procrustes-aligned shapes; FA as Procrustes distance).
- Documentation notes reference the published manuscript for collection details and data generation pipelines, ensuring traceability of methods and decisions.

## Data quality, limitations, and governance considerations
- Quality control is explicit for the primary FA dataset, but there exists a non-QC’d file (FA_data_with_metadata_3_3.csv) with caveats noted.
- Filtering thresholds (75th percentile cutoffs; wing angle differential limits) balance data quality with sample size, potentially introducing bias toward certain shapes/specimens.
- Temporal coverage is improved in the subsampled file but may still reflect collection biases inherent in museum records.
- Data licensing and portal publishing steps are implied (dataset ready for deposition and cataloguing via appropriate portals), aligning with data stewardship goals of discoverability and reuse.
- The datasets include rich metadata and processing scripts, supporting reproducibility and transparent provenance.

## Implications for data stewardship
- The project provides a well-documented data lineage from specimen collection to FA estimation, with explicit QC steps and metadata richness, enabling reuse across studies of environmental stress signals in pollinators.
- To maximize stewardship outcomes:
  - Maintain versioned releases with clear provenance and change logs, given multiple data files with different QC levels.
  - Preserve and cite accompanying scripts (01_Filtering_specimens_generating_FA.R; 03_Repeatability_analysis.R) and the R geomorph dependency for reproducibility.
  - Ensure metadata completeness (e.g., licensing, data access rights, explicit data use terms) and stable identifiers (ImageID, projID) for tracking.
  - Facilitate deposit in data portals with consistent metadata schemas to support discoverability and interoperability.
  - Consider documenting potential biases due to historical collection practices and spatial-temporal coverage.

## Key takeaways for data stewards
- The dataset demonstrates a rigorous pipeline from specimen imaging to quantitative morphometrics with clear QC and provenance.
- Multiple data products exist at different QC levels, enabling flexible reuse while highlighting the importance of understanding data quality and limitations.
- Comprehensive metadata, climate context integration, and reproducible processing scripts strengthen data usability for future research and governance.