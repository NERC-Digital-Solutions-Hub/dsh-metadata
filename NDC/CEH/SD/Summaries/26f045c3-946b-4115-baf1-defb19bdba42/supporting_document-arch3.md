# Collection/generation methods

- Study subjects and conditions
  - Fish (mean ± SD length 43 ± 3.2 mm) sourced from the River Cary, Somerset, UK.
  - Held in two large glass aquaria for 8 months before testing; water at 14°C with an 11:13 hour light/dark cycle.
  - Feeding: defrosted frozen bloodworm, given after experimental trials.
  - Timeline: experiments conducted between 23 September 2019 and 11 March 2020; 31 groups tested in total (groups of six individuals each).

- Experimental arena and procedures
  - Trials conducted in a white, opaque circular arena (diameter 97 cm; water depth 10 cm) within a square Perspex tank; external curtain minimized disturbances and diffused light.
  - Groups: up to two groups tested per week; fish not reused after testing.
  - Day 1: six fish from the same holding aquarium allocated to a group and filmed individually while swimming in the group.
  - Day 2: fish filmed as a group during a foraging task.
  - Group formation: fish housed in a central chamber overnight; chamber removed prior to group foraging.

- Behavioral assays
  - Individual behavioral assays (n_n2): fish placed in a transparent acetate cylinder (8 cm Ø, 25 cm height) for 1 minute to view the arena; released to swim for 10 minutes and video recorded.
  - Shoaling trial (n_shoal): all six fish in the group observed for 20 minutes after initial setup.
  - Group foraging trials (n_forage): six fish allowed 5 minutes to habituate; presented with a green stimulus (pipette tip) from four holes; two bloodworms provided as rewards upon approach; stimulus presented at least every 3 minutes; trial ends if both bloodworms are not consumed within 5 minutes.

- Recording and equipment
  - Video capture: Sony Handycam FDR-AX33 4K and GoPro Hero5 mounted above the arena; footage viewed on two external monitors.
  - Recording details: arena filmed from 156 cm height; resolution 3840×2160; 25 frames per second.
  - Group allocation and testing cadence: up to two groups per week; 31 groups tested in total.

- Data processing and tracking
  - Video data converted to MPEG-4 HD; 1 mm ≈ 1.05 pixels.
  - Trajectory extraction: automated 2D tracking to yield Cartesian coordinates (x_i, y_i) for each fish i at each time t.
  - Identity maintenance: reused individual fingerprints from idTracker across shoaling and foraging trials to track the same fish; individual tests re-tracked to improve quality by excluding central chamber data.
  - Raw data handling: all data are raw; any untracked frames marked as NA; some trials had periods of no movement or corrupted video files (noted in the data).

- Data structure and files
  - Data file n_n2.txt: x and y coordinates with descriptive labeling.
  - Data file n_shoal.txt: trajectories for six fish (trajectories.1–6 for x, trajectories.7–12 for y) plus frame information.
  - Data file n_forage.txt: trajectories for six fish in the foraging trials (x and y coordinates) plus frame information.
  - Notes on data units and file structure provided to aid interpretation and reuse.