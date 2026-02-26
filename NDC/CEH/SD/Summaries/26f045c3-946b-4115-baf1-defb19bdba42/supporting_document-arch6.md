# Collection/generation methods

- Study subject and setup
  - Fish: mean body length 43 ± 3.2 mm; collected from River Cary, Somerset, UK.
  - Housing: two large glass aquaria for 8 months; water at 14°C; 11:13 hour light/dark cycle; fed defrosted bloodworm after experimental trials.
  - Testing period: 23 Sept 2019 – 11 Mar 2020; groups of six tested over two consecutive days; 31 groups in total.
  - Arena: white opaque circular arena (diameter 97 cm, water depth 10 cm) inside a square Perspex tank, diffused light, filmed from above.

- Experimental design and trial structure
  - Day 1 (individual and group context): six fish from the same holding aquarium allocated to a group; filmed individually in an open arena after a 1-minute viewing period in an acetate cylinder; then free-swim for 10 minutes; group confinement in a central chamber overnight.
  - Day 2 (group context for foraging): group shoaling observed for 20 minutes; then group foraging trials with a green stimulus (pipette tip) appearing unpredictably from four holes; two boodworms provided as rewards upon approach; trial ends when both boodworms are not consumed within 5 minutes.
  - Reuse and timing: groups housed together overnight and not reused after testing; up to two groups tested per week.

- Data collection and recording
  - Video capture: arena filmed with a SONY Handycam 4K and a GoPro Hero5; setup includes external monitors for observation; 25 fps recording; 3840 × 2160 resolution for primary footage.
  - Data generated: trajectory data for each fish (x_i, y_i) at each time step t; identity tracked across trials using idTracker; central chamber used to assist tracking for group and individual phases.
  - File handling: videos converted to MPEG-4 HD; 1 mm = 1.05 pixels.

- Data processing and tracking
  - Tracking: automated two-dimensional tracking to produce per-fish Cartesian coordinates (x_i, y_i) at each frame.
  - Identity management: reused fingerprint references from idTracker across shoaling and foraging trials to maintain individual identities; for individual tests, tracking adjusted after including/excluding the central chamber to improve quality.
  - Data products: raw trajectory data per trial, enabling analyses of individual, shoaling, and group foraging behaviors.

- Quality control and data integrity
  - Data are provided in raw form; occasional NA entries where a fish could not be tracked in a frame.
  - Notable data issues: some trials with no movement (listed as specific file IDs); two video files corrupted (unrecoverable trajectory data).
  - Documentation of issues: NA markers indicate missing tracking; corrupted files noted within data files.

- Data structure and file descriptions
  - Data file: n_n2.txt
    - X1, Y1 coordinates for fish 1, 2, etc., with frame indexing.
  - Data file: n_shoal.txt
    - Trajectories for six fish: trajectories.1..6 correspond to x coordinates; trajectories.7..12 correspond to y coordinates; frame index included.
  - Data file: n_forage.txt
    - Trajectories for six fish similar to n_shoal.txt; includes x and y coordinates per fish, plus frame index.
  - Notes on structure: each file maps per-frame positions to each fish in the group context (shoal and forage) or per individual in the singlefish assays; frames align with video timing.

- Temporal and experimental details
  - Trials span multiple days with consistent group composition across days for each group.
  - Foraging trials include multiple stimulus presentations with a minimum 3-minute interval between presentations.

- Data usage considerations for researchers
  - The dataset is raw trajectory data suitable for analyses of movement patterns, shoaling dynamics, and foraging responses.
  - Researchers should account for occasional missing data (NA) and potential corrupted videos when performing analyses.
  - Reidentification across trials is supported via idTracker-based identities to enable longitudinal or cross-condition analyses within the same group.