# The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

## Aim
- Provide a GIS-enabled tool to estimate excreta produced by farm livestock and apportion it into field-deposited manure and handled manure.
- Track losses, gains, and transformations across the manure management continuum (housing/grazing → storage → land spreading).
- Quantify loadings of nutrients (N, P, K), organic carbon, and microbial pathogens (E. coli) to agricultural land over space and time.
- Output results to underpin and integrate with diffuse pollution models and inventories; support policy and inventory development.

## Scope and purpose
- Quantify nutrient (N, P, K), OC, and microbial pathogen loadings to land; quantify annual manure production and land application; synthesize knowledge in a GIS; develop a policy-support tool to underpin diffuse pollution models.

## Approach and conceptual framework
- Six livestock classes (dairy cattle, beef cattle, pigs, sheep and other stock, laying hens, broilers and other poultry) tracked through six stages: excretion, housing, grazing, hard standings, storage, export, and spreading.
- At each stage, manure composition changes via losses, gains, or transformations; outputs include spreadsheets and GIS maps at 10 km × 10 km (monthly or annual), linkable to other models.
- Flexible framework designed for updates and extension, including linking to additional models.

## Data sources and integration
- Spatial data: 2004 Agricultural Census (livestock numbers, land use at 10 km grid).
- Excreta quantity/composition: NVZ guidance, RB209 Fertiliser Manual.
- Timing: NARSES-based monthly excretion apportionment; Defra Farm Practices data for timing.
- Land-use distribution and spreading: 2004 Census; British Survey of Fertiliser Practice.
- Emission/transformations: NH3 losses (housing/hardstanding/storage) via NARSES; N2O/NO/N2 losses; CH4/CO2 relationships; leaching/evaporation; E. coli die-off data.
- Validation: RB209/NT2006 nutrient composition; NT2006 MANDE data; NVZ guidance; comparison with Ammonia Emissions Inventory.

## Data management and software structure
- Framework Manager: GUI to design/populate MANURES-GIS (Nodes/Links).
- Engine: tracks flow, applies losses/gains/transformations; supports monthly timesteps.
- Data Dictionary: stores spatial/temporal national data; look-up tables for land spreading.
- Data Manager/Scenario Manager: data import, run scenarios, view outputs, export data.
- Outputs: tabular data, graphs, and GIS maps at 1 km² and 10 km² resolutions, monthly/annual timesteps.

## Validation and benchmarking
- Outputs benchmarked against national manure loadings data and nutrient composition.
- Nutrient composition at spreading consistent with RB209 and NT2006 data; NH3 emissions align with the 2008 Ammonia Emissions Inventory.

## Key results and outputs
- Manure quantities
  - ~72 million tonnes (fresh weight) of handled manures produced annually; ~73 million tonnes deposited by grazing livestock (England and Wales).
  - Spatially strongest loadings in north-west and south-west England and Pembrokeshire.
- Nutrient and OC loadings
  - Total N applied via manure: ~310 kt (handled) and ~370 kt (grazing excreta) annually.
  - Total P applied via manure: ~70 kt (handled) and ~160 kt P2O5 (grazing).
  - Total K applied via manure: ~260 kt (handled) and ~310 kt K2O (grazing).
  - Organic carbon additions: ~3.3 Mt (handled) and ~2.7 Mt (grazing).
  - E. coli loadings tracked per hectare; highest where cattle density is higher.
- Spatial and temporal patterns
  - Highest loadings in regions with high cattle densities (NW/SW England, Pembrokeshire).
  - Monthly timesteps reveal seasonality in excretion, housing vs grazing, and land spreading.
- Emissions and losses
  - NH3 losses across sectors align with Ammonia Emissions Inventory values.
  - Time-dependent transformations cover gas emissions, leaching, evaporation, and E. coli die-off.

## Timing and application patterns
- Monthly timesteps enable exploration of how management changes affect emissions and land spreading.
- Examples: cattle slurry mainly applied to grassland in winter/spring; spring arable land receives peak slurry.

## Data governance, accessibility, and future maintenance
- Public-domain publication encouraged; intended to accompany broader Defra reporting.
- Acknowledges data accessibility and metadata barriers; emphasizes data provenance and governance.
- Potential for a web-based version to improve accessibility for policymakers/researchers.
- Plans to update with newer spatial datasets and updated nutrient production standards (e.g., later RB209, NVZ changes).

## Limitations and challenges
- Based on 2004 Agricultural Census; requires updates for current policy relevance.
- Poultry sectors rely on compiled assumptions/extrapolations.
- E. coli data derived from limited datasets with die-off assumptions.
- Simplifications in leachate/water-dilution practices; some farm-level complexities require refinement.

## Recommendations for further work
- Develop a simple web-based MANURES-GIS to broaden access.
- Update datasets as newer livestock numbers and nutrient production standards become available.
- Incorporate new scientific data on losses/transformations to keep framework current.
- Explore integration with additional models and outputs (e.g., heavy metals, other contaminants).

## Scenario testing (using MANURES-GIS)
- Seven scenarios were analyzed to assess policy-relevant changes:
  - Scenario 1: Reduce N and P excretion by 20% (dietary changes)
    - N deposition to land decreases from 374 kt to 305 kt; P deposition decreases from 59 kt to 45 kt.
    - Ammonia emissions from housing/storage and land spreading reduced; nitrate leaching and N2O emissions also reduced.
  - Scenario 2: Move all caged laying hens from deep-pit to belt-scraped housing
    - Ammonia losses from laying hens reduced from 4.4 kt to 3.6 kt (≈20% reduction inlayer NH3 losses); potential minor increases in land-spread NH3/N2O due to higher readily available N content in manure.
  - Scenario 3: Move all dairy cows and housed pigs from slurry to solid manure (FYM)
    - Ammonia losses reduced by about 24% (total from 41.4 kt to 31.6 kt; dairy −6.6 kt, pigs −3.2 kt).
    - Following land spreading, reductions in nitrate leaching and N2O emissions expected; storage-phase N2O may rise but net decrease overall.
  - Scenario 4: Cover all slurry stores
    - Ammonia losses reduced by ~4% (total from 59.3 kt to 56.8 kt); pig sector sees larger percentage reductions.
  - Scenario 5: All dairy cows housed indoors year-round
    - Ammonia losses increase from 33 kt to 55 kt (≈67% increase); storage/collection losses rise; overall ammonia emissions higher than baseline.
  - Scenario 6: Extend the grazing season (less housing)
    - Ammonia losses decrease from 33 kt to 27 kt (≈18% reduction); housing-related emissions drop, but grazing increases nitrate leaching and some N2O emissions; net efficiency decreases.
  - Scenario 7: Change livestock numbers to BAU projections (2020)
    - N and P loadings to land drop by about 10% overall (total N 684 kt → 616 kt; P 131 kt → 119 kt).
    - Ammonia emissions and land-spread impacts reflect reduced dairy/pig numbers and slightly increased poultry; overall reductions in N and P loadings to land.

## Policy relevance
- Provides a transparent, auditable framework linking livestock management to diffuse pollution outcomes.
- Supports Defra and other agencies in inventory development, scenario planning, and policy assessment for manure management and livestock numbers.
- Outputs usable for planning, environmental condition monitoring, and infrastructure considerations (e.g., storage, digestion).

## Summary of value
- MANURES-GIS offers a robust, auditable, and extensible tool to quantify and map livestock manure loadings to land over space and time, aiding policy formation, planning, and environmental management through transparent linkage of agricultural practices to diffuse pollution outcomes.