# Supporting information for Random forest model to predict long-term seasonal nitrate and orthophosphate concentrations in British river reaches

## Overview
- Describes model resources and data for two random forest models predicting seasonal nitrate and orthophosphate concentrations at Great Britain river reaches.
- Two Jupyter notebooks (nitrate and orthophosphate) train models, identify feature importances, then retrain with a selected feature set.
- Outputs map predictions onto the GB river network; the digital river network dataset itself is not included due to licensing (EIDC).
- Timeframe and data scope: seasonal readings aggregated 2010–2020 from the Environmental Agency Water Quality Archive; features derived by linking FEH catchment descriptors and Land Cover Map 2015 to the UKCEH digital river network.

## Data assets and structure
- Notebooks:
  - nitrate_model_for_the_paper_including_feat_selection.ipynb
  - orthophosphate_model_for_the_paper_including_feat_selection.ipynb
- Data files:
  - nitrate_readings.csv: aggregated, log-transformed seasonal nitrate readings (EA, seasons Spring/Summer/Autumn/Winter, 2010–2020)
  - orthophosphate_readings.csv: aggregated, log-transformed seasonal orthophosphate readings (EA, seasons Spring/Summer/Autumn/Winter, 2010–2020)
  - training_features.csv: features matched to all river reaches; columns include site_id (EA site), OBJECTID (river reach), and numerous descriptors (FEH catchment descriptors and Land Cover Map 2015 fractions)
  - reaches_no_na.csv: river reaches with no missing values; same feature structure as training_features.csv; used for model predictions
- Feature set details:
  - Examples of features: CCAR, HGHT, QALT, QASB, QASV, QB19, QBFI, QDPB, QDPS, QFAR, QFPD, QFPL, QLDP, QPRW, QR1D/QR1H/QR2D, QS47, QS69, QSPR, various urban/land cover indicators (UC2/UE2, ARABLE/HORTICULTURE, COASTAL, GRASSLAND, HEATH/BOG, INLAND ROCK, URBAN, WATER, WOODLAND)
  - Relationships: input features derived by matching gridded datasets (FEH catchment characteristics and land cover fractions) to the UKCEH digital river network; each water quality reading is matched to a river reach.
- Data provenance:
  - Readings from EA Water Quality Archive (seasonal, 2010–2020)
  - Land cover data from Land Cover Map 2015
  - FEH catchment descriptors from National River Flow Archive resources
  - UKCEH digital river network (not included in this submission; license restricted)

## Data provenance, quality, and governance
- Data lineage is well-documented: readings linked to river reaches; features derived from standardized environmental datasets.
- Quality control indicators are not provided in the submission (N/A for quality control sections).
- Licensing and access considerations:
  - The core digital river network dataset is licensed by EIDC and not included here.
  - External data sources (EA Water Quality Archive, FEH descriptors, Land Cover Map 2015) have their own licensing terms and are cited for reproducibility.
- Documentation of data structure and mappings aids traceability for data stewards: explicit mapping of site_id to river reach (OBJECTID/STATION), and detailed feature column explanations.

## Access, licensing, and sharing considerations for Data Stewards
- Sharing: present as notebooks and CSVs within this submission; external river network data not included due to license constraints.
- Licensing notes: respect for external data licenses (EIDC for the river network; FEH, Land Cover Map 2015, EA Water Quality Archive have separate terms).
- Metadata and discoverability:
  - Clear definitions of input features, units, and data sources; records link to the corresponding data catalogs.
  - Useful links provided for underlying datasets (UKCEH river network, Land Cover Map 2015, FEH catchment descriptors, EA Water Quality Archive).

## Reproducibility and practical use
- Reproducibility:
  - Two-stage modeling approach: train on all features to obtain importances, then train final model with selected features.
  - Predictions are designed to be mappable onto the GB river network for visualization and downstream analysis.
- Practical usage for data custodians:
  - Ensure access to external datasets (EIDC river network, FEH descriptors, Land Cover Map 2015, EA Water Quality Archive) per licenses.
  - Maintain provenance links to source datasets and document any feature selection criteria or changes in feature definitions.
  - Consider updates with more recent readings and network data as licenses permit.

## Useful references and links
- UKCEH digital river network of Great Britain (1:50,000): https://catalogue.ceh.ac.uk/documents/7d5e42b6-7729-46c8-99e9-f9e4efddde1d
- Land Cover Map 2015 (1km, GB): https://doi.org/10.5285/7115bc48-3ab0-475d-84ae-fd3126c20984
- National River Flow Archive – FEH catchment descriptors: https://nrfa.ceh.ac.uk/feh-catchment-descriptors
- Environmental Agency Water Quality Archive: https://environment.data.gov.uk/water-quality/view/landing