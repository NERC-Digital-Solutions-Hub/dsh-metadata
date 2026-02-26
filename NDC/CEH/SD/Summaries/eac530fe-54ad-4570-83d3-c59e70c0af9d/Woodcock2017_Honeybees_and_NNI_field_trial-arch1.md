# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- Dataset describing effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam) plus a control on wild pollinators, using Apis mellifera as model.
- Primary endpoints aligned with EFSA assessments: colony strength and overwintering success; additional metrics include population counts, brood stages, and stored resources.
- Includes neonicotinoid expression in pollen/nectar, honeybee diseases, foraging preferences, and landscape context.
- Connected to the Science paper by Woodcock et al. (2017) and extends prior work with hive-level data.
- Funded by Syngenta Ltd. and Bayer CropScience (data collection year: 2015).

## Experimental design and sampling
- 33 commercial sites across three countries: UK (12), Hungary (12), Germany (9).
- Oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015; six honeybee hives per site placed centrally to the crop.
- Three neonicotinoid treatments randomly allocated within blocks of three sites per country:
  - Clothianidin (Modesto) with fungicide
  - Thiamethoxam (Cruiser) with fungicide
  - Control (fungicide only)
- Hives relocated to overwintering sites within each country; supplementary feeding provided; Varroa treated.
- Assessments at two main periods:
  - Oilseed rape flowering period (Apr–Jun 2015): Liebefeld colony metrics every 4–7 days, excluding the first early sample to reflect peak exposure.
  - Post-winter period (Mar 2016): overwintering survival and colony strength (Liebefeld).

## Data collection and endpoints
- Population metrics:
  - Liebefeld counts: worker bees, eggs, larvae, pupae, male brood, and stored pollen/nectar.
  - Overwintering survival and colony strength (single median per site across six hives).
- Neonicotinoid exposure and residues:
  - Neonicotinoid residues measured in pollen and nectar from three routes:
    - Pollen/nectar stored in hive combs
    - Nectar in honey stomachs of foraging bees
    - Pollen traps and free-flying bees
  - Compounds tracked: clothianidin (CTD), thiamethoxam (TMX), imidacloprid (IMI; not applied in.crop but analyzed).
  - Analytical method: LC-MS/MS with defined LoQ/LoD; values below LoQ set to half LoD.
  - Combined neonicotinoid metric (NNI) computed using a LD50-based correction across TMX, CTD, and IMI.
- Neonicotinoid expression in the crop:
  - Use of caged honeybee colonies to sample pollen/nectar from the treated/untreated crop.
  - Pollens/nectars collected from crop edge and then stored for analysis; may cause crop depletion.
- Disease and health covariates:
  - Nosema spore infection levels (semi-quantitative scale) pre- and post-exposure.
  - Varroa mite infestation (percentage of bees with mites) during exposure and pre-winter.
- Pollen analysis and foraging landscape:
  - Pollen grains identified to genus/species; oilseed rape pollen quantified on a 0–5 scale.
  - Landscape context within a 1.5 km radius around hives categorized into land-use types (oilseed rape, arable, grassland, woodland, etc.).
  - Pollen diversity metrics (taxon richness, Shannon diversity).
- Additional data:
  - Autopsy and disease data for hive-level and site-level analyses.
  - Metadata on sampling dates, hive placements, and exposure days.

## Data structure and key data products
- apis_median.csv
  - Site-level medians for population metrics (six hives per site); links to individual hive data.
  - Includes country, site, treatment, block, sampling dates, hive exposure days, and various hive-level metrics (bees, brood stages, nectar/pollen cells).
  - Landscape context and neonicotinoid residue summaries per site.
  - Neonicotinoid exposure metrics: ctD, tmX, imi concentrations (median, maximum, and combined NNIs) for exposure and post-exposure periods.
- apis_allhives.csv
  - Individual hive-level data for all sites (33 sites × 6 hives ≈ 198 hives); detailed time-series of population metrics, hive weights, and disease/loadings.
  - Includes pre-exposure, deployment, and repeated sampling (r1–r5) windows; per-hive exposure days and counts.
- apis_tent.csv
  - Residue expression data from crop tents over pollen/nectar collected via tented hives.
  - Includes per-site treatment, hive, and tunnel sampling details; ND/LOQ metrics for nectar and pollen for CTD/TMX/IMI; overall event counts and sampling feasibility.
- Metadata fields (examples):
  - country, site, treatment (C, CLT, TMX), block
  - r0_date, r1_date… r5_date; rX_expdays
  - bees_r0, eggs_r0, larvastage_r0, pupastage_r0, nectar_r0, pollen_r0, etc.
  - brood_max, bees_max, egg_max, larvae_max, pupa_max, nectar_max, pollen_max
  - brood_ow, bees_ow, egg_stage_ow, larvastage_ow, etc. (post-overwintering metrics)
  - osr_abundance_pollengrain, no_taxons_pollengrain, shannon_diversity_pollengrain
  - broadleaf_cover, semi_grass_cover, urban_cover, arable_cover, osr_cover
  - ctD_nectar_exp, ctD_pollen_comb_Exp, tMX_nectar_exp, imi_pollen_trap_exp, etc.
  - nnI_exp_median, nnI_peak (combined neonicotinoid index)

## Analysis-ready aspects and considerations
- Data are designed to support correlations between neonicotinoid exposure (residue concentrations and LD50-adjusted indices) and colony health outcomes (population metrics, overwintering success).
- Multiple confounds captured:
  - Disease pressures (Nosema, Varroa) and their interactions with neonicotinoid exposure.
  - Landscape composition around colonies influencing foraging resources and pollen diversity.
  - Differences in crop exposure duration and sampling windows across countries.
- Data handling notes:
  - Site medians used to summarize within-site hive data to address skewness and non-independence among hives.
  - Some sampling was incomplete due to crop depletion or logistical challenges; dataset includes trial counts per site.
- Analytical opportunities:
  - Regression models linking residue metrics (median/peak concentrations, NNIs) to colony strength and overwintering success.
  - Path analyses examining mediating roles of disease, Varroa, and landscape on pesticide effects.
  - Cross-country comparisons of country-specific exposure-response patterns.
  - Exploration of pollen diversity and OSR pollen contribution to colony health under neonicotinoid exposure.

## Limitations and caveats
- Crop depletion observed in crop-tent sampling may affect residue estimates in nectar/pollen collections.
- Imidacloprid measured but not applied in crops; its presence in pollen/nectar is reported for context.
- Data span a specific cropping system (winter oilseed rape) and neonicotinoid seed treatments; generalizability to other crops or exposure routes may be limited.
- Some variables are semi-quantitative (Nosema; pollen grain diversity) and require careful interpretation alongside quantitative measures.

## Provenance and related work
- Linked to Woodcock et al. (2017) Science paper on country-specific effects of neonicotinoids on honeybees and wild bees.
- Dataset enriches the original publication by adding hive-level details and broader residue data across multiple matrices and landscapes.
- Data collection year: 2015; authorship includes multiple European research and industry-affiliated institutions.