# Supporting documentation for Hentley, W.T; Brien, M.N (2016). Coccinellidae competition. NERC Environmental Information Data Centre. http://doi.org/10.5285/c8c3f4ef-889b-457a-a05b-1b2214d5802c

## Context and Objective
- Describes two laboratory experiments examining interactions between coccinellid predators and aphid prey.
- Species involved: invasive Harmonia axyridis (predator) and native Coccinella septempunctata and Adalia bipunctata (prey); focal aphid: Amphorophora idaei (raspberry pest).
- Aphid culture maintained on raspberry plants; coccinellids reared in controlled conditions (20 ± 1°C, 16 h photoperiod).
- Field-collected specimens used; A. bipunctata supplemented from a biocontrol supplier.
- Aims to assess prey stage preferences and the impact of competition on feeding.

## Datasets Included
- Experiment1.csv: captures predator prey-stage interactions across trials.
- Experiment2.csv: captures competition effects on predation across focal and competing predator pairings.
- Both datasets include metadata on experimental conditions, predator species, prey stages, and counts of prey eaten.
- Data were collected under controlled environmental conditions, with manual counting (Experiment 1) and video analysis (Experiment 2).

## Experimental Design
- Experiment 1: Preference for aphid nymphal stages
  - Setup: Circular arena with a fixed set of 50 aphids (ten apterous adults and ten of each nymphal stage I–IV) and a single larval coccinellid.
  - Procedure: 1-hour trials; each larval stage tested across species; 120 bioassays total, in 12 temporal blocks (10 per block).
  - Goal: Determine nymphal stage preferences of each coccinellid larval stage.
- Experiment 2: Competition effects on prey consumption
  - Setup: Circular arena with 25 aphids distributed around the edge; two coccinellid larvae (larval stage IV) placed at center in focal-competitor pairings.
  - Procedure: One larva marked for identification; 1-hour video-recorded trials; 90 bioassays, including hetero- and conspecific pairings and a no-competition control; each pairing reversed so each species could act as focal.
  - Goal: Assess how competition (hetero- or conspecific) affects prey stage consumption and feeding rates.

## Data Collection and Variables
- Experiment1.csv
  - Key columns: id, individual coccinellid ID, block, ladybird_stage, coccinellid_lifestage, aphid_stage, aphid_lifestage, number_eaten, species, max.
- Experiment2.csv
  - Key columns: arena, metal dish / arena, aphid_lifestage, aphid_lifestage, focal_species, focal coccinellid species, pred_species, competing coccinellid species, eaten, painted, eaten_comp, total_aphid.
- Data capture methods:
  - Experiment 1: manual counting of consumed aphids per trial.
  - Experiment 2: video analysis to count aphid stages eaten by each focal and competing predator; marking of focal individuals for ID.

## Quality Control
- Data checked manually for errors; no further quality control required beyond manual verification.

## Analytical Methods
- Data analysis conducted in R (version 3.0.2).
- Analysis utilized the gamm4 package, indicating generalized additive mixed models or related approaches for the observational data.

## Provenance and Materials
- Aphid culture: Amphorophora idaei from field collection (James Hutton Institute, Dundee); maintained on raspberry cv. Malling Landmark.
- Coccinellids: collected in Oxfordshire, England; reared for laboratory generations; Adalia bipunctata supplemented from a biocontrol supplier to balance field-derived individuals.
- Experimental environment: controlled room conditions (20 ± 1°C, 16 h photoperiod).
- Publication context: Supporting documentation for the 2016 study on Coccinellidae competition, with dataset accessibility via the NERC Environmental Information Data Centre.