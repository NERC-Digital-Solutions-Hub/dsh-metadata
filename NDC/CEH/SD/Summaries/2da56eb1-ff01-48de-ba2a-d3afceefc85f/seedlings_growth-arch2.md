# Amazon Fertilization Experiment (AFEX)

## Objective and scope
- Provides standardized, multi-factor fertilization data to assess how nitrogen, phosphorus, and cations affect seedling growth in a humid tropical forest.
- Data are structured to support comparisons across treatments, seasons, and replication, enabling monitoring of environmental responses to nutrient additions.

## Study area and environmental context
- Location: KM41 reserve, ~100 km from Manaus, Brazil (02 24'S, 59 52'W) within the Biological Dynamics of Forest Fragments Project (BDFFP) area.
- Climate: humid, wet; mean annual temperature ~26.7°C; annual precipitation ~2200 mm; dry season July–September; peak rainfall March–April.
- Vegetation: dense Terra Firme rainforest; canopy 30–37 m on average, emergents up to 55 m.
- Soils: clayey red-yellow podzols and yellow latosols; highly weathered, acidic, low fertility; WRB classification geric ferrasols.
- Land-use context and site layout are represented in the KM41 reserve maps.

## Experimental design (Amazon Fertilization Experiment, AFEX)
- Start date: March 2017.
- Design: full factorial with seven nutrient treatments plus a control, total of 8 treatments.
- Replication: four replicates per treatment (including control) for 32 plots in total.
- Plot layout: 50 m × 50 m plots, arranged in four independent blocks at least 250 m apart.
- Fertilization regime: annual application divided into three events to mitigate leaching and runoff.
  - N: 125 kg N ha−1 year−1 as urea
  - P: 50 kg P ha−1 year−1 as triple superphosphate
  - CATIONS: 50 kg K ha−1 year−1 as KCl; 160 kg Ca ha−1 year−1 and 160 kg Mg ha−1 year−1 as dolomitic limestone
- Treatment combinations:
  - CONTROL
  - N
  - P
  - CATIONS
  - N+P
  - N+CATIONS
  - P+CATIONS
  - N+P+CATIONS

## Seedling sampling methodology
- Subplot layout: within each 50 m × 50 m plot, four 1 m × 1 m subplots are systematically placed inside a 30 m × 30 m area, yielding 16 subplots per treatment and 128 total subplots across all treatments.
- Seedling criteria: all individuals taller than 20 cm and with diameter at ground height (DGH) < 1 cm identified and tagged; palms and lianas not identified or sampled.
- Measurements per seedling:
  - Height: from ground to highest apical meristem
  - DGH: diameter at ground height (mm)
  - TOTAL_LEAVES: total number of leaves
  - LEAVES_WITH_HERBIVORY: number of leaves with herbivory damage
  - MORTALITY: binary death indicator (1 = dead, 0 = alive)
- Sampling schedule: every two months (bimonthly) over 12 months, totaling six replications per sub-plot (four during the rainy season, two during the dry season).

## Data file and structure
- Data file: seedlings_growth.csv
- Size and structure: 3409 data rows, 13 columns
- Columns:
  - A - CENSUS: Sampling number
  - B - MONTH: Month of sampling
  - C - DATA: Sampling day
  - D - TRT: Plot treatment (see AFEX design)
  - E - BLOCK: Block (1–4)
  - F - PLOT: Plot (1–8) within the block
  - G - SUBPLOT: Subplot number (1–4)
  - H - INDIVIDUAL: Seedling tag
  - I - DGH: Diameter at ground height (mm)
  - J - HEIGHT: Height (cm)
  - K - TOTAL_LEAVES: Total leaves
  - L - LEAVES_WITH_HERBIVORY: Leaves with herbivory
  - M - MORTALITY: 1 if dead, 0 if alive

## References and contextual foundation
- Chauvel A. (1982)
- Comita, Condit, & Hubbell (2007)
- Laurance et al. (1999)
- Lovejoy & Bierregaard (1990)
- Quesada et al. (2010, 2011)
- RADAMBRASIL (1978)
- Ranzani (1980)

## Implications for environmental monitoring and data use
- Provides a standardized dataset for evaluating nutrient addition effects on tropical seedling growth under controlled experimental conditions.
- Facilitates cross-treatment and seasonal analyses, with explicit metadata on plots, subplots, and individuals to support data integration into broader environmental monitoring portals.