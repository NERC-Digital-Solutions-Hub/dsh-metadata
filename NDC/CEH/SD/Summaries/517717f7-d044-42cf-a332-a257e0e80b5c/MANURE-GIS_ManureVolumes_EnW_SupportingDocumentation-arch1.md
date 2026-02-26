# The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

- Defra-funded GIS tool to inventory livestock manure loadings to agricultural land and model impacts on nutrients, organic carbon, and microbial loadings.
- Aims to quantify excreta production, apportion to land application vs grazing, and track emissions and nutrient losses through the manure management continuum.
- Outputs designed for publication and easy integration with other models and policy tools.

## Data Inputs and Conceptual Framework

- Node/Link flow structure across six livestock classes: dairy cattle, beef cattle, pigs, sheep and other stock, laying hens, broilers and other poultry.
- Six stages modelled: excretion, housing, grazing, hardstanding, storage, export, spreading; track losses, gains, and transformations (e.g., ammonia, immobilisation).
- Spatial and temporal resolution: outputs at 10 km x 10 km grids with monthly or annual timesteps; can export to spreadsheets and GIS; designed for interoperability with models like MAGPIE, PSYCHIC, NARSES.
- Core data inputs:
  - Primary spatial data from the 2004 Agricultural Census (livestock numbers, land use) on a 10 km grid.
  - Excreta composition and excretion rates from NVZ-AP and RB209 OC contents; adjustments to align cattle/beef categories with census classifications.
  - Validation against national data and published manuals (RB209, NVZ guidance, etc.).

## Key Inputs and Parameters (Tables A20–A25)

- Table A20: monthly proportions of manure types by land use (Grass, Spring cropping, Autumn cropping) for:
  - Cattle slurry and cattle FYM, with detailed monthly patterns (e.g., higher slurry applications in winter on grassland; variations by land use and month).
  - Pig slurry and pig FYM; poultry manure patterns by land use.
- Table A21: ammonia emission factors (EFs) by manure type and housing/storage type (e.g., dairy/slurry housing, solid manure housing, lagoon/tank storage; abatement factors for covers and other practices).
- Table A22: N2O/NO/N2-N emission factors (percent ammonium-N) by livestock and storage/housing type.
- Table A23: CH4-C emission factors (percent of manure OC) by livestock and storage/housing type.
- Table A24: reductions in E. coli concentrations during housing and storage (log reductions and final concentrations by manure type).
- Table A25: typical straw composition (DM, nutrients, OC, E. coli baseline values) used for assumptions in the framework.

## Scenario Testing and Key Findings

- MANURESGIS scenario testing examined seven scenarios to assess policy-relevant changes in emissions and nutrient loadings.

1) Scenario 1: 20% reduction in N and P excretion (dietary changes)
- N excretion: substantial reductions across livestock categories; example effects on total annual N in handled manures and excreta deposited: baseline total around 374 kt N → ~305 kt N (Scenario 1).
- P excretion: notable reductions in total P loadings to land: baseline ~59 kt P → ~45 kt P (Scenario 1).
- Overall: reduced ammonia emissions from housing/storage and land spreading; smaller reductions in nitrate leaching and N2O emissions after spreading.

2) Scenario 2: Move all caged laying hens from deep-pit to belt-scraped housing
- Ammonia losses from laying hens drop from ~4.4 kt to ~3.6 kt (≈20% reduction) during housing.
- Land-spread ammonia emissions may increase slightly due to higher readily available N content; overall manure N use efficiency improves.

3) Scenario 3: Move all dairy cows and housed pigs from slurry to solid manure (FYM)
- Ammonia losses during housing/storage reduce (dairy: 32.7 kt → 26.1 kt; pigs: 8.7 kt → 5.5 kt; total: 41.4 kt → 31.6 kt).
- After land spreading, reductions in nitrate leaching and N2O emissions, but storage emissions for FYM may differ.
- Net reduction in total ammonia-N losses (~24%).

4) Scenario 4: All slurry stores covered
- Ammonia losses reduced by ~2.5 kt total (≈4%), with Pig sector showing larger percentage reductions (≈15%).
- Overall manure N use efficiency increases; land spreading emissions may rise slightly due to drier, higher-N-content slurry.

5) Scenario 5: All dairy cows housed indoors year-round
- Ammonia losses increase markedly: housing, collecting yards, and storage rise; total losses ~33 kt baseline → ~55 kt Scenario 5 (+22 kt; ≈67% increase).
- Net effect: higher housing-related emissions; land spreading emissions may differ due to timing and management.

6) Scenario 6: Extend grazing season (extend grazing; more housing in winter reduced)
- Ammonia losses decrease: 33 kt baseline → 27 kt Scenario 6 (≈18% reduction).
- Direct excreta deposition in fields reduces housing emissions but may increase nitrate leaching and nitrous oxide emissions after spreading.
- Overall manure N use efficiency decreases slightly.

7) Scenario 7: Change livestock numbers to BAU projections (2007–2020)
- N and P excretion decline across several sectors due to reduced herd sizes; total annual N excretion ~10% lower vs Baseline.
- P loadings to land also decline (varies by sector); overall potential reductions in ammonia losses and nitrate leaching following land spreading.
- Results indicate improvements in N and P management under projected industry trends, with accompanying changes in emissions.

- Across scenarios, the tool consistently links management practices and livestock numbers to spatially explicit changes in ammonia, nitrate, nitrous oxide, methane emissions, and nutrient loadings to land.

## Implications for Policy, Modelling and Data Access

- Provides a transparent, modular framework to test how changes in diet, housing, manure handling, and livestock numbers affect diffuse pollution drivers.
- Supports policy discussions on waste management, livestock housing standards, and land-spreading practices; informs planning for nutrient loadings and emissions inventories.
- Scenario results can guide investments (e.g., belt-scraped housing, covered stores, year-round housing) by balancing emission reductions with practical constraints.
- Emphasizes need for up-to-date data; potential for web-based access and broader data sharing; integration with updated nutrient loss/transformation science.

## Limitations and Future Work

- Based on 2004 Agricultural Census data; recommended updates as newer livestock numbers become available.
- Some simplifications in flows (e.g., leachate handling) were made to maintain tractability; validation suggests limited impact but could be refined.
- Future work opportunities: web-based data access, incorporation of newer spatial datasets, and integration with updated science for nutrient losses and transformations.

## Conclusions

- MANURES -GIS offers a robust, flexible framework to estimate annual excreta production, apportionment to land, and loads of nutrients, OC, and E. coli on agricultural land.
- The Node/Link approach, monthly resolution, and 10 km grids provide a transparent basis for policy analysis and integration with other diffuse pollution models.
- Spatial and seasonal patterns show substantial variation in manure and nutrient loadings, with direct implications for pollution control, land management, and bioenergy planning.