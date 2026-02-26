# STUDY SPECIES

## Overview
- Studies 11 herbivore species in African savannahs to quantify vigilance, predator-response behaviors, and responses to heterospecific alarm calls.
- Data enable cross-species comparisons of alarm responsiveness, vigilance patterns, grouping behavior, and abundance.

## Datasets and data structure
- Data_VigilanceBehaviour
  - Key fields: Species; NumberHeadUps; VigilancePerMinute; GroupSize
- Data_PredatorSimulations
  - Key fields: Species; Date; Model (predator types or reedbuck control); Call (alarm call detected within 5 minutes); DistanceModel; GroupSize; NumberOffspring
- Data_PlaybackResponse
  - Key fields: FocalSpecies; CallerSpecies; Date; Response (1/0); FirstResponse (sec); DurationResponse (sec); SpeedHeadUp; NOScratch; NOShake; NOHeadUps; NOAlarm; Wind; Temperature; GrassHeight; DistanceCover; DistanceFocal; GroupSize; Full (all parameters)
- Data_SpeciesCounts
  - Key fields: Date; StudyPlain; Group; Tho (Thomson gazelles); Gra (Grant gazelles); Imp (Impala); War (Warthog); Zeb (Zebra); Top (Topi); Wil (Blue wildebeest); Har (Hartebeest); Ela (Eland); Gir (Giraffe); Buf (Buffalo); Ost (Ostrich)
- Species abbreviations and full names are provided for all study species
- Data dictionary style: each dataset includes clearly explained fields and units

## Methods at a glance
- Vigilance behaviour
  - Video-recorded monospecific foraging groups for ≥5 minutes
  - Logged for each visible individual: number and duration of vigilance bouts; computed mean vigilance parameters per group
- Predator simulations
  - Exposed groups to life-sized 2D predator models (lion, hyena, leopard, cheetah, jackal) and a reedbuck control
  - Stimuli revealed by car movement; recorded alarm calls within 5 minutes
- Playback experiments
  - Presented alarm calls of other study species (except Eland) and a non-alarm dove call as control
  - Stimuli delivered from ~65 m at a 90° angle; randomized stimulus category
  - Analyzed responses via video and Behavioral Observation Research Interface (BORIS)
- Species counts
  - 66 censuses across three plains (total ~54 km2)
  - Pre-defined tracks; recorded species identities within each group; computed relative abundance as mean individuals per census
  - Recorded group sizes and occurrence of mixed-species groups
- Reference for methods: Meise et al. 2018

## Data quality and considerations
- Data are observational with standardized stimuli, enabling cross-species comparisons but potential biases in detection and selection.
- Environmental covariates (Wind, Temperature, GrassHeight) captured for playback analyses
- Temporal and spatial coverage limited to specific plains and study periods; caution with broader generalizations
- For analyses bridging datasets, align on Species, Date, and StudyPlain; ensure consistent group-size and distance measures

## Potential data products and analyses (Data Support perspective)
- Cross-species dashboards of vigilance rates by species, group size, and environmental conditions
- Models linking predator-model exposure and alarm-call playback to subsequent foraging resumption or vigilance adjustments
- Combined dataset to examine the relationship between relative abundance and observed vigilance or responsiveness
- Data products enabling self-serve exploration of alarm-call responsiveness and heterospecific communication dynamics
- Data validation and quality checks to ensure consistency across datasets and time points

## Reference
- Meise, K., Franks, D. W., & Bro-Jørgensen, J. (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proceedings of the Royal Society B: Biological Sciences, 285(1882), 20172676