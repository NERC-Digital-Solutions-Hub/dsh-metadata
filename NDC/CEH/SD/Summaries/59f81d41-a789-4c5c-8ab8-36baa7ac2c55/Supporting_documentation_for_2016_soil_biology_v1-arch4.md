# Details of data structure to CINAg_soil_biology_data_2016_v2.csv

- Scope and dataset basics
  - Supplement detailing the data structure for CINAg_soil_biology_data_2016_v2.csv
  - Dataset contains 92 columns and 324 rows
  - Source: grassland fertiliser trial conducted in 2016

- Core dataset structure (highlights of key fields)
  - Experiment: Inorganic fertilizer experiment
  - Sample_ID: unique sample identifier (format Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths)
  - Year: year of sample collection
  - Site: farm platform (NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush)
  - Sampling_date: date of sampling (dd/mm/yyyy)
  - Sampling_time: time point (T0, T1, T2)
  - Plot: plot numbers 1–16
  - Treatment: fertilizer treatments (C = Control, U = Urea, IU = Urea inhibitor, AN = Ammonium nitrate)
  - Depth_cm: sampling depth (0–15 cm, 15–30 cm, 30–60 cm)
  - Repeat: replication indicator (0, 1, or 2)

- Molecular and DNA quality metrics
  - DNA_qubit_ng_per_µl: DNA concentration by Qubit
  - DNA_260_280_ratio: DNA purity (260/280) via Nanodrop
  - DNA_260_230_ratio: DNA purity (260/230) via Nanodrop
  - DNA_conc_ng_per_g_soil: DNA concentration per gram of dry soil

- Microbial gene copy data (per gram of dry soil)
  - Bacteria: X16S_bact_copy_per_g_soil
  - Archaea and ammonia-oxidisers: AOA_copy_per_g_soil, AOB_copy_per_g_soil
  - Additional functional genes: ureC_copy_per_g_soil, X16S_arch_copy_per_g_soil
  - Nitrogen cycle markers: nirS_copy_per_g_soil, nirK_copy_per_g_soil
  - Denitrification markers: nosZI_copy_per_g_soil, nosZII_copy_per_g_soil
  - Nitrogen fixation: nifH_copy_per_g_soil
  - Fungi: Fungi_ITS_copy_per_g_soil

- Relative abundances, diversity, and community metrics
  - AOA_AOB_ratio: ratio of archaea to bacteria ammonia-oxidisers
  - nirK_nirS_ratio: ratio of nirK to nirS nitrite genes
  - nosZI.nosZII: ratio of nosZI to nosZII nitrite genes
  - nirS_K.nosZI_II: ratio of nirS:nirK to nosZI/nosZII nitrite genes
  - Diversity metrics: div16s.tot (bacterial 16S richness from amplicon sequencing), div16s.shan (Shannon index for 16S), divFun.tot (fungal ITS richness), divFun.shan (fungal ITS Shannon index)
  - Abundance context: p__ entries indicating the frequency/relative abundance of specific bacterial phyla within samples (e.g., p__Firmicutes, p__Actinobacteria, p__Proteobacteria, and many others)

- Taxonomic and phylum-level abundance details
  - Large set of p__<phylum> columns representing percent abundance per sample
  - Abundances are described as percentages derived from reads, with a reference scale of up to 10,000 reads per sample for bacteria (and 5,000 reads per sample for fungi in the provided entries)
  - Note: the column listing includes numerous phyla (e.g., Firmicutes, Proteobacteria, Bacteroidetes, Cyanobacteria, Actinobacteria, Acidobacteria, and many less common or less widely annotated groups)

- Data usage context and considerations for data leaders
  - Rich, multi-omic-like dataset combining physical soil measurements, DNA quality metrics, and a broad panel of microbial gene copy numbers, diversity indices, and taxonomic abundances
  - Designed for integrative analysis across spatial (sites/platforms), temporal (sampling times), depth (soil layers), and treatment dimensions
  - Useful for data governance in terms of metadata clarity (units specified for DNA metrics; clear sampling/timepoint structure; explicit treatments and depths)
  - Highlights the need for careful data management given the large number of features (92 columns) and the reliance on standardized units and naming conventions for discoverability and future reuse
  - Potential considerations for data leadership: parsing and harmonizing a long list of phylum-level abundance columns; ensuring consistency of date formats, depth labels, and treatment codes; maintaining alignment between sample identifiers and metadata

- Practical implications for data strategy and governance
  - Provides a comprehensive schema useful for data discovery, lineage tracking, and metadata cataloging
  - Supports planning for data quality checks (e.g., DNA quality ratios, repeat handling, depth and treatment consistency)
  - Encourages establishment of standard naming conventions and documentation to facilitate cross-study integration and reuse
  - Underlines the importance of recording and preserving detailed sampling design information to enable robust downstream analyses and reproducibility