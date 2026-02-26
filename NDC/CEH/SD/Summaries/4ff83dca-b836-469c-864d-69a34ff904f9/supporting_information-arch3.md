# Data overview

- Purpose and scope
  - A dataset documenting the response of soil microbial communities and soil functioning to four climatic disturbances (drought, flooding, freezing, heat) plus a control, using soils from 30 European grassland sites. Includes end-of-disturbance and recovery measurements to help scrutinise and evaluate environmental policies and inform future monitoring decisions.
  - Measures span microbial community composition (bacteria and fungi), functional gene potential (metagenomes), greenhouse gas fluxes, enzymatic activities, substrate-induced respiration, and soil C and N pools.

- Experimental design and sampling regime
  - Sites: 30 replicate sites across 10 European locations representing diverse climates (alpine, subarctic, arctic, Atlantic, boreal, continental, Mediterranean, and steppic).
  - Soil types: 7 soil type categories, predominantly Haplic Cambisols.
  - Setup: 20 pots per replicate site, with four sampling times (S1 before disturbance impact, S2 at peak disturbance, S3 and S4 during recovery) across 5 treatments: Control, Drought, Flood, Freeze, Heat.
  - Scale: 600 microcosms overall (10 countries × 3 replicate sites × 5 treatments × 4 sampling times); 10 Russian samples excluded due to insufficient soil.
  - Climate data: Site climate data from WorldClim (1960–1990) used to contextualize conditions.

- Measurements and indicators
  - Soil environment and chemistry: initial and microcosm moisture, dissolved organic/inorganic N, dissolved organic carbon, total C and N, soil pH.
  - Microbial activity and function: substrate-induced respiration profiles; extracellular enzymatic activities (acetyl esterase, beta-glucosidase, phosphatase, leucine-aminopeptidase) using MUB/AMC substrates.
  - Gas fluxes: CO2, CH4, N2O fluxes measured in microcosms across time points.
  - Microbial community composition: bacteria (16S rRNA V4-V5) and fungi (ITS2) amplicon sequencing.
  - Functional potential: shotgun metagenomes sequenced for selected samples; functional annotation via MG-RAST SEED Subsystems.
  - Data transparency: European Nucleotide Archive accession numbers provided for molecular data.

- Data structure and metadata
  - Disturbance_data.csv: 91 columns, 620 samples, capturing sample provenance (site, replicate, treatments), measured metrics (functional measures, soil properties), and molecular data accession numbers.
  - Disturbance_metadata_header_description.csv: detailed description of the 91 headers.
  - Missing data: NA denotes missing values; some measurements are only available for certain times or subsets of sites; some assays performed on a subset of samples.
  - Data exclusions: DNA analyses exclude some samples due to low yield or quality, resulting in 574 samples used for molecular analyses.

- Molecular data processing and analyses
  - DNA extraction: PowerSoil Pro kit; quality checks and quantification performed.
  - Amplicon sequencing: 16S rRNA (bacteria) and ITS2 (fungi) via Illumina MiSeq; processed with DADA2 to generate ASVs; taxonomic assignment using SILVA (bacteria) and UNITE (fungi).
  - Metagenomics: shotgun sequencing ( TruSeq PCR-free library; NovaSeq); functional annotation with MG-RAST (SEED Subsystems).
  - Quality control: removal of low-read samples; several sites excluded due to insufficient DNA yield or low-quality sequences, leaving 574 usable samples.

- Data accessibility and governance
  - Molecular data are linked to ENA accession numbers, enabling public access and reuse.
  - Documentation provided via two CSV files ensuring metadata traceability and interpretability.
  - Methodological transparency includes primers, PCR conditions, sequencing platform, and processing pipelines (DADA2, SILVA, UNITE, MG-RAST).

- Relevance for monitoring frameworks and policy evaluation
  - Cross-site, standardized design with multiple disturbance scenarios provides a robust basis for evaluating environmental health monitoring approaches under climate stress.
  - Rich metadata and open data practices support comparability, reproducibility, and integration into policy-relevant dashboards or reports.
  - Data can inform indicators of soil health, microbial functional potential, and ecosystem resilience under climate perturbations.

- Limitations and considerations for data governance
  - Some data are missing or restricted by design (initial vs. laboratory measurements; subset availability for enzymes and metagenomics).
  - Cultural and logistical differences across sites may introduce variability; careful normalization and metadata use are required for cross-site comparisons.
  - Some sites or samples were excluded due to data quality issues, which may influence representativeness.