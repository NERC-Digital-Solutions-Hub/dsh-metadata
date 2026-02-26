# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Data overview
- Datasets comprise cleaned sequence data (reps_95.fasta), a binary interaction matrix (interaction_table.csv) linking bats to prey, and bat capture metadata (bat_capture_data.csv).
- Interaction table uses 1 for detected interactions and 0 for no interaction; columns align with bats listed in reps_95.fasta.
- All data were collected from insectivorous bats across Sabah locations (Danum Valley, Maliau Basin, and the SAFE project) and processed in the UK.

## Data files and structure
- reps_95.fasta: cleaned, simplified, and quality-controlled nucleotide sequences (FASTA format).
- interaction_table.csv: binary matrix of bat-prey interactions; columns correspond to bat IDs in reps_95.fasta.
- bat_capture_data.csv: metadata for each bat capture, including trap details, geolocation, sample IDs, and bat species codes.

## Sampling, sequencing and bioinformatics
- Study scope: ecological sampling of bat diet via guano across 2015–2017.
- Locations: Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project.
- Species: guano sampled from 10 bat species (codes provided at document bottom).
- Methods: bats captured with harp traps; guano collected and processed in the UK.
- Sequencing: metabarcoding and high-throughput sequencing performed at Queen Mary University of London.
  - Steps: DNA extraction, PCR with Zeale (2011) primers, library construction and index PCR, 150–250 bp paired-end Illumina MiSeq, demultiplexing, read merging and quality filtering, singleton removal, OTU clustering at 95% with post-clustering refinement, and creation of the interaction table.
- All samples collected by DHB, VK, JB; lab work by DHB and JB; data analysis by DHB. No data omissions reported.

## Data processing and availability
- Interaction data can be converted to other formats using the script r_network_gen.r.
- Script and data availability: GitHub repository at https://github.com/hemprichbennett/bat-diet.
- Data provenance: all samples and analyses are described, with explicit authorship and lab/workflow details.

## Data structure details (bat_capture_data.csv)
- Key fields include:
  - TrapName, Lat, Long, Elevation, Bat_no, Day, Month, Year, Date
  - Faeces_no1, Faeces_no2, Block, Fragment, Site, Species, Sex, Age
  - Blank cells indicate missing values
- Species codes map to specific bat species (e.g., Emballonura alecto, Hipposideros spp., Kerivoula spp., etc. with abbreviations provided in the document).

## Species codes (examples)
- Emballonura alecto (Emal.), Emballonura monticola (Emmo.)
- Hipposideros spp. (Hiare/hiple variations listed)
- Kerivoula spp. (Keha/Kein/etc.)
- Macroglossus minimus, Megaderma spasma, Murina spp., Myotis spp., Nycteris tragata, Phoniscus atrox, Philetor brachypterus, Pipistrellus spp., Rhinolophus spp., Scotophilus kuhlii
- Full mapping of codes to species provided in the document

## Data stewardship and governance considerations
- Data standards and provenance:
  - Clear linkage between sequence data (FASTA IDs) and capture metadata (bat_capture_data.csv) via bat IDs.
  - Documentation of laboratory steps, primer used (Zeale 2011), and sequencing platform (Illumina MiSeq).
- Metadata completeness:
  - Missing values are explicitly indicated; stewardship should ensure as complete as possible metadata for traceability and reuse.
- Formats and interoperability:
  - Use of standard formats (FASTA, CSV) facilitates reuse; maintain consistent naming and ID conventions across files.
- Reproducibility and provenance:
  - The r_network_gen.r script provides a reproducible path from raw data to the interaction table.
  - Detailed procedural steps enable replication of the bioinformatic workflow.
- Data sharing and access:
  - Data are accompanied by a public repository link; ensure ongoing access and versioning, and consider providing a data DOI and citation guidance.
- Quality and limitations:
  - Explicit quality-control steps for sequences and OTU clustering threshold (95%) are documented; stewardship should capture any potential primer biases or taxonomic limitations inherent to Zeale primers.

## Practical notes for reuse
- To reproduce the interaction matrix format, use the r_network_gen.r script from the provided GitHub repository.
- Reference the data provenance (collection periods, locations, and sequencing steps) to contextualize analyses.
- Maintain the linkage between sample IDs, trap details, and bat species codes to preserve data integrity across analyses.