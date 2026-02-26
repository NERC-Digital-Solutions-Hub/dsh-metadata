# Details of data structure to ' CINAg_soil_biology_data_2016_v2.csv '

## Overview
- Supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Dataset: CINAg_soil_biology_data_2016_v2.csv from a grassland fertiliser trial conducted in 2016.
- Structure: 92 columns and 324 rows of measured data.
- Focus: microbial and soil DNA measurements, gene copy numbers, diversity metrics, and relative abundances across samples.

## Dataset Composition and Structure
- Experiment metadata
  - Sample_ID: unique sample identifier (formatted Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths).
  - Year, Site, Farm platform (NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush), Sampling_date, Sampling_time (T0, T1, T2).
  - Plot and Depth (three depth bands: 0-15 cm, 15-30 cm, 30-60 cm).
  - Treatment: C = Control, U = Urea, IU = Urea inhibitor, AN = Ammonium nitrate.
  - Repeat: 0, 1, or 2.
- Laboratory measurements (DNA and quality metrics)
  - DNA_qubit_ng_per_µl: DNA concentration (Qubit).
  - DNA_260_280_ratio and DNA_260_230_ratio: DNA quality indicators (Nanodrop).
  - DNA_conc_ng_per_g_soil: DNA concentration per gram of dry soil.
- Microbial gene copy numbers per gram of soil
  - Bacteria: X16S_bact_copy_per_g_soil.
  - AOA (ammonia-oxidising archaea) and AOB (ammonia-oxidising bacteria) gene copies: AOA_copy_per_g_soil, AOB_copy_per_g_soil.
  - Additional functional/phylogenetic markers: ureC_copy_per_g_soil, X16S_arch_copy_per_g_soil, nirS_copy_per_g_soil, nirK_copy_per_g_soil, nosZI_copy_per_g_soil, nosZII_copy_per_g_soil, nifH_copy_per_g_soil, Fungi_ITS_copy_per_g_soil.
- Diversity and community metrics per sample
  - AOA_AOB_ratio; nirK_nirS_ratio; nosZI.nosZII: ratios among targets.
  - nirS_K.nosZI_II: ratio combining NirS, NirK, NosZI/NosZII.
  - div16s.tot and div16s.shan: bacterial 16S richness and Shannon index (amplicon data; 10,000 reads/sample).
  - divFun.tot and divFun.shan: fungal ITS richness and Shannon index (amplicon data; 5,000 reads/sample).
- Taxonomic and functional composition
  - p__<phylum>: frequency/percentage of bacterial phyla (e.g., p__Firmicutes, p__Proteobacteria, p__Actinobacteria, etc.).
  - The dataset lists numerous phyla and related groups (a large block of p__ taxa with corresponding percentages per sample).
- Notes on sequencing depth
  - Bacterial 16S data: ~10,000 reads per sample for the 16S dataset.
  - Fungal ITS data: ~5,000 reads per sample.

## Data Quality, Standards, and Metadata Considerations
- Clear, structured naming for key identifiers (Year, Site, Sampling_time, Treatment, Depth) to support traceability and discoverability.
- Metadata completeness is critical for reuse: ensure consistent codes for Site, Platform, Treatment, Depth, and Sampling_time.
- Data quality indicators included: DNA integrity metrics (260/280, 260/230) and DNA concentration per gram soil.
- Diverse data types require normalization considerations for cross-study comparability (e.g., differing read depths between 10k bacterial vs. 5k fungal datasets).
- The header names include detailed measures, but some lines show formatting irregularities (e.g., line breaks in p__ phyla entries), which could affect interoperability and should be cleaned in governance processes.

## Data Governance, Sharing, and Compliance
- The document functions as a data structure guide accompanying supporting CINAg experiments, aiding data discoverability and reuse.
- Data Stewards should ensure:
  - Standardized vocabularies and controlled terms for fields like Site, Platform, and Treatment.
  - Consistent units and formats across all columns (e.g., ng/µl, ratios, copies per g soil).
  - Versioning and documentation of any schema changes from v2 to future releases.
  - Proper documentation of data provenance and any transformations (cleaning, normalization) performed prior to sharing.
- Datasets are intended for upload to relevant data portals and cataloguing within collections of CINAg soil biology data.

## Practical Implications for Use and Stewardship
- Researchers can leverage:
  - Temporal (T0, T1, T2) and depth-resolved measurements to study fertiliser effects on soil microbiology.
  - Comprehensive gene copy and diversity metrics to link microbial structure with soil health indicators.
  - Rich phylum-level composition data to examine community shifts under different treatments and depths.
- Data Stewards should prepare guidance on:
  - How to handle missing values or incomplete samples.
  - Normalization strategies when comparing samples with different sequencing depths.
  - ClearReadme or data dictionary deployment to accompany the CSV for end users.

## Endnotes
- The dataset is tied to a 2016 grassland fertiliser trial and is part of CINAg’s broader suite of soil biology data.
- The file CINAg_soil_biology_data_2016_v2.csv represents a structured, multi-layered data resource requiring careful governance to maximize reproducibility and reuse.