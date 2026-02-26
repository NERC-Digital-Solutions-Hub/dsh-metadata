# Banded Mongooses Life History Data from Queen Elizabeth National Park, Uganda (2017-2020)

## Overview
- Dataset comprises experimental individuals and general life-history data, including daily body mass measurements, biometric data, and weather data.
- Collected to measure fitness and life-history trade-offs, and potential trans-generational effects.
- Study site: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E); data collection period: 2017–2020.

## Data collection and methods
- Eight groups of banded mongooses were habituated to human observers and trained to sit on a digital balance for body mass measurements.
- Over 95% of the population was marked; groups visited daily; death vs. dispersal distinguished due to group dispersal behavior.
- Weather data gathered via a field weather station recording daily precipitation, min and max temperatures.
- Capture data collected during trapping events:
  - Live traps used; anesthesia with isoflurane.
  - Individuals marked with a symbol, transponder microchips implanted, DNA via tail-tip biopsy collected.
  - Reproductive status recorded (PREG, OES, NONB, PE, BS, or combinations); foetus size and count estimated by palpation when relevant.
  - Weights and biometric measurements taken (weights primarily from a portable scale; morning or evening measurements).
  - Blood samples drawn from jugular vein when required; rapid recovery and release back to group.
- Life-history data recorded at two levels:
  - Individual level: START/END events, LIFE events coded (BORN, ADIED, ENDEV, FPREG, etc.).
  - Group level: IGI (InterGroup Interaction), BIRTH events.
- Experimental design: May 2017 to March 2020; age- and weight-matched females in six groups assigned to provisioned (P) or control (C) categories at start.
  - Provisioned females received ~1 egg omelette three times weekly; each provisioned female paired with an age-matched control within the group.
  - If a provisioned female died, a replacement was selected.
  - Sample: 18 provisioned and 15 controls; mean monitoring duration 561 days (range 165–1053 days); 71 litters born (mean 6.7 litters per female; range 2–15).

## Data content and structure
- Tables and key variables:
  - Table 1. Captures: capture date, individual ID, transponder, pack, pack status (PREG, OES, NONB, PE, BS, etc.), age category, examiner, drugs (anesthetic used), sex, reproductive status, lactation, ultrasound, foetuses, foet size, milk samples, weight and body measurements (weight, head width/length, body length, limb measurements, tail metrics, etc.), ticks, plasma/blood samples, WBC/RBC, and other biometrics.
  - Table 2. Experimental females: pack, ID, treatment group (C or P), date started, comments.
  - Table 3. Experimental males: pack, ID, breeding status, date started, date stopped, comments.
  - Table 4. Life history: date, pack, individual, sex, age category (AD/INF/PUP/SUB), status (AD/DEP/MULTI/PRIMIP, etc.), START_END coding, life-history CODE (23 possible levels including BIRTH, DIED, FPREG, IGI, etc.), exact flag, last seen date, cause of death, litter ID.
  - Table 5. Weather: date, rainfall (mm), max_temp (C), min_temp (C), observer.
  - Table 6. Weights: pack, date, individual, sex, weight (g), weight measurement accuracy.
- Data quality notes:
  - Capture and weight data may have missing entries due to escape during trapping or weighing.

## Data governance and stewardship considerations
- Data are organized with detailed variable definitions (as shown in the provided tables), supporting discoverability and reuse.
- Variables cover both individual- and group-level events, enabling nuanced life-history analyses.
- Provenance and processing steps implied by table structures (plans to document work done on datasets) support transparency and reproducibility.
- Potential data sharing considerations include:
  - Variation in data collection methods across different types (biometrics, genetics, reproductive measures, weather) requiring consistent metadata and units.
  - Missing data from capture/weight measurements; need for clear imputation guidance or data-use caveats.
- Data stewardship alignment:
  - Ensure metadata completeness (definitions, units, codes) and standardization across tables.
  - Maintain data update workflows and versioning to reflect ongoing discoveries or corrections.
  - Prepare data for deposition in appropriate data portals with clear licensing, access conditions, and provenance.

## Responsible parties
- Principal Investigator: Jonathan D. Blount (University of Exeter).
- Co-Investigator: Michael A. Cant (University of Exeter).
- Postdoctoral Researchers: Magali Meniri, Faye J. Thompson, Harry H. Marshall.

## Data quality, limitations, and context for use
- Data capture may be incomplete for some individuals due to escape from traps or weighing gaps.
- The provisioning experiment provides a controlled contrast (provisioned vs control) for assessing fitness and life-history trade-offs.
- The dataset integrates longitudinal individual data with group-level dynamics and environmental context (weather), enabling studies of trans-generational effects and life-history strategies under provisioning conditions.

## Temporal and geographic scope
- Temporal coverage: May 2017 – March 2020.
- Geographic coverage: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E).