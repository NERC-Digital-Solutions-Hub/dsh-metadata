# A taxonomic, genetic and ecological data resource for the vascular plants of Britain and Ireland

## Overview
- A comprehensive, online-accessible data repository for native and alien vascular plants of Britain and Ireland (BI), designed for ecological, evolutionary, and conservation analyses.
- Integrates taxonomic names, unique Kew identifiers, DNA barcodes, functional traits, distribution metrics, and ecological descriptors across 3,209 extant species (plus 18 extinct).
- Aims to support rapid data retrieval and map-based analyses, with GIS-ready attributes linked to stable identifiers.

## Data architecture and contents (GIS-relevant components)
- Main dataset: BI_main.csv
  - Taxonomy: uses World Checklist of Vascular Plants (WCVP) IDs (kew_id) with links to WCVP, POWO, and IPNI.
  - Native status and origin: native/alien classifications, including archaeophyte and neophyte distinctions.
  - Distributions: 10-km hectad-based occurrence counts within Britain & Ireland, plus partitions for Great Britain, Ireland, and Channel Islands.
  - Traits and ecology: core trait and ecological attributes per species.
- Supplementary datasets
  - chrom_num_BI.csv: chromosome counts (BI-sourced data from 1898–2017, with many counts at species level).
  - GS_BI.csv and GS_Kew_BI.csv: genome size measurements (1C/2C, pg/Mbp), including BI-origin material and calibration details from Kew.
  - Detailed_sources.csv: provenance and references for all data.
- Trait and ecological data categories (selection relevant to GIS):
  - Functional traits: Specific Leaf Area (SLA), leaf area, leaf dry matter content (LDMC), seed mass, vegetative height; derived from TRY database, with species-level averages.
  - Realized niche: Ellenberg indicator values (L, F, R, N, S, T) from PLANTATT and Central European sources where BI coverage is limited.
  - Life strategy: CSR framework (Competitor, Stress-tolerator, Ruderal) with imputed values where direct data are missing.
  - Growth form and life-form: Raunkiaer categories; assessment of succulence.
  - Associated biomes and origin: biome assignments and origin region for non-natives.
  - Species distributions: presence/occurrence counts by 10-km hectads; time-windowed data.
  - Hybrid propensity: per-species scores derived from BI-hybrid records.
  - DNA barcodes: rbcL, matK, ITS2 links (BOLD) for 1,413 BI species; up to three BOLD accessions per species.
- Data coverage (for GIS planning):
  - Native status: near-complete coverage (about 99% combined).
  - Functional traits and niche indicators: variable coverage (e.g., SLA ~56%, LDMC ~47%, seed mass ~68%, leaf area ~51%, height ~75%); Ellenberg values and life-strategy data also partial but substantial.
  - Distributions: comprehensive hectad-based metrics across BI, suitable for spatial analyses.

## Taxonomy and data harmonization
- Names reconciled to minimize digitization errors using Global Names Resolver and IPNI; higher ranks aligned via NCBI and WCVP (APG IV, etc.).
- Each species documented with a unique kew_id and cross-links to WCVP, POWO, and IPNI for robust taxonomic traceability.
- Extinctions and uncertain taxa treated with transparent notes; uncertain cases flagged for exclusion from analyses if needed.

## Access, data records, and reproducibility
- Static data snapshot available via the NERC Environmental Information Data Centre (EIDC) with DOI provided.
- BI_main.csv (core taxa and attributes), plus chrom_num_BI.csv, GS_BI.csv, GS_Kew_BI.csv, and Detailed_sources.csv.
- Repository notes and structure files (Database_structure.csv) describe trait categories and data scopes.
- R package BIFloraExplorer (GitHub) provides tools for exploration, updates, and integration of new taxonomic changes.
- Data provenance and validation are documented; unpublished data (e.g., newly generated genome-size measurements) follow approved protocols.

## How this supports GIS and map-based work
- GIS-ready attributes: species distributions by 10-km hectads, native vs alien statuses, ecological and functional traits, Ellenberg indicators, biomes, and life forms enable rich thematic maps, suitability analyses, and change-detection over time.
- Taxonomic stability and linking: stable kew_id IDs and web-links allow reliable integration with external maps, databases, and PDAs (e.g., POWO, IPNI, WCVP) for layered GIS products.
- Multi-dimensional mapping: combine distribution maps with environment (Ellenberg), biomes, growth form, CSR strategies, and genomic/barcoding context for phylogeographic or trait-based GIS analyses.
- Data provenance supports reproducible cartography: clearly cited sources enable GIS users to trace each attribute back to its origin when validating map layers or performing sensitivity analyses.

## Practical considerations and limitations for GIS use
- Spatial bias: distribution metrics are not bias-corrected for sampling effort; use with awareness of potential sampling gaps.
- Trait coverage gaps: while many core traits are covered, several categories have incomplete data; cross-check trait availability before large-scale mapping.
- Non-native data: native vs alien statuses are well-supported, but some non-native trait data rely on secondary sources; ensure region-specific interpretations when mapping invasions.
- Extinct taxa: included with caveats; may require filtering for certain temporal GIS analyses.

## Technical validation and quality assurance
- Compiled from peer-reviewed literature, field guides, and established trait databases; all data sources are cited.
- Manual checks and cross-referencing performed during taxonomic reconciliation and data extraction.
- Unpublished measurements (e.g., genome sizes) generated with standard, peer-aligned methodologies; quality-control details accompany the data.

## For GIS practitioners: implementation tips
- Start with BI_main.csv to build your base map layers (taxonomy, native status, distributions, basic traits).
- Enrich maps by linking to supplementary files (chrom_num_BI.csv, GS_BI.csv, GS_Kew_BI.csv) for cytogenetic and genome-size layers.
- Use Ellenberg values and biomes to create environmental constraint maps or to drive habitat suitability models.
- Incorporate DNA barcode links (BOLD) for layers that require phylogenetic context or species verification in field maps.
- Leverage the BIFloraExplorer R package to fetch updates, validate taxonomic changes, and integrate the BI dataset into GIS workflows seamlessly.

## Summary
- The resource provides a richly integrated, GIS-friendly database of Britain and Ireland vascular plants, combining taxonomy, native status, distribution metrics, ecological traits, and genomic/barcoding data.
- It enables robust map-based analyses for ecology, evolution, and conservation planning, with clear data provenance, stable identifiers, and accessible tooling for updates and exploration.