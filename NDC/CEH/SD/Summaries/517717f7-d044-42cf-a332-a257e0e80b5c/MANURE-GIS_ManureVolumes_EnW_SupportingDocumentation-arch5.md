# The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

## Overview
- GIS-based national inventory and map of livestock manure loadings to agricultural land, tracking nutrient loadings (N, P, K), organic carbon, and microbial indicators across time and space.
- Outputs support diffuse pollution modeling, emission inventories, and scenario analysis of management changes.
- Integrates excreta production, housing/grazing, storage, and land spreading through six livestock classes with monthly and land-use resolution.

## Data inputs, sources, and governance
- Inputs include excreta quantities and compositions derived from NVZ guidance, Defra datasets, and agricultural census categories; timing and apportionment follow NARSES and Defra practice surveys with monthly granularity.
- Spatial drivers come from the 2004 Agricultural Census (10 km grid; scalable to finer resolutions).
- Data governance framework includes:
  - Data Dictionary for spatial/temporal/national data and audit trails of flows/transformations.
  - Framework Manager for conceptual design; Data Manager for data import, scenario management, GIS viewing, and exporting.
- Look-up tables govern land-use spreading probabilities and monthly manure distribution.
- Outputs are designed for interoperability with Defra models and policy inventories, with traceability from inputs to results.

## Calculations and emissions modeling
- Excreta flows tracked node-to-node with losses, gains, and transformations (e.g., straw, immobilisation, mineralisation).
- Nutrients tracked: total N, ammonium-N, nitrate-N, organic-N; total P; total K; organic carbon; E. coli; dry matter and water content.
- Emissions and losses modeled:
  - NH3 losses from housing, hardstanding, and storage using NARSES-based factors.
  - CH4 and CO2 emissions linked to manure organic carbon with IPCC-based factors.
  - Leaching/evaporation from housing and storage based on WA0716 data.
  - E. coli reductions during storage with time-based assumptions.
- Dilution by rain and washdown accounted for; mineralisation/immobilisation processes included.
- Outputs include annual/monthly manure quantities and nutrient loadings by livestock type and land use, with regional patterns (notably high loadings in NW/SW England and Pembrokeshire).

## Validation and outputs
- Validation against:
  - RB209 manure compositions at spreading.
  - Defra NT2006 MANDE datasets for N production/composition.
  - NVZ guidance N-loads.
- Outputs include:
  - Totals and distributions of N, P, K, OC, and E. coli by livestock and land use.
  - Spatial maps and tables illustrating regional patterns and seasonal timing.
  - Tables and figures for model integration and policy inventories; supports downstream modeling (e.g., anaerobic digestion).

## Interoperability, reuse, and dissemination
- Data and results exportable to other modeling frameworks (MAGPIE, PSYCHIC) and policy analyses.
- Outputs available as tabular data, graphs, and GIS maps with monthly or annual timesteps.
- Web-based interface recommended to broaden access for policymakers and researchers; updates anticipated as census data and standards evolve.

## Scenario testing and key results (MANURES-GIS scenarios)
- Scenarios were chosen to reflect plausible management changes and policy options:
  1) Reduce total N and P excreted by livestock by 20% (dietary changes).
  2) Move all caged laying hens from deep pit to belt-scraped housing.
  3) Move all dairy cows and housed pigs from slurry to solid manure systems.
  4) Cover all slurry stores.
  5) House all dairy cows indoors year-round.
  6) Extend the grazing season for dairy cows.
  7) Change livestock numbers to Business As Usual (BAU) projections.

- Key quantified effects (illustrative totals from tables in the scenario appendix):
  - Scenario 1: N excretion in handled manures/direct excreta falls from about 374 kt to 305 kt; P excretion from about 59 kt to 45 kt (roughly 20% reductions in both N and P loadings).
  - Scenario 2: Ammonia-N losses from laying hens reduce by ~0.8 kt (about 20%), but land-spreading ammonia may rise slightly due to higher readily available N in belt-scraped manure.
  - Scenario 3: Ammonia-N losses reduced by ~9.8 kt (~24%) from dairy cows and housed pigs moving to solid manure systems; downstream nitrate leaching and N2O impacts also shift.
  - Scenario 4: Covering slurry stores reduces ammonia-N losses by ~2.5 kt (~4%), with pig sector gains in emissions reduction being larger proportionally.
  - Scenario 5: Housing dairy cows indoors increases ammonia-N losses by ~22 kt (~67%), due to housing, collecting yards, and storage, though land-spreading emissions may shift with different application timing.
  - Scenario 6: Extending grazing season lowers ammonia-N losses from ~33 kt to ~27 kt (~18%), driven by reduced housing losses but increased field deposition effects.
  - Scenario 7: BAU population changes reduce total N and P loadings by ~10% (N: 211 kt baseline to 169 kt FYM+slurry+excreta; P: 41 kt baseline to 33 kt), with livestock-specific contributions varying by sector.

- Overall takeaway: scenarios reveal trade-offs between housing/storage emissions and land-spreading emissions; some interventions reduce total ammonia-N losses but may increase nitrate leaching or nitrous oxide emissions in land spreading.

## Practical use for Data Stewards
- Provides a transparent, auditable data pipeline from inputs (census, guidance) to outputs (nutrient loadings, OC, E. coli) with traceable transformations.
- Maintains a data dictionary and framework that can be updated as new census data or policy standards are released.
- Documents provenance, assumptions (e.g., excretion rates, spreading probabilities), and validation to support reproducibility and trust.
- Enables data sharing and interoperability through standardized exports and alignment with Defra-informed models.

## Recommendations and future work
- Develop a simple web-based MANURES-GIS interface to broaden access to key outputs (manure quantities, nutrient loadings).
- Update spatial data sources as newer agricultural census data become available (current use is 2004 data).
- Refresh nutrient production standards and refine loss/transformations as new scientific data emerge, ensuring compatibility with evolving models and inventories.

## Publication and information governance
- Defra plans to publish SID 5 results publicly with annexes for sensitive information; final reports should be clear for broad understanding.
- Maintains compliance with information regulations and confidentiality where required.