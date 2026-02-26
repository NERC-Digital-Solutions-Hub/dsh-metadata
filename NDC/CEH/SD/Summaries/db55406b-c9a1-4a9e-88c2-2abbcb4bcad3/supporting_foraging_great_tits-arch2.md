# Data Collection

## Overview
- NERC-funded Independent Research Fellowship study on the role of social information in the evolution of prey defences, using great tits as the model species.
- Location: University of Jyväskylä Research Station, Konnevesi, Finland; field-relevant, with controlled housing and experimental facilities.
- Aim: test whether birds learn to associate prey characteristics with distastefulness by observing a demonstrator via video playback; validation of video playback as an appropriate method.
- Timeframe and scope: October 2013 – January 2014; 56 birds used across validation and main experiments; individuals categorized by sex and age.

## Experimental design and setup
- Subjects: 56 birds captured from the wild (12 adult females, 16 adult males, 13 juvenile females, 15 juvenile males); group size for catching and assignment included a demonstrator male.
- Housing and acclimation: birds housed individually in wooden cages; acclimatised overnight; acoustic contact only; ad libitum water and seeds with tallow; food-deprived for 2 hours prior to experiments to motivate foraging.
- Demonstrator assignment: one adult male designated as demonstrator per group; some birds used for both validation and main experiments.
- Ethical approvals: permissions from KESELY and ESAVI; no mortality; released back to capture site after experiments.

## Video playback validation
- Test chamber setup: wooden box with tinted plexiglass front, perch, and water; two-hour acclimation to motivate foraging.
- Demonstration: video of an adult male foraging on a bitter mealworm (chloroquine) showing disgust responses (beak wiping, head shaking); control showed the cup without a demonstrator.
- Foraging task during validation: birds chose among cups (red, white, brown) after viewing the video; recording focused on initial cup choice and subsequent foraging behavior.

## Foraging experiment
- Training: birds learned to open and search paper packets containing a piece of almond; packets printed with symbols (black/white for cryptic prey; square symbol for aposematic prey).
- Prey manipulation: aposematic prey (almond) soaked in chloroquine to render it unpalatable.
- Test environment: aviary room with a cross symbol floor pattern; video shown prior to release; objective to observe association between prey type and foraging decisions.
- Procedure: post-video release, time-to-enter recorded; prey type taken recorded; experiment continued for up to 12 prey items per session; repeated over two consecutive days before release.
- Repetition: testing conducted over three days per bird for the main dataset.

## Data collection and structure
- Video playback validation dataset:
  - BirdID, Sex, Age, Date.of.test, Treatment (social vs control), Cup.colour.chosen (red/white/brown).
- Foraging experiment dataset:
  - BirdID, Sex, Age, Treatment, DemonstratorID, Test (day), Date.of.test, time.out.box (seconds to enter aviary), first.prey.taken (aposematic or cryptic), number.apo.prey.taken, number.cryptic.prey.taken, Incl.in.validation, Validation.treatment (if applicable).

## Ethics and welfare
- Compliance with licensing and animal welfare requirements; no bird deaths; post-experiment release at capture site.

## Data management and sharing
- Data are stored with unique identifiers (BirdID) and are prepared for standardized analysis.
- Datasets were designed for compatibility with external portals and broader environmental data ecosystems, aligning with standardised QA and data curation practices.

## Relevance to environmental monitoring
- Demonstrates standardized, high-quality data collection from animal behavior to assess environmental health indicators (e.g., social learning and prey defense responses).
- Uses clear metadata (demonstrator, treatment, age/sex, timing) to enable cross-study comparisons and longitudinal monitoring.
- Emphasizes data validation, reproducibility, and accessibility to support policy-relevant environmental analyses.