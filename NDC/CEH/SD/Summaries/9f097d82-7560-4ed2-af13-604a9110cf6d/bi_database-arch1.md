# A taxonomic, genetic and ecological data resource for the vascular plants of Britain and Ireland

- A comprehensive, unified data repository for native and alien vascular plants in Britain and Ireland (BI), designed for rapid online access to support ecological, evolutionary and conservation analyses.
- Based on the New Flora of the British Isles (Fourth Edition) with taxon names linked to unique Kew identifiers (kew_id) and DNA barcode data.
- Currently covers 3,209 extant BI species (1,468 native, 1,690 alien, 51 unknown status) and 18 formally extinct species; includes both native and alien flora, including archaeophytes and neophytes.
- Data resource comprises 26 traits plus distribution, niche descriptions, hybridization, and genomic data to enable broad trait-based and distribution analyses.

## Scope and contents

- Taxonomy and nomenclature
  - Taxon list aligned to the World Checklist of Vascular Plants (WCVP) with links to WCVP, Plants of the World Online (POWO) and IPNI; each species identified by kew_id.
  - Taxonomy reconciled to allow tracking of name changes and synonyms; includes a flag for unclear species in problematic genera.
- Native status and origin
  - Native/alien classification drawn from multiple sources (Stace 2019; PLANTATT/ALIENATT; Alien Plants).
  - Non-native statuses include archaeophytes and neophytes with establishment categories (e.g., denizen, naturalized).
- Traits and data categories (26 total)
  - Functional traits: Specific Leaf Area (SLA), leaf dry matter content (LDMC), seed mass, leaf area, vegetative height (from TRY).
  - Realized niche: Ellenberg indicator values (L, F, R, N, S, T) from PLANTATT and Central European data where BI data are sparse.
  - Life strategy: Grime CSR (Competitor, Stress-tolerator, Ruderal) with imputation for many species.
  - Growth form and life-form: Raunkiaer life forms; succulent status; growth form categories from TRY.
  - Biomes: Associated biomes (Ecoflora) such as Boreal, Mediterranean, Temperate, etc.
  - Origin and distribution: Origin region for non-natives; BSBI distribution metrics (10-km hectads, time windows).
  - Hybrid propensity: 821 hybrid combinations across 641 BI species.
  - Genomics and barcodes: Genome size (1C/2C) and chromosome counts; DNA barcodes (rbcL, matK, ITS2) where available.
- Data sources and integration
  - Core lists and trait data compiled from Stace (2019), PLANTATT, Alien Plants, BSBI distribution data, TRY, Ecoflora, and related sources.
  - Linked resources provide traceable provenance for validation and reproducibility.

## Data architecture, access and structure

- Main dataset structure
  - BI_main.csv: core taxon list with kew_id, taxonomic ranks, native status, and per-taxon trait/ecology data.
  - GS_BI.csv: genome size measurements (per species, BI-origin notes included).
  - GS_Kew_BI.csv: newly generated genome size measurements from BI-origin material (flow cytometry details provided).
  - chrom_num_BI.csv: chromosome counts (BI-origin) and additional counts from other sources.
  - Detailed_sources.csv: complete list of publications and data sources.
  - Database_structure.csv: explanations of main data categories and fields.
- Access points
  - Static release available via the NERC Environmental Information Data Centre (EIDC) with DOI provided.
  - R package: BIFloraExplorer (GitHub) for ongoing releases and exploration of BI flora data.
  - Hyperlinks included for WCVP, POWO, and IPNI within the dataset to facilitate taxonomic queries.
- Coverage and completeness
  - Genome size: measurements for 2,117 species (including 467 BI-origin measurements newly generated).
  - Chromosome counts: 1,410 species with counts (BI-origin; extended sources included).
  - DNA barcodes: 1,413 species with at least one barcode; 935 species with all three markers (rbcL, matK, ITS2).
  - Growth form: high coverage; other traits show variable coverage across species; distribution data are broadly comprehensive for BI (BSBI-based), but not bias-corrected for sampling.

## Taxonomy, native status and origins

- Names and nomenclature
  - Taxon names reconciled to WCVP IDs (kew_id) with cross-links to WCVP, POWO, and IPNI for stable references.
  - Changes in accepted names tracked; discrepancies between taxon_name and taxon_name_WCVP noted when present.
- Native vs non-native datasets
  - Three datasets provided for native/alien status to enable cross-checks and robust categorization.
  - Non-native statuses include archaeophyte and neophyte designations with establishment levels.
- Geographic origin
  - For non-native species, origin descriptions reflect likely region of introduction to BI rather than global distribution; aligned with WGSRPD regions for interoperability.

## Traits, niche, and functional data

- Functional trait data
  - SLA, LDMC, seed mass, leaf area, and vegetative height; average trait values computed from available measurements, with 0-value exclusions.
- Realized niche
  - Ellenberg indicator values (L, F, R, N, S, T) sourced from PLANTATT and Central European datasets; separate BI and Central European values retained to avoid cross-region confounding.
- Life strategy and growth form
  - CSR classifications from Electronic Comparative Plant Ecology; imputed CSR for many species using trait data and Pierce et al. methodology.
  - Raunkiaer life-form categories; succulent status identified where applicable.
- Biomes and associated ecology
  - Biome assignment drawn from Ecoflora; representative biome categories such as Boreal Montane, Mediterranean, Temperate, etc.
- Hybridization and genetics
  - Hybrid propensity measured as the number of potential hybrid combinations per species (weighted by genus intrageneric opportunities for a genotypic context).
  - Genome size (1C/2C) and chromosome counts provide cytogenetic context for population genetics and evolutionary analyses.
- DNA barcoding
  - Publicly accessible barcode data linked to BOLD pages; aggregated sequences help in species identification and genetic diversity assessments.

## Methods and generation of the BI flora

- Species list generation
  - Names digitized from the New Flora of the British Isles; filtering removed unnamed hybrids, questionable records, intergeneric hybrids, and non-flora taxa; final extant species: 3,209 plus 18 extinct.
  - Taxonomic harmonization and quality checks with Global Names Resolver, taxize, and cross-validation against NCBI and WCVP.
- Data integration
  - Trait and distribution data sourced from established references; where BI data are sparse, Central European or other regional data are used (e.g., Ellenberg values).
  - CSR, growth form, biomes, and other trait data integrated and curated to maintain consistency.
- Data provenance and validation
  - All data sources are cited in Detailed_sources.csv; validation includes spot checks during manual extraction, and alignment checks against binomial names and taxonomic authorities.
- Accessibility for analysts
  - Data released as a static dataset with an accompanying R package for ongoing development; intended to support reproducible research, model development, and policy-relevant analyses.

## Data records, validation, and quality

- Data records
  - Static BI_main.csv with taxon identifiers, taxonomy, and trait metadata.
  - Supplementary files: GS_BI.csv, GS_Kew_BI.csv, chrom_num_BI.csv; Detailed_sources.csv; Database_structure.csv.
- Technical validation
  - Data compiled from peer-reviewed guides, atlases, and datasets with full source references; unpublished data generated with validated methods (e.g., genome size via flow cytometry).
  - Matching and reconciliation performed for taxonomic names across multiple sources; manual validation for mismatches or ambiguities.
- Quality considerations
  - Distribution data are not corrected for sampling bias; users should account for uneven sampling across BI.
  - CSR classifications rely on available data; where missing, imputation methods were used with documented approaches.

## Reuse, applications and caveats for analysts

- Analytical opportunities
  - Correlations between functional traits and distribution across native and alien floras.
  - Trait-based models predicting responses to climate change, land-use change, and pest/disease pressures.
  - Comparative analyses of genome size, chromosome counts, and hybrid propensity across BI species.
  - Niche modelling using Ellenberg values alongside distribution metrics to infer realized vs potential niches.
- Data handling considerations
  - Trait coverage varies by category; some analyses should incorporate data completeness indicators.
  - Hybrid propensity and barcoding data offer cross-species insights but may be biased toward well-studied groups.
  - Use the provided provenance files to verify data lineage and replicate analyses.

## Access and usage

- Data access
  - NERC EIDC dataset with DOI provided in the project materials.
  - R package BIFloraExplorer on GitHub for programmatic access and updates.
- Contact and updates
  - Ongoing releases and taxonomic updates anticipated via the BIFloraExplorer project; dataset maintained with transparency about sources and methods.