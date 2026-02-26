# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

## Overview
- Describes a component of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biodiversity, carbon and nitrogen cycles, and the functional roles of soil organisms.
- Location: Sourhope field site, Scottish Borders; long-term turf grassland experiments with 24 related projects.
- Core aim: understand how carbon is transferred within soil–plant–microbial systems, particularly via mycorrhizal networks, using mesh-core systems and 14C tracing.
- Dataset role: provides measurements of 14C transfer from plants to soil within mesh cores, including comparisons between static cores and cores with disrupted hyphal networks, plus CO2 respiration measurements.

## Dataset and Study Details
- Dataset: 1079 14C transfer 1.0 (P2117_14C_TRANSFER_1.csv); analyses conducted in August 2000.
- Key purpose: quantify the fate of recently photosynthesized carbon in grassland soil and its partitioning among plant shoots, soil, roots, and mycorrhizal networks.
- Experimental design: mesh-bound cores inserted into upland grassland turfs; cores either static (allow AM fungal hyphae to persist) or rotated to disconnect hyphae from host plants; 14CO2 used to label system and trace carbon flow.

## Materials & Methods (experimental design in detail)
- Site and vegetation: upland turf at Sourhope field site; grassland community dominated by species with high AM mycorrhizal association.
- Mesh-core system: nylon mesh cores (35 μm pore size) within turfs; cores (22 mm diameter, 120 mm deep) inserted into 8 turfs (10 cm × 10 cm × 15 cm each).
- Mycorrhizal control: rotation of one core per pot to break hyphal connections; comparison between rotated (disconnected) and static (connected) cores.
- Labeling and incubation: exposure to 14CO2 for 3 hours in a gas-tight box; headspace CO2 captured with NaOH traps; labelled period followed by sampling at multiple time points (6, 20, 28, 42, 51, 70 hours post-labelling).
- Measurements: plant tissue and soil samples dried and combusted; 14C quantified by liquid scintillation counting; respiration measured via 14CO2 trapped in NaOH; data corrected for core volume differences.
- Allocation estimates: 14C allocation to AM mycelium inferred by comparing static vs rotated cores.
- Results highlights: initial shoot 14C concentrations ranged 103–245 nmol 14C per pot; after 70 hours, shoot 14C declined by ~83% (to ~10 nmol g dry weight); overall decay followed a strong logarithmic pattern.

## Dataset Structure
- Dataset: 1079 14C_TRANSFER_1.csv
- Variables include:
  - SAMPLEID: unique sample identifier
  - SAMPLE_TYPE: Pot, Rotated core, Static core
  - SAMPLE_DATE: date of sampling
  - HOURS_POST_LABELLING: hours after labelling
  - SHOOT_14C: 14C in shoots (nmol 14C g shoot dwt-1)
  - RESP_14C: 14CO2 evolved from cores (pmol 14CO2 h-1 cm-2)
  - SOIL_14C: 14C in soil (nmol 14C g soil dwt-1)
  - ROOT_14C: 14C in root-associated soil (nmol 14C g root dwt-1)
- Notes on data types and units provided in the metadata; analyses conducted on samples collected in August 2000.

## References & Further Reading
- Johnson, D., Leake, J.R., Read, D.J. (2001). Novel in-growth core system enables functional studies of grassland mycorrhizal mycelial networks. New Phytologist 152, 555-562.
- Johnson, D., Leake, J.R., & Read, D.J. (2002). Transfer of recent photosynthate into mycorrhizal mycelium of an upland grassland: short-term respiratory losses and accumulation of 14C. Soil Biology and Biochemistry, 34(10), 1521-1524.
- Scott, R. et al. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Available via EIDC.
- Usher, M.B. et al. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.

## Quality Control and Data Governance
- Quality control: numeric range checks, formatting conformity, and logical integrity checks implemented.
- Assurance disclaimer: while data are subject to QA procedures, NERC cannot warrant the accuracy or fitness of the data for any particular use; no liability for losses or damages arising from use of the data.
- Governance implications: emphasizes the need for clear metadata, transparency about limitations, and explicit disclaimers regarding data accuracy and liability—key considerations for monitoring frameworks implementing open data and data-sharing policies.

## Relevance for Monitoring Framework Authors
- Illustrates a rigorous, field-based data collection approach linking experimental manipulation (static vs rotated cores) with biochemical tracing (14C) to understand carbon flow and ecosystem function.
- Demonstrates the importance of detailed metadata and clear data structure to support reuse in policy monitoring and decision-making.
- Highlights data governance practices, including quality control steps and explicit liability disclaimers, critical for open-data-enabled monitoring frameworks.
- Shows how complex ecological processes (mycorrhizal networks, carbon allocation) can be operationalized into measurable indicators suitable for policy scrutiny and future decision-making.
- Underlines challenges relevant to monitoring authorities, such as ensuring sufficient metadata, data accessibility, and managing dataset provenance across long-term ecological programmes.