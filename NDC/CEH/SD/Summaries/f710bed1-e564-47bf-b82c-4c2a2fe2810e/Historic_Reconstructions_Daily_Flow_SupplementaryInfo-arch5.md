# Historic Reconstructions of Daily River Flow for 303 UK Catchments

## Overview
- Provides consistent modelled daily river flow timeseries for 303 UK catchments from 1891 to 2015, including uncertainty estimates.
- Data are produced using the GR4J lumped hydrological model, calibrated with new rainfall data and temperature-derived PET, and presented as:
  - a single flow timeseries with uncertainty bands (upper/lower) and
  - an ensemble flow timeseries from 500 model realizations.

## Data Content and Provenance
- Created as part of the UK Drought and Water Scarcity Programme, through Historic Droughts and IMPETUS projects.
- Inputs:
  - Reconstructed daily rainfall data (1891–1958 extension with recently recovered gauges).
  - Daily PET derived from reconstructed monthly temperatures (McGuinness-Bordne method) to be compatible with UK CHESS climatology.
- Modelling approach:
  - GR4J model (v1.0.2) calibrated over 1982–2014 using 500,000 parameter sets via Bayesian Latin Hypercube Sampling.
  - Multi-objective calibration using six metrics to balance high/median/low flows; calibrations somewhat biased toward low flows due to drought context.
  - Observations from NRFA govern calibration; human influences on flows are not explicitly modelled.

## Data Format and File Organization
- Data organized into two folders:
  - Single_Run: top-ranking ensemble member daily flow files plus one metadata file.
  - Ensemble_500: daily flow files for all 500 ensemble members plus per-catchment metadata files.
- Catchments:
  - 303 catchments; two naturalised calibrations added for Thames at Kingston and Lee at Feildes Weir (NRFA IDs extended with a trailing 0).
- File naming conventions:
  - Single_Run daily files: HD_FlowSingle_<catchmentID>_18910101_20151130.csv
  - Ensemble daily files: HD_FlowEnsemble_<catchmentID>_18910101_20151130.csv
- Data columns (highlights):
  - Single_Run daily files: catchID, Date, Flow_Top_Calib, Min_500, Max_500.
  - Single_Run metadata: catchID, River, Station, Param1–Param4, performance metrics (NSE_Cal, NSElog_Cal, MAPE_Cal, absPBIAS_Cal, MAM30APE_Cal, Q95APE_Cal), Eval_Yrs, NSE_Eval, NSElog_Eval, MAPE_Eval, absPBIAS_Eval, MAM30APE_Eval, Q95APE_Eval, UncertWidth_500, ContRatio_500.
  - Ensemble daily files: Realisation_1_Flow … Realisation_500_Flow (502 columns total per row: catchID, Date, 500 realizations).
  - Ensemble metadata: 500 rows (one per realization) with 22 columns; note UncertWidth_500 and ContRatio_500 are not included in these per-realization metadata files.
- Data range:
  - Daily data from 1891-01-01 to 2015-11-30; 45624 rows per file.

## Metadata, Evaluation and Uncertainty
- Calibration and evaluation:
  - 32-year calibration window (1982-10-01 to 2014-09-30).
  - Evaluation years prior to calibration (vary by catchment); additional metrics computed over the full observed period.
- Uncertainty and ensemble quality:
  - Ensemble width: reported as UncertWidth_500 (calibration+evaluation period).
  - Containment Ratio: percentage of days observations fall within the 500-ensemble min/max range (calibration+evaluation period).
- Metadata provides per-catchment parameters and performance:
  - Top ensemble member parameters (Param1–Param4) and performance (NSE_Cal, NSElog_Cal, MAPE_Cal, absPBIAS_Cal, MAM30APE_Cal, Q95APE_Cal).
  - Evaluation metrics and years of evaluation (Eval_Yrs).
- Guidance notes emphasize variability:
  - Model performance differs across catchments; some catchments poorly reproduce observed flows.
  - Human influences not explicitly modelled; consult metadata to interpret results.

## Input Data and Modelling Approach
- Hydrological model: GR4J (v1.0.2) with four parameters (X1–X4) representing storage and routing characteristics.
- Forcing data:
  - Catchment-averaged rainfall and PET derived from gridded meteorological inputs aligned to NRFA catchment boundaries.
- PET data:
  - Derived from reconstructed monthly temperatures using McGuinness-Bordne equation due to historical data limitations.
- Ensemble construction:
  - 500,000 parameter sets sampled; model runs evaluated against NRFA observations using six metrics; 500 top realizations included in ensemble to capture parameter uncertainty.
- Two naturalised calibrations:
  - Thames at Kingston and Lee at Feildes Weir; NRFA IDs extended with a 0 to denote naturalised flow calibrations.

## Usage and Access Guidance
- The 500-member ensemble provides probabilistic information; single_run is deterministic and suitable for quick reference but does not capture parameter uncertainty.
- Users should consult the per-catchment metadata to understand model performance and applicability for their study catchment.
- The dataset spans 1891–2015; PET and rainfall inputs include an extended early period (1891–1958) with digitised gauge data.
- If resources are limited, the top ensemble member (Single_Run) can be used, but users should be aware of the lack of uncertainty representation.
- Data governance considerations:
  - Acknowledge project provenance (Historic Droughts, IMPETUS) and data sources (NRFA, Met Office CHESS meteorology, UK CHESS dataset).

## Data Governance Considerations for Data Stewards
- Provenance and context:
  - Clear linkage to UK Drought and Water Scarcity Programme projects; two naturalised calibrations provided for increased interpretability.
- Metadata completeness:
  - Comprehensive per-catchment parameter and performance metadata; ensemble-level uncertainty metrics included in Single_Run metadata.
- Interoperability and standards:
  - Uses NRFA catchment IDs; files are CSV with explicit column definitions; naming conventions enable traceability and reproducibility.
- Limitations and caveats:
  - GR4J does not account for human influences on river flows; model performance varies by catchment.
  - Users should select catchments and realizations based on metadata guidance; 500 ensemble members balance coverage and manageability.
- Licensing and citation:
  - Acknowledgements to NERC grants; references provided for underlying methodology and data sources.

## Acknowledgements and References
- Acknowledges NERC UK Droughts and Water Scarcity Programme grants NE/L01016X/1 and NE/L010267/1.
- References include key methodology and data sources for GR4J, PET and rainfall reconstructions, and evaluation frameworks.