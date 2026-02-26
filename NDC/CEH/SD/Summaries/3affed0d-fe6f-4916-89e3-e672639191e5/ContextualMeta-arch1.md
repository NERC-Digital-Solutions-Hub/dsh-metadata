# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Aim and scope
- Evaluate whether two leech species, Haemadipsa picta (Tiger leech) and Haemadipsa sumatrana (Brown leech), are suitable for sampling mammalian diversity in North Borneo using metabarcoding of leech gut contents.
- Provide a data package that links mammal detections to leech samples and OTU-level taxonomic information to support downstream analyses and reproducibility.

## Data products

- Leech_Diet_Detections_pa.csv
  - Presence/absence matrix of mammal taxa across leech samples.
  - Columns: four-letter codes for mammalian taxa (e.g., Cerv, Hede, Hymu, Masp, Hysp, Musp, Ruun, Rasp, Suba, Trsp, Trcr, Trfa, Vita).
  - Rows: individual leech samples; cells contain 0 (no detection) or 1 (detection).

- Leech_Diet_Detections_sample_Info.csv
  - Sample-level metadata for each leech pool.
  - Columns include: species (T = Tiger leech, B = Brown leech), poolCode, hab (habitat type), site (SAFE site code), totdetections (total mammal detections in the pool), log (continuous logged variable related to habitat or sampling context).

- OTU_info.csv
  - Operational Taxonomic Unit (OTU) details and sequence data used for mammal identifications.
  - Columns include: Common name, Family (subfamily), Order, Taxa assigned, Code, OTU, Bit Score, %Identity, Sequence.

## Study area, sampling design, and laboratory workflow

- Study area and sampling
  - Leech samples collected at SAFE project blocks: B, D, F, VJR, LF1, LF2, LF3, LFE.
  - Habitat types represented: fragments and logged forest.
  - Leech species sampled: Haemadipsa picta and Haemadipsa sumatrana.
  - Field protocol: 20-minute searches within 25 m^2 vegetation plots at each block; four visits per plot; sampling conducted February–June 2015.

- Molecular methods and sequencing
  - Metabarcoding and high-throughput sequencing performed at University of Copenhagen or Queen Mary University London.
  - Workflow steps (summarised):
    - Tissue digestion of leech individuals.
    - Amplification of a mammal-specific 16S rRNA fragment.
    - Pooling digests for DNA extraction in batches (ten per pool), pooling within leech species and block.
    - Pooling and purification of amplicons; library preparation and indexing PCR.
    - Sequencing on Illumina MiSeq (150–250 bp paired-end).
    - Demultiplexing, merging reads, and quality filtering.
    - Removal of singletons; filtering PCRs based on appearance in at least two PCR replicates.
    - Clustering reads into OTUs at 97% similarity; post-clustering filtering.
    - Taxonomic assignment with MEGAN (thresholds: >150 bit score and ~90% similarity) and BLAST against a Bornean reference database.
    - Contamination control by filtering samples based on minimum reads in control samples.

## Data structure and content details

- Leech_Diet_Detections_pa.csv
  - Presence/absence matrix where columns are mammalian taxa codes (e.g., Cerv, Hede, Hymu, Masp, etc.) and rows are leech samples.

- Leech_Diet_Detections_sample_Info.csv
  - Per-sample metadata including leech species, poolCode, habitat type, site, and detected mammal counts.

- OTU_info.csv
  - Taxonomic and sequence data for mammalian OTUs, including:
    - Common name, Family, Order, Taxa assigned, Code, OTU identifier
    - Bit Score, %Identity, and DNA Sequence

## How the data can be used

- Compare mammal detections between leech species (picta vs sumatrana) across habitat types and sites.
- Link sample-level detections to OTU identifications for robust taxonomic inferences.
- Build presence/absence models of mammal detections as a function of leech species, habitat, site, and pooling strategy.
- Use OTU metadata (bit score, identity, sequence) to assess confidence in taxonomic assignments and to integrate with reference databases for further validation.

## Quality control and data provenance

- Taxonomic assignments based on MEGAN with thresholds (>150 bit score, ~90% identity) and BLAST against a curated Bornean reference database.
- Contamination control via minimum read thresholds in control samples.
- Data are organized to enable traceability: sample-level pool codes, habitat and site metadata, and linked OTU information for reproducibility and re-use.