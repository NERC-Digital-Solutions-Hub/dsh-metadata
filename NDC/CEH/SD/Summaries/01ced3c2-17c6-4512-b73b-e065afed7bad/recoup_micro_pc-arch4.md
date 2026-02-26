# RECOUP-Moor Microbial data: Methodology

- Field Site
  - Stalybridge estate on Saddleworth Moor (UK), blanket bog ecosystem
  - Wildfire on June 24, 2018; fire affected 18 km² and caused large-scale loss of surface vegetation
  - Vegetation dominated by Calluna vulgaris and Eriophorum vaginatum

- Methods
  - Experimental design: 10 plots established in October 2018 at the post-fire site
    - 5 plots: shallower (less severe) burn
    - 5 plots: deeper (more severe) burn
  - Additional 5 plots at a neighboring unvegetated site within the burn area, likely unburned prior to fire (serves as reference)
  - Plot size: 10 m x 10 m
  - Sampling within each plot: extract 3 soil cores (≈1 cm diameter, 5 cm depth)
    - Cores split into top layer (0–2 cm) and bottom layer (4–5 cm); samples from each plot aggregated to one per depth
  - Reference site sampling: identical procedure, replicated five times
  - Sample handling: on-site drying ice, transport to University of Southampton, storage at –20°C
  - Molecular workflow:
    - DNA extraction: DNeasy PowerSoil kit
    - Target region: V4 of the 16S rRNA gene using primers 515F/806R
    - Amplicon sequencing: Illumina MiSeq
  - Data products: microbial sequence data (ASV sequences) with associated metadata

- Variable key for plot code
  - Unique_sample_ID: unique identifier for each microbial sample
  - Unique_plotID: identifier distinguishing plot features and replicates
    - Codes: S1–S5 (shallow burn), D1–D5 (deep burn), N1–N5 (unburned/reference)
  - Burn_severity: description of burn severity (observational)
  - Sampling_depth: 0–2 cm (top soil) or 4–5 cm (bottom soil)
  - Months_post-fire: approximate months since fire
  - ASV sequence: sequence of amplicon sequence variant (ASV) identified via sequencing

- Notes relevant to data management (implied by methodology)
  - Clear labeling and hierarchical identifiers to enable traceability across plots, depths, and burn treatments
  - Standardized metadata fields for burn severity, sampling depth, and timing to support downstream data integration and analysis
  - Documentation of sample processing and storage conditions to ensure data quality and reproducibility