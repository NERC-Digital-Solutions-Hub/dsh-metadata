# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Large field experiment at Sourhope, Scottish Borders (Macaulay/Sourhope site) to study soil biodiversity and functional roles of soil biota.
- Part of the NERC Soil Biodiversity Thematic Programme (1999–) with 24 projects; this dataset comes from project 160, focusing on diversity and predation roles of soil fauna.
- Data cover soil fauna collected during the Sourhope project including predatory beetles and their prey.

## Experimental Design
- Randomized complete block design: 5 blocks, 6 treatments per block (30 plots total).
- Three treatments used for this faunal sampling: control, nutrient enhancement (nitrogen & lime, N+L), and chlorpyrifos insecticide (biocide).
- Plot size and layout: 20 m x 12 m plots with buffer zones between plots (1.5 m on the longest edge; 3–5 m on the shorter edge).
- Treatments:
  - Nutrient enhancement (N+L): ammonium nitrate (NH4NO3) at 240 kg ha^-1 and lime (CaCO3) at 6000 kg ha^-1.
  - Insecticide: chlorpyrifos applied monthly May–September (5 applications/year) at 1.5 L ha^-1 (720 g a.i. ha^-1).
  - Control: no pesticide or nutrient amendments beyond mowing.
- Whole-site management: monthly mowing May–Sept with cut material removed.

## Sampling Methods and Taxa
- Invertebrate sampling schedule: July and October 2002; April, June, and October 2003.
- Collembola & Spiders (pitfall traps):
  - 4 traps per main plot (1 per sub-plot), 11 cm deep x 8 cm diameter, quarterly filled with 25% ethylene glycol, positioned 6 m apart.
  - Traps removed after 1 week; spiders identified to species; Collembola identified to species only for July 2002 due to practicality; abundance data available for all samples.
  - Identification keys cited: Collembola (Hopkin 2000; Fjellberg 1998), spiders (Roberts 1987).
- Invertebrates (soil cores):
  - Two soil cores per sub-plot (10 cm deep x 8 cm diameter) per sampling occasion; pooled per plot (8 cores total per sampling).
  - Extraction via Tullgren funnel over two weeks; identified to order, then to family/species where needed.
  - Beetles identified using standard keys; slugs and spiders identified with referenced guides.
- Slugs (defined area traps, DATs):
  - Four DATs per plot; 0.1 m^2 area; traps embedded 90 mm deep; grass within DATs searched for slugs at 24 h and 48 h after baiting with a cabbage leaf.
  - Slugs identified in laboratory.
- Data structure: CSV file P00160_ALL_FAUNA.csv with detailed field descriptions (see Data Structure section).

## Data Structure and Contents
- File: P00160_ALL_FAUNA.csv
- Categories of sampling types:
  - SOIL INVERTEBRATES - TULLGREN: two soil cores per sub-plot per treatment (Control, N+L, Biocide); invertebrates extracted via Tullgren funnel.
  - COLLEMBOLA - PITFALL: Collembola identified to species (July 2002); traps across Control, N+L, Biocide.
  - PITFALL: pitfall trap data (spiders, Collembola counts per trap).
  - SPIDER - PITFALL: spider counts from pitfall traps.
  - SLUGS: slug counts from DATs.
- Key fields:
  - BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y
  - TREATMENT (Control, Nitrogen & Lime, Biocide)
  - SPECIES (taxon name)
  - SP_COUNT_TRAP, SP_COUNT_m2, BIOMASS (slug data)
  - SAMPLING_DATE and DATE (month-year)
  - TYPE and DESCRIPTION (sampling type details)
- Data are organized to support per-trap, per-plot, and per-species analyses, with counts and biomass where applicable.

## Quality Control and Accessibility
- Quality control: numeric range checks, formatting conformity, and logical integrity checks.
- Data is subject to QA procedures; however, NERC does not warrant the data’s accuracy or fitness for any particular use and accepts no liability for misuse.
- Data availability and additional materials:
  - Supporting Information and Data Handbook (SOURHOPE FIELD DATA HANDBOOK 2003) available via EIDC catalogue.
  - Related publications and additional readings listed for context and methodology.
- Access notes:
  - Data may require understanding of field protocols and taxonomy; multiple data sources and historical context may be needed for comprehensive analysis.

## Related Publications and Further Reading
- Key related works and data handbooks:
  - Fountain et al. 2007, 2008, 2009 (effects of chlorpyrifos and nutrient treatments on soil biota and trophic interactions)
  - Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003)
  - Usher et al., 2006 (Understanding biological diversity in soil)
- These references provide methodological context, validation, and applications of the data in multi-trophic and ecosystem-process studies.

## Potential Analytical Use
- Assess treatment effects on soil fauna abundance, diversity, and biomass across multiple trophic groups.
- Examine multi-trophic interactions, e.g., predatory beetles and their prey under nutrient enrichment or insecticide exposure.
- Explore temporal dynamics across sampling dates (2002–2003) and spatial variation within blocks and plots.
- Support model development for predicting ecological responses to nutrient amendments and pesticide applications at a local scale.