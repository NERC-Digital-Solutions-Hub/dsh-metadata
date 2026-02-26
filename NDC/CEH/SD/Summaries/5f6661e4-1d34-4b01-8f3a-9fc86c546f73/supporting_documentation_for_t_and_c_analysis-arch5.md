# The energy and mass balance of Peruvian glaciers

- Purpose and provenance
  - Data and analyses accompany the study on energy and mass balance of Peruvian glaciers, part of the Peru GROWS and PEGASUS projects funded by NERC and CONCYTEC.
  - Peruvian component aligned with the Glacier Research Circles call; dataset supports the associated paper accepted in Journal of Geophysical Research: Atmospheres.

- Dataset scope
  - Five glaciers/ice bodies analyzed at the point scale: Artesonraju Glacier (AG), Shallap Glacier (SG), Cuchillacocha Glacier (CG), Quisoquipina Glacier (QQG), and Quelccaya Ice Cap (QIC).
  - Outputs and analysis from the Tethys-Chloris (T&C) physically-based melt and mass-balance model; model inputs and meteorological data referenced.
  - NOAA ONI data included for climate context, sourced from CPC.

- Data sources and inputs
  - Weather station locations and meteorological inputs feeding the T&C model.
  - NOAA ONI dataset used to characterize ENSO conditions.
  - Documentation of input data, model code, and dependencies provided to support reproducibility.

- Data products and analysis workflow
  - Analysis aims:
    - Compare energy fluxes and mass balance across sites.
    - Assess impacts of climate sensitivity scenarios (air temperature increased by 1–6 °C and precipitation varied by -30% to +30%).
  - Main outputs and analyses distributed across folders:
    - Main_runs_for_analysis: per-site model run outputs and NOAA ONI data (e.g., AG_Run_ax.mat, CG_Run_z.mat, QIC_Run_rosTa_510Pr_510.mat, etc.).
    - Main_analysis: code and results for site-level energy fluxes and mass balance; includes All_stations_analysis4.mat and CSV equivalents; descriptive Table 3 detailing variables saved in CSVs.
    - Climate_sensitivity: code and results for climate-sensitivity runs; includes per-site ablation, melt, sublimation, surface height change (specific mass balance), and total melt differences; matrices and CSVs summarizing differences.
    - Climate_sensitivity/Energy_ablation_change: subfolder with a focused comparison between standard and +2 °C perturbation; includes Climate_sensitivity_energy.m and outputs for energy/melt changes (Energy_compare_vars_2_with_ea_change.mat, SD_all_2.mat, Ta2_all_2.mat).
  - Data formats and variables
    - Outputs provided as MATLAB (.mat) files and CSVs for interoperability.
    - Variables cover albedo, snow/ice parameters, heat fluxes, radiation terms, temperature, precipitation, wind, snow/ice water equivalents, melt terms, and time-stamped meteorological and state variables (date, time, year, month, day, hour, season, hydrological year).
    - Tables describe the structure of output CSVs, with detailed field descriptions and units (e.g., Ta in °C, Pr in mm h^-1, G/H/Lout/etc in Wm^-2 or related units).

- Reproducibility and how to use
  - Analysis workflow requires adjusting pathnames in T_and_C_Peru_Analysis_EIDC.m to link to Main_runs_for_analysis data, then running the script to reproduce energy, melt, and El Niño-related figures.
  - Climate sensitivity analyses are executed via Climate_sensitivity_analysis_EIDC.mat (which loads Climate_sensitivity_vars_2_ea_change.mat); output CSVs contain differences between climate-change runs and standard runs.
  - The Climate_sensitivity_energy.m script enables direct comparison of standard vs. +2 °C perturbation runs across sites.

- Data governance and stewardship notes
  - Comprehensive documentation of data sources, model code, and analysis pipelines enhances reproducibility and data reuse.
  - Data are organized with per-site outputs and aggregated analyses, facilitating discovery and reuse by researchers comparing glacier energy and mass balance under varying climate perturbations.
  - Metadata coverage includes input data sources, model configuration, and description of outputs, supporting governance and lineage tracking.

- Practical considerations and caveats
  - The dataset employs multiple formats (MATLAB files and CSVs); users should ensure compatibility with their analysis tools.
  - Path management is required to run analysis scripts; users should mirror the documented directory structure.
  - Climate sensitivity results rely on defined perturbation ranges (-30% to +30% precipitation; +1 to +6 °C temperature) and may require contextual interpretation when comparing across sites.