# Sampling regime and collection methods

- Study subject and location: Wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda; ongoing since 1995; population typically 10–12 social groups with ~20 adults plus offspring per group.
- Individual identification and tracking: Unique marks (fur shave patches in adults; dye marks in pups); regular trapping every two months to maintain marks; most groups habituated to observers within ~5 meters.
- Group monitoring cadence: Groups visited every 1–3 days for at least 20 minutes to record group composition, life history, reproduction, and cooperative behaviour; daily visits during pup birth periods to record precise birth dates.
- Experimental design overview: Five focal groups underwent simulated intrusions (March 2016–May 2017) using olfactory, auditory, and visual stimuli from neighboring rival groups; trials per focal group included 4–6 trials with standardized stimuli.
- Control conditions: For each focal group, control trials used stimuli from the focal group itself (self-produced faeces/scent marks, focal group close calls, and four focal males trapped and transported away briefly).
- Stimulus presentation sequence: Stimuli collected and presented in a structured order (faeces/scent, war cries, then rival males) with standardized timing; each 30-second war-cry clip used once to avoid habituation.
- Trial structure and spacing: A total of 22 simulated intrusion trials and 22 control trials; trials separated by at least two weeks to prevent habituation.
- Behavioral data collection window: Observations span a 5-day period per trial: 2 days before, day of, and 2 days after stimulus presentation.
- Observation schedule and behaviours: Each day includes 2 hours in the morning and 2 hours in the afternoon; observations focus on grooming and aggressive interactions, recording actor, recipient, interaction type, group, trial, and time period.
- Data handling of observations: Two observers record all grooming and aggression with individual identities; interactions involving unidentifiable individuals are excluded from analysis; before/during/after data are pooled for analysis.
- Field instrumentation: Life history data entered via bespoke Mongoose 2000 app on Samsung tablets; data downloaded to MS Access; radio collars (~30 g) with 20 cm antennas; audio recordings of war cries/close calls with H1 Zoom and Sennheiser mic; playback via iHome speaker.
- Calibration and quality control: Field instruments calibrated to factory settings; data quality checks implemented through MS Access queries and bespoke R scripts to detect inconsistencies (e.g., multiple death records, ID typos).
- Data structure and content: Data stored in two CSV files:
  - Grooming or aggressive interactions (actor, recipient, focal group, trial, interaction type, time point) across simulated intrusion and control trials and time periods (before, during, after).
  - Individuals involved in interactions (indiv, sex, age, pack, trial) with IDs corresponding to the interaction records.
- Data processing approach: Edge lists created for grooming and aggressive interactions per trial and time period; nodes extracted from edge lists with age and sex metadata.
- Data governance and accessibility: Field data collected with standardized procedures and stored for downstream analysis; detailed metadata on interaction types, timings, and trials supports reproducibility and cross-trial comparisons.