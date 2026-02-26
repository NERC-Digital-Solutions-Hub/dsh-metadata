# Sampling regime and collection methods

- Long-term study of wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda, since 1995.
- Population typically 10–12 social groups; each group ~20 adults plus offspring; individuals uniquely marked for identification; reguar trapping every two months; radio collars fitted to 1–2 individuals per group for location.
- Groups are habituated to observers; groups visited every 1–3 days for at least 20 minutes to record group composition, life history, and reproductive/cooperative behaviours; daily visits during pup birth periods.

Experimental design

- Five focal groups subjected to simulated intrusions (March 2016–May 2017) to mimic intergroup conflict.
- Stimuli for simulated intrusions: rival group faeces, urine, scent marks (olfactory); rival war cries (auditory); rival males in traps (visual).
- Stimuli collected from neighbouring rival group; same rival group used for all trials within a focal group.
- 22 simulated intrusion trials and 22 control trials; trials separated by at least 2 weeks to reduce habituation.
- Control trials used stimuli from the focal group itself (faeces/scents from focal group, close-call vocalisations, and trapped focal males presented back).

Stimulus collection, playback, and presentation

- Stimuli collected fresh on the morning of presentation; standardized volumes and collection from multiple individuals (both sexes, various ages).
- Faeces presented in a semicircle around a plastic sheet along the focal group’s foraging path (07:43–10:27).
- War cries recorded previously; 30-second clips prepared, amplitude normalized to -1 dB, and played back via a portable USB speaker to the focal group. Each clip used once to avoid habituation.
- Rival males trapped, covered during transport to reduce stress, presented to focal group for 5 minutes (16:35–18:18), then returned.
- Timing and sequence of stimuli carefully controlled; control trials mirrored the intrusion trials but with focal-group-origin stimuli.

Fieldwork instrumentation

- Life-history data collected with a bespoke data collection app (Mongoose 2000) on Samsung Galaxy Note 10.1 tablets; data imported to MS Access.
- Individuals wear radio collars (~30 g) with 20 cm whip antennas.
- Acoustic data captured with H1 Zoom recorder and Sennheiser microphone; playback with iHome speaker.
- Presentations filmed with a Samsung Galaxy Note 10.1 or a Panasonic HC-V520 camera.
- Calibration performed to factory settings.

Calibration steps and values

- Field instruments calibrated to factory settings prior to use.

Analytical methods

- Data collected by a single observer from videos; not fully blind due to logistical constraints.
- Bias minimization: initial observations made without audio to hide treatment identity and timing; videos re-watched with sound to record exact call stimulus timing.
- Sampling protocol: scan across video at 30-second intervals starting 30 seconds after the first group member comes within 2 m of the stimulus, continuing until about 3 minutes 30 seconds post-start or video end.
- Inclusion criterion: at least two samples per stimulus type; trials with fewer than two samples excluded.
- Behaviours recorded for each sampling: stationary, walking/running, digging, standing upright, scent marking, attacking.
- Defensive behaviours defined as: standing upright, scent marking, or attacking; non-defensive as stationary, walking/running, digging.
- Derived metrics:
  - Spatial cohesion: mean proportion of group members within 2 m of the stimulus; number of group members foraging who could interact; whether stimulus occurred in the core territory.
  - Participation in collective defence: mean proportion of individuals acting defensively; number foraging who could interact; core territory status.
  - Homogeneity of behavioural response: mean behavioural diversity (H-index) across sampling points; foraging context considerations.

Quality control

- Mongoose 2000 app includes internal checks to reduce data-entry errors (e.g., ensuring marked individuals are present to collect data).
- Data quality checks performed with MS Access queries and bespoke R code to detect inconsistencies (e.g., multiple death records).

Details of data structure

- Data stored in three CSV files with the following content:
  1) Mean proportion of individuals within 2 m of the stimulus (within 2 m metric)
     - Columns: video, video ID code, grp, focal group ID code, stim (c_intruders, c_scents, t_intruders, t_scents), loc (Core or Non-core), field.grp.sz, stim.mean.prop2m.
  2) Mean proportion of group members exhibiting defensive behaviour (defensive propensity)
     - Columns: video, video ID code, grp, focal group ID code, stim (c_call, c_intruders, c_scents, t_call, t_intruders, t_scents), loc, field.grp.sz, stim.mean.propdef.
  3) Mean H-index of behavioural diversity (quality of response)
     - Columns: video, video ID code, grp, focal group ID code, stim (same set as above), loc, field.grp.sz, avg.h.bystim.