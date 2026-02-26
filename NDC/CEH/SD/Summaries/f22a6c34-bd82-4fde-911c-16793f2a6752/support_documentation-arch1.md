# Data consist of modelled maritime fuel demand projections at 1,377 ports globally for the year 2050

## Overview
- Modelled maritime fuel demand projections for 1,377 ports worldwide in 2050.
- Data serve as input to the paper by Verschuur et al. (2024) and come with full model code.
- Two data files are deposited: port metadata and port-level fuel demand projections for 2050.

## Method

### Vessel fuel consumption
- Vessel fuel use depends on vessel characteristics: deadweight tonnage (DWT), main engine power (P), and speed (V).
- Regression approach by vessel type (v):
  - Daily fuel consumption FC_v = β0 + β1·DWT_v + β2·P_v + β3·V_v^3 + ε
- Training data:
  - About 19,000 vessels from IHS Markit; 97,500 vessels in the dataset; 41,600 vessels with complete data.
  - For vessels with missing V and P, a DWT-based regression is used; R^2 ranges from 0.54–0.86 for these predictions.
- Conversion to per-km fuel use:
  - Convert daily FC to fuel per travelled kilometre by dividing by V.
- Outcome:
  - A fuel consumption database for 97,500 vessels.

### Transport and fuel demand model
- Data: AIS movements for 97,500 vessels in 2019; port-to-port visits across 1,377 ports with distances.
- Fuel demand on each route:
  - Route fuel = fuel per km × route distance.
- Port-level demand (present day):
  - All fuel for outgoing vessels allocated to the port of origin (simplified bunkering assumption).
- Future fuel demand (2050):
  - Scale present-day port-level fuel demand by projected changes in port throughput per vessel type (2015 baseline) to 2050.
  - Throughput projections derived from the OxMarTrans model, using country bilateral trade scenarios for 2050 (decarbonisation and growth scenarios).
  - Translate 2050 fuel demand into ammonia demand via fleet adoption rates and a conversion factor (1 t HFO ≈ 2.07 t ammonia).

## Data quality check
- Regression fits show good alignment with empirical data.
- Present-day global fuel estimate: approximately 233 million tonnes per year (MMTPA) for 2019.
- Comparison with IMO Ship Fuel Oil Consumption Database: ~213 MMTPA for 2019; discrepancy explained by vessel count differences (27,221 vessels in IMO vs 97,500 in this dataset) and inclusion/exclusion of passenger/cruise ships.

## Files
- port_reference.csv
  - Port metadata for 1,377 ports.
  - Columns: Id, Name, Port_name, Country, Iso3, Region, Sub-region, X (lon), Y (lat), Geometry.
- fuel_demand_port_2050_1000km.csv
  - Port-level 2050 fuel demand by vessel type; excludes trips < 1000 km (assumed electrified).
  - Columns include: Id, Scenario, Name, Iso3, Continent_code, vessel_type_main (Dry Bulk, General Cargo, Tanker, Container, Ro-Ro), throughput_factor, Fuel_tons_route (baseline HFO), Fuel_tons_route_slow, Fuel_tons_route_future (2050 HFO), Fuel_tons_route_slow_future (2050 HFO with slow steaming).
  - 14 future trade scenarios described (Table 1) across SSP/RCP combinations and trade liberalization (Multilateral vs Regionalization).

## Scenarios (Table 1)
- 14 trade scenarios combining:
  - SSP1, SSP2, SSP5
  - RCP2.6, RCP4.5, RCP8.5
  - Multilateral vs Regionalization
- Trade liberalization indicates either global (Multilateral) or regionalized (Regionalization) trade integration.

## Use and accessibility
- Data intended to inform assessments of future shipping fuel demand and decarbonisation options (e.g., ammonia as an alternative fuel).
- Model code is provided and can be used to reproduce or adapt projections.
- Results can be linked to port-level planning and global supply-chain risk assessments under varied trade and decarbonisation pathways.

## References (context)
- Verschuur et al. on climate risks to port infrastructure and related modelling (2023/2024).
- IMO Ship Fuel Oil Consumption Database and related emissions inventories.
- Supporting methodological and data sources on global trade and port criticality.