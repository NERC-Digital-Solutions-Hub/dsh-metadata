# Data consist of modelled maritime fuel demand projections at 1,377 ports globally for the year 2050.

## Overview
- Dataset models maritime fuel demand projections for 1,377 ports worldwide for 2050.
- Data are intended as input to a broader study (Verschuur et al., 2024) and full model code is provided via the linked dataset.
- Data deposit includes two files and accompanying metadata descriptions.

## Method

### Vessel fuel consumption
- Vessel fuel consumption depends on vessel characteristics: deadweight tonnage (DWT), installed engine power (P), and operational speed (V).
- A vessel-type specific linear regression is used to predict daily fuel consumption (FC, tonnes/day):
  FC_v = β0 + β1·DWT_v + β2·P_v + β3·V_v^3 + ε
- Regression models are fitted using a dataset from IHS Markit for ~19,000 vessels; results show strong fits (R^2 = 0.93–0.98) for 41,600 vessels with data.
- For the remaining vessels, a regression based on DWT alone is used, with V and P predicted from DWT; these have weaker fits (R^2 = 0.54–0.86).
- Daily FC is converted to fuel per travelled kilometre (tonnes/km) by dividing FC by V.
- Final product: a database of vessel fuel consumption for 97,500 vessels.

### Transport and fuel demand model
- Empirical vessel movement data (AIS) for 97,500 vessels in 2019 is used to build port-to-port visits for 1,377 ports, including inter-port distances.
- Combine vessel fuel consumption per km with route distances to estimate fuel need on each route.
- Global fuel demand per port is derived by assigning all fuel consumption of outgoing vessels to the port of origin (a simplification that enables projecting present-day demand into the future).

### Future fuel demand
- Present-day port-level fuel demand is scaled by projected future port throughput (per vessel type) for 2050 versus 2019.
- Throughput projections per port come from the OxMarTrans model, which simulates bilateral trade flows under various decarbonisation and growth scenarios.
- 2050 port-level fuel demand is translated into ammonia fuel demand using fleet adoption rates and a conversion factor: 1 tonne HFO = 2.07 tonnes ammonia.
- The study considers 14 future trade scenarios, across multiple SSPs and RCPs, including regionalisation vs. multilateral trade liberalisation.

## Data quality check
- The vessel fuel consumption regressions show good fits with empirical data.
- Present-day global fuel estimates (2019) are cross-checked against IMO’s 4th GHG emissions inventory:
  - This study: 233 million tonnes per annum (MMtpy) for 2019.
  - IMO reference: 213 MMt for 2019 (based on a subset of vessels >5,000 GT, plus some differences in coverage).
- The discrepancy is attributed to the larger vessel set in this study (97,500 vessels vs. ~27,221 in IMO data) and the inclusion/exclusion of passenger/cruise ships.

## Files

### port_reference.csv
- Port metadata for 1,377 ports, enabling merging with fuel demand data.
- Columns include:
  - Id: unique identifier
  - Name, Port_name, Country
  - Iso3: country code
  - Region, Sub-region
  - X, Y: longitude, latitude
  - Geometry: point location

### fuel_demand_port_2050_1000km.csv
- Port-level fuel demand scenarios for 2050, per vessel type, excluding trips shorter than 1000 km (assumed to be electrified).
- Covers 1,377 ports across 14 future trade scenarios (Table 1 details the scenario configurations, including SSP/RCP and trade liberalisation).
- Key columns include:
  - Id: unique identifier
  - Scenario: trade scenario modelled
  - Name, Iso3, Continent_code
  - vessel_type_main: vessel types considered (Dry Bulk, General Cargo, Tanker, Container, Ro-Ro)
  - throughput_factor: projected vs. present-day throughput ratio
  - Fuel_tons_route: baseline HFO fuel demand (tonnes)
  - Fuel_tons_route_slow: baseline slow-steaming HFO demand
  - Fuel_tons_route_future: 2050 HFO fuel demand
  - Fuel_tons_route_slow_future: 2050 slow-steaming HFO demand

## References
- Verschuur, J. et al. (2023) Climate risks to port infrastructure expansions for future global trade (under review).
- IMO (2021) ENERGY EFFICIENCY OF SHIPS: Ship Fuel Oil Consumption Database (GISIS).
- Verschuur, J. et al. (2024) Optimal fuel supply of green ammonia to decarbonise global shipping, Environmental Research: Infrastructure and Sustainability.
- Verschuur, J., Koks, E. E., and Hall, J. W. (2022) Ports’ criticality in international trade and global supply-chains, Nature Communications.
- Verschuur, J., Koks, E. E., and Hall, J. W. (2021) Global economic impacts of COVID-19 lockdown measures in high-frequency shipping data, PLOS ONE.