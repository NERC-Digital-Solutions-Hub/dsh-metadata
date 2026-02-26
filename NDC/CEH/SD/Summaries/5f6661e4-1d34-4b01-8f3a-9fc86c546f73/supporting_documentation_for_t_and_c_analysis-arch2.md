# The energy and mass balance of Peruvian glaciers

- Overview
  - Dataset and analysis produced as part of the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC through the Newton-Paulet Fund.
  - Peruvian component conducted under the Glacier Research Circles call (E031-2018-01-NERC) with FONDECYT as executing unit.
  - Associated with a Journal of Geophysical Research: Atmospheres paper on the energy and mass balance of Peruvian glaciers.
  - Dataset covers five glaciers: Artesonraju Glacier (AG), Shallap Glacier (SG), Cuchillacocha Glacier (CG), Quisoquipina Glacier (QQG), and Quelccaya Ice Cap (QIC).
  - Data comprise outputs and analyses from the Tethys-Chloris (T&C) physically-based melt and mass balance model; input data, weather station locations, and T&C model code are described in related datasets.
  - NOAA Ocean Niño Index (ONI) data are used to characterize climate variability (warm/cold phases defined when anomalies exceed ±0.5 °C).

- Analysis goals and methods
  - Purpose: enable comparison of site energy fluxes and mass balance, and assess the impact of climate sensitivity perturbations (temperature and precipitation changes) on modelled melt and mass balance.
  - Climate sensitivity experiments: perturb air temperature by +1 to +6 °C and vary precipitation by -30% to +30%.
  - Outputs include standard T&C model runs and climate sensitivity results, stored and organized to support cross-site comparison and visualization (figures in the associated paper).

- Data and code structure (Main folders)
  - Main_runs_for_analysis
    - Contains per-site T&C model outputs and NOAA ONI data.
    - Files include AG_Run_ax.mat, CG_Run_z.mat, QIC_Run_rosTa_510Pr_510.mat, QQG_Run_g_newval.mat, SG_Short_k.mat, and NOAA_ONI.mat.
  - Main_analysis
    - Code to perform main energy flux and mass balance analysis using T&C inputs.
    - Outputs include All_stations_analysis4.mat and per-site CSVs (AG_output_data.csv, CG_output_data.csv, QIC_output_data.csv, QQG_output_data.csv, SG_output_data.csv) plus a description Table 3 of variables.
    - Provides a T_and_C_Peru_Analysis_EIDC.m script to generate energy, mass balance, and El Niño figures.
    - Includes a colour map file (BWRnewmap.mat) for El Niño heatmaps.
  - Climate_sensitivity
    - Code and data to analyze climate sensitivity runs.
    - Contains Climate_sensitivity_analysis_EIDC.mat to load results saved in Climate_sensitivity_vars_2_ea_change.mat.
    - CSV difference grids report site-by-site differences in main melt and mass balance variables; grids show precipitation perturbation by column (-30% to +30%) and temperature perturbation by row (+1 to +6 °C).
    - Variables include ablation, ice melt, snow melt, sublimation, total melt, and surface height change (specific mass balance over the modelling period).
    - Each site (AG, CG, QIC, QQG, SG) has corresponding .csv difference files (e.g., AG_Abl_diff.csv, AG_Imelt_diff.csv, etc.).
  - Climate_sensitivity > Energy_ablation_change
    - Sub-folder for direct energy-malance comparison between standard run and +2 °C perturbation.
    - Climate_sensitivity_energy.m to generate comparison figures.
    - Outputs include energy comparison data (Energy_compare_vars_2_with_ea_change.mat) and standard vs +2 °C runs (SD_all_2.mat, Ta2_all_2.mat).

- Data content and variable details
  - Outputs encompass a comprehensive set of energy fluxes, mass-balance indicators, and meteorological inputs (e.g., albedo, snow cover, ice/melt rates, latent and sensible heat fluxes, net radiation, precipitation, air pressure, temperature, wind, etc.).
  - Outputs are provided as both MATLAB files (.mat) and comma-separated values (.csv) for reuse in other applications.
  - Table 3 (described in the dataset) enumerates variables with units and whether each is a model input or a model output (e.g., Ta, Tice, Pr, SWE, SWE, ALB, H, G, Rn, SWnet, LWnet, etc.).

- Practical notes for analysts
  - Reproducing analyses: adjust pathnames in T_and_C_Peru_Analysis_EIDC.m to point to Main_runs_for_analysis data, then run to generate energy, mass balance, and El Niño figures.
  - Climate sensitivity analyses: run Climate_sensitivity_analysis_EIDC.mat to load climate sensitivity results; examine the grid-based differences across -30% to +30% precipitation and +1 to +6 °C temperature perturbations.
  - Access and reuse: outputs are organized by site and by analysis type; the dataset supports cross-site comparisons and integration with other environmental data sources to enhance the value of monitoring outputs.
  - Data provenance: includes explicit notes on input data sources, weather station details, and the origin of model code (with minor subfunctions attributed to contributors).

- Funding and data provenance
  - Data are linked to the Peru GROWS and PEGASUS projects (NERC and CONCYTEC funding) and the Glacier Research Circles call.
  - NOAA ONI data sourced from the NOAA Climate Prediction Center (provided with a description of warm/cold phases based on 3-month running mean anomalies).