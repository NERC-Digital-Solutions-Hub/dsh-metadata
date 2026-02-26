# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Describes the effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam) and a control on honeybees (Apis mellifera) across 33 commercial sites in the UK, Hungary, and Germany during oilseed rape flowering (2015) and the pre-winter period (2016).
- Builds on the linked Science paper (Woodcock et al., 2017) and extends prior data by including hive-level information.
- Includes multiple data streams: colony-level population metrics, neonicotinoid residues in pollen/nectar, neonicotinoid expression in crops, disease and parasite metrics, foraging and landscape context.
- Provided datasets include site- and hive-level summaries, as well as detailed residue measurements from different collection methods (tent approach and direct foraging).

## Experimental design and field methods
- 33 commercial sites (UK 12, Hungary 12, Germany 9) established winter sown oilseed rape in 2014; flowering in April–June 2015.
- Within-country blocks: three sites per block randomly assigned to one of three seed treatments (clothianidin, thiamethoxam, or control with fungicide only).
- Six honeybee hives placed centrally to the crop at each site; hives moved to overwintering sites after flowering.
- Overwintering managed with fondant/sugar feeding; Varroa treated with formic or oxalic acid depending on country.
- Population responses assessed at multiple intervals during flowering (April–June 2015) and once post-winter (March 2016) using Liebefeld counts.
- Crop neonicotinoid exposure quantified via caged-bee pollen/nectar sampling, and residues measured in pollen/nectar collected by bees (ambient and cage-based methods). Residues analyzed for clothianidin, thiamethoxam, and imidacloprid.
- Additional data collected: neonicotinoid expression in crops (via pollinator-captured pollen/nectar from caged bees), honeybee diseases, Varroa and Nosema infection levels, pollen grain analysis, and landscape context within a 1.5 km radius.
- Data handling: medians used at the site level to summarize hive data due to within-site hive variation and drift; samples handled with strict cold-chain procedures.

## Measurements and endpoints
- Primary EFSA endpoints: colony strength and overwintering success.
- Secondary endpoints: population metrics across hive life stages (eggs, larvae, pupae, worker bees), brood and storage cell abundance, and various disease/parasitism indicators (Nosema spores, Varroa infestation).
- Neonicotinoid exposure metrics:
  - Concentrations of clothianidin, thiamethoxam, and imidacloprid in pollen and nectar (from different collection methods).
  - Expressions in the oilseed rape crop quantified via cage-based pollen/nectar collection with a dual sampling approach (days 2 and 9), plus nectar/pollen from free-flying bees.
  - Derived indices: median and peak concentrations, overall exposure medians/peaks, and a combined neonicotinoid index (corrected using LD50 values).
- Landscape and ecological context:
  - Land-use categories around hives within 1.5 km (arable, osr, grassland, woodland, urban, water, etc.).
  - Diversity metrics from pollen analysis (taxon richness, Shannon diversity).
- Health and stressors:
  - Nosema infection rates (pre-exposure and post-exposure periods).
  - Varroa infestation percentages (during flowering and pre-winter).
- Pollen analyses:
  - Pollen grain identification and semi-quantitative scoring of OSR pollen contribution and broader foraging diversity.
- Data collection timing:
  - Flowering period sampling occurred in 4–7 day intervals, with the first sampling ignored to reflect peak crop exposure timing.

## Data content and structure
- apis_median.csv: Site-level population responses using the median value across six hives per site; includes landscape context and neonicotinoid residues. Contains fields describing country, site, treatment, block, various sampling dates, hive exposure days, biotic metrics, and residue-derived measures.
- apis_allhives.csv: Hive-level population responses and associated hive-level metrics; contains per-hive measurements across the same sampling windows, including disease and parasite indicators, pollen grain data, and landscape context at the hive level.
- apis_tent.csv: Residue expression data from pollen/nectar collected via tented hive method; includes per-site/hive metrics for nectar and pollen concentrations of clothianidin, thiamethoxam, and imidacloprid under tent conditions, plus derived exposure indices and event counts.
- trial dataset (summary): Maximum number of pollen/nectar samples collected per trial, with notes on depletion limitations and sampling feasibility.

## Variables and derived metrics
- Endpoints and counts:
  - Bees, eggs, larval stages, pupae, male brood, nectar/pollen cells, brood and wax storage cells.
  - Overwintering and post-winter metrics (brood_ow, bees_ow, egg_stage_ow, etc.).
  - Nosema_rate_exp and nosema_rate_post (semi-quantitative scales).
  - Varroa_perc_100bees_exp and varroa_perc_100bees_post (percent infestation).
- Pollen/nectar analyses:
  - Osr_abundance_pollengrain; no_taxons_pollengrain; shannon_diversity_pollengrain; tree taxa metrics.
  - Pollen/nectar concentrations of CTD, TMX, IMI (including median, peak, and exp_median/exp_peak) across multiple sample types (nectar, pollen, trapped pollen).
  - Combined neonicotinoid index nnI_exp_median and nnI_peak (LD50-corrected).
- Landscape and habitat metrics:
  - Broadleaf_cover, semi_grass_cover, urban_cover, arable_cover, osr_cover within 1.5 km.
- Crop exposure and sample details:
  - ctd_nectar_Exp, ctd_nectar_free_s1_exp, etc., and analogous TMX/IMI variables for different collection methods and days.
  - ctd_exp_median, ctd_peak; imi_exp_median, imi_peak; tmx_exp_median, tmx_peak; and corresponding tunnel/tunnel_d2/d9 metrics for tent-based studies.
- Data quality and trial details:
  - LoQ/LoD handling for residue data; number of pollen/nectar samples collected per trial; notes on sample depletion and feasibility.

## Data quality, governance, and usage notes
- Data generated with standardized protocols across three countries, enabling cross-site comparability and meta-analyses of neonicotinoid exposure and bee health outcomes.
- Residue data incorporate limit-of-quantification adjustments and corrections based on known LD50 values to derive composite exposure indices.
- Hive-level data capture within-site correlations; site medians used to summarize central tendencies due to within-site hive drift.
- Data linked to a high-profile publication (Science, 2017) and extend prior datasets by adding hive-level granularity and crop-expression measurements.
- Potential limitations noted: partial sampling due to crop depletion in the cages; variability in sampling completeness across sites and treatment groups. 

## Metadata and access
- Key metadata files described:
  - apis_median.csv: site-level medians with associated landscape and residue fields.
  - apis_allhives.csv: per-hive population and health metrics with detailed sampling records.
  - apis_tent.csv: residue expression data from tent-based pollen/nectar collection.
- The dataset provides comprehensive long-form measurements suitable for data-system thinking around data discovery, quality, and reuse by data leaders and researchers.