# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Data overview
- reps_95.fasta: cleaned, simplified, and quality-controlled sequence data in FASTA format
- interaction_table.csv: tab-separated table of bat–prey interactions; columns correspond to individual bats; a binary matrix where 1 = detected interaction, 0 = no interaction; bat IDs align with the FASTA file
- bat_capture_data.csv: capture information for bats, including sample IDs used to generate the other two files

## Sampling, sequencing and bioinformatics
- Study context: capture and dietary data for insectivorous bats in Sabah, Malaysia
- Locations: Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project
- Sampling: 6 harp traps per location, used for one night; sampling conducted between 2015 and 2017
- Guano processing: guano sequenced to identify prey taxa into MOTUs; processing occurred in the UK
- Sequencing workflow (Queen Mary University of London):
  1. DNA extraction
  2. PCR with Zeale (2011) primers
  3. Library preparation and index PCR
  4. Illumina MiSeq 150–250 bp paired-end reads
  5. Demultiplex
  6. Read merging and quality filtering
  7. Remove singletons
  8. OTU clustering at 95% with post-clustering filtering
  9. Create interaction table
- Authorship and data handling: All samples collected by DHB, VK, JB; DHB and JB performed lab work; DHB analyzed data; no data omitted

## Details of data structure
- Interaction CSV conversion: can be converted to other formats using the script r_network_gen.r (GitHub: https://github.com/hemprichbennett/bat-diet)
- bat_capture_data.csv columns (examples): TrapName, Lat, Long, Elevation, Bat_no, Day, Month, Year, Date, Faeces_no1, Faeces_no2, Block, Fragment, Site, Species, Sex, Age
- Missing values: blank cells indicate unrecorded data
- Species codes: long list mapping bat species to short codes (e.g., Emballonura alecto -> Emal., Kerivoula hardwickii -> Keha, Hipposideros ater -> Hiat, etc.)
- Data linkage: interaction data, capture data, and sequence data are cross-referenced via IDs (e.g., bat IDs, sample IDs)

## Notes and usage considerations
- The interaction table can be reformatted for analyses using the provided conversion script
- The dataset provides a standardized, quality-controlled pipeline from field capture to molecular diet inference, suitable for monitoring biodiversity and ecosystem health
- Documentation emphasizes data verifiability and reproducibility, including clear metadata and a defined bioinformatics workflow

## Relevance to environmental monitoring (Analysts’ perspective)
- Standardized, auditable data streams enable monitoring of bat dietary breadth and prey community changes over time
- Potential to integrate with other environmental datasets (e.g., insect community surveys, habitat data) to assess ecosystem health and policy performance
- Data storage and access: structured formats and accompanying scripts support data hosting and sharing through appropriate portals
- Challenges to address in monitoring use:
  - Increasing the value of these datasets by integrating with additional data sources (avoiding single-use outputs)
  - Providing access to underlying data and methods to end-users and stakeholders for transparency and reuse