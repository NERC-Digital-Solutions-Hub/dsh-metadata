# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) conducted at Sourhope, Kelso, Scotland, to study soil biota diversity and functional roles in ecological processes.
- The programme funded 24 projects covering soil structure, carbon and nitrogen cycles, microfauna, meso-fauna, and macro-fauna.

## Experimental Setup and Location
- Location: upland grassland turf at Sourhope field site (NGR: NT 854196); grassland characterized by Festuca-Agrostis-Galium with AM-mycorrhizas.
- Core system: nylon mesh-bound cores (22 mm diameter, 120 mm deep) with 35 m m pore size to control mycorrhizal hyphae access while allowing bacteria, solutes, and water exchange.
- Experimental design: 16 cores inserted into 8 intact 10 cm x 10 cm x 15 cm deep turfs; turfs dominated by Agrostis capillaris, Anthoxanthum odoratum, Festuca rubra, Poa pratensis.
- Treatments: static cores vs rotated cores to create plus/minus mycorrhizal mycelial networks; rotation breaks hyphal connections.
- Growth conditions: growth room at 20°C (18 h day) / 15°C (6 h night), maintained for 10 weeks.

## Methods and Measurements
- Labeling: turfs exposed to 1 MBq of 14CO2 for 3 hours in a gas-tight box; 14CO2 introduced via 14C sodium bicarbonate with lactic acid to generate labelled CO2.
- Trapping and sampling: headspace CO2 captured with 1 ml of 1 M NaOH in Eppendorf tubes; traps replaced at 6, 20, 28, 42, 51, and 70 hours post-labelling.
- Tissue and soil sampling: post-labelling, subsamples of vegetation were dried and analysed for 14C; final sampling included total above-ground biomass, bulk soil, fine roots, and mesh cores.
- Analysis: 14C content determined by combustion and liquid scintillation counting (Packard 307 Oxidiser; Packard Tricarb 1600 TR).
- Data interpretation: 14C allocation to AM mycelium estimated by comparing static vs rotated cores; 14C in shoots tracked from 103–245 nmol 14C per pot immediately after labelling; 14C in shoots declined ~83% over 70 hours, following a logarithmic trend.
- References for methodology: Johnson et al. (2001, 2002); related field data handbook (2003); Usher et al. (2006).

## Dataset Details
- Dataset: 1079 14C_TRANSFER_1.0 (CSV)
- Content: Measurements of carbon-14 transfer from plants to soil within mesh cores; includes static and rotated cores to differentiate mycelial influence; 14C traced in plant shoots, soil, roots, and respiration.
- Sample schema (examples of fields):
  - SAMPLEID: Unique sample identifier
  - SAMPLE_TYPE: Pot, Rotated core, Static core
  - SAMPLE_DATE: Date of sampling
  - HOURS_POST_LABELLING: Hours after labelling
  - SHOOT_14C: 14C concentration in plant shoots (nmol 14C g shoot dwt-1)
  - RESP_14C: 14CO2 respiration from cores (pmol 14 CO2 h-1 cm-2)
  - SOIL_14C: 14C concentration in soil (nmol 14C g soil dwt-1)
  - ROOT_14C: 14C concentration in roots (nmol 14C g root dwt-1)
- Analytical context: Analyses conducted August 2000; measurements performed using standard 14C protocols; data support understanding carbon allocation between plants, mycorrhizal networks, and soil.
- Documentation: Related datasets and methodological references provided (see references below).

## Quality Assurance and Limitations
- Quality control: numeric range checks, formatting checks, and logical integrity checks applied to data.
- Limitations and liability: NERC acknowledges data are subject to QA but cannot warrant accuracy or fitness for a specific use; no liability for losses or damages arising from use of the data.
- Data provenance and context: dataset described with detailed Materials & Methods and site context to support reproducibility and re-use.

## Access, Usage, and References
- Data originate from Project 2117: The effect of mycorrhizal mycelium on soil microbial communities and its role in carbon/nutrient cycles.
- Primary references:
  - Johnson, D., Leake, J.R., Read, D.J. (2001). Novel in-growth core system enables functional studies of grassland mycorrhizal mycelial networks. New Phytologist.
  - Johnson, D., Leake, J.R., Read, D.J. (2002). Transfer of recent photosynthate into mycorrhizal mycelium of an upland grassland: short-term respiratory losses and accumulation of 14C. Soil Biology and Biochemistry.
  - Sourhope Field Data Handbook (2003).
  - Usher, M.B., et al. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology.
- Data accessibility: Dataset includes a structured data dictionary for 14C_TRANSFER_1.csv and associated methods; QA steps described to support reuse and cross-study comparability.