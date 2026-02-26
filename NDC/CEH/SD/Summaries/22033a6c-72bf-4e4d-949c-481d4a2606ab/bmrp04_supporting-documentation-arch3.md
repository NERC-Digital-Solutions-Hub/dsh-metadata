# Sampling regime and collection methods

- Study system and population
  - Wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Population studied since 1995; typically 10–12 social groups with about 20 adults plus offspring per group.
  - Individuals uniquely identified via fur shave marks (adults) or dye marks (pups); regular trapping every two months.
  - One to two individuals per group fitted with radio collars; most groups habituated to observers at close distance.
  - Groups visited every 1–3 days for at least 20 minutes to record group composition, life history, and reproductive/cooperative behavior; daily visits during pup births.

- Experimental design
  - Five focal groups subjected to simulated intrusions (March 2016–May 2017) to mimic intergroup conflict.
  - Stimuli included:
    - Olfactory: rival faeces and scent marks.
    - Auditory: rival war-cry recordings.
    - Visual: rival individuals placed in traps.
  - Stimuli collected from a single neighboring rival group per focal group; same rival group used across trials for a focal group.
  - Control trials used stimuli from the focal group themselves (self-origin); analogous procedures with focal-group stimuli.
  - Totals: 22 simulated intrusion trials and 22 control trials; minimum 2-week separation between trials to prevent habituation.
  - Data collection included filming the focal group during stimulus presentations.

- Fieldwork instrumentation
  - Data collection app (Mongoose 2000) on Samsung Galaxy tablets; data downloaded to an MS Access database.
  - Radio collars (~30 g) with 20 cm whip antennas; war cries and close calls recorded with H1 Zoom, Sennheiser mic; playback via iHome speaker.
  - Stimulus presentations filmed with Samsung tablets or Panasonic video camera.
  - Calibration: field instruments calibrated to factory settings.

- Calibration and measurement
  - Tools and recordings standardized to ensure consistency across trials (e.g., war-cry recordings trimmed to 30-second clips; amplitude normalized).

- Analytical methods
  - Behavioral data coded from videos by a single observer; attempt to minimize bias by initially removing audio, blinding to treatment identity and stimulus timing, then re-watching with audio to time the playback.
  - Sampling protocol:
    - Scan within 2 minutes at 30-second intervals starting 30 seconds after the first group member comes within 2 m of the stimulus.
    - Each stimulus type required at least two samples; presentations with fewer than two samples excluded.
  - Behavioral metrics recorded at each sampling:
    - Number of group members within 2 m of stimulus and out-of-contact foraging group size.
    - Six behaviors: stationary, walking/running, digging, standing upright, scent marking, attacking.
  - Defensive vs non-defensive categorization:
    - Defensive: standing upright, scent marking, attacking.
    - Non-defensive: stationary, walking/running, digging.
  - Derived metrics (per presentation):
    - Spatial cohesion: mean proportion of individuals within 2 m of stimulus; core vs non-core location assessment; out-foraging group size.
    - Participation in collective defence: mean proportion of individuals acting defensively; context of core region.
    - Homogeneity of behavioral response: mean H-index of behavioral diversity; context of core region.

- Quality control and data integrity
  - Mongoose 2000 app includes internal checks to reduce data errors (e.g., presence required to collect additional data for an individual).
  - Data quality checks via MS Access queries and bespoke R code to detect inconsistencies (e.g., death records).

- Data structure and variables
  - Data stored in three CSV files, each detailing a different aspect of the responses:
    - Mean proportion of individuals within 2 m of the stimulus per presentation.
    - Mean proportion of group members exhibiting defensive behavior per presentation.
    - Mean H-index (behavioral diversity) per presentation.
  - Key fields common across files include:
    - video ID code; focal group ID; stimulus type (intruder vs. control; scents, calls, or both); location (Core vs. Non-core); field.grp.sz (group size out on foraging); stimulus mean proportions (within 2 m or defensively).
  - Specific column descriptions cover qualifier codes for trial type (e.g., t_intruders, c_scents), core vs non-core designation, and mean metrics for each presentation.