# Supporting Information

## Overview and context
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biota diversity and functional roles within a large grassland microcosm experiment at Sourhope, UK.
- The programme funded 24 projects studying soil structure, processes (C/N cycles), and biota (microfauna to macrofauna).
- This document describes the arbuscular mycorrhizal (AM) fungal diversity data derived from grassland microcosms and a P. lanceolata bioassay used to assess AM diversity.

## Study design and data collection
- Experimental setup (1997): rendzina soil removed from the surface of a limestone grassland microcosm; 192 mature plants per box arranged 14x14 with randomization; four vegetated treatments: bare soil, Carex flacca monoculture, Festuca ovina monoculture, and a 12-species mix (three functional groups: sedges, grasses, forbs); each treatment replicated four times (16 microcosms total).
- Plant material for AM assessment: 5-day-old Plantago lanceolata bioassay seedlings transplanted into three of the four replicate microcosms per treatment; growth period of 12 weeks.
- AM diversity measurement: AM fungal diversity in P. lanceolata roots assessed by terminal-restriction fragment length polymorphism (T-RFLP) targeting the SSU rRNA gene with AMF-specific and universal primers.

## Data structure and content
- Dataset: Dataset 1005 – Arbuscular mycorrhizal (AM) fungal diversity dataset (Microcosm experiment at Sheffield University).
- Key variables:
  - MICROCOSMID: sample type (bare soil, monocultures of C. flacca, F. ovina, and 12-species mixture).
  - TREATMENT: sourhope soil treatment descriptor.
  - SPECIES: plant assembly type (C. flacca, F. ovina, or 12-species mixture).
  - BAND1-60: presence/absence matrix for 60 terminal-restriction fragments (TRFs) detected in P. lanceolata bioassays (1 = presence, 0 = absence).
- Technical details:
  - TRF analysis yields 60 bands; only presence/absence (not evenness) is recorded.
  - TRFs sized between 45 and 450 bp; fragments outside this range excluded from analysis.
- Microcosm replication and data integrity:
  - Reproducibility verified with internal replicates (duplication across sequencing slab gels).
  - Data are stored with descriptive metadata and are suitable for species richness analyses (not abundance metrics).

## Methods and laboratory workflow
- DNA extraction from root samples followed by purification.
- PCR amplification of SSU rRNA region using NS31 (universal) and AM1 (AMF-specific) primers.
- End-labeling with fluorescent dyes; product purification and preparation for capillary electrophoresis.
- Restriction digestion with two enzymes (HinFI and Hsp92II) to maximize polymorphism in TRFs.
- Fragment analysis on an ABI377 sequencer; TRF sizes determined with GeneScan software.
- Quality controls include duplicate runs to confirm reproducibility and restrictions to the 45–450 bp range for analysis.

## Data quality, governance, and use
- Quality control: numeric range checks, data formatting conformity, and logical integrity checks applied.
- Data provenance and reliability disclaimer: NERC could not warrant the accuracy or fitness of the data for any specific use; no liability for outcomes arising from data use.
- Documentation and reuse guidance:
  - Key references provided for methods and context (e.g., New Phytologist 2004; foundational AMF studies).
  - Related resources available (e.g., Sourhope Field Data Handbook 2003; UK Soil Biodiversity programme literature).
  - Data can be accessed via the indicated supporting information and EIDC catalogue records.

## Governance implications for data stewards
- Metadata and standardization:
  - Ensure complete metadata for Dataset 1005 (micromid, treatment, species, and 60 TRF presence/absence fields) to support discoverability and reuse.
  - Maintain clear definitions for each field (e.g., what constitutes a TRF presence, how bands were assigned, and the treatment descriptors).
- Data sharing and updates:
  - Include provenance notes on sample collection, lab methods, and processing steps to facilitate reproducibility.
  - Acknowledge that dataset includes presence/absence data only; no abundance metrics are provided.
  - Monitor and document any updates or corrections to TRF calls or sample lab procedures.
- Access and licensing:
  - Reference to supporting information and publications; ensure catalog records (eIDC) reflect access rights and licensing where applicable.
  - Highlight data provenance and disclaimer language in any data products derived from Dataset 1005.
- Interoperability and reuse:
  - Structure data to enable integration with other AMF datasets (consistent band numbering, treatment labeling, and plant species naming).
  - Promote cross-referencing with related field data handbooks and UK soil biodiversity resources to contextualize AMF diversity findings. 

## References and further reading
- Johnson, D., et al. 2004. Plant communities affect arbuscular mycorrhizal fungal diversity and community composition in grassland microcosms. New Phytologist, 161(2), 503-515.
- Vandenkoornhuyse P, Leyval C. 1998. SSU rDNA sequencing and PCR fingerprinting reveal genetic variation within Glomus mosseae. Mycologia, 90, 791-797.
- Helgason T, et al. 1998. Ploughing up the woodwide web? Nature, 394, 431.
- Helgason T, et al. 1999. Molecular diversity of AM fungi in Hyacinthoides non-scripta. Molecular Ecology, 8, 659-666.
- Schüßler A, Schwarzott D, Walker C. 2001. A new fungal phylum, the Glomeromycota: phylogeny and evolution. Mycological Research, 105, 1413-1421.