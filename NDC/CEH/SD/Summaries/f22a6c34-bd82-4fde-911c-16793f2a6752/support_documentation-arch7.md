# Data deposit: Modelled maritime fuel demand projections at 1,377 ports globally for 2050

## Overview
- Global port-level fuel demand projections for 2050, used as input to Verschuur et al. (2024).
- Covers 1,377 ports with geolocated data and port metadata; projections span 14 future trade scenarios.
- Based on vessel-level fuel consumption estimates derived from AIS data (approx. 97,500 vessels) and port-to-port movement.
- Full model code and data deposit available via Mendeley dataset.

## Method

### Vessel fuel consumption
- Vessel fuel use estimated per kilometre traveled using vessel-type-specific regression on daily fuel consumption (FC) with explanatory variables: deadweight tonnage (DWT), installed engine horsepower (P), and operational speed (V).
- Separate regressions for different vessel types; regression form: FC_v = β0 + β1*DWT_v + β2*P_v + β3*V_v^3 + ε.
- Calibration uses IHS Markit data (~19,000 vessels); good fit (R² = 0.93–0.98) for 41,600 vessels with complete data; a simpler regression based only on DWT used for remaining vessels (R² = 0.54–0.86).

### Transport and fuel demand model
- Port-level fuel demand derived from number of vessels calling a port, journey length, and vessel fuel consumption per km.
- AIS data (2019) for 97,500 vessels to build port-to-port movement across 1,377 ports, including route distances.
- Fuel demand on each route = fuel consumption per km × route distance; total port demand assigned to the origin port (all outbound fuel bunkered at the port of origin).
- This approach enables projecting present-day demand into 2050 despite its simplicity.

### Future fuel demand
- Projected by scaling 2019 port-level fuel demand with future port throughput (per vessel type) from OxMarTrans (2050 scenarios).
- Throughput changes are derived from future bilateral trade projections under various decarbonisation and growth scenarios.
- Fuel demand converted to ammonia by applying fleet adoption rates and assuming 1 tonne HFO ≈ 2.07 tonnes of ammonia.

## Data quality check
- Regression-based fuel consumption estimates align with empirical data and are validated against IMO’s 2019 Ship Fuel Oil Consumption Database.
- Global fuel consumption estimated at 233 Mt/year in 2019, comparable to IMO’s 213 Mt/year estimate (noting differences in vessel coverage and inclusion of certain vessel types).

## Data files

### port_reference.csv
- Port point locations and metadata for 1,377 ports.
- Key columns: Id, Name, Port_name, Country, Iso3, Region, Sub-region, X (longitude), Y (latitude), Geometry.

### fuel_demand_port_2050_1000km.csv
- Port-level 2050 fuel demand scenarios per vessel type, excluding trips shorter than 1000 km.
- 14 future trade scenarios (Table 1), with columns including:
  - Id, Scenario, Name, Iso3, Continent_code
  - vessel_type_main (Dry Bulk, General Cargo, Tanker, Container, Ro-Ro)
  - throughput_factor (future vs. 2015 throughput)
  - Fuel_tons_route (baseline HFO), Fuel_tons_route_slow
  - Fuel_tons_route_future (2050 HFO), Fuel_tons_route_slow_future

- Table 1 outlines the 14 trade scenarios combining SSP, RCP, and trade liberalization (Multilateral vs Regionalization).

## Reproducibility and references
- Full model code and data are provided in the linked Mendeley dataset.
- References include Verschuur et al. (2023, 2024), IMO (2021), and related works on ports, trade, and shipping emissions.