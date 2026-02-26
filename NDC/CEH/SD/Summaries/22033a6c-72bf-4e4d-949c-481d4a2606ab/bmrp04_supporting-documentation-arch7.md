# Sampling regime and collection methods

- Overview
  - Study of wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
  - Population includes 10–12 social groups; individuals are uniquely marked for identification; radio collars fitted to 1–2 individuals per group.
  - Groups are regularly observed (visits every 1–3 days; 20 minutes per visit) to record group composition, life history, reproduction, and cooperative behaviour; daily visits during pup births.

- Fieldwork instrumentation
  - Life history data collected with the Mongoose 2000 app on Samsung tablets; data stored in an MS Access database.
  - Radio collars (~30 g) with 20 cm whip antennas; audio recordings of rival war cries and focal group calls (H1 Zoom + Sennheiser mic); playback via portable speaker.
  - Stimuli presented and group behaviour filmed with tablets or video cameras; calibration performed to factory settings.

- Experimental design
  - Five focal groups subjected to simulated intrusions (Mar 2016–May 2017); stimuli include olfactory (faeces, scent marks), auditory (war cries), and visual (rival males in traps).
  - Stimuli collected from neighboring rival groups; identical rival group used per focal group across trials.
  - Procedures: collect fresh faeces/urine/scent marks, present in a semi-circle around focal group path, play back 30 s of rival war cries, then trap and present four rival males to the focal group for ~5 minutes.
  - Control trials mirror intrusion trials but stimuli originate from the focal group (faeces/scents from focal group, close-call calls, and focal group males trapped and presented).
  - Total: 22 simulated intrusion trials and 22 control trials; trials spaced at least 2 weeks apart to avoid habituation.
  - Focal group is filmed during stimulus presentations from ~5 m away.

- Data collection and storage
  - Field data and behavioural observations captured on video; recordings tagged by trial type (intruder vs. control) and stimulus type.
  - Data entries and video logs archived in CSV files (three files) and linked within the MS Access database.

- Analytical methods (GIS-relevant metrics)
  - Behavioural data collected from videos by a single observer; to reduce bias, initial coding is conducted without audio, then re-annotated with sound.
  - Sampling: 30-second interval scans commencing 30 seconds after the first group member comes within 2 m of the stimulus; continue until ~3 minutes 30 seconds or video end.
  - Measures recorded per sampling point:
    - Number of group members within 2 m of the stimulus.
    - Six behaviours: stationary, walking/running, digging, standing upright, scent marking, attacking.
    - Defensive behaviours: standing upright, scent marking, attacking.
  - Derived metrics:
    - Spatial cohesion: mean proportion of individuals within 2 m; foraging group size interacting; whether stimulus occurred in core territory.
    - Participation in collective defence: mean proportion acting defensively; foraging group size interacting; whether stimulus occurred in core territory.
    - Homogeneity of behavioural response: mean behavioural diversity (H-index); foraging group size interacting; whether stimulus occurred in core territory.

- Quality control and data integrity
  - In-app checks (Mongoose 2000) and external QC via MS Access queries and bespoke R code to detect inconsistencies (e.g., repeated death records).

- Data structure and file schema
  - Data stored in three CSV files, each documenting different aspects of the trial responses:
    - File 1: Mean proportion of individuals within 2 m of the stimulus
      - Key columns: video, video ID, grp, focal group ID, stim (trial/stimulus type), loc (Core or Non-core territory), field.grp.sz (group size >6 months on foraging), stim.mean.prop2m (mean proportion within 2 m)
      - Stimulus types include: c_intruders, c_scents, t_intruders, t_scents
    - File 2: Mean proportion of individuals exhibiting defensive behaviour
      - Key columns: video, grp, stim (types include c_call, c_intruders, c_scents, t_call, t_intruders, t_scents), loc, field.grp.sz, stim.mean.propdef
    - File 3: Mean H-index of behavioural diversity
      - Key columns: video, grp, stim (types as above), loc, field.grp.sz, avg.h.bystim

- Spatial/territorial context
  - Territory location is categorized as Core (within the 50% area of activity in the preceding 3 months) or Non-core.
  - Spatial analyses focus on proximity to stimuli, group spatial organization around stimuli, and variation of responses across core vs. non-core areas.