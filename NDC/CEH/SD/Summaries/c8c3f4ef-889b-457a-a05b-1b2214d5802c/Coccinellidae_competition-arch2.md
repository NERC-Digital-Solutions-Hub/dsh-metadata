# Supporting documentation for Hentley, W.T; Brien, M.N (2016). Coccinellidae competition. NERC Environmental Information Data Centre. http://doi.org/10.5285/c8c3f4ef-889b-457a-a05b-1b2214d5802c

- Purpose and scope
  - Documents laboratory experiments on interactions between invasive and native coccinellids and their shared prey, the European large raspberry aphid Amphorophora idaei.
  - Aims to identify feeding preferences and the impact of competition on feeding rates under controlled conditions.

- Organisms and sourcing
  - Invasive predator: Harmonia axyridis.
  - Native prey species: Coccinella septempunctata and Adalia bipunctata.
  - Aphid prey: Amphorophora idaei, sourced from field and lab/multiplication stocks.
  - Field-collected coccinellids from Oxfordshire, UK; some A. bipunctata sourced from a biocontrol supplier to supplement.

- Experimental design and conditions
  - Laboratory rearing: all coccinellids reared for at least one generation in controlled conditions (20 ± 1°C, 16 h light).
  - Aphid culture: maintained on raspberry (cv. Malling Landmark) under the same incubator conditions.
  - Experiment 1 (preference by larval stage)
    - Setup: circular arenas with 50 aphids (10 apterous adults and 10 nymphs each of stages I–IV) and a single larval coccinellid (stages I–IV).
    - Replication: 120 bioassays across 3 species × 4 larval stages, in 12 temporal blocks (10 assays per block).
  - Experiment 2 (competition on shared prey)
    - Setup: forced competition between two larvae (larval stage IV) in circular arenas with 25 aphids (5 adults and 5 of each nymphal stage) killed by chilling to allow staging of consumed prey.
    - Treatments: heterospecific and conspecific pairings plus a no-competitor control.
    - Replication: 90 bioassays across combinations; each assay lasted 1 hour and was video-recorded for analysis.
    - Identification: random marking of one focal larva for species identification during analysis.

- Data collection and structure
  - Experiment1.csv
    - Key fields: id, Individual coccinellid ID, block, ladybird_stage, Coccinellid lifestage, aphid_stage, aphid_lifestage, number_eaten, species, max.
  - Experiment2.csv
    - Key fields: arena, metal dish / arena, aphid_lifestage, focal_species, Focal coccinellid species, pred_species, Competing coccinellid species, eaten, painted, eaten_comp, total_aphid.
  - Data capture approach: manual counting of consumed aphid stages for Experiment 1; video analysis for Experiment 2 with marked focal individuals.

- Quality control and data integrity
  - Dataset checked manually for errors; no further quality control required noted.

- Analytical approach
  - Analysis performed in R (version 3.0.2) using the gamm4 package for generalized additive mixed models (GAMs) to assess feeding patterns and competitive effects.

- Availability and reproducibility
  - Data and methods are documented with explicit experimental conditions, groupings, and variable definitions to support reproducibility and reuse in environmental monitoring analyses.
  - DOI provides access to the data center entry for broader data accessibility.