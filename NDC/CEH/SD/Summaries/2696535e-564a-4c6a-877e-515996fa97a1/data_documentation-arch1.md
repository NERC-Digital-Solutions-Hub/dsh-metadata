Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

## Overview
- Study uses high-resolution images of bumblebee specimens from five UK museums (Natural History Museum London; National Museums Scotland; Oxford University Museum of Natural History; Tullie House Museum and Art Gallery; World Museum, Liverpool).
- Species include Bombus hortorum, B. muscorum, B. lapidarius, B. pascuorum, and B. sylvarum; specimens collected in Britain across 19th–21st centuries.
- Wing shapes are quantified via 13 landmarks on each forewing, with left and right wings analyzed after Procrustes alignment to measure fluctuating asymmetry (FA) as Procrustes distance.
- Location data derived from specimen labels and geocoded where possible; climate data linked to collection sites using UK Met Office historic climate regions.

## Data collection and processing
- For each specimen, both left and right forewings were landmarked; only specimens with both wings landmarked were used.
- Wing shapes aligned for scale, location, and rotation (Procrustes alignment); FA calculated from landmark positions.
- Quality control includes cross-checks on landmarking consistency and measurement error.

## Data quality control
- Two main data collectors landmarked a subset (20 B. hortorum drones) three times; mixed-effects models showed no significant inter-collector differences.
- Procrustes ANOVA indicated no significant measurement error.
- Filtering to ensure high-quality wings:
  - Wing shapes filtered to be within the 75th percentile of species mean similarity.
  - Wing angle differential between left and right wings constrained to the 75th percentile plus the interquartile range.
- Specific QC scripts referenced (01_Filtering_specimens_generating_FA.R; 03_Repeatability_analysis.R).

## Data files and contents
- Orientation_species_sex
  - For each species and sex, contains ImageID, Wing (left/right), Species, Caste, Orientation (horizontal/vertical), Flipped (Y/N).

- FA_data_with_metadata_3_3.csv
  - FA measures (ProcD) and wing angles: ImageID, ProcD, L_wing_angle, R_wing_angle, Angle.diff, projID.
  - Metadata: sample_species_ID, sex, caste, decade, sample_collected_curated, month, climate_region, std_location, lat, long, accuracy, ITD.
  - Climate data fields: temp_WIN, temp_SPR, temp_SUM, temp_AUT, temp_ANN; rain_WIN, rain_SPR, rain_SUM, rain_AUT, rain_ANN.

- 20210409_updated_dataset.csv
  - Same core structure as FA_data_with_metadata_3_3.csv, but with QC threshold updates.
  - Additional climate variables appended: Raindays1mm_ANN, Raindays1mm_WIN, Raindays1mm_SPR, Raindays1mm_SUM, Raindays1mm_AUT.
  - Max/Mean/Min temperature fields: WinMaxTemp, SprMaxTemp, SumMaxTemp, AutMaxTemp; WinMeanTemp, SprMeanTemp, SumMeanTemp, AutMeanTemp; WinMinTemp, SprMinTemp, SumMinTemp, AutMinTemp.
  - Queen-type cohorts added (early/late) for queen bumblebees.

- Subsampled_FA_Data_0_1_v3.csv
  - QC-filtered FA data with similar columns to 20210409_updated_dataset.csv.
  - Temporal subsampling to ensure >20 specimens per year from 1900–2000; complete data for location, date, and caste; queens that may have eclosed prior to collection excluded.

- Data notes
  - NA indicates Not Available data.
  - Dataset includes ImageID, coordinates (lat/long), geotag accuracy, and climate-region-derived environmental variables.

## Filtering criteria and temporal/geographic coverage
- Quality filtering implemented to balance data quality and sample size:
  - 75th percentile cut-off for wing shape similarity to species mean.
  - 75th percentile plus interquartile range cut-off for wing angle difference between wings.
- Subsampling (Subsampled_FA_Data_0_1_v3.csv) achieves even temporal coverage (1900–2000) with >20 specimens per year; excludes certain queen phenology (early/late cohorts) to standardize temporal signals.

## Data usage and applicability
- Data enables analysis of how wing shape fluctuating asymmetry (FA) relates to environmental stress indicators over roughly the last century.
- Coupled wing FA data with climate variables (temperature and precipitation across seasons and annually) to explore potential correlations between environmental stress and phenotypic asymmetry.
- Geo-located data allow regional analyses within the UK, with metadata to support reproducibility and cross-study comparability.

## Limitations and considerations
- Some data points contain missing values (NA), requiring careful handling in analyses.
- Climate data derive from historic climate regions, which may introduce spatial resolution limitations relative to exact collection localities.
- Only specimens with both forewings landmarked and meeting quality criteria were retained, potentially reducing sample size for certain species or time periods.
- Data interpretation requires consideration of potential biases from museum sampling, collection effort, and taxonomic changes over time.