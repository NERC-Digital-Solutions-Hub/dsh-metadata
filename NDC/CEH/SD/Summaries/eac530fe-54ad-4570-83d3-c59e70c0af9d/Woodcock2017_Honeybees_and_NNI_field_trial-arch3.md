# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK

## Purpose and scope
- Describes population responses of honeybees (Apis mellifera) to neonicotinoid seed treatments (clothianidin and thiamethoxam) in winter-sown oilseed rape across Hungary, Germany, and the UK.
- Focuses on EFSA primary endpoints (colony strength and overwintering success) and secondary endpoints, plus pesticide exposure via residues in pollen/nectar and neonicotinoid expression in crops.
- Integrates disease metrics and landscape context to inform environmental health monitoring and policy evaluation.

## Study design and locations
- 33 commercial OSR sites: UK (12), Hungary (12), Germany (9).
- Oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015 for exposure assessment.
- Experimental design: blocks of three sites per country; randomised treatment within blocks to clothianidin, thiamethoxam, or control (fungicide-only).
- Six honeybee hives per site; hives moved to country-specific overwintering sites with supplemental feeding; Varroa treated (formic/oxalic acids by country).
- Data collection periods: during OSR flowering (April–June 2015) and post-winter (March 2016).

## Endpoints and measures
- Population metrics: Liebefeld counts of workers, eggs, larvae, pupae, male brood, brood storage; colony strength; overwintering survival; site-level medians used to address non-independence between hives.
- Exposure metrics: residues of clothianidin, thiamethoxam, and imidacloprid in pollen and nectar from bees; crop neonicotinoid expression quantified with caged-hive method; comprehensive residue profiling across multiple matrices (pollen/nectar in combs, nectar in bees, pollen traps; pre- and post-exposure).
- Combined exposure index: LD50-weighted neonicotinoid index (NNI) combining compounds for a single metric.
- Foraging and landscape context: land-use within 1.5 km (oilseed rape, cereals, legumes, grassland, woodland, urban, water); OSR pollen in pollen grain analyses; taxon richness and Shannon diversity.
- Health covariates: Nosema spp. infection rates; Varroa infestation levels; bee disease sampling as covariate in analyses.
- Post-exposure overwintering and storage metrics: brood/bee counts, disease metrics, stored pollen/nectar.
- Tent-based residue assessment: apis_tent.csv captures neonicotinoid concentrations in nectar/pollen collected via crop tenting.

## Data collection and methods
- Population assessment: Liebefeld method for hive population and brood stages; multiple sampling rounds during flowering with a final overwintering assessment.
- Disease and health: Nosema spore counts (semi-quantitative), Varroa mite infestation (percentage per 100 bees), and routine disease screening.
- Pesticide exposure: LC-MS/MS-based residue analysis for clothianidin, thiamethoxam, imidacloprid; LoQ 0.53 ng/g, LoD 0.38 ng/g; non-detects recorded as half LoD or undetected per dataset rules.
- Crop neonicotinoid expression: using caged honeybee colonies to collect pollen/nectar from treated/untreated OSR during flowering; potential crop depletion noted as a limitation.
- Pollen and nectar analyses: pollen grain identification and semi-quantitative scoring of OSR pollen presence and plant diversity; pollen traps used for foraging data.
- Data structure: per-site and per-hive data across pre-exposure, exposure, and post-exposure periods; extensive metadata on dates, exposure days, and sample counts.

## Datasets and metadata
- apis_median.csv: site-level population responses (medians across six hives per site), landscape context, and neonicotinoid residues; end-of-OSR flowering and overwintering metrics; notes on data rounding and hive removal post-flowering.
- apis_allhives.csv: hive-level data for all six hives per site; individual hive metrics across exposure periods; includes pre-, during, and post-exposure measurements.
- apis_tent.csv: residue expression data from tent trials; includes day-2 and day-9 samples for multiple neonicotinoids; aggregated measures of modelled exposure.
- trial metadata: details on the number of pollen/nectar samples collected, depletion issues, and sample counts per site/hive.
- (All datasets include extensive fields for country, site, treatment, block, sampling dates, hive counts, brood stages, nectar/pollen counts, Nosema/Varroa metrics, pollen diversity, landscape covers, and specific residue concentrations.)

## Data quality, governance, and challenges
- Metadata completeness and data sharing: dataset documentation highlights the need for transparent sharing of underlying data and metadata; data governance considerations are explicit (data management, openness, and standards).
- Data harmonisation: central tendency measures (medians) used to account for skew and lack of independence among hives; cross-country field heterogeneity acknowledged.
- Limitations and data gaps: crop depletion in caged experiments may bias residue recoveries; unequal numbers of hives/sites across countries; some sampling rounds were skipped or limited by field conditions.
- Analytical handling: below LoQ values imputed as half LoD; LD50-based weighting applied to create a combined neonicotinoid exposure index.

## Relevance for monitoring policy
- Key indicators for environmental health monitoring:
  - Colony health and overwintering survival as core outcomes.
  - Direct exposure measures: neonicotinoid residues in bee-collected pollen/nectar; crop-level neonicotinoid expression.
  - Interaction with health stressors: Nosema and Varroa prevalence as covariates.
  - Landscape context and foraging resources, including OSR pollen representation and plant diversity.
- Policy-informed data design:
  - Standardised endpoints across sites and countries enable cross-comparison and trend detection.
  - Integration of exposure data with population outcomes supports risk-based policy assessments for seed treatment regulations.
  - Comprehensive metadata supports reproducibility and data sharing while highlighting governance needs.
- Data governance implications:
  - Emphasises openness and data sharing, but notes practical barriers; underscores importance of metadata quality and transparent data management processes for monitoring frameworks.

## Notable context and provenance
- Study linked to the Science article: Woodcock et al. (2017) Countryspecific effects of neonicotinoid pesticides on honeybees and wild bees.
- Funding and affiliation: CEH (UK), Eurofins Ecotox-GmbH, Institute for Bee Research; data described as extending earlier work with additional hive-level information.
- Purpose of the dataset: to provide a comprehensive, publicly interpretable data descriptor to enable policy-relevant monitoring and evaluation of neonicotinoid seed treatments on pollinator health.