# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

## Aims and Context
- Part of the NERC Soil Biodiversity Thematic Programme (1999) to understand soil biota diversity and their functional roles.
- Focused on a large field experiment at Sourhope, Scottish Borders, monitoring aboveground productivity, species composition, and relative abundance to study soil biota and ecological processes.
- The dataset corresponds to project 160: Diversity and functional role of predatory beetles and their prey in the Sourhope ecosystem.

## Experimental Design
- Randomized complete block design with five blocks; six treatments per block (30 plots total).
- Three treatments used for this faunal sampling: control, nutrient enhancement with lime (N+L), and chlorpyrifos insecticide (15 plots).
- Plot size: 20 m x 12 m with buffer zones between plots.
- Treatments:
  - Nutrient enhancement (N+L): nitrogen (NH4NO3) at 240 kg ha-1 and lime (CaCO3) at 6000 kg ha-1.
  - Insecticide: chlorpyrifos applied monthly May–September (5 applications per year) at 1.5 L ha-1 (720 g a.i. ha-1).
  - Control: no pesticide or added nutrients beyond mowing.
- Site management: monthly mowing May–September; cut material removed.

## Sampling Methods and Taxonomic Coverage
- Invertebrate sampling occurred in July and October 2002, and April, June, and October 2003.
- Collembola and spiders (pitfall traps):
  - Pitfall traps (11 cm deep, 8 cm diameter) with 25% ethylene glycol, four traps per main plot (one per sub-plot), 6 m apart.
  - Traps collected after 1 week; spiders identified to species across all samples; Collembola identified to species only for July 2002 due to effort constraints.
  - Identification references: Hopkin (2000) for Collembola, Fjellberg (1998) for Collembola, Roberts (1987) for spiders.
- Invertebrates (soil cores):
  - Two soil cores (10 cm deep x 8 cm diameter) per sampling occasion adjacent to pitfall traps (8 cores per plot total per occasion).
  - Extraction via Tullgren funnels over two weeks; organisms pooled per plot.
  - Identification to order, with family/species where needed. Beetles identified using Joy (1932), Unwin (1984), Lindroth (1974), Forsythe (1987); slugs using Cameron et al. (1983); spiders as above.
- Slugs (defined area traps DATs):
  - Four DATs per plot; contained 0.1 m2 area each; traps extended into the litter layer and baited with cabbage leaves; checked at 24 and 48 hours; slugs identified in the lab.
- Data scope: measurements include abundance, biomass where applicable, and species-level data for certain groups.

## Data Structure and Contents
- Data file: P00160_ALL_FAUNA.csv
- Key structure elements (types and content):
  - TYPE, DESCRIPTION: Sampling types (soil invertebrates via Tullgren, Collembola, Pitfall, Spider-Pitfall, Slugs) and corresponding data aggregation notes.
  - TYPE, UNITS and TYPE, DATA_TYPE: Data type declarations (text, numeric, etc.).
  - DATE, DESCRIPTION; SAMPLING_DATE: Sampling occasion and date information (month-year or text period).
  - BLOCK: Block number (1–5).
  - MAIN_PLOT: Main plot identifier (A–F).
  - SUB_PLOT: Sub-plot designation.
  - CELL_X, CELL_Y: Grid cell coordinates within plots.
  - TREATMENT: Treatment descriptor (Control, Nitrogen & Lime, Biocide/Chlorpyrifos).
  - SPECIES: Species name (where identified).
  - SP_COUNT_TRAP, SP_COUNT_m2: Counts per trap and per square meter for pitfall, spider-pitfall, Collembola (as applicable).
  - BIOMASS: Biomass measures (notably for slugs; units mg/m2 or similar as indicated).
- Coverage:
  - Data span across sampling occasions (2002 and 2003) with multiple data dimensions (species counts, trap-level counts, and biomass).

## Data Quality and Provenance
- Quality control steps included numeric range checks, formatting conformity, and logical integrity checks.
- Data are subject to quality assurance, but the providing body (NERC) does not warrant full accuracy or fitness for a specific use; no liability for errors or misuse is assumed.
- Metadata and experimental design details are provided to support data interpretation and re-use.

## Related Resources and Further Reading
- Related publications on the broader Sourhope dataset and insecticide/nutrient effects:
  - Fountain et al. (2007) Pedobiologia: effects of chlorpyrifos on spider and Collembola communities.
  - Fountain et al. (2008) Bulletin of Entomological Research: multitrophic effects of nutrient addition in upland grassland.
  - Fountain et al. (2009) Agriculture, Ecosystems & Environment: effects of nutrient and insecticide treatments on invertebrate numbers and slug predation.
- Sourhope Field Data Handbook 2003 (Scott et al., available as Supporting Information via EIDC).
- Usher et al. (2006) Understanding biological diversity in soil (Applied Soil Ecology) for broader programme context.

## Practical Considerations for Data Support and Reuse
- Useful for analyses of treatment effects on soil invertebrate communities, predator-prey dynamics (e.g., spiders and Collembola), and slug populations under pesticide and nutrient regimes.
- Data can support self-serve insights via dashboards or pivot tables by plot, treatment, and sampling occasion, given the structured MAIN_PLOT/SUB_PLOT and BLOCK metadata.
- Potential limitations to note:
  - Species-level identifications available only for certain groups/times.
  - Some data (e.g., Collembola species identifications) are limited to specific sampling events.
  - Not all taxonomic groups are equally represented across all sampling dates.