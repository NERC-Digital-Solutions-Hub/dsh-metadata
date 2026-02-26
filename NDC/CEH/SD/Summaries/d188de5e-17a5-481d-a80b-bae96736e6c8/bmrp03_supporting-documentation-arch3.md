# Sampling regime and collection methods

- Study context and population
  - Long-term study of wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Population comprises 10–12 social groups; individuals are uniquely marked for longitudinal identification; groups are regularly tracked via trapping and observer sightings.

- Sampling regime
  - Regular marking and tracking: individuals are shaved or dye-marked for life-long identification; radio collars attached to some individuals for group localization.
  - Monitoring cadence: groups visited frequently (every 1–3 days for at least 20 minutes) to record composition, life history, and cooperative/reproductive behavior.
  - Intensive monitoring during reproduction: daily visits when females are pregnant to record precise pup birth dates.
  - Data capture tools and storage: bespoke data app for field data; data subsequently stored in a database.

- Experimental design
  - Five focal groups subjected to simulated intrusions (March 2016–May 2017).
  - Stimuli types in intrusion trials: olfactory (rival faeces, urine, scent marks), auditory (rival war cry playback), visual (rival males in traps).
  - Control trials used stimuli from the focal group itself (e.g., focal group faeces/scent in the field, focal group close calls, and focal group males in traps).
  - Trial structure: 22 simulated intrusion trials and 22 control trials, with at least two weeks between trials to minimize habituation.
  - Stimuli collection and presentation: rival group samples collected in the morning and presented in a standardized sequence; war cries recorded and normalized; playback via a portable speaker; four rival adult males trapped for presentation in intrusion trials.

- Observational protocol
  - Behavioral observations: 5-day windows per trial (2 days before, day of, 2 days after) focused on grooming and aggression.
  - Temporal sampling: 1 hour in the morning and 1 hour in the afternoon per day when groups are foraging.
  - Data collection specifics: two observers record every grooming and aggressive interaction with actor/recipient identities; grooming defined as mouth-based fur manipulation; aggressive interactions include lunging, biting, growling, snarling, or displacement.
  - Data handling: only observations with confirmed identities are included; non-identifiable interactions are excluded.

- Fieldwork instrumentation
  - Data collection app: Mongoose 2000 on Samsung Galaxy Note tablets; data uploaded to MS Access database.
  - Recording equipment: radio collars for identity/locomotion; war cries/close calls recorded with H1 Zoom microphone and Sennheiser mic; playback via iHome speaker.
  - Calibration: field instruments calibrated to factory settings.

- Analytical methods and data structure
  - Data representations: edge lists (grooming and aggressive interactions) and node lists (individuals involved).
  - Edge lists: capture actor, recipient, focal group, trial, interaction type (Grooming or Aggression), and time point (Before, During, After).
  - Node data: individual ID, sex, age, pack (focal group), trial ID.
  - Time periods: Before (2 days pre-presentation), During (day of presentation), After (2 days post-presentation).
  - Data quality control: internal checks in the Mongoose app; MS Access and bespoke R code used to detect errors (e.g., multiple death records, typos in IDs).
  - Data structure and availability: stored in two CSV files:
    - File 1: grooming or aggressive interactions with columns: actor, recipient, focal group, trial, interaction, time.point.
    - File 2: individuals involved with columns: indiv, sex, age, pack, trial.
  - Data governance and traceability: explicit documentation of observation protocols, standardized interaction definitions, and reproducible data processing steps.