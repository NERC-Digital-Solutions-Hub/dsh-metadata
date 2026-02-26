# Data description for banded mongooses study in Queen Elizabeth National Park, Uganda (2017-2020)

## Overview
- The dataset combines detailed life-history data on banded mongooses with daily body mass measurements, biometric data from trapping events, and weather data.
- It includes an experimental component designed to assess fitness and life-history trade-offs, potentially with trans-generational effects.

## Data collected
- Experimental individuals plus general life-history information
- Daily body mass measurements
- Biometric data gathered during trapping events
- Weather data recorded at the field site

## Study site and period
- Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)
- Timeframe: 2017–2020

## How data were collected
- Eight groups habituated to observers; groups trained to sit on a digital balance for body mass.
- >95% of the population marked; regular capture for biometric data and blood samples.
- Death vs dispersal differentiation achieved because mongooses disperse in groups.
- Weather data from a field-site weather station: daily precipitation, minimum and maximum temperatures.
- Capture data collected during trapping events:
  - Live traps; anaesthesia with isoflurane; transponder microchips implanted; DNA sampling (tail tip tissue).
  - Reproductive status recorded (PREG, OES, NONB, PE, BS, or combinations); foetus size and number estimated by palpation.
  - Weights and body measurements taken during first year of life; blood samples drawn quickly (2–3 minutes) and animals released promptly.
  - Weights measured in morning (MW) or evening (EW).
- Life-history events tracked at two levels:
  - Individual level: START/END (birth/immigration or death/emigration), CODE (e.g., BORN, DIED, FPREG), plus additional life events.
  - Group level: IGI (InterGroup Interaction), BIRTH (synchronous births).

## Experimental design details
- Study period: May 2017 – March 2020.
- Design: age- and weight-matched females in six groups assigned to provisioned (P) or control (C) categories.
- Provisioning: provisioned females fed one egg three times per week; each provisioned female paired with an age-matched control within the group.
- Replacements: if a provisioned female died, a replacement from the group used.
- Sample sizes: 18 provisioned females; 15 control females.
- Outcomes: 71 litters born; average 6.7 litters per female (range 2–15).
- Mean monitoring duration per subject: 561 days (min 165, max 1053).

## Purpose and use
- To measure fitness and life-history trade-offs in banded mongooses.
- To evaluate potential trans-generational effects.

## Data responsibility and governance
- Principal Investigator: Jonathan D. Blount (University of Exeter)
- Co-investigator: Michael A. Cant (University of Exeter)
- Postdoctoral researchers involved in data collection/analysis: Magali Meniri, Faye J. Thompson, Harry H. Marshall

## Data completeness and gaps
- Some capture and weight data may be missing due to occasional escape from traps or weighing events.

## Variables and data tables (structure)
- Table 1. Captures
  - Key fields: CAPTURE_DATE, INDIV, TRANSPONDER, PACK, PACK_STATUS (PREG, OES, NONB, PE, BS, etc.), AGE, EXAMINER, DRUGS (ISO/ISOF), SEX (M/F/Pups), REPRO_STATUS, LACTATING, ULTRASOUND, FOETUSES, FOET_SIZE, MILK_SAMPLE_MK, WEIGHT, HEAD_WIDTH, HEAD_LENGTH, BODY_LENGTH, HINDFOOT_LENGTH, TAIL_LENGTH, TAIL_CIRC, TICKS, PLASMA_SAMPLE_PL, BLOOD_SAMPLE_BL, WBC, RBC, WSK, etc.
- Table 2. Experimental females
  - PACK, ID, TREATMENT_GROUP (C or P), DATE_STARTED, COMMENT
- Table 3. Experimental males
  - PACK, ID, STATUS (BREEDING or NON-BREEDING), DATE_STARTED, DATE_STOPPED, COMMENT
- Table 4. Life history
  - DATE, PACK, INDIV, SEX (M/F/P), AGE CAT (AD/INF/PUP/SUB), STATUS (AD/DEP/MULTI/PRIMIP), START_END (END/RESTART/START/STOP), CODE (23 levels of life events), EXACT (Y/N), LSEEN, CAUSE, LITTER, etc.
- Table 5. Weather
  - DATE, RAIN_MWEY A, MAX_TEMP, MIN_TEMP, OBSERVER
- Table 6. Weights
  - PACK, DATE, INDIV, SEX (M/F), WEIGHT, ACCURACY

## Notes on interpretation
- The variable codes (e.g., PACK_STATUS, REPRO_STATUS, LIFE EVENT CODES) provide granular context for life-history analyses and cross-table relationships.
- The dataset supports analyses of growth, reproduction, survival, dispersal, social dynamics, and environmental influences on life history.