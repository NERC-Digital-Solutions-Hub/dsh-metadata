# CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13

## Overview
- Dataset captures CO2 efflux, hydraulic parameters, and water chemistry across six field sites (two in Scotland, four in the Amazon) over multiple years to cover a range of seasons and flow conditions.
- Measurements are taken at locations within each site to sample a range of flow intensities.

## Study Sites and Periodicity
- Scotland
  - River Kelvin (RK): 335 km2 semi-urban catchment; sampling in a 30 m reach upstream of Clyde estuary; data collected Jun 2012–Dec 2013 (weekly to every three weeks).
  - Drumtee Water (DW): 9.6 km2 peat-dominated catchment; 19 m reach; data collected Jun 2012–Dec 2013 (weekly to every three weeks).
- Amazon (Tambopata National Reserve, Peru)
  - Main Trail (MT): ~5 km2 catchment; sampling during the rainy season; campaigns Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012.
  - New Colpita (NC): 7 km2 perennial stream; campaigns Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012.
  - La Torre river (LT): 2000 km2 catchment; sampling near confluence with Tambopata; similar campaign windows as MT/NC.
  - Tambopata river (TP): 14,000 km2 catchment; sampling near 200 m-wide channel; campaigns within 2011–2012.
- Note: MT, NC, LT, TP were sampled during three field campaigns spanning wet and dry seasons; RK and DW were sampled regularly over 2012–2013 to cover all seasons.

## Measurements and Methods
- CO2 efflux
  - Measured with a floating chamber (volume 0.0029 m3) connected to a LICOR LI-840A IR analyzer.
  - Internal circulation with a Schego pump (0.3–1.0 L min-1); CO2 accumulation measured over four minutes, repeated three times.
  - Flux calculated from CO2 accumulation rate using FCO2 = (δCO2/δt) × (V / (R × T × S)).
  - Additional qualitative surface state assessment at UK sites: smooth, medium, or rough water surface; wind not directly measured.
- Hydraulic parameters
  - Velocity measured with a Valeport flow meter at 20% and 80% of flow depth and three additional heights to identify outliers; depth-averaged mean velocity (ū) used for Fr and Re.
  - Fr (Froude number) = ū / sqrt(gH); Re (Reynolds number) based on water depth and kinematic viscosity.
- Water chemistry
  - pH and conductivity logged in various configurations (continuous logging at DW, MT, NC; spot measurements at LT, TP).
  - For RK, pH was derived from a discharge–pH relationship due to equipment malfunction.
  - [DIC] determined from triplicate samples collected within 15 minutes of flux measurements; analyses done with GasBench/Delta V Plus; pCO2 calculated from [DIC], pH, and temperature.
  - Temperature measured with handheld thermometers or Troll probes; air temperature recorded where applicable.
- Instrument calibration
  - Troll 9000 pH probe calibrated ~every 5 weeks (pH4 and pH7).
  - Troll 9500 pH probe calibrated ~monthly (pH4 and pH7); electrolyte top-ups and field cleaning as needed.
  - Regular quality checks with standards for [DIC] measurements and drift monitoring.

## Data Structure and Content
- File: CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13 (CSV).
- 11 columns:
  - Date (dd/mm/yyyy)
  - Region (Amazon or Scotland)
  - Site (stream name)
  - Mean CO2 efflux (µmol CO2 m-2 s-1)
  - SD of mean CO2 efflux
  - Flow (m s-1)
  - Water depth (m)
  - pCO2 (µatm)
  - [DIC] (mM C)
  - pH
  - Water temperature (°C)
- Data notes
  - Missing values indicated as NA.
  - Some data gaps due to equipment malfunction, or in MT where streams dry up seasonally.
  - DIC samples collected within 15 minutes of flux measurements; pCO2 calculated from DIC, pH, and temperature.

## Quality Control and Limitations
- Data collection targeted parallel measurement of CO2 flux, hydraulics, and chemistry to enable explanatory modeling of CO2 efflux.
- Known data gaps:
  - DW and RK lack [DIC] and pCO2 data from June 2012 to January 2013.
  - MT dries during the dry season; no samples Sept–Nov 2011.
- Some sites required discharge-based pH estimation (RK) due to equipment issues.
- Instrument calibration and drift monitored through periodic calibrations and standard checks.

## Notes on Use and Governance
- Dataset is suitable for analyzing links between hydraulic conditions, surface gas exchange, and aquatic carbon chemistry across tropical and temperate fluvial systems.
- Metadata includes site-specific details, sampling cadence, measurement protocols, calibration procedures, and data quality notes, supporting reproducibility and cross-site comparability.
- References provided for measurement methods and calibration standards.