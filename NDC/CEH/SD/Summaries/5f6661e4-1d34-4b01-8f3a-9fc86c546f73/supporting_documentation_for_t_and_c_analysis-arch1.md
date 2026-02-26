# The energy and mass balance of Peruvian glaciers

- Overview
  - Data from the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC (Newton-Paulet Fund).
  - Peruvian component conducted under the call E031-2018-01-NERC "Glacier Research Circles" via FONDECYT.
  - Associated with the paper “The energy and mass balance of Peruvian glaciers” in Journal of Geophysical Research: Atmospheres.
  - Dataset comprises outputs and analyses from Tethys-Chloris (T&C) melt and mass balance modelling at point scale for five glaciers: Artesonraju (AG), Shallap (SG), Cuchillacocha (CG), Quisoquipina (QQG), and Quelccaya Ice Cap (QIC).

- Modelling and data provenance
  - Modelling: physically-based melt and energy/mass balance using the Tethys-Chloris (T&C) model.
  - Outputs produced by Catriona Fyffe; most analysis code written by Fyffe, with the Incoming_longwave.m function contributed by Simone Fatichi.
  - NOAA Ocean Niño Index (ONI) data used as part of the climate context; ONI sourced from NOAA Climate Prediction Center (3-month running mean, threshold ±0.5°C defines warm/cold phases).

- Scope of analysis
  - Purpose: enable comparison of energy fluxes and mass balance across sites and assess climate sensitivity scenarios (temperature perturbations +1 to +6°C and precipitation changes -30% to +30%).
  - Primary outputs: standard T&C runs and climate sensitivity runs, with corresponding analyses and visualizations.

- Data structure and main components
  - Main_runs_for_analysis
    - Contains model outputs for each weather station and the NOAA ONI data.
    - Key files: AG_Run_ax.mat, CG_Run_z.mat, QIC_Run_rosTa_510Pr_510.mat, QQG_Run_g_newval.mat, SG_Short_k.mat, NOAA_ONI.mat.
  - Main_analysis
    - Contains code and results for site-by-site energy fluxes and mass balance analyses.
    - Outputs saved as All_stations_analysis4.mat and CSV files (e.g., AG_output_data.csv, CG_output_data.csv, QIC_output_data.csv, QQG_output_data.csv, SG_output_data.csv).
    - Additional files include T_and_C_Peru_Analysis_EIDC.m (main analysis script) and a colour map file (BWRnewmap.mat).
    - Table 3 describes the variables saved in the CSVs (e.g., albedo, snow cover, vapour pressure, various energy fluxes, melt terms, snow/ice properties, precipitation, temperature, wind, etc.), with flags for measured vs. modelled data.
  - Climate_sensitivity
    - Contains code and results for climate sensitivity experiments.
    - Files describe differences between climate-change and standard runs for each site (e.g., AG_Abl_diff.csv, AG_Imelt_diff.csv, AG_ISWE_diff.csv, AG_Smelt_diff.csv, AG_Sub_diff.csv, AG_Tmelt_diff.csv, and analogous files for CG, QIC, QQG, SG).
    - Climate_sensitivity_analysis_EIDC.m loads saved outputs (Climate_sensitivity_vars_2_ea_change.mat). Gridded CSVs show differences in key melt and mass-balance variables; grid layout varies precipitation (-30% to +30%) across columns and temperature (+1°C to +6°C) across rows.
    - Differences are reported as: ablation, ice melt, snow melt, total melt, sublimation (in mm w.e. h^-1) and specific mass balance changes (in m w.e. yr^-1).
  - Energy_ablation_change
    - Subfolder within Climate_sensitivity; compares standard run with a +2°C perturbation.
    - Key files: Climate_sensitivity_energy.m (script), Energy_compare_vars_2_with_ea_change.mat (outputs of comparison), SD_all_2.mat (standard runs), Ta2_all_2.mat (+2°C runs).

- How to reproduce and use
  - Main analysis workflow
    - Update pathnames in T_and_C_Peru_Analysis_EIDC.m to point to the Main_runs_for_analysis data.
    - Run T_and_C_Peru_Analysis_EIDC.m to generate energy, mass balance, and El Niño figures; outputs include the *_output_data.csv files and All_stations_analysis4.mat.
  - Climate sensitivity workflow
    - Run Climate_sensitivity_analysis_EIDC.mat to load climate sensitivity results (Climate_sensitivity_vars_2_ea_change.mat).
    - View differences in CSV grids (e.g., AG_Abl_diff.csv, CG_Tmelt_diff.csv, etc.) to compare climate-change vs. standard runs.
    - Use Energy_ablation_change/Climate_sensitivity_energy.m to compare standard vs. +2°C perturbation; outputs stored in Energy_compare_vars_2_with_ea_change.mat, SD_all_2.mat, and Ta2_all_2.mat.

- Data access and metadata
  - Outputs are provided as MATLAB (.mat) and CSV files for interoperability.
  - Input data and meteorological details are described in the related dataset titled “The physically-based melt model Tethys-Chloris and meteorological input data for five Peruvian glaciers.”
  - The dataset includes documentation on variable definitions, units, and the meaning of measured versus modelled data (Table 3 in the Main_analysis description).

- Associated publication and data sources
  - Tethys-Chloris model outputs and climate analyses are tied to the paper on the energy and mass balance of Peruvian glaciers (accepted at Journal of Geophysical Research: Atmospheres).
  - NOAA ONI data sourced from the NOAA CPC page; ONI defined by sea surface temperature anomalies over a 3-month running mean, with ±0.5°C thresholds for warm/cold phases.

- Summary of site coverage
  - Five Peruvian glacial/ice bodies analyzed: Artesonraju (AG), Shallap (SG), Cuchillacocha (CG), Quisoquipina (QQG), and Quelccaya Ice Cap (QIC).
  - Site-specific outputs are stored in individual MAT/CSV files and aggregated in All_stations_analysis outputs.