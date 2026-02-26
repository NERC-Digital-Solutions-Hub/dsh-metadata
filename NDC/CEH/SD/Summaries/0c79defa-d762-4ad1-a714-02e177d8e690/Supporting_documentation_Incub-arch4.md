# Laboratory soil incubation respiration rates from permafrost in subarctic Canada

## Overview
- Study of laboratory soil incubations to quantify gas production rates with depth along the soil profile in subarctic Canada.
- Samples collected from three soil cores per site, with four depths per core (coded A–D; A is shallowest).
- Sites include FFU (FireFox Unburnt), FFB (FireFox Burnt, 1998), BLF (BlackFox), WHF (WhiteFox), TPP (Teslin Peatland Plateau), and TW (Teslin Wetland); TW includes permafrost-related peatland features.
- Depths include active layer and permafrost; any permafrost labeling noted in dataset.

## Sampling design and sites
- For each site: 3 soil cores; 4 depths per core (A–D).
- Depth-specific columns include soil_depth_interval_cm and Permafrost status.
- Samples prepared by removing top vegetation and large roots; mineral soil sieved to remove pebbles as needed.
- Replication: 3 replicates per site (column 'replicate').

## Experimental setup and measurements
- Incubations conducted under both oxic (aerobic) and anoxic (anaerobic) conditions.
- Temperatures: 5°C and 15°C.
- Moisture: soils kept at water holding capacity; extra water added for anaerobic saturations.
- Aerobic incubations:
  - 0.5 L glass jars with soil in 0.5 L jars.
  - CO2 measured at time 1 and time 2 (within 24 h for high-temperature treatments, TPP and TW; 48 h for low-temperature).
  - Instrument: EGM-4 Infrared Gas Analyzer (PP Systems).
  - Time 2 measurements followed by dilution corrections to reflect real jar concentrations.
- Anaerobic incubations:
  - Jars flushed with N2 at start and where gas accumulation was greatest.
  - 30 mL headspace sampled and analyzed for CO2 (EGM4) and CH4 (DP-IR Detecto Pak).
  - Dilution corrections applied to reflect real concentrations.
- Gas production rates calculated from the difference between time 1 and time 2 concentrations, assuming linear increase.
- Productivity units: mg of C (as CO2 or CH4) per day per gram of dry soil.
- Carbon and nitrogen contents provided as a percentage of dry mass.

## Data processing and calculations
- Headspace concentrations corrected using dilution calculations for both aerobic and anaerobic setups.
- Production rates expressed as mg C per day per gram dry soil.
- Data include both CO2 and CH4 production rates; conversion assumes linear accumulation between measurements.
- Note on units: carbon content (%) refers to dry mass basis; nitrogen content (%) likewise.

## Key variables and data products
- site code (e.g., FFU, FFB, BLF, WHF, TPP, TW)
- replicate (1–3)
- soil_layer (A–D; depth index)
- soil_depth_interval_cm (depths corresponding to layers)
- Permafrost (status label for that layer; TW note explains peatland permafrost history)
- incubation_condition (aerobic/anaerobic)
- temperature_C (5 or 15)
- time1_measurement_co2, time2_measurement_co2
- time1_measurement_ch4, time2_measurement_ch4
- production_rate_C_mg_per_g_day (CO2)
- production_rate_CH4_mg_per_g_day (CH4)
- soil_carbon_content_percent, soil_nitrogen_content_percent

## Permafrost note
- In TW site, layers D labeled as permafrost; these samples come from a wetland formed by permafrost thaw where the peat is considered permafrost-bearing below the active layer.

## Data quality, access, and use considerations for Data Leaders
- Data are multi-site, depth-resolved, and replicate-based, enabling comparisons of gas production by depth, site type, and permafrost influence.
- Metadata completeness needed for discovery: site codes, depth intervals, permafrost labeling, replicate IDs, incubation conditions, and measurement timings.
- Challenges analogous to data governance: scattered data sources, need for consistent metadata standards (depth, permafrost status, measurement times), and clear data provenance for reproducibility.
- Potential uses: modeling soil carbon fluxes, understanding depth- and permafrost-related gas production, cross-site comparisons of aerobic vs. anaerobic pathways, and informing data sharing across networks studying subarctic soils and permafrost dynamics.