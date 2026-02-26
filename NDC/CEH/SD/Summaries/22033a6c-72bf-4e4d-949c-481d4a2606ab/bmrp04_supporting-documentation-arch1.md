# Sampling regime and collection methods

## Study context
- Banded Mongoose Research Project on wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda.
- Long-running study since 1995; population typically 10–12 social groups, about 20 adults per group plus offspring.
- Individuals are uniquely marked; one to two individuals per group fitted with radio collars for location via radio telemetry.
- Groups habituated to observers (approach within <5 m); visits every 1–3 days for 20 minutes to record composition, life history, reproduction, and cooperative behaviour.
- Reproduction is highly synchronized within groups; births recorded daily when females are pregnant.

## Experimental design
- Five focal groups subjected to simulated intrusion trials (Mar 2016–May 2017) to mimic intergroup conflict.
- Stimuli from neighboring rival group included: olfactory cues (faeces, scent marks), auditory cues (war cry recordings), and visual cues (rival males in traps).
- For each focal group, the same rival group provided stimuli across all trials; 22 simulated intrusion trials and 22 matched control trials.
- Trial structure:
  - Simulated intrusions: samples collected from multiple rival individuals (both sexes, various ages); 100 × 137 mm samples presented around a plastic sheet; 3-minute exposure followed by playback of rival war cries; four rival adult males trapped and presented to focal group in the late afternoon for ~5 minutes.
  - Controls: stimuli from the focal group itself (faeces/scent marks, close-call calls); four focal-group adult males trapped and presented similarly.
- Timing and sequencing: stimuli presented between 07:43–10:27 (morning) and 16:35–18:18 (afternoon); trials separated by at least two weeks to minimize habituation.
- Data capture: focal group filmed during presentations using tablet or video camera.

## Fieldwork instrumentation
- Life-history data collected with a bespoke data collection app (Mongoose 2000) on tablets; data stored in MS Access.
- Individuals wear radio collars (~30 g) with 20 cm antennae.
- War cries recorded via H1 Zoom recorder with Sennheiser microphone; playback through hidden iHome speaker.
- Stimuli presentations filmed with tablets or a Panasonic video camera.

## Calibration steps and values
- Field instruments calibrated to factory settings.

## Analytical methods
- Data collection performed by a single observer from videos; not fully blind to treatment due to field constraints.
- Bias-minimization: initial observations made without audio to avoid cue bias; videos re-watched with sound to log exact timing of call playback.
- Sampling protocol: at 30-second intervals starting 30 seconds after the first group member comes within 2 m of the stimulus; continue for ~3 minutes 30 seconds, discarding samples if fewer than two samples per stimulus type are obtained.
- Recorded measures per sampling point:
  - Number of group members within 2 m of the stimulus.
  - Number of group members exhibiting each of six behaviours: stationary, walking/running, digging, standing upright, scent marking, attacking.
- Classification:
  - Defensive behaviours: standing upright, scent marking, attacking.
  - Non-defensive: stationary, walking/running, digging.
- Derived metrics:
  - (1) Spatial cohesion: mean proportion of group members within 2 m; count of foraging group members; whether stimulus occurred in core territory.
  - (2) Participation in collective defence: mean proportion exhibiting defensive behaviours; foraging context; core vs non-core location.
  - (3) Homogeneity of behavioural response: mean H-index of behavioural diversity; plus context for foraging and core location.
- Data quality: Mongoose 2000 includes checks to reduce errors (e.g., ensuring individuals present before recording data); data quality checks performed via MS Access queries and bespoke R code to detect inconsistencies.

## Quality control
- Internal checks in Mongoose 2000 to limit data entry errors (e.g., presence requirements for recording data about individuals).
- Additional quality control through MS Access queries and R scripts to detect anomalies (e.g., duplicate death records).

## Details of data structure
- Data stored in 3 CSV files, each corresponding to a different metric set:

1) Mean proportion of individuals within 2 m of the stimulus during each presentation
- Columns include:
  - video, video ID code (video)
  - grp (focal group ID)
  - stim (trial/type: c_intruders, c_scents, t_intruders, t_scents)
  - loc (Core = within 50% activity area; Non-core = outside)
  - field.grp.sz (number of group members >6 months on foraging)
  - stim.mean.prop2m (mean proportion within 2 m)

2) Mean proportion of group members exhibiting defensive behaviour
- Columns include:
  - video, video ID code
  - grp, focal group ID code
  - stim (type: c_call, c_intruders, c_scents, t_call, t_intruders, t_scents)
  - loc (Core/Non-core)
  - field.grp.sz
  - stim.mean.propdef (mean proportion of group members exhibiting defensive behaviour)

3) Mean H-index of behavioural diversity
- Columns include:
  - video, video ID code
  - grp, focal group ID code
  - stim (types as above)
  - loc (Core/Non-core)
  - field.grp.sz
  - avg.h.bystim (mean H-index of behaviour exhibited by group members)

- The datasets enable analysis of how intrusion vs. control stimuli affect spatial withdrawal, defensive participation, and behavioural diversity across core and non-core territories.