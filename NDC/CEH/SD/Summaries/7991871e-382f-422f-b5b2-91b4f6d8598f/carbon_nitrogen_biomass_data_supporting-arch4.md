# Carbon_Nitrogen_Biomass_data_Supporting.docx EIDC submission

## Overview
- Ex situ dataset from an experiment testing growth (mass) and carbon and nitrogen concentration in needles of birch and pine seedlings.
- Seedlings grown in soils from forest stands: Scots pine only, silver birch only, and 1:1 mixed stands.
- Focus on foliar carbon to nitrogen ratio, total C and N content, seedling dry mass, and ectomycorrhizal status.

## Study Site and Design
- Location: Hambleton Forest, Yorkshire, UK (54°13' N, 001°07' W); Forestry Commission managed.
- Stand types: birch-only, pine-only, and 1:1 mixed; planted in 1961; thinned in 1998 and 2003.
- Plots: 0.2 ha each; 900 trees per stand; mixed plots arranged in a 5x5m checkerboard pattern.
- Ex situ sampling (19 Sep 2019): ten replicate soil samples per stand; samples 5x5 cm, 20 cm deep; soil stored at 4°C for up to 5 days before use.

## Ex Situ Experiment and Procedures
- Soil samples homogenized and allocated to seedling tubes (Ray Leach Cone-tainers).
- Seed contents per tube: two pine seeds, 4–10 birch seeds, or a pine + birch combination; stratified and decontaminated with 1% hydrogen peroxide.
- Growth conditions: 18°C, 16 h light / 8 h dark; moisture maintained to promote root coverage.
- Seedlings destructively sampled between weeks 19 and 22 after seed addition.
- Harvested data: shoot dry mass, foliar carbon:nitrogen ratio, and growth notes on mycorrhizal status (ectomycorrhizal vs non-mycorrhizal). Roots stored for potential future analysis.

## Data Organization and Variables
- Data structure aligned with the experimental design using five headers:
  - Plot_replicate
  - Stand (Pine, birch, or mixed)
  - Tube_content (Pine-only, birch-only, or mixed)
  - Seedling (pine or birch)
  - Replicate (individual ex situ system derived from each plot)
- Data handling:
  - When a tube contains the same species, data represent the average across seedlings harvested from that tube.
- Measured variables:
  - foliar_CN_ratio (foliar carbon to nitrogen ratio)
  - mass_g (dry mass of the seedling, including roots and shoots)
  - myc_status (Myc = observed ectomycorrhizas; NM = non-mycorrhizal)
  - %N (nitrogen concentration in foliage)
  - %C (carbon concentration in foliage)

## Key Outputs and Implications
- Enables comparison of how stand origin (birch, pine, mixed) influences seedling growth, foliar C and N content, and mycorrhizal associations.
- Provides a structured, findable data asset with metadata-style organization suitable for integration into broader data communities and reproducible analyses.
- Data reference contextualizes within long-term mixtures study (Mason & Connolly, 2016). 

## Reference
- Mason, B. and T. Connolly. 2016. Long-term development of experimental mixtures of Scots pine (Pinus sylvestris L.) and silver birch (Betula pendula Roth.) in northern Britain. Annals of Silviculture Research 40: 11-18