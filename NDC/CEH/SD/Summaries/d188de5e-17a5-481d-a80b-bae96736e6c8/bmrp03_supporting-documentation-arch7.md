# Sampling regime and collection methods

- Study area and subjects
  - Wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′ E).
  - Long-term population study since 1995; typically 10–12 social groups with ~20 adults per group plus offspring.
  - Individuals uniquely marked (shave patches in adults; dye marks in pups); regular trapping every two months.
  - 1–2 individuals per group fitted with radio collars to enable group localization; most groups habituated to observers at close range.

- Experimental design
  - Five focal groups subjected to simulated intrusion trials (Mar 2016–May 2017) to mimic intergroup conflicts.
  - Stimuli types: olfactory (rival faeces, urine, scent marks), auditory (rival war cries), and visual (rival males in traps).
  - Stimuli drawn from neighboring rival group; same rival group used across all trials for a given focal group.
  - Control trials used focal-group-origin stimuli (faeces/scent marks from focal group; close-call recordings instead of war cries; focal-group males trapped and returned).
  - 22 simulated intrusion trials and 22 control trials; intervals of at least 2 weeks to prevent habituation.
  - Behavioral observations collected over 5 days per trial: 2 days before, day of, and 2 days after stimulus presentation; daily observation windows in morning and afternoon.

- Observational methodology
  - During each observation window: minimum two observers recorded all grooming and aggressive interactions, noting actor/recipient identities and direction.
  - Grooming: defined as mouth-based fur manipulation; episodes recorded with rules for interruptions and partner changes.
  - Aggression: defined as lunging, biting, growling, snarling, or displacement; same-pair interactions noted with short breaks treated as a single event.
  - Data quality: observations with uncertain individual IDs excluded.

- Field instrumentation and data capture
  - Life history data collected with a bespoke app (Mongoose 2000) on Samsung Galaxy tablets; data imported into MS Access.
  - Observations recorded on paper and transcribed to MS Excel spreadsheets.
  - Individuals equipped with ~30 g radio collars (5 cm antenna) for localization; war cries recorded with H1 Zoom and Sennheiser mic; playback via portable speaker.

- Calibration and data integrity
  - Field instruments calibrated to factory settings.
  - Internal app checks reduce data collection errors; data quality checked via MS Access queries and bespoke R code to detect inconsistencies (e.g., duplicate death records, ID typos).

- Analytical approach and data structure
  - Analytical focus on social networks through edge lists and nodes:
    - Edge lists: grooming and aggressive interactions by actor-recipient, trial, focal group, and time period (before/during/after).
    - Nodes: individuals involved in any interactions; include age and sex.
  - Data collection results organized into two CSV files:
    - File 1: Grooming or aggressive interactions (actor, recipient, focal group, trial, interaction type, time point).
    - File 2: Individuals involved (indiv ID, sex, age, pack, trial).
  - Time framing for analysis: before (2 days prior), during (day of), and after (2 days post) stimulus presentation; observations aggregated per 1-hour blocks within morning and afternoon sessions.

- Data accessibility and schema overview
  - Two CSV files capture the full dataset: one for interaction events (actor→recipient, type, trial/time window) and one for participant metadata (ID, sex, age, group, trial).
  - Clear column definitions provided to enable replication, validation, and integration with spatial or network analyses.