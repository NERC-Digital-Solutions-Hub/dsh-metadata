# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

## Overview
- Datasets from the NERC Soil Biodiversity Thematic Programme (1999 onward) focusing on carbon-14 transfer from plants to soil within mesh-bound cores.
- Aimed to understand the role of mycorrhizal mycelium in carbon and nutrient cycling, using turf from an upland Scottish field site (Sourhope, Kelso, Scotland).
- Experimental design contrasts static vs rotated cores to manipulate access by mycorrhizal networks and roots.
- Measurements tracked carbon-14 through plant tissues, soil, and respiration over a 70-hour post-labelling period.

## Dataset description
- Dataset created from Project 2117: The effect of mycorrhizal mycelium on soil microbial communities and its role in carbon and nutrient cycles. Project Leader: Dr J. Leake.
- Data collected at Sourhope field site (NGR: NT 854196) using mesh-core systems in grassland turfs.
- Data files recorded in August 2000; primary dataset available as 1079 14C_TRANSFER_1.csv.
- Data quality assurance included numeric range checks, formatting checks, and logical integrity checks. However, data are provided without warranty of accuracy or fitness for a specific use; no liability accepted by NERC.

## Materials & Methods (data collection context)
- Site: Upland grassland turf with a mix of species, many forming AM-arbuscular mycorrhizas; no recent fertilizer application.
- Core system: Nylon mesh-bound cores (35 μm pore size) inserted into turf to control AM hyphae colonization while excluding roots.
- Experimental setup: 16 cores across 8 turfs; each core in a 10 cm × 10 cm × 15 cm turf, with six root-containing turfs and two root-free cores per turf.
- Treatments: Static cores vs rotated cores to alter hyphal connectivity with host plants.
- Isotope tracing: 14CO2 labelling (1 MBq) for 3 hours in a gas-tight box; lactic acid aided release of labelled CO2 into the headspace.
- Sampling schedule: timepoints at 6, 20, 28, 42, 51, and 70 hours post-labelling; vegetation subsamples dried and analysed for 14C; NaOH traps for CO2 flux measurements; final harvesting of plant material, soil, and cores for 14C analysis.
- Measurements: 14C in plant shoots, soil, roots; 14CO2 evolved from cores; 14C allocation to AM mycelium estimated by comparing static and rotated cores.
- Outcome metrics: concentration of 14C in shoots, soil, roots; total 14C recovered in plant and soil fractions; rate of 14CO2 evolution.

## Data file and structure
- Dataset: 1079 14C_TRANSFER_1.csv
- Key variables (sample and measurement context):
  - SAMPLEID: Unique sample identifier
  - SAMPLE_TYPE: Pot (no. 1-7, whole pot), Rotated core (no. 1-7), Static core (no. 1-7)
  - SAMPLE_DATE: Date of sampling
  - HOURS_POST_LABELING: Hours after labelling
  - SHOOT_14C: 14C in plant shoots (nmol 14C g shoot dry weight^-1)
  - RESP_14C: 14CO2 released from cores (pmol 14C per hour per cm^2)
  - SOIL_14C: 14C concentration in soil (nmol 14C g soil dry weight^-1)
  - ROOT_14C: 14C concentration in roots (nmol 14C g root dry weight^-1)
- Analysis and processing notes:
  - Samples were oven-dried, combusted, and counted via liquid scintillation counting.
  - Residual 14C in soil adjusted for core volume differences; allocation to AM mycelium inferred by comparing rotated vs static cores.
- Additional dataset context:
  - Other outputs include total above-ground biomass, mesh-core residuals, and detailed methodological descriptions in related publications and field data handbooks.

## Context and interpretation
- Purpose of the data: to quantify carbon flow from plant sources into soil and microbial networks, and to understand how mycorrhizal associations influence carbon allocation and soil microbial functioning.
- Data products enabled by the dataset: values suitable for dashboards or tables illustrating temporal dynamics of 14C transfer, comparisons between core treatments, and estimation of mycelial-mediated carbon transfer.
- Potential caveats:
  - Quality checks performed, but data disclaimer from NERC states no guarantee of accuracy or fitness for a particular use.
  - Experimental design relies on core rotation to infer mycelial connections; interpretation assumes consistent core behaviour across turfs.

## References & Further Reading
- Johnson, D., Leake, J.R., Read, D.J. (2001). Novel in-growth core system enables functional studies of grassland mycorrhizal mycelial networks. New Phytologist 152, 555-562.
- Johnson, D., Leake, J. R., & Read, D. J. (2002). Transfer of recent photosynthate into mycorrhizal mycelium of an upland grassland: short-term respiratory losses and accumulation of 14C. Soil Biology and Biochemistry, 34(10), 1521-1524.
- SOURHOPE FIELD DATA HANDBOOK 2003. Usher et al.
- Usher, M. B., Sier, A. R., Hornung, M., & Millard, P. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.