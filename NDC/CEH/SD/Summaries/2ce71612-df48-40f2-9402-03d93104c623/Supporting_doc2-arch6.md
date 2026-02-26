# Supporting documentation

## Overview
- Describes a simulation of carbon and nitrogen dynamics in the Sunjia catchment, Jinaxi province, Southeast China.
- Two-year daily simulations using a pool-based ECOSSE model.
- Outputs a daily time series of soil organic carbon and nitrogen in 5 cm layers, plus daily soil fluxes.
- Driven by measurements from the Sunjia Cropping and Observational (CZO) site; outputs intended for understanding soil biogeochemistry under local crops and climate.

## Data sources and study site
- Sunjia CZO location: Jiangxi Province, SE China (approx. 116°05′30″E, 28°05′30″N); area ~50 ha; elevation 41–55 m.
- Land cover: peanuts ~50% of area; citrus trees ~17%; typical crops of the area.
- Cropping management: peanuts ploughed annually (affecting soil structure); citrus is perennial with deeper roots.
- Soil parent material: kaolinitic quaternary red clay; soil extent ~101.9 ha beyond CZO.
- Climate: subtropical with distinct rainy/dry seasons; average annual rainfall ~1884 mm (measurement period 2012–2013 ~1584 mm).
- Measurements used to drive simulations:
  - Soil data: measured at 4 depths (0.05, 0.2, 0.4, 0.8 m) for each crop type; bulk density, C content, N content.
  - Weather data: hourly measurements of temperature, precipitation, humidity, wind speed; potential evapotranspiration via Penman–Monteith from site station.
- Simulation period: 2014 (Year 1) and 2015 (Year 2).

## Model and inputs
- Model: ECOSSE (pool-based carbon and nitrogen turnover) with base decomposition rates modulated by decomposition drivers.
- Inputs:
  - Soil data by crop type and depth (bulk density, C, N).
  - Weather data from a single monitoring station (hourly).
  - Depth considered: soil profile up to 3 m (as outputs are reported for the full simulated profile).
- Outputs are provided as annualized totals per day across the 3 m profile, with units converted to kg/ha for most pools and mm for available water.

## Data outputs and structure
- Daily outputs for 2014 (Year 1) and 2015 (Year 2) including:
  - Decomposable plant material: dpm_c_kg/ha
  - Recalcitrant plant material: rpm_c_kg/ha
  - Biomass carbon: bio_c_kg/ha
  - Humus: hum_c_kg/ha
  - Total soil organic carbon: total_soc_kg/ha
  - Carbon dioxide emitted: co2_c_kg/ha
  - Total soil organic nitrogen: total_son_kg/ha
  - Ammonium nitrogen: nh4_n_kg/ha
  - Nitrate nitrogen: no3_n_kg/ha
  - Denitrified nitrogen: denitrified_n_kg/ha
  - Nitrification nitrogen: nitrification_n_kg/ha
  - Nitrous oxide emissions: n2o_n_kg/ha
  - Nitrogen oxide nitrogen: no_n_kg/ha
  - Available water in soil: avail_water_mm
- Data conventions:
  - All units are kg/ha except avail_water_mm (mm).
  - Day represents day of year; Year indicates Year 1 or Year 2.
- Primary data file:
  - Short_SIM.csv: outputs from a short simulation of carbon turnover for the Southeastern China catchment.

## Data quality and provenance
- Quality control:
  - Input files checked for missing or incorrect data.
- Provenance:
  - Data derived from Sunjia CZO measurements and site-specific weather observations, integrated into the ECOSSE model to generate the daily soil carbon and nitrogen dynamics.

## Access and usage notes
- The dataset provides a time-resolved view of soil C and N dynamics under local cropping systems.
- Useful for researchers or practitioners interested in soil biogeochemistry, model validation, or local-scale carbon and nitrogen budgeting.
- Given the one-station weather data source and crop-specific inputs, users should consider site representativeness and potential need for additional meteorological or management data for broader application.