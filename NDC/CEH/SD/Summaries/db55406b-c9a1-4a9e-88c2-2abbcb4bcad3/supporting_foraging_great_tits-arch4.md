# Data Collection

## Context and Aim
- Part of a NERC-funded Independent Research Fellowship studying the role of social information in the evolution of prey defences.
- Model system: great tits; objective to test if birds learn to associate prey characteristics with distastefulness by observing a demonstrator via video playback.
- Study conducted to validate video playback as a method and to assess social transmission of foraging behavior.

## Study Setting and Subjects
- Location: University of Jyväskylä Research Station, Konnevesi, Finland (coordinates provided).
- Population: abundant local population; established capture protocol; animal housing facility available.
- Experimental design involved 56 birds captured between Oct 17, 2013 and Jan 24, 2014; breakdown: 12 adult females, 16 adult males, 13 juvenile females, 15 juvenile males.
- Birds caught in groups of 5; one adult male per group designated as demonstrator.
- Birds housed individually in wooden cages with acclimatisation; acoustic contact only; food provisioning details described; birds food-deprived for 2 hours prior to experiments.
- Ethical approvals and licenses obtained; no mortality in captivity; birds released back at capture site after experiments.

## Data Assets and Metadata
- Two main data components:
  - Video playback validation data
  - Foraging experiment data
- Video playback validation captures:
  - BirdID, Sex, Age, Date.of.test, Treatment (social vs control), Cup.colour.chosen (red, white, or brown)
- Foraging experiment captures:
  - BirdID, Sex, Age, Treatment, DemonstratorID, Test (repeated over 3 days), Date.of.test, time.out.box (seconds), first.prey.taken (aposemate vs cryptic), number.apo.prey.taken, number.cryptic.prey.taken, Incl.in.validation, Validation.treatment
- Additional design details:
  - Validation used an adult male demonstrator with a distasteful mealworm; control lacked a demonstrator.
  - Foraging trials involved cryptic vs aposematic prey representations and two-day repetition after initial video exposure.
- Data collection ensured tagging and tracking of individual birds with unique IDs for linkage across validation and main experiments.

## Data Collection Procedures and Workflow
- Birds caught in groups and acclimatised individually; water and food provided with controlled deprivation to motivate foraging.
- Validation phase:
  - Birds placed in test chambers; exposed to video of demonstrator foraging on distasteful prey; subsequent choice recorded among cups.
- Foraging phase:
  - Birds trained to locate paper packets containing almond; prey items prepared as aposematic (bitter) vs cryptic; identical video exposure prior to testing.
  - Sessions conducted in an aviary room; recording time to enter, order of prey items taken, and behavior indicators (e.g., beak wiping, head shaking) as in validation.
  - Each bird experienced the test across multiple days; the main test followed by a two-day repetition before release.

## Ethics, Permits and Welfare
- Approvals: KESELY license number provided; ESAVI animal experiment board permit.
- Welfare: Birds housed individually with access to water; no deaths; all birds released at capture sites after testing.

## Data Quality, Validation and Reliability
- Use of unique BirdID to maintain consistent identification across validation and main experiments.
- Clear delineation between validation and main data with explicit treatment labeling (social vs control) and DemonstratorID for social condition.
- Video playback validation designed to establish an appropriate method prior to the main foraging experiment.
- Repeated measures across days to assess consistency and potential learning effects.

## Data Management, Access and Provenance
- Data collected at a single research site with explicit experimental controls and protocols.
- Datasets structured with standardized metadata fields to enable linkage between validation and foraging outcomes.
- provenance clearly documented through experimental steps, consent, and licensing information.

## Notable Observations for Data Leaders
- Demonstrates rigorous metadata design (BirdID, Sex, Age, Treatment, DemonstratorID, Test, Date, timing metrics, and outcome counts) facilitating data discoverability, reuse, and cross-study collaboration.
- Integrates validation data with main outcome data to support methodological transparency and replicability.
- Emphasizes ethical governance and welfare considerations alongside data integrity.