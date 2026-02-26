# Details on data collection:

- Overview
  - Datasets describe wood mice (Apodemus sylvaticus) and other small mammals collected 2014-2018, combining wild/captive populations.
  - Main components include a longitudinal trapping study (2015-2018) with gut microbiome profiling, diet and parasite data; a dissection study linking GI microbiota to helminths; and a diet shift experiment in a captive colony.
  - Related data from Silwood Park is noted (Project 1: Wild rodents social networks and the microbiome).

- Datasets and Study Design
  - Longitudinal Trapping (Wytham Woods, 2015-2018)
    - 100 m² main grid plus additional habitat grids; species: Apodemus sylvaticus, Apodemus flavicollis, Myodes glareolus.
    - Fortnightly to 2-4 weekly trapping using Sherman traps; PIT-tags for identification; samples: fecal for microbiota and gut parasite analyses.
    - Processing included measurements (species, sex, mass, age), ethical approvals, and storage at -80°C or formalin as appropriate.
  - Dissection Study (Wytham Woods, 2017-2018)
    - Ethical trapping at eight locations; juvenile/pregnant/lactating excluded; euthanasia performed for analysis.
    - GI tract segmented into five sections (duodenum, jejunum, ileum, caecum, colon) for microbiota and parasite assessment; tissues stored at -80°C; helminths stored in ethanol.
    - Ethical approvals from RVC and University of Oxford.
  - Experimental Diet (Edinburgh, May 2017)
    - Diet shift experiment with five diet treatments varying seed (peanut) vs insect (mealworm) content; semi-barrier, SPF conditions.
    - Sampling included fecal microbiota and metabolite data, body mass, and food intake; mice culled after study under UK Home Office license.
  - Diet Shift Metadata (Diet_shift_experiment_2017_metadata.csv)
    - 30-day interval data per mouse, capturing diet type, shift period, group, cage origin, body weight, food intake, fecal metabolites, and other processing details.

- Data Processing and Structure
  - Microbiome data processing
    - DNA extraction using Zymo Quick-DNATM kits with bead beating; two sequencing batches.
    - Amplicon sequencing of the 16S rRNA V4 region (Illumina) with dual-indexing; MiSeq 2x250 bp reads.
    - Two-step PCR with mock community and negative controls; data processed with DADA2 to infer ASVs; taxonomies assigned with Silva Database v138.
    - Output provided as a full_Wytham_processed microbiome dataset in a four-slot phyloseq object (otu_table, tax_table, sample_data, refseq). The object is provided raw without downstream filtering or normalization.
  - Metadata and data dictionaries
    - Full_Wytham_trapping_data.csv: trap-level processing data (capture, misfire, trap, grid, habitat, processing times, measurements, PIT data, etc.).
    - Wytham_longitudinal_sample_metadata.csv: per-sample measurements and sequencing metadata; includes trap details, grid, species, sex, age, reproductive status, body metrics, ectoparasite data, diet indicators, fecal sample links, and more.
    - Diet_shift_experiment_2017_metadata.csv: per-mouse per-day data for the diet shift trial; includes intervention type, shift period, diet type, timing, group, housing, body metrics, food intake, and fecal/poo metrics.
  - Data access and quality
    - Two MiSeq runs each for different study sets; extraction/sequencing performed in two rounds with batch tracking.
    - QA controls included mock community and water blanks; detailed extraction and sequencing metadata are included to support reproducibility.
    - The microbiome dataset is intentionally provided in a raw state to allow user-defined preprocessing (e.g., filtering, normalization).

- Metabolomics and Diet Characterization
  - Faecal metabolite profiling using GC-FID
    - Sample prep includes internal standard (2-methylpentanoic acid) and solvent extraction; metabolites identified against standard mixes of SCFAs (acetic, propionic, butyric, etc.).
    - Data expressed as metabolites per mg faecal material; GC conditions and detection details are specified.
  - Faecal sampling approach for metabolites occurs from fresh feces and bedding to maximize metabolite yield.

- Parasitology and Helminth Data
  - Gut parasites detected by faecal flotation in sodium nitrate solution (EPG counts for multiple nematodes and cestodes; not all trematodes detectable with this method).
  - Data fields include parasite burdens (EPG) for numerous taxa, flotation date, and qualitative notes.

- Data Files and Outputs
  - Project_4_processed_microbiome_data.rds
    - Phyloseq object containing microbiome data across the three main datasets (longitudinal, dissection, and experiment), minimally preprocessed (no filtering or normalization applied beyond removal of non-gut taxa).
  - Wytham_longitudinal_sample_metadata.csv
    - Detailed sample-level metadata for the longitudinal study, including collection specifics, trap/grid information, host traits, ecto-parasite data, diet indicators, and sample processing details.
  - Full_Wytham_trapping_data.csv
    - Comprehensive trap-level data covering processing times, species, sex, measurements, PIT tagging, trap outcomes, and sample collection details.
  - Diet_shift_experiment_2017_metadata.csv
    - Day-by-day data for the diet shift experiment, including intervention type, diet composition, time points, weights, intake, and metabolite data.

- Ethics, Compliance, and Governance
  - Ethical approvals obtained for trapping and dissection studies; Home Office license 70/8543 for the diet experiment; institutional approvals from RVC and University of Oxford.
  - Data readiness for governance and reuse emphasizes data provenance, batch tracking, and explicit metadata to enable reproducibility and cross-study integration.

- Relevance for Data Leaders
  - Demonstrates end-to-end data lifecycle management across observational and experimental studies.
  - Highlights the complexity of multi-modal data assets (microbiome sequencing, metabolomics, host metrics, parasitology) and the need for robust metadata, data provenance, and clear data-object schemas (phyloseq) to support discoverability and reuse.
  - Provides a raw-data-first approach enabling flexible, user-defined preprocessing and integration across datasets, with explicit batch, extraction, and sequencing metadata to manage data quality and comparability.
  - Illustrates governance requirements for cross-study collaboration, including ethical compliance, data standards, and documentation to minimize duplication of effort and maximize the value of data assets for broader data communities.