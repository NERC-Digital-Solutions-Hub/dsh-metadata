# Metadata for: MultihostBDdata.csv

- Objective
  - Report data from a mesocosm experiment (late summer 2017) to assess how non-reservoir hosts influence maintenance and transmission of infections (Bd) supported by reservoir hosts.
  - Context: amphibian community in Guadarrama Mountain National Park, Spain; salamander larvae suspected to largely drive Bd dynamics due to overwintering, high infection prevalence, and sustained infections.

- Experimental setup
  - Location: Centre for Captive Breeding of Threatened Amphibians, Rascafría, Spain.
  - System: network of ponds within the park; 10 co-occurring amphibian species in the area.
  - Focus species: Salamandra salamandra (larval stage as seasonal reservoir), Hyla meridiensis (tree frog), Bufo spinosus (spiny toad).
  - Experimental units: 36 mesocosm tanks.

- Treatments (five host community compositions)
  - Ss control: 24 salamanders only
  - Ss + Bs: 12 salamanders + 12 toads
  - Ss + Hm: 12 salamanders + 12 tree frogs
  - Ss + Bs + Hm non-random: 12 salamanders, 6 toads, 6 tree frogs
  - random: 3-species composition with random relative abundances

- Data/variables collected
  - unique_ID: unique identifier for each datapoint
  - date: sampling date
  - tank_ID: identifier for the mesocosm tank (36 total)
  - time_interval: sampling period (initial, intermediate, final)
  - sample_type: method of pathogen sampling (swab, mouth clip, tail clip, toe clip, or dead)
  - treatment: coded treatment label (Ss control; Ss + Bs; Ss + Hm; Ss + Bs + Hm; random)
  - fate: outcome for the individual (euthanised, metamorphosed, or died)
  - infection_load: Bd DNA quantity (genomic equivalents) in the sample

- Sampling details
  - Salamanders: sampled across three time intervals
  - Frogs and toads: sampled only at the final interval

- References (contextual literature)
  - Studies on Bd infection and transmission in multi-host amphibian communities and factors influencing Bd dynamics, including host diversity, transmission costs, and habitat/host structure effects.

- Potential analyses and uses
  - Explore correlations between host community composition and Bd infection dynamics (infection_load) across time.
  - Assess the role of salamander larvae as reservoirs in maintaining or amplifying Bd transmission within mixed-species communities.
  - Compare outcomes (fate) across treatments to infer impacts of added species on survival and metamorphosis in Bd-exposed communities.
  - Use data and metadata to enable cross-study synthesis on multi-host parasite dynamics and to support data discovery and reuse.