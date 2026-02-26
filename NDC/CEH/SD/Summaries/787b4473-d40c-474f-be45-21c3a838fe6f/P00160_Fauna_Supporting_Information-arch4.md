# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, Scotland, to study soil biota diversity and functional roles in ecological processes.
- Data pertain to project 160 focusing on diversity and functional roles of soil fauna and their predation in the Sourhope ecosystem.
- Site details: Sourhope field site, randomized experiments with multiple treatments to assess impacts on soil invertebrates and associated processes.

## Experimental design
- Design: Randomized complete block with five blocks; six treatments per block (30 plots total).
- Treatments used in this dataset: control, nutrient enhancement with lime (N+L), and chlorpyrifos insecticide; other plots included but not central to this data subset.
- Plot dimensions: 20 m x 12 m; buffer zones between plots.
- Treatment specifics:
  - Insecticide: chlorpyrifos applied monthly May–September (five applications/year) at 1.5 L ha-1 (720 g a.i. ha-1).
  - Nutrient enhancement (N+L): ammonium nitrate (NH4NO3) at 240 kg ha-1 and lime (CaCO3) at 6000 kg ha-1.
- Management: site mown monthly May–September with cut material removed.
- Documentation includes a figure showing plot locations and treatment assignments.

## Invertebrate sampling and identification
- Sampling times: July and October 2002; April, June, and October 2003.
- Collembola and spiders (pitfall traps):
  - 11 cm deep, 8 cm diameter traps with 25% ethylene glycol; four traps per main plot (one per sub-plot), 6 m apart.
  - Traps collected after 1 week; specimens stored in 70% ethanol.
  - Species-level identification for spiders and July 2002 Collembola; other Collembola abundance data available.
  - Identification keys cited for Collembola and spiders.
- Invertebrates from soil cores:
  - Two soil cores per sampling occasion per plot (10 cm deep, 8 cm diameter); total 120 cores per occasion.
  - Extraction via Tullgren funnel over two weeks; pooled per plot.
  - Identification to order; beetles to species where required; slugs and spiders identified with species-level keys.
- Slugs (defined area traps, DATs):
  - 0.1 m2 traps with galvanized collar; cabbage leaf bait; 24- and 48-hour checks; slugs chilled and stored for lab identification.
- Data capture and metadata are organized in a comma-separated file (see Data Structure).

## Data structure and contents
- Data file: P00160_ALL_FAUNA.csv
- Data types and fields include:
  - TYPE: Sampling type (SOIL INVERTEBRATES - TULLGREN; COLLEMBOLA; PITFALL; SPIDER - PITFALL; SLUGS)
  - DATE / SAMPLING_DATE: Sampling occasion (month/year or date)
  - BLOCK: Block number (1–5)
  - MAIN_PLOT: Main plot letter (A–F)
  - SUB_PLOT: Sub-plot identifier
  - CELL_X / CELL_Y: Grid cell coordinates
  - TREATMENT: Treatment label (Control, Biocide [chlorpyrifos], Nitrogen & Lime)
  - SPECIES: Species name
  - SP_COUNT_TRAP: Trap-based counts (various interpretations depending on TYPE)
  - SP_COUNT_m2 / BIOMASS: Counts per square meter or biomass metrics
- The dataset encompasses various sampling methods and provides both abundance and, where applicable, biomass metrics for invertebrates (including Collembola, spiders, beetles, slugs, and other invertebrates).

## Data usage, context, and related reading
- Related publications exploring treatment effects and multitrophic interactions:
  - The effects of chlorpyrifos on spider and Collembola communities (Pedobiologia, 2007)
  - Multitrophic effects of nutrient addition in upland grassland (Bulletin of Entomological Research, 2008)
  - Effects of nutrient and insecticide treatments on invertebrate numbers and slug predation (Agriculture, Ecosystems & Environment, 2009)
- Useful companion resources:
  - Sourhope Field Data Handbook (2003) and related Supporting Information via EIDC catalogue
  - General context on UK Soil Biodiversity Programme (Usher et al., 2006)

## Data quality, access, and limitations
- Quality control: Numeric range checks, formatting conformity, and logical integrity checks implemented.
- Data responsibility: While quality assurance procedures were applied, NERC does not warrant the data’s accuracy or fitness for a particular use; no liability for losses or damages arising from data use.
- Accessibility: Data are provided with metadata and are suitable for analyses of treatment effects on soil invertebrates, as well as cross-method comparisons and multi-trophic interactions, subject to the stated quality caveats.