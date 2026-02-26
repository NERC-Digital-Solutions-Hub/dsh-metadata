# Supporting documentation for Hentley, W.T; Brien, M.N (2016). Coccinellidae competition. NERC Environmental Information Data Centre.

## Overview
- Laboratory-based study of predator-prey interactions and interspecific competition among three coccinellid species.
- Focal prey: Amphorophora idaei (raspberry aphid), a major pest of raspberry.
- Objectives include identifying aphid nymphal-stage preferences, and assessing how competition (hetero- and conspecific) affects feeding rates on shared prey.
- Data are organized into two experiments with separate CSV datasets and metadata.

## Experimental design and data collection
- Insect culturing
  - Predator: Harmonia axyridis (invasive) and two native UK species (Coccinella septempunctata, Adalia bipunctata).
  - Field origins: Oxfordshire, UK (May 2013); additional A. bipunctata from a biocontrol supplier.
  - Rearing: at least one lab generation in controlled conditions (20 ± 1°C, 16 h photoperiod); diet of mixed-age Acyrthosiphon pisum.
  - A. bipunctata mixed from field and supplier to minimize source bias; larvae starved 24 h before trials.
- Aphid culture
  - Species: Amphorophora idaei (raspberry aphid), maintained on raspberry cultivar Malling Landmark at 20 ± 1°C, 16 h photoperiod.
  - Initiated from field aphids at JHI (James Hutton Institute, Dundee, UK).
- Experiments
  - Experiment 1: Preference for aphid nymphal stages
    - Setup: 50 aphids per trial (10 apterous adults + 10 nymphal stage I, II, III, IV each).
    - Arena: circular dish (185 mm diameter, 25 mm high) with glass lid.
    - Procedure: one larval coccinellid placed center; after 1 h, count eaten aphids by stage.
    - Replication: 120 bioassays (10 replicates per larval stage × 3 coccinellid species × 4 stages), randomized into 12 blocks.
  - Experiment 2: Competition effects on a shared prey
    - Setup: 25 aphids arranged around arena (5 apterous adults + 5 of each four nymphal stages).
    - Prey treatment: chilled to kill but preserve tissue; cadavers placed at 25 Points.
    - Arena and focal organisms: two Coccinellid larvae (larval stage IV) in center, with either hetero- or conspecific combinations; one larva marked with paint for ID.
    - Procedure: 1 h trial with video recording; later analysis to count aphid stages eaten by each focal larva.
    - Replication: 90 bioassays (including all pairings and a no-competitor control), with arena reversals to ensure each species acts as focal in both roles.
- Metadata and blocks
  - Randomization across temporal blocks for Experiment 1.
  - Video analysis used in Experiment 2 for precise stage-specific consumption.

## Datasets and key fields
- Experiment1.csv
  - id: individual coccinellid ID
  - block: temporal block
  - ladybird_stage: lifestage of the ladybird
  - Coccinellid_lifestage: lifestage classification
  - aphid_stage: aphid stage (I-IV or adults)
  - aphid_lifestage: aphid lifestage
  - number_eaten: count of aphids eaten by aphinellid_lifestage
  - species: coccinellid species
  - max: total aphids available at start

- Experiment2.csv
  - arena: arena identifier
  - metal dish / arena: unit of replication
  - aphid_lifestage: aphid lifestage
  - Aphid_lifestage: aphid lifestage (naming variant)
  - focal_species: focal coccinellid species
  - Focal_coccinellid_species: focal predator species
  - pred_species: competing predator species
  - Competing_coccinellid_species: competing predator species
  - eaten: number of aphid lifestage eaten by focal species
  - painted: presence/absence of paint mark for ID
  - eaten_comp: number of aphid lifestage eaten by the competitor
  - total_aphid: total aphids available at start

## Quality control and provenance
- Data checked manually for errors; no further quality control required beyond manual verification.

## Analytical methods
- Data analysis conducted in R (version 3.0.2) using the gamm4 package.

## GIS-relevance and data integration considerations
- Provenance and context
  - Collection sites for field-origin specimens (Oxfordshire) and lab culture locations (JHI, Dundee, UK) provide traceable geographic context for metadata.
  - Experimental conditions (temperature, photoperiod, diet) can be documented as environmental covariates if integrating with GIS-enabled workflows.
- Data structure for mapping
  - Datasets describe experimental units (arena, blocks, larval stage, species) and outcomes (numbers eaten). These can be aggregated by species, life stage, or treatment to create map-ready summaries of feeding preferences or competition effects if linked to metadata or field data.
  - Potential spatial integration if paired with a field-based study or provenance mapping (e.g., distribution of species in Oxfordshire) to compare lab-derived preferences with field observations.
- Metadata richness and standardization
  - Two datasets with clearly defined fields enable joining by common keys (e.g., focal species, arena, block) for composite analyses.
  - Clear labeling of stages and lifestages supports harmonization with other datasets that use similar ontologies.
- Limitations for GIS use
  - Data are from controlled laboratory experiments, not field surveys; geographic interpretation is limited to origin of specimens and lab locations rather than spatially distributed observations.
  - Temporal scope is confined to experimental blocks and lab trials; external environmental variation is not spatially explicit.

## Implications for mapping and visualization
- Possible map-based outputs
  - Visualizations of feeding preferences by aphid nymphal stage aggregated by coccinellid species.
  - Comparative charts of consumption by focal vs. competitor species under different competition scenarios.
  - Provenance maps linking species origins to potential distribution or garden-scale pest management implications, if combined with field data.
- best practices
  - Maintain explicit links between Experiment1 and Experiment2 via identifiers and blocks for integrated visual analyses.
  - Use metadata fields (origin, rearing conditions, lab location) to annotate GIS layers and ensure reproducibility in map-based analyses.

## Data access notes
- Reference: Supporting documentation for Hentley, W.T; Brien, M.N (2016). Coccinellidae competition. NERC Environmental Information Data Centre.
- DOI/link: http://doi.org/10.5285/c8c3f4ef-889b-457a-a05b-1b2214d5802c