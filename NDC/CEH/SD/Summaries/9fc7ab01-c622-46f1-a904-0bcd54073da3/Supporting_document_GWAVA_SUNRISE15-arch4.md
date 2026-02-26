# GWAVA Modelling- SUNRISE1.5

## 1.1 Model Setup
- GWAVA is a large-scale, semi-distributed water resources model developed by the UK Centre for Ecology & Hydrology.
- It estimates local runoff per grid cell using a lumped conceptual probability distribution model (PDM) and comprises three components: probability-distributed soil moisture storage, surface storage, and groundwater storage.
- A demand-driven routine accounts for anthropogenic stresses; demands include domestic (urban and rural), industrial, and agricultural sectors.
- Domestic and livestock demands are user-defined and time-invariant but spatially dynamic; irrigation demand is both temporally and spatially dynamic, driven by user-defined crop types and planting months.
- The model was applied to the Upper and entire Narmada Basin at a 0.125-degree spatial resolution, disaggregating the basin into 318 (Upper Narmada) and 653 (Whole Narmada) modelling cells.
- The basin modelling includes domestic, irrigation, livestock demands, large reservoirs, minor reservoirs, and agriculture within command and rural areas.

## 1.2 Future Projections
- An ensemble climate dataset was created to represent future climate for GWAVA runs.
- The ensemble comprises a wide range of climate models (various CMIP-models listed, e.g., ACCESS1-0, ACCESS-ESM1-5, BCC-CSM2-MR, CanESM2, CanESM5, CCSM4, CESM1-BGC, CNRM-CM5, CSIRO-Mk3.6.0, EC-Earth3, GFDL models, IPSL models, MIROC, MPI-ESM, MRI-ESM2-0, NorESM variants, and more).
- Scenarios include projections for the period 2028-2060 and extensions to other future periods, with outputs used to represent RCP4.5 and RCP8.5 pathways (and, in some files, paddy crop substitutions as part of scenario analyses).

## 1.3 Quality control
- Calibration was performed at 13 gauging stations across the basin using the SIMPLEX auto-calibration routine.
- Four parameters were tuned: surface and groundwater routing parameters, a PDM parameter describing spatial variation in soil moisture capacity, and a multiplier for rooting depths.
- Validation was conducted at the same 13 stations and at 100 groundwater observational wells, using Kling-Gupta Efficiency (KGE) as the performance metric.
- Reported KGE values (calibration/validation) vary by sub-catchment (e.g., Manot, Mohgaon, Patan, Belkheri, Gadarwara, Chhigaon, Kohgaon, Barmanghat, Sandia, Hoshangabad, Handia, Mandleshwar, Garudeshwar) with most sub-catchments showing moderate to high performance (e.g., 0.72–0.86 in calibration; 0.32–0.79 in validation, with a few lower outliers).

## 1.4 Details of data structure
- The data are organized into twelve CSV files, covering historical baseline data, alternative crop scenarios, and future climate projections.
- Baseline and historical data
  - Narmada_Baseline_1981_2013.csv: daily baseline data (1981–2013) with variables including total runoff (totQ), aquifer level (aqlevel), and various demand components (urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems, and unfulfilled demand variants uf_…_dems).
  - Narmada_Paddy_1981_2013.csv: similar structure to baseline but with Paddy irrigation context (note: an error reference in the source).
  - Upper_Narmada_Baseline_1970_2013.csv: total runoff for the upper basin (daily, 1970–2013), with grid coordinates and totQ.
- Future climate and impact projections
  - Upper_Narmada_Climate_2028_2060.csv: daily totQ for the upper basin under climate projections (structure includes xll, yll, year, timestep, totQ).
  - Narmada_climate_45_totQ_2021_2099.csv and Narmada_climate_85_totQ_2021_2099.csv: daily total runoff for RCP4.5 and RCP8.5, respectively, for 2021–2099, with multiple model-specific totQ columns (e.g., ACCESS_totQ, BCCSCM_totQ, CANESM_totQ, GFDL_totQ, IPSL_totQ, etc.).
  - Narmada_climate_45_aqlevel_2021_2099.csv and Narmada_climate_85_aqlevel_2021_2099.csv: daily aquifer level outputs under RCP4.5 and RCP8.5, respectively, for 2021–2099 (model-specific aqlevel variables).
  - Narmada_climate_paddy_45_totQ_2021_2099.csv and Narmada_climate_paddy_85_totQ_2021_2099.csv: daily totQ for future period replacing wheat with paddy under RCP4.5 and RCP8.5 (with multiple model-specific columns), including spatial coordinates and year/timestep.
  - Narmada_climate_paddy_45_aqlevel_2021_2099.csv and Narmada_climate_paddy_85_aqlevel_2021_2099.csv: daily aquifer level outputs for paddy-replaced scenarios under RCP4.5 and RCP8.5.
- File structure emphasizes daily, grid-level outputs with clear metadata for each variable (coordinate xll/yll, year, timestep, description of each totQ or aqlevel column).
- The dataset supports analysis of baseline vs. future climate under multiple climate models and crop scenarios, with both water availability (totQ) and groundwater depth (aqlevel) components.

## 1.5 Acknowledgements
- Acknowledges the World Climate Research Programme and its CMIP6 framework, climate modelling groups that produced model outputs, the Earth System Grid Federation for data archiving and access, and the funding agencies supporting CMIP6 and ESGF.