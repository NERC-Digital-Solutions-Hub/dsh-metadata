# GWAVA Modelling- SUNRISE1.5

## Aim and scope
- Presents GWAVA 5.0 modelling outputs for the Upper and whole Narmada Basin to assess local water availability and environmental health under climate and anthropogenic stress.
- Uses a semi-distributed, grid-based approach to simulate natural processes and human demands, enabling consistent monitoring of environmental health and policy performance over time.
- Produces standardized outputs (runoff, aquifer levels, demands, and unfulfilled demands) for monitoring and policy evaluation, with datasets stored in appropriate portals.

## Model Setup
- GWAVA (Global Water Availability Assessment) is a large-scale water resources model integrating natural processes and human stresses.
- Grid resolution: 0.125-degree cells; Upper Narmada modelled with 318 cells and whole Narmada with 653 cells.
- Core components: probability-distributed soil moisture storage, surface storage, and groundwater storage.
- Demand routine accounts for domestic (urban/rural), industrial, and agricultural water use; irrigation is dynamic and crop-type/month-dependent; large and minor reservoirs and transfers are included.

## Climate projections and ensemble
- Future climate represented by an ensemble dataset from CMIP6 models to capture uncertainty and variability.
- Models come from multiple modelling centres (e.g., CSIRO/BOM, BOM, Beijing Normal University, various CMIP6 contributors).
- Scenarios: Representative Concentration Pathways (RCP4.5 and RCP8.5) used to drive GWAVA runs and to create projections of totals and aquifer responses.

## Quality control: calibration and validation
- Calibration at 13 gauging stations using SIMPLEX auto-calibration with four parameters (surface and groundwater routing, soil moisture capacity, and rooting-depth multiplier).
- Validation at the same 13 stations over a later period and across 100 groundwater wells.
- Performance assessed with Kling-Gupta Efficiency (KGE); results include multiple sub-catchments with calibration and validation KGE values (e.g., many sub-catchments show KGE in the 0.7–0.86 range; some sub-catchments show lower values, e.g., 0.32–0.79, indicating variable performance across areas).

## Data structure and content
- Data organized into twelve CSV files, covering:
  - Baseline period 1981–2013 (daily scale) for Narmada_Baseline with variables such as total runoff (totQ), aquifer level (aqlevel), and various demand and unfulfilled-demand components (urban/rural, livestock, industrial, irrigation, and unfulfilled counterparts).
  - Narmada_Paddy_1981–2013 (similar structure; note indicates a reference issue in the source).
  - Upper_Narmada_Baseline_1970–2013 (daily total runoff, totQ).
  - Upper_Narmada_Climate_2028–2060 and Narmada_climate_45_totQ_2021–2099 and Narmada_climate_85_totQ_2021–2099 (daily totQ for multiple climate models under RCP4.5 and RCP8.5).
  - Narmada_climate_45_aqlevel_2021–2099 and Narmada_climate_85_aqlevel_2021–2099 (daily aquifer levels for RCP4.5 and RCP8.5).
  - Narmada_climate_paddy_45_totQ_2021–2099 and Narmada_climate_paddy_85_totQ_2021–2099 (replace wheat with paddy in future period; totQ per climate model).
  - Narmada_climate_paddy_45_aqlevel_2021–2099 and Narmada_climate_paddy_85_aqlevel_2021–2099 (aquifer levels with paddy substitution).
- File fields include grid coordinates (xll, yll), time (year, timestep), and variables such as totQ (total runoff), aquifer level, and various demand and unfulfilled-demand metrics.

## Outputs and usage
- Outputs provide spatially and temporally resolved runoff, aquifer status, and demand fulfillment to support environmental monitoring and policy assessment.
- Data are stored and accessible via appropriate portals, aligning with standard monitoring data practices and enabling reuse by other analysts.

## Accessibility and data governance
- Emphasises verification, quality assurance, and standardized methods to ensure datasets are usable for monitoring over time.
- Encourages data sharing and linking GWAVA outputs with other relevant datasets to enhance value and facilitate broad access for policy and environmental health monitoring.

## Acknowledgements
- Acknowledges CMIP6 framework and Earth System Grid Federation (ESGF) for model output archiving and access, and supporting funding agencies.