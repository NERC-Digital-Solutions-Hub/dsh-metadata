# Life history and experimental provisioning data for banded mongooses in Queen Elizabeth National Park, Uganda (2017-2020)

## Overview
- Data describe life history, biometric measurements, reproductive status, and environmental context for banded mongooses, including an experimental provisioning component.
- Study site: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E); data collected from 2017 to 2020 (May 2017–March 2020 for the experiment).
- Primary purpose: measure fitness and life history trade-offs and potential trans-generational effects.

## Data collected and domain coverage
- Life history events at the individual level (birth, death, migration, pregnancy, etc.) and at the group level (inter-group interactions, synchronous births).
- Daily body mass and a suite of biometric data (weights, body measurements, head/tail dimensions, etc.) collected in the field.
- Biometric sampling during trapping (blood, DNA via tail tissue, transponder implantation).
- Reproductive status data (pregnancy, oestrus, non-breeding, pack-escort, pack-babysitting) with foetus information when applicable.
- Weather context from a field weather station (daily precipitation, min/max temperatures).
- Experimental provisioning data: a subset of females assigned to provisioned (P) or control (C) groups to assess effects on fitness.

## Experimental design
- Six age- and weight-matched female groups randomly assigned to provisioned (P) or control (C) at the start of the experiment.
- Provisioned females received one egg omelette three times a week; each provisioned female had an age-matched control within the same group.
- Replacement of deceased provisioned or control individuals as needed.
- Sample sizes: 18 provisioned females and 15 controls; total experimental period ~561 days (min 165 days, max 1053 days).
- Reproductive output: 71 litters born across the experiment, average 6.7 litters per female (range 2–15).

## Data structure and schema (Tables)
- Table 1. Captures
  - Key fields: CAPTURE_DATE, INDIV, TRANSPONDER, PACK, PACK_STATUS, AGE (ADULT/INF/M/PUP/SUBADULT), Examiner, DRUGS, SEX (M/F), REPRO_STATUS (PREG/OES/NONB/PE), LACTATING, ULTRASOUND, FOETUSES, FOET_SIZE, MILK_SAMPLE_MK, WEIGHT, HEAD_WIDTH, HEAD_LENGTH, BODY_LENGTH, HINDFOOT_LENGTH, TAIL_LENGTH, TAIL_CIRC, TICKS, PLASMA_SAMPLE_PL, BLOOD_SAMPLE_BL, WBC, RBC, WSK, etc.
- Table 2. Experimental females
  - Fields: PACK, ID, TREATMENT_GROUP (C or P), DATE_STARTED, COMMENT.
- Table 3. Experimental males
  - Fields: PACK, ID, STATUS (BREEDING/NON BREEDING), DATE_STARTED, DATE_STOPPED, COMMENT.
- Table 4. Life history
  - Fields: DATE, PACK, INDIV, SEX, AGE CAT (AD/INF/PUP/SUB), STATUS (AD/DEP/MULTI/PRIMIP), START_END (START/END/RESTART/STOP), CODE (23 life-history codes, e.g., BORN, BIRTH, DIED, EM/EMERGE, IGI, FPREG, SOES, etc.), EXACT (Y/N), LSEEN (Date last seen), CAUSE (Death cause), LITTER (Litter ID).
- Table 5. Weather
  - Fields: DATE, RAIN_MWEY A, MAX_TEMP, MIN_TEMP, OBSERVER.
- Table 6. Weights
  - Fields: PACK, DATE, INDIV, SEX (M/F), WEIGHT, ACCURACY.

## Data quality and completeness
- Some capture and weight data may be missing due to occasional escape from traps or weighing events.
- Data are collected under a structured protocol to distinguish death from dispersal (critical for life-history analyses).

## Personnel and governance
- Principal Investigator: Jonathan D. Blount (University of Exeter).
- Co-Investigator: Michael A. Cant (University of Exeter).
- Postdoctoral researchers involved in collection and analysis: Magali Meniri, Faye J. Thompson, Harry H. Marshall.

## How the data can be used
- Analyze fitness and life-history trade-offs in wild mongooses.
- Explore trans-generational effects and provisioning impacts on survival, reproduction, and group dynamics.
- Build dashboards or self-serve analyses for end users by combining life-history events, biometric data, and environmental context.
- Promote data reuse and sharing to maximize value and insights across related studies.