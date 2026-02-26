# Collection/generation methods

- Study and subjects: 96 three-spined sticklebacks (Gasterosteus aculeatus), ~27 ± 2.4 mm, collected from the River Cary, Somerset, UK in Sept 2016; housed in a controlled lab setting for 10 months to prevent reproduction.

- Experimental design and group assignment:
  - Random block design: 96 fish divided into twelve groups of eight, with careful cross-sourcing from holding tanks to balance group composition.
  - Habituation: groups held in smaller tanks for six days with enrichment (PVC tubing, artificial plant) before testing.

- Arena and environmental controls:
  - Oval arena with four stimulus entry holes.
  - Water kept at 16°C, 10 cm depth; light/dark cycle aligned to maintain non-reproductive condition.
  - Overhead camera setup for high-resolution video; curtain to reduce disturbances and reflections.

- Stimulus and trial protocol:
  - Visual bloodworm stimulus delivered via a pipette tip (red-taped for visibility) through a randomly chosen hole.
  - Trials: 8 fish per trial, acclimation period of 2 minutes, then up to six stimulus presentations per trial (mean ~4.2 minutes), separated by at least 3 minutes to allow normal swimming in between.
  - Presentation timing varied to ensure the entire group was opposite the stimulus location at presentation.

- Trial schedule and group rotation:
  - Trials conducted 31 July–25 August 2017, Monday–Friday over four weeks.
  - Groups divided into two sets and tested on alternate days; each group tested no more than once every two days.
  - Post-trial feeding: all groups fed bloodworms after daily testing; ad libitum on weekends.
  - Minor replacements: during the first week, one fish per three groups replaced with naive individuals to maintain experimental integrity.

- Data collection and tracking:
  - Video capture: 4K video (3840 × 2178) at 25 fps, camera positioned above the arena.
  - Data capture: automated 2D tracking to obtain x and y coordinates (cartesian positions) for each of the eight fish per frame; identity maintained across trials using software-generated fingerprints.
  - Data format: raw video converted to MPEG-4; coordinates stored per fish per time step; missing data marked as NA when a fish cannot be tracked in a frame.
  - Spatial calibration: 1 mm ≈ 2.7 pixels (recorded for analysis reference).

- Data structure and file organization:
  - Each file contains data for one group during a single trial.
  - Files are grouped by trial and group (e.g., Group 1, Group 2, etc.), with explicit mapping of fish coordinates (x.i, y.i for fish i = 1–8) and frame numbers.
  - Tracking identifiers reused across trials to maintain individual identity across the experiment.

- Quality control and data notes:
  - Data are provided in raw form; occasional untracked frames are noted with NA.
  - Some minor data gaps due to tracking limitations; provenance and handling of missing data are documented in the data files.

- Additional information and references:
  - Related methodological and theoretical context provided in MacGregor et al. and Ioannou’s work on collective behaviour and group dynamics.