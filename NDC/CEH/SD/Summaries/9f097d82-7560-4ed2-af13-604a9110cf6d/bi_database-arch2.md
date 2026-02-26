# A taxonomic, genetic and ecological data resource for the vascular plants of Britain and Ireland

## Overview
- Presents the first comprehensive, standardized data repository for native and alien vascular plants in Britain and Ireland (BI), optimized for fast online access for ecological, evolutionary and conservation analyses.
- Covers 3,209 extant species and 18 extinct species, with 26 traits and extensive genomic, ecological and distribution data.
- Linked to unique Kew taxon identifiers and includes DNA barcode data; aims to support both fundamental research and applied conservation under climate change and biodiversity loss.

## Data Scope and Content
- Taxonomy and nomenclature
  - Species list derived from the New Flora of the British Isles; names linked to World Checklist of Vascular Plants (WCVP) IDs (kew_id) and standardized higher taxonomy (family, order) with links to WCVP, POWO and IPNI.
  - Includes a column for unclear species markers to flag microspecies issues; accommodates taxonomic changes since publication.
- Native status and origin
  - Three datasets describing native vs non-native status and establishment level (native, archaeophyte, neophyte, denizen, etc.) from Stace 2019, PLANTATT/ALIENATT, and Alien Plants resources.
- Functional traits
  - Five ecologically relevant traits: Specific Leaf Area (SLA), Leaf Dry Matter Content (LDMC), seed mass, leaf area, and vegetative height; data sourced mainly from TRY with averages across available measurements.
  - Includes maximum vegetative height where available.
- Realized niche and environment
  - Ellenberg indicator values (L, F, R, N, S, T) to describe species’ environmental preferences; data from PLANTATT and Central European sources (Döring) for non-native species to ensure broader coverage.
- Life strategy and growth
  - Grime CSR classifications (Competitor, Stress-tolerator, Ruderal) with data from the Electronic Comparative Plant Ecology database; where missing, CSR strategies were imputed using trait-based methods.
  - Growth form and Raunkiaer life-form categorization; succulent status identified from TRY data.
  - Associated biomes described via Ecoflora; origins for non-natives mapped to WGSRPD regions.
- Distribution and hybridization
  - Species distributions expressed as the number of 10-km hectads in BI, drawn from BSBI Distribution Database, with GB, Ireland, and Channel Islands breakdown; data are indicative of trends (not corrected for sampling bias).
  - Hybrid propensity for 641 species (821 combinations after filtering); weighted by intrageneric combinations to account for genus size.
- Genomic and cytogenetic data
  - DNA barcodes: rbcL, matK, ITS2 data for up to 1,413 BI species; 935 species have all three markers; links to BOLD records.
  - Genome sizes: measurements for 2,117 species (including 467 BI-origin measurements from Millennium Seedbank) with 1C and 2C values; origin-aware filtering available.
  - Chromosome counts: data for 1,410 species (BI-origin counts prioritized); additional counts from Czech and Dutch flora and Plant DNA C-values database to fill gaps.
- Data records and accessibility
  - Static data hosted at NERC Environmental Information Data Centre (DOI provided); includes BI_main.csv (core list with trait and distribution data), GS_BI.csv, GS_Kew_BI.csv, chrom_num_BI.csv, and Detailed_sources.csv.
  - R package BIFloraExplorer (GitHub) for regular updates and data exploration; links to WCVP, POWO, and IPNI provided per species.

## Taxonomy, Status and Access
- Taxonomy harmonized using Global Names Resolver and NCBI, with manual checks against WCVP for unresolved names.
- Native/non-native status aligned across multiple authoritative sources, with clear distinctions for archaeophytes, neophytes, denizens, colonists, etc.
- Data fields designed for reproducibility and traceability, enabling cross-referencing of taxon concepts and nomenclatural changes.

## Functional Traits and Ecological Attributes
- Trait data compiled from TRY, with calculated species-level averages; emphasis on traits influencing ecological interactions and responses to environmental change.
- Ellenberg values and CSR classifications provide a framework for trait-based analyses and capacity to model responses to climate and habitat shifts.

## Spatial Distributions and Biogeography
- Distribution metrics derived from historical and recent occurrence data; regionally partitioned to Great Britain, Ireland, and Channel Islands for comparative analyses.
- Biome associations and geographic origins annotated to support spatial ecology and invasion biology studies.

## Genomic and Molecular Data
- DNA barcoding enhances species identification, traceability, and molecular ecological studies.
- Genome size and chromosome counts provide genomic context for evolutionary and cytogenetic investigations.

## Data Access, Validation and Reproducibility
- Data are deposited as a static release with accompanying metadata and source documentation; includes comprehensive notes on data provenance and validation.
- Technical validation involves cross-referencing multiple peer-reviewed sources, explicit taxonomic reconciliation, and quality-control checks; uncertainty markers provided for problematic taxa.
- Regular updates planned; BIFloraExplorer R package and GitHub resources enable ongoing extension and reproducibility.

## Applications for Environmental Monitoring
- Enables flora-wide, standardized monitoring of biodiversity changes, trait-environment linkages, and distributional responses under climate and land-use change.
- Facilitates data-driven conservation prioritization, red-list assessments, and forecasting of native vs alien dynamics in BI.
- Supports research and policy analysis by providing interoperable, openly accessible datasets with clear provenance and taxonomic clarity.