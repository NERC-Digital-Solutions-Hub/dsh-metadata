# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Data assets and formats
- reps_95.fasta: cleaned, simplified, and quality-controlled set of bat diet sequence data in FASTA format.
- interaction_table.csv: binary interaction matrix between bats and prey taxa; 1 = interaction detected, 0 = no interaction; columns correspond to individual bats in reps_95.fasta.
- bat_capture_data.csv: metadata for bat captures, including trap details, coordinates, date, faecal sample IDs, site, species code, sex, and age; blank cells indicate no value recorded.

## Study context and sampling
- Ecological study of insectivorous bats in Sabah, Malaysia.
- Locations: Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project.
- Sampling: 6 harp traps per location, one night of trapping per site between 2015 and 2017.
- Guano samples collected from captured bats and processed in the UK.
- Species represented: 10 bat species (codes listed at document bottom); laboratory work performed at Queen Mary University of London.

## Data processing and quality control
- Metabarcoding workflow to classify prey taxa into MOTUs (Molecular Operational Taxonomic Units):
  1) DNA extraction
  2) PCR with Zeale (2011) primers
  3) Library preparation and index PCR
  4) 150–250 bp paired-end Illumina MiSeq sequencing
  5) Demultiplexing
  6) Read merge and quality filtering
  7) Removal of singletons
  8) OTU clustering at 95% similarity and post-clustering filtering
  9) Creation of the interaction table
- All samples were collected by DHB, VK, and JB; lab work by DHB and JB; DHB performed data analysis.
- No data were omitted from the study.

## Data structure and metadata
- The interaction_table.csv can be reformatted to other formats using the script r_network_gen.r, available at: https://github.com/hemprichbennett/bat-diet
- bat_capture_data.csv column contexts include:
  - TrapName, Lat, Long, Elevation
  - Bat_no, Day, Month, Year, Date
  - Faeces_no1, Faeces_no2
  - Block, Fragment, Site
  - Species (bat code), Sex, Age
- Blank cells indicate unrecorded values.
- Species codes provided map to full species names (long list included in the document).

## Data governance, sharing and reuse
- Data are curated with explicit quality control and documentation to support discoverability and reuse.
- The primary data assets (sequence data, interaction matrix, and capture metadata) are described and linked to a public script for format conversion.
- Reuse potential includes analyses of bat-diet networks, host–diet interactions, and ecological studies of insectivorous bats in Sabah.