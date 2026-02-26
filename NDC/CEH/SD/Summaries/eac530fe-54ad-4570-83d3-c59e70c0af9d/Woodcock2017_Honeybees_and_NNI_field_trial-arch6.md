# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

- Purpose and scope
  - Describes the effects of three neonicotinoid seed treatments (clothianidin, thiamethoxam, and a control) on honeybees (Apis mellifera) at 33 commercial oilseed rape sites across Hungary, Germany, and the UK during crop flowering (2015) with follow-up overwintering (2016).
  - Extends the linked 2017 Science paper by including detailed hive- and individual-level information and residue data.

- Study design and setting
  - Countries and sites: 12 UK, 12 Hungary, 9 Germany; sites clustered in blocks of three with random assignment of three treatments within each block.
  - Crop and exposure: Winter sown oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015; large blocks (~63 ha) per site.
  - Hives: Six honeybee hives placed per site; hives centralized to the crop; overwintering site in each country; supplementary feeding during overwintering; Varroa treatment using formic/oxalic acid per country.
  - Sampling timeline: During flowering (April–June 2015) with 4–7 day intervals; post-flower sampling and a single overwintering assessment in March 2016.

- Data collected and endpoints
  - Population metrics (Liebefeld method): worker bees, egg cells, larvae, pupae, male brood, storage cells (pollen/nectar); site medians used to summarize six hives per site.
  - Overwintering outcomes: colony strength and survival; weight data around exposure; disease and parasite covariates.
  - Residue and exposure measurements:
    - Neonicotinoid residues (clothianidin, thiamethoxam, imidacloprid) in pollen and nectar collected via bees.
    - Crop neonicotinoid expression quantified using caged bees to sample pollen/nectar from the crop.
    - Residue data include multiple matrices: pollen/bees, nectar collected from hives, and crop pollen/nectar.
  - Disease and parasites: Nosema spore load, Varroa mite infestation percentages.
  - Pollen analysis and landscape context: pollen grain identification (oilseed rape and other taxa), pollen richness, Shannon diversity; landscape composition within 1.5 km (broadleaf, grassland, arable, oilseed rape, water, urban, woodland).
  - Temporal and treatment covariates: pre-exposure, exposure, and post-exposure sampling rounds; season-specific measurements; treatment group and block; country-specific factors.

- Laboratory analyses and metrics
  - Residue quantification: LC-MS/MS with strict LoQ/LoD standards; residues below LoQ treated as half LoD; combined neonicotinoid index calculated using LD50-equivalent weighting across CTD, TMX, and IMI.
  - Disease and pests: Nosema spore counts (semi-quantitative), Varroa percents (per 100 bees).
  - Pollen analysis: pollen loads sorted and scored on a 0–5 scale for oilseed rape and other taxa; taxon richness and taxon-level diversity metrics.
  - Data processing: site medians used for population endpoints to account for non-independence among hives and skew.

- Datasets and structure
  - apis_median.csv: site-level medians (six hives per site) plus landscape and residue metrics; includes end points for flowering and overwintering, along with combined neonicotinoid indices and landscape covariates.
  - apis_allhives.csv: detailed hive-level data across all sites (33 sites × 6 hives); granular measurements for each sampling round (bee counts, brood stages, nosema, varroa, weights, etc.).
  - apis_tent.csv: residue expression data from tented exposures (pollen and nectar sampled under controlled foraging) across sites; includes ctd, tmx, imi residues with tunnel- and sample-level statistics.
  - Metadata notes: sampling counts may vary by site due to crop depletion; not all sites yielded all sample types; up to four pollen/nectar samples per tent; some datasets include combined neonicotinoid indices and LD50-adjusted measures.

- Data quality, limitations, and considerations
  - Depletion issues: crop depletion in cage/tent experiments reduced recovered pollen/nectar in some sites.
  - Sampling completeness: not all countries had identical sampling intensity; some hives/sites contributed fewer measurements.
  - Data treatment: use of median site values to mitigate within-site non-independence and skew; LD50-based correction applied to combine multiple neonicotinoid residues.
  - Covariates: disease status, Varroa pressure, Nosema, and landscape factors included to explain variation in population responses.

- How to use the data
  - Compare country- or site-specific effects of neonicotinoid seed treatments on honeybee population metrics and overwintering success.
  - Explore relationships between hive-level disease/parasite loads and exposure to treated crops.
  - Assess neonicotinoid exposure pathways by linking crop expression, hive residues, and foraging diversity.
  - Utilize landscape context and pollen diversity to understand habitat-mediated responses.
  - Use the structured datasets to reproduce analyses related to the linked Science paper and to conduct secondary analyses with self-serve, hive-level granularity.

- References and provenance
  - Primary linked paper: Woodcock B.A., et al. (2017) Countryspecific effects of neonicotinoid pesticides on honeybees and wild bees. Science, 356, 1393-1395.
  - Methodological references: EFSA pesticide risk assessment framework; pollen analysis methods; prior work on Nosema, Varroa, and bee health in neonicotinoid contexts.