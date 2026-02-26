# Net ecosystem carbon dioxide (CO2) exchange and meteorological observations from an eroded, high altitude, blanket bog, Scotland, 2018-2020

## Overview
- Time series of land–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), plus meteorological observations.
- Site: eroded upland blanket bog peatland (UK-BAL) in the Eastern Cairngorms, Scotland; maritime temperate montane climate; coordinates 56.93° N, -3.16° E, 642 m above sea level.
- Data resolution: raw fluxes at 20 Hz processed to 30-minute means; meteorological data at 15-minute processed to 30-minute means.
- Observation period: 04/07/2018–04/11/2020; notable data gaps due to power issues and peatland restoration-related events; some data discarded due to spectral issues and COVID-related access limits.

## What is included
- Primary flux measurements: NEE, LE, H (30-minute processed) with associated random uncertainties.
- Storage terms: CO2_strg, LE_strg, H_strg.
- Gap-filled products and components: NEE_filled, LE_filled, H_filled, with corresponding uncertainties; TER (total ecosystem respiration) and GEP (gross ecosystem production) derived from NEE partitioning.
- Ancillary variables: atmospheric pressure (Pa), air temperature (Tair), relative humidity (RH), vapor pressure deficit (VPD); radiation components (SWin, SWout, LWin, LWout, Rnet); soil temperature at multiple depths (Tsoil), soil heat flux (G1, G2), soil volumetric water content (VWC), precipitation, water table depth, wind metrics (WS, WD), friction velocity (Ustar), turbulent kinetic energy (TKE), Obukhov length (L), stability parameter (zL).
- Metadata details on units and data structure provided; dataset updates a previously deposited record and includes gap-filling and uncertainty estimates.

## Data collection and instrumentation
- Eddy covariance (EC) system: Windmaster sonic anemometer at 3.2 m height; LI-7200 enclosed-path gas analyzer for CO2 and H2O.
- Ancillary sensors: Net radiometer above canopy, PAR sensor, soil sensors for temperature, moisture, and heat flux, tipping-bucket precipitation gauge, and a water table sensor.
- Field conditions: fully vegetated surface with static canopy height assumption; fetch >1000 m (except N direction restricted by cliff edge).
- Calibration: gas analyzer calibrated per manufacturer; no on-site span/zero checks during data capture; instrument cleaned mid-August 2020; overall signal quality remained high prior to late-2019.

## Data processing and quality control
- Flux processing: EddyPRO v7.0.6; corrections for cospectral attenuation, density effects, humidity, and lag removal; 30-minute fluxes used for QC and gap-filling.
- QC criteria: outlier detection (MAD), stationarity tests, physically plausible flux ranges, low-turbulence periods identified via u* thresholds (excluded when u* < 0.17 m s^-1).
- Gap filling and partitioning: REddyProc used to gap-fill H, LE, and NEE and to partition NEE into GEP and TER (MDS approach for gap-filling); annual sums rely on Braemar station data for missing periods; Tair used as driving temperature when Tsoil data gaps exist.
- Uncertainty estimation: standard deviation of observations averaged to fill gaps; uncertainty provided for gap-filled values.

## Data structure and accessibility
- Data stored in a single CSV file with columns including DateTime, NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, Lwin, LWout, Rnet, G1, G2, Tsoil, WaterLevel, Precipitation, WS, WD, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
- Documentation notes that this dataset is an update to a shorter, daily-data version deposited previously.
- Access details and full metadata are available via the CEH catalogue link provided in the submission.

## Data quality, limitations, and caveats
- Data coverage during the monitoring period: approximately NEE 51%, LE 54%, H 76%; biomet data 92–97% except long-wave radiation (80%) due to a faulty sensor in mid-2019.
- Major gaps: 14 Nov–27 Dec 2019 data lost due to power supply issues; peat restoration activity caused wind-blown peat particulate interference with Li-7200 spectral response; COVID travel restrictions delayed on-site repairs until Aug 2020, resulting in discarded NEE and LE data until mid-August 2020.
- Site-specific considerations: bare peat gullies and erosion impact flux footprint; canopy height treated as static; fetch and wind-direction limitations noted.
- The dataset relies on standard, recognized processing and QC methods (Mauder et al., Reichstein et al., etc.) to ensure reproducibility and comparability with other eddy covariance datasets.

## Uses, governance and provenance
- Purpose: supports analysis of carbon flux dynamics in a degraded peatland, including partitioning of NEE into GEP and TER and assessment of energy exchanges.
- Data governance: follows established micrometeorology QC/processing workflows; gap-filling and uncertainty estimation are clearly documented; metadata links to foundational methodological literature.
- Provenance: authored by Rebekka Artz, Mhairi Coyle, Gillian Donaldson-Selby, and Ross Morrison; dataset is an incremental deposit with updates and related documentation.