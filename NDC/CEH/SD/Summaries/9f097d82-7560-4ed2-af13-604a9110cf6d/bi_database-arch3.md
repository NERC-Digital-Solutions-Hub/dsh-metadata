# A taxonomic, genetic and ecological data resource for the vascular plants of Britain and Ireland

## Overview
- Presents a comprehensive data repository of vascular plants in Britain and Ireland (BI), including native and alien species.
- Integrates taxonomy, genetics, ecology, and conservation data for rapid online access and multi-faceted analyses.
- Encompasses 3,209 extant species and 18 extinct species (totaling 3,227 taxa) across 26 traits; linked to unique Kew taxon identifiers and DNA barcode data.
- Designed to support both fundamental science and applied conservation/management in the face of climate change and biodiversity loss.

## Data Scope and Content
- Taxonomic basis: New Flora of the British Isles (Fourth Edition) with nomenclature aligned to the World Checklist of Vascular Plants (WCVP); inclusion criteria exclude hybrids and questionable records to ensure data quality.
- Taxa: 3,209 extant species (1,468 native, 1,690 alien, 51 unknown status) and 18 extinct species; included taxa are mapped to kew_id and provide links to WCVP, POWO, and IPNI.
- Traits and data categories (26 traits in total): 
  - Taxonomy and native status (native/alien; archaeophyte vs. neophyte; establishment level)
  - Functional traits (specific leaf area SLA, leaf dry matter content LDMC, seed mass, leaf area, vegetative height; maximum height)
  - Realized niche (Ellenberg indicator values; L, F, R, N, S, T)
  - Life strategy (CSR: competitor, stress-tolerator, ruderal; imputed where missing)
  - Growth form, succulence, life-form (Raunkiaer categories)
  - Biome association (associated biomes)
  - Origin of non-native species (region of origin; WGSRPD level 1 mapping)
  - Species distributions (10-km hectad records for BI)
  - Hybrid propensity (number of reported hybrids; scaled by intrageneric opportunities)
  - DNA barcodes (rbcL, matK, ITS2; links to BOLD; coverage ~1,413 species; full three-sequence coverage for 935 species)
  - Genome size (1C/2C, in pg or Mbp) and chromosome counts (from BI-focused and external sources)
- Data integration: draws on diverse sources (Stace 2019; PLANTATT; AlienATT; Alien Plants; BSBI distributions; TRY database for traits; Ecoflora for biomes; CSR data from Electronic Comparative Plant Ecology; Ellenberg values from PLANTATT and Döring 2017; hybridization data from Hybrid flora of the British Isles; BOLD for barcodes; genome size/chromosome data from Šmarda 2019, Zonneveld 2019, Plant DNA C-values database, and in-house BI measurements).

## Taxonomy, Status and Traits
- Taxonomic standardization: names reconciled via Global Names Resolver (taxize), with NCBI and WCVP as references; includes kew_id with hyperlinks to WCVP, POWO, and IPNI.
- Native status classification: multiple datasets used (Stace 2019; PLANTATT; ALIENATT; Alien Plants) with native/alien designations and establishment levels (native, archaeophyte, neophyte, denizen, etc.).
- Trait data sources: TRY database for functional traits; Ellenberg indicator values from PLANTATT and Döring (Central Europe data) where British coverage is lacking; CSR classifications from Electronic Comparative Plant Ecology, with imputation for missing values using trait-based methods.

## Data Structure and Access
- Main data file: BI_main.csv containing taxa, kew_id, taxonomy, native status, and trait/distribution data; includes summary chromosome numbers and smallest genome size per species.
- Supporting files: GS_BI.csv (additional genome size data), GS_Kew_BI.csv (new genome size measurements from BI-origin material), chrom_num_BI.csv (chromosome counts), Detailed_sources.csv (data provenance), Database_structure.csv (structure and field explanations).
- Access points:
  - Static data release via NERC Environmental Information Data Centre (DOI provided)
  - R package: BIFloraExplorer on GitHub for reproducible querying and exploration
  - Dataset is designed for open sharing, with metadata to facilitate validation and reuse

## Data Records and Validation
- Data records are accompanied by extensive metadata and source references to enable traceability and validation.
- Validation approaches include: cross-checking against published guides, manual reconciliation for taxonomic updates, spot checks during data extraction, and careful matching of binomials to BI nomenclature.
- Acknowledges potential data gaps (e.g., CSR coverage limited to a subset of species; non-native barcode data are less complete) and documents these limitations.

## Uses for Monitoring Frameworks
- Enables policy-relevant monitoring of biodiversity, species distributions, trait-based responses to environmental change, and invasion dynamics (native vs. alien flora).
- Supports scenario testing and forecasting for climate change impacts, habitat alteration, and pest/disease pressures using standardized trait and distribution data.
- Provides a transparent data governance framework through explicit data provenance, metadata, and open access to underlying datasets.

## Challenges, Limitations and Governance
- Data gaps and uneven trait coverage across species and groups; reliance on imputed CSR classifications for many species.
- Potential data access barriers due to proprietary or non-updated metadata in some sources; ongoing need for metadata enhancement and dataset harmonization.
- Silos and fragmentation across sources historically; addressed through taxonomic harmonization and centralized BI_main data structure to facilitate coherent analyses.

## Governance, Reuse and Acknowledgments
- Data compiled from a broad consortium of institutions; Darwin Tree of Life Project and NERC funding supported the work.
- Data and accompanying tools are released to facilitate reuse in biodiversity monitoring, conservation planning, and policy evaluation.
- Acknowledges contributions from numerous researchers and institutions; provides clear data provenance and references to enable independent validation.