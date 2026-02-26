# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019' deposited in the Environmental Information Data Centre repository

## Overview
- Landscape-scale study across three alpine grassland sites in the Oetztal Alps, Tyrol, Austria, examining shrub expansion (Calluna vulgaris and Vaccinium spp.) and climate-related effects on soil biogeochemistry and microbial communities.
- Data collected include abiotic soil properties, microbial biomass and community composition, enzyme activities, soil respiration, PLFA biomarkers, and extensive DNA-based microbial profiling (16S for bacteria; ITS2 for fungi).
- Two interconnected experiments: a broadscale vegetation manipulation and a snow-vegetation manipulation to disentangle effects of shrub expansion and snow cover.
- Data are organized into multiple csv files and sequencing tables; raw sequence data are deposited or planned for deposition at ENA.

## Field sites and experimental design
- Sites: Obergurgl, Soelden, and Vent in the Tyrolean Alps; shallow podzol soils; elevations 2279–2472 m; mean site pH ~4.8–5.1; mean site C:N ~16.9–18.5.
- Treatments (2 m x 2 m plots): shrub-invaded, grass-control (non-invaded), shrub removal; randomized block design with 9 blocks per site (n ≈ 27 per treatment initially; excluded plots due to instrument failure reducing total to 68 plots).
- Snow-vegetation manipulation at Vent: 48 plots with cross design of snow removal vs snow cover and three vegetation treatments, enabling mechanistic studies of snow/shrub effects on soil processes.
- Notable data governance point: 8 plots at Obergurgl and 5 plots at Soelden were excluded from analyses due to instrument failure.

## Data files and structure
- Broadscale_Soil_micro_env.csv: metadata and soil abiotic, PLFA, enzyme activity, and related variables for the landscape-scale broadscale experiment. Key columns include plot_ID, site, veg (vegetation treatment), geographic coordinates, soil chemistries (pH, %N, %C, CN ratio), soil moisture, inorganic N (NH4+, NO3−), DON, TN, TOC, microbial biomass (MicBN, MicBC), and enzyme activities (nagr, phor, glcr, cbhr, xylr, perr, poxr, urer).
- Snow_Veg_manipulation_Soil_micro_env.csv: metadata and soil/biogeochemical data for the snow-vegetation manipulation experiment. Includes similar variables as Broadscale file plus snow treatment (snow vs control) and soil respiration (soilres).
- Broadscale_16S_seq_table and Broadscale_ITS_seq_table: OTU/ASV tables for bacterial (16S) and fungal (ITS) communities; post-rarefaction, with sample names aligned to Broadscale_Soil_micro_env.csv.
- Broadscale_16S_taxa and Broadscale_ITS_taxa: taxonomic information for the OTUs/ASVs.
- Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table: OTU/ASV tables for the snow-vegetation manipulation samples; taxonomic information in Snow_Veg_manipulation_16S_taxa and Snow_Veg_manipulation_ITS_taxa.
- Raw sequencing data: undergoing deposition at the European Nucleotide Archive (ENA).
- Data processing notes: sequences processed with DADA2; rarefaction depths and mapping to GreenGenes v13.8 (16S) and UNITE v7.2 (ITS) for taxonomy.
- 2-step Illumina PCR protocol documents and primer sequences included for reproducibility and provenance.

## Field sampling and laboratory analyses
- Field sampling: July 22–24, 2019; soil cores (diameter 2 cm, depth 10 cm) taken from five random locations per plot; cores pooled and homogenised; vegetation/litter removed.
- Sample handling: portions allocated for DNA/RNA preservation in DNA/RNA shield; field lysis performed; lysates stored at -80°C and shipped to UK Centre for Ecology and Hydrology.
- Additional analyses: soil was sieved (4 mm) and stored at 4°C before enzymatic and biogeochemical assays at downstream labs.
- Biogeochemical measurements: plant-available NH4+-N and NO3−-N (via 1 M KCl extraction) and DON (via water extraction); mineralisation rates after 14 days at 25°C; dissolved organic carbon (TOC) via water extraction; soil pH, gravimetric moisture, and bulk density for carbon and nitrogen stock calculations.
- Microbial biomass: C and N via chloroform-fumigation extraction with EC factors (KEC = 0.45; KEN = 0.54) to partition living vs dead microbial pools.
- Enzyme assays: eight extracellular enzymes measured (GLC, CBH, XYL, NAG, PHO, URE, POX, PER) using high-throughput colorimetric/photometric assays; substrates include p-nitrophenyl derivatives and L-DOPA for POX/PER; activities standardised per soil weight and, where applicable, per unit microbial biomass C.
- Soil respiration: CO2 flux measured with a soil respiration chamber and IRGA over 2 minutes per plot.
- PLFA: phospholipid fatty acid analysis to estimate fungal, GP-associated, GN-associated microbial biomass, and actinomycetes; data used to derive total PLFA and microbial community structure indicators.
- DNA handling: DNA extracted from soil using Zymo kit with an enhanced lysis step; final DNA stored at -20°C prior to downstream analyses.

## Molecular data and sequencing
- Bacterial and fungal profiling: 16S rRNA and ITS2 amplicons generated using a two-step Illumina PCR protocol with tagged primers; samples barcoded for multiplexing.
- Library preparation: first-step gene-specific amplification with Illumina adapters; second-step indexing with unique barcodes; library pooling and sequencing on Illumina MiSeq (V3 chemistry).
- Bioinformatics: quality filtering, dereplication, and ASV inference with DADA2 in R; taxonomic assignment using GreenGenes v13.8 (16S) and UNITE v7.2 (ITS); sequence depth normalization (rarefaction) to even depths per dataset.
- Data provenance: sample names align across metadata and sequence tables (plot_ID matches sample IDs in sequencing tables); raw data intended for ENA deposition; taxonomic tables accompany ASV tables.

## Data processing and quality assurance
- Sequencing data processing included trimming, merging, denoising, chimera removal, and ASV construction; sequences rarefied to specified depths to mitigate uneven sampling.
- Enzyme and PLFA data quality controlled via replicates (typically triplicates or more) and standard calculation methods; potential enzyme activities reported relative to microbial biomass where applicable.
- Metadata fields are comprehensive, enabling reproducible integration of abiotic, biotic, and molecular data across two linked experiments.

## Data availability and access
- Data are deposited in the Environmental Information Data Centre repository with associated CSV metadata files and sequencing data to be deposited in ENA.
- Cross-referenced datasets:
  - Broadscale: soil abiotic, PLFA, enzyme activity, microbial biomass, and sequencing tables (16S, ITS).
  - Snow_Veg_manipulation: analogous data for the snow-vegetation treatment.
- Data structure ensures traceability between plots, treatments, sampling dates, and molecular results via consistent identifiers (plot_ID, sample_ID_for_sequencing).

## Field notes and limitations
- Instrument failure led to exclusion of several plots (8 at Obergurgl, 5 at Soelden), reducing the sample size for some analyses.
- Large-scale and cross-treatment design increases complexity for data harmonization and subsequent meta-analyses; careful handling of missing plots and cross-referenced IDs is required.

## Acknowledgements
- Funded by UK NERC (NE/N009452/1); additional support acknowledged for researchers and field access, highlighting collaborative infrastructure underpinning data collection and processing.