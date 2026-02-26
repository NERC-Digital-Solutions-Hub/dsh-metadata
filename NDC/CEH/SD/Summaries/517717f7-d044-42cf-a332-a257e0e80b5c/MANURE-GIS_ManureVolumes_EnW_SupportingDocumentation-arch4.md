# The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

## Overview
- A Defra-funded GIS tool and dataset to produce a national inventory and map of livestock manure loadings to agricultural land.
- Outputs support diffuse pollution and emissions modelling (NH3, N2O, NO, CH4, P, N leaching) and underpin Defra policy assessments.
- Outputs can be exported as tables, graphs, or GIS maps at 10 km × 10 km (monthly or annual) and can link to models like MAGPIE and PSYCHIC.

## Data Architecture and Handling
- Framework uses separate conceptual models per sector (dairy, beef, pigs, sheep/other stock, layers, broilers/poultry).
- Node types include Source, Housing, Hardstanding, Storage, Export, Grazing, Spreading, Constraint, Marker, Watcher; links define monthly flows with proportions.
- Data Dictionary stores spatial/temporal/national inputs (e.g., straw composition, monthly spreading), and an Engine computes monthly distributions and transformations (losses/gains) across Nodes.
- Look-up tables drive spreading decisions by land use (grassland, crops) with probabilities normalised to local land-use distributions.
- Outputs include nutrient loads (N, P, K), OC, and E. coli by Node, stage, livestock type, and land use; large data volumes with maps and tables; interfaces support integration with MAGPIE and PSYCHIC.

## Data Inputs and Sources
- Spatial and livestock data: 2004 Agricultural Census (10 km grid).
- Excreta content and production data: NVZ-AP, Cottrill & Smith; RB209 for manure compositions.
- Supporting data: NARSES, 2007 British Survey of Fertiliser Practice, WA0716, NT2006 MANDE for OC and E. coli; NVZ emission and nitrate guidance.
- Outputs are generated for monthly timesteps and multiple resolutions (1 km^2 and 10 km^2) for compatibility with other models.

## Outputs and Validation
- Outputs quantify loadings of N, P, K, OC, and E. coli; also track transformations (NH3, N2O, NO, CH4, CO2, immobilisation, mineralisation, leaching, evaporation).
- Validation benchmarks against RB209 manure composition data and NVZ-N excretion; NH3 losses align closely with the 2008 Ammonia Emissions Inventory.

## Scenario Testing and Results
- The tool supports scenario analyses to test policy/practice changes (monthly timing, housing, storage, grazing, and livestock numbers). Seven scenarios were analyzed against the Baseline England/Wales context.

1) Scenario 1: Reduced N and P excretion by 20% (dietary changes)
- N: Baseline total ~374 kt (handled/manured + grazing excreta) reduced to ~305 kt.
- P: Baseline total ~59 kt reduced to ~45 kt.
- Impacts: Lower ammonia emissions from housing/storage and reduced nitrate leaching and N2O emissions after land spreading.

2) Scenario 2: Move all caged laying hens from deep pit to belt-scraped housing
- Ammonia losses from housing reduced from ~4.4 kt to ~3.6 kt (~0.8 kt decrease).
- Potential increase in readily available N in layer manure leading to slightly higher land-spreading ammonia and nitrate leaching, but overall manure N use efficiency increases.

3) Scenario 3: Move all dairy cows and housed pigs from slurry to solid manure (FYM)
- Ammonia losses decrease: dairy ~6.6 kt; pigs ~3.2 kt; total ~9.8 kt (≈24% reduction).
- Land-spreading losses and associated N transformations also reduce; storage emissions may rise, offsetting some gains.

4) Scenario 4: Cover all slurry stores
- Ammonia losses decrease by ~2.5 kt overall (≈4%), with larger relative gains in pigs.
- Greater dry matter and readily available N in slurry could increase land-spreading emissions slightly.

5) Scenario 5: All dairy cows housed indoors (no grazing)
- Ammonia losses increase by ~22 kt (≈67% rise) due to housing/collection/storage increases.
- Land spreading emissions may rise or differ due to timing; overall manure N use efficiency changes favorably or unfavorably depending on management.

6) Scenario 6: Extend the grazing season
- Ammonia losses decrease by ~6 kt (≈18%) in dairy sector.
- Direct deposition of excreta in fields reduces housing emissions but increases nitrate leaching and N2O emissions after spreading; overall manure N use efficiency decreases.

7) Scenario 7: Change livestock numbers to BAU projections (2020)
- N reductions: ~10% (Baseline total ~684 kt N; Scenario 7 ~616 kt).
- P reductions: ~9–10% (Baseline ~131 kt; Scenario 7 ~119 kt).
- Overall, reductions in N and P loads with accompanying changes in emissions/agrarian dynamics.

## Implications for Policy and Data Leadership
- Provides a transparent, auditable data-driven framework for quantifying manure-derived nutrient loadings at national and grid scales.
- Integrates diverse data sources (census, guidance, practice surveys, and emissions studies) into a cohesive modelling platform with explicit loss and transformation physics.
- Supports policy inventories and scenario analysis for emissions (NH3, N2O) and nutrient management (N, P, K, P runoff) within broader environmental models.
- Validated against established datasets to strengthen credibility for data-driven decision making.
- Data governance and publication considerations are integrated to balance openness with confidentiality where needed.

## Recommendations and Future Work
- Develop a simple web-based version to broaden policy-maker and researcher access.
- Update spatial data with newer livestock censuses and revised production standards; refresh understanding of nutrient losses and transformations.
- Improve linkages and integration with other modelling frameworks and reflect new scientific findings.