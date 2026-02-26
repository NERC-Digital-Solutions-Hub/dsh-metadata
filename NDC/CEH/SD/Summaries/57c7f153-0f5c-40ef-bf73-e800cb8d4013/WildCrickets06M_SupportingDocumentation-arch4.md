# SUPPORTING DOCUMENTATION: Trade-off between reproduction and body maintenance in a wild field cricket ( Gryllus campestris ) population

- Context and study site
  - WildCrickets field site in Asturias, North Spain, near the Atlantic, in a river valley; meadow of about 20,000 m2 with surrounding meadows, orchards, and patches of eucalyptus, chestnut, and oak.
  - Population resides in a meadow on the northwest slope adjacent to an old riverbed and near a railway line; 800 m2 inhabited by Gryllus campestris.
  - Long-term monitoring: 12 consecutive years with consistent meadow management (mowing in mid-March and July-August; grass kept short August–March).

- Population and ecology
  - Flightless, univoltine field cricket; overwinter as late instar nymphs; adults emerge in spring; eggs laid from May; last adults die by end of June/early July.
  - Crickets occupy burrows in the flat meadow area; prefer sun-exposed areas; limited migration due to surrounding shade and roads.
  - Population dynamics observed through a fixed meadow area, with more burrows than crickets and more crickets than cameras.

- Sampling regime and data collection over time
  - Each individual trapped a few days after adult emergence using a purpose-built device; weighed (±0.01 g), photographed, and marked with a unique PVC tag on the pronotum (1–2 character code) for identification via video.
  - Biological samples collected per individual: cuticular hydrocarbons, a small haemolymph sample, and a small piece of hind leg tip for pheromone/DNA profiling.
  - Imaging and surveillance: installation of 64–140 infrared day/night cameras around burrows before late April; continuous recording around burrow entrances.
  - Video and field data are integrated with a weather station (Davis Vantage Pro2) logging variables every 10 minutes, plus seven additional sensors in artificial burrows around the meadow.

- Data infrastructure, calibration, and storage
  - Instruments are factory calibrated.
  - Video data are captured via a DVR system and stored on multiple computers; camera allocation is dynamic to maximize information per burrow.
  - Data extraction and storage: two-step per-day video processing; initial broad pass to identify burrow use, followed by detailed viewing of selected cameras; data entered into MS Access database for processing.
  - Quality control: data integrity checks to detect inconsistencies (e.g., same cricket recorded at two different burrows simultaneously); data are only used after passing consistency checks.

- Data processing and analytical workflow
  - Emergence date: adult emergence is highly synchronized; about 95% of males emerge within a two-week window (mean ≈14 days, SD ≈3.66 days).
  - Calling activity: quantified as singing presence in the first 10 minutes of each hour; any positive sample within the hour marks the cricket as singing.
  - Searching activity: measured by burrow visit durations; transformed into a binary variable (short ≤ 77 min = 1; long > 77 min = 0) to reflect intensive searching, focusing on visits when the focal male is alone.
  - Dominance in fights: fights at burrows recorded with a win/loss score for each participant; data used relative to the male’s age.
  - Mating promptness: latency from initial encounter to mating converted to a binary variable (≤50 minutes = 1; >50 minutes = 0) due to highly skewed distributions.
  - Data integration: multiple data streams (emergence, calling, searching, fights, mating) are compiled into a consistent dataset to enable longitudinal analyses.

- Fieldwork logistics and non-video observations
  - Each burrow flagged with a unique identifier; direct observations conducted for non-videoed burrows to record occupant identity and emergence events.
  - Post-season review of videos to extract additional events (emergence, encounters, singing, matings, fights, oviposition, predators, movement).

- Observational scope and temporal coverage
  - Surveillance spans from the start of adult eclosion through the end of the breeding season; continuous camera operation across the period via motion-triggered recording, with removal of equipment after activity declines to ensure yearly reuse.

- Relevance for data management and leadership
  - Demonstrates a multi-modal, long-term data system with unique identifiers, metadata-rich samples, and rigorous quality control.
  - Emphasizes data discoverability, calibration, and integration across behavioral, physiological, and environmental data streams.
  - Provides a structured approach to capturing, validating, and transforming complex ecological data into analyzable formats, suitable for longitudinal analyses and cross-dataset reuse.