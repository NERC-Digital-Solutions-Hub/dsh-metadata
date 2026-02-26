# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

- Overview
  - Part of the NERC Soil Biodiversity Thematic Programme (1999–2003) at Sourhope, Scottish Borders, to study soil biota diversity and their functional roles.
  - Data contributed from project 160: Diversity and functional role of predatory beetles and their prey in the Sourhope ecosystem.
  - Focused on monitoring aboveground productivity, species composition, and soil invertebrate diversity using standardized methods.
  - Site located at Sourhope Farm (Grid NT8545019630); 24 projects funded overall, with this dataset representing soil fauna observations under specific treatments.

- Experimental Design
  - Randomized complete block design with five blocks; six treatments per block, but this dataset uses three: control, nitrogen + lime (N + L), and chlorpyrifos (biocide).
  - Plots: 30 total (20 m x 12 m) with buffer zones between plots.
  - Treatments:
    - Nutrient enhancement (N + L): ammonium nitrate and lime applied annually.
    - Insecticide (chlorpyrifos): monthly applications May–Sept (five applications/year).
    - Control: no biocide or nutrient additions beyond mowing.
  - Mowing: entire site cut monthly May–Sept with material removed.

- Invertebrate Sampling and Identification
  - Sampling occasions: July and October 2002; April, June, and October 2003.
  - Collembola & Spiders (pitfall traps):
    - Pitfalls: 11 cm deep, 8 cm diameter, 4 traps per main plot, 6 m spacing, filled with 25% ethylene glycol, collected after 1 week.
    - Spiders identified to species; Collembola identified to species only for July 2002 due to effort constraints.
    - Identification sources: Hopkin (2000), Fjellberg (1998), Roberts (1987).
  - Invertebrates (soil cores):
    - Two soil cores per sampling occasion per main plot (eight cores per sub-plot) extracted via Tullgren funnels over two weeks.
    - Identified to order; families or species where needed (Beetles, Slugs, Spiders referenced to standard keys).
  - Slugs:
    - Defined Area Traps (DATs): four per plot; 0.1 m2 area; baited with cabbage leaf; checked at 24 and 48 h.
  - Data structure:
    - Raw data compiled in P00160_ALL_FAUNA.csv with fields detailing sampling type, date, plot layout (block, main plot, sub-plot, grid cell), treatment, species, and counts/biomass.

- Data Structure and Content
  - File: P00160_ALL_FAUNA.csv
  - Sampling types included in the dataset:
    - SOIL INVERTEBRATES - TULLGREN: two soil cores per sub-plot (Control, N+L, Biocide); invertebrates extracted via Tullgren funnel.
    - COLLEMBOLA - Pitfall traps: Collembola identified to species for July 2002; abundance data for all samples.
    - PITFALL - Pitfall traps: general trap data.
    - SPIDER - PITFALL: spiders from pitfall samples.
    - SLUGS - DAT traps: slug counts per plot from defined area traps.
  - Key fields:
    - DATE / SAMPLING_DATE: sampling occasion (month/year or period).
    - BLOCK: Block number (1–5).
    - MAIN_PLOT, SUB_PLOT: plot identifiers (A–F and sub-division within plots).
    - CELL_X, CELL_Y: grid coordinates within the study area.
    - TREATMENT: treatment code (Control 1, Biocide, Nitrogen & Lime/ NL).
    - SPECIES: species name (where identified).
    - SP_COUNT_TRAP, SP_COUNT_m2, BIOMASS: counts per trap, per m2, and biomass (for slugs where applicable).
  - Data notes:
    - Absolute densities from soil cores; abundance from pitfall traps and slug DATs.
    - Taxonomic identifications supported by standard keys and references listed in the document.

- Quality Control and Use
  - Quality control: numeric range checks, data formatting conformity, and logical integrity checks.
  - Caveats:
    - Data subject to QA procedures; no warranty on accuracy by NERC.
    - NERC disclaims responsibility for fitness of use and for any losses or damages arising from use of the data.
  - Data management: datasets designed to be stored, curated, and uploaded to appropriate data portals; underlying data available for reuse with proper understanding of limitations.
  - Further reading and related work:
    - Several associated publications exploring insecticide effects on spider and Collembola communities and multitrophic interactions.
    - Sourhope Field Data Handbook (2003) and related UK soil biodiversity literature referenced for context and methodology.

- Relevance for Environmental Monitoring and Analysis
  - Demonstrates standardized, replicable methods for monitoring soil invertebrate communities under controlled treatments.
  - Provides a structured dataset suitable for analysis of treatment effects on biodiversity, community composition, and potential predation dynamics (e.g., predatory beetles and prey).
  - Aligns with monitoring aims to verify data quality, enable cross-study comparisons, and facilitate data sharing for broader environmental health assessments.
  - Highlights ongoing need to increase data value by integrating with additional data sources and ensuring broad data accessibility.