# CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13

- A field dataset containing CO2 efflux, hydraulic and water-chemistry data from six field sites (two in Scotland: River Kelvin and Drumtee Water; four in the Amazon: Madre de Dios/Tambopata region: Main Trail, New Colpita, La Torre river, Tambopata river) collected over multiple years to capture a range of seasons and flow conditions.
- Sites vary in location, catchment size and land use (semi-urban and agricultural in Scotland; predominantly rainforest with small-scale agriculture and gold mining in the Amazon).

## Field Site Details
- Scotland
  - River Kelvin (RK): 335 km2, semi-urban catchment, measurement reach ~30 m, near Clyde Estuary.
  - Drumtee Water (DW): headwater, peat-dominated, ~9.6 km2, rough grazing land.
- Amazon
  - Main Trail (MT): catchment ~5 km2, active only in the rainy season.
  - New Colpita (NC): perennial stream, ~7 km2.
  - La Torre river (LT): ~2000 km2 catchment, sampling near Tambopata confluence.
  - Tambopata river (TP): catchment ~14,000 km2, ~200 m wide channel near sampling point.

## Sampling Periodicity and Coverage
- RK and DW: regular sampling from June 2012 to December 2013 (weekly to monthly), spanning all four seasons and diverse flow conditions.
- MT, NC, LT, TP: field campaigns Feb-Apr 2011, Sept-Dec 2011, Mar-May 2012 (wet and dry seasons, varying water levels).

## Measurements and Methods

- CO2 Efflux
  - Measured with a floating chamber (volume 0.0029 m3) connected to a LI-840A IR gas analyzer.
  - Internal circulation with a Schego pump (0.3–1.0 L/min); CO2 accumulation tracked over four minutes, three repeats.
  - Flux calculation: F_CO2 = (δCO2/δt) × (V / (R × T × S)).
  - Surface area (S) corresponds to chamber-water interface; temperature is air temperature for gas calculations.
  - Additional qualitative surface state assessment in UK sites: smooth, medium, rough (wind effects implicitly included).

- Hydraulic Parameters (UK sites)
  - Velocity measured with Valeport flow meter (50 mm impeller), 60 s averaging, at 20% and 80% depth plus at least three other heights for outlier detection.
  - Key parameters: mean velocity (ū), Froude number (Fr), Reynolds number (Re).
  - Fr and Re used to relate hydrodynamics to gas exchange and mixing processes.
  - Amazon sites: near-surface velocity measured directly under the chamber at MT/NC/LT/TP; Fr and Re not available for these sites.

- Water Chemistry
  - pH, conductivity, temperature measured at the time of flux measurement; pH measured in situ where possible to minimize microbial alteration of samples.
  - DW: continuous pH logged at 30-minute resolution (MP Troll 9000).
  - RK: pH calculated from a discharge-pH relationship due to equipment issues (validated against upstream monitoring data).
  - MT/NC: 15-minute resolution pH, conductivity, temperature (Troll 9500).
  - LT/TP: spot measurements (pH, conductivity, temperature) during flux measurements; Trolls equilibrated for >20 minutes.
  - Dissolved Inorganic Carbon ([DIC]) sampled in triplicate within 15 minutes of flux measurement; analyzed later with Gas Bench/Delta V Plus.
  - pCO2 calculated from [DIC], pH, and temperature.
  - Troll 9000 (DW, calibrated ~every 5 weeks) and Troll 9500 (MT/NC/LT/TP, calibrated ~monthly).

- DIC and pCO2
  - [DIC] measured using pre-acidified exetainers and a Gas Bench/Delta V Plus; standards used to span expected concentrations; instrumental drift monitored with mid-range standards.

## Data Structure and Formats
- Dataset: 11-column Excel (.csv) file titled “CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13.csv”.
- Columns (examples):
  - Date (dd/mm/yyyy)
  - Region (Amazon or Scotland)
  - Site
  - Mean CO2 efflux (µmol CO2 m-2 s-1)
  - SD of mean CO2 efflux
  - Flow (m s-1)
  - Water depth (m)
  - pCO2 (µatm)
  - [DIC] (mM C)
  - pH
  - Water temperature (°C)
- Missing values are indicated as NA.
- All values are within method detection limits.

## Quality Control and Data Gaps
- Data gaps due to logistics and equipment:
  - [DIC] and pCO2 data missing at DW and RK from June 2012 to January 2013 (sampling for DIC started mid-Jan 2013 at DW/RK).
  - MT dries up in the dry season; no data Sep–Nov 2011 for MT.
  - Some missing data due to equipment failure or inaccessibility from high flows.
- Calibration and QA:
  - Troll pH meters calibrated in field using two-point buffers (pH4 and pH7); field cleaning performed at calibration.
  - DIC standards used to bracket sample concentrations; drift monitored with mid-range standards.

## Instrumentation and Calibration Details
- CO2 measurement: LI-840A IR analyzer; chamber circulation and 4-minute uptake protocol.
- pH meters: Troll 9000 (DW) and Troll 9500 (MT, NC, LT, TP) with regular two-point field calibrations.
- Temperature and conductivity: Troll meters and handheld thermometers; in-field equilibration practices described.
- DIC analysis: Thermo-Fisher Gas Bench/Delta V Plus; samples preserved with phosphoric acid and analyzed within 6 months.

## Potential Uses and Notes for Data Support
- Data can support analyses on CO2 efflux dynamics in rivers under varying hydrological conditions and land-use regimes.
- Useful for exploring hydraulic parameters as predictors of gas exchange (Fr, Re, mean velocity).
- Data gaps should be considered in models; cross-site comparability requires attention to different pH measurement approaches and DIC-derived pCO2 estimation.
- The dataset supports development of data products such as CO2 flux dashboards, site-specific flux models, and comparative analyses across tropical vs. temperate river systems.