# Kākāpō Egg Fertility 2019: Documentation

- What this dataset covers
  - Information on origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season.
  - Eggs were laid in natural nests, then artificially incubated as part of the Kākāpō Recovery Programme.
  - Yolk samples from undeveloped eggs were preserved, shipped to the University of Sheffield, and examined with fluorescence microscopy to determine fertilization status and count sperm on the perivitelline layer (PVL).

- Project purpose and funding
  - Aims to distinguish between fertilisation failure and early embryo death to inform conservation management.
  - Motivated by high hatching failure in this critically endangered species; funded by Natural Environment Research Council Urgency Grant NE/T00200X/1.

- Population context
  - The kākāpō population on predator-free offshore islands (Anchor Island and Whenua Hou/Codfish Island) is managed by the NZ Department of Conservation.
  - The season featured record breeding activity (252 eggs); 12 females were artificially inseminated.
  - Mating patterns and reproductive management are tracked by the Kākāpō Recovery Team.

- Roles and data collection process
  - Key personnel: Nicola Hemmings (PI, University of Sheffield), James Savage (Researcher Co-Investigator, University of Sheffield), Jodie Crane (Senior Ranger, NZ DOC), and the Kākāpō Recovery Team.
  - Eggs were candled daily during artificial incubation; undeveloped eggs were opened, yolks preserved in formalin, and samples sent to Sheffield.
  - In Sheffield, yolks were examined for embryonic cells and PVL sperm using fluorescence microscopy; PVL sperm counts were recorded.
  - Data management and coordination involved the University of Sheffield teams and the Kākāpō Recovery Programme.

- Study population details
  - Breeding population of about 110 kākāpō on Anchor Island and Whenua Hou.
  - Nests monitored; artificial incubation used; chicks returned to nests after hatching.
  - Reproductive timing linked to food abundance; 12 females were artificially inseminated during the season.

- Sample collection and analysis workflow
  - Eggs candled daily; undeveloped eggs removed after no embryo visible for 5 days.
  - 128 undeveloped eggs yielded samples for analysis (representing 98% of undeveloped eggs laid).
  - Preserved yolks shipped to University of Sheffield (CITES GB041).
  - In Sheffield, yolks processed for fertilization status (fertilized or not; embryonic development) and PVL sperm analysis.

- Dataset structure and contents
  - Two CSV files:
    - kakapo_egg_fertility_2019-1_all_eggs: 252 rows, 10 columns
      - egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI
    - kakapo_egg_fertility_2019-2_undeveloped_eggs: 129 rows, 15 columns
      - egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
  - The egg_id field is the key for merging the two datasets.
  - File 1 provides per-egg fertility and study-relevant attributes; File 2 provides detailed measurements and PVL observations for undeveloped eggs.

- What the data enable
  - Determine fertilization status across all eggs and compare with development outcomes.
  - Analyze relationships between egg morphology/weights and fertilization outcomes.
  - Assess PVL sperm counts as a potential indicator of fertilization likelihood.
  - Combine with broader population and management data (available from NZ DOC) for larger-scale conservation insights.

- Additional notes
  - NZ Department of Conservation holds broader data on the kākāpō population, management practices, and reproductive histories relevant to these eggs.
  - The dataset includes some fields with binary outcomes and some with continuous measurements (e.g., PVL area, various weights).
  - Data collection involved formalin preservation and international shipment, with local field monitoring and laboratory analysis coordinating to build the full picture.