The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

- Purpose and scope
  - GIS-based tool (MANURES-GIS) to inventory and map manure loadings to agricultural land in England and Wales.
  - Captures flows from excretion through housing, storage, export, and land spreading with monthly or annual timesteps.
  - Outputs include tabular data and maps at 1 km2 and 10 km2 resolutions for integration with diffuse pollution models (e.g., MAGPIE, PSYCHIC).

- Key data inputs and framework
  - Table A20: Proportions of manure type by land use and month (e.g., cattle slurry/FYM, pig slurry/FYM, poultry) across Grass, Spring cropping, Autumn cropping.
  - Table A21–A24: Ammonia emission factors, N2O/NO/N2-N emission factors, CH4-C emission factors, and E. coli reduction during housing/storage.
  - Table A25: Typical straw composition (used for nutrient balance and carbon content).
  - Emission and transformation processes are embedded in a node/link GIS framework (Source, Housing, Hardstanding, Storage, Export, Grazing, Spreading, etc.) with monthly timing and land-use allocation.
  - Spatial drivers include land use, livestock counts, and spreading patterns to generate grid-based loadings.

- Spatial-temporal outputs
  - Monthly and annual maps of manure loadings and nutrient loadings (N, P, K), organic carbon (OC), and E. coli by manure type and land use.
  - Grid outputs at 1 km2 and 10 km2 for model integration; summary matrices of key properties by sector, land use, node, and transformation.

- Scenario testing and findings (USING MANURESGIS FOR SCENARIO TESTING)
  - seven scenarios evaluated to assess policy-relevant changes and management options
  - Scenario 1: Reduce total N and P excreted by livestock by 20% (dietary changes)
    - N: total annual N in handled manures and grazing excreta reduced from 374 kt to 305 kt (approx. 69 kt less N).
    - P: reduced from 59 kt to 45 kt (approx. 14 kt less P).
    - Ammonia emissions reductions in housing/storage and land spreading around 14 kt N.
  - Scenario 2: Move all caged laying hens from deep-pit to belt-scraped housing
    - Ammonia losses from laying hens reduced by about 0.8 kt N (20% in this sector); slight rise in land-spread emissions due to higher readily available N in belt-scraped manure.
  - Scenario 3: Move all dairy cows and housed pigs from slurry to solid manure (FYM) systems
    - Ammonia losses reduced: total ~9.8 kt N (roughly 20% in dairy; pig reductions ~3.2 kt N); land-spread emissions and N losses shift due to different manure form.
  - Scenario 4: Cover all slurry stores
    - Ammonia losses reduced by ~2.5 kt N (about 4% of housing/storage losses), with larger relative gains in pigs.
  - Scenario 5: All dairy cows housed indoors (no grazing)
    - Ammonia losses increase by ~22 kt N (housing, collecting yards, storage); potential shifts in land-spread emissions.
  - Scenario 6: Extend grazing season (more grazing months)
    - Ammonia losses decrease by ~6 kt N (about 18% reduction for dairy sector); some increase in nitrate leaching and N2O during land spreading.
  - Scenario 7: Change livestock numbers to BAU projections
    - Overall N excretion declines by ~10%; P excretion declines by ~10% in total.
    - Ammonia losses decrease by ~c.10% relative to baseline in housing/storage/spreading; total N and P loadings drop (N ~68 kt; P ~12 kt) across England and Wales.

- Map- and data- product implications for GIS specialists
  - Enables scenario-driven map layers of NH3, N2O/NO/N2 emissions, land-applied N and P, and other nutrients.
  - Supports spatial planning for policy inventories, ammonia/nitrous oxide emission accounting, nitrate leaching models, and phosphorus fate modeling.
  - Provides a modular data dictionary and look-up structures to facilitate coupling with external models and future scenario extensions.

- Utility and integration
  - The MANURES-GIS framework is designed for extensibility, enabling future web-based access, dataset updates, and refined loss/transformation data as science advances.
  - Outputs are designed for straightforward export to MAGPIE, PSYCHIC, and other modeling frameworks at both 1 km2 and 10 km2 scales.