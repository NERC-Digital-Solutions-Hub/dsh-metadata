# STUDY SPECIES

## Objective and scope
- Quantify vigilance and anti-predator responses across multiple herbivore species.
- Assess alarm-call responsiveness to heterospecific and conspecific cues via predator simulations and playback experiments.
- Determine relative abundance and grouping behavior through line-transect-like censuses across study plains.
- Provide standardized data outputs suitable for monitoring environmental health and policy performance over time.

## Target species and abbreviations
- Thomson gazelle (Gazella thomsonii) — Tho
- Grant gazelle (Gazella granti) — Gra
- Impala (Aepyceros melampus) — Imp
- Common warthog (Phacochoerus aethiopicus) — War
- Ostrich (Struthio camelus) — Ost
- Topi (Damaliscus lunatus) — Top
- Hartebeest (Alcelaphus buselaphus) — Har
- Blue wildebeest (Connochaetes taurinus) — Wil
- Plains zebra (Equus quagga) — Zeb
- African buffalo (Syncerus caffer) — Buf
- Common eland (Tragelaphus oryx) — Ela
- Giraffe (Giraffa camelopardalis) — Gir

## Methods and data collection protocols
- Vigilance behaviour
  - Monospecific foraging groups observed for ≥5 minutes.
  - For each visible individual, record number and duration of vigilance bouts (head raised above shoulder level).
  - Compute mean vigilance parameters per group.
- Predator simulations
  - Expose study species to life-sized lateral photographs of five predators (lion, spotted hyena, leopard, cheetah, black-backed jackal) and a reedbuck control.
  - Groups are relaxed, and models are revealed by moving the vehicle forward.
  - Record occurrence of alarm calls within 5 minutes of model detection.
- Playback experiments
  - Present alarm calls from other study species (except Eland) to assess cross-species responsiveness; use non-alarm dove calls as control.
  - Three recordings per stimulus category; focal animal is relaxed and foraging ≥20 s prior.
  - Speaker ~65 m away at 90° angle; stimuli chosen randomly; analyzed with Behavioural Observation Research Interface.
- Species counts
  - 66 censuses across three plains, covering 54 km².
  - Pre-defined tracks; record species composition within groups; calculate relative abundance as mean per census.
  - Capture group sizes and occurrence of mixed-species groups.

## Data sets and key variables
- Data_VigilanceBehaviour
  - Species; NumberHeadUps; VigilancePerMinute; GroupSize
- Data_PredatorSimulations
  - Species; Date; Model; Call (alarm call occurrence); DistanceModel; GroupSize; NumberOffspring
- Data_PlaybackResponse
  - FocalSpecies; CallerSpecies; Date; Response; FirstResponse; DurationResponse; SpeedHeadUp; NOScratch; NOShake; NOHeadUps; NOAlarm; Wind; Temperature; GrassHeight; DistanceCover; DistanceFocal; GroupSize; Full
- Data_SpeciesCounts
  - Date; StudyPlain; Group; Tho; Gra; Imp; War; Zeb; Top; Wil; Har; Ela; Gir; Buf; Ost

## Data management and outputs
- Data are verified, quality assured, cleaned, and transformed.
- Standardised analysis outputs include reports, maps, and charts.
- Datasets are stored and uploaded to appropriate data portals for accessibility and re-use.

## Challenges and opportunities
- Increase dataset value by combining with additional environmental and ecological data (avoiding single-use datasets).
- Improve accessibility of underlying data to support broader analyses and policy evaluation.

## Reference
- Meise, K., Franks, D. W., & Bro-Jørgensen, J. (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proceedings of the Royal Society B: Biological Sciences, 285(1882), 20172676