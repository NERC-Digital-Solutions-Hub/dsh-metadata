# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands)

## Executive summary
- Standardised counts of taxon abundances (bacteria, fungi, micro eukaryotes) from soil samples across 32 UK grassland sites with paired intensive and extensive management and varying soil pH.
- Samples collected in winter–spring 2015–2016; DNA extracted and taxonomic marker genes analyzed via high-throughput sequencing to assess microbial diversity and abundance.
- Aimed to understand soil functional change under different management and climatic scenarios as part of the NERC U-GRASS Soil Security Programme.

## Aims and scientific context
- Investigate relationships between soil biodiversity, soil properties, and functionality under diverse management regimes.
- Determine how biodiversity components contribute to soil resistance and resilience to land-use and climate change.
- Use molecular approaches to characterize soil biodiversity and link it to biogeochemical processes and ecosystem services (e.g., carbon storage, nutrient cycling).

## Methods and data collection
- Field sampling: 32 sites across the UK with low–high intensity land-use contrasts; soil cores (15x5 cm) collected along 100 m of land-use interface at five paired replicates per site; sampling Nov 2015–Feb 2016; samples stored at -20°C.
- DNA extraction and quantification: total soil DNA extracted using MoBio PowerSoil kit; quantified with Qubit fluorometer and Nanodrop.
- Microbial diversity assessment: taxonomic amplicon sequencing for 16S (bacteria), 18S (microeukaryotes), and ITS (fungi) using Illumina MiSeq (V3 chemistry, 600 cycles); demultiplexed and processed with in-house pipelines; OTUs clustered at 97% similarity; taxonomic assignments via GreenGenes (bacteria) and UNITE (fungi).
- Diversity analysis: R Vegan package used to compute Shannon’s index, species richness, and evenness after rarefaction.

## Data structure and contents
- Seven primary CSV files comprising the dataset:
  - UgrassStandardisedCountsOfTaxonAbundances.csv (450 rows, 23 columns): site and sample metadata (latitude/longitude, unique sample IDs for 16S/18S/ITS), DNA concentration metrics (Nanodrop, Qubit), and diversity metrics (Shannon, richness, evenness for bacteria, fungi, and microeukaryotes) plus richness at various abundance thresholds.
  - 16sTaxonomy.csv (33,975 rows, 8 columns): OTU taxonomic assignments for bacteria (kingdom to species) with bootstrap threshold ≥ 0.8.
  - 18sTaxonomy.csv (24,110 rows, 8 columns): OTU taxonomic assignments for microeukaryotes.
  - ItsTaxonomy.csv (35,750 rows, 8 columns): OTU taxonomic assignments for fungi.
  - 16sAmpliconData.csv (33,975 rows, 425 columns): rarefied bacterial OTU counts per sample.
  - 18sAmpliconData.csv (24,110 rows, 430 columns): rarefied microeukaryote OTU counts per sample.
  - ItsAmpliconData.csv (35,750 rows, 426 columns): rarefied fungal OTU counts per sample.
- Column relationships: OTU numbers link AmpliconData files to Taxonomy files; sample identifiers in AmpliconData correspond to Sample_ID columns in UgrassStandardisedCountsOfTaxonAbundances.csv.
- Descriptions emphasize cross-referencing across taxonomic levels and samples.

## Associated outputs and data handling
- Associated bioinformatic outputs:
  - 16sAmpliconData.csv, 16sTaxonomy.csv (bacterial OTUs and taxonomy)
  - 18sAmpliconData.csv, 18sTaxonomy.csv (microeukaryotes)
  - ItsAmpliconData.csv, ItsTaxonomy.csv (fungi)
- Primary analysis output: UgrassStandardisedCountsOfTaxonAbundances.csv (standardised taxon abundance counts used for downstream analyses)

## Context, significance, and potential uses
- Addresses soil security and the provision of ecosystem services by linking soil biodiversity with management and climate variables.
- Enables monitoring of soil microbial communities across land-use contrasts and geographic contexts, supporting assessments of environmental health and policy performance over time.
- The standardized dataset supports cross-site comparisons, tracking changes in soil biodiversity, and relating these to soil functions such as nutrient cycling and carbon storage.

## Access and data management
- Data exported to and deposited in the EIDC; standardized CSV formats with explicit field descriptions, units, and cross-referencing identifiers.
- Clear documentation of protocols, sampling design, and data processing to support reproducibility and integration into environmental monitoring workflows.