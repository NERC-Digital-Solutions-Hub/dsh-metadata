# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

## Overview
- Describes regional and temporal occurrence of plants foraged by managed honey bees (Apis mellifera) based on DNA metabarcoding of pollen from honey.
- Source: UK National Honey Monitoring Scheme (NHMS) for 2019; first full-year dataset with future years released as processing completes.
- Funded by Natural Environment Research Council (NERC) and Biotechnology and Biological Sciences Research Council (BBSRC) under NE/N018125/1 LTS-M ASSIST.
- Data archiving and long-term preservation through the NHMS archive at CEH Wallingford.

## Datasets included
- Taxonomy.csv
  - Taxonomic affiliation of plant species identified via DNA metabarcoding.
  - Columns include: Full binomial species name, Lowest_taxa_level, Genus, Family, Order, Class, Phylum, Kingdom, BRCcode, NBN_ID.
  - Data type: alphanumeric strings; NA indicates not available for a field.
- NHMS_2019_Regional_data.csv
  - Regional DNA read counts by plant species (taxa defined in Taxonomy.csv) plus metadata.
  - Key fields: Country, Region, Yield (kg, from beekeepers), Percentage.sugar, Percentage.water, VROA_Had_It (Varroa mite probability), DFWV_Had_It (Deformed Wing Virus probability), Species names (link to Taxonomy.csv) with DNA read counts.
  - Description: Average regional DNA reads following meta-barcoding of pollen samples; also includes disease probabilities and hive yield/context data.
- NHMS_2019_Seasonal_data.csv
  - Monthly (seasonal) DNA reads by country, with same supporting metadata as regional data.
  - Key fields: Country, Month (M04=M4/April, etc.), Yield, Percentage.sugar, Percentage.water, VROA_Had_It, DFWV_Had_It, Species names (linked to Taxonomy.csv) with DNA read counts.
- Note: Both regional and seasonal datasets include species names as per taxonomy.csv, and provide numeric DNA read counts per species.

## Methods (how the data were generated)
- NHMS context
  - Beekeeping activity in the UK is extensive; 535 honey samples were collected in 2019 (England, Wales, Scotland, Isle of Man) as the scheme’s first full year.
  - Samples collected by both amateur and professional beekeepers; honey scraped from recently filled comb edges; samples returned with spatial and temporal metadata; optional yield and colony health data (Varroa and deformed wing virus) where recorded.
  - QA includes online instructional videos and an online portal requiring minimum site/location metadata before sampling packs are issued.
  - All samples archived long-term in the NHMS archive at CEH Wallingford.
- DNA metabarcoding workflow
  - Pollen extracted from honey; DNA isolated (DNeasy PowerPlant Pro Kit) and quantified.
  - Amplification with Q5 High Fidelity polymerase and MiSeq-compatible primers; sequencing via Illumina MiSeq (V3 chemistry).
  - Bioinformatics: HONEYPI pipeline (Python 2.7) used to quality-filter reads, generate ASV abundance tables (via DADA2), trim conserved ITS2 flanks, and taxonomically classify sequences against an in-house ITS2 database.
  - Data integration: ASVs aggregated to DNA read counts per plant species; Brassica DNA reads used as a covariate in analyses.
  - R-based processing: phylotyped data with phyloseq; allows merging data across sequencing runs without re-clustering.
- Metadata and data quality
  - Taxonomy and sample metadata are maintained for traceability and re-use; quality control designed to support large-scale processing and interoperability.
  - Brassica DNA reads aggregated as a single covariate; metadata include country/region, month, yield, and disease likelihoods.

## Data structure and usage notes
- Taxonomy linkage
  - Taxonomy.csv provides the authority and hierarchical classification (species to kingdom) for all pollen identifications; use BRCcode/NBN_ID to cross-reference external taxonomic identifiers if needed.
- Regional data (NHMS_2019_Regional_data.csv)
  - Contains average regional DNA reads by species, alongside yield, sugar, water content, and disease probability indicators (Varroa and Deformed Wing Virus).
  - Units and descriptions are provided for each column (e.g., Yield in kg; Percentage.sugar as percent; probabilities between 0 and 1).
- Seasonal data (NHMS_2019_Seasonal_data.csv)
  - Mirrors regional data but organized by country and month (M04–M11 mapping to April–November).
  - Useful for temporal trend analyses and for aligning honey composition with seasonal foraging.
- Sample counts
  - Table 1 (embedded in the dataset) outlines the number of honey samples contributed by country/region and month, illustrating data coverage across the UK in 2019.
- Limitations and scope
  - Data cover only the first full year (2019); subsequent years will be added as processing completes.
  - Some yield data and disease occurrence metadata were not available for all samples.
  - Regional and national coverage varies (England, Scotland, Wales, Isle of Man) with regional granularity at NUTS1-like divisions and English regions.

## Provenance, access, and governance
- Authorship and affiliations
  - Woodcock, B.A.; Oliver, A.E.; Newbold, L.K.; Gweon, H.S.; Roy, D.B.; Pywell, R.F. from CEH and University of Reading.
- Data governance
  - Primary archive at CEH Wallingford; data are prepared for reuse with explicit taxonomic and metadata documentation.
  - Data are intended to be discoverable and usable by researchers and data stewards, with clear linking between species-level identifications and taxonomic metadata.
- References and methodological grounding
  - Foundational methods and pipelines cited (Kozich et al. 2013; McMurdie & Holmes 2013; Oliver et al. 2021; Sickel et al. 2015) to support and reproduce the metabarcoding analysis and downstream processing.