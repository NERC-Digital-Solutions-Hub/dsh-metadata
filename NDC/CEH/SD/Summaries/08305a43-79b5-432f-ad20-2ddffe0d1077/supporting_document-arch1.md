# Information can explain the dynamics of group order in animal collective behaviour

- Purpose and scope
  - Describes collection, experimental design, data collection, and data structure for a study of how groups of fish exhibit collective dynamics in response to a simulated prey stimulus.
  - Subjects: 96 three-spined sticklebacks (Gasterosteus aculeatus), ~27 ± 2.4 mm, from the river Cary, Somerset, UK.
  - Groups: 12 groups of 8 fish each, assembled to balance representation from three holding tanks; random block design to minimize group-level bias.

- Experimental setup and husbandry
  - Pre-experiment housing: three glass tanks (~50 fish per tank) for 10 months; temperature 16°C; photoperiod 11:13 h light:dark to prevent reproductive condition.
  - Feeding: brine shrimp or defrosted bloodworms; daily during housing; ad libitum after trials.
  - Habituation: 6 days in smaller holding tanks with enrichment (PVC tubing, artificial plant).

- Trial arena and stimulus
  - Arena: oval arena, 133.5 cm by 72 cm with 62 cm high walls; four 3.5 mm holes in the wall for stimulus presentation.
  - Stimulus: a bloodworm-like visual cue—pipette tip wrapped in red tape (17 mm long, 3 mm diameter)—presented when the group is on the opposite side of the arena to the stimulus hole.
  - Presentation protocol: up to six presentations per trial, with a minimum 3-minute interval between presentations; total trial duration 4.2 ± 0.9 minutes.
  - Video capture: overhead 4K camera (25 fps), 161 cm above water, 10 cm water depth; curtain to reduce disturbances and reflections.

- Experimental schedule and randomization
  - Timing: trials conducted Monday–Friday over four weeks (31 July–25 August 2017); groups tested in two sets of six on alternate days; no group tested more than once every two days.
  - Acclimation: 2 minutes before each trial start; randomization of group order within each day.
  - Group composition: each group included at least two fish from each of the three holding tanks.

- Data collection and processing
  - Video processing: footage converted to MPEG-4; pixel-to-length conversion: 1 mm = 2.7 pixels.
  - Tracking: automated 2D tracking to obtain x and y coordinates for each fish (eight individuals per group) at each time step; identities maintained across trials via fingerprint references.
  - Raw data: presented in raw form; any untracked fish frames marked as NA.
  - Data scope: trajectory data for eight fish per group per trial; corresponding dataset metadata included in the files.

- Data structure and content
  - File organization: each file contains data for a single group during a single trial.
  - Group and file mapping: groups 1–12 with specified file identifiers; columns include x and y coordinates for each fish (x.1, y.1, x.2, y.2, ..., x.8, y.8) and a frame indicator (frame).
  - Data details: explicit mapping of fish identities within a group across trials using the initial fingerprinting references.

- Quality control and limitations
  - Data are raw; occasional frames where one or more fish cannot be tracked are indicated as NA.
  - Tracking fidelity relies on automated software with occasional data gaps; considerations needed for missing data during analysis.

- Related works and further information
  - Core methodology and data underpinning the study: MacGregor, H.E.A., Herbert-Read, J.E., & Ioannou, C.C. Information can explain the dynamics of group order in animal collective behaviour. Nature Communications 11, 2737 (2020). DOI: https://doi.org/10.1038/s41467-020-16578-x
  - Additional on group dynamics in fish shoals: MacGregor, H.E.A. & Ioannou, C.C. Collective motion diminishes, but variation between groups emerges, through time in fish shoals. Royal Society Open Science. In press.