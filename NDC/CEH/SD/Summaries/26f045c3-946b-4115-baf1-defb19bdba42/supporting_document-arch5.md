# Collection/generation methods

## Overview
- Describes experimental collection, housing, and behavioral testing of fish (mean length 43 ± 3.2 mm) conducted in the UK.
- Aims to generate raw trajectory data for individual and group behaviors across shoaling and foraging contexts, with detailed recording and post-processing steps.

## Subjects and housing
- Fish caught from the River Cary, Somerset, UK; housed in two large glass aquaria (70 cm L × 45 cm W × 37.5 cm H) for 8 months before testing.
- Environmental conditions: 14°C water, 11:13 hour day/night photoperiod; fed daily with defrosted frozen bloodworm after testing.
- Experimental window: 23 September 2019 to 11 March 2020.
- Grouping: six fish per group; 31 groups tested over two consecutive days; fish not reused across trials.

## Experimental setup and filming
- Arena: white opaque circular arena (97 cm diameter, 61 cm high) in a square Perspex tank (100 × 100 × 40 cm) with a white curtain to minimize disturbances.
- Recording: filmed from above by a SONY Handycam 4K camera (3840 × 2160; 25 fps) and a GoPro Hero5 (linear FOV), with external monitors for observation.
- Trial schedule: up to two groups per week; 31 groups total.

## Trial design and tasks
- Day 1 (individual): six fish per group filmed individually within an arena after placement in a central central chamber; each fish is observed for 10 minutes of free swimming following a 1-minute viewing period in an acetate cylinder.
- Day 2 (group): all six fish released as a group; two-minute central chamber containment before release; 20-minute shoaling observation.
- Group foraging trials (n_forage): after 5-minute habituation, groups encounter a green stimulus (pipette tip) appearing from four holes; two bloodworms provided as rewards per presentation if consumed within 5 minutes; minimum 3-minute intervals between stimuli; trial ends when the worms are not consumed.

## Data collection and processing
- Data capture: videos converted to MPEG-4 HD (1920 × 1080) using Handbrake v1.0.7; 1 mm corresponds to 1.05 pixels.
- Trajectory extraction: automated 2D tracking yields Cartesian coordinates (x_i, y_i) for each fish at each time step.
- Individual identity tracking: idTracker used to generate fingerprint references; for foraging trials, fingerprint references from shoaling trials reused to maintain individual identities; for individual assays, central chamber data included during tracking to establish identities, then re-tracked excluding the central chamber to improve quality.

## Data formats and structure
- Data are stored in raw form with explicit NA entries where tracking failed.
- Files:
  - Data structure n_n2.txt: x coordinate (X1) and y coordinate (Y1) with descriptions.
  - Data structure n_shoal.txt: trajectories for six fish (trajectories.1 to trajectories.12 for x and y coordinates) plus frame data.
  - Data structure n_forage.txt: trajectories similarly organized for the six fish and frame data, with coordinates split across multiple fields (trajectories.1…12 and frame).

## Quality control and limitations
- Data are presented in raw form; some frames unavailable (NA) due to tracking failures.
- Failures: four cases where individual fish did not move (files: 3_3, 21_5, 22_4, 24_5); two corrupted video files (files: 17_4, 17_5) with no trajectory data.
- No further processing beyond initial tracking and data extraction; limitations documented for downstream use.

## Data stewardship considerations
- Documentation includes detailed experimental conditions, timelines, and tracking methods to support reproducibility.
- Use of idTracker fingerprints enables re-identification of individuals across related trials; ensure metadata records linkage between shoaling and foraging datasets.
- Data are raw; for reuse, clear provenance and processing parameters (camera setup, frame rate, resolution, tracking software versions) should be captured in metadata.
- Consider adding a formal data dictionary and versioning, given the explicit file structures and tracking conventions, to support discoverability and interoperability.