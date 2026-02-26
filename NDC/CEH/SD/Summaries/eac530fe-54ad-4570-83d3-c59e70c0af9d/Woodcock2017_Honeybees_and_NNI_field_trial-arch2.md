# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK

## Overview
- Describes the effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam, and a control) on wild pollinators, focusing on honeybees (Apis mellifera) as a model system.
- Conducted across 33 commercial oilseed rape sites in the UK (12), Hungary (12), and Germany (9) during 2015.
- Builds on Woodcock et al. (2017) Science paper and extends datasets to include individual hive-level information.
- Data include EFSA primary endpoints (colony strength and overwintering success) and multiple secondary endpoints, plus neonicotinoid residue measurements and landscape context.

## Experimental design
- Crop and treatments
  - Winter-sown oilseed rape established Aug–Sept 2014; flowered Apr–Jun 2015.
  - Randomised blocks: within each of 11 country blocks, three sites received one of three treatments (clothianidin, thiamethoxam, control with fungicides only).
- Hives and placement
  - Six honeybee hives per site, located centrally or at field boundaries during flowering.
  - After flowering, hives moved to country-specific overwintering sites with access to flowering resources.
  - Varroa and disease management practices implemented (formic/oxalic acid treatments depending on country).
- Sampling and timing
  - Flowering period assessments conducted during April–June 2015 at 4–7 day intervals; overwintering assessments occurred March 2016.
  - Median values across six hives per site used to derive site-level metrics; individual hive data also recorded.
- Data collection constraints
  - Some sites had limited hive sampling due to crop depletion by many foragers; not all planned samples were collected.

## Measurements and endpoints
- Population metrics
  - Liebefeld method used to quantify hive population stages: workers, eggs, larvae, pupae, male brood, brood storage for pollen/nectar.
  - Overwintering survival and colony strength assessed on single dates per country.
- Primary EFSA endpoints
  - Colony strength
  - Overwintering success
- Secondary endpoints (during flowering and post-exposure)
  - Egg cells, larval cells, pupal cells, male brood, nectar and pollen storage cells, and total brood/bee counts.
- Disease and health covariates
  - Nosema spp. infection (semi-quantitative scoring)
  - Varroa infestation levels (percentage with mites)
  - Other disease loading; samples preserved for later molecular verification
- Foraging and pollen analysis
  - Pollen grain analysis to identify plant taxa foraging sources; diversity metrics including Shannon diversity; breadth of taxa.
  - Landscape context within a 1.5 km radius around each hive: habitat categories (oilseed rape, arable, grassland, woodland, etc.)
- Neonicotinoid exposure and residues
  - Pollen and nectar samples analyzed for clothianidin, thiamethoxam, and imidacloprid using LC-MS/MS.
  - Limit of quantification and detection; residues handled with half-LOD for below-quantification values.
  - Combined neonicotinoid index (NNI) calculated using acute LD50-based weighting to reflect overall toxicity.
  - Crop neonicotinoid expression quantified by using caged honeybee colonies to harvest pollen/nectar from the target crop.
- Crop exposure and residue context
  - Pollen/nectar residues collected from various bee-derived matrices (hive pollen, hive nectar, nectar from free-flying bees, pollen traps).
  - Post-exposure (post-flowering) residues measured to assess lingering exposure.
- Additional variables
  - Osr (oilseed rape) pollen grain abundance and diversity; taxon richness and tree pollen considerations.
  - Pesticide exposure metrics during both flowering and overwintering periods.

## Datasets included
- apis_median.csv
  - Site-level data describing honeybee population responses using the median value across six hives per site.
  - Includes country, site, treatment, block, sampling dates, hive counts, weight data, and landscape context; includes neonicotinoid residue metrics and Osr pollen data.
- apis_allhives.csv
  - Hive-level data across all 33 sites, including individual hive metrics, disease loadings, pollen grain analyses, weights, and sample dates.
- apis_tent.csv
  - Neonicotinoid residue expression from tent-based experiments where pollen/nectar were collected via tented colonies over the crop.
  - Includes ctd (clothianidin), tmx (thiamethoxam), imi (imidacloprid) concentrations in nectar and pollen, tunnel sampling details, and sample counts.
- Metadata and data dictionaries
  - Detailed metadata for apis_median.csv, apis_allhives.csv, and apis_tent.csv describing variable definitions, units, and sampling schemes.

## Methods and analytical details
- Residue analysis
  - Quantification of clothianidin, thiamethoxam, and imidacloprid using UKAS-accredited LC-MS/MS methods; LoQ and LoD specified.
  - For multi-compound metrics, concentrations combined using LD50-based correction factors to compute a unified neonicotinoid exposure index.
- Disease and health assays
  - Nosema spores counted microscopically and confirmed via molecular techniques.
  - Varroa infestation assessed as mites per 100 bees.
- Foraging and landscape
  - Pollen grains identified to genus/species where possible; Osr pollen abundance scored; landscape cover categories quantified (broadleaf, semi-grass, urban, arable, Osr, etc.).

## Timeline and geographic context
- Field establishment: August–September 2014
- Crop flowering and honeybee exposure: April–June 2015
- Overwintering assessment: March 2016
- Countries and site distribution: United Kingdom (12), Hungary (12), Germany (9)

## Relevance and use for monitoring and policy
- Provides country-specific population-level and hive-level responses of honeybees to neonicotinoid seed treatments in oilseed rape.
- Integrates ecological health endpoints with residue data, for assessing environmental health and policy performance over time.
- Data offer a comprehensive, standardized framework for cross-country environmental monitoring of pollinator responses to agrochemical seed treatments.