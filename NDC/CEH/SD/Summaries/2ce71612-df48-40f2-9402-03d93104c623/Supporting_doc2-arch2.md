# Supporting documentation

## Aim
- Simulate carbon and nitrogen dynamics in the Sunjia catchment (Jiangxi Province, SE China) over two years using an established, pool-based carbon and nitrogen model (ECOSSE).
- Provide daily outputs of soil organic carbon and nitrogen across 5 cm soil layers and daily soil fluxes.
- Use Sunjia CZO measurements to drive the simulations.

## Study area and context
- Location: Sunjia catchment, Jiangxi Province, SE China (coordinates given in the document); area ~50 ha; elevation 41–55 m.
- Land cover: peanuts 50% and citrus 17% of the area; peanuts are annual with shallow roots and ploughed annually; citrus is perennial with deeper roots.
- Soil: kaolinitic quaternary red clay parent material extending beyond the CZO (regional soil context ~101.9 ha).
- Climate: subtropical with distinct rainy and dry seasons; average annual rainfall ~1884 mm (rainfall during measurement period was 1584 mm from Oct 2012 to Dec 2013).
- Purpose of measurements: drive and validate the ECOSSE simulations for soil carbon and nitrogen dynamics.

## Data and inputs
- Soil measurements: collected at 5 points per crop type across 4 depths (0.05, 0.20, 0.40, 0.80 m); inputs include bulk density, carbon content, and nitrogen content per depth and crop type.
- Weather data: hourly measurements of temperature, precipitation, humidity, and wind speed from a single monitoring station at the Sunjia catchment.
- Evapotranspiration: potential evapotranspiration calculated using the Penman–Monteith method.
- Model: ECOSSE, a pool-based carbon and nitrogen turnover model; each pool has a base decomposition rate modified by drivers.
- Simulation scope: outputs for 2014 (Year 1) and 2015 (Year 2), with the entire soil profile up to 3 m depth.
- Outputs units: most pools in kg/ha; available water in mm.
- Data quality: input files undergo quality control to check for missing or incorrect data.

## Model structure and outputs
- Model framework: ECOSSE simulates turnover of soil carbon and nitrogen from multiple pools (e.g., decomposable plant material, recalcitrant plant material, biomass carbon, humus) with parameters per pool and driver effects.
- Outputs presented: daily values for soil organic carbon, soil organic nitrogen, and fluxes such as carbon dioxide emitted; available water is reported as a soil moisture metric.
- Variables included (examples): dpm_c_kg/ha (decomposable plant material carbon), rpm_c_kg/ha (recalcitrant plant material), bio_c_kg/ha (biomass carbon), hum_c_kg/ha (humus), total_soc_kg/ha (total soil organic carbon), co2_c_kg/ha (CO2 emitted), total_son_kg/ha (total soil organic nitrogen), nh4_n_kg/ha (ammonium), no3_n_kg/ha (nitrate), denitrified_n_kg/ha, nitrification_n_kg/ha, n2o_n_kg/ha, no_n_kg/ha, avail_water_mm (available water in soil).
- Data package: includes a Short_SIM.csv with outputs from a short simulation of carbon turnover in a small catchment.

## Quality assurance and data management
- Quality control steps ensured data completeness and correctness prior to model input.
- Outputs are structured to support standardized interpretation and integration with other monitoring outputs (e.g., charts, maps), facilitating assessment of environmental health and policy performance over time.

## Relevance for environmental monitoring
- Demonstrates how field measurements feed a standardized, repeatable modelling workflow to monitor soil carbon and nitrogen dynamics.
- Provides a framework to combine site-specific monitoring data with process-based modelling to assess environmental health and inform policy-relevant insights over multi-year timescales.