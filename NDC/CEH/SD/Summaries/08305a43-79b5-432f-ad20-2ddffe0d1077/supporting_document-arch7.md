# Information can explain the dynamics of group order in animal collective behaviour.

## Overview
- A study of collective movement in 96 three-spined sticklebacks (Gasterosteus aculeatus) collected from the River Cary, UK, in 2016.
- Fish were housed and tested in controlled lab conditions to observe group dynamics in a 2D arena.
- Data are raw trajectory coordinates for animals within group trials, suitable for mapping and spatio-temporal analysis.

## Data collection and experimental design
- 96 fish housed in three glass tanks, kept at 16°C and a 11:13 h light:dark cycle to prevent reproduction.
- Random block design: 12 groups of eight fish each, formed to minimize group-level bias (habituation period provided).
- Experimental arena: oval arena with four entry holes for a bloodworm stimulus; goal was to study response to a standardized visual cue.
- Trials: conducted over four weeks (weekdays), with random group assignment to testing days; each trial involved 8 fish per group.
- Stimulus presentation: a pipette-wrapped bloodworm presented through a hole at multiple opportunities per trial, after ensuring the entire group was on the opposite side of the arena.
- Post-trial care: fish returned to holding tanks and fed; some individuals replaced during the first week to maintain habituation.

## Recording and measurement
- Video recording: 4K video at 25 frames per second, captured from above; arena water depth 10 cm, temperature consistent with holding tanks.
- Setup details: central camera position, diffuse overhead lighting to minimize reflections; an opaque curtain reduced disturbances.
- Pixel-to-real-world mapping: 1 mm corresponds to 2.7 pixels in video space.
- Data extraction: automated 2D tracking to obtain Cartesian coordinates (x_i, y_i) for each fish i at each time t.
- Identity tracking: individual fish identities maintained across trials using software-generated fingerprint references.

## Data structure and content
- Each file contains the trajectory data for a single trial of a group of eight fish.
- Grouping and file IDs: 12 groups with multiple trial files (e.g., Group 1 files: 10, 23, 32, 45, 53; many others listed similarly across groups).
- Variables:
  - x.i and y.i: coordinates for fish i (i = 1…8) at each frame.
  - Corresponding pairs: x.1/y.1 for fish 1, x.2/y.2 for fish 2, …, x.8/y.8 for fish 8.
  - frame: frame number in the video.
- Data quality:
  - Data are provided in raw form; occasional untracked fish are indicated as NA in the data files.
  - Identity retention across trials relies on initial fingerprinting for each group.

## Spatial and temporal characteristics
- Temporal span: each trial lasts approximately 4.2 ± 0.9 minutes, with six stimulus presentations per trial.
- Spatial context: coordinates are within the experiment arena; no real-world geographic coordinates are provided—coordinates map to arena space.
- Spatial resolution: derived from video resolution and the 1 mm = 2.7-pixel conversion, enabling movement metrics within the arena scale.

## Relevance to GIS and data visualization
- Provides rich 2D trajectory data suitable for GIS-based visualization and analysis of movement patterns, spatial cohesion, and group dynamics.
- Enables creation of:
  - Trajectory animations in a defined 2D space (arena coordinates).
  - Computation of spatial metrics (e.g., inter-fish distances, group centroid, area coverage).
  - Temporal analyses of movement responses to stimuli (time series of positions per fish and per group).
- Preparation steps for GIS:
  - Convert arena coordinates into a consistent coordinate system with units in millimeters (using 1 mm = 2.7 pixels as needed).
  - Aggregate per-frame coordinates into time-indexed features (e.g., centroid position, polarization, nearest-neighbor distances).
  - Handle missing data by marking NA where tracking failed.

## Limitations and considerations
- Coordinates are relative to a controlled arena; external validity to natural habitats may require contextual interpretation.
- Data are raw trajectories; additional processing is required to derive higher-level GIS metrics.
- Group-level analyses require careful handling of group membership and trial-level identifiers.

## References and further information
- MacGregor, H.E.A., Herbert-Read, J.E., & Ioannou, C.C. Information can explain the dynamics of group order in animal collective behaviour. Nature Communications 11, 2737 (2020). https://doi.org/10.1038/s41467-020-16578-x
- MacGregor, H.E.A. & Ioannou, C.C. Collective motion diminishes, but variation between groups emerges, through time in fish shoals. Royal Society Open Science. In press.