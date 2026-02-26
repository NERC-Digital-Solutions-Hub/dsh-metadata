# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands)
UK grasslands: Standardised counts of bacteria, fungi and micro eukaryotes abundances across geo linked sampling locations on grassland, UK (2016)

## Executive summary
- Standardised counts of taxon abundances for bacteria, fungi, and microeukaryotes from soil samples across 32 UK grassland sites.
- Paired design comparing intensive vs. extensive grassland management, including sites with low and high pH soils.
- Sampling occurred in winter/spring 2015–2016; DNA extracted and taxonomic marker genes sequenced to assess microbial diversity and abundance.
- Part of the NERC U-GRASS Soil Security Programme; aims to understand soil functional change under varying management and climatic scenarios.
- Data collection, processing, and deposition: field sampling, DNA extraction, amplicon sequencing, OTU clustering, and generation of standardized abundance data; dataset deposited as CSVs into the EIDC.
- Keywords highlight connections between land-use, soil biodiversity, and soil functions across UK grasslands.

## Project context and aims
- Addresses soil security and the need to understand soil processes that underpin ecosystem services (e.g., carbon storage, nutrient cycling, water regulation) under land-use and climate change.
- Seeks to determine how biodiversity (across bacteria, fungi, and microeukaryotes) relates to soil properties and functionality under different management regimes and geographic contexts.
- Evaluates whether biodiversity components drive soil resilience and resistance to change, informing management decisions to maintain or enhance soil services.

## Study design and sampling
- 32 UK grassland sites selected to represent land-use contrasts (low vs. high intensity management).
- Soil cores (15x5 cm) collected along 100 m interfaces with 25 m sampling intervals; five paired replicates per site.
- Sampling window: November 2015 to February 2016; soils stored at -20°C prior to analysis.

## Methods

### 2.1 Soil sampling
- Calibrated to capture land-use contrasts and associated soil conditions.
- Samples prepared for chemical, physical, molecular, and functional analyses.

### 2.2 DNA extraction and quantification
- DNA extracted from 0.25 g of field-moist soil using MoBio PowerSoil kit.
- DNA quantified with Qubit and Nanodrop to assess concentration and quality.

### 2.3 Microbial diversity indices
- Amplicon sequencing conducted at CEH Wallingford:
  - 16S rRNA for Bacteria (V3–V4 region)
  - 18S rRNA for Microeukaryotes
  - ITS for Fungi
- Sequencing performed on Illumina MiSeq (V3 chemistry, 600 cycles); reads demultiplexed with Illumina Basespace.
- Data processed with in-house pipelines: quality filtering, merging, OTU clustering at 97% similarity, and taxonomic assignment (GreenGenes for bacteria; UNITE for fungi).
- Diversity analyses in R (vegan): rarefaction, Shannon index, species richness, and evenness computations.

## Data structure and contents
- Seven flat CSV files comprising the dataset:

### UgrassStandardisedCountsOfTaxonAbundances.csv
- 450 rows, 23 columns.
- Core fields: latitude, longitude; Sample_ID_16S, Sample_ID_18S, Sample_ID_ITS; nanodrop and qubit DNA concentrations; Shannon’s index, richness, and evenness for bacteria, fungi, and microeukaryotes; richness at abundance thresholds (>1%, >0.001%).

### Taxonomy and Amplicon data
- 16sTaxonomy.csv (bacteria) – 33,975 rows, 8 columns: OTU_number, kingdom, phylum, class, order, family, genus, species; bootstrap ≥ 0.8.
- 18sTaxonomy.csv (microeukaryotes) – 33,975 rows, 8 columns (similar taxonomy columns).
- ItsTaxonomy.csv (fungi) – 35,750 rows, 8 columns.

- 16sAmpliconData.csv – 42,040 rows, 425 columns: OTU counts per sample.
- 18sAmpliconData.csv – 24,110 rows, 430 columns.
- ItsAmpliconData.csv – 35,750 rows, 426 columns.
- Each file uses OTU_number to cross-reference with taxonomy files; columns include sample identifiers.

## Associated outputs and data availability
- Bioinformatic outputs:
  - 16sAmpliconData.csv, 16sTaxonomy.csv
  - 18sAmpliconData.csv, 18sTaxonomy.csv
  - ItsAmpliconData.csv, ItsTaxonomy.csv
- Analysis outputs:
  - UgrassStandardisedCountsOfTaxonAbundances.csv
- Data were generated via standardized pipelines and are organized for cross-referencing across abundance data, taxonomy, and sample metadata.

## Data access, governance and usage implications
- Data are structured for integration into monitoring, reporting, and policy evaluation workflows.
- Metadata include precise geographic coordinates, sampling times, and DNA metrics to support reproducibility and auditability.
- Emphasis on standardised, open data practices (data deposition into EIDC; clear cross-referencing between OTUs, taxonomy, and sample data) to support monitoring of soil biodiversity as an indicator of soil health and ecosystem service provision.
- The use of rarefied counts and diversity indices facilitates comparisons across sites and management regimes, aiding policy decisions aimed at sustaining soil functionality under changing management and climate.

## Relevance for monitoring frameworks
- Provides multi-taxa, DNA-based biodiversity indicators aligned with soil health and ecosystem service monitoring goals.
- Demonstrates a replicable, transparent workflow from field sampling through molecular analysis to standardized abundance metrics and diversity indices.
- Facilitates evaluation of policy and management impact on soil biodiversity and associated services across geographic and land-use contexts.
- Highlights data governance considerations (metadata completeness, data sharing, and data transformation) that are central to effective monitoring and reporting.