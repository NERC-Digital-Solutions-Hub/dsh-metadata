# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

- Overview: Provides time series observations of land surface-atmosphere exchanges including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) using an open-path eddy covariance setup from 2015-01-01 to 2018-10-11 at site AF-LN (Anglesey, UK). Ancillary meteorological and soil physics data accompany the flux measurements. Data were processed to produce gap-filled and partitioned fluxes with quality controls.

- Study site: AF-LN flux observation site located at Cors Erddreiniog National Nature Reserve, Anglesey, North Wales (53°18'37.18" N, 4°17'28.06" W; 63 m a.s.l.). The fen is grass-dominated, peat-based, cherry-pieced with marl bands, and is managed with low-intensity pony grazing. The climate is temperate maritime; peat is shallow-to-moderate with high carbon content and near-surface water levels year-round.

- Sampling regime: Automated flux, meteorological, and soil physics measurements conducted between 2015-01-01 00:30 and 2018-10-11 00:00. Observations logged as 30-minute means; 20 Hz raw data collected.

- Flux data acquisition: 
  - Instrumentation: Open-path eddy covariance system at 2.0 m height; CSAT3 ultrasonic anemometer and LI-7500 CO2/H2O infrared gas analyser; CR3000 Micrologger for data logging.
  - Measured fluxes: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), τ (kg m^-1 s^-2); plus related sensor data (wind speed/direction, temperatures, humidity, density terms, etc.).
  - Data characteristics: Raw 3-vector wind components, sonic temperature, water vapor and CO2 density; data at 20 Hz.

- Ancillary data acquisition:
  - Co-located meteorological and soil observations: air temperature (Ta), relative humidity (RH), net radiation (Rnet), incoming shortwave (SWin), soil heat fluxes (G1, G2), near-surface soil temperatures (Tsoil), precipitation (two measurements), wind speed/direction, friction velocity (u*), turbulence metrics (TKE, L, z/L), and flux footprint estimates.
  - Observations summarized as 30-minute means or sums for precipitation.

- Data processing:
  - Processing tool: EddyPRO v6.1 used to compute flux densities, with corrections for QC, tilt, coordinate rotation, spectral corrections, density corrections, and humidity and storage-term adjustments.
  - Outputs: Fluxes and auxiliary variables, plus calculated metrics (u*, TKE, L, z/L) and flux footprints.
  - Uncertainty and quality: Random uncertainties calculated; fluxes subjected to quality control and post-processing checks.

- Quality control:
  - Outlier removal: Median absolute deviation approach; non-stationary turbulence periods removed; flux values constrained to plausible ranges (-200 to 500 W m^-2 for H, -60 to 500 W m^-2 for LE, -50 to 30 μmol CO2 m^-2 s^-1 for NEE).
  - Night-time NEE handling: NEE data removed when fluxes were negative at night; a friction velocity threshold (u*) of 0.18 m s^-1 applied to filter unreliable periods.
  - Manual checks: Weekly visual checks of all flux and ancillary data to remove any outliers missed by automated QC.

- Data gap-filling and flux partitioning:
  - Gap-filling: Used Marginal Distribution Sampling (Reichstein et al., 2005) to fill NEE, LE, and H gaps.
  - Flux partitioning: NEE partitioned into GEP and TER using the Reichstein et al. framework; driven by air temperature observations.
  - Tools: REddyProc (R) for gap-filling and partitioning; where possible, meteorological gaps filled using data from a nearby eddy covariance station within 1 km.
  - Outputs: Gap-filled time series including NEE_filled, LE_filled, H_filled, TER, GEP, and their associated uncertainties (e.g., NEE_filled_sd, LE_filled_sd, H_filled_sd).

- Details of data structure:
  - File: AF-LN_Lowland_Valley_Fen_2015_2018.csv
  - Time span: 2015-01-01 00:30 to 2018-10-11 00:00; missing records denoted by -9999.
  - Data format: Single CSV with tabular data; columns described in Table 1 (DateTime, NEE, NEE_sd, LE, LE_sd, H, H_sd, Tau, Tau_sd, CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, SWin, Rnet, G1, G2, Tsoil1, Precipitation, WS, WD, Ustar, TKE, L, zL, x_peak, x_70, x_90, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.).
  - Units and descriptions: Variables and units follow LI-COR conventions and Reichstein et al. (2016) conventions; includes both raw (pre-gap-fill) and gap-filled products with corresponding uncertainties.

- Nature and units of recorded values:
  - The dataset includes 30-minute time-series records for flux densities (NEE, LE, H, τ) and ancillary environmental variables, plus storage terms and derived flux components (NEE_filled, LE_filled, H_filled, TER, GEP) and their uncertainties.
  - Descriptions and units are provided for all variables, aligned with established micrometeorological standards.

- Acknowledgments and references:
  - Funding and support: Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE and Defra SP1210 project; permissions from Natural Resources Wales to install the flux tower and access Cors Erddreiniog Nature Reserve.
  - Key references cover methodology and processing standards for eddy covariance, QC, gap-filling, and partitioning algorithms (e.g., Reichstein et al., 2005, 2016; Mauder et al., 2013; Moncrieff et al., 1997, 2004; Webb et al., 1980; etc.).