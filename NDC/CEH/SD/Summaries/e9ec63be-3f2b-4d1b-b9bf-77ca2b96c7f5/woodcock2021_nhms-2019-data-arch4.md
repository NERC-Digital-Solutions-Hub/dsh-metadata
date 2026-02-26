# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

## Overview
- First full-year data (2019) from the UK National Honey Monitoring Scheme (NHMS) analyzing pollen plants foraged by honey bees via DNA metabarcoding.
- 535 honey samples collected across England, Wales, Scotland, and Isle of Man in 2019; future years released as processing completes.
- Funding: Natural Environment Research Council (NERC) and Biotechnology and Biological Sciences Research Council (BBSRC) under the ASSIST program; samples archived long-term at CEH Wallingford.

## Data content and structure
- Taxonomy data (Taxonomy.csv): plant identifications from pollen with taxonomic level (species, genus, family, etc.), including Genus, Family, Order, Class, Phylum, Kingdom, and associated codes (BRCcode, NBN_ID).
- Regional data (NHMS_2019_Regional_data.csv): average regional DNA reads by country/region, month; accompanying metadata on yield (hive production), honey sugar content, water content; probability of Varroa and Deformed Wing Virus (DWV) infections; species read counts.
- Seasonal data (NHMS_2019_Seasonal_data.csv): monthly (country-level) DNA reads plus yield, sugar, water, disease probabilities, and species read counts.
- Species-level data are aligned to Taxonomy.csv for consistent naming.
- Data are presented as averages and include NA for missing values.

## Methods and data processing pipeline
- Sampling methodology: honey collected by beekeepers (amateur and professional) by scraping from recently filled combs; 535 samples with location and time metadata; some samples include colony-health data (Varroa, DWV).
- Quality assurance: standardized collection via online portal and instructional videos; mandatory metadata submission; long-term archiving at NHMS.
- DNA metabarcoding workflow:
  - Pollen removal from honey via vacuum filtration; DNA extraction with Qiagen PowerPlant Pro Kit.
  - DNA quantification and amplification using Q5 polymerase; Illumina MiSeq sequencing (V3 chemistry).
  - Amplicon sequence variants (ASVs) generated with a DADA2-like approach; ITS2 regions trimmed; taxonomic classification via in-house ITS2 database.
  - Data merged across sequencing runs using the ASV framework (no re-clustering needed).
- Data processing pipeline: HONEYPI (Python 2.7) for quality filtering, ASV generation, ITS2 trimming, and taxonomic assignment; open source at GitHub (https://github.com/hsgweon/honeypi).

## Metadata and data documentation
- Taxonomy.csv provides the taxonomic hierarchy and identifiers for pollen-derived plant species.
- NHMS_2019_Regional_data.csv and NHMS_2019_Seasonal_data.csv document region- and month-level aggregates, including disease probabilities and environmental metrics (yield, sugar, water).
- Metadata supports traceability from sample to species identifications and regional/seasonal aggregations.

## Data quality, limitations, and provenance
- DNA metabarcoding enables scalable, timely plant identification from pollen compared to microscopy, with documented QA via HONEYPI and references (Kozich et al. 2013; McMurdie & Holmes 2013; Oliver et al. 2021; Sickel et al. 2015).
- Metadata and regional/seasonal datasets include some incomplete fields (NA) and variable sample coverage by region and month, reflecting real-world field data.
- All methods and pipelines are transparently described, enabling reproducibility and cross-study comparability.

## Access, use, and future data
- 2019 data are available; future NHMS years will be released as samples are processed.
- Data archiving and the HONEYPI pipeline’s open-source status support discoverability and reuse.
- Funding and collaboration span multiple UK institutions, contributing to a collaborative data ecosystem for pollinator foraging research.

## Implications for Data Leaders
- Demonstrates end-to-end data stewardship: from standardized collection and QA to robust processing pipelines and rich metadata.
- Highlights the importance of a unified data model linking sample metadata, taxonomy, and regional/seasonal aggregates for system-level insights.
- Illustrates governance considerations: long-term archiving, open-source tooling, documentation, and cross-institution collaboration.
- Provides a scalable model for national-scale citizen science data integration with clear provenance and reproducibility.

## References
- Kozich et al. 2013; McMurdie & Holmes 2013; Oliver et al. 2021; Sickel et al. 2015.