# Carbon_Nitrogen_Biomass_data_Supporting.docx

## Overview
- Dataset from an ex situ growth experiment testing growth (mass) and carbon and nitrogen concentrations in birch and pine seedlings grown in soil from forest stands that are pine-only, birch-only, or a 1:1 mix.
- Study site: Hambleton Forest, Yorkshire, UK (54°13'N, 001°07'W); planted in 1961, thinned in 1998 and 2003; stands are 0.2 ha with 900 trees per stand (1.5 m spacing). Mixed stands planted as a 5x5 m checkerboard with alternating birch and pine trees.
- Seeds and seedlings were grown in controlled conditions, then destructively sampled after 19–22 weeks to measure shoot dry mass and foliar C and N concentrations.

## Study design and methods
- Soil sampling: ten replicate soil samples per stand type (birch, pine, mixed); samples are 5x5 cm, 20 cm deep, stored at 4°C and used within 5 days.
- Ex situ setup: soil samples allocated to seedling tubes (Ray Leach Cone-tainers); tubes prepared to have specific seed content (two Pinus seeds, 4–10 Betula seeds, or a mix) with stratification and surface decontamination.
- Growth conditions: 18°C, 16 hours light / 8 hours dark; careful management to achieve target seedling densities (maximizing root coverage in each tube).
- Harvest and measurements: 19–22 weeks after seed addition; seedlings assessed for ectomycorrhizal status (Myc or NM); shoots dried at 60°C; roots stored for potential future analysis; foliar carbon and nitrogen concentrations measured using a Vario EL Cube.

## Data structure and contents
- Data arrangement: organized in columns representing experimental design elements.
- Key design headers:
  - Plot_replicate
  - Stand (Pine, birch, or mixed)
  - Tube_content (Pine only, birch only, or a mixture)
  - Seedling (pine or birch)
  - Replicate (individual ex situ replicate).
- Measurements available per data row:
  - mass_g (dry mass of the seedlings, including roots and shoots)
  - foliar_CN_ratio (foliar carbon to nitrogen ratio)
  - %N (nitrogen concentration in foliage)
  - %C (carbon concentration in foliage)
  - myc_status (whether ectomycorrhizas were observed: Myc or NM)
- Data handling notes:
  - When a tube contained the same species for multiple seedlings, the corresponding data are the average of the seedlings harvested from that tube.

## Site and experimental context
- Soil samples were collected equidistantly in mixed stands to ensure balanced representation between birch and pine roots.
- The study provides a structured comparison across stand types (pine, birch, mixed) to explore how substrate composition influences seedling growth, foliar C and N status, and mycorrhizal associations.

## Reference
- Mason, B. and T. Connolly. 2016. Long-term development of experimental mixtures of Scots pine (Pinus sylvestris L.) and silver birch (Betula pendula Roth.) in northern Britain. Annals of Silviculture Research 40: 11-18