# Sampling Regime

## Overview
- Data from two small streams (MT - Main Trail; NC - New Colpita) in the Western Amazonian Tambopata National Reserve, Madre de Dios, Peru (approx. 12°49'54.30"S, 69°16'52.37"W).
- Timeframe: February 2011 to October 2012.
- Focus: Continuous water chemistry and hydrology, with targeted field campaigns for dissolved inorganic carbon (DIC), dissolved organic carbon (DOC), and particulate organic carbon (POC) to understand hydrological controls on carbon concentrations and fluxes.
- Output aims to support long-term environmental monitoring and policy-relevant assessment of carbon dynamics in tropical stream systems.

## Sampling Design and Study Sites
- MT (Main Trail): seasonally active; width 3.5–5 m; drains ~4.9 km² upstream.
- NC (New Colpita): flows also during the dry season; width 4.5–7.5 m depending on water level; drains ~7.2 km² upstream.
- Sampling point distinctions reflect differing hydrological regimes to capture seasonal and flow-condition variability.

## Data Collected and Variables
- Water chemistry: pH, temperature, dissolved oxygen (% saturation), electrical conductivity (µS/cm).
- Hydrology: stage height (cm), flow velocity (m/s) at a fixed point, stream discharge (m³/s) derived from velocity and cross-section data.
- Carbon: DIC (mg/L), DOC (mg/L), POC (mg/L).
- Temporal resolution: 15-minute time steps (continuous), with additional field campaigns for grab measurements during specific flow conditions.

## Methods and Instrumentation
- In-field instruments: Troll 9500 (pH, temperature, DO, conductivity), Rugged Troll (stage height), Flowlink2150 (flow velocity); supplementary hand-held flow meter at the flux chamber site.
- Cross-sections: detailed measurements used to convert stage height and velocity to discharge.
- CO2 data: additional CO2 efflux and pCO2 data available from a related dataset (Hazel Long et al., 2011–2013).

## Field Sampling and Laboratory Analysis
- DIC: collected in pre-acidified evacuated exetainers; headspace method with isotopic composition (δ13C) measured via Thermo-Fisher Gas Bench/Delta V Plus.
- DOC: collected in poly bottles, filtered (GF/F 0.7 µm), acidified to pH ~3.9, degassed, and analyzed by combustion (TOC analyzer).
- POC: determined by loss on ignition after drying and combustion of filter papers; assumes ~50% organic carbon content.
- Calibration and drift checks: multi-point calibrations for DIC/DOC; isotopic standards included; midrange standard used to check instrumental drift.

## Data Structure and Access
- Time series with 15-minute resolution; missing values marked as NA.
- CSV files:
  - Perennial_stream_NC: NC time series.
  - Seasonal_stream_MT: MT time series.
- Core columns (example): Site, Date (dd/mm/yyyy), Time (hh:mm:ss), Temperature (°C), pH, Oxygen saturation (%), Conductivity (µS/cm), Stage height (cm), DIC (mg/L), DOC (mg/L), POC (mg/L), Flow velocity at measurement site (m/s), Velocity (m/s) from stage calculation, Discharge (m³/s).

## Quality Control and Uncertainty
- Data gaps due to instrument malfunctions:
  - Perennial NC pH gap: 1 Jul–7 Sep 2011; gap filled with model-based estimates using conductivity and stage height (MICE in R).
  - MT data: larger gaps in 2012 due to instrument problems; presented in non-gap-filled form.
- Flood-related issues:
  - During high water, rating curves produced unrealistically high velocities; velocity/ discharge adjusted downward linearly from maximum observed velocity until stage height limit is reached.
- Sensor reliability notes:
  - NC stream pressure sensor: August–October 2012 shows lack of event peaks despite rainfall; stage height-derived metrics should be treated with caution.
  - NC oxygen saturation: intermittent very low readings (<60% in modelling datasets) likely due to probe fouling; readings below 60% flagged as cautious.
- Overall, data quality notes emphasize cautious interpretation of affected periods and the use of model-assisted gaps where appropriate.

## Related Data and References
- Related CO2 flux and hydraulic data for Amazonian streams available from Hazel Long et al. dataset (2011–2013).
- Analytical and calibration methods align with standard approaches for carbon concentration measurements; methodological details discussed in Waldron et al. (2014) on DIC isotopic analyses.