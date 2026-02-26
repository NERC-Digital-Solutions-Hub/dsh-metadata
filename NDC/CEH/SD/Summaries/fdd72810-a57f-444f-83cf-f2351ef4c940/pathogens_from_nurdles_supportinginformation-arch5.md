# Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

- Purpose and scope
  - Study of realistic environmental concentrations of potential pathogens colonising microplastic beads on Scottish beaches.
  - Supports UKRI NERC projects on microbial hitchhikers of marine plastics.

- Data and structure
  - Twelve CSV files containing:
    - Field observations at beaches
    - Nurdle colour counts
    - Bacterial concentrations on nurdles, in water, and in sand
    - Sand dry weight and drying changes
    - Virulence and genome-related data for Klebsiella isolates from plastics
  - Note: Filenames may not reflect the data period, but file contents are correct.

- Sampling locations and timing
  - Ten Scottish beaches (Montrose; Broughty Ferry; Yellowcraig; Portobello; Eyemouth; Erskine; Largs; Turnberry; Ayr; Irvine)
  - Beads collected in November 2022
  - Map reference provided in the accompanying figures

- Field and laboratory methods (highlights)
  - Microplastic beads collected, sorted by polymer (PE/PS) and colour (white PE analysed); sites with fewer than 10 beads per polymer excluded.
  - Bacterial quantification on selective media with standardized washes and filtration; CFU enumerated after incubation.
  - Environmental metadata collected: salinity, conductivity, turbidity, organic matter, substrate type, beach user presence, weather.
  - Polymer identification via Fourier Transform Infrared Spectrometry (FTIR).
  - Isolate sequencing: DNA extraction, Oxford Nanopore long-read sequencing, basecalling, assembly (Flye), quality checks (CheckM, GTDB-Tk), annotation, and taxonomic confirmation.
  - Comparative genomics and virulence/resistance/plasmid analyses using established tools (PathogenFinder, VirulenceFinder, ResFinder, PlasmidFinder, etc.).
  - Phylogenetic and sample consolidation steps to select the most complete genome per isolate.

- Virulence assessment
  - Galleria mellonella infection model with Klebsiella isolates from plastics (site 2), including controls and repeated biological trials.
  - Survival monitoring at 24, 48, and 72 hours post-injection.

- Data provenance and purpose
  - Data collected to understand environmental concentrations and pathogenic potential of microbes associated with marine plastics.
  - Supported by NERC grants: “Microbial hitchhikers of marine plastics” and SPACES project.
  - Principal data steward: Rebecca Metcalf.

- Data completeness and quality control
  - Data checked for anomalous values; missing data flagged as ND.
  - Sequencing data quality criteria documented (reads with Q > 8 and >1000 bp used; assembly and contamination checks performed).
  - Replicates validated for species consistency; the most complete genome retained for downstream analysis.

- Data file contents (summary of each CSV)
  - FieldObservationsBeaches2023: Beach/site field observations (water temp, salinity, organic matter, substrate, beach use, weather, nurdle counts).
  - NurdleColour2023: Counts by colour for nurdles per site.
  - BacterialConcentrationsOnNurdles2023: Bacteria on nurdles by site, material, species, replication, CFU, and CFU per 100 nurdles.
  - BacterialConcentrationsInWater2023: Bacteria in water by site, species, replicate, CFU per 12 ml and per 100 ml.
  - BacterialConcentrationsInSand2023: Bacteria in sand by site, species, replicate, CFU per 2 g, per 1 g wet weight, and per 100 g dry weight; includes percentage weight change.
  - SandDryWeight2023: Dry weight measurements for sand samples.
  - VirulenceOfKlebsiellaIsolatesFromPlastics2023: Virulence assay results (Galleria survival) for Klebsiella isolates, with concentration and timepoints.
  - GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023: Assembly/sequence quality metrics and taxonomy for Klebsiella isolates.
  - CombinedGenomeSamplesOfKlebsiellaFromPlastics2023: Consolidated genome stats across replicates.
  - VirulenceFinderOfKlebsiellaFromPlastics2023: In silico virulence factor data per isolate/contig.
  - ResistanceFinderOfKlebsiellaFromPlastics2023: Antimicrobial resistance gene data per isolate/contig.
  - PlasmidFinderOfKlebsiellaFromPlastics2023: Plasmid content and contig details per isolate.
  - Note: “ND” used for missing data.

- Data governance and stewardship notes
  - Data steward and collection responsibility: Rebecca Metcalf.
  - Data are provided as CSVs with explicit field descriptions to support discoverability and reuse.
  - Filenames: content-dominant; period misalignment acknowledged; the data content is correct.
  - Completeness tracking and QC indicators documented to assist data custodians and users in assessing reliability.

- Practical implications for reuse
  - Rich, multi-faceted dataset suitable for studies on environmental microbiology, plastisphere communities, and virulence/resistance profiling.
  - Provides a clear lineage from field collection to sequencing and virulence testing, aiding reproducibility.
  - Versioning and updates recommended if extensions or re-analyses are planned, given the governance notes and provenance.