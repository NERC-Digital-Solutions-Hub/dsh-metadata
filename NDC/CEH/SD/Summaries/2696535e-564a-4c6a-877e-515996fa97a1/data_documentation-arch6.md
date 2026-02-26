# Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

## Overview
- A study of wing shape fluctuating asymmetry (FA) in five bumblebee species collected in Britain from the 19th to 21st centuries.
- Uses high-resolution specimen images, wing landmarking, and climate data to explore environmental stress over time.
- Data are stored in multiple CSV files with detailed metadata and climate variables; missing values are marked as NA.

## Data collection sources and scope
- Specimens and label data sourced from five UK museums: Natural History Museum (London), National Museums Scotland, Oxford University Museum of Natural History, Tullie House Museum and Art Gallery, and World Museum (Liverpool).
- Bumblebee species: Bombus hortorum, B. muscorum, B. lapidarius, B. pascuorum, B. sylvarum.
- Time frame: specimens collected in Britain across the 19th to 21st centuries.
- Location data: specimen collection locations transcribed; where possible, latitude/longitude assigned via Google Maps Geocoding API.

## Data processing and wing morphology metrics
- Wing geometry: thirteen landmarks plotted on each forewing (left and right) to capture venation patterns.
- Only specimens with both left and right forewings landmarked were analyzed.
- Wing alignment: Procrustes alignment to standardize scale, position, and orientation.
- FA metric: fluctuating asymmetry quantified as Procrustes distance between left and right wings after alignment.
- Software: geomorph package in R used for FA calculations.

## Quality control and filtering
- Inter-observer reliability: two data collectors landmarked a subset (20 B. hortorum drones) thrice; mixed-effects models showed no significant differences.
- Measurement error: wings landmarked twice per specimen; Procrustes ANOVA indicated no significant error.
- Filtering criteria for high-quality wings: keep specimens with wing shape close to species mean and with similar wing angles.
  - Filtering thresholds based on percentiles; final datasets use 75th percentile cut-offs for wing shape and wing angle differential.
- Datasets note: multiple QC states exist across files, with progressive tightening of quality criteria.

## Datasets and fields
- FA_data_with_metadata_3_3.csv
  - FA measure: ProcD (wing shape FA), L_wing_angle, R_wing_angle, Angle.diff.
  - Metadata: ImageID, projID, sample_species_ID, sex, caste, decade, sample_collected_curated, month.
  - Location and geography: climate_region, std_location, lat, long, accuracy.
  - Physical measurements: ITD (intertegular distance).
  - Climate data: temp_WIN, temp_SPR, temp_SUM, temp_AUT, temp_ANN; rain_WIN, rain_SPR, rain_SUM, rain_AUT, rain_ANN.
- 20210409_updated_dataset.csv
  - Same core columns as above, with additional UK Met Office climate variables:
    - Raindays1mm_ANN, Raindays1mm_WIN, Raindays1mm_SPR, Raindays1mm_SUM, Raindays1mm_AUT.
    - AnnMaxTemp, WinMaxTemp, SprMaxTemp, SumMaxTemp, AutMaxTemp.
    - AnnMeanTemp, WinMeanTemp, SprMeanTemp, SumMeanTemp, AutMeanTemp.
    - AnnMinTemp, WinMinTemp, SprMinTemp, SumMinTemp, AutMinTemp.
- Subsampled_FA_Data_0_1_v3.csv
  - Same structure as 20210409_updated_dataset.csv (QCed data).
  - Temporal subsampling: >20 specimens per year between 1900 and 2000 to ensure even coverage.
  - Additional constraints: complete location/date/caste data; exclusion of queens eclosing the year prior to collection.
- Orientation data (Orientation_species_sex)
  - Per-species and sex CSVs detailing wing orientation.
  - Fields include ImageID, Wing (Left/Right), Species, Caste, Orientation (horizontal/vertical), Flipped (Y/N).
- Notes on missing data
  - NA indicates Not Available; users should account for gaps in FA, wing angles, location, climate, or other metadata.

## Data quality notes and caveats
- Data collection depends on museum records and may reflect collection biases over time.
- Climate variables are derived from UK Met Office historic data and linked to sample locations/periods.
- While FA is a robust proxy for developmental/stress-related perturbations, interpretation should consider potential non-environmental sources of wing asymmetry.

## Temporal and geographic coverage
- Geographic scope: Britain across multiple sites represented in five museums.
- Temporal scope: specimens from the 19th through the 21st centuries, with specific datasets designed to support even temporal coverage (1900–2000 in subsampled data).

## Access and data handling guidance
- The CSV files provide a rich, multi-dimensional dataset suitable for analyses linking wing FA to environmental variables.
- When using the data, account for missing values (NA), apply the QC-enabled subset for robust analyses, and reference the accompanying metadata for proper interpretation of each variable.
- For methodological details and data provenance, refer to the associated manuscript: "Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens" (Arce & Cantwell-Jones et al.).