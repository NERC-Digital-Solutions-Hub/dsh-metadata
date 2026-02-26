# Data Collection

## Aim and context
- Part of a NERC-funded Independent Research Fellowship examining the role of social information in the evolution of prey defences.
- Model system: great tits; aim to test whether birds learn to associate prey characteristics with distastefulness by observing a demonstrator via video playback.
- Location: University of Jyväskylä Research Station, Konnevesi, Finland.
- Ethical approvals: KESELY/1017/07.01/2010 and ESAVI-2010-087517Ym-23.
- Key outcome: behavioral data on social learning and foraging choices collected under controlled conditions with video demonstrations and foraging tasks.

## Study setting and sampling
- Timeframe: 17 October 2013 – 24 January 2014.
- Sample: 56 wild-caught birds (12 adult females, 16 adult males, 13 juvenile females, 15 juvenile males).
- Grouping: caught in groups of 5; one adult male designated as demonstrator.
- Use: 14 individuals used for both validation and main experiment.
- Housing: individuals housed in wooden cages (65 x 50 x 80 cm) with a fixed light cycle; acoustic contact only between birds; ad libitum water, sunflower seeds, and tallow; 2 h food deprivation prior to experiments to ensure motivation.
- Release: birds released at their capture site after experiments; no mortality in captivity.

## Experimental design

### Video playback validation
- Setup: test chamber (wooden box, 50 x 50 x 67 cm) with tinted Plexiglass front; two-hour acclimation for motivation to forage.
- Demonstration: an adult male interacts with a cup containing a bitter mealworm (chloroquine-treated) showing disgust responses (beak wiping, head shaking).
- Treatments: social (video of demonstrator) vs control (video of feeding cups without demonstrator).
- Foraging task: birds learn to open a packet containing almond; aviary environment includes cryptic vs aposematic prey cues (cross vs square symbols) and a time-limited observation window.
- Procedure: video shown before release; test period recorded over two consecutive days; birds free to move; objective: measure how social demonstration influences foraging choices.

### Foraging experiment
- Task structure: two prey types—cryptic and aposematic (chloroquine-treated almond).
- Procedure: video demonstrations precede foraging in the aviary; test continues until 12 prey items are taken.
- Repetition: experiment repeated on two consecutive days without additional video playback.
- Treatments: social (demonstrator video) vs control (prey-only video).

## Data collected and structure

### Video playback validation
- BirdID: unique identifier for each bird.
- Sex
- Age: juveniles (from 2013 breeding season) vs adults (>1 year)
- Date.of.test: date of the validation test
- Treatment: social (demonstrator video) or control (prey-only video)
- Cup.colour.chosen: color of the first cup landed on (red, white, or brown)

### Foraging experiment
- BirdID: unique identifier
- Sex
- Age
- Treatment: social or control (as above)
- DemonstratorID: BirdID of the individual used as demonstrator in the social treatment videos
- Test: which day of testing (repeated over 3 days in the protocol)
- Date.of.test: date of the experiment
- time.out.box: time (in seconds) for the bird to enter the aviary
- first.prey.taken: whether the first prey taken was aposematic or cryptic
- number.apo.prey.taken: total number of aposematic prey taken
- number.cryptic.prey.taken: total number of cryptic prey taken
- Incl.in.validation: whether the bird was included in the validation dataset
- Validation.treatment: if included in validation, whether the validation was social or control

## Ethics, welfare, and data governance
- Animals housed and handled under approved ethical licenses; no mortality; post-experiment release back to the wild.
- Data collection employed unique identifiers (BirdID) and standardized metadata fields to enable traceability across validation and main experiments.
- Experimental records include provenance (demonstrator identity, treatment type) to support potential secondary analyses and data governance considerations.