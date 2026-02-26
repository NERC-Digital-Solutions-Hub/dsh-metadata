# Details of data structure to ' CINAg_Digestate_experiment_2017_soil_biology.csv '

- Scope and context
  - Supplement to the supporting documentation for CINAg experiments.
  - Datasets derived from the winter wheat digestate trial 2017.
  - Part of an inorganic fertilizer experiment conducted across two sites (NW = North Wyke, HF = Henfaes Farm).

- Dataset characteristics
  - 87 columns and 180 rows.
  - Column headers carry explanations and units.
  - Structure supports analysis of treatment effects, location, depth, and time points.

- Key design and metadata fields
  - Experiment: Inorganic fertilizer experiment.
  - Sample_ID: Unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths).
  - Year, Site, Sampling_date, Sampling_time: sampling metadata.
  - Plot: Plot numbers.
  - Treatment: C (control), D (digestate), ADNI (acidified digestate with nitrification inhibitor DMPP).
  - Depth_cm: 0-15, 15-30, 30-60 cm.
  - Repeat: 0, 1, or 2.

- Molecular and quality metrics
  - DNA_qubit_ng_per_µl: DNA concentration by Qubit.
  - DNA_260_280_ratio, DNA_260_230_ratio: DNA purity metrics (Nanodrop).
  - DNA_conc_ng_per_g_soil: DNA concentration per gram of dry soil.

- Microbial gene abundance (per g soil)
  - X16S_bact_copy_per_g_soil: bacterial 16S gene copies.
  - X16S_arch_copy_per_g_soil: archaeal 16S gene copies.
  - fungi_ITS_copy_per_g_soil: fungal ITS gene copies.
  - AOA_copy_per_g_soil: ammonia-oxidising bacteria gene copies.
  - AOB_copy_per_g_soil: ammonia-oxidising archaea gene copies.
  - nirS_copy_per_g_soil, nirK_copy_per_g_soil: nitrite reductase genes.
  - nifH_copy_per_g_soil: nitrogen fixation gene.
  - nosZI_copy_per_g_soil, nosZII_copy_per_g_soil: nitrous oxide reductase genes.

- Diversity metrics
  - div16s.tot: bacterial 16S richness (amplicon data), from 10,000 reads/sample.
  - div16s.shan: Shannon diversity (bacterial 16S).
  - divFun.tot: fungal ITS richness (amplicon data), from 5,000 reads/sample.
  - divFun.shan: Shannon diversity (fungal ITS).

- Taxonomic composition (phylum-level, read-based)
  - p__ prefixed entries representing bacterial phyla.
  - Entries given as percentages of reads per sample (based on 10,000 reads for bacteria).
  - Examples include p__Chlorobi, p__Chloroflexi, p__Cyanobacteria, p__Firmicutes, p__Proteobacteria, p__Planctomycetes, p__Actinobacteria, p__Bacteroidetes, among many others.
  - Includes unassigned identities (p__.): e.g., p__. (unassigned) and a long list of named phyla (p__.Caldithrix, p__.Thermi, p__.Acidobacteria, etc.).

- Sequencing read context and notes
  - Bacterial phylum composition reflects relative frequencies from 10,000 reads per sample.
  - Fungal composition metrics derived from amplicon data (divFun) with 5,000 reads per sample.
  - Several phyla are listed with percentages; the full set covers a broad range of bacterial lineages.

- Practical considerations for analysts
  - Rich, multi-dimensional dataset enabling analysis of treatment, depth, site, and time effects on microbial abundance, diversity, and community composition.
  - Potential to model relationships between soil chemistry/plant inputs (digestate treatments) and microbial gene abundances, diversity indices, and phylum-level structure.
  - Requires careful handling of units, scales, and potential missing values across 87 columns.
  - Taxonomic percentages are dependent on sequencing depth and read assignment; consider normalization or offsetting for robust comparisons.
  - Data are organized to support cross-dataset integration, with explicit metadata fields facilitating join operations and metadata-driven analyses.