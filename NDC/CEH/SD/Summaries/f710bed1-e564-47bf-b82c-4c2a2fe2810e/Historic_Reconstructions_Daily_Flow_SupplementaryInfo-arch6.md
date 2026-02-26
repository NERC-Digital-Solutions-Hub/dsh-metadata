# Historic Reconstructions of Daily River Flow for 303 UK Catchments

## What the dataset contains
- Consistent modelled daily river flow timeseries for 303 UK catchments from 1891-01-01 to 2011-11-30 (reported as 2015-11-30 in some files; see metadata for scope), with uncertainty estimates.
- Two data forms:
  - Single Run: the best-performing single flow timeseries plus upper/lower uncertainty bands.
  - Ensemble 500: daily flow timeseries from 500 model realizations (ensemble members).
- Metadata and guidance:
  - A metadata file per catchment (or per catchment with naturalised calibrations) detailing model parameters and performance.
  - Guidance notes emphasize variability in performance across catchments and the need to consult metadata for interpretation.
- Catchments and context:
  - 303 catchments; some near-natural, some influenced by human activity (abstraction, regulation).
  - Two naturalised calibrations for the Thames at Kingston and the Lee at Feildes Weir.

## Modelling and calibration approach
- Hydrological model: GR4J lumped catchment model (v1.0.2) with four parameters (X1-X4).
- Calibration period: 1982-10-01 to 2014-09-30 (32 water years).
- Parameter uncertainty: 500,000 model realizations sampled via Bayesian Latin Hypercube Sampling.
- Multi-objective calibration using six metrics:
  - Nash Sutcliffe Efficiency (NSE)
  - NSE on log-transformed flows (log NSE)
  - Mean Absolute Percent Error (MAPE)
  - Absolute Percent Bias (PBIAS)
  - Absolute Percent Error in Mean Annual Minimum flows over 30 days (MAM30)
  - Absolute Percent Error in the 95th percentile flow (Q95)
- Top-ranking realizations selected per catchment to form the ensemble; later, 500 realizations retained to characterize parameter uncertainty.

## Input data and drivers
- Meteorological inputs required by GR4J:
  - Rainfall: reconstructed daily rainfall data. Extended dataset for 1891-1958 with newly recovered digitised gauges.
  - Potential Evapotranspiration (PET): derived daily PET from reconstructed monthly temperatures using McGuinness-Bordne method (to maintain consistency with UK CHESS dataset) due to lack of daily PET in early period.
- Meteorological data sources:
  - UK Met Office reconstructions for rainfall and temperature-derived PET; catchment-averaged inputs mapped from gridded datasets using National River Flow Archive (NRFA) boundaries.

## Catchment selection and data scope
- 303 UK catchments chosen to cover a wide range of hydrology.
- 115 catchments are part of the UK Benchmark Network (near-natural, low-flow suitability); others included for historical research continuity.
- Some catchments are heavily influenced by human activity; two naturalised calibrations provided for specific catchments (Thames Kingston, Lee Feildes Weir).
- A full list of gauging stations is included in the Single_Run metadata.

## Data formats and access

- Common base period: 1891-01-01 to 2015-11-30 (file content reflects this span; see metadata for exact periods per catchment).
- Single_Run folder
  - 305 daily flow files for top-ranked ensemble member plus 1 metadata file: HD_FlowSingle_<catchmentID>_18910101_20151130.csv
  - File columns: catchID, Date (YYYY-MM-DD), Flow_Top_Calib (top ensemble member), Min_500 (min of 500 ensemble members), Max_500 (max of 500 ensemble members)
  - Metadata file: HD_FlowSingle_Metadata.csv with 305 rows and 23 columns:
    - catchID, River, Station
    - Param1–Param4 (GR4J parameters for top member)
    - Thresh_Met and NSE_Cal, NSElog_Cal, MAPE_Cal, absPBIAS_Cal, MAM30APE_Cal, Q95APE_Cal
    - Eval_Yrs, NSE_Eval, NSElog_Eval, MAPE_Eval, absPBIAS_Eval, MAM30APE_Eval, Q95APE_Eval
    - UncertWidth_500, ContRatio_500
- Ensemble_500 folder
  - 305 daily flow files for all 500 ensemble members plus 305 metadata files: HD_FlowEnsemble_<catchmentID>_18910101_20151130.csv
  - Daily file columns: catchID, Date, Realisation_1_Flow, Realisation_2_Flow, ..., Realisation_500_Flow
  - Metadata files: HD_FlowEnsemble_<catchmentID>_Metadata.csv with 500 rows (one per ensemble member) and 22 columns (Param1–Param4, performance metrics, etc.). Note: UncertWidth_500 and ContRatio_500 omitted in ensemble metadata.
- Guidance notes
  - 500 realizations were chosen to balance uncertainty estimation with data size; users may subset the ensemble as needed.
  - Some catchments may show substantial artificial influence on flows; GR4J is calibrated to observations but does not explicitly model these human effects.
  - For resource-limited use, the Single_Run top member provides a deterministic output, but does not reflect parameter uncertainty; the full ensemble provides probabilistic context.

## Guidance for use and interpretation
- Always consult catchment-specific metadata to assess model performance and suitability for your analysis.
- Use the ensemble to assess parameter uncertainty and the robustness of inferred hydrological signals; uncertainty bands (Min_500 to Max_500) illustrate the spread across 500 realizations.
- Be aware that model bias toward low flows exists due to the UK Drought and Water Scarcity Programme calibration focus.
- The GR4J model does not explicitly account for human influences; interpret results with knowledge of catchment-level management and modifications.
- If computational resources are limited, the top-ranked Single_Run member is available, but it does not quantify uncertainty.

## Use cases and outputs for data support
- Reconstructing historical river flows to study droughts, water resource planning, and hydrological drought indicators (e.g., for SSI-type analyses).
- Comparing observed vs. reconstructed flows across catchments to understand regional hydrology and data reliability.
- Exploring uncertainty due to parameterization through the 500-member ensemble.

## Acknowledgements and references
- Funded by NERC UK Droughts and Water Scarcity Programme (Historic Droughts and IMPETUS projects) and collaborators across multiple UK institutions.
- Key references include methodological and data-context sources on GR4J, PET/rainfall reconstructions, and drought indices.