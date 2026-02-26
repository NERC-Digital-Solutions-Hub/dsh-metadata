# Historic Reconstructions of Daily River Flow for 303 UK Catchments

- This dataset provides consistent modeled daily river flow timeseries for 303 UK catchments from 1891-01-01 to 2015-11-30, including uncertainty estimates.
- Data formats:
  - Single_Run: the top-ranked ensemble member flow with daily uncertainty bounds (Min_500, Max_500) across all catchments.
  - Ensemble_500: daily flows for 500 ensemble realizations per catchment, enabling probabilistic analysis of model parameter uncertainty.
- Two naturalised reconstructions are included (Thames at Kingston and Lee at Feildes Weir) calibrated to naturalised flows (NRFA IDs suffixed accordingly).
- Data for each catchment are accompanied by metadata detailing model parameters and performance.
- The dataset has been used to derive the Standardised Streamflow Index (SSI) and to support drought analyses across the UK.

- Modelling framework:
  - GR4J lumped hydrological model (v1.0.2) used to generate daily flow reconstructions.
  - inputs: catchment-averaged rainfall and potential evapotranspiration (PET).
  - PET derived from reconstructed monthly temperature via the McGuinness-Bordne equation to ensure consistency with UK climada datasets; rainfall data extended from Met Office records (1891-1958) incorporating newly recovered gauges.
  - No snow module (CemaNeige) was used due to computational demands.

- Calibration and uncertainty:
  - Calibration period: 1982-2014 (water-year based).
  - 500,000 model parameter sets sampled with Bayesian Latin Hypercube Sampling; each run evaluated against NRFA observations using six metrics: NSE, NSE on log(Flow), MAPE, PBIAS, MAM30, Q95.
  - Top-ranking model realisations (by multi-metric ranking with acceptable trade-offs) were retained; 500 realizations form the ensemble for uncertainty assessment.
  - Model evaluation extended to pre-1982 observations; additional metrics computed: relative width of uncertainty range and containment ratio (proportion of observed days within ensemble min-max).
  - Performance varies by catchment; some catchments poorly reproduced > users should consult catchment-specific metadata.

- Data quality and guidance:
  - Model calibration does not account for artificial human influences on river flows; catchments differ in degree of anthropogenic impact.
  - Metadata provide catchment-specific performance and parameter values to aid interpretation.
  - Users may subset the ensemble to suit resources; however, the full 500-member ensemble better represents parameter uncertainty and tends to cover a high percentage of observations for most catchments.
  - For some catchments, observed flows are not well captured; consult metadata before applying results to decision-making.

- Data format and access details:
  - Time period: 1891-01-01 to 2015-11-30.
  - Files organized into:
    - Single_Run: 305 daily flow files plus 1 metadata file (HD_FlowSingle_Metadata.csv).
      - File naming: HD_FlowSingle_<catchmentID>_18910101_20151130.csv
      - Columns: catchID, Date, Flow_Top_Calib, Min_500, Max_500
    - Ensemble_500: 305 daily flow files plus 305 metadata files (HD_FlowEnsemble_<catchmentID>_Metadata.csv).
      - File naming: HD_FlowEnsemble_<catchmentID>_18910101_20151130.csv
      - Columns in daily files: catchID, Date, Realisation_1_Flow, ..., Realisation_500_Flow
      - Metadata contains 22 descriptive columns corresponding to the 500 ensemble members (UncertWidth_500 and ContRatio_500 omitted).
  - Catchment metadata (HD_FlowSingle_Metadata.csv) includes:
    - catchID, River, Station, Param1-Param4 (GR4J parameters for top member),
    - Performance metrics for calibration (NSE_Cal, NSElog_Cal, MAPE_Cal, absPBIAS_Cal, MAM30APE_Cal, Q95APE_Cal),
    - Eval_Yrs, NSE_Eval, NSElog_Eval, MAPE_Eval, absPBIAS_Eval, MAM30APE_Eval, Q95APE_Eval,
    - UncertWidth_500, ContRatio_500 (for ensemble assessment across calibration+evaluation period).
  - Additional notes:
    - Some catchments rely on artificial influences not explicitly modelled; interpret results with catchment-specific context in mind.
    - 500 ensemble realizations were chosen to balance uncertainty representation with dataset size.

- Project context and purpose:
  - Part of the UK Droughts and Water Scarcity Programme, covering Historic Droughts and IMPETUS projects.
  - Aims to provide a consistent national flow dataset across periods with sparse gauged observations, enabling drought analysis, SSI calculations, and resource management insights.
  - The work supports long-term monitoring of environmental health and policy performance through standardized hydrological reconstructions.

- Acknowledgements and references:
  - Funded by NERC (Historic Droughts: NE/L01016X/1; IMPETUS: NE/L010267/1).
  - References include methodological details on GR4J, PET/rainfall inputs, and drought indices used in downstream analyses.