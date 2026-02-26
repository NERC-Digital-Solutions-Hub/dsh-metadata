# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Data overview
- Three CSV data files:
  - Leech_Diet_Detections_pa.csv: presence/absence table of mammal detections by leech sample. Columns are mammal taxa codes; rows are leech samples.
  - Leech_Diet_Detections_sample_Info.csv: sample-specific metadata for each leech pool; rows align with the detections file.
  - OTU_info.csv: OTU-level information including taxonomy assignment, sequence data, and sequence quality metrics.

## Sampling, sequencing and bioinformatics
- Study area and sampling context:
  - Leechsamples collected at SAFE project blocks: B, D, F, VJR, LF1, LF2, LF3, LFE.
  - Habitat types: fragments and logged forest.
  - Leech species: Haemadipsa picta and Haemadipsa sumatrana.
  - Sampling design: 20-minute searches within 25 m^2 plots, February–June 2015; four visits per plot.
- Laboratory workflow (metabarcoding pipeline):
  - Tissue digestion of leech specimens.
  - Amplification of 16s rRNA fragment using mammal-specific primers with tags.
  - Pooling of digests by leech species and block for DNA extraction (batches of ten).
  - Library preparation: equimolar pooling, indexing PCR, and Illumina MiSeq sequencing (150–250 bp, paired-end).
  - Sequence processing: demultiplexing, merging, quality filtering, and removal of singletons.
  - OTU clustering at 97% similarity; post-clustering filtering.
  - Taxonomy assignment: MEGAN with >150 bit score and ≥90% similarity; BLAST against a Bornean reference GenBank-derived database.
  - Contamination control: filtering samples by minimum reads in control samples.

## Data structure and file details
- Leech_Diet_Detections_pa.csv (presence/absence matrix)
  - Columns: four-letter mammal taxon codes (e.g., Cerv for Cervinae, Hede for Hemigalus derbyanus, Ecgy for Echinosorex gymnura, Hymu for Hylobates sp, Masp for Macaca spp, Hysp for Hystrix spp, Musp for Muntiacus spp, Ruun for Rusa unicolor, Rasp for Rattus spp, Suba for Sus barbatus, Trsp for Tragulus spp, Trcr for Trachypithecus spp, Trfa for Trichys fasciculata, Vita for Viverra tangalunga).
  - Rows: leech samples.
- Leech_Diet_Detections_sample_Info.csv (sample metadata)
  - Fields:
    - species: leech species in the pool (T = Tiger leech Haemadipsa picta; B = Brown leech Haemadipsa sumatrana).
    - poolCode: unique identifier for the sequenced leech pool.
    - hab: habitat type.
    - site: SAFE site where leeches were collected (B, F, LF, LFE, VJR).
    - totdetections: total number of mammalian detections in the pool.
    - log: indicates whether the pool is from a logged habitat.
- OTU_info.csv (OTU details)
  - Fields:
    - Common name: mammal name assigned to OTU.
    - Family (subfamily): mammal family, subfamily in brackets if distinct.
    - Order: mammal order.
    - Taxa assigned: taxonomic level assigned to the OTU.
    - Code: mammal taxon code (as above).
    - OTU: unique OTU identifier.
    - Bit Score: alignment score from taxonomy assignment.
    - %Identity: BLAST percent identity to reference.
    - Sequence: DNA amplicon sequence.

## Data processing workflow and quality control
- Data integration:
  - Aligns detections with corresponding sample metadata and OTU assignments.
  - Provides a self-serve-friendly dataset for downstream analyses (e.g., presence/absence by sample, taxa detection patterns across leech species and habitats).
- Quality controls and filtering:
  - OTUs refined post-clustering with a BLAST-based refinement and a threshold-based taxonomy assignment.
  - Contamination control via minimum read thresholds in control samples.
  - Removal of singletons to reduce spurious detections.

## How the data can be used
- Compare mammal detection patterns across:
  - Leech species (Haemadipsa picta vs Haemadipsa sumatrana).
  - Habitat types (fragments vs logged forest).
  - Sites within the SAFE project blocks.
- Build data products such as dashboards or pivot tables to explore:
  - Presence/absence of mammals per leech pool.
  - Taxonomic composition and OTU-level information.
  - Relationships between sampling design (pool composition, habitat) and mammal detections.
- Facilitate data-driven decisions on sampling strategy and the relative suitability of leech species for mammalian biodiversity assessments.