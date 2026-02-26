# Kākāpō Egg Fertility 2019: Documentation

## Purpose and scope
- Documents origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season.
- Part of the Kākāpō Recovery Programme’s conservation management activities; aims to distinguish fertilisation failure from early embryo death to inform effective conservation decisions.
- Funded by a Natural Environment Research Council Urgency Grant.

## Study population and setting
- Species: kākāpō (Strigops habroptilus); critically endangered.
- Management: on predator-free offshore islands; breeding population around 110 individuals.
- Islands involved: Whenua Hou / Codfish Island and Anchor Island.
- Monitoring and management: nests monitored, eggs replaced with decoys, eggs artificially incubated, and chicks returned to nests.
- Notable breeding context: large season with 252 eggs laid; twelve females were artificially inseminated; data linked to ongoing reproductive histories.

## Data collected and structure
- Two linked CSV datasets:
  - File 1: kakapo_egg_fertility_2019-1_all_eggs (252 eggs, 10 columns)
    - Key fields include: egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI
  - File 2: kakapo_egg_fertility_2019-2_undeveloped_eggs (129 undeveloped eggs, 15 columns)
    - Key fields include: egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
- egg_id is the unique identifier and linking key between the two files.
- Data cover all eggs laid during the season, plus detailed analyses for undeveloped eggs transported to Sheffield.

## Methods and analyses
- Field collection: daily candling; undeveloped eggs removed if no embryo visible after 5 days; yolks preserved in 5% formalin.
- Laboratory analysis (University of Sheffield): yolk extraction, PVL examination for sperm and embryonic cells using Hoechst 33342 stain; fluorescence microscopy to determine fertilization status and early embryo mortality; counts of PVL sperm.
- Measurements recorded for undeveloped eggs: egg size (length, width), weights (preserve, fresh, albumen, yolk, shell), and PVL metrics (PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm).

## Data governance and provenance
- Detailed metadata accompany both datasets; data types are clearly defined (binary, integer, numeric, string).
- Datasets are designed for merging via egg_id to enable integrated analyses of fertility status and physical/biometric attributes.
- Additional data exist within the New Zealand Department of Conservation Kākāpō Recovery Programme, including broader population data, management practices for 2018/19 and other seasons, and reproductive histories.

## Roles and responsibilities
- Nicola Hemmings (University of Sheffield): Principal Investigator; oversaw analysis of undeveloped eggs and project administration.
- James Savage (University of Sheffield): Researcher Co-Investigator; oversaw sampling logistics and data management.
- Jodie Crane (Kākāpō Recovery, NZDOC): Senior Ranger; conducted egg sampling and data collection; liaison among teams.
- Kākāpō Recovery Team: broader field support and management, including operations, technical, scientific, and logistical roles.

## Relevance for monitoring frameworks
- Provides a concrete example of structured environmental health monitoring within a conservation program.
- Demonstrates the integration of field data, laboratory analyses, and biometric measurements to derive fertilisation outcomes.
- Illustrates data governance practices (metadata, data sharing considerations, cross-institution collaboration) and the importance of clear linking keys for multi-file datasets.
- Supports decision-making for management actions (e.g., artificial insemination, mating strategies) by distinguishing causes of hatching failure.
- Highlights potential data-collection challenges and sensitivities (e.g., shipping samples, formalin preservation, data sharing barriers) relevant to monitoring frameworks.