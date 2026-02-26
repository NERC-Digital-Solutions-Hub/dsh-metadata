# Supporting information for Random forest model to predict long-term seasonal nitrate and orthophosphate concentrations in British river reaches

## Overview
- Provides notebooks and data to support a study on river reach-level nutrient estimation in Great Britain using random forest models.
- Two nearly identical notebooks (one for nitrate, one for orthophosphate) train models on observed seasonal readings to predict concentrations at each GB river reach.
- Process: train with all features to derive importances, then retrain with a selected subset of features.

## Data sources and inputs
- Environmental Agency (EA) Water Quality Archive readings used as targets:
  - nitrate_readings.csv (seasonal, log-transformed nitrate, 2010–2020)
  - orthophosphate_readings.csv (seasonal, log-transformed orthophosphate, 2010–2020)
  - Columns include SITE_ID (EA site), SEASON, RESULT (log-transformed seasonal average)
- Feature data matched to the UKCEH digital river network:
  - training_features.csv contains EA site_id, river reach OBJECTID, and a large set of FEH catchment descriptors and Land Cover Map 2015 fractions.
  - reaches_no_na.csv includes river reaches for GB with no missing values, formatted identically to training_features.csv (used for predictions).
- File list:
  - nitrate_model_for_the_paper_including_feat_selection.ipynb
  - orthophosphate_model_for_the_paper_including_feat_selection.ipynb
  - nitrate_readings.csv
  - orthophosphate_readings.csv
  - training_features.csv
  - reaches_no_na.csv
- Note: The digital UKCEH river network is not included in this submission due to licensing (EIDC).

## Modeling approach
- Random Forest models trained separately for nitrate and orthophosphate at river-reach scale.
- Training workflow:
  - Step 1: train with all features to obtain feature importances.
  - Step 2: train a final model using only the selected (feature-importances-based) features.
- Targets are the log-transformed seasonal concentrations (2010–2020).
- Outputs are predictions that can be mapped back onto the river network for visualization and further analysis.

## Features and data preparation
- Features are derived by matching gridded FEH catchment descriptors and Land Cover Map 2015 data to the UKCEH digital river network.
- Example features (as listed in training_features.csv) cover:
  - FEH descriptors (e.g., CCAR, HGHT, QALT, QASB, QASV, QB19, QBFI, QDPB, QDPS, QFAR, QFPD, QFPX, QLDP, QPRW, PROPWET, QR1D/QR1H/QR2D, QS47/QS69, QSPR, etc.)
  - Land cover fractions (e.g., ARABLE AND HORTICULTURE, COASTAL, GRASSLAND, HEATH/BOG, INLAND ROCK, URBAN, WATER, WOODLAND, plus UNKNOWN)
  - Various auxiliary descriptors related to catchment geometry, hydrology, and urbanization
- Each row in reaches_no_na.csv represents a GB river reach with no NA values, suitable for predictions.

## Outputs and visualization
- Model predictions are designed to be mapped onto the GB river network for visualization and post-analysis.
- The workflow enables assessment of long-term nutrient concentrations at river reaches, supporting decision-making and environmental planning.

## Reproducibility and licensing
- Two notebooks are essentially identical in structure; one handles nitrate, the other handles orthophosphate.
- The network data itself is not included due to licensing; external datasets and licenses are linked in the documentation.
- Useful references and data sources are provided to facilitate replication, including FEH descriptors, Land Cover Map 2015, and EA Water Quality Archive.

## Useful links
- UKCEH digital river network of Great Britain (1:50,000)
- Land Cover Map 2015 (1km)
- FEH catchment descriptors (NRFA/FEH)
- Environmental Agency Water Quality Archive
- Additional workflow and dataset context available in the notebooks and accompanying paper:
  Tso C.-H.M., Magee, Huxley, Eastman, Fry (2023) River reach-level machine learning estimation of nutrient concentrations in Great Britain. Frontiers in Water.