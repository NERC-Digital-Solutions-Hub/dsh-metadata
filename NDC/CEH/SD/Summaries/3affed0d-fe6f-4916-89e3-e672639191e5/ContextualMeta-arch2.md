# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Aim and context
- Assess the suitability of two leech species (Haemadipsa picta and Haemadipsa sumatrana) for sampling mammalian diversity in North Borneo via metabarcoding.
- Generate standardized datasets of mammalian detections from leech-derived DNA to support environmental monitoring and policy performance assessments.

## Data overview
- Three CSV data files underpin the study:
  - Leech_Diet_Detections_pa.csv: presence/absence matrix of mammal detections
    - Columns: four-letter mammal taxon codes (e.g., Cerv, Hede, Ecgy, Hymu, Masp, Hysp, Musp, Ruun, Rasp, Suba, Trsp, Trcr, Trfa, Vita)
    - Rows: leech samples
  - Leech_Diet_Sample_Info.csv (sample metadata)
    - Fields include: species (leech pool species), poolCode (unique pool identifier), hab (habitat type), site (SAFE site), totdetections (total detections), log (logarithmic or coded value)
  - OTU_info.csv (OTU taxonomic and sequence data)
    - Fields include: Common name, Family (subfamily), Order, Taxa assigned, Code, OTU, Bit Score, %Identity, Sequence

## Sampling, sequencing and bioinformatics
- Field sampling design
  - Location: SAFE project blocks in North Borneo (B, D, F, VJR, LF1, LF2, LF3, LFE)
  - Habitats: fragments vs. logged forest
  - Leech species collected: Haemadipsa picta (Tiger leech pool) and Haemadipsa sumatrana (Brown leech pool)
  - Sampling method: 20-minute searches within 25 m2 vegetation plots
  - Timeline: February–June 2015, with four visits per plot
- Laboratory workflow (metabarcoding)
  1. Tissue digestion of leech individuals
  2. DNA extraction by pooling digests in batches of ten (pooled within leech species and block)
  3. Amplification of mammal-specific 16S rRNA fragment using tagged primers
  4. Pooling and purification of amplicons
  5. Equimolar library pooling
  6. Library build and index PCR
  7. 150–250 bp paired-end MiSeq sequencing
  8. Demultiplexing
  9. Merging reads and quality filtering
  10. Sorting by primer tag
  11. Removing singletons
  12. Filtering PCRs by minimum appearance in two replicates
  13. OTU clustering at 97%, followed by post-clustering filtering
  14. Taxonomic assignment with MEGAN (score >150 bit, ≥90% similarity)
  15. BLAST OTUs against a Bornean reference database (GenBank) and study sequences
  16. Contamination control: filter samples by minimum reads in control samples
- Data structure details (how outputs map to the study design)
  - Leech_Diet_Detections_pa.csv: presence/absence of each mammal taxon per leech sample
  - Leech_Diet_Sample_Info.csv: per-pool metadata (leech species, poolCode, habitat, site, total detections, log)
  - OTU_info.csv: per-OTU taxonomy, assignment level, reference codes, sequence details, and quality metrics (Bit Score, %Identity)

## Outputs and relevance for environmental monitoring
- Standardized data products (detection matrix, sample metadata, OTU taxonomy/sequence info) suitable for integration into environmental health and biodiversity monitoring workflows.
- Clear provenance from field collection to bioinformatics outputs, enabling reuse, QA, and potential combination with other data sources (e.g., other sensors or surveys) to enhance monitoring value.
- Datasets are organized to allow scrutiny of mammalian diversity signals across habitat types and leech species, supporting assessments of sampling effectiveness and coverage.

## Data management and access considerations
- Data are partitioned into clearly defined files with explicit metadata, supporting transparency and reproducibility.
- The structured approach facilitates sharing of underlying data used to generate final outputs, aligning with goals to enable access to datasets and underlying data for broader analysis and policy evaluation.