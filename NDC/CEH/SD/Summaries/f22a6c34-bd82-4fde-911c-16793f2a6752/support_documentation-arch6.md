# Data consist of modelled maritime fuel demand projections at 1,377 ports globally for the year 2050

- Purpose and scope
  - Modelled maritime fuel demand projections at 1,377 ports for 2050, informing a related paper (Verschuur et al., 2024).
  - Full model code and data deposit available (Mendeley dataset linked in the document).

- Key data sources
  - AIS data for 97,500 vessels (2019) to construct port-to-port movements and route distances.
  - IHS Markit vessel database for ~19,000 vessels to calibrate vessel-specific fuel consumption models.
  - OxMarTrans global maritime transport model for 2050 port throughput projections under multiple scenarios.
  - IMO Ship Fuel Oil Consumption Database for validation against present-day fuel estimates.

- Methods (how the future port-level fuel scenarios are determined)
  - Vessel fuel consumption modeling
    - Vessel-type specific linear regression using daily fuel consumption (FC, tonnes/day) as the target.
    - Predictors: deadweight tonnage (DWT), installed engine power (P), and operational speed (V) with V^3 term; separate regressions by vessel type.
    - Model form: FC_v = β0 + β1*DWT_v + β2*P_v + β3*(V_v)^3 + ε.
    - Calibration uses ~19,000 vessels; high fit (R^2 0.93–0.98). For ~41,600 vessels lacking complete data, regressions based on DWT predict V and P; R^2 0.54–0.86.
    - Convert daily FC to fuel per travelled kilometre by dividing FC by V.
  - Transport and fuel demand model
    - From 2019 AIS data, build port-to-port movement dataset for 1,377 ports, including route distances.
    - Compute route fuel demand as FC_per_km × route distance; assign all outbound vessel fuel to the origin port’s fuel demand (a simplifying assumption to project present-day demand forward).
  - Future fuel demand projection
    - Scale present-day port-level fuel demand by changes in port throughput from 2019 to 2050, per vessel type, using OxMarTrans projections under different decarbonisation and socioeconomic growth scenarios.
    - Translate total fuel demand into ammonia fuel demand using fleet adoption rates and an energy conversion factor: 1 tonne HFO ≈ 2.07 tonnes ammonia.
  - Data processing and quality checks
    - Regression-based estimates are validated against IMO’s 2021 fuel consumption inventory; present-day global fuel is estimated at ~233 Mt/year (vs. IMO’s ~213 Mt/year for a larger vessel set). Differences explained by vessel coverage and included ship types.

- Data products and outputs
  - Port-level fuel demand projections for 2050 by vessel type
    - Excludes trips shorter than 1000 km (assumed electrified); results available for 1,377 ports across 14 future trade scenarios.
    - Main output file: fuel_demand_port_2050_1000km.csv
    - Columns include: port identifiers, scenario, vessel_type_main, throughput_factor (throughput change vs. 2015), Fuel_tons_route (baseline HFO), Fuel_tons_route_future (2050 HFO), and slow-steaming variants.
  - Port reference data
    - port_reference.csv containing port identifiers, names, country, ISO codes, UN region classifications, and geographic coordinates.
  - Table of scenarios
    - 14 scenarios defined by combinations of SSPx, RCP, and trade liberalisation (Multilateral vs Regionalization), as listed in Table 1 of the document.
  - Access to code and methodology
    - Full model code and methodology linked in the data deposit for reproducibility.

- Scenario context and interpretation
  - Scenarios cover a matrix of socioeconomic and climate trajectories (SSP, RCP) with varying levels of global trade liberalisation (Multilateral vs Regionalization).
  - Enables comparative analysis of how different futures affect port-level fuel demand and potential ammonia fuel needs.

- Data quality and limitations
  - High-fidelity vessel-level fits for a substantial subset; broader vessel coverage relies on simpler regressions.
  - Present-day validation aligned with IMO benchmarks but differences exist due to dataset scope (number and type of vessels included).
  - Simplifying assumptions (e.g., routing fuel from origin port) used to enable forward projection; results intended as scenario-based projections rather than exact forecasts.

- Practical uses for data support
  - Building dashboards or pivot tables to explore 2050 port-level fuel demand across scenarios and vessel types.
  - Scenario analysis for policy planning, decarbonisation planning, and ammonia-fuel adoption strategies.
  - Identifying ports with high projected fuel demand and potential infrastructure or supply-chain implications.