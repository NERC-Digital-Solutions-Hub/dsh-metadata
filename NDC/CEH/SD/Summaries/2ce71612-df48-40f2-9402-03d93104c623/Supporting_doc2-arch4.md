# Supporting documentation

## Overview
- Describes a simulation of carbon and nitrogen dynamics in the Sunjia catchment, Jinaxi province, Southeast China, using the ECOSSE pool-based model.
- Two-year study period with daily outputs: soil organic carbon (SOC) and nitrogen (SON) in the soil, across 5 cm layers, plus daily soil fluxes.
- Outputs cover the entire simulated soil profile to 3 m depth and are driven by measurements from the Sunjia CZO.

## Study area and data context
- Sunjia CZO location: Jiangxi Province, SE China (approx. 116°5′30″E, 28°5′30″N); area 50 ha; elevation 41–55 m.
- Land use: peanuts ~50% of area; citrus trees ~17%; peanut soil managed by annual ploughing.
- Climate: subtropical with distinct rainy/dry seasons; average annual rainfall ~1884 mm (study period 1584 mm).
- Soil parent material: kaolinitic quaternary red clay (extends beyond CZO to ~101.9 ha).
- Moisture data: October 2012–December 2013; measurements during a slightly below-average rainfall period.
- Data provenance: measurements and samples obtained from Sunjia CZO; crops and soil properties used as inputs to the model.

## Data and model approach
- Model: ECOSSE (pool-based carbon and nitrogen turnover) with a structured pool system and decomposition drivers.
- Temporal resolution: daily time steps; outputs describe a full soil profile (up to 3 m).
- Output scope: carbon and nitrogen pools, fluxes (including CO2 emissions) across soil layers and pools.
- Inputs described in detail (below) to drive the ECOSSE model and generate outputs.

## Data inputs
- Soil data inputs:
  - Collected at 5 points per crop type across depths 0.05, 0.2, 0.4, and 0.8 m (total of four depths reported).
  - Measured properties: bulk density, carbon content, and nitrogen content.
  - Depth- and crop-specific averages used as ECOSSE inputs.
- Weather data:
  - Hourly measurements of temperature, precipitation, humidity, and wind speed from a single monitoring station at the Sunjia catchment.
  - Potential evapotranspiration estimated using the Penman-Monteith method from local measurements.
- Output scope and units:
  - All outputs expressed as kg/ha for soil carbon and nitrogen pools (except available water, which is in mm).
  - Outputs cover the entire soil profile (up to 3 m).
  - Day, year, and pool fluxes are clearly labeled (e.g., dpm_c_kg/ha, rpm_c_kg/ha, bio_c_kg/ha, hum_c_kg/ha, total_soc_kg/ha, total_son_kg/ha, co2_c_kg/ha, n2o_n_kg/ha, avail_water_mm).

## Model outputs
- SOC and SON distributions by pool and depth, updated daily.
- Carbon and nitrogen fluxes including emissions (CO2, N2O) and transformations (nitrification, denitrification).
- Available soil water content (avail_water_mm) for the simulated profile.
- Two-year simulation labeled as Year 1 (2014) and Year 2 (2015) with daily results.

## Quality control and data provenance
- Inputs checked for missing values and data integrity prior to running simulations.
- File referenced: Short_SIM.csv, containing outputs from a short simulation of carbon turnover for a small Southeast China catchment.

## Data assets and file list
- Short_SIM.csv: outputs from a short simulation of carbon turnover in a small catchment in Southeast China.