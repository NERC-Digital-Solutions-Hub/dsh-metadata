# Details of data structure to CINAg_soil_biology_data_2016_v2.csv

- Overview
  - Holds data from the grassland fertiliser trial of 2016.
  - Dataset comprises 92 columns and 324 rows.
  - Designed to capture both field metadata and extensive molecular biology measurements of soil samples.

- Dataset structure and key fields
  - Experiment, Sample_ID (unique sample identifier)
  - Year, Site (Farm platform: NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush)
  - Sampling_date, Sampling_time (T0, T1, T2)
  - Plot (1–16), Treatment (C = Control, U = Urea, IU = Urea inhibitor, AN = Ammonium nitrate)
  - Depth_cm (0–15 cm, 15–30 cm, 30–60 cm), Repeat (0, 1, 2)
  - DNA metrics: DNA_qubit_ng_per_µl; DNA_260_280_ratio; DNA_260_230_ratio; DNA_conc_ng_per_g_soil
  - Microbial gene copies per g soil: X16S_bact_copy_per_g_soil; AOA_copy_per_g_soil; AOB_copy_per_g_soil; ureC_copy_per_g_soil; X16S_arch_copy_per_g_soil
  - Functional genes: nirS_copy_per_g_soil; nirK_copy_per_g_soil; nosZI_copy_per_g_soil; nosZII_copy_per_g_soil; nifH_copy_per_g_soil; Fungi_ITS_copy_per_g_soil
  - Community and diversity metrics: AOA_AOB_ratio; nirK_nirS_ratio; nosZI.nosZII_ratio; nirS_K.nosZI_II_ratio
  - Amplicon diversity: div16s.tot; div16s.shan; divFun.tot; divFun.shan
  - Taxonomic composition (phylum-level relative abundances per sample): numerous p__<phylum> entries (e.g., p__Firmicutes, p__Bacteroidetes, p__Proteobacteria, p__Cyanobacteria, etc.) expressed as percentages per 10,000 reads
  - Note: The dataset expresses some formatting irregularities in phylum field names (e.g., line breaks around certain entries), but the intention is phylum-level abundance percentages from amplicon reads

- Spatial relevance for GIS analysis
  - Site codes (NW, HF, EB) enable grouping by farm platform and site
  - Depth and sampling time enable vertical and temporal mapping of soil microbiology
  - Primary spatial linkage tokens: Sample_ID, Year, Site, Plot, Depth_cm, Treatment
  - Limitation: no explicit geographic coordinates included; spatial mapping requires joining to external site polygons or layouts that map Site/Plot to coordinates

- Data quality, standardization, and preparation for GIS use
  - High-dimensional, multi-measurement dataset with a mix of counts, concentrations, ratios, and percentages
  - Units must be consistently interpreted (e.g., gene copies per gram dry soil vs per gram soil)
  - Relative abundance data are based on 10,000 reads; may require normalization or transformation for cross-sample comparisons
  - Data cleaning needed for formatting inconsistencies in phylum fields and potential missing values
  - To map in GIS, join keys such as Sample_ID, Year, Site, Plot, Depth_cm, Sampling_time, and Treatment to external metadata and site location layers
  - Consider converting measurements to map-friendly formats (e.g., densities or normalized indices) and choosing appropriate visualization scales for diversity indices and gene-copy abundances

- Usage recommendations and potential map visualizations
  - Create maps showing spatial variation across sites/platforms for:
    - Gene copy densities per g soil (e.g., X16S_bact_copy_per_g_soil, AOA_copy_per_g_soil)
    - Diversity metrics (div16s.tot, divFun.tot, div16s.shan, divFun.shan)
    - Key ratios (AOA_AOB_ratio, nirK_nirS_ratio, nosZI.nosZII_ratio)
    - Phylum-level relative abundances (select major phyla) per sample
  - Visualizations by:
    - Site-level choropleths or graduated symbols for selected metrics
    - Depth-specific maps (0–15 cm, 15–30 cm, 30–60 cm) to show vertical distribution
    - Temporal sequences by Sampling_time (T0, T1, T2) if site-level coordinates are available
    - Treatment effects by comparing control vs fertilizer types across sites
  - Data integration ideas:
    - Link to soil property layers (e.g., soil type, pH, moisture) for more contextual GIS analyses
    - Combine with field management layers to support policy or advisory visuals
  - Reporting and interpretability:
    - Use standardized units and, where appropriate, normalize by depth or soil mass
    - Clearly annotate that phylum abundances are based on 10,000 reads and may require normalization when aggregating across samples

- Caveats and limitations for GIS applications
  - No explicit geographic coordinates provided; spatial mapping depends on external site-location data
  - Data reflect a single year (2016) grassland trial; temporal generalization may be limited
  - Complex, high-dimensional dataset requiring careful preprocessing (unit consistency, missing values, formatting)
  - Some phylum field names may have formatting inconsistencies; ensure consistent field mapping during data import

- Bottom-line takeaway for GIS specialists
  - The CINAg_soil_biology_data_2016_v2.csv dataset provides rich, site- and depth-resolved molecular soil biology measurements from a 2016 grassland fertiliser trial, suitable for map-based exploration of spatial and temporal patterns in microbial abundance, diversity, and community composition, once coordinates are attached and data are standardized for GIS visualization.