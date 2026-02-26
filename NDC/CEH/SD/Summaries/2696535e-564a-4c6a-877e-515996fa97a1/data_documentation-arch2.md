# Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

- Purpose and scope
  - Investigates long-term environmental stress signals in bumblebees by measuring wing shape fluctuating asymmetry (FA) across five species collected in Britain from the 19th to 21st century.
  - Uses high-resolution specimen imagery and morphometric analysis to produce standardized FA metrics suitable for temporal and spatial comparisons, complemented by climate context.

- Data collection and sources
  - Specimens sourced from five UK museums: Natural History Museum (London), National Museums Scotland, Oxford University Museum of Natural History, Tullie House Museum and Art Gallery, and World Museum (Liverpool).
  - Bumblebee species analyzed: Bombus hortorum, B. muscorum, B. lapidarius, B. pascuorum, B. sylvarum.
  - Data gathered: species labels, collection date, and collection location (transcribed; geolocated to latitude/longitude when possible via Google Maps Geocoding API).
  - Wing data: high-resolution images; left and right forewings manually landmarked with 13 landmarks per wing using tpsDig2 and tpsUtil.

- Morphometrics and analysis
  - Only specimens with both left and right forewings landmarked were used.
  - Wings were Procrustes-aligned to remove scale, position, and rotation differences.
  - Fluctuating asymmetry (FA) quantified as Procrustes distance between left and right wings, computed with the geomorph R package.
  - Orientation and quality checks implemented to ensure consistent landmark placement.

- Quality control and filtering
  - Inter-observer repeatability: two data collectors landmarked a subset (20 B. hortorum drones) thrice; mixed-effects models showed no significant difference between collectors or repeated landmarking.
  - Measurement error: Procrustes ANOVA indicated no significant error.
  - Filtering criteria to retain high-quality wings:
    - Wing shape similarity to species mean within the 75th percentile.
    - Left/right wing angle differences within 75th percentile plus interquartile range.
  - Datasets reflect different QC levels:
    - FA_data_with_metadata_3_3.csv: not QCed beyond initial filtering (only extreme outliers (>3x IQR) filtered from the mean).
    - 20210409_updated_dataset.csv: QCed; retains wings with shape and angle differences within 0 and 1x IQR above the upper quartile.
    - Subsampled_FA_Data_0_1_v3.csv: QCed; subsamples to achieve >20 specimens per year (1900–2000) for even temporal coverage; excludes queens eclosed before collection.

- Data files and contents
  - Orientation_species_sex: contains left/right wing orientation data, including ImageID, wing side, species, sex/caste, orientation (horizontal/vertical), and flipped status.
  - FA_data_with_metadata_3_3.csv: FA (ProcD) and related metrics for five species; includes image ID, wing measurements (L_wing_angle, R_wing_angle, Angle.diff), project ID, species, sex, caste, decade/year, location, latitude/longitude, geolocation accuracy, Intertegular Distance (ITD), climate region, and UK Met Office climate-derived variables (temperatures and precipitation).
  - 20210409_updated_dataset.csv: QCed FA data with added climate context; includes late-year fields like QueenType (early/late cohort) and expanded climate metrics (e.g., Raindays1mm_ANN, WinMaxTemp, SprMeanTemp, etc.).
  - Subsampled_FA_Data_0_1_v3.csv: QCed, temporally even dataset subset; includes same columns as 20210409_updated_dataset.csv with complete location/date/caste data; excludes certain queen flight timing artifacts.
  - Metadata and processing scripts (for QC and repeatability): 01_Filtering_specimens_generating_FA.R and 03_Repeatability_analysis.R.

- Climate and contextual data
  - Climate variables linked to sample collection sites and periods from UK Met Office historic climate region data:
    - Seasonal and annual mean temperatures (temp_WIN, temp_SPR, temp_SUM, temp_AUT, temp_ANN)
    - Seasonal and annual precipitation (rain_WIN, rain_SPR, rain_SUM, rain_AUT, rain_ANN)
  - Additional climate layers added in updated datasets (example: Raindays1mm_ANN, WinMaxTemp/SprMaxTemp/SumMaxTemp/AutMaxTemp, WinMeanTemp/SprMeanTemp/SumMeanTemp/AutMeanTemp, WinMinTemp/SprMinTemp/SumMinTemp/AutMinTemp)
  - Geographic context includes collection location (std_location) and coordinates (lat/long) with accuracy indicators.

- Data generation and stewardship
  - Data collection and processing are documented in the associated manuscript; downstream data handling includes quality assurance, data cleaning, and standardization for comparability over time.
  - Datasets are prepared for storage and sharing through appropriate data portals; emphasis on making underlying data accessible to support transparency and reuse.

- Relevance for environmental analysis
  - Provides a long-term, standardized measure of environmental stress signals in pollinators by linking wing FA to historical climate context.
  - Enables trend analysis across decades and potential correlations with climatic variables, aiding monitoring of environmental health and policy performance over time.
  - The inclusion of multiple QC levels and subsampling supports robust temporal analyses while balancing data quality and coverage.