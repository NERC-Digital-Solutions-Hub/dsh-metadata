# Data Collection

- Overview
  - Part of a NERC-funded Independent Research Fellowship examining the role of social information in the evolution of prey defences.
  - Model system: great tits; study conducted at the University of Jyväskylä Research Station, Konnevesi, Finland (geospatial coordinates provided).
  - Timeline: Oct 2013 – Jan 2014; 56 wild-caught birds (mixed sex and age classes) used; birds housed individually with acclimatization; no mortality; birds released after experiments.
  - Ethical compliance: approvals from KESELY and the National Animal Experiment Board; birds released back to capture site after testing.
  - Experimental aim: test whether birds learned to associate prey characteristics with distastefulness via demonstrator observations presented through video playback (validated prior to main experiments).

- Study design and scope
  - Two main components:
    - Video playback validation: demonstrator-presented foraging (distasteful prey) shown via video; control treatment without demonstrator.
    - Foraging experiment: training and testing with aposematic (distasteful) vs cryptic prey, using a cross-symbol setup in an aviary; repeated over consecutive days; demonstrations presented before testing.
  - Experimental environment: individual test chambers, aviary room with marked floor, food deprivation prior to experiments to motivate foraging, ad libitum water and standard foods otherwise.

- Data collected: datasets and variables
  - Video playback validation dataset
    - BirdID: Unique ID for each bird
    - Sex
    - Age: juveniles from 2013 breeding season; adults >1 year
    - Date.of.test: date of validation test
    - Treatment: social (video of demonstrator) or control (video of cups only)
    - Cup.colour.chosen: final cup landed on (red, white, or brown)
  - Foraging experiment dataset
    - BirdID: Unique ID for each bird
    - Sex
    - Age: as above
    - Treatment: social or control
    - DemonstratorID: BirdID of demonstrator used in social treatment videos
    - Test: sequence of the experiment (repeated over 3 days)
    - Date.of.test: date of the experiment
    - time.out.box: time (seconds) to enter aviary
    - first.prey.taken: whether the first prey item was aposematic or cryptic
    - number.apo.prey.taken: count of aposematic prey taken
    - number.cryptic.prey.taken: count of cryptic prey taken
    - Incl.in.validation: whether the bird was used in validation
    - Validation.treatment: if included, whether validation was social or control

- Experimental procedures and data provenance
  - Bird handling and housing
    - Birds captured in groups; one adult male designated as demonstrator per group
    - Individual housing in wooden cages with standardized light cycle
    - Acclimatization period; acoustic contact only
    - Food deprivation of ~2 hours before experiments; water available at all times
  - Validation procedure
    - Test chamber: wooden box with tinted plexiglass front; LCD video playback adjacent to the bird
    - Demonstrator behavior: adult male foraging a distasteful mealworm (chloroquine-treated) with characteristic disgust responses
    - Validation controls: cup options presented without demonstrator
  - Foraging experiment procedure
    - Training: birds trained to open and search packets containing almond sections
    - Prey stimuli: aposematic prey (chloroquine-treated) vs cryptic prey
    - Experimental setup: cross-symbol floor for cryptic vs aposematic prey; video precedes each test
    - Timeframe: 2-minute observation windows for nymphal movements; 1-minute windows for adult female movements; total testing period per day limited; birds removed after 12 prey items or after 3 days
    - Repetition: experiments repeated over two consecutive days (after initial video exposure) and again across days as specified
  - Data linkage and traceability
    - Data tables are designed to be linked via BirdID and DemonstratorID
    - Validation status and treatments recorded to enable cross-dataset joins
    - Clear recording of test dates and sequence to support longitudinal analyses

- Ethics, welfare, and approvals
  - Central Finland KESELY permit and National Animal Experiment Board license obtained
  - No mortality reported; all birds released back to their capture sites after completion

- Data governance and sharing considerations for stewardship
  - Data structure supports reproducibility: two clearly defined datasets with explicit field names and units
  - Important metadata to maintain: BirdID scheme, age classification, treatment assignments, DemonstratorID links, validation inclusion, and test sequencing
  - Potential data quality considerations: consistency of age labeling (juveniles vs adults), accurate time measurements (time.out.box), and alignment of validation vs foraging records across datasets
  - Access considerations: data should be accompanied by a data dictionary detailing variable options (e.g., treatment codes, cup colors, prey types) and the meaning of flags such as Incl.in.validation

- Summary takeaway for data stewardship
  - The Data Collection document describes a well-documented, ethically approved behavioral ecology study with two interconnected datasets focused on social learning and foraging in great tits.
  - Key data elements are clearly defined, enabling robust data governance, provenance tracking, and cross-dataset analysis, with explicit opportunities to enhance metadata (data dictionary, standardized date/time formats, and consistent age classifications) for improved discoverability and reuse.