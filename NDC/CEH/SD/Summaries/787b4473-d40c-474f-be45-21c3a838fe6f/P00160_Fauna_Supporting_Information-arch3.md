# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, aiming to understand soil biota diversity and their functional roles in ecological processes.
- This dataset pertains to the project on the diversity and functional role of predatory beetles and their prey, within a larger program examining soil structure, processes (carbon and nitrogen cycles), and soil micro- and macro-fauna.

## Experimental design and treatments
- Site used a randomized complete block design: 5 blocks, 6 treatments per block (30 plots total).
- Three treatments analyzed here: control, nutrient enhancement with lime (N + L), and chlorpyrifos insecticide.
- Plot details: 20 m x 12 m with buffer zones between plots.
- Treatment specifics:
  - Insecticide: chlorpyrifos applied monthly May–September (5 applications/year) at 1.5 L/ha (720 g active ingredient per ha).
  - Nutrient enhancement (N + L): nitrogen as NH4NO3 (240 kg/ha) and lime CaCO3 (6000 kg/ha); nitrogen applied twice yearly (early and late spring), lime between nitrogen applications.
- Site management: whole site mown monthly May–September with cut material removed.

## Invertebrate sampling and taxa targeted
- Sampling periods: July and October 2002; April, June, and October 2003.
- Methods and targets:
  - Collembola (springtails) and spiders via pitfall traps (4 traps per main plot; 6 m spacing; samples stored in 70% alcohol; spiders identified to species; Collembola identified to species only for July 2002 due to effort constraints).
  - Soil invertebrates via two soil cores per sub-plot (10 cm deep, 8 cm diameter) collected per sampling occasion; extraction with Tullgren funnels over two weeks; identification to order, then to family/species where needed.
  - Beetles identified to species using standard keys; slugs identified with genus-specific keys; spiders identified as above.
  - Slugs assessed using defined area traps (DATs) in each plot, with cabbage leaf bait, and 24- to 48-hour checks.
- Data sources and references for taxonomy and methods provided.

## Data structure and content
- Data file: P00160_ALL_FAUNA.csv
- Key data elements include:
  - TYPE: sampling method (e.g., SOIL INVERTEBRATES - TULLGREN; COLLEMBOLA; PITFALL; SPIDER - PITFALL; SLUGS)
  - DATE/SAMPLING_DATE: sampling occasion (month/year)
  - BLOCK: block number (1–5)
  - MAIN_PLOT: main plot identifier (A–F)
  - SUB_PLOT: sub-plot identifier
  - CELL_X/CELL_Y: grid coordinates
  - TREATMENT: treatment (Control, Biocide/N+L, Nitrogen & Lime)
  - SPECIES: species name
  - SP_COUNT_TRAP: counts from traps (different interpretations depending on TYPE)
  - SP_COUNT_m2: counts per square meter (for certain types)
  - BIOMASS: slug biomass (for DAT-derived data) or related metrics
- Metadata and variable descriptions accompany the dataset, including sampling dates and plot design references.

## Quality control and governance
- Quality checks include numeric range validation, data format conformity, and logical integrity checks.
- Data are subject to quality assurance; however, NERC disclaims warranty of accuracy and accepts no liability for use of the data.
- Data governance considerations include documentation of methods, identification keys, and provenance; underlying data sharing is allowed but may be constrained by governance and metadata completeness.

## Accessibility and references
- Data are provided as Supporting Information via the EIDC catalogue record.
- Related materials include the Sourhope Field Data Handbook (2003) and several subsequent papers detailing effects of chlorpyrifos and nutrient/insecticide interactions.
- Key further readings:
  - The effects of chlorpyrifos on spider and Collembola communities.
  - Multitrophic effects of nutrient addition in upland grassland.
  - Effects of nutrient and insecticide treatments on invertebrate numbers and predation on slugs.

## Relevance to environmental health monitoring
- Demonstrates a rigorous approach to multi-taxa soil health monitoring using a factorial experimental design to isolate treatment effects (insecticide and nutrient amendments).
- Exemplifies critical data management practices for monitoring frameworks: explicit metadata, standardized sampling protocols, species-level identifications where feasible, and clear data structure.
- Highlights common data governance and use barriers relevant to monitoring systems:
  - Need for complete metadata and taxonomic keys.
  - Potential data sharing constraints and liability considerations.
  - Importance of data quality checks and documentation of provenance.
- Provides a case study of integrating ecological measurements (diversity, abundance, and functional roles in soil ecosystems) with management interventions (insecticides and nutrient amendments) to inform policy and future monitoring decisions.