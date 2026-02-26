# Sampling regime and collection methods

- Study context
  - Long-term study of a wild banded mongoose (Mungos mungo) population on Mweya Peninsula, Queen Elizabeth National Park, Uganda, with ongoing monitoring since 1995.
  - Population typically 10–12 social groups; individuals uniquely marked for identification; regular trapping every two months; radio collars fitted to 1–2 individuals per group for location; groups habituated to observers.

- Experimental design
  - Five focal groups underwent simulated intrusions (intergroup conflicts) between March 2016 and May 2017.
  - Stimuli included olfactory ( rival faeces/urine/scents ), auditory (rival war cries), and visual (rival males in traps). Each focal group used the same rival group across trials.
  - Control trials used stimuli from the focal group itself (self-origin), with appropriate substitutions (e.g., close calls instead of war cries); four adult males from the focal group were trapped and then reintroduced as a control.
  - Trials: 22 simulated intrusion and 22 control, separated by at least two weeks to prevent habituation.
  - Presentations conducted in a semi-circle around a plastic sheet, with standardized volumes and timings; war cries played back once per clip; rival males from traps presented for a fixed period.
  - Behavioral data collected from video recordings.

- Data collection regime and sampling
  - Focal groups observed and filmed during stimuli presentations (approx. 5 m distance) across multiple sessions per trial.
  - Repeated visits to groups: every 1–3 days for at least 20 minutes per session; daily during pup births for accurate birth dates.
  - Data on group composition, life history, reproduction, and cooperative behavior recorded via field protocols.

- Fieldwork instrumentation
  - Bespoke data app (Mongoose 2000) on Samsung Galaxy tablets for life history data; data downloaded into an MS Access database.
  - Identification via fur marks in adults and dye marks in pups; radio collars (~30 g) with 20 cm whip antennas for location data.
  - Acoustic data: war cries and close calls recorded with H1 Zoom, Sennheiser mic; playback via portable iHome speaker.
  - Visual stimuli captured on Samsung Galaxy tablets or Panasonic video camera; stimuli presentations filmed.

- Calibration and data quality
  - Field instruments calibrated to factory settings; regular quality checks implemented.
  - Data quality control using MS Access queries and bespoke R code; checks to detect inconsistencies (e.g., multiple death records).
  - Observers conducted initial analyses blind to treatment (audio removed during initial coding) to reduce bias; full coding later with audio to timestamp stimuli precisely.

- Analytical methods (data capture and metrics)
  - Behavioral coding at 30-second sampling intervals from videos, beginning after first approach to stimulus until ~3.5 minutes post-approach.
  - Behaviors recorded: stationary, walking/running, digging, standing upright, scent marking, attacking.
  - Derived metrics:
    - Spatial cohesion: mean proportion of group members within 2 m of the stimulus; core vs non-core location recorded.
    - Participation in collective defence: mean proportion acting defensively (standing upright, scent marking, attacking).
    - Homogeneity of behavioural response: mean behavioral diversity (H-index).
  - Each sampling point included counts of foraging group members that could interact with the stimulus and whether the stimulus occurred in core territory.

- Data structure and outputs
  - Data stored as three CSV files, each representing a different summary metric per presentation:
    1) Mean proportion of individuals within 2 m of the stimulus
       - Columns: video, video ID code, grp, focal group ID code, stim, type (c_intruders, c_scents, t_intruders, t_scents), loc (Core/Non-core), field.grp.sz, stim.mean.prop2m
    2) Mean proportion of individuals exhibiting defensive behaviour
       - Columns: video, video ID code, grp, focal group ID code, stim (c_call, c_intruders, c_scents, t_call, t_intruders, t_scents), loc, field.grp.sz, stim.mean.propdef
    3) Mean H-index of behavioural diversity
       - Columns: video, video ID code, grp, focal group ID code, stim (c_call, c_intruders, c_scents, t_call, t_intruders, t_scents), loc, field.grp.sz, avg.h.bystim

- Considerations for data governance and stewardship
  - Data provenance: linkage between raw field records (life history, localization, acoustic/video data) and summarized CSV outputs via consistent identifiers (video codes, group IDs, stimulus types).
  - Metadata and documentation: clear definitions for stimuli types, behavioral categories, core vs non-core locations, and sampling windows; explicit column definitions for each CSV file.
  - Data availability and updates: dataset includes complete trial set (22 intrusion and 22 control) with repeated measures; future updates would require maintaining consistent schema and versioning.
  - Access and privacy: no sensitive personal data; data are observational and tied to animal groups; storage in MS Access with exports to CSV for sharing.
  - Quality assurance: ongoing QA processes via app constraints, database checks, and R-based validation to ensure data integrity before analysis.
  - Reproducibility: detailed methodological notes on stimuli preparation, playback, and behavioral coding facilitate reproducibility and data reuse.