# GWAVA Modelling- SUNRISE1.5

- The GWAVA (Global Water Availability Assessment) model (version 5.0) is used to evaluate large-scale water resources and future availability in the Narmada Basin. It is a semi-distributed gridded model that combines natural hydrological processes with human (anthropogenic) stresses.
- Core modelling approach:
  - Local runoff in each grid cell is estimated with a lumped conceptual probability distribution model (PDM).
  - Model configuration includes three storage components: soil moisture storage, surface storage, and groundwater storage.
  - A demand-driven routine accounts for domestic (urban/rural), industrial, and agricultural water demands; irrigation demand is dynamic and crop/planting month dependent; domestic and livestock demands are user-defined and static in time but dynamic in space.
- Study area and resolution:
  - Upper Narmada Basin modelled at 0.125-degree grid, with the Upper Narmada split into 318 cells and the entire Narmada Basin into 653 cells.
  - The basin includes domestic, irrigation, and livestock demands, large and minor reservoirs, major water transfers, and agricultural areas within command and rural zones.
- Purpose for Analysts:
  - The model aims to identify correlations and inform practical decisions by integrating hydrological processes with anthropogenic demands under various climate scenarios.
  - Outputs are structured to be usable in reports and for informing policy or management decisions, with attention to traceability of data sources and metadata.

## 1.1 Model Setup

- GWAVA is a large-scale tool developed by the UK Centre for Ecology & Hydrology.
- The configuration integrates natural processes and human demands, with the PDM providing runoff estimation and the three storage components driving water balance.
- The model explicitly includes domestic, industrial, and agricultural water demands, with irrigation demands tied to crop type and planting month.

## 1.2 Future Projections

- An ensemble climate dataset under multiple CMIP6 models is used to represent future climate for GWAVA runs.
- Climate models involved (representative centers and model families) include, for example:
  - ACCESS1-0, ACCESS-CM2, ACCESS-ESM1-5
  - BCC-CSM1-1, BCC-CSM2-MR
  - CanESM2, CanESM5
  - CCSM4, CESM1-BGC
  - CNRM-CM5, CSIRO-Mk3.6.0
  - EC-Earth3, EC-Earth3-Veg
  - GFDL-CM3, GFDL-ESM2M
  - IPSL-CM5A-LR, IPSL-CM5A-MR
  - INM-CM4-8, INM-CM5-0
  - MIROC5, MIROC-ESM, MIROC-ESM-CHEM
  - MPI-ESM-LR, MPI-ESM-MR, MPI-ESM1-2-HR, MPI-ESM1-2-LR
  - MRI-ESM2-0
  - NorESM2-LM, NorESM2-MM
- The climate dataset supports period-specific projections such as baseline, and future scenarios including RCP4.5 and RCP8.5, with additional Paddy-crop substitution scenarios for future periods.
- Outputs are provided for total runoff (totQ) and other hydrological variables under multiple climate model realizations, enabling ensemble assessment of hydrological responses.

## 1.3 Quality Control

- Calibration:
  - The model was calibrated at 13 gauging stations across the basin using the SIMPLEX auto-calibration routine.
  - Four parameters were tuned: a surface and groundwater routing parameter, a PDM parameter describing spatial variation in soil moisture capacity, and a multiplier to adjust rooting depths.
- Validation:
  - Validation performed at the same 13 gauging stations over a different time period and at 100 groundwater observational wells.
  - Performance is reported as Kling-Gupta Efficiency (KGE) values (Table 2), across sub-catchments.
- Key results (examples):
  - Sub-catchments (e.g., Manot, Mohgaon, Patan, Belkheri, Gadarwara, Chhigaon, Kohgaon, Barmanghat, Sandia, Hoshangabad, Handia, Mandleshwar, Garudeshwar) show calibration KGE values ranging roughly from 0.72 to 0.83, with validation KGE values generally close (0.65–0.86) for many catchments.
  - Some sub-catchments exhibit lower validation performance (e.g., f, g with validation KGEs around 0.32–0.33), and a few others show moderate validation (e.g., d around 0.65, i around 0.63–0.79).
- Overall implication:
  - The model demonstrates generally good calibration/validation performance in many sub-catchments, with some areas showing weaker predictive capability, which is pertinent for interpretation and uncertainty assessment in decision support.

## 1.4 Details of data structure

- The dataset comprises twelve CSV files structured to provide both baseline and future climate-informed outputs.
- Baseline and climate data files:
  - Narmada_Baseline_1981_2013.csv
    - Daily baseline period (1981–2013) for grid cells; includes:
      - xll, yll: grid cell coordinates
      - year, timestep: calendar details
      - totQ: total runoff (m3/s)
      - aqlevel: aquifer level (m below ground)
      - urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems: various demand components
      - uf_* variables: unfulfilled demand components
  - Narmada_Paddy_1981_2013.csv
    - Similar structure to Narmada_Baseline with Paddy-cultivation adjustments (note: reference indicated as "Error: Reference source not found" in the text).
  - Upper_Narmada_Baseline_1970_2013.csv
    - Daily total runoff (totQ) for the Upper Narmada baseline period (1970–2013); includes coordinate and flow variables.
- Climate and future projections:
  - Upper_Narmada_Climate_2028_2060.csv
    - Daily totQ across the Upper Narmada for the climate-model ensemble covering 2028–2060; includes multiple model-specific totQ columns (e.g., ACCESS_totQ, BCCSCM_totQ, CANESM_totQ, etc.).
  - Narmada_climate_45_totQ_2021_2099.csv
  - Narmada_climate_85_totQ_2021_2099.csv
    - Daily totQ for RCP4.5 and RCP8.5 ensembles across the Narmada, with model-specific totQ columns for each climate model.
  - Narmada_climate_45_aqlevel_2021_2099.csv
  - Narmada_climate_85_aqlevel_2021_2099.csv
    - Daily aquifer level (aqlevel) outputs for RCP4.5 and RCP8.5 ensembles, across models.
  - Narmada_climate_paddy_45_totQ_2021_2099.csv
  - Narmada_climate_paddy_85_totQ_2021_2099.csv
    - Daily totQ outputs for Paddy-cropping scenarios under RCP4.5 and RCP8.5, with multiple climate-model columns.
  - Narmada_climate_paddy_45_aqlevel_2021_2099.csv
  - Narmada_climate_paddy_85_aqlevel_2021_2099.csv
    - Daily aquifer level outputs for Paddy-cropping scenarios under RCP4.5 and RCP8.5, with multiple climate-model columns.
- Data structure notes:
  - Each file includes grid coordinates (xll, yll), year, and timestep (Julian day), along with variables representing hydrology and demands.
  - The ensemble structure provides model-specific columns to enable multi-model analysis and uncertainty assessment.

## 1.4 Acknowledgements

- Acknowledges CMIP6 support through the World Climate Research Programme and its Working Group on Coupled Modelling.
- Thanks to climate modelling groups for providing model outputs, the Earth System Grid Federation (ESGF) for data archiving and access, and the funding agencies that support CMIP6 and ESGF.