# Metadata for: MultihostBDdata.csv

- Background and purpose
  - Data come from a mesocosm experiment (late summer 2017) at the Centre for Captive Breeding of Threatened Amphibians in Rascafría, Spain.
  - Objective: assess how non-reservoir hosts influence maintenance and transmission of the Bd pathogen within an amphibian community.
  - System context: amphibian assemblage in a network of ponds in Guadarrama Mountain National Park; 10 co-occurring species with phenology-driven community turnover; salamander larvae identified as a key seasonal reservoir for Bd.
  - The study informs whether salamanders alone can sustain Bd dynamics or if other species modulate transmission.

- Experimental design
  - Host community treatments (five total):
    - Ss control: 24 salamanders only
    - Ss + Bs: 12 salamanders + 12 toads (Bufo spinosus)
    - Ss + Hm: 12 salamanders + 12 frogs (Hyla meridiensis)
    - Ss + Bs + Hm: 12 salamanders, 6 toads, 6 frogs (non-random 3-species)
    - Random: relative abundances of the three species chosen at random (3-species)
  - Setup: 36 mesocosm tanks
  - Target species: Salamandra salamandra (salamanders), Hyla meridiensis (tree frogs), Bufo spinosus (spiny toads)
  - Sampling and measurements:
    - Variables tracked per datapoint:
      - unique_ID: unique identifier for the datapoint
      - date: sampling date
      - tank_ID: tank identifier
      - time_interval: when the salamander sample was collected (initial, intermediate, final); frogs/toads sampled only at final
      - sample_type: method of pathogen sampling (swab, mouth clip, tail clip, toe clip, or dead specimen analysis)
      - treatment: codified treatment label (Ss control, Ss + Bs, Ss + Hm, Ss + Bs + Hm, random)
      - fate: ultimate outcome for the individual (euthanised, metamorphosed, or died)
      - infection_load: Bd DNA quantified as genomic equivalents
  - Notes on data collection timing:
    - Salamanders were sampled at three time points
    - Frogs and toads were sampled only at the final time point

- Data quality, metadata, and context
  - Metadata include explicit variable names, descriptions, and units to support clarity and reuse.
  - Infection_load is the primary quantitative outcome, expressed in genomic equivalents.
  - Reference framework: five cited studies provide ecological and epidemiological context for Bd dynamics and host interactions.

- Accessibility, sharing, and governance
  - The metadata are designed to enable discovery, interpretation, and reuse of the dataset within the broader Bd-host literature.
  - The dataset is embedded with institutional authorship (multiple institutions in the UK and Spain) and references, supporting traceability and proper attribution.

- References and context
  - Provided references (1–5) document prior work on Bd infection dynamics, host interactions, and related amphibian disease research:
    - Fernández-Beaskoetxea et al. 2016
    - Bosch et al. 2018
    - Medina et al. 2015
    - Gabor et al. 2017
    - Hite et al. 2016