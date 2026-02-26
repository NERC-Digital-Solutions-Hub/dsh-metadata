# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

## Overview
- Describes regional and temporal occurrence of plants foraged by managed honey bees (Apis mellifera) using DNA metabarcoding of pollen from honey.
- Based on the first full year of the UK National Honey Monitoring Scheme (NHMS) in 2019; future years will be added as samples are processed.
- Aims to support environmental monitoring of pollinator foraging patterns and hive health, with outputs suitable for mapping and temporal trend analysis.
- Data generated from 535 honey samples collected across England, Wales, Scotland, and the Isle of Man; includes metadata on sample origin and limited colony health indicators.

## Methods and Data Collection
- National Honey Monitoring Scheme context:
  - Beekeeping is widespread in the UK (over 29,000 beekeepers, ~126,000 colonies); samples collected from amateur and professional beekeepers.
  - Sampling involved scraping honey from recently filled cells; samples accompanied by spatial and temporal metadata; some samples include yield and colony health data (Varroa mite presence and deformed wing virus).
  - 2019 represents the first full year of operation; year-to-year data will be released as processed.
- DNA metabarcoding approach:
  - Replaces traditional microscopy for plant-pollen identification to enable large-scale processing.
  - Pollen extracted from honey, DNA extracted, amplified, and sequenced (Illumina MiSeq V3); targeted ITS2 region for plant identification.
  - HONEYPI pipeline used to process sequences: quality filtering, DADA2 ASV generation, trimming of conserved regions, taxonomic assignment against in-house ITS2 database.
  - Outputs a hive-by-DNA reads matrix for plant taxa; Brassica (oilseed rape) reads used as a covariate in analyses.
- Quality assurance:
  - Standardized sample collection guided by online instructional videos; minimum metadata required before sampling packs are issued.
  - Samples archived long-term at CEH Wallingford.
  - HONEYPI pipeline is open-access to enable reproducibility and data merge across sequencing runs.

## Data Products and Metadata
- Taxonomy.csv:
  - Contains taxonomic affiliation for plant species identified via meta-barcoding.
  - Fields include full binomial name, lowest taxonomic level achieved (species/genus/family), and standard identifiers (BRCcode, NBN_ID) when available.
- NHMS_2019_Regional_data.csv:
  - Average regional DNA reads by country/region (NUTS1 level), plus ancillary data per region: yield (kg), honey sugar percentage, honey water percentage.
  - Includes probability values for Varroa destructor (VROA_Had_It) and Deformed Wing Virus (DFWV_Had_It) as reported by keepers.
  - Contains species DNA read counts aligned to taxonomy.csv.
- NHMS_2019_Seasonal_data.csv:
  - Average monthly DNA reads by country, plus the same set of ancillary fields as regional data (yield, sugar, water, disease probabilities) and species read counts.
- Table 1 (embedded in the dataset description):
  - An overview of the number of honey samples submitted to NHMS in 2019 by country, region, and month (M04–M11 as April–November).
- References:
  - Key methodological and analytical sources detailing the HONEYPI pipeline, meta-barcoding workflows, and foundational analyses.

## Data Access, Provenance, and Reuse
- Archive and processing:
  - All honey samples are archived long-term at the UK CEH Wallingford.
  - Data processing relies on the HONEYPI pipeline (open access) and established meta-barcoding workflows.
- Availability of subsequent years:
  - Data from years after 2019 will be released as samples are processed.
- Links to broader NHMS context:
  - NHMS portal and project references provided for methodology and data framework.

## Relevance for Environmental Monitoring
- Provides a standardized, scalable dataset to monitor:
  - Pollinator foraging landscapes through plant taxa detected in honey pollen.
  - Temporal and regional shifts in forage resources.
  - Potential links between forage diversity and colony health indicators (Varroa, DWV) at regional and monthly scales.
- Supports integration with other environmental datasets to enhance ecological health assessments and policy performance monitoring.
- Emphasizes standardized QA and data stewardship to maximize data value and accessibility to downstream users.

## Considerations for Analysts
- First-year baseline (2019) with potential gaps in metadata (yield and disease data were not available for all samples).
- Taxonomic resolution varies (species, genus, or family level) depending on meta-barcoding results.
- Data are suitable for building maps, dashboards, and time-series analyses, with Brassica reads serving as a covariate in ecological analyses.
- Potential for combining NHMS data with other environmental datasets to enhance understanding of pollinator resources and ecological health over time.