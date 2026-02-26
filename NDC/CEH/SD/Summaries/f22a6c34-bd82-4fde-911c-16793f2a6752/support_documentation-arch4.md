# Data consist of modelled maritime fuel demand projections at 1,377 ports globally for the year 2050

- Purpose: Dataset models future port-level maritime fuel demand and serves as input to a related publication (Verschuur et al., 2024). Full model code is publicly available at Mendeley.
- Scope: 1,377 ports worldwide; 14 future trade scenarios; 2050 projections; excludes short trips (<1000 km) in the primary fuel demand file.

## Data scope and structure

- Files included:
  - port_reference.csv: port metadata (Id, Name, Iso3, Region/Sub-region, coordinates, geometry).
  - fuel_demand_port_2050_1000km.csv: port-level fuel demand by vessel type and scenario; includes baseline and 2050 projections, with columns for Fuel_tons_route (baseline) and Fuel_tons_route_future (2050), among others.
- Vessel types covered: Dry Bulk, General Cargo, Tanker, Container, Ro-Ro.
- Scenarios: 14 trade scenarios linked to SSP/RCP frameworks and regional/multilateral trade liberalization.

## Data sources and provenance

- Vessel fuel consumption data:
  - Based on empirical vessel movement data for ~97,500 vessels (AIS-derived) for 2019.
  - Regression models fitted per vessel type using daily fuel consumption (FC) as the outcome and DWT, engine horsepower (P), and speed (V) as predictors.
  - For ~41,600 vessels with IHS Markit data, vessel-type-specific regressions used; for others, a DWT-based regression estimated V and P.
- Movement and demand modeling:
  - Port-to-port visits and distances derived from AIS data (2019) for 1,377 ports.
  - Fuel per route calculated as fuel consumption per km times route distance; global port fuel demand assigned to origin port (simplistic bunkering assumption).
- Future projections:
  - Throughput scaling using OxMarTrans model projections for 2050; scenarios informed by bilateral trade flows under decarbonisation and growth assumptions.
  - Ammonia fuel demand conversion assuming equal global fleet distribution and a conversion factor of 1 tonne HFO = 2.07 tonnes ammonia.

## Methodology overview

- Vessel fuel consumption modeling:
  - FC_v = β0 + β1*DWT_v + β2*P_v + β3*V_v^3 + ε
  - Separate regressions by vessel type; good fit (R^2 0.93–0.98) for vessels with IHS data; reduced-fit model for remaining vessels (R^2 0.54–0.86).
  - Convert daily FC to per-km FC by dividing by V.
- Transport and fuel demand model:
  - Use AIS-derived 2019 movement data to map port-to-port routes and distances.
  - Estimate route fuel demand by multiplying fuel per km by route distance; allocate all outgoing port fuel to the port of origin.
- Future fuel demand projection:
  - Scale 2019 baseline with 2050 throughput changes per port (per vessel type).
  - Convert to ammonia demand using fleet adoption rates and energy conversion factor.

## Data quality and validation

- Regression-based fuel estimates align with external benchmarks:
  - Present-day global fuel consumption estimated at ~233 MMTPA for 2019, close to IMO’s 213 MMTPA when considering dataset scope differences (vessel counts, inclusion of non-major vessels, and exemptions for some ship types).
- Validation acknowledges differences due to data coverage (97,500 vessels vs. IMO’s dataset) and inclusion/exclusion of certain ship classes.

## Data artifacts and schema details

- port_reference.csv:
  - Columns include Id, Name, Port_name, Country, Iso3, Region, Sub-region, X (longitude), Y (latitude), Geometry.
- fuel_demand_port_2050_1000km.csv:
  - Columns include Id, Scenario, Name, Iso3, Continent_code, vessel_type_main, throughput_factor, Fuel_tons_route (baseline HFO), Fuel_tons_route_slow (baseline slow steaming), Fuel_tons_route_future (2050 HFO), Fuel_tons_route_slow_future (2050 HFO slow steaming).
  - Excludes trips shorter than 1000 km; 14 future trade scenarios described (Table 1) with SSP/RCP and regional vs. multilateral trade liberalization.

## Access and reuse

- Data and model code are publicly accessible:
  - Model code and data deposition linked in the repository: Mendeley dataset v4yz7778mh/1.
- References supporting methodology include:
  - Verschuur et al. on climate risks to port infrastructures, global trade, and ammonia decarbonisation; IMO Ship Fuel Oil Consumption Database; related works on ports’ criticality and global trade dynamics.

## Assumptions, limitations, and considerations for data leaders

- Key assumptions:
  - Bunkering fuel is sourced from the port of origin; simplistic representation of fuel supply.
  - Exclusion of short-haul voyages (<1000 km) from the primary 2050 fuel demand file to reflect likely electrification.
  - Global fleet distribution assumed uniform for ammonia energy conversion.
- Limitations:
  - Regression models for a subset of vessels rely on high R^2 values; simpler models for remaining vessels have lower explanatory power.
  - AIS-based movement data from 2019 used to project 2050; ignores potential structural shifts beyond throughput changes.
- Data governance implications:
  - Clear metadata and unit definitions are present, enabling cross-portal discoverability and reuse.
  - Requires careful interpretation when integrating with other datasets (e.g., sector-level data standards, harmonization of vessel-type classifications).
  - Opportunities for establishing a standardized workflow for port-level freight fuel projections, including explicit handling of exceptions and sensitivity analyses.

## Relevance for Data Leaders

- Demonstrates end-to-end data pipeline from raw vessel data to future scenario projections, including validation against external benchmarks.
- Highlights importance of data provenance, model transparency, and accessible code/data repositories for reproducibility.
- Illuminates governance needs around data standards, metadata, and cross-disciplinary collaboration to support strategic planning and policy analysis in maritime decarbonisation efforts.