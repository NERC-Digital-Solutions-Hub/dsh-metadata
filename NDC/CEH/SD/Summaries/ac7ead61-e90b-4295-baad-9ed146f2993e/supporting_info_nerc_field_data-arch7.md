# Banded mongooses life history and provisioning experiment data from Queen Elizabeth National Park, Uganda (2017-2020)

- A comprehensive data collection on banded mongooses combining life history, biometric, genetic, and environmental information to study fitness and life-history trade-offs, including trans-generational effects.
- Data types include: experimental individuals (with detailed life history), field-collected biometric measurements (daily body mass, weight measurements), trapping-biopsy data (DNA from tail tissue, transponder IDs), blood samples, reproductive status (pregnancy, oestrus, non-breeding, pack-escorting, pack-babysitting), ultrasound data, foetus counts and sizes, and weather data (daily precipitation, min/max temperatures).

- Study site and period
  - Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)
  - Timeframe: 2017–2020; experiment ran May 2017–March 2020

- Data collection and field procedures
  - Eight mongoose groups were habituated to human observers and trained to sit on a digital balance for body mass measurements; >95% of the population marked and regularly captured for biometric data and blood samples.
  - Daily field visits; individuals are tracked within groups, allowing clear distinction between death and dispersal.
  - Trapping and sampling: live traps, anesthesia (isoflurane), transponder microchips for identification, DNA sampling from tail tissue, blood samples when required, and release back to the group after recovery.
  - Reproductive data: pack reproductive status (PREG, OES, NONB, PE, BS), foetus size and number estimated by palpation when relevant.
  - Morphometrics: weights measured, with timing (MW = morning, EW = evening); additional body measurements (head width/length, body length, limb lengths, tail measurements, tail circumference, etc.).
  - Life history data collection at two levels:
    - Individual level: START/END (birth, immigration, death, emigration), CODE (e.g., BORN, ADIED, FPREG), and related sub-events.
    - Group level: IGI (InterGroup Interaction), BIRTH (synchronous birth events).
  - Weather data: field weather station recording daily rainfall and daily min/max temperatures.

- Experimental design
  - Six age- and weight-matched female groups randomly assigned to provisioned (P) or control (C) categories at the start.
  - Provisioned females received a cooked egg three times per week; each provisioned female had an age-matched within-group control.
  - Replacement rules: if a provisioned female died, a replacement from the group was selected.
  - Sample sizes: 18 provisioned females and 15 controls; mean monitoring duration 561 days (range 165–1053 days).
  - Reproductive output observed: 71 litters born during the experimental period, average 6.7 litters per provisioned female (range 2–15).

- Data organization and content (Tables)
  - Table 1. Captures: capture date, individual ID, pack, transponder, sex, age, reproductive status, weights, measurements, ultrasound status, samples collected, and related lab data.
  - Table 2. Experimental females: pack, individual ID, treatment group (C or P), date started, comments.
  - Table 3. Experimental males: pack, individual ID, breeding status, date started/stopped, comments.
  - Table 4. Life history: date, pack, individual, sex, age category, status, start/end markers, life history code, exactness flag, cause of death, litter ID, and related events.
  - Table 5. Weather: date, rainfall, max/min temperatures, observer.
  - Table 6. Weights: pack, date, individual, sex, weight, and measurement accuracy.

- Data quality and limitations
  - Some capture and weight data may be missing due to escape from trapping or weighing events.
  - Data are linked via multiple identifiers (PACK, INDIV, TREATMENT_GROUP, etc.), enabling integration across tables but requiring careful cross-referencing for GIS use.

- GIS-relevant aspects and potential uses
  - Spatial identifiers: packs and individual IDs enable mapping of group territories and individual lifeways across the study site (coordinates provided for the site; pack-level geospatial data may be inferred or augmented with external shapefiles).
  - Temporal dimension: rich time-series data (dates for captures, births, deaths, life-history events, provisioning periods, and weather) suitable for animated or time-enabled GIS analyses.
  - Event-based mapping: births, deaths, migrations, and intergroup interactions can be visualized as events tied to space and time.
  - Weather integration: coupling of environmental layers (daily rainfall and temperature) with life-history events to assess environmental forcing on fitness and reproductive timing.
  - Data standards: multiple tables with clearly defined codes (e.g., reproductive status, life-history codes, age categories) facilitate standardized GIS attribute schemas and cross-dataset joins.

- Governance and personnel
  - Principal Investigator: Jonathan D. Blount (University of Exeter) with Co-Investigator Michael A. Cant (University of Exeter).
  - Postdoctoral researchers involved in collection and analysis: Magali Meniri, Faye J. Thompson, Harry H. Marshall.

- Purpose and intended outcomes
  - Objectives: quantify fitness and life-history trade-offs, assess potential trans-generational effects, and examine how provisioning influences reproductive strategies and lifespans in wild banded mongooses.