# Data consist of modelled maritime fuel demand projections at 1,377 ports globally for the year 2050

## Overview
- Modelled port-level fuel demand projections for 2050, covering 1,377 ports globally.
- Data provide input to Verschuur et al. (2024) and include full model code (link provided).
- Aimed at supporting environmental monitoring and policy performance assessment over time through standardised outputs.

## Method

### Vessel fuel consumption
- Based on vessel characteristics: deadweight tonnage (DWT), main engine horsepower, and operational speed.
- Regression models (one per vessel type) predict daily fuel consumption (tonnes/day) using DWT, horsepower, and speed (V) as predictors; functional form includes V^3.
- Training data from IHS Markit for ~19,000 vessels; good fit with R^2 0.93–0.98.
- Applied to 41,600 vessels with complete data; for remaining vessels, a DWT-only regression estimates V and P with R^2 0.54–0.86.
- Daily fuel consumption is converted to per-km consumption by dividing by vessel speed (tonnes/km), yielding a vessel-level fuel dataset for 97,500 vessels.

### Transport and fuel demand model
- Uses AIS data (2019) for 97,500 vessels, constructing port-to-port visits across 1,377 ports with inter-port distances.
- Route fuel demand = vessel fuel per km × route distance; global port fuel demand is allocated to the origin port (assumes bunkering fuel sourced from the port just visited before departure).
- This creates a present-day baseline fuel demand framework suitable for future projection.

### Future fuel demand
- Projected by scaling 2019 fuel demand by changes in port throughput for 2050.
- Throughput changes are derived from OxMarTrans, a global maritime transport model that simulates bilateral trade route allocations under various decarbonisation and growth scenarios.
- Present-day port-level fuel demand scaled by throughput changes per port and per vessel type to yield 2050 projections.
- Conversion to ammonia fuel: apply fleet adoption rates and a conversion factor where 1 tonne of HFO energy ≈ 2.07 tonnes of ammonia.

## Data quality check
- Regression-based vessel fuel estimates show strong empirical support; 2019 global fuel consumption estimated at 233 MMt/yr, aligning with IMO’s 213 MMt/yr estimate (the difference attributed to dataset size and inclusion of additional vessel types, e.g., passenger ships).
- Validation against IMO data is used to corroborate baseline estimates.

## Files

### port_reference.csv
- Port metadata for 1,377 ports, enabling geographic joins.
- Columns: Id, Name, Port_name, Country, Iso3, Region, Sub-region, X (lon), Y (lat), Geometry (point location).

### fuel_demand_port_2050_1000km.csv
- Port-level fuel demand scenarios for 2050 per vessel type, excluding trips shorter than 1000 km (assumed to be electrified).
- Includes 14 future trade scenarios (Table 1): combinations of SSPs, RCPs, and trade liberalization (Multilateral/Regionalization).
- Key columns: Id, Scenario, Name, Iso3, Continent_code, vessel_type_main, throughput_factor, Fuel_tons_route, Fuel_tons_route_slow, Fuel_tons_route_future, Fuel_tons_route_slow_future.

## Scenario context
- Table 1 lists the 14 future trade scenarios used, defined by SSP, RCP, and trade liberalization format (Multilateral vs Regionalization).

## Reproducibility and references
- Full model code and data deposit available (Mendeley link).
- References include Verschuur et al. (2023, 2024) and IMO (2021), among others, supporting model components and validation.