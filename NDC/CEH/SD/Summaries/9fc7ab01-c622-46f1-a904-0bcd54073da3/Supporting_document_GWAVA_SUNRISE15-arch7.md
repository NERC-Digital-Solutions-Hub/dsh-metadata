# GWAVA Modelling- SUNRISE1.5

- A description of the GWAVA model (Global Water Availability Assessment) used to simulate water resources in the Upper and Whole Narmada Basins at high spatial resolution, including baseline and future climate projections, data structure, and quality control.

## Overview of the GWAVA model and purpose

- Large-scale, semidistributed gridded water resources model developed by the UK Centre for Ecology & Hydrology.
- Estimates local runoff per grid cell using a lumped probability distribution model (PDM) with components for soil moisture storage, surface storage, and groundwater storage.
- Includes a demand-driven routine for anthropogenic stresses (domestic, industrial, agricultural; irrigation demand is crop- and month-dependent).
- Basin coverage: Upper Narmada and Whole Narmada modeled at 0.125-degree resolution.
- Cells: Upper Narmada disaggregated into 318 cells; Whole Narmada into 653 cells.
- Outputs include daily grid-based data for various hydrological and demand variables, enabling map-style visualizations.

## Model setup and scope

- Spatial scale: 0.125 degree grid for the Upper and Whole Narmada basins.
- Components: soil moisture storage, surface storage, groundwater storage, and a demand routine for anthropogenic stresses.
- Administrative demands considered: domestic (urban/rural), industry, irrigation, livestock; irrigation demand is crop-type and planting-month dependent.
- Basins modeled: Upper Narmada and the entire Narmada basin with detailed sub-catchment breakdowns.

## Climate projections and ensemble models

- Uses an ensemble climate dataset to represent future climate for GWAVA runs.
- Climate models (CMIP6) used (examples include ACCESS1-0, ACCESS-CM2, ACCESS-ESM1-5, BCC-CSM variants, CanESM, CCSM/CESM variants, GFDL variants, IPSL variants, MIROC variants, MPI-ESM variants, MRI-ESM, NorESM variants, etc.).
- Projections cover multiple scenarios and model realizations to capture climate uncertainty.

## Quality control and model performance

- Calibration: performed against 13 gauging stations across the basin using SIMPLEX auto-calibration with four parameters.
- Validation: conducted at the same 13 gauging stations (over a different time period) and at 100 groundwater wells.
- Performance metric: Kling-Gupta Efficiency (KGE).
- Reported calibration/validation performance by sub-catchment (KGE values typically in the 0.3–0.86 range, with several sub-catchments showing higher values and some lower in validation).
- This quality control demonstrates the model’s ability to reproduce observed runoff and groundwater behavior to varying degrees across sub-catchments.

## Data structure and files

- Data are provided as twelve CSV files, each containing daily-scale outputs and metadata.
- 1. Narmada_Baseline_1981_2013.csv
  - Baseline daily data (1981–2013) with grid-cell means for variables including totQ (total runoff), aqlevel (aquifer level), and various demand and unfulfilled demand metrics.
  - Core variables: totQ, aqlevel, urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems, and their unfulfilled counterparts, with xll/yll coordinates, year, and timestep (Julian day).
- 2. Narmada_Paddy_1981_2013.csv
  - Baseline Paddy-adjusted data for 1981–2013 (similar structure to 1).
- 3. Upper_Narmada_Baseline_1970_2013.csv
  - Baseline total runoff (totQ) for Upper Narmada (1970–2013).
- 4. Upper_Narmada_Climate_2028_2060.csv
  - Total runoff outputs by climate model for the period 2028–2060 under future scenarios (labels include outputs for multiple models, e.g., ACCESS_totQ, BCCSCM_totQ, CANESM_totQ, etc.).
- 5. Narmada_climate_45_totQ_2021_2099.csv
  - Daily total runoff for RCP4.5 (2021–2099) with multi-model outputs (e.g., ACCESS_CM2_45_totQ, CANESM_totQ, etc.).
- 6. Narmada_climate_85_totQ_2021_2099.csv
  - Daily total runoff for RCP8.5 (2021–2099) with multi-model outputs.
- 7. Narmada_climate_45_aqlevel_2021_2099.csv
  - Daily aquifer level for RCP4.5 (2021–2099) across models.
- 8. Narmada_climate_85_aqlevel_2021_2099.csv
  - Daily aquifer level for RCP8.5 (2021–2099) across models.
- 9. Narmada_climate_paddy_45_totQ_2021_2099.csv
  - Paddy-replaced wheat scenario for RCP4.5 (2021–2099) with multi-model totQ outputs.
- 10. Narmada_climate_paddy_85_totQ_2021_2099.csv
  - Paddy-replaced wheat scenario for RCP8.5 (2021–2099) with multi-model totQ outputs.
- 11. Narmada_climate_paddy_45_aqlevel_2021_2099.csv
  - Paddy-replaced wheat scenario for RCP4.5 aquifer levels (2021–2099).
- 12. Narmada_climate_paddy_85_aqlevel_2021_2099.csv
  - Paddy-replaced wheat scenario for RCP8.5 aquifer levels (2021–2099).
- File structure notes:
  - Each file includes xll, yll, year, timestep, and model-specific columns for totQ and/or aqlevel, with units and detailed variable descriptions.
  - Paddy scenario files modify irrigation assumptions by replacing wheat with paddy in future periods.

- Baseline and future coverage
  - Baseline periods: 1981–2013 (and 1970–2013 for Upper Narmada).
  - Future projections: 2021–2099 under RCP4.5 and RCP8.5, including Paddy-replacement scenarios.
- Data use in GIS
  - Daily, grid-based values per modelling cell (318 upper-Narmada cells; 653 total cells for the basin) suitable for map-based visualization of runoff, groundwater depth, and demand dynamics.
  - Variables suitable for thematic mapping: totQ, aquifer depth, domestic/industrial/agricultural demands, irrigation, and unfulfilled demands.
  - Supports scenario comparisons across climate models and emission pathways.

## Practical notes for GIS specialists

- Data are provided as clean, structured CSVs with spatial and temporal metadata enabling straightforward plotting on maps and in time-series analyses.
- The 0.125-degree grid and daily time steps support high-resolution spatial visualization and dynamic temporal change assessment.
- The ensemble climate outputs facilitate uncertainty analysis and scenario planning in map-based decision support tools.
- Some inconsistencies or placeholders are noted (e.g., a reference note in Narmada_Paddy_1981_2013.csv indicating a missing reference source), so verify column descriptions against metadata when integrating.
- Acknowledges CMIP6 data sources and ESGF infrastructure, underscoring the provenance and reproducibility of projections.

## Acknowledgements

- Recognizes CMIP6, World Climate Research Programme, ESGF archiving and access, and supporting funding agencies for climate model outputs used in GWAVA.