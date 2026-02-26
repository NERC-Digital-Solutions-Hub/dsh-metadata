# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

## Overview
- Describes regional and temporal occurrence of plants foraged by managed honey bees (Apis mellifera) using DNA metabarcoding of pollen from honey.
- Based on the UK National Honey Monitoring Scheme (NHMS); covers the first full year (2019); future years to be released as processing completes.
- Funded by Natural Environment Research Council (NERC) and Biotechnology and Biological Sciences Research Council (BBSRC) under ASSIST program.

## Data Content
- Data describe plant taxa detected in honey samples and their regional and monthly distribution for 2019.
- Primary data product: data matrix of hive-level DNA reads by plant species.
- Brassica reads used as a covariate (oilseed rape and related crops) in analyses.
- Metadata and datasets include:
  - Taxonomy.csv: taxonomic affiliations (full binomial name, lowest taxonomic level achieved, genus, family, order, class, phylum, kingdom) and identifiers (BRCcode, NBN_ID). NA indicates not available.
  - NHMS_2019_Regional_data.csv: average regional DNA reads by plant species, plus regional honey characteristics and hive health indicators.
    - Country, Region, Yield (kg), Percentage sugar, Percentage water.
    - VROA_Had_It (Varroa mite infection probability), DFWV_Had_It (Deformed Wing Virus infection probability).
    - Species names (see taxonomy.csv) with DNA read counts.
  - NHMS_2019_Seasonal_data.csv: average monthly DNA reads by country, plus honey characteristics and disease probabilities.
    - Month (M04–M11), Yield, Percentage sugar, Percentage water.
    - VROA_Had_It, DFWV_Had_It, and species DNA read counts (see taxonomy.csv).
- Data provenance and scope:
  - 535 honey samples collected in 2019 from England, Wales, Scotland, and Isle of Man; samples from amateur and professional beekeepers.
  - Metadata includes site/location data, and, for some samples, yield and disease data.
  - All samples archived long term in the NHMS archive at CEH Wallingford.

## Methods and Quality Assurance
- Sampling and data collection:
  - Beekeepers submitted honey samples scraped from recently filed storage cells; samples accompanied by spatial and temporal metadata.
  - QA via online portal requirements, and YouTube instructional videos to standardize collection.
  - The scheme collected 535 samples in 2019; ongoing years processed as data become available.
- DNA metabarcoding workflow (vs traditional microscopy):
  - Pollen removed from honey via vacuum filtration; DNA extracted (DNeasy PowerPlant Pro Kit).
  - Amplification of DNA using Q5 High Fidelity Polymerase with Illumina-compatible adapters.
  - Sequencing on Illumina MiSeq; data processed with HONEYPI pipeline (Python 2.7):
    - Quality filtering and adapter removal.
    - DADA2 to generate Amplicon Sequence Variant (ASV) table (chimera-removed, high-quality).
    - ITS2 regions trimmed; taxonomic classification against in-house ITS2 database using naive Bayesian classifier.
    - ASV tables can be merged across sequencing runs without re-clustering.
- Data processing and reproducibility:
  - HONEYPI pipeline is open access (GitHub: hsgweon/honeypi).
  - Taxonomic identifications mapped to Taxonomy.csv; downstream analyses use ASVs rather than clustering.

## Metadata and Data Structure
- Taxonomy.csv: taxonomic details for pollen identified via meta-barcoding (species, genus, family, etc.) and associated identifiers.
- NHMS_2019_Regional_data.csv: regional data including country, region, yield, sugar and water content, disease probabilities, and DNA read counts by species.
- NHMS_2019_Seasonal_data.csv: monthly data by country with the same variables as regional data plus month.
- Table-style notes and region-month mappings are embedded in the data description (e.g., monthly breakdowns by UK regions).

## Data Access and Usage
- Primary data derived from the NHMS 2019 program; additional years to be released as processing completes.
- Data are accompanied by the HONEYPI workflow for reproducibility and potential re-analysis.
- NHMS project and methods documented in referenced literature; data suitable for analyses of foraging preferences, regional and seasonal patterns, and links to hive health indicators.

## Potential Analyses for Analysts
- Identify which plant taxa are most foraged across the UK and by region.
- Compare regional differences in plant foraging profiles and relate to agricultural/land-use patterns.
- Examine seasonality in plant foraging by month and country.
- Assess correlations between foraged plant taxa (DNA read counts) and hive health indicators (Varroa, DWV) or yields.
- Incorporate Brassica read counts as covariates to explore crop-foraging influence on overall pollen composition.
- Combine Taxonomy.csv with regional/seasonal data to produce species-level foraging maps and temporal trends.

## Limitations and Considerations
- Year 2019 only; future years pending processing and release.
- Metadata completeness: not all samples include yield or disease data; regional representation varies.
- DNA read counts are relative abundances and may be influenced by sample processing and beekeeping practices; interpretation should consider such biases.
- Some geographic/local-level analyses may be constrained by sample distribution and metadata granularity.

## Funding and References
- Funding: Natural Environment Research Council (NERC) and Biotechnology and Biological Sciences Research Council (BBSRC); grant number NE/N018125/1 (LTS-M ASSIST).
- Key references for methods:
  - Kozich et al. 2013; McMurdie & Holmes 2013; Oliver et al. 2021; Sickel et al. 2015.