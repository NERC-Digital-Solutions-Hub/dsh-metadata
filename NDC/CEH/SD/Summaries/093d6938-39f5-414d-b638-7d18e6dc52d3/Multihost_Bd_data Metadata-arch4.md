# Metadata for: MultihostBDdata.csv

## Overview
- Describes a mesocosm experiment from late summer 2017 at the Centre for Captive Breeding of Threatened Amphibians, Rascafría, Spain.
- Objective: determine how non-reservoir hosts influence maintenance and transmission of Batrachochytrium dendrobatidis (Bd) infections supported by reservoir hosts.
- Focus on an amphibian community in Guadarrama Mountain National Park, near Madrid, Spain, with ten co-occurring species and dynamic seasonal assemblage.
- Salamander larvae (Salamandra salamandra) act as a seasonal reservoir, overwintering in ponds and maintaining infections, potentially driving Bd dynamics independently of other hosts.
- The study investigates whether these hypotheses hold across a three-species community and varying relative abundances.

## Experimental design and sampling
- Host community treatments (five total):
  - (1) Control: 24 salamanders only (Ss control)
  - (2) 2 species with toads: 12 salamanders and 12 Bufo spinosus (toads) (Ss + Bs)
  - (3) 2 species with frogs: 12 salamanders and 12 Hyla meridiensis (tree frogs) (Ss + Hm)
  - (4) 3 species non-random: 12 salamanders, 6 toads, 6 frogs (Ss + Bs + Hm)
  - (5) 3 species random: relative abundances of salamanders, toads, and frogs chosen at random (random)
- Setup:
  - 36 mesocosm tanks in total.
  - Salamanders sampled at three time points (initial, intermediate, final); frogs and toads sampled only at the final interval.
- Pathogen focus: Bd infection dynamics across host community compositions.

## Data structure and variables
- Unique identifiers:
  - unique_ID: unique data point identifier
  - tank_ID: unique mesocosm tank identifier
- Time and sampling:
  - date: date of sample collection
  - time_interval: sampling interval for salamanders (initial, intermediate, final); final only for amphibian groups other than salamanders
  - sample_type: method for pathogen detection (swab, mouth clip, tail clip, toe clip, dead analysis)
- Experimental treatment and outcomes:
  - treatment: coded treatment label (Ss control, Ss + Bs, Ss + Hm, Ss + Bs + Hm, random)
  - fate: ultimate outcome for the individual (euthanised, metamorphosed, or died)
- Measurements:
  - infection_load: Bd DNA quantified as genomic equivalents
- Notes:
  - Data capture aligns with a structured design to compare Bd dynamics across host community compositions and timepoints.

## Treatments and context
- Five experimental treatments defined by host composition and arrangement (as above).
- Distinct sampling timelines across species to capture infection dynamics within the community.

## References (contextual)
- Key literature on Bd infection dynamics, multi-host transmission, and amphibian community responses, including:
  - Fernández-Beaskoetxea et al. 2016
  - Bosch et al. 2018
  - Medina et al. 2015
  - Gabor et al. 2017
  - Hite et al. 2016

## Data governance and reuse notes
- Clear unique identifiers (unique_ID, tank_ID) support traceability and reproducibility.
- Comprehensive variable definitions and sampling metadata enable robust quality assessment and cross-study reuse.
- Timepoint structure and treatment coding facilitate comparative analyses of infection dynamics across community compositions and over time.