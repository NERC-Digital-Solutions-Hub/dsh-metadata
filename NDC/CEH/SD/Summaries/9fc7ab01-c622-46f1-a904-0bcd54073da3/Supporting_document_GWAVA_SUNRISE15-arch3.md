# GWAVA Modelling- SUNRISE1.5

- Overview
  - GWAVA is a large-scale, semi-distributed gridded water resources model developed by the UK Centre for Ecology & Hydrology.
  - It integrates natural processes and anthropogenic stresses to estimate local runoff and water availability, used here for the Upper Narmada Basin.
  - The model supports demand-driven management across domestic, industrial, agricultural sectors, with dynamic irrigation and crop-type/planting-month inputs.
  - Spatial resolution is 0.125 degree, with the Upper Narmada modeled as 318 cells and the entire Narmada as 653 cells, including reservoirs, transfers, and rural/command area irrigation.

- Model Setup
  - Structure comprises three components: probability-distributed soil moisture storage, surface storage, and groundwater storage, plus a demand-driven routine for anthropogenic stresses.
  - Domestic and livestock demands are user-defined and spatially dynamic; irrigation demand is both spatially and temporally dynamic.
  - The dataset includes major water use sectors and infrastructure within command and rural areas.

- Future Projections
  - An ensemble climate dataset under CMIP6 (and related CMIP outputs) is used to represent future climate for GWAVA runs.
  - Climate models listed include a wide range of modelling centres (e.g., CSIRO/BOM, BOM, Beijing Normal University, Canadian Centre for Climate Modelling and Analysis, NCAR, Centre National de Recherches Météorologiques, Max Planck, NOAA GFDL, Institut Pierre-Simon Laplace, and others).
  - Scenarios cover:
    - 2028–2060 climate runs for Upper Narmada (Upper_Narmada_Climate_2028_2060) using multiple models.
    - 2021–2099 future runs under RCP4.5 and RCP8.5 (Narmada_climate_45_totQ_2021_2099, Narmada_climate_85_totQ_2021_2099) and corresponding aquifer level files (Narmada_climate_45_aqlevel_2021_2099, Narmada_climate_85_aqlevel_2021_2099).
    - Paddy substitution scenarios replacing wheat with paddy for the future period (Narmada_climate_paddy_45_totQ_2021_2099, Narmada_climate_paddy_85_totQ_2021_2099) and identical aquifer-paddy variants (Narmada_climate_paddy_45_aqlevel_2021_2099, Narmada_climate_paddy_85_aqlevel_2021_2099).

- Quality Control
  - Model calibration at 13 gauging stations across the basin using the SIMPLEX auto-calibration routine.
  - Four calibration/transfer parameters used: surface and groundwater routing, PDM soil-moisture capacity variation, and a rooting-depth multiplier.
  - Validation performed over different periods at the same 13 gauging stations and 100 groundwater wells.
  - Performance summarized by Kling-Gupta Efficiency (KGE) values for each sub-catchment (examples include calibration KGE around 0.80–0.83 and validation KGE around 0.6–0.86 across sub-catchments such as Manot, Mohgaon, Patan, Belkheri, Gadarwara, Chhigaon, Kohgaon, Barmanghat, Sandia, Hoshangabad, Handia, Mandleshwar, Garudeshwar).

- Details of data structure
  - Data are organized into twelve CSV files, each providing daily-scale, grid-averaged variables.
  - Baseline data files (1981–2013 and 1970–2013) cover total runoff and various demand-related variables:
    - Narmada_Baseline_1981_2013.csv: daily grid-mean totals for totQ and several demand/deficit variables (urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems, unfulfilled demand variables, etc.), plus aquifer level.
    - Narmada_Paddy_1981_2013.csv: similar structure to baseline (note an error reference in the source).
    - Upper_Narmada_Baseline_1970_2013.csv: total runoff (totQ) with grid-based coordinates and day/hour indexing.
  - Future climate and scenario files (daily, grid-mean totals) include:
    - Upper_Narmada_Climate_2028_2060.csv: total runoff components per model scenario for 2028–2060.
    - Narmada_climate_45_totQ_2021_2099.csv and Narmada_climate_85_totQ_2021_2099.csv: total runoff for RCP4.5 and RCP8.5, respectively, 2021–2099, with model-specific columns.
    - Narmada_climate_45_aqlevel_2021_2099.csv and Narmada_climate_85_aqlevel_2021_2099.csv: aquifer levels corresponding to the above scenarios.
    - Narmada_climate_paddy_45_totQ_2021_2099.csv and Narmada_climate_paddy_85_totQ_2021_2099.csv: total runoff under Paddy substitution scenarios for RCP4.5 and RCP8.5.
    - Narmada_climate_paddy_45_aqlevel_2021_2099.csv and Narmada_climate_paddy_85_aqlevel_2021_2099.csv: aquifer levels for Paddy substitution scenarios.
  - Each file includes coordinates (xll, yll), time (year, timestep), and model-specific columns labeled for each climate model or scenario (e.g., ACCESS_totQ, BCCSCM_totQ, CanESM_totQ, etc., and corresponding aQlevel fields where applicable).
  - Paddy substitution variants explicitly replace wheat with paddy in the future period data.
  - Files reflect daily time steps (Julian day 1–366) and grid-mean values for runoff, demand, and aquifer levels.

- Acknowledgements
  - Recognition of CMIP6 and the World Climate Research Programme’s contributions.
  - Gratitude to climate modelling groups for producing model outputs and to ESGF for data archiving and access.
  - Acknowledgement of funding bodies supporting CMIP6 and ESGF activities.

- Relevance for monitoring framework authors
  - Demonstrates end-to-end data lifecycle for environmental monitoring: model setup, scenario-driven projections, calibration/validation, and structured data outputs.
  - Emphasizes the importance of metadata and data descriptions (variable names, units, and descriptions) to support traceability and reuse.
  - Highlights handling of data complexity (ensemble climate models, multiple scenarios, Paddy substitution) to inform policy decisions under uncertainty.
  - Illustrates integration of physical hydrology with anthropogenic demands, relevant for policy scrutiny, evaluation, and future decision-making.
  - Shows data governance considerations at the source level (clear data structure, model provenance, and model validation results).