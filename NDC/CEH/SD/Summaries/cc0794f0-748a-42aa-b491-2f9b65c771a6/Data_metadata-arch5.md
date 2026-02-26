# STUDY SPECIES

## Overview
- Describes observational and experimental data on savannah herbivores, including vigilance, responses to predator cues, heterospecific alarm calls, and species counts.
- Species include Thomson gazelle, Grant gazelle, impala, warthog, ostrich, topi, hartebeest, blue wildebeest, plains zebra, African buffalo, common eland, and giraffe, with numeric abbreviations provided.
- Data were collected to quantify behavioral responses, relative abundance, group dynamics, and interspecific communication effects.
- Key reference: Meise, Franks, & Bro-Jørgensen (2018).

## Datasets and Key Variables
- Data_VigilanceBehaviour
  - Key fields: Species, NumberHeadUps, VigilancePerMinute, GroupSize
  - Purpose: quantify species-specific vigilance rates from video recordings (minimum 5 minutes per monospecific group)
- Data_PredatorSimulations
  - Key fields: Species, Date, Model (predator type or reedbuck control), Call (alarm call occurrence within 5 minutes), DistanceModel (laser-measured distance), GroupSize, NumberOffspring
  - Purpose: assess responses to life-sized 2D predator models (lion, spotted hyena, leopard, cheetah, black-backed jackal) versus control
- Data_PlaybackResponse
  - Key fields: FocalSpecies, CallerSpecies, Date, Response (whether a behavioral change occurred within 10s), FirstResponse (latency to first response), DurationResponse, SpeedHeadUp, NOScratch, NOShake, NOHeadUps, NOAlarm, Wind, Temperature, GrassHeight, DistanceCover, DistanceFocal, GroupSize, Full
  - Purpose: evaluate responses to heterospecific alarm calls and various contextual factors
- Data_SpeciesCounts
  - Key fields: Date, StudyPlain, Group, Tho, Gra, Imp, War, Zeb, Top, Wil, Har, Ela, Gir, Buf, Ost
  - Purpose: determine relative abundance and group composition across three plains (66 censuses over 54 km²)

## Methods and Data Collection
- Vigilance data: monospecific foraging groups observed for at least 5 minutes; record number and duration of vigilance bouts per visible individual; compute group-level means.
- Predator simulations: life-sized 2D predator models placed beside vehicle; groups relaxed prior to exposure; alarm calls recorded within 5 minutes.
- Playback experiments: alarm calls from other study species (except Eland) presented via loudspeaker at ~65 m distance and 90° angle; three recordings per stimulus; relaxed, foraging individuals targeted.
- Data processing: videos analyzed with Behavioural Observation Research Interface Software; detailed data dictionaries accompany each dataset.
- Abundance and grouping: 66 censuses across three plains; herbivore presence along predefined tracks; group-by-group counts recorded.

## Data Quality, Metadata, and Standards (Governance Considerations)
- Rich metadata fields accompany each dataset (e.g., definitions in Data_VigilanceBehaviour, Data_PredatorSimulations, etc.), with explicit explanations for each variable.
- Binary and continuous metrics clearly defined (e.g., Response as 1/0; latency and duration in seconds; distances in meters).
- Full dataset option indicated (e.g., Full in Data_PlaybackResponse) to denote complete parameter availability.
- Temporal and spatial scope documented (dates, study plains, area covered).
- Provenance tied to a published study (Meise et al., 2018) for methodological transparency.

## Access, Use, and Provenance
- Data are organized into distinct, well-documented data dictionaries suitable for data cataloging and interoperability.
- Primary publication for methods and context: Meise et al. 2018; users should consult for detailed protocols and model specifications.

## Temporal, Spatial Scope
- Spatial coverage: three study plains spanning 54 km².
- Temporal details: dates included in each dataset (e.g., Date fields in predator simulations and playback responses).

## Related Literature
- Meise, K., Franks, D. W., & Bro-Jørgensen, J. (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proceedings of the Royal Society B: Biological Sciences, 285(1882), 20172676.