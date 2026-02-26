# Sampling regime and collection methods

- Study context
  - Wild banded mongoose population on Mweya Peninsula, Queen Elizabeth National Park, Uganda, studied since 1995.
  - Groups typically 10–12, ~20 adults plus offspring; individuals uniquely marked for identification.
  - Regular trapping every two months; radio collars fitted to 1–2 individuals per group; observers habituated to allow close approaches.
  - Behavioral and life-history data collected through field observations and recordings; daily observations during pregnancy for pup birth dating.

- Experimental design
  - Five focal groups subjected to simulated intrusions (March 2016–May 2017) to mimic intergroup conflict.
  - Stimuli included rival faeces and scent marks (olfactory), rival war cries (auditory), and rival males in traps (visual).
  - Stimuli sourced from a neighboring rival group; same rival group used for all trials within a focal group.
  - Intermixed with control trials using same-type stimuli from focal group itself (replacing intruder stimuli with focal-group cues and close-call vocalizations; four focal-group males trapped and presented as control).
  - 22 simulated intrusion trials and 22 control trials; minimum 2-week interval between trials to limit habituation.
  - Trials video-recorded from about 5 m away to minimize disturbance.

- Stimuli collection and presentation protocol
  - Rival faeces, urine, and scent marks collected in the morning; standardized presentation around a plastic sheet to encourage marking.
  - Faeces samples consistently sized (100 × 137 mm) and presented in a semi-circle around the sheet along the foraging path.
  - War cries recorded from rival group and edited into 30-second clips with standardized amplitude; playback via a portable speaker.
  - Rival males trapped, transported to the presentation site for 5 minutes, then returned; same timing and sequence used for intrusion trials.

- Data capture and fieldwork instrumentation
  - Life-history data collected with the bespoke Mongoose 2000 app on Samsung Galaxy tablets; data downloaded into an MS Access database.
  - Individuals equipped with ~30 g radio collars (20 cm whip antenna).
  - War cries and close calls recorded with an H1 Zoom recorder and Sennheiser microphone; playback through an iHome speaker.
  - Stimulus presentations filmed with tablets or a Panasonic video camera.
  - Calibration of field instruments aligned with factory settings.

- Analytical methods
  - Behavioral data coded from videos by a single observer; limited blinding to treatment due to logistical constraints, mitigated by initial audio-free observations and subsequent re-review with sound.
  - Sampling strategy: 30-second intervals, starting 30 seconds after first individual within 2 m of the stimulus, continuing for ~3.5 minutes; require at least two samples per stimulus type per trial.
  - Recorded measures per sampling point: number of group members within 2 m; behaviors (stationary, walking/running, digging, standing upright, scent marking, attacking).
  - Derived classifications: defensively acting (standing upright, scent marking, attacking) vs. non-defensively (stationary, walking/running, digging).
  - Key metrics:
    - Spatial cohesion: mean proportion within 2 m; consider foraging group size and whether stimulus occurred in the core territory.
    - Participation in collective defence: mean proportion acting defensively; plus context variables.
    - Homogeneity of behavioural response: mean behavioural diversity (H-index) across sampling points; plus context variables.

- Quality control and data validation
  - Mongoose 2000 app includes internal checks to minimize data-entry errors (e.g., presence checks linked to death records).
  - Data validation performed via MS Access queries and bespoke R code to detect inconsistencies.

- Data structure and content
  - Data organized into three CSV files.

  - File 1: Mean proportion of individuals within 2 m of the stimulus
    - Key columns: video, video ID, grp (focal group), stim (trial/type; e.g., c_intruders, t_intruders, c_scents, t_scents), loc (Core vs Non-core), field.grp.sz (group size on foraging), stim.mean.prop2m (mean proportion within 2 m).

  - File 2: Mean proportion of group members exhibiting defensive behaviour
    - Key columns: video, grp, stim (e.g., c_call, c_intruders, c_scents, t_call, t_intruders, t_scents), loc, field.grp.sz, stim.mean.propdef (mean proportion defending).

  - File 3: Mean H-index of behavioural diversity
    - Key columns: video, grp, stim (as above), loc, field.grp.sz, avg.h.bystim (mean H-index by stimulus).

- Overall aim aligned with data support
  - Creates accessible, analyzable datasets describing spatial dynamics, defensive participation, and behavioural diversity in response to intruder vs. control stimuli.
  - Enables downstream data products and self-serve analyses for end users interested in primate social dynamics, intergroup competition, and behavioural responses.