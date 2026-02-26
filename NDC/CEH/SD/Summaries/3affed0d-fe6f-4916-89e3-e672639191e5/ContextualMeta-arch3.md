# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Data overview
- Leech_Diet_Detections_pa.csv
  - Presence/absence matrix: rows are leech samples; columns are four-letter mammalian taxa codes (e.g., Cerv, Hede, Ecgy, Hymu, Masp, Hysp, Musp, Ruun, Rasp, Suba, Trsp, Trcr, Trfa, Vita).
  - Each cell indicates detection (1) or non-detection (0) of a given mammal taxon in a leech sample.
- Leech_Diet_Detections_sample_Info.csv
  - Sample-specific metadata for each leech pool.
  - Includes: leech species in the pool (T = Haemadipsa picta; B = Haemadipsa sumatrana), poolCode (unique identifier), habitat type (frag or logged), site (SAFE sites B, F, LF, LFE, VJR), and tot detections (total mammal detections); an indicator (log) for whether the sample is from a logged habitat.
- OTU_info.csv
  - Operational Taxonomic Unit (OTU) details used to assign mammal taxa.
  - Includes: Common name, Family (subfamily), Order, Taxa assigned, Code, OTU, Bit Score, %Identity, and Sequence (DNA amplicon).

## Sampling, sequencing and bioinformatics
- Study design and sampling
  - Location: SAFE project blocks B, D, F, VJR, LF1, LF2, LF3, LFE.
  - Habitat types: fragments and logged forest.
  - Leech species collected: Haemadipsa picta (Tiger leech) and Haemadipsa sumatrana (Brown leech).
  - Sampling protocol: 20-minute searches within 25 m² vegetation plots at each block, between February and June 2015; each plot visited four times.
- Sequencing and data processing
  - Conducted at University of Copenhagen or Queen Mary University of London.
  - Workflow (high-level):
    - Tissue digestion of leech individuals.
    - Amplification of a mammal-specific 16S rRNA fragment with tagged primers.
    - Pool digests by leech species and block for DNA extraction (batches of ten).
    - Pool and purify amplicons; prepare equimolar library pool.
    - Library construction and index PCR.
    - Illumina MiSeq sequencing (150–250 bp paired-end reads).
    - Read merging and quality filtering; demultiplexing; sorting by primer tag.
    - Remove singletons; filter PCRs by presence in at least two replicates.
    - Cluster reads into OTUs at 97% similarity; post-clustering refinement.
    - Taxonomic assignment using MEGAN (>150 bit score and 90% similarity).
    - BLAST OTUs against a Bornean reference database (GenBank-derived, study sequences included).
    - Contamination control: filter samples by minimum reads in control samples.
  
## Details of data structure
- Leech_Diet_Detections_pa.csv
  - Structure: presence/absence of each mammalian taxon across sites.
  - Column headings: four-letter codes for mammalian taxa (example mappings include Cerv = Cervinae; Hede = Hemigalus derbyanus; Ecgy = Echinosorex gymnura; Hymu = Hylobates sp; Masp = Macaca spp; Hysp = Hystrix spp; Musp = Muntiacus spp; Ruun = Rusa unicolor; Rasp = Rattus spp; Suba = Sus barbatus; Trsp = Tragulus spp; Trcr = Trachypithecus spp; Trfa = Trichys fasciculata; Vita = Viverra tangalunga).
- Leech_Diet_Detections_sample_Info.csv
  - Columns and examples:
    - species: leech species in the pool (T = Tiger leech Haemadipsa picta; B = Brown leech Haemadipsa sumatrana).
    - poolCode: unique identifier for the sequenced leech pool.
    - hab: habitat type.
    - site: SAFE site where leeches were collected (B, F, LF, LFE, VJR).
    - totdetections: total number of mammalian detections in the pool.
    - log: indicator for continuous logged habitat.
- OTU_info.csv
  - Columns:
    - Common name: mammal name assigned to the OTU.
    - Family (subfamily): taxonomic family (subfamily in brackets if distinct).
    - Order: mammal order.
    - Taxa assigned: taxonomic level of assignment.
    - Code: reference code for the taxon.
    - OTU: unique OTU identifier.
    - Bit Score: BLAST-based score for the OTU assignment.
    - %Identity: percent identity to reference sequence.
    - Sequence: DNA amplicon sequence.