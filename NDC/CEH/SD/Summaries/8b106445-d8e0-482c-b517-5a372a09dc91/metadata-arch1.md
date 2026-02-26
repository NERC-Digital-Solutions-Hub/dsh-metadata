# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Data overview
- reps_95.fasta: cleaned, simplified, and quality-controlled nucleotide sequences in FASTA format.
- interaction_table.csv: binary interaction matrix (1 = detected interaction, 0 = no interaction) with columns corresponding to the bats listed in reps_95.fasta.
- bat_capture_data.csv: metadata for bat captures, including sample IDs linking to the other two files.
- The study represents dietary data for 10 bat species, indicated by species codes provided at the bottom of the document.
- All samples were collected across multiple sites in Sabah, Malaysia (Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project).

## Sampling, sequencing and bioinformatics
- Ecological study of insectivorous bats captured at three sites in Sabah between 2015 and 2017.
- Bats captured using 6 harp traps per location for one night; guano collected from captured bats and processed in the UK.
- Metabarcoding and high-throughput sequencing performed at Queen Mary University of London to classify consumed prey into MOTUs (Molecular Operational Taxonomic Units).
- Sequencing workflow: DNA extraction -> PCR with Zeale primers -> library build and index PCR -> 150-250 bp paired-end Illumina MiSeq -> demultiplex -> merge reads and quality filter -> remove singletons -> cluster into OTUs at 95% similarity -> post-clustering filtering -> create interaction table.
- Researchers: DHB, VK, JB (lab work by DHB and JB; data analysis by DHB); no data omitted.

## Details of data structure
- The interaction_table.csv can be converted to other formats using the script r_network_gen.r, available at https://github.com/hemprichbennett/bat-diet.
- bat_capture_data.csv column meanings:
  - TrapName, Lat, Long, Elevation, Bat_no, Day, Month, Year, Date
  - Faeces_no1, Faeces_no2 (tube IDs for fecal samples)
  - Block, Fragment (relevant to SAFE project)
  - Site, Species (bat species code), Sex, Age
  - Blank cells indicate missing values
- Species codes map to full species names (a long list covering Emballonura, Harpiocephalus, Hesperoptenus, Hipposideros, Kerivoula, Macroglossus, Megaderma, Megaerops, Murina, Myotis, Nycteris, Phoniscus, Philetor, Pipistrellus, Rhinolophus, Scotophilus, and others).
- All samples were collected by DHB, VK, and JB; lab work by DHB and JB; analyses by DHB; no data omissions.
- The document provides a comprehensive mapping between bat IDs in reps_95.fasta and their corresponding capture metadata in bat_capture_data.csv.

## Access and reuse
- r_network_gen.r used to convert the interaction CSV is hosted on GitHub: https://github.com/hemprichbennett/bat-diet.
- Data descriptions, methods, and metadata enable construction and analysis of bat-prey interaction networks, site comparisons, and prey diversity assessments by bat species.

## Analyses and applications (for analysts)
- Build bipartite networks of bat–prey interactions to identify key prey taxa for different bat species.
- Compare prey spectra and interaction richness across sites (Danum Valley, Maliau Basin, SAFE project).
- Explore correlations between bat traits (e.g., species, sex, age) and prey composition or detection rates.
- Develop predictive models of prey diversity or interaction likelihood under different spatial or temporal conditions.
- Integrate with other datasets by linking rep_95 sequences to prey MOTUs and Exercise OTU data.