# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Data overview
- rep_95.fasta: cleaned, simplified, quality-controlled set of nucleotide sequences in FASTA format.
- interaction_table.csv: a binary interaction matrix where columns correspond to bats (as listed in reps_95.fasta) and a '1' indicates a detected interaction (predation) with prey; '0' indicates no interaction.
- bat_capture_data.csv: capture metadata for bats, including sample IDs that link to the other two files.
- The interaction table is designed to be converted to the desired format using a provided script.

## Sampling, sequencing and bioinformatics
- Study scope: capture and dietary data for insectivorous bats in Sabah, Malaysia.
- Locations: Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project.
- Field collection: 6 harp traps per location, deployed for one night; sampling occurred between 2015 and 2017.
- Guano processing: samples collected from captured bats and sequenced in the UK.
- Laboratory workflow at Queen Mary University of London:
  - DNA extraction
  - PCR using Zeale (2011) primers
  - Library preparation and index PCR
  - Illumina MiSeq sequencing (150–250 bp, paired-end)
  - Demultiplexing
  - Read merging and quality filtering
  - Singleton removal
  - OTU clustering at 95% similarity; post-clustering refinement
  - Creation of the interaction table
- Personnel: all samples collected by DHB, VK, JB; DHB and JB conducted the lab work, DHB analyzed the data.
- Data completeness: no data omitted.

## Details of data structure
- Interaction CSV: can be converted to alternative formats using the script r_network_gen.r, available at:
  https://github.com/hemprichbennett/bat-diet
- bat_capture_data.csv columns:
  - TrapName: unique trap identifier
  - Lat, Long: geographic coordinates (NA if GPS error)
  - Elevation: elevation (NA if missing)
  - Bat_no: capture number
  - Day, Month, Year, Date: capture date
  - Faeces_no1, Faeces_no2: tube IDs for fecal samples
  - Block: experimental block at SAFE project
  - Fragment: fragment size for SAFE project
  - Site: Sabah site of capture
  - Species: bat species code (see below)
  - Sex, Age: sex and age (J = juvenile, A = adult; blank if not recorded)
  - Note: blank cells indicate missing values
- Species codes (mapping provided in document) include codes for multiple bat species (e.g., Emballonura alecto = Elal, Emballonura monticola = Elmo, Harpiocephalus harpia = Haha, etc.), covering a range of genera such as Emballonura, Hipposideros, Kerivoula, Macroglossus, Megaderma, Megaerops, Murina, Myotis, Nycteris, Phoniscus, Philetor, Pipistrellus, Rhinolophus, Scotophilus, and others.

## Data accessibility and usage notes
- The interaction data can be generated into different formats via the r_network_gen.r script located in the referenced GitHub repository.
- The dataset provides linkages between physical capture data (locations and metadata) and molecular diet information (prey detected via metabarcoding), enabling spatial visualization of bat-diet interactions when combined with the coordinate data.

## GIS relevance and potential applications
- The included latitude/longitude, site, and trap metadata enable map-based visualization of bat captures and their inferred prey interactions.
- Data can be integrated to analyze spatial patterns in bat diets across Sabah’s conservation areas and the SAFE project site.
- The linkage between capture records and molecular interaction data supports creating interactive maps and network visualizations of predator-prey relationships across space and time.