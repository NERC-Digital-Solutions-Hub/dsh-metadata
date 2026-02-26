# Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores

- Purpose and scope
  - Document study aims to quantify vigilance, predator-elicited alarm responses, and responsiveness to heterospecific alarm calls among savannah herbivores.
  - Data intended to illuminate interspecific information transfer and inform ecological monitoring and policy decisions related to wildlife behavior.

- Study species and identifiers
  - 12 focal species with abbreviations: Thomson gazelle (Tho), Grant gazelle (Gra), Impala (Imp), Common warthog (War), Ostrich (Ost), Topi (Top), Hartebeest (Har), Blue wildebeest (Wil), Plains zebra (Zeb), African buffalo (Buf), Common eland (Ela), Giraffe (Gir).

- Methods and measures
  - Vigilance behaviour
    - Monospecific foraging groups observed via video for at least 5 minutes.
    - For each visible individual: count and duration of vigilance bouts (head-up until head-down).
    - Compute mean vigilance parameters per group.
  - Predator simulations
    - Life-sized lateral predator models (lion, spotted hyena, leopard, cheetah, black-backed jackal) plus reedbuck control.
    - Monospecific groups observed for at least 1 minute; models revealed from behind car; alarm calls recorded within 5 minutes.
    - Details linked to Meise et al. 2018.
  - Playback experiments
    - Alarm calls from other study species presented to focal herbivores (excluding eland, which was not observed alarm-calling at the site).
    - Control: non-alarm dove call.
    - Each stimulus category had three recordings; focal animals relaxed and foraging for at least 20 s prior.
    - Playback distance ~65 m, 90° to focal animal; stimulus chosen randomly.
    - Analyses conducted with Behavioural Observation Research Interface Software (BORIS).
  - Species counts
    - 66 censuses across three plains, covering 54 km2.
    - Pre-defined tracks to assess presence; record species identity within groups; compute relative abundance as mean individuals per census; capture group sizes and mixed-species occurrences.

- Data structures (Data_ datasets) and key variables
  - Data_VigilanceBehaviour
    - Species; NumberHeadUps; VigilancePerMinute; GroupSize.
  - Data_PredatorSimulations
    - Species; Date; Model; Call; DistanceModel; GroupSize; NumberOffspring.
  - Data_PlaybackResponse
    - FocalSpecies; CallerSpecies; Date; Response; FirstResponse; DurationResponse; SpeedHeadUp; NOScratch; NOShake; NOHeadUps; NOAlarm; Wind; Temperature; GrassHeight; DistanceCover; DistanceFocal; GroupSize; Full.
  - Data_SpeciesCounts
    - Date; StudyPlain; Group; Tho; Gra; Imp; War; Zeb; Top; Wil; Har; Ela; Gir; Buf; Ost.
  - Abbreviations and species list are provided to support data interpretation and cross-study comparability.

- Data quality, metadata, and sharing implications
  - Explicit data dictionaries and variable explanations accompany datasets.
  - Emphasis on transparent data provenance, clear definitions, and the need for sharing underlying data to enable replication and policy-relevant analysis.
  - Acknowledges potential barriers to data sharing and the importance of metadata adequacy and standardized formats.

- Relevance to monitoring frameworks
  - Demonstrates a structured approach to converting behavioral indicators (vigilance, alarm responsiveness) into standardized, shareable datasets suitable for monitoring.
  - Highlights the necessity of detailed metadata, standardized protocols, and governance around data storage, access, and reuse.
  - Provides a model for integrating multiple data streams (behavioral observations, experimental stimuli responses, and census counts) to inform environmental health and wildlife management decisions.

- Practical implications for policy and governance
  - Supports development of dashboards and reports that integrate behavioral metrics with environmental covariates (wind, temperature, grass height) for policy-relevant decision making.
  - Underscores the importance of early planning for data rights, licenses, and provenance to facilitate multi-site monitoring and data sharing.
  - Demonstrates the value of standardized data dictionaries to enable cross-site comparisons and synthesis for monitoring programs.

- Reference
  - Meise, K., Franks, D. W., & Bro-Jørgensen, J. (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proceedings of the Royal Society B: Biological Sciences, 285(1882), 20172676