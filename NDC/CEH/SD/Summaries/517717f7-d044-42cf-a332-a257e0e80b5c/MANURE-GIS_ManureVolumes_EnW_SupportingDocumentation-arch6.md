# The National Inventory and Map of Livestock Manure Loadings to Agricultural Land: MANURES - GIS

## Overview
- Develops a national, GIS-based inventory and map of livestock manure loadings to agricultural land.
- Quantifies nutrients (N, P, K), organic carbon (OC) and microbial pathogens (E. coli) from livestock manures on a spatial and temporal basis.
- Produces monthly and annual land loadings and supports policy modelling with a software policy-support tool.

## Data inputs and architecture
- Spatial data: 2004 Agricultural Census (10 km grid) for livestock numbers and land use.
- Excreta data: derived from NVZ-AP and related Defra projects; includes N, P, K excretion plus OC and E. coli data.
- Land-use distributions and timing: based on 2004/2007 datasets (e.g., British Survey of Fertiliser Practice) with monthly excretion/spreading timing from NARSES and Defra surveys.
- Apportionment: look-up tables link manure types to land uses and monthly application patterns.

## Model structure and processing
- Node-and-Link framework:
  - Source Nodes (inputs for animal numbers and excreta)
  - Housing, Hardstanding, Storage, Export, Grazing, Spreading
  - Constraint/Watcher/Marker nodes for timing and audits
- Data management:
  - Data dictionary tracks spatial/temporal/national data, straw additions, water dilution, transformations.
- Monthly calculations:
  - Route manure through nodes with losses, gains, and transformations (e.g., NH3, CH4) to compute N, P, K, OC, and E. coli loadings to land.
- Spreading and land use:
  - Proportions spread to grassland, spring/autumn cropping, normalized to local land-use in 10 km grid cells.
- Outputs:
  - Tables, graphs, and GIS maps by manure type and land-use combination; supports monthly/annual temporal analysis and spatial distribution.
  - Exportable data for integration with other models (MAGPIE, PSYCHIC) and higher-resolution needs (e.g., 1 km^2).

## Outputs and data products
- Quantities:
  - Manure produced; land loadings by nutrient and OC; direct excreta loadings on grassland.
- Nutrients and OC:
  - N, P, K, and OC loadings with regional patterns linked to livestock density.
  - E. coli loadings reported per hectare alongside nutrients.
- Temporal and spatial resolution:
  - 10 km x 10 km grid; monthly timesteps with annual aggregates; can be aggregated to finer scales for compatibility with other models.
- Visuals and data exports:
  - GIS maps, figures, and data matrices by livestock type and land-use; ready for policy analysis and scenario testing.

## Validation and reliability
- Benchmarked against national datasets (RB209, NT2006 MANDE, NVZ-AP) with good agreement for nutrients and ammonia losses.
- Outputs reflect known patterns and established datasets, supporting policy and modelling reliability.

## Applications and uses
- Policy and modelling support:
  - Underpins Ammonia Emissions Inventory, N2O and nitrate leaching assessments (MAGPIE, PSYCHIC) and phosphorus loss estimates (PSYCHIC).
- Scenario planning:
  - Evaluate environmental impacts of changing livestock numbers, housing systems, manure management, and regulatory measures.
- Practical planning:
  - Inform manure management infrastructure development (e.g., anaerobic digestion locations/capacities).

## Timing, granularity and accessibility
- Temporal: monthly timesteps with annual totals.
- Spatial: 10 km x 10 km grid; outputs can be aggregated to 1 km^2 as needed for model compatibility.
- Accessibility: outputs and GIS viewer included; designed for self-serve use by policymakers and researchers.

## Data management, tools and operational notes
- Implementation: MANURES-GIS is a VBA-based tool with Engine, Data Manager, and Framework Manager.
- Framework Manager: GUI for designing Node/Link frameworks and labeling stages; supports default value edits and custom actions.
- Data Manager: data import (spatial/non-spatial), scenario management, GIS viewing, and exporting for MAGPIE and PSYCHIC.
- Extensibility: VBA modules enable integration with other models (e.g., MANNERNPK, PLANET) for expanded capabilities.

## Scenario testing (using MANURES-GIS)
- Purpose: test impacts of changes to husbandry practices and manure management. Seven scenarios assessed against the England & Wales Baseline.

1) Reduce N and P excretion by livestock (dietary changes)
- N and P excretion reduced by 20%.
- Results: substantial reductions in ammonia emissions (approx. 14 kt N) and land nitrate leaching; notable reductions in total N and P loadings.

2) Move all caged laying hens from deep pit to belt-scraped housing
- Shifts reduce housing ammonia losses by about 20% in laying hens.
- Outcome: lower housing/storage losses but potential slight increases in land-spread ammonia and N losses due to higher readily available N content in belt-scraped manure.

3) Move all dairy cows and housed pigs from slurry to solid manure (FYM)
- Assumes ~30% housing ammonia reduction (as with FYM). 
- Outcome: total ammonia-N losses reduced by about 9.8 kt (roughly 24%), with downstream reductions in land spreading emissions, though some storage-phase nitrous oxide may increase.

4) Cover all slurry stores
- Slurry-store coverings reduce storage ammonia emissions (~4% total) with larger relative gains in pigs; significant investment required.
- Outcome: overall ammonia-N losses drop by about 2.5 kt (4%).

5) House all dairy cows indoors year-round
- Increases ammonia losses across housing, collecting yards, and storage.
- Outcome: total ammonia losses rise by roughly 67% (about 22 kt), reducing grazing-related benefits.

6) Extend grazing season (reduce indoor housing months)
- Extending grazing lowers housing losses; overall ammonia losses decrease by about 18%.
- Outcome: better balance with field deposition but potential increases in nitrate leaching and N2O from land spreading.

7) Change livestock numbers to Business As Usual projections (BAU)
- Reductions in dairy, beef, sheep, pigs; increases in poultry; overall ~10% decrease in total N and P loadings.
- Outcome: phosphorus loadings to land decrease and related losses reduce, with overall improved manure use efficiency.

- Note: Results include scenario-specific tables (A26–A33) detailing N and P totals, and accompanying figures illustrating spatial patterns and emissions.

## Recommendations for future work
- Develop a simple web-based version of MANURES-GIS to improve data accessibility.
- Update inputs with newer spatial datasets and revised livestock production standards.
- Refine inputs and loss/transformations as new scientific data become available, maintaining compatibility with updated models.

## Key takeaways for Data Support
- MANURES-GIS is a robust, transparent data-driven framework for quantifying and mapping manure and nutrient loadings across England and Wales.
- Integrates diverse data sources (census, NVZ guidance, field studies) into an auditable, version-traceable model with clear provenance.
- Outputs are self-serve, enabling policy analysis, scenario testing, and integration with other environmental models.