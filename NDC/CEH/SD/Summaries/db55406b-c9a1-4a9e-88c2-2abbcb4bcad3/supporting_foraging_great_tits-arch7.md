# Data Collection

## Study setting and scope
- NERC-funded Independent Research Fellowship exploring the role of social information in the evolution of prey defences.
- Model system: great tits (Parus major); experimental work at University of Jyväskylä Research Station, Konnevesi, Finland (62°37.7′ N, 026°17′ E).
- 56 birds captured Oct 17, 2013 – Jan 24, 2014; composition: 12 adult females, 16 adult males, 13 juvenile females, 15 juvenile males.
- Birds caught in groups of 5; one adult male designated as demonstrator.
- Birds housed individually with acclimatisation, acoustic contact only; ad libitum water and food (sunflower seeds, tallow); food deprived 2 hours prior to experiments to enhance foraging motivation.
- Permits: KESELY/1017/07.01/2010; ESAVI-2010-087517Ym-23. No mortality; all released at capture site after experiments.

## Experimental design
- Video playback validation: demonstrations of distasteful prey using a feeding cup and a bitter mealworm delivered to motivate a disgust response (beak wiping, head shaking). Comparisons made with control videos showing the cup without a demonstrator.
- Foraging experiment: birds trained to open and search for packets containing almond; prey presented on a cross-marked floor (cryptic) vs. a red square symbol (aposematic). Almonds soaked in chloroquine to be unpalatable. Each bird viewed a demonstrator foraging before testing; sessions conducted over 3 days with a stopping rule after 12 prey items were taken; testing occurred on two consecutive days prior to release.

## Datasets and schema
- Video playback validation dataset
  - BirdID: unique ID for each bird
  - Sex
  - Age: juveniles from 2013 breeding season; adults >1 year
  - Date.of.test: date of the validation test
  - Treatment: social (demonstrator video) or control (cup-only video)
  - Cup.colour.chosen: cup color landed on first (red, white, brown)
- Foraging experiment dataset
  - BirdID: unique ID for each bird
  - Sex
  - Age: juveniles from 2013 breeding season; adults >1 year
  - Treatment: social or control (as above)
  - DemonstratorID: BirdID of demonstrator in videos for social treatment
  - Test: number of days the experiment was repeated (3 days total)
  - Date.of.test: date of the experiment
  - time.out.box: seconds to enter aviary
  - first.prey.taken: whether the first prey item was aposematic or cryptic
  - number.apo.prey.taken: count of aposematic prey taken
  - number.cryptic.prey.taken: count of cryptic prey taken
  - Incl.in.validation: whether the bird was included in the validation dataset
  - Validation.treatment: if applicable, whether the bird belonged to the social or control validation group

## Sampling, housing, and procedures
- Birds captured from wild populations and housed individually in wooden cages with specified dimensions; light regime ~11.5 hours.
- Acclimatisation overnight; access to water ad libitum; acousto-sensory contact only.
- Behavioral testing involved a test chamber for video exposure, followed by an aviary testing room with defined prey cues and symbols; testing durations and intervals defined per protocol.
- Post-experiment: all birds released back to their capture sites.

## Ethics, permits, and welfare
- Permits from KESELY and ESAVI; no bird deaths; all birds released after completion of experiments.

## GIS-relevant notes and data reuse considerations
- Spatial context: precise study site coordinates enable geospatial tagging of experimental sessions.
- Temporal context: explicit test dates and repeated-measures design support longitudinal analysis.
- Data integration: two linked datasets (validation and foraging experiments) with shared identifiers (BirdID, DemonstratorID) suitable for merging to analyze behavior across conditions.
- Data quality considerations: unique identifiers, explicit inclusion in validation, and clear treatment labeling facilitate cleaning, de-duplication, and cross-dataset aggregation.