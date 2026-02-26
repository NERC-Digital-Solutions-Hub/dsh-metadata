# Metadata for: MultihostBDdata.csv

## Overview and Aim
- Document describes metadata for a mesocosm experiment (2017) investigating how non-reservoir hosts influence maintenance and transmission of Batrachochytrium dendrobatidis (Bd) in an amphibian community.
- Location: Guadarrama Mountain National Park, Penalara Massif near Madrid, Spain; Centre for Captive Breeding of Threatened Amphibians in Rascafría.
- Key biological context: Salamandra salamandra (larval) acts as a seasonal Bd reservoir, with high infection susceptibility and potential to drive Bd dynamics in the community.
- Relevance for environment monitoring: Provides a standardized data structure for multi-host pathogen dynamics, enabling cross-study comparisons, long-term monitoring, and data sharing.

## Experimental Design
- Mesocosm experiment with 36 tanks examining Bd infection dynamics across host community compositions.
- Five treatments:
  1) Control: 24 salamanders only (Ss control)
  2) Two species with toads: 12 salamanders + 12 Bufo spinosus
  3) Two species with frogs: 12 salamanders + 12 Hyla meridiensis
  4) Three species non-random: 12 salamanders, 6 toads, 6 frogs
  5) Three species random: relative abundances of salamanders, toads, and frogs chosen at random
- Target hosts: Salamanders (S. salamandra), Tree frogs (Hyla meridiensis), Spiny toads (Bufo spinosus)
- Sampling window: Salamanders sampled at three time points (initial, intermediate, final); frogs and toads sampled only at final interval
- Outcome measure: Bd infection load, expressed as Bd DNA genomic equivalents

## Variables and Data Fields
- unique_ID: unique identifier for each datapoint
- date/time: date sample was collected
- tank_ID: identifier for the mesocosm tank (36 total)
- time_interval: sampling time point (initial, intermediate, final)
- sample_type: method of sampling (swab, mouth clip, tail clip, toe clip, dead specimen)
- treatment: experimental host community composition (Ss control, Ss + Bs, Ss + Hm, Ss + Bs + Hm non-random, random)
- fate: ultimate outcome for the individual (euthanised, metamorphosed, died)
- infection_load: Bd DNA quantity (genomic equivalents)

## Study Site and Organisms
- Site: Centre for Captive Breeding of Threatened Amphibians, Rascafría, Spain
- Environment: network of ponds in Guadarrama Mountain National Park
- Species context: multi-host amphibian community with varying phenology and Bd susceptibility; salamander larvae highlighted as key reservoir

## Data Management and Access
- Metadata emphasizes standardized data capture to support data quality assurance, cleaning, and transformation
- Data intended to be stored and accessible through appropriate data portals; facilitates data reuse and combination with other datasets for environmental health monitoring

## References (contextual literature)
- Fernández-Beaskoetxea et al. 2016
- Bosch et al. 2018
- Medina et al. 2015
- Gabor et al. 2017
- Hite et al. 2016