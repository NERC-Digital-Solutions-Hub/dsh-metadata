# A taxonomic, genetic and ecological data resource for the vascular plants of Britain and Ireland

- Presents the first comprehensive data repository of native and alien vascular plants for Britain and Ireland (BI), optimized for fast online access and ecological, evolutionary, and conservation analyses.
- Core scope: 3,209 extant species (1,468 native, 1,690 alien, 51 status-unknown) and 18 formally extinct species; 26 associated traits and data types.
- Taxonomy and identifiers: all species linked to unique Kew IDs (kew_id) with links to WCVP, POWO, and IPNI for robust taxonomic traceability.

Overview of data content
- Taxonomy and nomenclature
  - Taxon names reconciled to accepted higher ranks (order, family) and World Checklist of Vascular Plants (WCVP) references.
  - Each species provided with kew_id and hyperlinks to WCVP, POWO, and IPNI pages.
- Native status and origin
  - Three datasets describing native vs non-native status: Stace (2019) codes, PLANTATT/ALIENATT, and Alien Plants (regional non-native status frameworks).
  - Non-native categories include archaeophytes, neophytes, denizens, naturalized, and related distinctions.
- Functional traits
  - Five ecologically important traits: specific leaf area (SLA), leaf dry matter content (LDMC), seed mass, leaf area, and vegetative height.
  - Averages computed from TRY trait data; maximum vegetative height included where available.
- Realized niche and environment
  - Ellenberg indicator values (L, F, R, N, S, T) from PLANTATT for BI, supplemented by Central European values (Döring) for non-native species to fill gaps.
- Life strategy and growth form
  - Grime CSR framework (Competitor, Stress-tolerator, Ruderal, and combos) derived from Electronic Comparative Plant Ecology and imputed for many species using trait data.
  - Growth form categories from TRY; Raunkiaer life-form classification for BI contexts; succulent status flagged.
- Biomes and origin
  - Associated biomes drawn from Ecoflora; non-native origin described with region-level origin aligned to TDWG WGSRPD (level 1).
- Species distributions
  - Distribution metrics as the number of 10-km hectads in BI with records, drawn from BSBI Distribution Database; GB, Ireland, and Channel Islands partitioned; note: data not bias-corrected.
- Hybrid propensity
  - Hybridization data for 641 species, resulting in 821 documented hybrids (after filtering); a per-species hybrid propensity score and a genus-weighted (scaled) score.
- Genomics, DNA barcodes, and chromosomes
  - Genome sizes: 2,117 specimens (across species), with 467 newly estimated from BI-origin material; 1C/2C values in pg and Mbp.
  - Chromosome counts: 1,410 species with BI-derived counts; broader counts compiled from multiple sources to supplement gaps.
  - DNA barcodes: 1,413 species with at least one barcode (rbcL, matK, ITS2); 935 species with data for all three sequences; hyperlinks to BOLD records.
- Data coverage and completeness
  - Comprehensive data integration across taxonomy, native status, functional traits, niche, life history, biomes, origin, distributions, hybrids, barcodes, genome sizes, and chromosome counts; coverage varies by trait and dataset.

Data structure, access, and provenance
- Data records
  - Static data release available through NERC Environmental Information Data Centre (DOI provided); BI_main.csv (main taxon-centered dataset) plus supporting files:
    - GS_BI.csv and GS_Kew_BI.csv (genome size data)
    - chrom_num_BI.csv (chromosome counts)
    - Detailed_sources.csv (data sources)
  - An R package, BIFloraExplorer, on GitHub for ongoing releases and updates.
- Data validation and quality
  - Taxonomy cross-checked with Global Names Resolver and NCBI; resolved names linked to WCVP, POWO, IPNI.
  - Data provenance clearly documented; unpublished data validated via established protocols or peer-reviewed methods; spot checks performed during extraction.
- Generation of species list and scope
  - Based on New Flora of the British Isles (Fourth Edition) with taxonomic harmonization; careful exclusion of non-flora taxa, dubious records, and problematic hybrids; extinct species noted but not always included in complete-data calculations.

Utility and potential applications for data leaders
- System-wide data perspective
  - Enables integrative analyses of biotic and abiotic drivers shaping BI flora, supports forecasting responses to climate change, biodiversity loss, land-use shifts, and emerging pests/diseases.
- User-centered data products and collaboration
  - Rich trait and distribution context supports policy colleagues, conservation planning, and cross-network collaboration for flora-wide assessments.
  - Data discoverability via kew_id and linked taxonomic pages facilitates cross-referencing with external resources and networks.
- Data quality, stewardship, and updates
  - Clear documentation of data sources, methods, and validation supports reproducibility and governance; project maintains an updating pathway (R package) to incorporate new data and taxonomic changes.
- Strategic value
  - The resource provides a unified, harmonized BI flora dataset optimized for comparative analyses, enabling rapid re-use in ecological modelling, conservation prioritization, and biodiversity monitoring across Britain and Ireland.

End notes and accessibility
- Static data release DOI available; ongoing development and updates via BIFloraExplorer (GitHub) and the associated data packages.
- Acknowledges substantial community data contributions and support from the Darwin Tree of Life Project; authorship and funding details provided.