# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Standardised counts of bacteria, fungi and micro eukaryotes abundances across geo linked sampling locations on grassland, UK (2016)

## Executive summary
- Dataset of standardised counts of taxon abundances for bacteria, fungi, and microeukaryotes from soil samples.
- Collected from paired intensive and extensive grassland systems across 32 sites in the UK, including low and high pH soils.
- Sampling occurred in winter and spring 2015–2016; DNA was extracted and taxonomic marker genes sequenced to profile microbial diversity and abundance.
- Part of the NERC U-GRASS project (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) within the Soil Security Programme.
- Lineage: field collection across 32 UK sites; DNA extraction from field-moist soil; amplicon sequencing and bioinformatics processing; data exported as CSV for deposition into the EIDC.
- Keywords: land-use, paired, grassland, UK, soil, molecular, microbial, diversity, abundance, amplicon, 16S, ITS, 18S, ribosomal, internal transcribed spacer.
- Authors and affiliations: Griffiths, R.I.; Puissant, J.; Goodall, T.I. (Centre for Ecology & Hydrology, UK).

## Protocols
- 2.1 Soil sampling
  - 32 sites with land-use contrasts (low vs. high intensity) were sampled.
  - Soil cores (15x5 cm) collected along 100 m of the land-use interface every 25 m (5 paired replicates per site).
  - Sampling period: November 2015–February 2016; cores stored frozen at -20°C prior to processing.
- 2.2 DNA extraction and quantification
  - DNA extracted from 0.25 g of field-moist soil using MoBio PowerSoil DNA isolation kit.
  - DNA quantified with Qubit dsDNA HS assay and Nanodrop.
- 2.3 Microbial diversity indices
  - Diversity indices measured: Shannon’s index and richness (via vegan in R).
  - Amplicon sequencing targets: 16S rRNA (bacteria) using V3–V4 primers; 18S rRNA (microeukaryotes) with 18S primers; ITS (fungi) using ITS primers.
  - Sequencing platform: Illumina MiSeq, 600-cycle kit; demultiplexed with Illumina Basespace.
  - Bioinformatics: quality filtering, merging, OTU clustering at 97% similarity; taxonomic assignment against GreenGenes (16S) and UNITE (ITS) with bootstrap ≥0.8.
  - Analyses: OTU data processed in R with vegan; rarefaction applied; diversity and richness metrics computed; evenness calculated as Shannon divided by log richness.

## Data structure
- The dataset comprises seven flat CSV files:
  - UgrassStandardisedCountsOfTaxonAbundances.csv
    - 450 rows × 23 columns
    - Key columns: id, latitude, longitude, Sample_ID_16S, Sample_ID_18S, Sample_ID_ITS, nanodrop, qubit, sha_bac, rich_bac, eve_bac, rich_bacn1, rich_bacn0.001, sha_fun, rich_fun, eve_fun, rich_funn1, rich_funn0.001, sha_eu, rich_eu, eve_eu, rich_eun1, rich_eun0.001
  - 16sTaxonomy.csv
    - 33,975 rows × 8 columns
    - OTU_number, kingdom, phylum, class, order, family, genus, species (bootstrap ≥ 0.8)
  - 16sAmpliconData.csv
    - 33,975 rows × 425 columns
  - 18sTaxonomy.csv
    - 24,110 rows × 8 columns
  - 18sAmpliconData.csv
    - 24,110 rows × 430 columns
  - ItsTaxonomy.csv
    - 35,750 rows × 8 columns
  - ItsAmpliconData.csv
    - 35,750 rows × 426 columns
- Each AmpliconData file contains OTU_number plus per-sample counts; Taxonomy files provide taxonomic assignments for OTUs; UgrassStandardisedCountsOfTaxonAbundances.csv cross-references samples via Sample_ID columns.

## Associated files
- Bioinformatic outputs
  - 16sAmpliconData.csv (rarefied bacterial OTU counts)
  - 16sTaxonomy.csv (bacterial OTU taxonomy)
  - 18sAmpliconData.csv (rarefied microeukaryote OTU counts)
  - 18sTaxonomy.csv (microeukaryote OTU taxonomy)
  - ItsAmpliconData.csv (rarefied fungal OTU counts)
  - ItsTaxonomy.csv (fungal OTU taxonomy)
- Analysis outputs
  - UgrassStandardisedCountsOfTaxonAbundances.csv (aggregated per-sample taxon abundances and diversity metrics)

## Data provenance and usage notes
- Collected across 32 UK grassland sites with contrasting land use to investigate how biodiversity and soil properties relate to management and climatic contexts.
- Data development and processing conducted by CEH Wallingford and Rothamsted Research; prepared for deposition into the EIDC.
- Provides a structured, cross-referenced dataset enabling analysis of microbial community composition and diversity in relation to soil health and ecosystem services across different soil types and management regimes.