# Data: Modelled maritime fuel demand projections at 1,377 ports globally for the year 2050

## Overview
- Dataset models port-level fuel demand projections for 2050, based on vessel-level fuel consumption estimates, transport demand modelling, and fuel demand modelling.
- Covers 1,377 ports globally and uses AIS data (2019) for 97,500 vessels to derive route-level fuel needs.
- Data intended as input to a related paper (Verschuur et al., 2024) with full model code available in a linked dataset.

## Data scope and purpose
- Purpose: provide a reproducible basis for future port-level fuel demand and to support research on decarbonisation scenarios in global shipping.
- Key outputs: port-level fuel demand by vessel type for 2050 under multiple trade/scenario settings; includes both baseline and slowed-steaming scenarios.
- Important design assumptions:
  - Fuel demand on a route is the product of per-km fuel consumption and route distance.
  - All bunkering at the port of origin (simplistic but used to project present-day demand forward).
  - Short trips under 1000 km are excluded from the main dataset (to align with electrification assumptions).
  - Future 2050 demand scaled from 2019 through port throughput projections (OxMarTrans) and fleet adoption rates for ammonia.

## Methodology (Data model and provenance)
- Vessel fuel consumption modelling:
  - Vessel-type specific linear regression using daily fuel consumption (FC) as the dependent variable.
  - Explanatory variables: deadweight tonnage (DWT), installed engine horsepower (P), and operational speed (V); V cubed term included.
  - Separate models per vessel type; good fit (R² 0.93–0.98) for vessels with complete IHS Markit data (≈19,000 vessels; 41,600 covered in the regression-based extension).
  - For remaining vessels, a DWT-based regression estimates V and P; still reasonable R² values (0.54–0.86).
  - Conversion to fuel per travelled kilometre by dividing FC by vessel speed.
- Transport and fuel demand modelling:
  - AIS data (2019) for 97,500 vessels to construct port-to-port movements across 1,377 ports.
  - Route-level fuel demand: fuel per km × route distance; port-level demand attributed to the port of origin.
- Future fuel demand projection:
  - Scale 2019 route fuel demand by projected changes in port throughput for 2050 (via OxMarTrans model, incorporating decarbonisation and growth scenarios).
  - Convert HFO fuel demand to ammonia demand using fleet-adoption rates and a conversion factor (1 tonne HFO ≈ 2.07 tonnes NH3).
  - Scenarios incorporate SSP/RCP combinations and trade liberalisation variants (14 scenarios in Table 1).

## Data quality and validation
- Regression models show strong fit to empirical data; validation against IMO emissions data:
  - Global 2019 fuel consumption estimated at 233 MMt/year vs IMO Ship Fuel Oil Consumption Database estimate of 213 MMt/year.
  - Differences explained by scope (dataset covers more vessels but excludes some large vessels and cruise ships; IMO data includes a broader vessel mix).
- Overall alignment supports credibility, with caveats noted around scope and data coverage.

## Data files and metadata
- port_reference.csv
  - Port-level metadata and geography for 1,377 ports.
  - Fields: Id, Name, Port_name, Country, Iso3, Region, Sub-region, X, Y, Geometry.
- fuel_demand_port_2050_1000km.csv
  - Port-level fuel demand scenarios for 2050, per vessel type; excludes trips <1000 km.
  - Fields include: Id, Scenario, Name, Iso3, Continent_code, vessel_type_main, throughput_factor, Fuel_tons_route, Fuel_tons_route_slow, Fuel_tons_route_future, Fuel_tons_route_slow_future.
  - Contains 14 future trade scenarios (based on SSP/RCP and trade liberalisation settings) across 1,377 ports.
- The deposit includes two files plus the full model code linked in the dataset.

## Data sharing, access, and documentation
- Data and code are deposited in a public dataset (link provided in the document).
- Files are in CSV format with a clearly defined schema; a dedicated data dictionary/README is advisable to accompany the deposit for discoverability and reuse.
- Consider explicit licensing, citation instructions, and versioning to enable proper reuse and attribution.

## Limitations and considerations for data stewards
- Exclusions and simplifications:
  - Excludes trips shorter than 1000 km from the main dataset; short-segment electrification is assumed for these trips.
  - Bunkering assumed at origin port; does not model intermediate deviations or port-stop patterns.
  - Fleet distribution is assumed equal globally in the ammonia conversion step; local fleet heterogeneity not captured.
- Interoperability and data coherence:
  - Different sources (AIS, IHS Markit vessel data, OxMarTrans outputs) require careful provenance tracking.
  - Regression model parameters and data quality depend on the subset of vessels with complete data.
- Update and maintenance:
  - Future updates would require re-running the regression with updated vessel datasets, updated port throughput projections, and revised scenario definitions.
  - Documentation should capture version, data sources, and any changes to methodology.

## Governance and maintenance recommendations
- Metadata and provenance:
  - Provide a comprehensive data dictionary (variable definitions, units, Data types, valid ranges).
  - Document data sources (AIS 2019, IHS Markit vessel data, OxMarTrans scenarios) and processing steps.
  - Include model version, parameter values, and regression coefficients per vessel type.
- Licensing and access:
  - Attach a clear license for reuse; provide citation guidance and DOI where possible.
  - Include access controls or embargo notices if future updates are anticipated.
- Data quality and validation:
  - Maintain an audit trail of validation steps (e.g., comparison to IMO datasets) and rationale for any discrepancies.
  - Publish uncertainty estimates or sensitivity analyses where feasible.
- Reproducibility and interoperability:
  - Ensure code and data transformations are fully reproducible; consider providing a reproducible workflow (e.g., scripts, containerization).
  - Align with common data standards for maritime data (coordinate reference systems, port identifiers, vessel types) to facilitate interoperability with other datasets.

## Practical guidance for reuse
- When using the dataset, account for:
  - The 1000 km cutoff and the implications for electrification assumptions.
  - The origin-port bunkering assumption and potential deviations in real-world supply chains.
  - The scenario-specific nature of results (14 scenarios with SSP/RCP and trade-liberalisation variants).
  - The conversion factor for HFO to ammonia and fleet adoption rates as sources of uncertainty.
- Integrate with other port/throughput datasets carefully, ensuring consistent port identifiers (Id/Name/Iso3) and country metadata.

## References (as listed)
- Verschuur, J. et al. (2023) 'Climate risks to port infrastructure expansions for future global trade', under review.
- IMO (2021) ENERGY EFFICIENCY OF SHIPS: Report of fuel oil consumption data submitted to the IMO Ship Fuel Oil Consumption Database in GISIS, IMO Ship Fuel Oil Consumption Database.
- Verschuur, J. et al. (2024) 'Optimal fuel supply of green ammonia to decarbonise global shipping', Environmental Research: Infrastructure and Sustainability, 4(1), p. 015001.
- Verschuur, J., Koks, E. E. and Hall, J. W. (2022) 'Ports' criticality in international trade and global supply-chains', Nature Communications, 13(1), p. 4351.
- Verschuur, J., Koks, E. E. and Hall, J. W. (2021) 'Global economic impacts of COVID-19 lockdown measures stand out in high-frequency shipping data', PLOS ONE, 16(4), p. e0248818.