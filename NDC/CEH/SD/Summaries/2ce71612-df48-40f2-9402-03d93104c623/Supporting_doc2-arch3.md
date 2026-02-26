# Supporting documentation

- Purpose and scope
  - Simulated carbon and nitrogen dynamics in the Sunjia catchment, Jinaxi province, Southeast China.
  - Two-year daily simulations of soil organic carbon and nitrogen across 5 cm soil layers.
  - Outputs include daily soil carbon and nitrogen fluxes and related metrics to support environmental monitoring and decision-making.

- Modelling approach
  - Uses an established pool-based ECOSSE model to represent turnover of soil carbon and nitrogen.
  - Model structure includes multiple pools (e.g., decomposable material, recalcitrant material, biomass carbon, humus) with base decomposition rates driven by environmental factors.
  - Simulations cover 2014 (Year 1) and 2015 (Year 2), with results for the entire simulated soil profile (up to 3 m depth).
  - Outputs are provided as kg/ha for most variables and mm for available water.

- Data inputs and site context
  - Sunjia CZO data collected in Jiangxi Province (50 ha site) with crops dominated by peanuts (50%) and citrus trees (17%).
  - Peanut crops are annual with shallower roots; citrus is perennial with deeper roots; peanut fields ploughed annually.
  - Soil parent material: kaolinitic quaternary red clay; soil data collected at 5 points per crop type across depths of 0.05, 0.2, 0.4, and 0.8 m.
  - Measured inputs: bulk density, soil carbon content, soil nitrogen content at the specified depths.
  - Weather data: hourly measurements (temperature, precipitation, humidity, wind speed) from a single Sunjia monitoring station; potential evapotranspiration calculated using Penman-Monteith.
  - Site climate: subtropical with distinct wet/dry seasons; average annual rainfall ~1884 mm (recorded 2012–2013 as 1584 mm).

- Outputs and metrics
  - Daily outputs for soil organic carbon and soil nitrogen components across 5 cm layers; includes total soil organic carbon (total_soc_kg/ha) and total soil organic nitrogen (total_son_kg/ha).
  - Carbon and nitrogen pool components: decomposable plant material (dpm_c_kg/ha), recalcitrant plant material (rpm_c_kg/ha), biomass carbon (bio_c_kg/ha), humus (hum_c_kg/ha).
  - Fluxes and processes: CO2 emissions (co2_c_kg/ha), denitrification (denitrified_n_kg/ha), nitrification (nitrification_n_kg/ha), nitrate (no3_n_kg/ha), ammonium (nh4_n_kg/ha), nitric oxide (no_n_kg/ha), nitrous oxide (n2o_n_kg/ha).
  - Available soil water (avail_water_mm) and related soil moisture dynamics.
  - Data formatting and units: all outputs in kg/ha except avail_water_mm (mm).

- Quality control and data management
  - Input files were checked for missing or incorrect data.
  - Included a short simulation dataset (Short_SIM.csv) for carbon turnover in a small Southeast China catchment.
  - Considerations raised for data governance, metadata, and openness of underlying datasets to support reuse and transparency.

- Relevance for monitoring frameworks
  - Demonstrates how to combine field measurements, site-specific weather data, and a process-based model to generate continuous environmental health indicators for policy scrutiny.
  - Provides a reproducible workflow for deriving daily soil carbon and nitrogen metrics across soil layers, useful for evaluating management practices and policy impacts.
  - Highlights data governance considerations: data availability, metadata adequacy, data transformation needs, and sharing challenges.
  - Addresses practical challenges relevant to monitoring frameworks, including data gaps, data access, siloed information, up-to-date data maintenance, and transparent communication of complex model outputs.