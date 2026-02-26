# Collection/generation methods

- Study subject and origin
  - Three-spined sticklebacks (Gasterosteus aculeatus), 96 individuals collected from the River Cary, Somerset, UK in September 2016.
  - Environmentally controlled laboratory setting at the University of Bristol; ambient temperature 16°C; 11:13 h light:dark photoperiod to prevent reproduction.

- Experimental design and grouping
  - 96 fish randomly assigned into twelve groups of eight using a complete random block design to balance group composition.
  - A six-day habituation period in smaller holding tanks prior to testing; enrichment provided (PVC tubing, artificial plant).

- Trials and setup
  - Trials conducted in an oval arena with four potential food-stimulus holes; 10 cm water depth; 4K overhead video recording at 25 frames per second.
  - Bloodworm visual stimulus presented via a standardized pipette tip at random hole positions; each trial allowed up to six stimulus presentations with a minimum 3-minute interval between presentations.
  - Trials run Monday–Friday over four weeks (31 July–25 August 2017); groups tested on alternate days to avoid repeat testing within two days.

- Data collection and processing
  - Video captured from directly above; footage converted to MPEG-4 HD (1920 × 1080).
  - Trajectory data extracted for each fish to obtain Cartesian coordinates (x_i, y_i) at each time step using automated 2D tracking software.
  - Individual fish identities preserved across trials by reusing fingerprint references from the initial trial per group.
  - 1 mm to pixel conversion noted (1 mm = 2.7 pixels) to relate coordinates to physical space.

- Data packaging and file structure
  - Each file contains data for a single group during a single trial, comprising eight fish trajectories.
  - Group and file organization:
    - Group 1: files 10, 23, 32, 45, 53
    - Group 2: files 02, 15, 29, 39, 51, 62, 69, 80, 87, 97, 111
    - Group 3: files 09, 20, 35, 43, 54, 60, 72
    - Group 4: files 01, 17, 26
    - Group 5: files 08, 22, 33, 44, 55
    - Group 6: files 06, 13, 28, 34, 42, 57, 59, 71, 81, 90, 99, 108
    - Group 7: files 07, 21, 36
    - Group 8: files 05, 18, 27, 38, 50, 63, 73, 84
    - Group 9: files 11, 19, 31, 46, 56, 64, 76, 89
    - Group 10: files 12, 24, 41, 52, 83, 91, 96, 110
    - Group 11: files 04, 14, 25, 37, 49, 61, 74, 82, 94, 105
    - Group 12: files 03, 16, 30, 40
  - Data columns encode coordinates as x.i and y.i for each fish i (1–8), plus a frame column; i.e., x.1, y.1, ..., x.8, y.8, frame.
  - NA values indicate frames where one or more fish could not be tracked.

- Data content scope
  - Raw trajectory data for eight fish per trial; no derived behavioral metrics are included in the raw files.
  - Documentation notes include the order of fish identities and the reuse of fingerprints across trials to maintain identity tracking.

- Quality control and limitations
  - Data are provided in raw form; occasional frames with untracked fish are indicated as NA.
  - Experimental details include occasional replacement of one individual per three groups during the first week, with a 24-hour habituation period prior to testing for replacements.

- Documentation and references
  - Processing details: video-to-MPEG-4 conversion; 2D tracking software used for coordinate extraction; Handbrake version 1.0.7 referenced for video processing.
  - Related literature available: MacGregor, Herbert-Read, and Ioannou (Nature Communications 2020) and MacGregor & Ioannou (in press) provide context on collective dynamics and temporal variation in group order.

- Data governance and reuse considerations
  - Provenance and experimental context are captured (species, collection site/date, housing, arena setup, stimuli, trial timing, and group assignment).
  - Clear data structure with per-trial, per-group files supports dataset discoverability and re-use, though the data are specific to this single experimental paradigm.
  - To facilitate reuse, consider adding a formal data dictionary, a metadata schema (including units, coordinate reference frame, and observer notes), and access/reuse terms (license) if sharing beyond the current repository.