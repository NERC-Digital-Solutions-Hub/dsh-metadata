# Behavioral assays and data collection methods for group foraging and shoaling in fish from River Cary, Somerset, UK

- Purpose
  - Document collection, handling, and analysis methods for behavioural assays to assess individual, shoaling, and group foraging behaviours in fish, with an emphasis on standardized data suitable for monitoring environmental health and policy performance over time.

- Experimental subjects and housing
  - Fish collected from the River Cary, Somerset, UK.
  - Mean body length at testing: 43 ± 3.2 mm.
  - Held in two large glass aquaria (70 cm × 45 cm × 37.5 cm) for 8 months.
  - Water temperature: 14°C; photoperiod: 11 hours light / 13 hours dark.
  - Feeding: defrosted frozen bloodworm daily after testing days.

- Experimental design and timeline
  - Trials conducted between 23 September 2019 and 11 March 2020.
  - Groups: six fish per group; up to two groups tested per week; 31 groups in total.
  - Day 1: individual testing followed by 2-minute central-group interaction in arena.
  - Day 2: group foraging trials in the same groups.
  - Group assignments: fish allocated by random sampling across holding aquaria; fish not reused after testing.
  - Arena: white opaque circular arena (97 cm diameter, 61 cm height, water depth 10 cm) within a white Perspex tank; curtain to diffuse light and reduce disturbances.
  - Recording setup: overhead filming using a Sony Handycam (4K) and GoPro Hero5 connected to external monitors for observer viewing.

- Experimental procedures
  - Individual assays: fish placed in a transparent acetate cylinder for 1 minute to view arena, then released for 10 minutes of free swimming; behavior video-recorded.
  - Post-individual pause: all six group members placed in a central chamber for 2 minutes, then released to swim freely for shoaling observation (20 minutes).
  - Group foraging trials: six fish released into arena, allowed 5 minutes to habituate; then the group is presented with a green stimulus (pipette tip) from four holes in the arena wall. Upon approach within 10 cm, two bloodworms are added as rewards and the stimulus remains for 15 seconds; stimulus is repeated at least three-minute intervals. Trial ends when either bloodworm is not consumed within 5 minutes, indicating satiation.

- Recording and data collection
  - Video data collected from two angles/cameras; high-resolution digital footage (HD to 4K as recorded).
  - Trajectory data extracted per fish from video using automated 2D tracking to obtain (x_i, y_i) coordinates at each time step.
  - Individual identities tracked across trials using idTracker, with consistent re-identification between shoaling and foraging trials for the same group.

- Data processing and file structures
  - Data are stored in raw form; some frames may contain NA where tracking failed.
  - File: n_n2.txt
    - x coordinate (X1) and y coordinate (Y1) for individuals.
  - File: n_shoal.txt
    - Trajectories for six fish: trajectories.1…trajectories.6 (x coordinates); trajectories.7…trajectories.12 (y coordinates); frame.
  - File: n_forage.txt
    - Trajectories for six fish: trajectories.1…trajectories.6 (x coordinates); trajectories.7…trajectories.12 (y coordinates); frame.
  - Data quality notes
    - Some trials contain NA entries where a fish could not be tracked.
    - Four instances where a fish did not move during a trial.
    - Two video files (17_4, 17_5) were corrupted and could not be analyzed.
  - Data preparation details
    - Videos converted to MPEG-4 HD; spatial scale: 1 mm ≈ 1.05 pixels.
    - Tracking yields Cartesian coordinates for each fish per time step, enabling subsequent analyses of movement, proximity, and shoaling/foraging behaviors.

- Quality control and considerations for environmental monitoring
  - Data are raw and include occasional gaps, highlighting the importance of documenting missing data for transparency.
  - Standardized experimental conditions (temperature, photoperiod, arena dimensions, and procedure) support comparability across datasets and over time.
  - The combination of individual, shoal, and group foraging measures provides a multi-faceted behavioural profile that can be linked to environmental factors and policy-relevant monitoring programs.