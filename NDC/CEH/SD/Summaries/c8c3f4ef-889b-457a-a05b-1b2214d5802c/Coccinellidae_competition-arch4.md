# Supporting documentation for Hentley, W.T; Brien, M.N (2016). Coccinellidae competition. NERC Environmental Information Data Centre.

## Scope and purpose
- Documents two laboratory experiments on interactions between coccinellids (predators) and aphids (prey).
- Data are organized into two CSV datasets (Experiment1.csv and Experiment2.csv) with detailed field definitions to enable reuse, verification, and secondary analysis.
- Aimed at supporting transparency, reproducibility, and potential integration with broader data systems.

## Experimental system and organisms
- Species involved:
  - Predator: Harmonia axyridis (invasive)
  - Native prey: Coccinella septempunctata and Adalia bipunctata
- Field collection: Oxfordshire, UK, May 2013; A. bipunctata supplemented from a biocontrol supplier due to low field numbers.
- Rearing and environment:
  - Controlled lab conditions: 20 ± 1°C, 16 h photoperiod
  - Diet: mixed-age Acyrthosiphon pisum
  - Lab generation used; aphid culture maintained on raspberry (cv. Malling Landmark)
- Aphid prey: European large raspberry aphid, Amphorophora idaei, chosen as the focal prey and pest species for raspberry.

## Experimental design

- Experiment 1: prey-stage preference
  - Objective: identify preferences for specific aphid nymphal stages by larval stages of three coccinellid species.
  - Setup: circular arena; 50 aphids (10 apterous adults + 10 nymphal stage I, II, III, IV per trial); one larval coccinellid placed center; 1 h trial.
  - Replication: 10 trials per larval stage for each species (total 120 bioassays); randomized into 12 temporal blocks.
  - Outcome: aphid nymphal stage consumed; data recorded for analysis.

- Experiment 2: competition effects on feeding
  - Objective: assess impact of interspecific and intraspecific competition on feeding on a shared prey.
  - Setup: 25 aphids (cadavers used to mark nymphal stage) positioned around arena; two coccinellid larvae (larval stage IV) in center forming focal-competitor pairs.
  - Variation: heterospecific, conspecific, and control (no competitor) pairings; random marking of one larva for identification; video-recorded for analysis.
  - Procedure: 1 h trials; reciprocal pairing to swap focal species; total 90 bioassays.
  - Outcome: counts of aphid nymphal stages eaten by focal species and by competitors.

## Datasets and metadata

- Experiment1.csv
  - Key fields: id, Individual coccinellid ID, block, ladybird_stage, Coccinellid lifestage, aphid_stage, aphid_lifestage, number_eaten, species, max
- Experiment2.csv
  - Key fields: arena, metal dish / arena (replication unit), aphid_lifestage, Aphid_lifestage, focal_species, Focal coccinellid species, pred_species, Competing coccinellid species, eaten, painted, eaten_comp, total_aphid
- Metadata notes: detailed descriptors for lifestages, replication, and initial prey availability to support reproducibility and downstream analyses.

## Quality control and analysis

- Quality control: dataset checked manually for errors; no further QC required.
- Analytical methods: analyses performed in R 3.0.2 using the gamm4 package.

## Access, provenance, and reuse

- Documentation and data are archived at the NERC Environmental Information Data Centre (DOI provided in the document).
- Study conditions and data capture are described to support reproducibility and potential data integration with broader ecological datasets.

## Considerations for data leaders

- Demonstrates end-to-end data lifecycle: careful experimental design, structured and well-documented datasets, explicit metadata, manual quality checks, and a reproducible analysis workflow.
- Provides clear provenance and replication blocks, facilitating auditability and potential cross-study synthesis.
- Highlights the importance of detailed field-to-lab data lineage and standardized field naming to enhance discoverability and reuse.