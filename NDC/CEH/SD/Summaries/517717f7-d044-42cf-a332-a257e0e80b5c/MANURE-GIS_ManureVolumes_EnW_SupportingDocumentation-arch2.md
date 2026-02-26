# The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

- Purpose and scope
  - National inventory and GIS-based map of livestock manure loadings to agricultural land.
  - Quantifies nutrients (N, P, K), organic carbon (OC) and microbial pathogen (E. coli) loadings from livestock excreta on a spatial and temporal basis.
  - Tracks manure production and deposition along the management chain (housing/grazing → storage → land spreading) and supports diffusion-pollution modelling.

- Data inputs and framework
  - Spatial data from the 2004 Agricultural Census (livestock numbers, land use) at 10 km grid; outputs at 10 km × 10 km (England and Wales).
  - Excreta composition and production benchmarks from RB209, NVZ-AP, NT2006 MANDE, Defra projects; land-spreading patterns from surveys.
  - Node-Link framework with six livestock classes and multiple stages (excretion, housing, grazing, hardstanding, storage, export, spreading) to allocate flows.
  - Outputs include totals and distributions by livestock type, land use, and management stage; supported monthly and annual timesteps; exportable to GIS/maps and other models.

- Validation and robustness
  - Consistency checks against RB209 and NVZ-AP data; alignment with NH3 emission inventory and other nutrient loadings methods.
  - Cross-checks with livestock production data corroborate estimated N losses and overall nutrient loadings.

- Key outputs and spatial/temporal patterns
  - Manure quantities: ~72 million tonnes (fresh weight) of handled manure annually; ~73 million tonnes deposited by grazing livestock.
  - Nutrient and OC loadings: ~310 kt N from handled manure applications; ~370 kt N from grazing excreta; ~70 kt P; ~260 kt K; annual OC additions of ~3.3 million tonnes from handled manure and ~2.7 million tonnes from grazing excreta.
  - Spatial patterns: highest loadings in the north-west and south-west of England and Pembrokeshire, correlating with high cattle densities.
  - Temporal/land-use patterns: monthly outputs show seasonal excretion and application (e.g., cattle slurry mainly to grassland in winter/spring; distinct spring vs autumn cropping patterns).
  - Outputs and data products: regional-scale maps and tabulated data by livestock type and land use; supports planning for anaerobic digestion plants and nutrient-management strategies.
  - Accessibility: two spatial resolutions (1 km2 and 10 km2); monthly and annual timesteps; potential for a web-based version.

- Applications and policy relevance
  - Supports national emission inventories and environmental modelling (NH3, N2O, nitrate leaching via MAGPIE; phosphorus losses via PSYCHIC).
  - Enables scenario testing of livestock management changes, housing/storage practices, and regulatory impacts on diffuse pollution.
  - Aids spatial planning for manure-management infrastructure and land-use planning.

- Data management and tools
  - Software components: Data Manager, Scenario Manager and GIS Viewer.
  - Capabilities: import data, run scenarios (e.g., updated livestock numbers), view outputs, export data.
  - Outputs available at 1 km2 and 10 km2 resolutions; monthly and annual timesteps; potential for a web interface.

- Limitations and future work
  - Current reliance on 2004 Agricultural Census data; requires updates as newer census data become available.
  - Ongoing refinement of inputs and loss/transformations; integration with broader diffuse-pollution models.
  - Future work includes updating nutrient-production standards and expanding data sharing and web access.

- Scenario testing (examples of policy-relevant tests)
  - Scenario 1: 20% reduction in N and P excretion (dietary changes)
    - NH3 losses reduced by ~14 kt N (housing/storage and land spreading).
    - N and P loadings to land decline (N excretion and P excretion reduced; e.g., N total from baseline ~684 kt to around 570 kt; P total from ~131 kt to ~117 kt in the depicted output sets).
  - Scenario 2: Move all caged laying hens from deep-pit to belt-scraped housing
    - NH3 losses from laying hens reduced by about 0.8 kt N (~20% reduction in that sector’s NH3-N).
    - Potential small increases in land-spreading NH3 emissions due to drier manure but overall modest change.
  - Scenario 3: Move all dairy cows and housed pigs from slurry to solid manure (FYM)
    - NH3 losses reduced by ~9.8 kt N (about 24% of baseline).
    - Reductions in nitrate leaching and indirect/ direct N2O emissions after land spreading; some storage emissions may change.
  - Scenario 4: Cover all slurry stores
    - NH3 losses reduced by ~2.5 kt N (about 4% of slurry-system losses).
    - Increases in readily available N in land spreading due to drier slurry; minor changes in nitrate and N2O post-spreading.
  - Scenario 5: All dairy cows housed indoors year-round
    - NH3 losses increase by ~22 kt N (about 67% rise; housing/storage-related increases dominate).
  - Scenario 6: Extend grazing season (less housing)
    - NH3 losses decrease by ~6 kt N (about 18% reduction).
    - Direct grazing reduces field excreta emissions but may raise nitrate leaching and N2O after spreading.
  - Scenario 7: Change livestock numbers to BAU projections
    - Total N and P loadings to land drop by ~10% relative to baseline (N ~684 kt to ~616 kt; P ~131 kt to ~119 kt).
    - Overall ammonia emissions reduce by around 10% compared with baseline; land spreading emissions decrease correspondingly.