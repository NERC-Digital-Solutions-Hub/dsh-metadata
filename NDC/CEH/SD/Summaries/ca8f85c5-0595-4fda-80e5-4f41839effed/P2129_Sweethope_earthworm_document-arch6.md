# Earthworm diversity and the integration of physical, biochemical and microbiological functions.

- Overview
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biodiversity, carbon and nitrogen cycles, and interactions between earthworms, microbes, and soil structure.
  - Study site: Sweethope mesocosms (end of the Sweethope site) linked to the Sourhope main plots in Scotland; final sampling in October 2001.
  - Data describe earthworm abundance/biomass and botanical composition from controlled inoculation experiments (epigeic, endogeic, andecic earthworms) and lime treatment, mirroring the main Sourhope plots but in an animal-proof enclosure to prevent cross-contamination.

- Study design and field methodology
  - Site details: Sourhope upland grassland with Brown Forest Soils, fenced since 1998; soil moved to a separate enclosure (“Sweethope”) about 100 m away for the experiment.
  - Experimental setup: 100 soil boxes relocated; half hand-sorted to remove earthworms; inoculations included: no inoculation, single species (epigeic, endogeic, or anecic), and all three together (ABC); lime treatment also applied to set of boxes.
  - Inoculation species used to represent ecological groups: Lumbricus rubellus (epigeic), Allolobophora chlorotica (endogeic), Lumbricus terrestris (anecic); inocula per box: 20, 15, and 4 individuals respectively.
  - Box and sampling design: 5 rows with replicated blocks; boxes were earthworm-proofed with fine mesh lids; grass cutting and lime application performed to maintain treatments.
  - Sampling period: final census of earthworm communities and plant composition conducted in October 2001.

- Data files and structure (datasets)
  - Dataset 1009: Sweethope Endpoint Botanical Composition Data (2129_BOTANICAL_COMPOSITION.csv)
    - Purpose: Botanical composition for each experimental treatment at the Sweethope endpoint (Oct 16–17, 2001).
    - Key fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), SPECIES, BOTANICAL_COMPOSITION (Braun-Blanquet scale 0–6).
  - Dataset 1010: Sweethope Endpoint Earthworm Survey Data (P2129_EARTHWORM_SURVEY.csv)
    - Purpose: Earthworm census data at Sweethope endpoint (Oct 16–17, 2001) including abundance and biomass per species.
    - Key fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), SPECIES, ABUNDANCE (per m2), BIOMASS (per m2).

- Data content and measurement details
  - Earthworms: hand-sorted specimens identified to species (Sims & Gerard, 1985); abundance and biomass calculated per m2; specimens preserved in 40% ethanol prior to identification.
  - Botanical data: presence and abundance of plant species recorded using Braun-Blanquet scale (0 = not present to 6 = 76–100% cover).
  - Data granularity: per sub-plot within each main plot and block; measurements tied to specific grid cells (CELL_X, CELL_Y).

- Data quality and usage notes
  - Quality control: numeric range checks, data format conformity, and logical integrity checks implemented.
  - Limitations and disclaimers: while subjected to QA procedures, data accuracy for end-users cannot be guaranteed by NERC; no liability for misuse or inaccuracies.
  - Accessibility and references: data are provided as Supporting Information; associated with the EIDC catalogue and linked to the SOURHOPE FIELD DATA HANDBOOK (2003); related publications and theses noted (e.g., liming effects on earthworms, soil carbon characteristics).

- References and further reading
  - Bishop, Grieve, Chudek & Hopkins (2008). Liming upland grassland: effects on earthworm communities and soil carbon casts.
  - Scott et al. (2003). SOURHOPE FIELD DATA HANDBOOK.
  - Sims & Gerard (1985). Earthworms: keys and notes for identification.
  - Spring (2003). The effects of earthworms on soil structure in upland grassland (PhD thesis).
  - Usher et al. (2006). Understanding biodiversity in soil: UK Soil Biodiversity Programme.

- Practical notes for data use
  - Data enable self-service exploration of how lime treatment and earthworm functional groups affect earthworm communities and plant composition within a controlled mesocosm experiment.
  - Two complementary datasets allow linking belowground biota (earthworms) with aboveground plant responses across treatments, blocks, and spatial cells.