# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

- Purpose and scope
  - Describes regional and temporal occurrence of plants foraged by managed honey bees (Apis mellifera) in the UK during the first full year of the UK National Honey Monitoring Scheme (NHMS) in 2019.
  - Data derived from DNA metabarcoding of pollen extracted from honey samples collected across England, Wales, Scotland, and the Isle of Man.
  - Aims to support understanding of bee foraging preferences and plant-pollinator interactions at regional and seasonal scales.

- Data products and files
  - NHMS_2019_Regional_data.csv: regional averages of DNA reads per plant species, plus metadata and end-user variables
    - Country, Region (NUTS1-level), Yield (hive yield reported by beekeepers), Percentage sugar in honey, Percentage water in honey
    - Disease probabilities: VROA_Had_It (Varroa mite), DFWV_Had_It (Deformed Wing Virus)
    - Species names: DNA read counts per plant species (linked to Taxonomy.csv)
  - NHMS_2019_Seasonal_data.csv: monthly (seasonal) DNA reads by country
    - Month (M04–M11 mapping to Apr–Nov), Yield, Percentage sugar, Percentage water
    - Disease probabilities and species DNA read counts
  - Taxonomy.csv: taxonomic affiliations for plant species identified via metabarcoding
    - Full binomial name and hierarchical levels (Genus, Family, Order, Class, Phylum, Kingdom)
    - Identification level (species/genus/family), alternative identifiers (BRCcode, NBN_ID)

- Methods and data generation
  - Sample collection
    - 535 honey samples collected in 2019 from England, Wales, Scotland, and Isle of Man
    - Beekeepers included both amateur and professional; samples collected from recently filled combs
    - Associated metadata includes site/location and, for a subset, honey yield and colony health indicators
  - DNA metabarcoding workflow (HONEYPI)
    - Pollen extraction from honey via vacuum filtration; DNA extraction and amplification
    - Amplicon sequencing with Illumina MiSeq (V3 kit)
    - Quality filtering, ASV generation via DADA2, and taxonomic assignment against an in-house ITS2 database
    - Data structure: hive-by-DNA reads per plant species; Brassica (oilseed rape) reads treated as a covariate
    - Pipeline is open access (HONEYPI) and designed to enable merging across sequencing runs without re-clustering
  - Quality assurance
    - Standardised sample collection guided by online instructional videos
    - Portal-based verification of required site/location data before sampling packs are issued
    - Long-term archiving of samples in the NHMS archive at CEH Wallingford

- Metadata and data structure details
  - Taxonomy.csv provides the taxonomic context for reported species identifications (species, genus, family, etc.) with associated codes (BRCcode, NBN_ID)
  - NHMS_2019_Regional_data.csv contains regional averages and per-species DNA read counts, plus yield, sugar, and water metrics and disease probabilities
  - NHMS_2019_Seasonal_data.csv provides monthly data per country, including similar metrics and per-species reads
  - The dataset notes that yield and disease metadata were not universally provided for all samples
  - Brassica (oilseed rape) reads are used as a covariate in analyses to account for a major UK flowering crop

- Context and usage notes
  - 2019 data represent the first full year of NHMS; data from subsequent years will be released as samples are processed
  - The dataset supports analysis of:
    - Geographic patterns of plant foraging by bees
    - Seasonal shifts in foraged plant taxa
    - Relationships between plant-derived pollen signals and honey characteristics (yield, sugar, water content)
    - Potential associations between foraging patterns and hive health indicators (Varroa mite and Deformed Wing Virus probabilities)
  - References for the methodology and data processing are provided (Kozich et al. 2013; McMurdie & Holmes 2013; Oliver et al. 2021; Sickel et al. 2015)

- Practical implications for data support work
  - Enables creation of self-serve data products (e.g., dashboards, pivot tables) to explore plant taxa occurrences by region and month
  - Facilitates data integration with environmental or agricultural context (e.g., crop flowering periods, land use)
  - Highlights data quality considerations and gaps (partial metadata for some samples; year-specific dataset; regional representation)
  - Provides a transparent, open-access pipeline (HONEYPI) for reproducibility and future data incorporation

- References
  - Methodological and analytical references supporting metabarcoding and data processing (Kozich et al. 2013; McMurdie & Holmes 2013; Oliver et al. 2021; Sickel et al. 2015)