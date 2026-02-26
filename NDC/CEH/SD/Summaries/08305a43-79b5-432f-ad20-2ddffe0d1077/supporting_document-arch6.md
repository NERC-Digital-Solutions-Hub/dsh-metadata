# Collection/generation methods

## Subject, housing, and experimental setup
- 96 three-spined sticklebacks (Gasterosteus aculeatus), 27 ± 2.4 mm, collected from the River Cary, Somerset, UK in Sept 2016; housed in three glass tanks (~50 fish per tank) for 10 months before testing.
- Maintained at 16°C with a 11:13 h light:dark cycle; fed daily with brine shrimp or defrosted bloodworms.
- Experimental arena: oval tank (133.5 cm long × 72 cm wide) with 62 cm high walls; water depth 10 cm; four stimulus holes (3.5 mm diameter) positioned 5 cm above the base.
- Visual stimulus: pipette tip wrapped in red tape to mimic a bloodworm; presented when all eight fish in the group were on the opposite half of the arena.

## Grouping and habituation
- Random block design to form twelve groups of eight fish each; each group included at least two fish from each of the three holding tanks.
- Six-day habituation period in smaller holding tanks with enrichment (PVC tubing and artificial plant).

## Trial scheduling and maintenance
- Trials conducted over four weeks (Mon–Fri) between 31 July and 25 August 2017; groups randomly assigned to two sets of six groups and tested on alternate days (no group tested more than once every two days).
- Post-trial: group returned to holding tank; all groups fed bloodworms in holding tanks after the final trial of the day; ad libitum feeding on weekends.
- Handling: during the first trial week, one fish per three groups replaced with naive individuals due to injury or death; 24 hours to habituate within groups before testing.

## Trial procedure and stimuli presentation
- Each trial begins with eight fish netted to the center; 2 minutes to acclimate.
- Stimulus presented through a randomly chosen wall hole; up to six presentations per trial, with a minimum 3-minute interval between presentations and a total trial duration of 4.2 ± 0.9 minutes.
- Presentations allowed the group to resume normal swimming between stimuli; time between presentations varied with group dynamics.

## Data collection and identity tracking
- Filming: overhead 4K video (3840 × 2178) at 25 frames per second using a Panasonic HC-VX980; camera fixed at 161 cm above water; curtain to diffuse lighting and reduce reflections.
- Data capture: automated 2D tracking to obtain Cartesian coordinates (xi, yi) for each fish i at each time step t; individual identities preserved across trials using software-derived fingerprints.
- File handling: data stored per group per trial; each file represents a single trial for eight fish.

## Data formats, structure, and quality control
- Video converted to MPEG-4 HD; 1 mm ≈ 2.7 pixels.
- Quality control: data provided in raw form; occasional frames where one or more fish could not be tracked are marked as NA.
- Data structure details: 12 groups, each with multiple trial files; mapping of files to groups provided (e.g., Group 1: files 10, 23, 32, 45, 53; Group 12: files 03, 16, 30, 40).
- Coordinate columns: x.1 to x.8 and y.1 to y.8 for eight fish; additional columns labeled x.9 to x.16 correspond to the y coordinates of the eight fish; frame column indicates video frame.

## Metadata, provenance, and related information
- Raw trajectory data allow analysis of group dynamics and individual trajectories; suitable for self-serve data exploration and replication of analyses in collective behaviour studies.
- Related publications: MacGregor et al. 2020 (Nature Communications) and MacGregor & Ioannou (Royal Society Open Science, in press) provide broader context on collective dynamics and group order.

## Reuse considerations
- Data include precise experimental conditions (species, rearing conditions, arena setup, stimulus parameters, timing, and trial schedule) essential for reproducing or reusing the dataset in studies of collective motion.
- Raw trajectory data with NA gaps should be considered in preprocessing steps (e.g., handling missing frames) prior to analysis of group-level metrics.