# Collection/generation methods

## Subjects and sampling
- Fish collected from the River Cary, Somerset, UK (grid reference ST 469 303).
- Mean body length 43 ± 3.2 mm at testing.
- Maintained in two large glass aquaria for 8 months prior to testing; water temperature 14°C; 11:13 hour day/night photoperiod.
- Fed daily with defrosted frozen bloodworm, after experimental testing days.
- Experiments conducted between 23 September 2019 and 11 March 2020.
- Groups of six fish tested per trial; up to two groups per week; 31 groups tested in total.

## Experimental setup
- White opaque circular arena: diameter 97 cm, water depth 10 cm.
- Arena housed inside a square white Perspex tank (100 L × 100 W × 40 H cm) with a wooden frame and covered by a white opaque curtain to minimize disturbances and diffuse light.
- Filming: two cameras - a SONY Handycam FDR-AX33 (4K) mounted 156 cm above the water (3840 × 2160 px, 25 fps) and a GoPro Hero5 with linear FOV connected to two external monitors.
- Group allocation: on day 1, six fish from the same holding aquarium allocated to a group by stratified random sampling; fish filmed individually and then as a group.
- Day 2: the same six fish filmed as a group during a foraging task.
- Fish housed in groups overnight and not reused after testing.

## Behavioral assays

### Individual behavioural assays
- Each fish transferred to a transparent acetate cylinder (8 cm Ø × 25 cm height) for 1 minute to view the arena, then released to swim for 10 minutes with video recording.
  
### Shoaling (group) trials
- Immediately after the individual test, all six fish in the group placed in a central chamber for two minutes.
- Chamber lifted and group allowed to swim freely for 20 minutes; shoaling behavior recorded.

## Group foraging trials
- All six fish in the group netted into the arena and allowed 5 minutes to habituate.
- Green stimulus: pipette tip (1 cm long, 3.5 mm diameter) wrapped in green tape, appearing unpredictably from one of four equally spaced holes (4 mm Ø) in the arena wall.
- Upon approach within 10 cm of the stimulus, two bloodworms pipetted into the arena as rewards.
- Stimulus held for 15 seconds after bloodworms released; presented at least every 3 minutes, with fish on opposite side of the selected hole between presentations.
- Trial ends when both bloodworms are not consumed within 5 minutes (fish deemed satiated).

## Data collection and processing
- Videos converted to MPEG-4 HD; 1 mm ≈ 1.05 pixels.
- Automated two-dimensional tracking used to generate Cartesian coordinates (x_i, y_i) for each fish i at each time step t.
- Identity maintenance across trials: idTracker fingerprints from the shoaling trial reused to process the foraging trial.
- For individual assays, central chamber tracking included; subsequent re-tracking excluding the central chamber to improve individual-tracking quality.

## Data quality and file structure
- Data provided in raw form; NA used where a fish could not be tracked in a frame.
- Some trials had no movement (specific file IDs noted) and some video files were corrupted.
- Data files:
  - Data structure n_n2.txt: x and y coordinates (X1, Y1… descriptions).
  - Data structure n_shoal.txt: trajectories for six fish (trajectories.1 to trajectories.6 for x coordinates; trajectories.7 to trajectories.12 for y coordinates) plus frame information.
  - Data structure n_forage.txt: trajectories for six fish (trajectories.1 to trajectories.6 for x coordinates; trajectories.7 to trajectories.12 for y coordinates) plus frame information.