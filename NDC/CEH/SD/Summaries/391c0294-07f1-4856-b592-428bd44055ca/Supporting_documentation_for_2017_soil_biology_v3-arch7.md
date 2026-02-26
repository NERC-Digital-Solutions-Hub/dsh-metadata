# Details of data structure to CINAg_Digestate_experiment_2017_soil_biology.csv

- Dataset overview
  - 180 rows (samples) and 87 columns
  - Winter wheat digestate trial 2017
  - Supplement to supporting documentation for CINAg experiments
  - Sample_ID encodes Year, Experiment, Site, Sampling_time, Treatment, Plot, Depth

- Experimental design and sampling
  - Experiment: Inorganic fertilizer experiment
  - Site codes: NW = North Wyke, HF = Henfaes Farm
  - Sampling_time: two time points (T1 and T2)
  - Sampling_date: dd/mm/yyyy
  - Depth_cm categories: 0-15, 15-30, 30-60 cm
  - Plot: plot numbers
  - Treatment: C (control), D (digestate), ADNI (acidified digestate with nitrification inhibitor DMPP)

- Data columns and measurement types
  - DNA quality and quantity
    - DNA_qubit_ng_per_µl: DNA concentration (Qubit)
    - DNA_260_280_ratio: DNA purity (protein contamination indicator)
    - DNA_260_230_ratio: DNA purity (salt contamination indicator)
    - DNA_conc_ng_per_g_soil: DNA per gram of dry soil
  - Microbial gene copies per gram of soil
    - X16S_bact_copy_per_g_soil: bacterial 16S gene copies
    - X16S_arch_copy_per_g_soil: archaeal 16S gene copies
    - fungi_ITS_copy_per_g_soil: fungal ITS copies
    - AOA_copy_per_g_soil: ammonia-oxidising bacteria (AOB) gene copies
    - AOB_copy_per_g_soil: ammonia-oxidising archaea gene copies
    - nirS_copy_per_g_soil, nirK_copy_per_g_soil: nitrite reductase gene copies
    - nifH_copy_per_g_soil: nitrogen fixation gene copies
    - nosZI_copy_per_g_soil, nosZII_copy_per_g_soil: nitrous oxide reductase gene copies
  - Amplicon sequencing diversity and richness
    - div16s.tot: bacterial 16S richness (from amplicon sequencing; 10,000 reads/sample)
    - div16s.shan: Shannon diversity (bacterial 16S)
    - divFun.tot: fungal ITS richness (from amplicon sequencing; 5,000 reads/sample)
    - divFun.shan: Shannon diversity (fungal ITS)
  - Taxonomic/phyla composition (relative abundances, percentages)
    - p__… entries showing frequency of bacterial phyla within sample’s 10,000 reads (percentages)
    - Includes numerous phyla (e.g., Caldiserica, Chlorobi, Cyanobacteria, Firmicutes, Proteobacteria, and many others)
    - Some entries show formatting nuances (e.g., p__SR1, OP11) but denote phylum-level abundances
  - Note: All phylum abundance values described as percentages of reads; sequencing depth specified as 10,000 reads per sample (or 5,000 reads for fungi in some entries)

- Spatial and temporal dimensions for GIS use
  - Spatial identifiers: Site (NW/HF) and Plot; potential for geolocation by linking to site coordinates
  - Temporal identifiers: Year, Sampling_date, Sampling_time (T1/T2)
  - Depth as an additional dimension (0-15, 15-30, 30-60 cm)

- GIS-ready opportunities and applications
  - Map layers to create:
    - Site-level and plot-level distribution of gene copy numbers per g soil
    - Depth-stratified layers (0-15, 15-30, 30-60 cm)
    - Treatment-specific visualizations (C, D, ADNI)
    - Temporal comparisons across T1 vs T2 and across years if extended
  - Visualizations:
    - Choropleth or bubble maps for DNA quantity, gene copy numbers, and diversity indices
    - Faceted maps by site, depth, or treatment
    - Relative abundance maps for selected phyla (e.g., Proteobacteria, Firmicutes)
  - Data integration:
    - Combine with other agronomic or management data (soil properties, yields, fertilizer regimens)
    - Link microbial indicators to spatial features for policy, extension, or public-facing dashboards

- Data processing and quality notes
  - Structure implies composite Sample_ID parsing to extract Year, Experiment, Site, Sampling_time, Treatment, Plot, Depth
  - Depth_cm values are categorical ranges; may require normalization or discretization for certain analyses
  - High-dimensional microbial data (gene copies, diversity metrics, phyla abundances) may necessitate dimensionality reduction or selective visualization for GIS outputs
  - Data completeness and consistency not specified in the document; standard GIS practice would include data validation and handling of missing values during integration

- Units and data interpretation cues
  - Gene copies per gram of soil (per_g_soil)
  - DNA concentration in ng/µl; purity ratios from nanodrop and Qubit measurements
  - Diversity indices (Shannon, richness as totals) and relative abundances as percentages of sequencing reads
  - Depths specified as 0-15, 15-30, 30-60 cm; sampling times T1 and T2

- Practical considerations for users
  - The dataset is specifically tied to the CINAg Digestate experiment and may benefit from cross-referencing with the supporting documentation for experimental metadata and methods
  - To map effectively, additional geospatial coordinates or a geographic reference for NW and HF sites may be required if not provided elsewhere in linked datasets