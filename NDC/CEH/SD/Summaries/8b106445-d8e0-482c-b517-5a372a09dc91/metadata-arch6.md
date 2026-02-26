# Metabarcoding data from the guano of insectivorous bats in Sabah, Malaysia

## Data overview
- Data files:
  - reps_95.fasta: cleaned, quality-controlled sequence data in FASTA format.
  - interaction_table.csv: binary interaction matrix (1 = detected bat–prey interaction, 0 = no interaction); columns correspond to bats (per the IDs in reps_95.fasta); rows represent detected prey MOTUs.
  - bat_capture_data.csv: metadata for bat captures, including sample IDs linking to the other two files.
- Study scope and data products:
  - Metabarcoding data capture and dietary characterization for insectivorous bats captured in Sabah, Malaysia.
  - 10 bat species represented; samples collected between 2015–2017.
  - Output includes a putative bat–prey interaction matrix and the underlying sequence data used to derive MOTUs.
- Data provenance and quality:
  - All samples collected by DHB, VK, and JB; lab work by DHB and JB; data analysis by DHB.
  - No data omitted; rigorous quality control and processing steps applied to sequence data.

## Data structure and access
- Interaction data format:
  - Interaction table created from sequencing data; can be converted to alternative formats using the provided script (see below).
- Access to the conversion tool:
  - r_network_gen.r script available at https://github.com/hemprichbennett/bat-diet to transform the interaction CSV into other network formats.
- bat_capture_data.csv structure (key columns and meanings):
  - TrapName: unique trap identifier
  - LatLong: GPS coordinates (Lat, Long) and Elevation (if recorded)
  - Bat_no: bat capture number
  - Day, Month, Year, Date: capture timing
  - Faeces_no1, Faeces_no2: tube IDs for fecal samples
  - Block, Fragment: experimental block and fragment size (SAFE project)
  - Site: Sabah site of capture
  - Species: bat species code (see mapping below)
  - Sex, Age: recorded sex and age (J = juvenile, A = adult)
  - Blank cells indicate missing values
- Species code mapping:
  - Detailed mapping from short codes (e.g., Emal. for Emballonura alicto, etc.) to full species names is provided in the data document (list includes many Hipposideros, Kerivoula, Myotis, Rhinolophus, Pipistrellus, and others).

## Sampling, sequencing, and bioinformatics
- Study design:
  - Bats captured at Danum Valley Conservation Area, Maliau Basin Conservation Area, and the SAFE project sites in Sabah, Malaysia.
  - Harp traps used (6 per location) for one night per sampling occasion; sampling occurred 2015–2017.
  - Guano collected from captured bats and processed in the UK.
- Laboratory workflow (Queen Mary University of London):
  - DNA extraction; PCR using Zeale (2011) primers; library build and index PCR; 150–250 bp paired-end Illumina MiSeq sequencing.
  - Bioinformatics:
    - Demultiplex reads; merge reads and apply quality filters.
    - Remove singletons; cluster OTUs at 95% similarity; post-clustering filtering.
    - Create the bat–prey interaction table from MOTUs.
- Roles and scope:
  - All samples collected by the three authors; lab work by DHB and JB; data analysis by DHB.
- Data completeness:
  - No data omitted; full pipeline applied to all samples.

## Usage, reuse, and integration
- Potential data products for end users:
  - Self-serve exploration of bat–prey interactions via the interaction_table.csv and MOTU-based data.
  - Reuse of the FASTA file (reps_95.fasta) for downstream phylogenetic or OTU analyses.
  - Conversion to alternative network formats using the r_network_gen.r script.
- Documentation and provenance:
  - Comprehensive methodological details included (sampling locations, primers, sequencing platform, OTU clustering threshold).
  - Species and specimen metadata linked to the interaction data to support cross-dataset analyses.

## Considerations for researchers (key notes)
- The dataset represents a single ecological study window (2015–2017) across specific Sabah sites; broader generalizations should be made cautiously.
- Prey identifications are MOTUs derived from metabarcoding; some taxa may be unresolved to species level due to primer biases or reference databases.
- The data support the construction and exploration of bipartite networks of bat–prey interactions and can be integrated with additional ecological or environmental data for broader analyses.