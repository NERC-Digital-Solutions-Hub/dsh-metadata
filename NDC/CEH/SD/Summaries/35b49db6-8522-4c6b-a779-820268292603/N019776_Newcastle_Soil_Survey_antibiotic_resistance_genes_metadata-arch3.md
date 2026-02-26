# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

- Purpose and scope
  - A dataset describing the relative abundance of antimicrobial resistance (AMR) genes detected in soil DNA from soils around Newcastle upon Tyne.
  - Aims to support environmental health monitoring by informing policy decisions on AMR in soils and potential links to metal contamination and land-use.
  - Four treatment categories used to capture combinations of metal presence and land-use: low-metal/rural, low-metal/urban, high-metal/rural, high-metal/urban.

- Fieldwork design
  - Locations preselected based on prior metal concentration data and land-use patterns (Rothwell & Cooke, 2015).
  - Sampling conducted in June 2016.
  - Target soil horizon: upper layer, within 15 cm of surface.
  - Samples refrigerated post-collection to preserve integrity.

- Analytical methods
  - DNA extraction performed on soil samples (FastDNA Spin Kit for Soil).
  - DNA stored at -80°C prior to analysis.
  - 500–2000 ng of DNA processed for high-throughput qPCR via the OpenArray platform (Institute of Urban Environment, Chinese Academy of Sciences).
  - qPCR primers/approaches referenced from prior work (e.g., Zhu et al. 2013, 2017; Looft et al. 2012).
  - Detection threshold: Ct = 37 used as the limit of detection.

- Data units and interpretation
  - AMR gene abundances are reported as relative abundances (delta-delta Ct method; Livak & Schmittgen, 2001).
  - 16S rRNA levels quantified to provide a surrogate measure of total bacterial abundance.

- Data structure and content
  - Core dataset rows are organized around high-throughput qPCR assay results tied to ARDB (Antibiotic Resistance Genes Database) nomenclature.
  - Includes mappings between: 16S rRNA, ARDB gene, and Antibiotic Classification (e.g., various aminoglycoside, beta-lactamase, MLSB, sulfonamide, tetracycline resistance genes, etc.).
  - Extensive gene-by-gene coding table listing gene identifiers and their antibiotic class classifications (e.g., aac, aadA variants, bla genes, erm genes, tet genes, van genes, etc.).
  - A comprehensive reference table supports traceability of gene names to resistance categories.

- References and methodological context
  - Key sources for gene-expression analysis and AMR gene databases (Livak & Schmittgen 2001; ARDB by Liu & Pop 2009).
  - Foundational studies informing AMR gene detection in environmental contexts (Looft et al. 2012; Zhu et al. 2013, 2017).
  - Supporting background on soil metal concentrations and urban background levels (Rothwell & Cooke 2015).

- Monitoring framework considerations for policy use
  - Strengths for monitoring
    - Design enables policy-relevant comparisons across urban/rural settings and metal contamination levels.
    - Quantitative AMR gene metrics provide a concrete environmental health indicator.
    - Detailed gene-to-class mappings support interpretation of resistance risk profiles.
  - Data quality and governance needs
    - Requires explicit metadata on sampling, QA/QC procedures, and data provenance for governance and reproducibility.
    - Openness and sharing of underlying datasets should be aligned with data governance standards to facilitate transparency.
  - Implementation considerations
    - Relative abundance metrics enable trend analysis but should be complemented with metadata on detection limits, sample handling, and potential batch effects.
    - The dataset is region-specific (NE England); for broader policy uptake, ensure comparability with metadata to enable cross-site synthesis and benchmarking.