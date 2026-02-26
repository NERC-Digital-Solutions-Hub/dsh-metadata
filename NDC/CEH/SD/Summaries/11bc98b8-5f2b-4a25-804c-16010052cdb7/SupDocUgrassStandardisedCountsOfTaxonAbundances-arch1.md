# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Standardised counts of bacteria, fungi and micro eukaryotes abundances across geo linked sampling locations on grassland, UK (2016)

## Executive summary
- Standardised counts of taxon abundances for bacteria, fungi, and micro eukaryotes from soil samples
- Paired intensive and extensive grassland systems across 32 sites in the UK; includes low and high pH parent soils
- Samples collected in winter/spring 2015–2016; DNA was extracted and taxonomic marker genes sequenced to assess microbial diversity
- Part of the NERC U-GRASS award, addressing soil functional change under different management and climatic scenarios
- Lineage: field sampling across 32 UK grassland sites; DNA extracted from field-moist soil; amplicon sequencing and bioinformatics at CEH, Wallingford; data exported as CSV for deposition into the EIDC
- Key terms: land-use, paired, grassland, UK, soil, molecular, microbial, diversity, amplicon, 16S, ITS, 18S

## Protocols
- 2.1 Soil sampling
  - 32 sites with a land-use intensity contrast (low vs high intensity)
  - Soil cores (15 x 5 cm) collected along 100 m of the land-use interface, every 25 m (5 paired replicates per site)
  - Sampling occurred Nov 2015–Feb 2016; samples stored at -20°C prior to processing
- 2.2 DNA extraction and quantification
  - DNA extracted from 0.25 g field-moist soil using MoBio PowerSoil kit
  - DNA quantified with Qubit dsDNA BR assay and Nanodrop
- 2.3 Microbial diversity indices
  - Amplicon sequencing for 16S (bacteria), 18S (microeukaryotes), and ITS (fungi) using Kozich et al. 2013 methodology; Illumina MiSeq with V3 chemistry, 600 cycles
  - Demultiplexing in Illumina Basespace
  - Bioinformatics: quality filtering, merging, OTU clustering at 97% similarity; taxonomic assignment via GreenGenes (16S) and UNITE (ITS/18S) with bootstrap ≥0.8
  - Diversity analyses in R using vegan: rarefaction; compute Shannon index, species richness, and evenness
  - Taxonomic ranks reported from Kingdom to Species

## Data structure
- The dataset comprises seven CSV files:
  - UgrassStandardisedCountsOfTaxonAbundances.csv
    - 450 rows x 23 columns
    - Includes: coordinates (latitude, longitude), sample IDs for 16S/18S/ITS, DNA concentration metrics (nanodrop, qubit), and diversity metrics for bacteria, fungi, and microeukaryotes (Shannon, richness, evenness; richness at >1% and >0.001% for each group)
  - 16sTaxonomy.csv (33975 rows, 8 columns)
  - 18sTaxonomy.csv (24110 rows, 8 columns)
  - ItsTaxonomy.csv (35750 rows, 8 columns)
  - 16sAmpliconData.csv (33975 rows, 425 columns)
  - 18sAmpliconData.csv (24110 rows, 430 columns)
  - ItsAmpliconData.csv (35750 rows, 426 columns)
- Each taxonomy/amplicon data file links via OTU_number to the corresponding sample identifiers in UgrassStandardisedCountsOfTaxonAbundances.csv
- Column headers in amplicon data files identify samples; taxonomy files include taxonomic assignments with bootstrap ≥0.8

## Associated files
- Bioinformatic outputs
  - 16sAmpliconData.csv
  - 16sTaxonomy.csv
  - 18sAmpliconData.csv
  - 18sTaxonomy.csv
  - ItsAmpliconData.csv
  - ItsTaxonomy.csv
- Analysis outputs
  - UgrassStandardisedCountsOfTaxonAbundances.csv

## Purpose and potential analyses
- Enable analysis of relationships between soil biodiversity (bacteria, fungi, microeukaryotes) and management intensity, soil properties, and geographic/climatic context
- Compare cross-kingdom diversity and abundance patterns across land-use contrasts
- Support modelling of soil functional changes under different agricultural practices and environmental conditions
- Provide a structured, machine-readable dataset with metadata and standardized diversity metrics for reproducible analyses and external data sharing (deposited to EIDC)