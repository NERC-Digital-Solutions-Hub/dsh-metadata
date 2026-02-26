# Introduction to the project

- What the dataset covers
  - Outputs and analysis from the Tethys-Chloris (T&C) melt and mass balance model for five Peruvian glaciers: Artesonraju (AG), Shallap (SG), Cuchillacocha (CG), Quisoquipina (QQG), and Quelccaya Ice Cap (QIC).
  - Part of the Peru GROWS and PEGASUS projects funded by NERC and CONCYTEC; linked to research on glacier energy balance for the paper The energy and mass balance of Peruvian glaciers.

- Data sources and inputs
  - Model inputs: meteorological data, weather station locations, and T&C model code (referenced as the dataset 'The physically-based melt model Tethys-Chloris and meteorological input data for five Peruvian glaciers').
  - Observational context: NOAA ONI (Oceanic Niño Index) data for climate variability (El Niño/La Niña context), with ONI values derived from a 3-month running mean of SST anomalies.

- Structure and contents of the data and code
  - Main_runs_for_analysis: per-site T&C model outputs (AG, CG, QQG, SG, QIC) and NOAA ONI data stored as MATLAB files; ready for analysis.
  - Main_analysis: code to analyze energy fluxes and mass balance; outputs provided as:
    - CSV: AG_output_data.csv, CG_output_data.csv, QIC_output_data.csv, QQG_output_data.csv, SG_output_data.csv
    - MATLAB: All_stations_analysis4.mat; accompanying tables describe variables, units, and data types.
    - Key variable descriptions (Table 3) include albedo, snow/ice mass balance terms, energy fluxes (G, H, QE, Qfm, Rn, Rsw, etc.), melt terms (Imelt, Smelt, Tmelt), precipitation, air/ice temperatures, wind, humidity, snow/ice depths, SWE, albedo, and various fluxes.
  - Climate_sensitivity: code and data to assess how perturbations affect outputs.
    - Files for each site: ABL_diff.csv, Imelt_diff.csv, ISWE_diff.csv, Smelt_diff.csv, Sub_diff.csv, Tmelt_diff.csv (and equivalents for CG, QIC, QQG, SG, AG) detailing differences under climate perturbations.
    - Climate_sensitivity_analysis_EIDC.m to analyze and graph results; saved outputs in Climate_sensitivity_vars_2_ea_change.mat.
    - Additional CSV grids show changes across a -30% to +30% precipitation and +1 to +6 °C temperature perturbations; differences are reported in mm w.e. h-1 and m w.e. yr-1 for specific mass balance.
  - Energy_ablation_change: sub-folder comparing standard vs +2 °C perturbation.
    - Climate_sensitivity_energy.m to generate comparison figures; outputs include Energy_compare_vars_2_with_ea_change.mat, SD_all_2.mat, Ta2_all_2.mat.

- How to use the data (GIS-relevant workflow)
  - Run the main analysis to generate energy, mass balance, and El Niño figures by configuring and executing T_and_C_Peru_Analysis_EIDC.m; outputs appear as .mat and .csv files suitable for GIS workflows.
  - Use the per-site CSV outputs to create map layers of key variables (e.g., SWE, ice melt, total melt, albedo, net radiation) and compare spatially across the five glaciers.
  - Compare climate sensitivity scenarios by loading Climate_sensitivity_analysis_EIDC.mat and the associated CSV grids to produce difference maps and identify which sites are most responsive to temperature/precipitation changes.
  - Inspect energy and mass balance components and differences (e.g., Ablation, Ice melt, Snow melt, Total melt, Surface height change) to support GIS-based visualization of drivers of glacier change.
  - The Weather and climate context is anchored by NOAA ONI data, enabling integration with regional climate maps.

- Data formats and accessibility
  - Outputs are provided as both MATLAB (.mat) and comma-separated values (.csv) for easy integration with GIS tools.
  - The variable documentation (Table 3) explains units and whether each variable is a measured value or model output, aiding consistent mapping and interpretation.

- Reproducibility and reference
  - The dataset accompanies a peer-reviewed (accepted) paper on the energy and mass balance of Peruvian glaciers and includes the complete codebase to reproduce analyses and figures.

- Practical considerations for GIS work
  - Data come from five discrete glacier sites; ensure proper spatial alignment with glacier outlines for map-based analyses.
  - Be mindful of varying data resolutions and formats across inputs and outputs; preprocessing may be needed to harmonize datasets for GIS layering.
  - Climate sensitivity results provide a structured way to visualize potential impacts under warming and precipitation changes, useful for scenario planning and policy-oriented maps.