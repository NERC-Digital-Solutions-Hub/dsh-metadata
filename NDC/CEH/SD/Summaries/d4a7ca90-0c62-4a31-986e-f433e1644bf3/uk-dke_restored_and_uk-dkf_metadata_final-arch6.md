Metadata pertaining to EIDC submission: 'Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration'

## Context and Sites
- Study at two blanket bog sites on Forsinard RSPB Reserve, Flow Country, Caithness and Sutherland, Scotland.
- Former forestry plantation felled in Nov 2017; area affected by wildfire between May 15–19, 2019.
- UK-DKF: area burned by wildfire; UK-DKE-RESTORED: nearby area protected from fire and instrumented; instrumentation moved slightly from original locations.
- Paired design to assess restoration effects on carbon, water, and energy fluxes.

## What the dataset contains
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), methane (CH4), sensible heat (H), latent heat (LE), plus meteorological observations.
- Flux data originally at 20 Hz, processed to 30-minute intervals; meteorological data originally at 15-minute intervals, processed to 30-minute intervals.
- Time period covered: 25/09/2019 to 20/05/2021 (data capture through 16/10/2020 affected by instrument/power issues; later data have additional gaps due to power/logger faults).

## Data collection methods and instruments
- Eddy covariance (EC) system for LE, H, NEE; open-path CH4 flux for CH4.
- Sonic anemometers at 2.3–2.55 m heights; LI-COR gas analysers for CO2 and H2O; Li-7700 for CH4.
- Additional micrometeorology: air temperature (Ta), relative humidity (RH); net radiation (Rn), incoming shortwave (Rg), photosynthetically active radiation (PPFD).
- Soil and surface measurements near EC mast: soil heat flux (G), soil temperature (Tsoil) at ~0.05 m, soil volumetric water content (VWC); water table depth where installed.
- Precipitation (tipping bucket gauge) and wind-related measurements (wind speed/direction, friction velocity u*, stability parameter (z-d)/L).
- Data collected at high frequency (20 Hz for fluxes; 15-min to 30-min processing) with flags appended for quality.

## Data processing and quality control
- Fluxes computed with EddyPRO software; time lags and coordinate rotation applied; corrections for cospectral attenuation and density effects applied.
- H flux corrected for humidity influence; NEE assumed equal to turbulent CO2 flux; CO2 storage considered negligible at measurement height.
- Calibration: gas analysers calibrated per manufacturer guidelines; no routine on-site span/zero during period; June 2021 zero/span check showed no significant drift.
- Data screening: dataset submitted due to extremely patchy data capture without full screening; quality flags included to support future QA/QC.
- References for QA/QC methods provided (Mauder et al. 2013; Vickers & Mahrt 1997; Wilczak et al. 2001; Nakai et al. 2006; Moncrieff et al. 1997, 2004; Schotanus et al. 1983; Webb et al. 1980).

## Data structure, units, and availability
- Single CSV file with columns for DateTime and a comprehensive set of variables, each with accompanying FLAG fields.
- Key variables include: SWC microforms, Ts (soil temperature), Ta, RH, PPFD, Rn, Rg, P_rain, WTD, G, H, LE, co2_flux (NEE), h2o_flux, ch4_flux, gas/trace gas mixing ratios, u*, L, wind_speed, wind_dir, (z-d)/L.
- Flags use codes indicating raw, primary, calibrated, gaps, interpolations, or modelled data, with a maximum interpolation gap of 1 hour.
- Units are provided in the metadata (e.g., Ta in °C, Rn in W m^-2, LE/H in W m^-2, fluxes in μmol CO2 m^-2 s^-1 or μmol CH4 m^-2 s^-1, etc.).
- References and metadata explain the flagging scheme and data structure details.

## Limitations and caveats
- Data are patchy with significant gaps due to instrument power issues, sonic anemometer problems, site management, adverse weather, and COVID-19 travel restrictions.
- Early-period data capture affected; post-16/10/2020 data have additional gaps from power/logger faults.
- Some outputs are provided as raw or partially processed; users should leverage the included quality flags for reprocessing or gap-filling if needed.

## Access notes and references
- Data include both raw and processed fluxes to enable reanalysis or reprocessing.
- Key methodological references for flux calculations, QA/QC, and eddy covariance processing are cited for users who wish to understand or reproduce the processing steps.