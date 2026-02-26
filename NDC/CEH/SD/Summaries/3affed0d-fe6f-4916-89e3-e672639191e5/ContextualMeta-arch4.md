# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Data overview
- Three CSV data assets:
  - Leech_Diet_Detections_pa.csv: presence/absence (1/0) of mammalian taxa by leech sample; columns are four-letter mammal codes; rows are leech samples.
  - Leech_Diet_Detections_sample_Info.csv: sample-specific metadata for each leech pool; ties to detections file.
  - OTU_info.csv: OTU-level information including taxonomic assignment, sequence data, BLAST metrics (bit score, % identity), and sequence details.
- Taxa codes included in detections file cover various mammal groups (e.g., Cerv = Cervinae, Hede = Hemigalus derbyanus, Hymu = Hylobates sp, Masp = Macaca spp, etc.).

## Study design and sampling
- Location and habitat:
  - SAFE project blocks: B, D, F, VJR, LF1, LF2, LF3, LFE.
  - Habitat types classified as fragments and logged forest.
- Leech sampling:
  - Two leech species: Haemadipsa picta (Tiger leech pool, T) and Haemadipsa sumatrana (Brown leech pool, B).
  - Sampling method: 20-minute searches within 25 m2 vegetation plots at each block; four visits per plot between February and June 2015.
- Mammal detection approach:
  - Metabarcoding of pooled leech DNA to detect mammal taxa in leech diets.
  - Sequencing platform: Illumina MiSeq (150–250 bp paired-end reads).

## Sequencing and bioinformatics workflow
- Laboratory and analysis steps (high level):
  - Tissue digestion of leeches; DNA extraction from pooled digests within leech species and block.
  - PCR amplification of a mammal-specific 16S rRNA fragment with tagged primers.
  - Library preparation with equimolar pooling, index PCR, and sequencing.
  - Demultiplexing, read merging, quality filtering, and removal of singletons.
  - OTU clustering at 97% similarity; post-clustering filtering.
  - Taxonomic assignment with MEGAN (min >150 bit score, >90% similarity) and BLAST against a curated Bornean reference database.
  - Contamination control by filtering samples based on minimum reads in control samples.
- Replication and filtering:
  - Require a given OTU to appear in at least two PCR replicates.
  - Final data include filtered OTUs and assigned mammal taxa.

## Data structure details
- Leech_Diet_Detections_pa.csv
  - Columns: four-letter codes for mammalian taxa (e.g., Cerv, Hede, Hymu, Masp, etc.).
  - Rows: individual leech samples; cell values: 1 (detection) or 0 (no detection).
- Leech_Diet_Detections_sample_Info.csv
  - Columns include:
    - species: T (Tiger leech pool, H. picta) or B (Brown leech pool, H. sumatrana)
    - poolCode: unique identifier for the sequenced leech pool
    - hab: habitat type
    - site: SAFE site code (B, F, LF, LFE, VJR)
    - totdetections: total number of mammalian detections in the pool
    - log: indicates a logged habitat category
- OTU_info.csv
  - Columns include:
    - Common name, Family (subfamily), Order
    - Taxa assigned, Code, OTU
    - Bit Score, %Identity
    - Sequence (DNA amplicon sequence)

## Data quality, standards, and provenance
- Taxonomic assignment criteria:
  - MEGAN with >150 bit score and >90% similarity
  - BLAST against a curated Bornean reference database
- Data cleaning and reliability:
  - Remove singletons
  - Minimum read threshold based on control samples to limit contamination
  - Equimolar library pooling; Illumina MiSeq sequencing
  - Clustering and refinement of OTUs at 97% with downstream filtering
- Provenance and traceability:
  - Clear linkage among leech species, poolCode, site, habitat, and sample-level mammal detections
  - Documentation of the sequencing and bioinformatics workflow enables reproducibility and method comparison

## Implications and use for data leaders
- System-level view:
  - Demonstrates end-to-end data lifecycle from field collection to sequence-based taxon detection and curation.
  - Provides a structured, multi-file dataset (detections, sample metadata, and OTU details) suitable for integrating with broader data systems.
- Discoverability and metadata:
  - Rich sample metadata (species, poolCode, site, habitat) enhances discoverability and cross-study reuse.
  - Taxon codes and OTU mappings support crosswalks to other datasets and methods.
- Data quality and standards:
  - Clear QC thresholds (replicate presence, read thresholds, OTU clustering, taxonomy assignment criteria) support data quality assessment.
  - Highlights need for consistent data standards, documentation of codes, units, and provenance for reuse in benchmarking metabarcoding pipelines and cross-study comparisons.
- Governance considerations:
  - Structured data assets can be integrated into wider data-sharing and governance practices, facilitating collaboration across networks studying biodiversity via iDNA and related approaches.

## Limitations and considerations for data leaders
- Data type and scope:
  - Results are presence/absence detections, not abundance, and derived from pooled leech samples within blocks and species.
  - Spatial and temporal scope is limited to specific blocks, habitats, and a single time window in 2015, which may affect generalizability.
- Potential biases:
  - Pooling and leech species differences may influence detection probabilities across mammal taxa.
  - Taxonomic resolution depends on reference databases and MEGAN/BLAST thresholds; some taxa may be underrepresented or misassigned.