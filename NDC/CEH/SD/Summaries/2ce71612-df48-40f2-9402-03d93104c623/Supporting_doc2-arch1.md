# Supporting documentation

## Objective and approach
- Simulate carbon and nitrogen dynamics in the Sunjia catchment, Jinaxi province, Southeast China, using an established pool-based ECOSSE model.
- Produce daily simulations of soil organic carbon and nitrogen across 5 cm soil layers, plus daily soil fluxes.
- Calibrate and drive simulations with site measurements from Sunjia CZO for 2014 (year 1) and 2015 (year 2).

## Study site and crops
- Sunjia CZO location: Jiangxi Province, SE China (approx. 116°5′30″E, 28°5′30″N); area ~50 ha; elevation 41–55 m.
- Land cover: peanuts ~50% of area; citrus trees ~17%; crops are representative of the region.
- Crops characteristics: peanuts are annual with shallow rooting and ploughing each year; citrus is perennial with deeper roots.

## Climate, soils, and context
- Climate: subtropical with distinct rainy and dry seasons; average annual rainfall ~1884 mm (observed ~1584 mm Oct 2012–Dec 2013).
- Parent material: kaolinitic quaternary red clay (extending beyond the CZO).
- Soil data collected at 4 depths (0.05, 0.2, 0.4, 0.8 m) across 5 points per crop type; measurements include bulk density, C content, and N content.

## Data inputs and model structure
- Weather inputs: hourly temperature, precipitation, humidity, wind speed from a single monitoring station; potential evapotranspiration via Penman–Monteith.
- Model: ECOSSE, a pool-based soil carbon and nitrogen model; each pool has a base decomposition rate altered by decomposition drivers.
- Depth coverage for outputs: entire simulated soil profile up to 3 m.
- Units: outputs generally in kilograms per hectare (kg/ha) except available water (avail_water_mm) in millimeters (mm).

## Model inputs and outputs
- Inputs fed into ECOSSE:
  - Soil data: 5 points per crop type, 4 depths; variables include bulk density, C content, N content.
  - Weather data: hourly measurements; PET via Penman–Monteith.
- Outputs produced by the model (daily timesteps):
  - Pools: decomposable plant material (dpm_c_kg/ha), recalcitrant plant material (rpm_c_kg/ha), biomass carbon (bio_c_kg/ha), humus (hum_c_kg/ha), total soil organic carbon (total_soc_kg/ha).
  - Gaseous and dissolved fluxes: CO2 emitted (co2_c_kg/ha).
  - Nitrogen pools: total soil organic nitrogen (total_son_kg/ha), ammonium (nh4_n_kg/ha), nitrate (no3_n_kg/ha), denitrified nitrogen (denitrified_n_kg/ha), nitrification nitrogen (nitrification_n_kg/ha), nitrous oxide (n2o_n_kg/ha), nitric oxide/nitrogen oxide (no_n_kg/ha).
  - Hydrology: available water in soil (avail_water_mm).
- Simulation period and framing:
  - Year 1: 2014; Year 2: 2015.
  - Outputs reflect the entire 3 m soil profile.

## Data quality and provenance
- Input data undergo quality control to check for missing or incorrect values.
- Provided data artifact: Short_SIM.csv, representing outputs from a short simulation of carbon turnover in a small Southeast China catchment.

## Considerations for analysts
- Scale and data limitations: single weather station, limited crop representation, and 3 m soil depth may affect local specificity.
- Data integration: ECOSSE requires harmonised soil and weather inputs; differences in crop management (e.g., peanut tillage) influence decomposition drivers.
- Outputs are day-level summaries across the full soil profile, enabling analysis of carbon and nitrogen dynamics, soil moisture, and gas emissions over the two-year period.