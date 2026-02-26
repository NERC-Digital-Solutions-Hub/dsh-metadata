# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

- Purpose and scope
  - Describes regional and temporal occurrence of plants foraged by managed honey bees (Apis mellifera) in 2019.
  - Data derived from DNA metabarcoding of pollen extracted from honey, as part of the UK National Honey Monitoring Scheme (NHMS).
  - First full year of NHMS data; future years will be released as samples are processed.

- Data collection and coverage
  - UK beekeeping context: >29,000 beekeepers managing ~126,000 colonies; large-scale sampling opportunity.
  - Samples: 535 honey samples collected in 2019 from England, Wales, Scotland, and the Isle of Man (amateur and professional beekeepers).
  - Metadata: samples linked to spatial and temporal data; some samples include honey yield and colony health indicators (Varroa mite and Deformed Wing Virus), but yield/disease data are not consistently available.
  - Geographic and temporal resolution: regional (NUTS1) and country-level coverage with monthly (seasonal) breakdowns; Table 1 summarizes sample distribution by country/region and month.

- Methods and quality assurance
  - Rationale: microscopy (melissopalynology) is time-consuming; DNA metabarcoding enables large-scale processing.
  - Laboratory workflow: pollen extraction from honey, DNA quantification, amplification, and sequencing (Illumina MiSeq with V3 chemistry).
  - Bioinformatics: HONEYPI pipeline (open access) processes sequences; DADA2 used to generate Amplicon Sequence Variants (ASVs); ITS2 regions trimmed; taxonomic classification against an in-house ITS2 database.
  - Output: a hive-by-DNA reads data matrix for plant species; Brassica reads used as a covariate in analyses.
  - Metadata standards: dataset includes Taxonomy.csv and NHMS_2019_Regional_data.csv and NHMS_2019_Seasonal_data.csv; provenance and software details documented.
  - Data management: samples archived long-term in the NHMS archive at CEH Wallingford; NHMS data processing tools are described and accessible.

- Datasets and metadata (key components)
  - Taxonomy.csv: taxonomic affiliation of plant species identified via pollen meta-barcoding; fields include full binomial name, lowest_taxa_level, Genus, Family, Order, Class, Phylum, Kingdom, BRCcode, NBN_ID.
  - NHMS_2019_Regional_data.csv: average regional DNA reads after meta-barcoding, honey yield, percentage sugar, percentage water, and probabilities of Varroa (VROA_Had_It) and Deformed Wing Virus (DFWV_Had_It) infections; includes per-country and per-region data with species read counts.
  - NHMS_2019_Seasonal_data.csv: average monthly DNA reads, honey yield, percentage sugar, percentage water, and disease probabilities; includes country, month, and species read counts.
  - Data notes: NA indicates missing data; regional and monthly breakdowns enable monitoring of foraging patterns and health indicators over time.

- Data governance, openness, and accessibility
  - Data sharing and transparency: underlying data intended to be shared publicly; metadata and data management practices aligned with monitoring framework principles.
  - Open-source tools: HONEYPI pipeline is open access (GitHub repository).
  - Data provenance and references: dataset accompanies methodological references detailing metabarcoding, ASV analysis, and reproducible workflows (e.g., Kozich et al., McMurdie & Holmes, Oliver et al., Sickel et al.).

- Relevance for monitoring and policy
  - Enables assessment of foraging preferences and plant taxa contributing to pollen resources for honey bees.
  - Outputs can inform landscape management, pollinator conservation, and agricultural policy by identifying plant groups important for foraging and potential health associations (through disease probability data).

- Limitations and considerations for use
  - Metadata completeness varies (yield and disease data not always available); regional/monthly sampling intensity differs by region.
  - Taxonomic resolution may vary (taxonomy.csv supports species, genus, or higher-level identifications depending on DNA data quality).
  - Data are from a single year (2019) with plans to expand to subsequent years as data processing continues.

- Funding and affiliations
  - Funded by Natural Environment Research Council (NERC) and BBSRC under the ASSIST program.
  - Collaborating institutions: NERC Centre for Ecology & Hydrology (UK) and University of Reading (UK).

- References (methodological basis)
  - Kozich et al. (2013); McMurdie & Holmes (2013); Oliver et al. (2021); Sickel et al. (2015).