# Kākāpō Egg Fertility 2019: Documentation

## Overview
- Dataset on origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season.
- Eggs were laid in natural nests and artificially incubated as part of the Kākāpō Recovery Programme.
- Total eggs: 252; 129 failed to develop.
- Yolk from undeveloped eggs preserved in formalin and transported to the University of Sheffield, UK.
- At Sheffield, yolks were dissected and inspected via fluorescence microscopy to determine if eggs were unfertilised or fertilised but died very early.
- Sperm counts were recorded on the perivitelline layer (PVL).

## Project context and rationale
- The kākāpō is critically endangered with high hatching failure; undeveloped eggs can be due to male infertility or fertilisation failure followed by embryo death.
- Objective: distinguish between fertilisation failure and embryo death to inform conservation management.
- Funding: Natural Environment Research Council Urgency Grant NE/T00200X/1.

## People & roles
- Dr Nicola Hemmings (University of Sheffield): Principal Investigator; analyzed undeveloped eggs and managed project administration.
- Dr James Savage (University of Sheffield): Researcher Co-Investigator; oversaw sampling/transport and data management.
- Dr Jodie Crane (Kākāpō Recovery, NZ DOC): Senior Ranger; conducted egg sampling and data collection on egg sizes and weights; liaison between teams.
- Kākāpō Recovery Team (NZ DOC): Monitors breeding, nests, and incubation; multiple team members contributed (names listed).

## Study population
- Managed population on predator-free offshore islands: Whenua Hou / Codfish Island and Anchor Island.
- Breeding population around 110 individuals.
- Reproduction details: nests monitored; eggs incubated with decoys; chicks returned after hatching; 12 females artificially inseminated during season.
- Large breeding event: 252 eggs laid in 2018/19, first egg on 25 December; record food abundance.

## Sample collection & analysis
- Eggs candled daily during artificial incubation; undeveloped eggs removed after no embryo after 5 days.
- yolks from undeveloped eggs preserved in 5% formalin and shipped to Sheffield (CITES GB041).
- In Sheffield: yolks removed from formalin, washed, and examined for germinal disc and PVL sperm using Hoechst 33342 staining and fluorescence microscopy; PVL sperm counted.
- Data collected on undeveloped eggs: fertilisation status, PVL sperm, PVL holes, PVL area, and related observations.

## Dataset structure and contents
- Dataset comprises two CSV files:
  - File 1: kakapo_egg_fertility_2019-1_all_eggs
    - 252 rows, 10 columns
    - Key fields: egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI
    - Describes all eggs laid in the season
  - File 2: kakapo_egg_fertility_2019-2_undeveloped_eggs
    - 129 rows, 15 columns
    - Key fields: egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
    - Details for undeveloped eggs transported to Sheffield; allows merging with File 1 via egg_id
- Data merging: egg_id is the common key to link the two files if combining datasets.

## Data quality, scope, and notes
- Samples obtained from 128 undeveloped eggs; these represent 98% of undeveloped eggs during the season (note slight discrepancy with 129 undeveloped eggs in File 2).
- Additional data exist within the NZ Department of Conservation Kākāpō Recovery Programme on broader population, management methods, and reproductive histories.
- Dataset age: tied to the 2018/19 breeding season; aims to support conservation decision-making by elucidating causes of hatching failure.