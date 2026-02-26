# Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens

## Overview
- A data-centric study built from high-resolution images of bumblebee specimens housed in five UK museums, spanning Britain collections from the 19th to the 21st century.
- Focuses on wing morphology as a potential proxy for environmental stress, quantified as fluctuating asymmetry (FA) between left and right forewings.
- Wing shapes are characterized by 13 manually plotted landmarks per wing; analyses use Procrustes alignment and the Procrustes distance to measure FA via the geomorph package in R.
- The dataset integrates specimen metadata, geographic information, and climate variables to enable spatial and temporal analyses.

## Data collection and processing
- Specimens and labels sourced from five museums: Natural History Museum (London), National Museums Scotland, Oxford University Museum of Natural History, Tullie House Museum and Art Gallery, and World Museum (Liverpool).
- Target species: Bombus hortorum, B. muscorum, B. lapidarius, B. pascuorum, B. sylvarum.
- Specimens collected in Britain between the 19th and 21st centuries.
- Location data were transcribed from labels and geocoded to latitude/longitude using Google Maps Geocoding API where possible.
- For each specimen, both left and right forewings were landmarked (13 landmarks per wing) using tpsDig2 and tpsUtil64; only specimens with both wings landmarked were included.
- Wings were Procrustes-aligned to standardize scale, location, and rotation; FA was estimated as Procrustes distance between wings.
- Orientation data were compiled for each wing (left/right), including orientation (horizontal/vertical) and whether the wing was flipped.

## Quality control
- Repeatability: two data collectors landmarked a subset (20 B. hortorum drones) three times; mixed-effects models showed no significant differences between collectors or repetitions.
- Measurement error: Procrustes ANOVA indicated no significant measurement error.
- Filtering criteria to ensure high-quality wings: specimens must be close to the species mean wing shape and have similar left-right wing angles. Wing angle difference was computed from landmark coordinates (absolute difference between corresponding wing angles).
- Filtering thresholds: based on the 75th percentile for wing shape and wing angle, with 75th percentile plus the interquartile range applied to wing data (as detailed in updated datasets).

## Datasets and key fields
- Orientation_species_sex
  - Per-specimen, per-wing records with fields: ImageID, Wing (left/right), Species, Caste/Sex, Orientation (horizontal/vertical), Flipped (Y/N), etc.
- FA_data_with_metadata_3_3.csv
  - FA values and accompanying metadata: ImageID, Procrustes distance (ProcD), L_wing_angle, R_wing_angle, Angle.diff, projID, sample_species_ID, sex, caste, decade, sample_collected_curated, month, climate_region (UK Met Office), std_location, lat, long, accuracy, ITD; climate variables (temp_Ann, temp_Win, temp_SPR, temp_SUM, temp_AUT; rain_Ann, rain_Win, rain_SPR, rain_SUM, rain_AUT).
- 20210409_updated_dataset.csv
  - Same structure as above with quality-control filters applied: wing shape and wing-angle differences > 0 and > 1×IQR above upper quartile; includes queen cohort field QueenType (early/late) indicating emergence relative to collection year; expanded climate variables (Raindays1mm_ANN/WIN/SPR/SUM/AUT and various Temp/Rain statistics).
- Subsampled_FA_Data_0_1_v3.csv
  - Quality-controlled subset with the same columns as 20210409_updated_dataset.csv; temporal stratification to >20 specimens per year between 1900–2000; complete location/date/caste data; queens excluded if eclosed before collection.

## Geospatial and climate context
- Geospatial data include lat/long coordinates and geotagging accuracy for each specimen.
- Climate variables derived from UK Met Office historic climate region data accompany each specimen (seasonal and annual temperatures and precipitation; also included are more detailed climate metrics in updated datasets).

## How the data support GIS analysis
- Enables spatial mapping of wing FA across regions and decades, facilitating exploration of environmental stress signals.
- Supports correlation analyses between FA and climate metrics (temperature, precipitation, rain days) by species, sex, and time period.
- Multi-layer GIS visualization: specimen locations, species distribution, climate layers, and time dimension (decades).

## Usage considerations and limitations
- Data are historical and derived from museum collections; potential sampling biases across time and space.
- Coordinate accuracy varies by source; metadata includes geotagging accuracy to inform GIS analyses.
- Data filtering reduces sample sizes but improves reliability of FA estimates; users should consider filtering criteria when replicating analyses.

## provenance and references
- Primary data provenance from the manuscript: Arce, Cantwell-Jones, et al., “Signatures of increasing environmental stress in bumblebee wings over the past century: Insights from museum specimens.”
- Quality-control scripts referenced: 01_Filtering_specimens_generating_FA.R and 03_Repeatability_analysis.R.
- Updated datasets provide enhanced filtering and expanded climate metrics (20210409_updated_dataset.csv and Subsampled_FA_Data_0_1_v3.csv).