# STUDY SPECIES

- Thomson gazelle (Tho), Grant gazelle (Gra), Impala (Imp), Common warthog (War), Ostrich (Ost), Topi (Top), Hartebeest (Har), Blue wildebeest (Wil), Plains zebra (Zeb), African buffalo (Buf), Common eland (Ela), Giraffe (Gir)

## Objective
- Quantify vigilance rates and patterns across species
- Assess alarm-call responsiveness to predators and heterospecific calls
- Determine relative abundance and group structure across study plains
- Provide data-driven insights to understand cross-species communication and anti-predator behavior

## Methods

- Vigilance behaviour
  - Video-record monospecific foraging groups for at least 5 minutes
  - For each visible individual, record number and duration of vigilance bouts (head above shoulder level)
  - Compute mean vigilance parameters for each group

- Predator simulations
  - Expose groups to life-sized lateral photographs of five main predators: lion, spotted hyena, leopard, cheetah, black-backed jackal; reedbuck as control
  - Use monospecific groups; ensure at least 1 minute of relaxation before stimulus
  - Models revealed by car movement; record occurrence of alarm calls within 5 minutes
  - Details follow Meise et al. 2018

- Playback experiments
  - Present alarm calls of other study species (excluding Eland) to assess responsiveness to heterospecific alarms
  - Control: non-alarm call of ring-necked dove
  - Three recordings per stimulus category
  - Target relaxed foragers ≥20 seconds prior; focal animal is the closest to the car
  - Loudspeaker ~65 meters away at 90°; playback stimuli randomized
  - Analysis with Behavioural Observation Research Interface Software; details follow Meise et al. 2018

- Species counts
  - 66 censuses across three study plains, covering 54 km^2
  - Herbivore presence along predefined tracks; record species identity per individual in each group
  - Relative abundance calculated as mean number of individuals per census
  - Data include group sizes and occurrence of mixed-species groups

## Data and key variables

- Data_VigilanceBehaviour
  - Species, NumberHeadUps, VigilancePerMinute, GroupSize

- Data_PredatorSimulations
  - Species, Date, Model, Call, DistanceModel, GroupSize, NumberOffspring

- Data_PlaybackResponse
  - FocalSpecies, CallerSpecies, Date, Response, FirstResponse, DurationResponse, SpeedHeadUp, NOScratch, NOShake, NOHeadUps, NOAlarm, Wind, Temperature, GrassHeight, DistanceCover, DistanceFocal, GroupSize, Full

- Data_SpeciesCounts
  - Date, StudyPlain, Group, Tho, Gra, Imp, War, Zeb, Top, Wil, Har, Ela, Gir, Buf, Ost

## Notes

- Reference: Meise, Franks, & Bro-Jørgensen (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proceedings of the Royal Society B: Biological Sciences, 285(1882), 20172676