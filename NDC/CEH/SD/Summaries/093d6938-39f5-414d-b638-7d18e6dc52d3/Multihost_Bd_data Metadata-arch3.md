# Metadata for: MultihostBDdata.csv

## Overview
- Data from a mesocosm experiment conducted in late summer 2017 at the Centre for Captive Breeding of Threatened Amphibians in Rascafría, Spain.
- Objective: determine the extent to which non-reservoir hosts affect maintenance and transmission of infections from reservoir hosts.
- Study system: amphibian community in Guadarrama Mountain National Park (Penalara Massif near Madrid), with dynamic species assemblages due to phenology; focus on Batrachochytrium dendrobatidis (Bd) dynamics and potential reservoir role of larval fire salamanders (Salamandra salamandra).

## Experimental design
- Host species involved: salamanders (Salamandra salamandra), tree frogs (Hyla meridiensis), and spiny toads (Bufo spinosus).
- Treatments (five total):
  1) Control: 24 salamanders only (Ss control)
  2) Ss + Bs: salamanders and toads
  3) Ss + Hm: salamanders and frogs
  4) Ss + Bs + Hm: three species non-random
  5) Random: three species with random relative abundances
- Setup: 36 mesocosm tanks housing the amphibian communities.
- Sampling schedule: salamanders sampled at three time points (initial, intermediate, final); frogs and toads sampled only at the final time point.
- Variables measured per sample: Bd infection load (genomic equivalents), along with metadata describing samples.

## Variables and data structure
- unique_ID: unique identifier for each datapoint
- date/time_interval: date of collection; interval indicates initial, intermediate, or final sampling
- tank_ID: identifier for the mesocosm tank
- sample_type: method used for pathogen detection (swab, mouth clip, tail clip, toe clip, or analysis of a corpse)
- treatment: coded as the five experimental treatments (Ss control; Ss + Bs; Ss + Hm; Ss + Bs + Hm non-random; random)
- fate: ultimate outcome for the individual (euthanised, metamorphosed, or died)
- infection_load: Bd DNA quantity expressed as genomic equivalents

## Data interpretation and aims
- Aims to quantify Bd infection dynamics across host-community compositions and determine how non-reservoir hosts influence transmission and maintenance of Bd within amphibian communities.
- Data enable assessment of host interactions, potential reservoir status, and consequences for host survival across different community structures.

## References
- Fernández-Beaskoetxea et al. 2016: infection and transmission heterogeneity of Bd within multi-host communities
- Bosch et al. 2018: long-term monitoring after climate change and disease-driven species extirpation
- Medina et al. 2015; Gabor et al. 2017; Hite et al. 2016: related Bd transmission dynamics, host costs, and disease ecology in amphibians