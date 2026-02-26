# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999) studying soil biota diversity and ecosystem processes at Sourhope field site, Scottish Borders.
- Focus: measurements of carbon-14 transfer from plants to soil within nylon mesh-bound cores, tracking 14CO2 through shoots, roots, soil, and respiration.
- Experimental design includes static versus rotated cores to compare mycorrhizal mycelial networks and their effect on carbon transfer.
- Dataset associated with Project 2117: “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”

## Data content
- Dataset: 1079 14C_TRANSFER_1.0.csv
- Describes measurements of carbon-14 transfer from plants to soil within mesh cores, with additional tracing of 14CO2 via respiration.
- Sample types: Pot (1–7), Rotated core (1–7), Static core (1–7).
- Time points: 6, 20, 28, 42, 51, and 70 hours post-labelling.
- Measured variables include:
  - SHOOT_14C: 14C in plant shoots (nmol 14C g shoot dwt-1)
  - RESP_14C: 14CO2 released from cores (pmol 14CO2 h-1 cm-2)
  - SOIL_14C: 14C in soil (nmol 14C g soil dwt-1)
  - ROOT_14C: 14C in soil from roots (nmol 14C g root dwt-1)
- Data were collected in August 2000; sampling and labelling used 14CO2 with detailed methods described below.

## Methods and procedures
- Site: upland grassland turf at Sourhope (NGR NT 854196); community with extensive AM-mycorrhizas; no fertilizer for ~40 years.
- Core system: nylon mesh-bound cores (pore size 35 μm) inserted into intact turf to control mycorrhizal colonization while allowing hyphae, bacteria, solutes, and water movement.
- Labelling: 1 MBq 14CO2 exposure for 3 hours in a gas-tight box, using lactic acid to generate labelled CO2; headspace CO2 captured with NaOH traps at multiple time points (0–70 h).
- Post-labelling processing: vegetation subsamples dried and analysed for 14C; cores and soils similarly processed; 14C quantified by combustion and liquid scintillation counting.
- Calculations: allocation of 14C to AM mycelium estimated by comparing static vs rotated cores; final data include biomass, soil, and root compartments.
- Quality checks: numeric range checks, formatting conformity, and logical integrity checks described as part of QA.

## Data structure and documentation
- Data file fields (example): SAMPLEID, SAMPLE_TYPE (Pot, Rotated core, Static core), SAMPLE_DATE, HOURS_POST_LABELLING, SHOOT_14C, RESP_14C, SOIL_14C, ROOT_14C.
- Data types and units provided for each field; some fields use -999 as missing value indicators.
- References and further reading list core methodological papers and the Sourhope Field Data Handbook (2003).

## Quality and governance
- QA steps include numeric range checks, format conformity, and logical integrity checks.
- Limitations and liability: NERC asserts no warranty on data accuracy or fitness for a particular use; no liability for loss, damage, or injury from data use.
- Provenance and documentation are provided (method descriptions, project context, and bulk referencing).
- Data sharing context: references indicate availability via related catalog records (e.g., EIDC/Sourhope field data resources).

## Relevance for data stewards
- Metadata completeness: dataset includes a clear study context, site description, methodology, variables, units, time points, and data dictionary for the primary CSV.
- Data standards: consistent labeling of sample types, time post-labelling, and measurement types; explicit units for each variable; explicit missing value indicator (-999).
- Provenance and references: linked to primary publications and field data handbooks; supports traceability and re-use.
- Access and reuse: data described with method transparency and QA, but with explicit liability disclaimer; availability noted through catalog records and project references.
- Governance considerations: potential updates or corrections should align with the initial QA practices and provenance notes; ensure ongoing interoperability with related datasets (e.g., similar AM-mycorrhizal transfer studies).