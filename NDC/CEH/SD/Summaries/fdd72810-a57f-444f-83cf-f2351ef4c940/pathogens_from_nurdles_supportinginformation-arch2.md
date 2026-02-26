# Supporting information for: Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

- Purpose and scope
  - Study of realistic environmental concentrations of potential pathogens colonising microplastic beads (nurdles) on Scottish beaches.
  - Data collected to support UKRI/NERC grants related to microbial hitchhikers of marine plastics and related ecology projects.
  - Data include bacterial concentrations on nurdles, in water and sand, and virulence/genome information for Klebsiella isolates from plastics.

- Data products and file structure
  - Twelve CSV data files, content correct though filenames do not perfectly match data period.
  - Data categories include field observations, nurdle colours, bacterial concentrations on nurdles, in water, and in sand, sand dry weight, virulence and genome statistics for Klebsiella, and associated in silico analyses (virulence, resistance, plasmids).
  - File list:
    - FieldObservationsBeaches2023
    - NurdleColour2023
    - BacterialConcentrationsOnNurdles2023
    - BacterialConcentrationsInWater2023
    - BacterialConcentrationsInSand2023
    - SandDryWeight2023
    - VirulenceOfKlebsiellaIsolatesFromPlastics2023
    - GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023
    - CombinedGenomeSamplesOfKlebsiellaFromPlastics2023
    - VirulenceFinderOfKlebsiellaFromPlastics2023
    - ResistanceFinderOfKlebsiellaFromPlastics2023
    - PlasmidFinderOfKlebsiellaFromPlastics2023
  - Data identifiers and fields are described within each file overview (see sections 8.1–8.12 for details).

- Sampling locations and timing
  - Ten Scottish beaches sampled: Montrose, Broughty Ferry, Yellowcraig, Portobello, Eyemouth, Erskine, Largs, Turnberry, Ayr, Irvine.
  - Sampling conducted in November 2022.
  - Figure map provided to show sampling sites on east and west coasts.

- Sampling and laboratory methods (4.1–4.3)
  - Nurdle collection and sorting
    - Microplastic beads collected on five days in November 2022 using sterile forceps; beads sorted by material (PE or PS) and PE beads by colour (white selected for analysis).
    - Sites with fewer than 10 beads of each polymer excluded from analysis.
  - Bacterial quantification
    - Washing protocol for nurdles, suspension in PBS, filtration onto selective media.
    - Media used to target specific bacteria: Campylobacter, E. coli, enterococci, Klebsiella, Pseudomonas, Salmonella, Vibrio.
    - Incubation conditions per medium; positive colonies counted as CFU.
    - Additional measurements: salinity, electrical conductivity, turbidity; FTIR used to identify polymer composition.
  - Isolate sequencing and bioinformatics (Klebsiella)
    - DNA extraction, quality checks (NanoDrop, gel).
    - Nanopore sequencing (ONT MinION) with barcoding; basecalling and read filtering (Q>8, >1000 bp).
    - Genome assembly (Flye) with trimming/normalisation steps; annotation via KBase and DTU resources.
    - Quality checks: completeness and contamination (CheckM); species ID (GTDBtk); phylogeny (SpeciesTree); pathogenicity (PathogenFinder); virulence genes (VirulenceFinder); resistance genes (ResFinder); plasmids (PlasmidFinder); virus detection (VirSorter).
    - Taxonomy confirmed for combined assemblies; replicates reconciled; the most complete genome chosen for further analysis.

- In vivo virulence model (4.3)
  - Galleria mellonella infection model to assess virulence of Klebsiella isolates from plastics.
  - Bacterial cells prepared in exponential phase, serial dilutions, and injected into larvae; controls included a positive pathogenic strain and PBS negative control.
  - Mortality assessed at 24, 48, and 72 hours post-injection; injections performed in triplicate with sterile technique.

- Data completeness and quality
  - Missing data marked as ND.
  - Data checked for anomalies and outliers; sites with insufficient replication excluded from analyses.

- Data use and accessibility considerations for environmental monitoring
  - Data are organized to enable integration with other environmental datasets (e.g., combining nurdle-associated microbial data with site physico-chemical and ecological context).
  - Standardised formats and descriptive metadata support transparency and longitudinal monitoring.
  - Data storage and portal deposition considerations implied by the authors (dataset curation and reuse in monitoring workflows).

- Data file contents (overview by dataset)
  - FieldObservationsBeaches2023: site-level observations including water temperature, salinity, organic matter, substrate type, beach usage, weather, nurdle counts (overall and by PS), and colour notes.
  - NurdleColour2023: counts of nurdles by colour per site, including white, yellow, blue, grey, green, red, purple, pink, black, and total.
  - BacterialConcentrationsOnNurdles2023: per-site, per-replicate CFU counts for each bacterial species on nurdles; includes material, replicate, number of nurdles, and CFU per 100 nurdles.
  - BacterialConcentrationsInWater2023: per-site, per-replicate CFU counts in water for each bacterial species; includes volume metrics.
  - BacterialConcentrationsInSand2023: per-site, per-replicate CFU counts in sand (2 g, 1 g wet weight, 100 g dry weight) plus percentage weight change during drying.
  - SandDryWeight2023: sand dry weight experiment data (before/after drying, differences, and percentage change) per site and replicate.
  - VirulenceOfKlebsiellaIsolatesFromPlastics2023: virulence assay outcomes (numbers alive at 24h/48h/72h) for Klebsiella isolates on plastics, with concentration and replication details.
  - GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023 and CombinedGenomeSamplesOfKlebsiellaFromPlastics2023: sequencing and assembly statistics (barcodes, contigs, completeness, contamination, GC%, coverage, longest contig, rRNA genes) and combined genome stats across replicates.
  - VirulenceFinderOfKlebsiellaFromPlastics2023, ResistanceFinderOfKlebsiellaFromPlastics2023, PlasmidFinderOfKlebsiellaFromPlastics2023: in silico characterisation results including virulence factors, resistance genes, and plasmids with positional and identity data.
  - Each dataset includes variable descriptions and units to support consistent interpretation and cross-dataset analyses.

- Bibliography and tools referenced
  - Genome assembly and quality assessment: Flye; CheckM; GTDB-Tk; SpeciesTree; PathogenFinder; VirulenceFinder; ResFinder; PlasmidFinder; VirSorter.
  - Taxonomic and phylogenetic methods: GTDB taxonomy, SpeciesTree, and related tools.
  - Analytical references for sequencing and in silico characterisation of Klebsiella isolates and environmental pathogens.