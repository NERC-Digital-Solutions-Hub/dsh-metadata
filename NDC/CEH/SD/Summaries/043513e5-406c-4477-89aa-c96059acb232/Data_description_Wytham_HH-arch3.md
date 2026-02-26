# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

- A study linking social networks of wild rodents with their gut microbiomes in Holly Hill, Wytham Woods, Oxford, UK, during 2018–2019.
- Integrated data collection across trapping, tracking, habitat surveys and microbiome profiling to study gut microbe transmission among three rodent species (wood mouse, yellow-necked mouse, bank vole).

## Overview of aims and approach

- Aimed at characterising how social contacts and space use relate to gut microbiota composition and transmission.
- Combines individual-level capture data, high-resolution spatial tracking, vegetation/microhabitat data, and gut microbiome sequencing for a holistic ecological health signal.

## Study design and data collection

- Trapping (Nov 2018–Nov 2019): 4 ha Holly Hill grid; 200 Sherman traps in a checkerboard layout; fortnightly to monthly sessions; identify species, sex, age, weight, reproductive status, and permanently tag with PIT-tags; collect fresh faecal samples for microbiome analysis.
- Tracking: 115 custom PIT-tag loggers (RFID) recording rodent presence with ~1 m2 detection fields; two schemes:
  - Above-ground loggers (AG): random movement monitoring, rotated biweekly across grid cells.
  - Burrow loggers (B): positioned at known mouse burrow entrances (July–November) across a core area; biased toward ~70% of burrows.
- Vegetation/microhabitat survey: for each 10 x 10 m cell, percent cover of eight ground types, open canopy, dead wood, presence/absence of other flora; Table of prevalent tree and herb species provided.
- Study area: Holly Hill grid within Wytham Woods; includes a core 2.56 ha area with a subset of loggers.

## Data types and files

- Four main data components (with detailed column-level descriptions in the dataset):
  - Wytham_HH_rodent_capture_data.csv: per-capture records with trap info, species, sex, age, PIT-tag history, body measurements, ectoparasite screen results, release outcome, and qualitative notes.
  - Wytham_HH_logger_tag_data.csv: logger-level records of each rodent’s time-stamped presence per logger, including logger type (AG or Burrow), location, sex/age/species, tagging date, and potential disturbance flags.
  - Mouse_microbiome_genera_phenotypes.csv: phenotypes for bacterial genera from wood mouse microbiomes (aerotolerance and spore-formation) with references and inference notes.
  - Additional metadata and processing outputs related to microbiome data (e.g., sequencing batch identifiers, extraction/library plates, and sample metadata to support downstream analyses).
- Sequencing and analysis outputs are designed to be reproducible and include batch information (two Illumina MiSeq runs) and mock controls.

## Laboratory methods and sequencing

- Sample processing: DNA extraction using Zymo Quick-DNATM kit on 96-well plates; inclusion of mock community controls to monitor accuracy.
- Library preparation and sequencing: two-step PCR targeting the V4–V5 region of bacterial 16S rRNA; unique dual indexing; 2 x 250 bp paired-end reads on Illumina MiSeq; sequencing batch design accommodates temporal variation.
- Quality controls: negative controls included; samples randomized across extraction and library prep plates to assess technical effects; mock community included to verify pipeline performance.

## Bioinformatics and data processing

- Data processing: DADA2 pipeline (version 1.14) used for sequence variant inference; primer/adaptor trimming with cutadapt; reads trimmed to uniform lengths; ASVs inferred and chimera removed; taxonomy assigned against SILVA v138.
- Phyloseq object: produced to encapsulate ASV table, sample metadata, taxonomy, and phylogeny; provided with the dataset but kept in a raw, minimally preprocessed state (no standard downstream filtering or normalization applied by default).
- Batch integration: two sequencing batches combined for final analysis; awareness of batch-related variation.
- Contamination caveats: evidence of contamination in extraction plates (DNA in extraction controls, spatial autocorrelation of contaminant ASVs); stronger in controls, indicating plate-level vulnerability.
- Decontamination guidance: recommendation to use the decontam package (threshold ~0.75) to identify and remove contaminants, applied to a subset (e.g., wood mouse samples with their water controls) to maintain integrity.
- Mock community visualization supports pipeline validity, though some deviations in relative abundances from theory were noted.

## Data quality, integrity and governance

- Metadata richness: extensive capture, trap, logger, sample, and environmental metadata enabling robust monitoring and downstream analyses.
- Data provenance and reproducibility: detailed methods, batch information, and processing steps documented; ready for audit and re-analysis.
- Data sharing and openness: underlying data and the phyloseq object are intended to be shared publicly; users are advised to perform contamination filtering prior to analysis to reduce technical noise.
- Practical considerations for use in monitoring: design includes explicit notes on potential biases (e.g., burrow logger coverage, variable trapping effects, and logger rotation), which informs interpretation and comparability across monitoring programs.

## Key considerations for monitoring frameworks

- Data utility: integrates behavioral (social network), habitat, and microbiome health signals relevant for environmental health monitoring and policy evaluation.
- Data standardisation: clear metadata schema across trap, logger, and microbiome workflows; facilitate cross-study comparability.
- Data quality safeguards: explicit contamination awareness and remediation workflow (decontam) to ensure analytic reliability.
- Governance and openness: explicit data sharing pathways and documentation to enable reuse in policy evaluation and scientific scrutiny.
- Communication of results: structured outputs (raw phyloseq data alongside detailed field and lab methods) to support transparent interpretation of complex ecological health metrics.

## References and tools used

- DADA2 (Callahan et al., 2016)
- Simple contaminant removal in marker-gene data (Davis et al., 2018)
- Cutadapt (Martin, 2011)
- phyloseq (McMurdie & Holmes, 2013)
- Decontam (Davis et al., 2018)
- SILVA database (Quast et al., 2013; version 138)
- Related methodological and phenotypic references (Suzuki et al., 2019; Walters et al., 2016; others listed in the dataset).