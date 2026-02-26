# Sampling regime and collection methods

- Study context
  - Banded Mongoose Research Project on wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Population studied since 1995; groups typically 10–12 social groups with ~20 adults plus offspring.
  - Individuals uniquely marked for identification; radio collars fitted to 1–2 individuals per group for location; groups habituated to observers.

- Sampling regime
  - Regular Trapping: individuals trapped every two months for mark maintenance.
  - Group monitoring: visits every 1–3 days for at least 20 minutes to record group composition, life history, and reproductive/cooperative behavior.
  - Reproduction monitoring: daily visits when females are pregnant to record pup birth dates.

- Experimental design
  - Five focal groups subjected to simulated intrusions (March 2016–May 2017) to mimic intergroup conflict.
  - Stimuli used: rival faeces/urine/scent marks (olfactory), rival war cry recordings (auditory), and rival males in traps (visual).
  - Each focal group used the same rival group across all intrusion trials.
  - Controls: same stimuli types but originating from the focal group (self-produced cues); close-call playbacks and self-representation via trapped males.
  - Trial count: 22 simulated intrusion trials and 22 control trials; at least 2 weeks between trials to prevent habituation.

- Stimuli presentation details
  - Olfactory: faeces, urine, scent marks collected from rival group the morning of presentation; samples kept in a standardized 100 × 137 mm ziplock bag; presented in a semi-circle around a plastic sheet in the focal group’s foraging path.
  - Auditory: 30-second war-cry clips from rival group; recordings standardized and amplitude normalized to -1 dB; playback via portable speaker hidden in vegetation; each clip used once.
  - Visual: four adult rival males trapped, transported to presentation site for 30 minutes, then returned; presentation timed 16:35–18:18.

- Observational regime
  - For each trial, observations of social interactions over 5 days: 2 days before, day of, and 2 days after presentation.
  - Daily observation windows: 1 hour in the morning (07:00–12:00) and 1 hour in the afternoon (16:00–19:30) when mongooses are foraging.
  - Data collected: all grooming and aggressive interactions with identities and direction; two observers minimum; grooming definitions and aggression criteria specified.

- Definitions and data inclusion rules
  - Grooming: interaction where one mongoose grooms another using mouth and fur manipulation; pairing and timing rules (e.g., separate interactions if breaks >30 seconds; one interaction per actor–recipient pair per grooming bout).
  - Aggression: includes lunging, biting, growling, snarling, or displacement; one aggressive interaction recorded per pair if breaks are ≤30 seconds; observations with unidentified individuals are excluded.
  - Data are pooled by period: before (2 days prior), during (day of), and after (2 days post) presentations.

- Fieldwork instrumentation
  - Data collection app: Mongoose 2000 on Samsung Galaxy Note 10.1 tablets; data imported into MS Access.
  - Observations: recorded on paper and transcribed to MS Excel.
  - Tracking equipment: radio collars (~30 g) with 20 cm whip antenna.
  - Acoustic data: war cries and close calls recorded with H1 Zoom + Sennheiser mic; playback with iHome speaker.

- Calibration and quality control
  - Field instruments calibrated to factory settings.
  - Mongoose 2000 app includes internal checks to reduce data collection errors.
  - Data quality checks: MS Access queries and bespoke R code to detect inconsistencies (e.g., multiple death records); verification of observer IDs and individual identities.

- Data structure and storage
  - Data stored in two CSV files.
  - File 1: Grooming or aggressive interactions (actor, recipient, focal group, trial, interaction type, time.point).
  - File 2: Individuals involved (indiv, sex, age, pack, trial).
  - Time points defined as Before, During, and After relative to stimulus presentation.

- Analytical approach
  - Edge lists: create actor–recipient interactions for grooming and aggression across trials and time periods.
  - Nodes: compile list of individuals involved in any interactions; extract age and sex for analyses.