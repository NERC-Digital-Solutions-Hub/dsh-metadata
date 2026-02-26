# Supporting documentation

## Overview
- Simulates carbon and nitrogen dynamics in the Sunjia catchment, Jinaxi province, Southeast China.
- Uses a two-year, pool-based ECOSSE model to produce daily soil organic carbon and nitrogen for 5 cm layers.
- Outputs include daily soil carbon and nitrogen for the full 3 m soil profile and daily fluxes.

## Study site and data sources
- Sunjia CZO location: Jiangxi Province, SE China (116°5′30″E, 28°5′30″N); area 50 ha; elevation 41–55 m.
- Land cover: peanuts ~50% of area; citrus trees ~17%.
- Soil parent material: kaolinitic quaternary red clay (area extends beyond CZO to 101.9 ha).
- Climate: subtropical with distinct rainy/dry seasons; average rainfall ~1884 mm/year (measured 1584 mm Oct 2012–Dec 2013).
- Crop management: peanuts ploughed annually (affecting soil structure); citrus is perennial with deeper roots.
- Data inputs: soil measurements at 5 points for each crop type, at depths 0.05, 0.2, 0.4, 0.8 m; measured bulk density, C content, N content.
- Weather data: hourly readings (temperature, precipitation, humidity, wind) from a single Sunjia station; PET calculated with Penman–Monteith.

## Model and inputs
- Model: ECOSSE (pool-based carbon and nitrogen turnover) with base decomposition rates adjusted by drivers.
- Depth and scope: outputs refer to the entire simulated soil profile to 3 m depth.
- Input handling: average values across the 5 points per crop type used as model inputs.
- Output scope: daily timesteps; years 2014 (Year 1) and 2015 (Year 2).

## Outputs and variables
- Carbon pools (kg/ha): dpm_c_kg/ha, rpm_c_kg/ha, bio_c_kg/ha, hum_c_kg/ha, total_soc_kg/ha.
- Nitrogen pools (kg/ha): total_son_kg/ha, nh4_n_kg/ha, no3_n_kg/ha, denitrified_n_kg/ha, nitrification_n_kg/ha, n2o_n_kg/ha, no_n_kg/ha.
- Water: avail_water_mm (available water in soil).
- GHG emissions: co2_c_kg/ha.
- Metadata: Day (day of year), Year (Year 1 or 2), units fields documented.
- Output file: Short_SIM.csv (outputs from a short simulation).

## Quality control
- Input data checked for missing values and incorrect data prior to modeling.

## GIS relevance and considerations
- Outputs are suitable for conversion into GIS-ready time-series layers or rasters (soil carbon, nitrogen, water, and CO2 fluxes) for mapping and analysis.
- Spatial applicability: single 50 ha catchment; may require aggregation to subcatchments or gridded formats for standard GIS workflows.
- Data integration: can be combined with land-cover, topography, and crop maps to produce spatially explicit maps of soil biogeochemical dynamics.
- Metadata needs: clear documentation of units, depth layering, and temporal resolution (daily) for interoperability and reuse.

## Limitations and caveats
- Spatial replication limited to one site; inputs averaged across 5 measurement points per crop type.
- Simulation spans two years (2014–2015); not long-term dynamics.
- Outputs cover up to 3 m depth; input soil data extend to 0.8 m for some properties.