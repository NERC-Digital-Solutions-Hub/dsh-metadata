# Data on banded mongooses in Queen Elizabeth National Park, Uganda (2017-2020)

## Data overview
- Includes life-history data and general field information for banded mongooses, plus daily body mass measurements, biometric data from trapping events, and weather data.
- Captures and life-history events are recorded at both individual and group levels, with detailed event codes.

## Study location and time period
- Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)
- Study period: 2017–2020 (experimental period May 2017–March 2020)

## Data collection methods
- Eight mongoose groups are completely habituated to human observers and trained to sit on a digital balance for body mass measurements.
- >95% of the population is marked; individuals are regularly captured for biometric data and blood samples.
- Daily group visits; banded mongooses disperse in groups, enabling clear distinction between death and dispersal.
- Weather data collected via a weather station at the field site (daily precipitation, min/max temperatures).
- Capture data: live traps, anaesthetized with isoflurane; transponder microchips implanted; tissue samples taken for DNA; pregnancy/stage data recorded; weights recorded at first year of life.
- Weights: morning (MW) or evening (EW) measurements on a portable scale.
- Life-history data tracked at the individual level (START/END, life-event codes) and at the group level (e.g., InterGroup Interaction, synchronous births).
- Experimental manipulation: age- and weight-matched females assigned to provisioned (P) or control (C) groups; provisioning involved three weekly eggs; replacements used if a provisioned female died.
- Experimental period for the provisioning study: May 2017–March 2020; 18 provisioned females and 15 controls; mean monitoring duration 561 days (range 165–1053 days); 71 litters born (average 6.7 litters per female).

## Why the data were collected
- To measure fitness and life-history trade-offs in banded mongooses and to assess potential trans-generational effects.

## Roles and provenance
- Principal Investigator: Jonathan D. Blount (University of Exeter)
- Co-Investigator: Michael A. Cant (University of Exeter)
- Postdoctoral researchers involved in data collection/analysis: Magali Meniri, Faye J. Thompson, Harry H. Marshall

## Data completeness and limitations
- Some capture and weight data may be missing for certain individuals due to escape from traps or weighing gaps.

## Data structure and key variables (Tables 1–6)
- Table 1. Captures
  - Variables include: Capture_DATE, INDIV (individual ID), TRANSPONDER, PACK, PACK_STATUS (breeding status), AGE (adult/infant/m/pup/subadult), Examiner, DRUGS (anesthetic), SEX, REPRO_STATUS (PREG, OES, NONB, PE, BS), ULTRASOUND, FOETUSES, FOET_SIZE, MILK_SAMPLE_MK, WEIGHT, HEAD_WIDTH, HEAD_LENGTH, BODY_LENGTH, HINDFOOT_LENGTH, TAIL_LENGTH, TAIL_CIRC, TICKS, PLASMA_SAMPLE_PL, BLOOD_SAMPLE_BL, WBC, RBC, WSK, etc.
- Table 2. Experimental females
  - Variables: PACK, ID, TREATMENT_GROUP (C or P), DATE_STARTED, COMMENT
- Table 3. Experimental males
  - Variables: PACK, ID, STATUS (BREEDING vs NON-BREEDING), DATE_STARTED, DATE_STOPPED, COMMENT
- Table 4. Life history
  - Variables: DATE, PACK, INDIV, SEX, AGE_CAT (AD/INF/PUP/SUB), STATUS (AD/DEP/MULTI/PRIMIP, etc.), START_END (END/RESTART/START/STOP), CODE (23-level life-history codes, e.g., BIRTH, BORN, DIED, FPREG, IGI, LEAVE, LITTER, SOES, etc.), EXACT (Y/N), LSEEN (date last seen), CAUSE (cause of death), LITTER (litter ID)
- Table 5. Weather
  - Variables: DATE, RAIN (mm), MAX_TEMP (C), MIN_TEMP (C), OBSERVER
- Table 6. Weights
  - Variables: PACK, DATE, INDIV, SEX, WEIGHT (g), ACCURACY

## Potential uses and considerations for analysis
- Investigate effects of provisioning vs control on reproductive success, survival, and litter outcomes.
- Explore relationships between body mass, biometric measurements, and reproductive status across individuals and packs.
- Assess life-history trade-offs and potential trans-generational effects under differing provisioning regimes.
- Integrate weather data to examine environmental influences on breeding timing and success.
- Handle data limitations by accounting for missing capture/weight observations and potential sampling bias due to trap/dropout.

## Data management and accessibility notes
- Data are described with extensive metadata in spreadsheet-like tables; the dataset emphasizes traceability of sources and provenance, with explicit documentation of variables, units, and coding schemes.
- The project emphasizes making datasets discoverable and usable by providing metadata and clear data structures.