# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Standardised counts of bacteria, fungi and micro eukaryotes abundances across geo linked sampling locations on grassland, UK (2016)

## Executive summary
- Standardised counts of taxon abundances for bacteria, fungi, and microeukaryotes from soil across 32 UK grassland sites, with paired low/high intensity land-use contexts.
- Samples collected winter–spring 2015–2016; DNA extraction and high-throughput amplicon sequencing used to profile microbial diversity and abundance.
- Part of the NERC U-GRASS Soil Security Programme; aims to understand soil functional change under different management and climatic scenarios.

## Data lineage and collection
- 32 grassland sites across the UK, each with a low vs high intensity management contrast.
- Soil cores (15x5 cm) collected along 100 m transects (every 25 m), 5 paired replicates per site; Nov 2015–Feb 2016; stored at -20°C.
- DNA extracted from 0.25 g field-moist soil using MoBio PowerSoil kit; quantified by Nanodrop and Qubit.
- Amplicon sequencing for 16S (bacteria), 18S (microeukaryotes), and ITS (fungi) using Kozich 2013 approach; Illumina MiSeq with V3 chemistry (600 cycles).
- OTUs clustered at 97% similarity; taxonomy assigned against GreenGenes (bacteria) and UNITE (fungi) with bootstrap ≥0.8.
- Diversity analyses performed in R with vegan; data rarefied to compute Shannon’s index, richness, and evenness.

## Data structure and files
- Seven flat CSV files:
  - UgrassStandardisedCountsOfTaxonAbundances.csv: 450 rows x 23 columns; contains coordinates, Sample_IDs for 16S/18S/ITS, DNA quantifications (nanodrop, qubit), and diversity metrics (Shannon, richness, evenness) for bacteria, fungi, and microeukaryotes; richness at >1% and >0.001% abundance.
  - 16sTaxonomy.csv, 18sTaxonomy.csv, ITS Taxonomy.csv: OTU taxonomic assignments (kingdom→species) with bootstrap ≥0.8; thousands of OTUs.
  - 16sAmpliconData.csv, 18sAmpliconData.csv, ITS AmpliconData.csv: OTU count tables by sample; ~34k–35k rows with 425–430 columns; OTU_number plus sample identifiers.
- Associated outputs include rarefied count tables and linked taxonomy files for cross-referencing via OTU numbers.

## Data quality, processing and standards
- In-house pipelines used for quality filtering, sequence merging, and 97% OTU clustering; taxonomic assignments anchored to GreenGenes (bacteria) and UNITE (fungi) with bootstrap ≥0.8.
- Diversity metrics computed using vegan in R; with rarefied data to enable comparability across samples.
- Metadata fields include sequencing quality measures and sample metadata; data deposited to EIDC for long-term access.

## Data governance, access and provenance
- Clear data lineage from field collection to DNA processing, sequencing, data processing, and deposition.
- Cross-referencing enabled by consistent identifiers (Sample_IDs, OTU_numbers) across counts, taxonomy, and amplicon data.
- Project: NERC NE/M017125/1; data and outputs documented for reuse and meta-analysis.

## Practical considerations for data stewards
- Large, multi-file dataset requiring strict ID consistency across 16S/18S/ITS counts and taxonomy files.
- Documentation needed on pipelines, parameters (e.g., 97% clustering, bootstrap threshold), and reference databases to support reproducibility.
- Plan for versioning and updates if reprocessing or reannotation occurs; consider linking to raw data and processed outputs separately.

## Potential reuse and applications
- Examine relationships among soil biodiversity, soil properties, and ecosystem services under varying management and climate scenarios.
- Compare intensive vs extensive farming impacts on microbial communities and soil function (C storage, nutrient cycling, GHG regulation).
- Inform models of soil resilience and guide sustainable land-use practices across grassland and cropland systems.