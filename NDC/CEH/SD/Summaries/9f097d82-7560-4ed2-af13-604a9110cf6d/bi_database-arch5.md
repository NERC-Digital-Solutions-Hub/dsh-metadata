# A taxonomic, genetic and ecological data resource for the vascular plants of Britain and Ireland

## Aim
- Provide a comprehensive, standardized data repository for vascular plants in Britain and Ireland (BI), combining taxonomic, genetic, ecological, and distributional data to enable ecological, evolutionary, and conservation analyses.
- Facilitate research on native and alien flora and inform conservation decisions amid climate change and biodiversity loss.

## Data scope and contents
- Taxa and status
  - Extant flora: 3,209 species (1,468 native, 1,690 alien, 51 unknown status).
  - Extinct species: 18 (listed for potential reintroduction but not included in data completeness calculations).
- Taxonomy and identifiers
  - Names linked to World Checklist of Vascular Plants (WCVP) IDs (kew_id) with links to WCVP, Plants of the World Online (POWO), and IPNI URLs.
  - Taxonomic harmonization using Global Names Resolver and taxize; resolutions cross-checked against NCBI and WCVP.
- Datasets and structure
  - Main dataset: BI_main.csv (taxa, taxonomy, native status, distribution, trait data).
  - Supporting datasets: GS_BI.csv (chromosome-related data), GS_Kew_BI.csv (Kew-generated genome sizes with methodological notes), chrom_num_BI.csv (chromosome counts from BI material and supplementary sources), Detailed_sources.csv (data provenance).
  - Metadata and structure files: Database_structure.csv (trait coverage and definitions) and related documentation.
  - Access point: static release in the NERC Environmental Information Data Centre; R package BIFloraExplorer on GitHub for ongoing releases.
- Traits and data categories
  - Functional traits: five key traits (specific leaf area SLA, leaf area, leaf dry matter content LDMC, seed mass, vegetative height) with mean values where multiple measurements exist (sourced from TRY, with note on measurement filtering).
  - Realized niche: Ellenberg indicator values, including separate entries for British data (PLANTATT) and Central European data (Döring) to preserve region-specific assessments.
  - Life strategies: CSR (Competitor, Stress-tolerator, Ruderal, and combinations) with partial empirical data and imputed values based on trait-based methods.
  - Growth form, life-form, and succulence: Raunkiaer life-form categories; succulence identified from TRY-growth form data.
  - Associated biomes: biosphere associations (Ecoflora) mapped to recognized biome categories.
  - Origin and native status: native vs non-native designations with subcategories (archaeophyte, neophyte, denizen, naturalized, etc.) from Stace, PLANTATT, ALIENATT, and Alien Plants databases.
  - Species distributions: occurrence counts in 10-km hectads within BI over time, not corrected for sampling bias.
  - Hybrid propensity: per-species measure of hybridization potential (from Stace et al. 2015; 821 documented hybrid combinations after filtering).
  - DNA barcodes: barcode data for rbcL, matK, ITS2; hyperlinks to BOLD; 1,413 species with barcode data; 935 species with data for all three markers.
  - Genome size and chromosome counts: genome sizes (1C and 2C) and chromosome counts for BI-origin material; additional measurements integrated from Czech, Dutch flora and Plant DNA C-values database; BI-origin flag to enable filtering.
  - Associated data: genome size and chromosome data include provenance notes and measurement details; some measurements are newly generated at BI origin (Kew Millennium Seed Bank work).
- Data provenance and interoperability
  - Extensive provenance via Detailed_sources.csv; explicit attribution for all trait data and measurements.
  - Cross-references to major biodiversity information standards and resources (WCVP, POWO, IPNI; TRY; Ellenberg; CSR literature; BSBI distribution data).

## Data records and access
- Static data release
  - BI_main.csv with taxon and trait data.
  - GS_BI.csv, GS_Kew_BI.csv (genome size data), chrom_num_BI.csv (chromosome counts).
  - Detailed_sources.csv (data sources and references).
  - Database_structure.csv (data schema and trait coverage).
- Access and reuse
  - NERC EIDC DOI: static data version as of publication.
  - R package: BIFloraExplorer on GitHub for ongoing releases and taxonomic updates.
  - DNA barcode links: BOLD records linked per species; integration with nomenclature updates to reflect latest roots (kew_id).

## Technical validation and quality control
- Data compilation from peer-reviewed sources, field guides, and expert databases; full bibliographic provenance provided.
- Manual validation steps
  - Taxonomic name reconciliation and normalization.
  - Cross-checks of higher taxonomy against APG IV and related standards.
  - Spot checks during data extraction; manual alignment of synonymous names with current accepted nomenclature.
- Data integrity features
  - Clear separation of primary and supplementary trait data; explicit BI-origin filter for genome size data.
  - Documentation clarifying data coverage and limitations (e.g., incomplete CSR and trait coverage for many species).

## Practical considerations for Data Stewards
- Governance and maintenance
  - Clearly defined taxonomic backbone with stable kew_id linking to external resources; traceable updates via Detailed_sources.csv.
  - Versioned releases via NERC EIDC and BIFloraExplorer; plan for regular updates as new data emerge.
- Data quality and interoperability
  - Standardized data model enabling cross-study integration (taxonomy, native status, distribution, traits, genome size, chromosome counts, barcodes).
  - Interoperability with global plant databases (WCVP, POWO, IPNI) and trait resources (TRY; Ellenberg; CSR literature).
- Completeness and bias considerations
  - Trait data coverage varies by trait and by native vs non-native status; explicit percentages provided in the documentation (e.g., SLA, LDMC, seed mass, leaf area, vegetative height).
  - Distribution data not bias-corrected; users should account for sampling effort when interpreting counts across hectads and time windows.
- Research and decision support
  - Enables trait-based ecology, niche modeling, and climate change impact assessments for BI flora.
  - Supports conservation planning via integrated native/non-native dynamics, hybridization potential, and genomic measures.

## Endnotes and contributions
- Data assembled and validated by a multi-institutional team; authors provide guidance on data compilation, validation, and documentation.
- Collaborative acknowledgments to BSBI, Darwin Tree of Life, and Kew for datasets and support.
- Corresponding authors and institutional affiliations listed for provenance and contact.