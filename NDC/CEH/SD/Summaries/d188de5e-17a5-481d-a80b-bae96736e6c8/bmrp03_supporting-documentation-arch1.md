# Sampling regime and collection methods

- Study context and population
  - Wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Long-term study since 1995; typically 10–12 social groups; groups ~20 adults plus offspring.
  - Individuals uniquely marked (fur shave patches in adults; dye marks in pups); regular trapping every two months for identification.
  - 1–2 individuals per group fitted with radio collars; groups habituated to observers at <5 m.

- Experimental design
  - Five focal groups subjected to simulated intrusion trials (March 2016–May 2017) to mimic intergroup conflict.
  - Stimuli from a neighboring rival group: olfactory (faeces, urine, scent marks), auditory (war cries), and visual (rival males in traps).
  - Rival group used for all trials within a focal group; control trials used stimuli from the focal group itself (self-stimuli).
  - 22 simulated intrusion trials and 22 control trials; minimum 2-week spacing between trials to prevent habituation.
  - Each trial includes a 5-day observation window: 2 days before, day of, and 2 days after stimulus presentation.

- Behavioral observations
  - Daily observation schedule: 1 hour in the morning and 1 hour in the afternoon per day.
  - Two observers recorded grooming and aggressive interactions, noting actor, recipient, and identities.
  - Grooming defined as mouth-based fur grooming; interactions counted per actor–recipient pair with rules for repeats across short rest periods.
  - Aggressive interactions defined by specific behaviours (lunging, biting, growling, displacement); same-pair interactions counted with short breaks considered.
  - Observations with unidentified individuals excluded from analyses.

- Stimuli presentation details
  - Stimuli collected from rival group on the morning of presentation; 100 × 137 mm bags used for faeces; semi-circular arrangement around a central sheet to encourage marking.
  - War cries: 30-second playback clips from rival group, standardized in amplitude to -1 dB; each clip used once.
  - Rival males: four adult males trapped, covered during transport, then presented to focal group for ~5 minutes; post-presentation they were returned.
  - Control trials used focal-group stimuli (faeces and scent marks from focal group; close call recordings from focal group; trapping of focal-group males presented to the group).

- Fieldwork instrumentation
  - Data collected with a bespoke app (Mongoose 2000) on Samsung Galaxy tablets; data imported into MS Access.
  - Observations noted on paper data sheets and transcribed to MS Excel.
  - Equipment: radio collars (~30 g, 20 cm antenna); war cry recordings with H1 Zoom and Sennheiser mic; playback via iHome speaker.

- Calibration
  - Field instruments calibrated to factory settings.

- Analytical methods
  - Edge lists created for grooming and aggressive interactions by trial, focal group, and time period (before, during, after).
  - Nodes derived from individuals involved in interactions; ages and sexes recorded.
  - Data structure prepared for network and statistical analyses.

- Quality control
  - Mongoose 2000 includes internal checks to reduce data collection errors.
  - Data quality checks via MS Access queries and bespoke R code to detect issues (e.g., multiple death records, ID typos).

- Data structure and contents
  - Two CSV files:
    - Grooming or aggressive interactions: actor, recipient, focal group, trial, interaction type (Grooming/Aggression), time.point (Before/During/After), along with identifiers for each interaction.
    - Individuals involved: indiv, sex (M/F), age (years), pack (focal group), trial.
  - Column descriptions provide explicit mapping for actor/recipient identities, trial IDs (R1–R6 for simulated intrusions; C1–C7 for controls), and time period classifications.