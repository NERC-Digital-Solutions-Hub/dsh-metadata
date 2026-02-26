# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

- The NERC Soil Biodiversity Programme (1999-) studied soil biota diversity and ecological functions at Sourhope, Scottish Borders (Grid NT8545019630). The dataset covers soil fauna collected during project 160 (Diversity and functional role of predatory beetles and their prey in the Sourhope ecosystem).
- Site design and scope: 5 randomized complete blocks, 6 treatments per block (30 plots total). Treatments include control, nutrient enhancement (nitrogen & lime, N+L), and chlorpyrifos insecticide (biocide); plots are 20 m x 12 m with specified buffer zones. Insecticide applied monthly May–September; N+L rates: NH4NO3 at 240 kg ha-1 and CaCO3 at 6000 kg ha-1. Whole site mown May–Sept; control plots receive no additional treatments.

## Experimental design and treatments
- Randomized complete block with 5 blocks, 6 treatments per block (30 plots total).
- Treatments:
  - Control (no pesticide or nutrient addition)
  - Nitrogen & Lime (N+L)
  - Biocide (chlorpyrifos)
- Plot structure: main plots A–F with sub-plots; 20 m x 12 m plots; buffer zones between plots.
- Sampling timing: invertebrate sampling conducted July and October 2002 and April, June, and October 2003.

## Invertebrate sampling and identification
- Collembola (springtails) and Spiders via pitfall traps:
  - 11 cm deep, 8 cm diameter, filled with 25% ethylene glycol.
  - 4 traps per main plot (one per sub-plot), 6 m spacing, trapped for 1 week.
  - Spiders identified to species for all four sampling occasions; Collembola identified to species only for July 2002 due to effort constraints.
  - Identification references: Hopkin (2000), Fjellberg (1998), Roberts (1987).
- Invertebrates from soil cores:
  - Two soil cores per sampling occasion per plot (10 cm deep, 8 cm diameter); 8 cores per sub-plot total.
  - Extracted via Tullgren funnel over two weeks and pooled per plot.
  - Identification: order, then family/species where required; key references provided (Joy 1932; Unwin 1984; Lindroth 1974; Forsythe 1987; Cameron et al. 1983; Roberts 1987).
- Slugs:
  - Defined area traps (DATs) of 0.1 m2, with a raised collar installed to 90 mm depth; grass removed to litter layer; cabbage leaf bait; traps checked at 24 and 48 hours; slugs chilled and returned to lab for identification.
- Data structure: a CSV file P00160_ALL_FAUNA.csv with fields describing sampling type, dates, blocks, plots, treatments, species, counts, and biomass where applicable.

## Data structure and key fields
- TYPE and DESCRIPTION: sampling type (e.g., SOIL INVERTEBRATES - TULLGREN; COLLEMBOLA - PITFALL; PITFALL; SPIDER - PITFALL; SLUGS).
- DATE and SAMPLING_DATE: sampling occasion (month/year); actual date or period.
- BLOCK: block number (1–5) and related identifiers.
- MAIN_PLOT and SUB_PLOT: plot designations (A–F and sub-plots).
- CELL_X and CELL_Y: grid coordinates for spatial referencing.
- TREATMENT: plot treatment (Control, Biocide, Nitrogen & Lime).
- SPECIES: species name (for invertebrates when identified).
- SP_COUNT_TRAP, SP_COUNT_m2: trap-based counts (various interpretations across sampling types).
- BIOMASS: slug biomass (mg/m2) or related metrics (where applicable).
- Note: dataset supports per-trap counts, per-m2 densities, and, for slugs, biomass metrics.

## Data quality, usage, and licensing
- Quality control included numeric range checks, formatting conformity, and logical integrity tests.
- Data are QA’d but not guaranteed by NERC; no liability for accuracy or fitness for use. Users should assess suitability for their purposes.
- References for further methodological and contextual reading are provided, including the Sourhope Field Data Handbook (2003) and related studies on chlorpyrifos effects and nutrient treatments.

## Further reading and related resources
- Key publications on the Sourhope experiment and related treatments (2007–2009) exploring insecticide effects, nutrient interactions, and multi-trophic responses.
- Sourhope Field Data Handbook 2003 (Scott et al., 2003) and UK Soil Biodiversity Programme literature for methodological context.
- Data availability note: Supporting Information via EIDC catalogue record.