# Details of data structure to ' CINAg_Digestate_experiment_2017_soil_biology.csv '

- Overview
  - Supplements supporting data series for CINAg experiments.
  - Dataset: winter wheat digestate trial 2017; 87 columns, 180 rows.
  - Focus: soil biology measurements across inorganic fertilizer treatments.

- Dataset structure and contents
  - Experiment: Inorganic fertilizer experiment
  - Sample_ID: unique sample identifier encoding Year, Experiment, Site, Sampling_time, Treatment, Plot, Depth
  - Time and location fields
    - Year: year of sampling
    - Site: farm platform (NW = North Wyke, HF = Henfaes Farm)
    - Sampling_date: date of sampling (dd/mm/yyyy)
    - Sampling_time: two time points (T1, T2)
    - Plot: plot numbers
  - Treatments and depth
    - Treatment: C (control), D (digestate), ADNI (acidified digestate with nitrification inhibitor DMPP)
    - Depth_cm: 0-15, 15-30, 30-60 cm
    - Repeat: 0, 1, or 2
  - Core measurement groups
    - DNA quality and concentration
      - DNA_qubit_ng_per_µl, DNA_260_280_ratio, DNA_260_230_ratio
      - DNA_conc_ng_per_g_soil
    - Microbial gene abundances (per g soil)
      - X16S_bact_copy_per_g_soil, X16S_arch_copy_per_g_soil
      - fungi_ITS_copy_per_g_soil
      - AOA_copy_per_g_soil, AOB_copy_per_g_soil
      - nirS_copy_per_g_soil, nirK_copy_per_g_soil
      - nifH_copy_per_g_soil
      - nosZI_copy_per_g_soil, nosZII_copy_per_g_soil
    - Diversity metrics
      - div16s.tot (bacterial 16S richness from amplicon sequencing)
      - div16s.shan (Shannon index for bacterial 16S)
      - divFun.tot (fungal ITS richness)
      - divFun.shan (Shannon index for fungal ITS)
    - Taxonomic profile (relative abundances, based on 10,000 reads)
      - p__ taxonomy entries (e.g., p__Chlamydiae, p__Chlorobi, p__Chloroflexi, p__Cyanobacteria, p__Firmicutes, p__Proteobacteria, etc.)
      - Many lines show “Frequency of bacterial phylum p__ within sample's 10,000 reads: percentage”
      - Some entries listed with multiple aliases (e.g., p__SR1/OP11) reflecting taxonomic groupings
  - Data characteristics
    - Mix of quantitative measurements (concentrations, gene copy numbers, diversity indices, abundances)
    - Many fields have explicit units (e.g., ng/µl, copies/g soil, percentages)
    - Taxonomic abundance fields are percentage values derived from amplicon reads

- Data quality, provenance, and documentation
  - Data are described with explicit column headers and explanations per field
  - Includes quality-relevant metrics (DNA quality ratios, Qubit concentration)
  - Metadata available to link samples to experimental design (site, treatment, depth, sampling time)
  - Documentation implies an intention to curate and transform raw data prior to sharing

- Metadata, standards, and interoperability considerations
  - Rich metadata mapping for each sample (Year, Site, Sampling_date, Depth, Treatment, etc.)
  - Structured naming convention for Sample_ID enables traceability across experiment components
  - Taxonomic data uses standard phylum-level groupings with explicit frequency percentages
  - Recommendation for continued alignment with data dictionaries and controlled vocabularies to enhance interoperability across CINAg datasets

- Data governance, sharing, and lifecycle considerations
  - Dataset is part of a broader CINAg dataset ecosystem; sharing should respect data availability and potential restrictions
  - Systems in place or needed to upload to portals and catalogue holdings
  - Documentation of data processing steps (quality assurance, cleaning, transformation) should accompany shared data
  - Maintainability: ensure updates reflect new sampling rounds, revised metadata, or corrected measurements

- Key takeaways for Data Stewards
  - Ensure complete, consistent metadata for sample identification and experimental design
  - Validate units and measurement formats across all fields; maintain clear data dictionaries
  - Preserve linkage between samples and their measurement results (e.g., linking Sample_ID to all measurement columns)
  - Establish and enforce data quality checks (e.g., DNA metrics, sequencing-derived abundances, diversity indices)
  - Manage data sharing with clear access constraints, licensing, versioning, and update protocols
  - Plan for interoperability with other CINAg data (standardized taxonomic naming, consistent depth and treatment encoding)