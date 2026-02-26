The energy and mass balance of Peruvian glaciers

- Overview
  - Data and project context come from Peru GROWS and PEGASUS projects, funded by NERC and CONCYTEC, linked to the paper on energy and mass balance of Peruvian glaciers (accepted in Journal of Geophysical Research: Atmospheres).
  - Weather station data serve as inputs for an hourly ecohydrological model (Tethys-Chloris) to calculate melt and mass balance at five Peruvian glaciers.
  - Data are organized and provided to enable replication and further analysis, with attention to data provenance and quality.

- Data sources and study sites
  - On-glacier weather stations: Shallap Glacier (SG), Artesonraju Glacier (AG), Cuchillacocha Glacier (CG), Quisoquipina Glacier (QQG), Quelccaya Ice Cap (QIC).
  - Off-glacier and nearby stations used for filling, corrections, and precipitation data (e.g., Morder, Santiago Antúnez de Mayolo).
  - Model inputs include Ta (air temperature), RH, Ws (wind speed), S↓ (incoming shortwave), S↑ (outgoing shortwave), L↓/L↑ (longwave), Pr (precipitation), SR50 (snow depth sensor), and air pressure where available.
  - Modelled time periods vary by site, with some data gaps and periods where relationships with off-glacier data are used to fill missing values.

- Station locations and instrumentation
  - Detailed station attributes: coordinates, elevation, variables measured, instrument type/heights, and modelled periods.
  - Examples: AG on-glacier with Ta, RH, WS, S↓, S↑, L↓, L↑, SR50; CG on-glacier with Ta, Ts, RH, WS, S↓, S↑, Rn; QQG on/off glacier with Ta, RH, WS, S↓, S↑, L↓, L↑, Pr; QIC on-glacier with Ta, RH, WS, Pr, S↓, SR50, etc.
  - Instruments include Vaisala HMP45, Campbell CS215, Kipp&Zonen sensors, Apogee sensors, Ott Pluvio precipitation gauges, and SR50 snow depth sensors, with specifics on shielding and measurement heights.

- Data cleaning and quality control
  - Rigorous cleaning and quality checks prior to modelling: removal of clearly erroneous data, range corrections (e.g., RH capped at 100%), handling of negative or nonsensical values.
  - Specific steps: remove zero wind speeds (to avoid artificial flux suppression), fill gaps using nearby stations, other years, or model outputs (WRF) when possible; inspection for large jumps (Ta changes >10°C, RH changes >40%), and removal of repeated identical values.
  - Documentation of corrections per variable (as summarized in the study tables).

- Data correction and filling procedures
  - Continuous timeseries created by filling gaps in on-glacier data; when necessary, off-glacier data are corrected to represent on-glacier conditions.
  - Gap-filling approaches include linear regressions, hourly differences between stations, and diurnal/seasonal cycle preservation.
  - Site-by-site filling details:
    - SG (Shallap): all variables measured; substantial gaps in 2011-2012; some radiation/wind gaps not filled due to limited overlap with moraine data.
    - AG (Artesonraju): off-glacier data used for some variables; Pr from artesonraju moraine or WRF data; seasonal adjustments applied.
    - CG (Cuchillacocha): limited on-glacier data; most variables filled from off-glacier relationships; some time-aligned corrections in winter for Ta, S↓, WS.
    - CQ (Cuchillacocha Quilcay) and QIC (Quelccaya): most variables measured; Pr and S↓ corrections derived from related stations and WRF; snow undercatch corrections where applicable.
    - Morder and Santiago Antúnez de Mayolo: precipitation corrected for altitude and instrument differences; undercatch corrections applied for snow under snow conditions; hourly resampling of daily totals; snow/rain partition adjustments.
  - Precipitation corrections and undercatch
    - Use of Ding et al. (2014) precipitation partition to identify snow vs rain.
    - Under-catch corrections based on instrument type and shielding (e.g., Pluvio with no wind shield; factors around 0.63 to 0.57 depending on conditions).
    - Snowfall adjusted and added to liquid precipitation to produce final corrected timeseries.
  - Challenges and gaps
    - Notable data gaps at SG for most variables and between Dec 2011 and May 2012; limited overlap between Shallap datasets restricts filling in some periods.
    - On-glacier CG data available only for a short period; majority of the record relies on relations with off-glacier CQ data for validation and filling.

- Tethys-Chloris model (TC model)
  - The modeling workflow uses T_and_C_Peru_EIDC.m as the main run file, along with PARAM_Peru.m and radiation partition tools (Peru_Automatic_Radiation_Partition_I.m and Precipitation_partition_Ding.m).
  - Input requirements for site adaptation: Ta, U (relative humidity), Ws, Rsw, Pr; optional L↓; albedo (Ameas) and albedo parameterizations; air pressure; hourly versus static instrument heights.
  - Albedo handling: can use measured albedo or model albedo via snow/ice parameterizations; options to force modelled albedo if required.
  - Output conventions: flux directions follow the technical reference; downstream analysis converts to downward positive fluxes.
  - Model documentation is supported by TC_Variable_and_Parameter_List.pdf and TeC_technical_reference.pdf, with detailed parameter settings in PARAM_Peru and associated model files.

- Data structure and access
  - Three main folders for data and code:
    - Input_data: corrected on-glacier meteorological data in .mat and .csv formats; includes datetime, Ta, Pr, U, Ws, Rsw, Rsw_out, Latm, L_out, NetR, SR_50, zatm_hourly_m, Ameas; NaNs indicate missing data.
    - Main_run_code: PK scripts for running TC model; includes Peru_Automatic_Radiation_Partition_I.m, Precipitation_partition_Ding.m, T_and_C_Peru_EIDC.m, PARAM_Peru.m.
    - T_and_C: extensive library of model functions for energy balance, albedo, radiation, hydrology, and related processes.
  - Data are provided to enable replication of the modelling workflow and site-specific parameterization; the .csv files present corrected inputs with local time stamps suitable for running the model in Matlab.

- Reproducibility, governance, and references
  - The dataset emphasizes transparent provenance, with explicit links to raw inputs, corrections, model configurations, and parameter files.
  - Key references informing methodologies include Chubb et al. (2015) on wind-induced gauge undercatch, Ding et al. (2014) on precipitation partitioning, Fatichi et al. (2012) on the ecohydrological modelling framework, Mastrotheodoros et al. (2020) on related glacier studies, and Nitu et al. (2018) SPICE-related corrections.
  - Funding acknowledgments highlight the collaboration and support for glacier research in Peru, enabling data sharing and method development.

- Practical implications for monitoring frameworks
  - Demonstrates a rigorous workflow for assembling, cleaning, correcting, and filling environmental time series used in glacier energy balance modelling.
  - Highlights the importance of metadata, station documentation, and cross-station data transfer to overcome data gaps and ensure consistency.
  - Shows explicit data governance steps (data provenance, sharing of inputs/outputs, and reproducible code) relevant to environmental health monitoring and policy evaluation.
  - Illustrates challenges common to environmental monitoring (data gaps, data standardization, need for model-based filling, and undercatch corrections) and how to address them in a monitoring framework.