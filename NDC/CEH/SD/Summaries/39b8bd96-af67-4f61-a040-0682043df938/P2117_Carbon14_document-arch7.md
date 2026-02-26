# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme]

## Overview
- Reports measurements of carbon-14 transfer from plants to soil within mesh cores, tracing movement through shoots, roots, soil, and respiration.
- Part of the NERC Soil Biodiversity Thematic Programme (started 1999) at Sourhope field site, Scottish Borders.
- Aimed at understanding how mycorrhizal networks influence carbon and nutrient cycling in grassland soils.

## Study context and site
- Field site: Sourhope, Kelso, Scotland (NGR: NT 854196; broader project site grid reference NT8545019630).
- Grassland community: upland turf (U4d) with 24 higher plant species; majority form AM-mycorrhizas.
- Long-term management: no fertilizer for at least 40 years.
- Project: 2117, “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”

## Data collection and methods
- Experimental setup: nylon mesh-bound cores (35 µm pore size; 22 mm diameter, 120 mm deep) inserted into intact turf to control AM hyphae colonization while excluding roots.
- Cores: 16 total (in 8 turfs; 2 cores per turf: one rotated, one static).
- Post-labelling exposure: 14CO2 introduced for a 3-hour daytime period; turfs then incubated in growth room (controlled temperature cycle).
- Tracking: 14CO2 traced through plant shoots, soil, roots, and respiration via NaOH traps in core headspace.
- Sampling timeline: 14C measurements taken at 6, 20, 28, 42, 51, and 70 hours post-labelling; final biomass and soil/root samples processed at 70 hours.
- Analytical methods: drying of plant material, combustion in a Packard oxidiser, liquid scintillation counting; NaOH traps dissolved in scintillation fluid for counting.
- Key metrics: total 14C in shoots, soil, roots; 14C in CO2 respired from cores; estimation of 14C allocation to AM mycelium by comparing rotated vs static cores.
- Primary data source: field turf at Sourhope; initial shoot 14C ranged 103–245 nmol 14C per pot, with 70-hour shoot content decreasing significantly.

## Data products
- Dataset: 1079 14C transfer 1.0 (P2117_14C_TRANSFER_1.csv)
- Sample schema:
  - SAMPLEID: unique sample identifier
  - SAMPLE_TYPE: Pot (1-7), Rotated core (1-7), Static core (1-7)
  - SAMPLE_DATE: date of sampling
  - HOURS_POST_LABELLING: hours after labelling
  - SHOOT_14C: 14C in plant shoots (nmol 14C g shoot dwt-1)
  - RESP_14C: 14CO2 evolved from cores (pmol 14CO2 h-1 cm-2)
  - SOIL_14C: 14C in soil (nmol 14C g soil dwt-1)
  - ROOT_14C: 14C in soil from cores/roots (nmol 14C g root dwt-1)
- Data context:
  - Analysis conducted August 2000.
  - Pots and cores included both rotated and static configurations to separate mycorrhizal/mycelial contribution.
- Data quality and metadata:
  - Includes detailed methodological notes in the dataset description and linked references.
  - Site and method descriptions embedded in project context.

## Analysis and interpretation notes
- Allocation of 14C to AM mycelium can be inferred by comparing static versus rotated cores, indicating the extent of mycelial transfer from plant to soil.
- Observed rapid loss of 14C from shoots over the 70-hour period, consistent with redistribution dynamics in the grassland-mycorrhizal system.

## Quality control and limitations
- Quality checks performed: numeric range checks, formatting conformity, and logical integrity checks.
- Quality assurance is applied, but data accuracy and fitness for a specific purpose are not guaranteed by NERC.
- Users should assess data suitability for their GIS-based analyses and accompany results with caveats from the original methodologies.

## References and further reading
- Johnson, D., Leake, J.R., Read, D.J. (2001). Novel in-growth core system enables functional studies of grassland mycorrhizal mycelial networks. New Phytologist.
- Johnson, D., Leake, J.R., Read, D.J. (2002). Transfer of recent photosynthate into mycorrhizal mycelium of an upland grassland. Soil Biology and Biochemistry.
- Sourhope Field Data Handbook (2003). Supporting information.
- Usher, M.B., Sier, A.R., et al. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology.