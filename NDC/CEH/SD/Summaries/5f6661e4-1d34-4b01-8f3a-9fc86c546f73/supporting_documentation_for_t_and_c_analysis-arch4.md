# 1 Introduction to the project

- This dataset stems from the Peru GROWS and PEGASUS projects (funded by NERC and CONCYTEC) and is linked to a paper on the energy and mass balance of Peruvian glaciers.
- It contains outputs and analyses from the Tethys-Chloris (T&C) melt and mass balance model applied at five Peruvian glaciers: Artesonraju Glacier (AG), Shallap Glacier (SG), Cuchillacocha Glacier (CG), Quisoquipina Glacier (QQG), and Quelccaya Ice Cap (QIC).
- Data inputs include model weather inputs, weather station locations, and the T&C model code; the dataset also includes NOAA Oceanic Niño Index (ONI) data.
- The modelling and analysis were produced primarily by Catriona Fyffe (analysis code largely written by Fyffe; one function by Simone Fatichi). The NOAA ONI data source is the CPC.

- Associated outputs support comparison of energy and mass balance across sites and assessment of climate sensitivity experiments perturbing temperature and precipitation.

## Data sources and scope

- Model: physically-based melt model Tethys-Chloris; outputs cover energy fluxes and mass balance for each site.
- Climate inputs: meteorological data from weather stations and NOAA ONI index (3-month running mean; warm/cold phases defined by ±0.5°C anomaly thresholds).
- Climate sensitivity experiments: perturb inputs by increasing air temperature from +1°C to +6°C and varying precipitation from -30% to +30%.

## Data structure and contents

- Main_runs_for_analysis: site-specific T&C model outputs (AG, CG, QIC, QQG, SG) plus NOAA ONI data, stored as MATLAB .mat files.
  - Examples: AG_Run_ax.mat, CG_Run_z.mat, QQG_Run_g_newval.mat, SG_Short_k.mat, NOAA_ONI.mat, QIC_Run_rosTa_510Pr_510.mat
- Main_analysis: code and outputs used to compute energy fluxes and mass balance; produces per-site CSVs and All_stations analyses.
  - Key files: AG_output_data.csv, CG_output_data.csv, QIC_output_data.csv, QQG_output_data.csv, SG_output_data.csv, All_stations_analysis4.mat
  - Includes a description of variables and units (Table 3) and the main analysis script T_and_C_Peru_Analysis_EIDC.m
- Climate_sensitivity: code and data for climate sensitivity runs; differences across sites are saved as .csv grids.
  - Files include: AG_Abl_diff.csv, AG_Imelt_diff.csv, AG_ISWE_diff.csv, AG_Smelt_diff.csv, AG_Sub_diff.csv, AG_Tmelt_diff.csv (and analogous files for CG, QIC, QQG, SG)
  - Includes Climate_sensitivity_analysis_EIDC.m and Climate_sensitivity_vars_2_ea_change.mat
- Climate_sensitivity>Energy_ablation_change: dedicated comparison of standard vs +2°C perturbation.
  - Climate_sensitivity_energy.m, Energy_compare_vars_2_with_ea_change.mat, SD_all_2.mat, Ta2_all_2.mat

## Variables and metadata

- Per-site output CSV files (Table 3) include both observed (M) and modelled (S) data for numerous variables, such as:
  - Ta (air temperature), Tice, Ts (surface temperature)
  - Rn (net radiation), Latm (incoming longwave), L_out (outgoing longwave), G (ground heat flux), H (sensible heat), QE (latent heat), Qfm (melting/freezing heat of water in snow), Rsw/Rsw_out (shortwave radiation)
  - Pr, Pr_liq, Pr_sno (precipitation components)
  - SWE (snow water equivalent), ICE/SWE-related melt terms (Imelt, Smelt, Smelt), ICE/ICE_D (ice pack depth)
  - AlB (albedo), N (cloudiness), U (relative humidity), Ws (wind), etc.
- Data include time stamps and a hydrological year convention (Season HyYear) based on a November start; YearMonth and seasonal indicators are provided.
- The tables describe whether each variable is observed (M) or modelled (S) and include units and descriptions.

## Analysis workflow and reproducibility

- Reproducing main analyses:
  - Update T_and_C_Peru_Analysis_EIDC.m to point to the Main_runs_for_analysis folder, then run to generate energy, melt, and mass balance figures (and corresponding .csv outputs).
- Climate sensitivity analyses:
  - Run Climate_sensitivity_analysis_EIDC.mat to load climate-sensitivity outputs; examine per-site differences in key melt and mass balance variables stored as .csv grids.
  - Interpret grids where precipitation varies by column (-30% to +30%) and temperature increases by row (+1°C to +6°C).
- Energy/melt comparison:
  - In Climate_sensitivity_energy.m (within Energy_ablation_change), compare standard runs to +2°C perturbations to produce energy and mass balance comparison figures.
  - Outputs include: Energy_ablation_change figure and data files (Energy_compare_vars_2_with_ea_change.mat, SD_all_2.mat, Ta2_all_2.mat).

## Relationship to publication and credits

- The dataset supports the paper: The energy and mass balance of Peruvian glaciers (Fyffe et al., accepted in Journal of Geophysical Research: Atmospheres).
- NOAA ONI data are sourced from the CPC; the energy and mass balance analyses are tied to multiple sites and climate sensitivity scenarios.

## Data governance and usage notes

- The dataset integrates model outputs, derived analyses, and climate sensitivity results, with explicit instructions for reproduction and analysis.
- Data are delivered with code and metadata descriptions (Tables 2 and 3) to aid interpretability and reuse across sites.
- Proper attribution should accompany use, given model authorship and project provenance.