# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Aim and scope
- Ecological study of bat diet using metabarcoding of guano from insectivorous bats in Sabah, Malaysia.
- Samples collected 2015–2017 across three sites (Danum Valley, Maliau Basin, SAFE project) using harp traps.
- Sequencing and analysis performed in the UK to classify prey taxa into Molecular Operational Taxonomic Units (MOTUs).

## Data products
- reps_95.fasta: cleaned, simplified, quality-controlled nucleotide sequences (fasta format).
- interaction_table.csv: binary interaction matrix linking bats (matching IDs in reps_95.fasta) to prey MOTUs; '1' = detected interaction, '0' = no interaction.
- bat_capture_data.csv: metadata for bat captures, including trap info, location, date, bat species code, sex, age, and sample IDs for faecal tubes.

## Sampling, sequencing and bioinformatics
- Field sampling:
  - Locations: Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project.
  - Bats captured with 6 harp traps per location, for one night per site.
  - Guano collected from captured bats; samples processed in the UK.
- Laboratory workflow (Queen Mary University of London):
  - DNA extraction → PCR with Zeale primers → library preparation and index PCR → 150–250 bp paired-end Illumina MiSeq sequencing.
  - Demultiplexing, read merging, quality filtering, singleton removal.
  - OTU clustering at 95% similarity; post-clustering filtering.
  - Creation of the interaction table.
- Authorship and data handling:
  - All samples collected by DHB, VK, JB; lab work by DHB and JB; data analysis by DHB.
  - No data omitted.

## Data structure and metadata
- Interaction data format:
  - Can be converted to other formats using the script r_network_gen.r (repository: https://github.com/hemprichbennett/bat-diet).
- bat_capture_data.csv details:
  - TrapName, Lat, Long, Elevation, Bat_no, Day, Month, Year, Date.
  - Faeces_no1, Faeces_no2; Block and Fragment (SAFE project-related).
  - Site, Species (bat code), Sex, Age (J = juvenile, A = adult); blanks indicate missing values.
- Species codes list (mapping of codes to bat species names) provided for interpretation.

## Accessibility, reproducibility and data governance
- Data and processing tools are openly available:
  - Interaction network script provided in the repository listed above.
  - Clear documentation of data structure and the steps to reproduce the interaction matrix.
- Data sharing and transparency:
  - Data are openly organized with accompanying metadata; the study notes that blanks exist where data were not recorded.
  - No explicit licensing details provided in the summary; emphasis on data transparency and reproducibility through documentation and scripts.

## Metadata quality and challenges
- Metadata gaps noted (e.g., some GPS coordinates missing, blanks in several fields).
- Data transformation required to align formats (e.g., converting interaction data to preferred formats).
- The study emphasizes metadata completeness and clear data provenance to support verification and reuse.

## Relevance to monitoring frameworks
- Demonstrates end-to-end data lifecycle for environmental monitoring: field collection, laboratory processing, data curation, metadata documentation, and public sharing.
- Highlights practical challenges relevant to monitoring frameworks:
  - Need for robust metadata and data standardization.
  - Balancing data openness with practical barriers (e.g., missing metadata, data format heterogeneity).
  - Importance of transparent pipelines and reproducible analyses to inform policy and future decisions.