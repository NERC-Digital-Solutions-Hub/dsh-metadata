# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme]

## Aim and context
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biodiversity and the functional roles of soil organisms.
- Field site: Sourhope, Kelso, Scotland; upland grassland turf with 24 higher plant species (21 AM-mycorrhizas) in a no-fertilizer regime for ≥40 years.
- 24 related projects studied soil structure, carbon/nitrogen cycles, and soil biota across micro-, meso-, and macro-fauna.

## Dataset scope
- Measurements of carbon-14 transfer from plants to soil within nylon mesh cores, traced through roots, shoots, soil, and respiration.
- Mesh cores (static or rotated) used to create plus/minus mycorrhizal mycelium conditions and to assess mycorrhizal networks’ role in carbon and nutrient cycling.
- Data output associated with Project 2117: “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”
- Dataset reference: 1079 14C transfer 1.0 (P2117_14C_TRANSFER_1.csv).

## Methods and experimental design
- Site: turf from upland grassland at Sourhope (NGR: NT 854196); community dominated by species with substantial AM colonization.
- Core system: nylon mesh-bound cores (35 μm pore, 22 mm diameter, 120 mm deep) inserted into intact turf to regulate AM hyphae ingress while excluding roots.
- Procedure:
  - 16 cores per pot, 8 turfs; two cores per pot rotated vs static to distinguish mycelial connectivity.
  - Cores filled with field soil; turfs maintained in a controlled environment (approx. 20°C day/15°C night).
  - 14CO2 labelling: 1 MBq of 14CO2 delivered for 3 hours in a gas-tight box; lactic acid enhanced bicarbonate solution used with 14C.
  - Post-labelling sampling at 6, 20, 28, 42, 51, and 70 hours.
  - Measurements: plant tissue combusted and analysed by liquid scintillation counting; CO2 fluxes trapped with 1 M NaOH in headspace; final biomass, soil, and root samples dried and 14C content determined.
- Data handling:
  - Total 14C in shoots, soil, roots, and respired CO2 quantified; allocation to mycelium inferred by comparing static vs rotated cores.
  - Final biomass and core volume adjustments applied to 14C calculations.

## Data schema and content
- Dataset: 1079 14C transfer 1.0 (CSV)
- Key fields:
  - SAMPLEID, SAMPLE_TYPE (Pot, Rotated core, Static core), SAMPLE_DATE
  - HOURS_POST_LABELLING (time since labelling)
  - SHOOT_14C (nmol 14C g shoot dwt-1)
  - RESP_14C (pmol 14CO2 h-1 cm-2)
  - SOIL_14C (nmol 14C g soil dwt-1)
  - ROOT_14C (nmol 14C g root dwt-1)
- Notes:
  - Sample types distinguish measurement context (whole pots, cores with/without mycelium connections).
  - Data collected August 2000; analyses used combustion and scintillation counting.

## Key findings and interpretation
- Shoot 14C concentration declined markedly over 70 hours: about 83% loss from shoots (62 to 10 nmol g plant dwt-1).
- Allocation of 14C into AM mycelium estimated by comparing static vs rotated cores, enabling inference of carbon transfer pathways via mycorrhizal networks.
- Overall results illuminate short-term carbon partitioning between plant shoots, soil, and mycorrhizal networks under controlled AM conditions.

## Quality control and limitations
- Quality control included numeric range checks, data formatting conformity, and logical integrity checks.
- While QA procedures were applied, NERC cannot warrant data accuracy or fitness for a specific use; no liability for data use or results.
- Data are tightly scoped to a specific mesocosm experiment with particular mesh-core design and short-term labelling, which may limit broader generalizability without further context.

## References and data access
- Foundational references:
  - Johnson, Leake, Read (2001) on in-growth core system for mycorrhizal networks.
  - Johnson, Leake, Read (2002) on transfer of recent photosynthate into mycorrhizal mycelium.
  - Sourhope Field Data Handbook (2003); UK Soil Biodiversity Programme overview (2006).
- Data provenance: Sourhope field site, NERC Soil Biodiversity Programme; dataset available as 1079 14C TRANSFER 1.0 (P2117_14C_TRANSFER_1.csv) with detailed metadata.
- Project context: Project 2117, “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”