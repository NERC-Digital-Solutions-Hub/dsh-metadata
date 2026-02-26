# 1 Introduction to the project

## Overview
- Data from the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC via the Newton-Paulet Fund.
- Peruvian component conducted under the Glacier Research Circles call, via FONDECYT.
- Associated with the paper on the energy and mass balance of Peruvian glaciers (accepted at Journal of Geophysical Research: Atmospheres).
- Weather station input data originate from multiple stations (Shallap, Artesonraju, Cuchillacocha, Quelccaya, Quisoquipina) with additional off-glacier data used for filling; modelled data include averaged WRF outputs.
- The data are used with the Tethys-Chloris (T&C) ecohydrological model to calculate melt and mass balance at the point scale for five Peruvian glaciers.

## Data provenance and inputs
- On-glacier weather stations used for modelling: Shallap Glacier (SG), Artesonraju Glacier (AG), Cuchillacocha Glacier (CG), Cuchillacocha Quilcay (CQ), Quelccaya Ice Cap (QIC), Quisoquipina Glacier (QQG), plus Shallap Moraine data variants.
- Variables measured (and available for modelling): air temperature (Ta), relative humidity (RH), wind speed (WS), incoming/outgoing shortwave radiation (S↓/S↑), incoming/outgoing longwave radiation (L↓/L↑), precipitation (Pr), snow depth proxy (SR50).
- Data corrections and quality checks applied; data cleaned to produce suitable timeseries for modelling. Some datasets include modelled inputs (e.g., WRF) or off-glacier data used for filling.

## Data cleaning and gap filling
- Meteorological data cleaned to remove erroneous values; non-physical values corrected or removed.
- Zero wind speeds removed due to potential instrument freezing and modelling impact; gaps filled with monthly diurnal averages or by using nearby stations or WRF outputs when possible.
- Large jumps identified (e.g., Ta changes >10 °C, RH changes >40%) and inspected; persistent identical values over time inspected and corrected if needed.
- For several variables, data were filled using donor stations or modelled data (especially precipitation and radiation) to maintain diurnal and seasonal cycles.
- Acknowledgement of specific gaps:
  - Shallap data: significant gaps in December 2011 and Feb–Apr 2012; no appropriate fill due to short timeseries, resulting in a modelled gap from 1/12/2011 00:00 to 27/05/2012 23:00 aligned to snow-free conditions.
  - Cuchillacocha (CG) data: only a short overlap with on-glacier data; relationships between on- and off-glacier data based on winter (dry) conditions; some corrections applied to Ta, S↓, WS using nearby stations and seasonal adjustments.
- Data corrections and filling details are documented per station in Table 4 of the source document.

## Data correction specifics and data integration
- Donor relationships used to fill gaps:
  - SG: corrections based on SG data itself with small gaps interpolated; zero wind values replaced with monthly diurnal averages.
  - AG: Ta, RH corrected using off-glacier AM and Morder data; WS filled from AM with seasonal adjustments; S↓, S↑, L↓, L↑ corrected using AG and CQ relationships; Pr filled via AM/Santiago with undercatch corrections when modelled as snow.
  - CG: limited on-glacier data; Ta and RH linked to off-glacier CQ data with polynomial/linear fits; wind speed derived from AG/CQ differences; Pr primarily modelled or corrected using CQ data and undercatch considerations.
  - QIC and QQG: data largely measured at site; where gaps exist, filled with same-day data from random years or modelled inputs (e.g., WRF) as appropriate.
- Precipitation and snowfall handling include undercatch corrections for snow events (Chubb et al. 2015; other cited methods) and conversion of daily to hourly formats where needed.

## Model and methods (Tethys-Chloris)
- All T&C model code used for the Peruvian on-glacier application is provided.
- Main run file: T_and_C_Peru_EIDC.m; site-specific parameters configured via PARAM_Peru.m.
- Required inputs for adaptation to other sites: Ta, RH, Ws, Rsw, Pr; time zone, latitude/longitude, elevation; optional longwave radiation and albedo inputs if available.
- Radiation handling:
  - Cloudiness derived from shortwave radiation; longwave radiation optional if provided, otherwise calculated from cloudiness.
- Albedo handling:
  - Optional input Ameas; if NaN, albedo simulated from ice/snow parameters; can force model to use modelled albedo.
- Snow/ice surface parameters include snow density, initial depths, and ice depth; controls for wind, roughness, and longwave parameterisations.
- Output conventions follow the technical reference; later analysis converts flux directions to downward positive.
- Model equations for clean ice/snow are provided in supplementary information; parameter and structure details available in TC_Variable_and_Parameter_List.pdf and TeC_technical_reference.pdf.

## Data structure and units
- Data are provided in three folders:
  - Input_data: cleaned on-glacier input meteorological data (MAT-files for MATLAB processing; CSV files with corrected data ready for model input). Fields include:
    - Datetime (dd/mm/yyyy hh:mm, local time)
    - Ta (°C), Pr (mm h-1), U (relative humidity as fraction), Ws (m s-1)
    - Rsw (W m-2), Rsw_out (W m-2), Latm (W m-2), L_out (W m-2)
    - NetR (W m-2), SR_50 (m), zatm_hourly_m (instrument heights), Ameas (albedo)
  - Main_run_code: scripts for running the model, including Peru_Automatic_Radiation_Partition_I.m, Precipitation_partition_Ding.m, PARAM_Peru.m, and T_and_C_Peru_EIDC.m.
  - T_and_C: modelling functions and parameter files (e.g., Aerodynamic_Resistence.m, Albedo_Snow_Properties.m, Precipitation_partition.m, MAIN_FRAME.m, etc.).
- The .mat inputs contain processed data; .csv files reflect the data in ready-to-run units; NaNs indicate missing data.
- Documentation describes the purpose and usage of files, including site-specific adaptations and required input fields.

## Access, reproducibility, and notes
- The project provides a fully documented workflow to reproduce point-scale simulations for Peruvian glaciers, including data cleaning, filling strategies, and model parameterization.
- Files and structure enable adaptation to other sites with similar data types by supplying Ta, RH, Ws, Rsw, and Pr, adjusting time zones, coordinates, and elevation, and managing albedo and longwave inputs as available.

## References
- Chubb et al. (2015) on wind-induced undercatch corrections.
- Ding et al. (2014) on precipitation partitioning.
- Fatichi et al. (2012a, 2012b) on the mechanistic ecohydrological model framework.
- Mastrotheodoros et al. (2020) on ecohydrological analyses.
- Nitu et al. (2018) on SPICE precipitation intercomparison and undercatch factors.