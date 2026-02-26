# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2013 to 2017

## Overview
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured over a Miscanthus x. giganteus plantation (Lincolnshire, UK).
- Data collected 2013-07-05 00:30 to 2017-11-07 00:00 using micrometeorological eddy covariance (EC) with an open-path system.
- Includes ancillary weather and soil physics observations and atmospheric turbulence variables.
- Raw 20 Hz EC observations processed to 30-minute averages using EddyPRO v6.1; includes quality control, corrections, and uncertainty estimates.
- Gap-filled and partitioned data provided for key fluxes (NEE, GEP, TER, LE, H) and meteorological variables, with -9999 indicating missing records.

## Study site
- Location: Miscanthus plantation near Lincoln, UK (53°19'10.07"N, 0°35'18.65"W), 11.5 ha mature commercial bioenergy plantation.
- Climate: temperate maritime; mean annual temp ~9.8°C and precipitation ~614 mm year-1 (1981–2010).
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; details on bulk density, texture, soil organic carbon, nitrogen, pH.
- Management: established 2006 on former arable land; annual spring harvests since 2008; soil amendments/inoculations applied during 2013–2016.

## Sampling regime
- Flux data: EC and micrometeorology above canopy using an open-path system on a tall mast; measurement height adjusted to ~2× canopy height.
- Sensors: R3 sonic anemometer, LI-7500 CO2/H2O infrared analyzer; data at 20 Hz; Ta and RH measured at 2 m with 0.1 Hz sampling; 30-minute means for meteorology.
- Ancillary data: net radiation (Rnet) and components, sunshine sensor, below-canopy PPFD, soil heat flux (G), soil moisture (VWC), soil temperature (Ts), precipitation; logged as 30-minute means or sums.

## Ancillary data acquisition
- Additional meteorological and soil observations from a scaffold tower.
- Instruments: CNR1 net radiometer, BF3 sunshine sensor, Tube Solarimeters for below-canopy PPFD, HFP01-SC soil heat flux plates, CS616 VWC sensors, PT107 soil thermocouples, tipping-bucket rain gauge.
- Data quality: 30-minute means; alignment with EC data for integrated analysis.

## Data processing
- Flux calculations: EddyPRO® Flux Calculation Software V6.1; 30-minute block-averaging.
- QC steps: outlier removal (median absolute deviation), non-stationarity checks, value range filters, nighttime NEE exclusions, friction velocity threshold (u* > 0.14 m s-1), footprint checks (≥75% within target ecosystem), visual inspection.
- Outputs: computed wind metrics (wind speed, direction, u*, TKE, L, z/L) and stability-related parameters.

## Quality control
- Statistical outliers removed; non-stationary periods excluded; fluxes filtered to within specified bounds for H, LE, and NEE.
- NEE treated with nighttime exclusions and footprint validation to ensure representativeness of the target ecosystem.
- All flux and ancillary data visually inspected weekly; clearly erroneous values removed.

## Data gap-filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled with Marginal Distribution Sampling (MDS).
- Gaps in key meteorological variables filled with linear relationships from neighboring weather stations.
- NEE partitioned into GEP and TER via Reichstein et al. (2005) approach, driven by Ta; gap-filled EC data and partitioning performed with REddyProc (R).
- Data products include both gap-filled fluxes and partitioned components.

## Details of data structure
- File: Lincolnshire_Bioenergy_Miscanthus_2013_2017.csv (single CSV time series).
- Time range: 2013-07-05 00:30 to 2017-11-07 00:00 (30-minute intervals).
- Missing records indicated by -9999.
- Outputs include:
  - NEE, NEE_sd, LE, LE_sd, H, H_sd, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd
  - TER, GEP
  - CO2_strg, LE_strg, H_strg, etc. (storage terms)
  - CO2_mol_density, H2O_mol_density, Pa, Ta, RH, SH, e, es, VPD, Tdew
  - SWin, SWin_total, SWin_diffuse, SWout, LWin, LWout, Rnet
  - PPFDbc1/2/3, G1/G2, Tsoil1/2, VWC1/2, Precipitation, Windspeed, Winddir
  - FootprintFraction, Ustar, TKE, Tstar, L, zL
- Variable descriptions and units aligned with LI-COR LI-7500 conventions and Reichstein et al. (2016)/REddyProc guidelines.

## Nature and units of recorded values
- Primary time-series columns (30-minute means): NEE, LE, H, and related uncertainty terms; NEE_filled and partitioned outputs (GEP, TER).
- Ancillary environmental variables include meteorological, radiation, soil, and footprint-related metrics with standard SI units (e.g., μmol CO2 m^-2 s^-1 for fluxes, W m^-2 for radiative fluxes, m s^-1 for wind, kPa for pressure, °C for temperatures).

## Acknowledgments
- Data collection funded by the Natural Environment Research Council; acknowledgments extended to landowners and support staff for eddy covariance instrumentation and field maintenance.