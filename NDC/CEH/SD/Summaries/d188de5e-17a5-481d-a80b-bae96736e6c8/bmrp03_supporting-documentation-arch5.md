# Sampling regime and collection methods

## Overview
- Long-running study of wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′S, 29°54′E).
- Population typically comprises 10–12 social groups with ~20 adults per group, plus offspring.
- Individuals are uniquely marked for identification; regular trapping every two months; radio collars deployed on 1–2 individuals per group.
- Groups are visited frequently to record group composition, life history, and reproductive/cooperative behavior.
- Data collection supports analyses of social interactions and responses to simulated intergroup intrusions.

## Study design and stimuli
- Experimental design: simulated intrusions in five focal groups from March 2016 to May 2017.
- Intrusion trials: rival faeces, urine, scent marks (olfactory), rival war cry recordings (auditory), and rival males in traps (visual).
- Stimuli collected from neighboring rival groups; same rival group used per focal group across trials.
- Control trials: same stimulus types but derived from focal group itself (self-stimuli or non-threatening cues).
- Trial structure: 22 simulated intrusion trials and 22 control trials; trials spaced at least two weeks apart to prevent habituation.
- Presentation sequence per intrusion trial:
  - Faeces/scent marks placed on a plastic sheet in foraging path (07:43–10:27).
  - After ~3 minutes, play back rival war cries (30-second clips) via portable speaker; clips standardized to prevent habituation.
  - Afternoon: four adult rival males trapped, transported to presentation site for 30 minutes, then returned.
  - Presentation window for rival males: 16:35–18:18.
- Trial IDs and data: each pack has trial IDs (R1–R6 for intrusion; C1–C7 for controls).

## Observations and time framing
- Observation window per trial: 5 days total
  - 2 days before presentation (Before)
  - Day of presentation (During)
  - 2 days after (After)
- Daily observation schedule:
  - 1 hour in the morning (07:00–12:00)
  - 1 hour in the afternoon (16:00–19:30)
- Behavioral data collected:
  - Grooming and aggressive interactions recorded with actor and recipient identities and direction.
  - Grooming defined as mouth-based fur grooming; multiple interactions between pairs treated with specific rules (e.g., rest periods >30 seconds treated as new interactions).
  - Aggressive interactions defined by lunging, biting, growling, snarling, or displacement.
  - Interactions without confirmable identities excluded from dataset.
- Data synthesis: observations pooled into Before, During, and After periods for analysis.

## Fieldwork instrumentation and data capture
- Data collection app: Mongoose 2000 on Samsung Galaxy Note 10.1 tablets; data stored in an MS Access database.
- Observations of social interactions: recorded on paper datasheets and transcribed to MS Excel.
- Tracking equipment: radio collars (~30 g with 20 cm antenna).
- Audio data: war cries and close calls captured with H1 Zoom recorder and Sennheiser mic; playback via iHome speaker.
- Calibration: field instruments calibrated to factory settings.

## Data processing and quality control
- Analytical approach:
  - Edge lists created for grooming and aggressive interactions (actor, recipient, focal group, trial, time period).
  - Node list extracted from individuals involved in observed interactions; age and sex recorded.
- Quality control:
  - Mongoose 2000 includes internal checks to ensure data consistency (e.g., presence requirement for data collection).
  - Data quality checks performed in MS Access and bespoke R code to detect errors (e.g., conflicting death records, ID typos).

## Data structure and content
- Data stored in two CSV files:
  - File 1: Grooming or aggressive interactions (actor, recipient, focal group, pack, trial, ID, interaction, time.point)
    - time.point: Before, During, After
    - trial: R1–R6 (simulated intrusion), C1–C7 (control)
  - File 2: Individuals involved in grooming or aggressive interactions (indiv, sex, age, pack, trial)
- Columns provided:
  - actor (ID of individual performing interaction)
  - ID (recipient ID)
  - focal group
  - pack
  - trial (trial ID)
  - interaction (Grooming or Aggression)
  - time.point (Before, During, After)
  - indiv (ID of individual involved)
  - sex (M/F)
  - age (in years)

## Provenance and readiness for reuse
- Clear lineage from field collection to digital datasets:
  - Observational data collected in the field, digitized via Mongoose 2000 app, stored in MS Access, and exported to CSV for sharing.
  - Defined time windows (Before, During, After) and clearly labeled trial identifiers (R1–R6, C1–C7).
  - Comprehensive definitions for grooming and aggression, with explicit treatment of partial/missing identifications.
- Metadata considerations for reuse:
  - Species, study site, time frame, group composition, and stimuli details are specified.
  - Data are organized to support social network analyses and temporal comparisons across trials and time periods.