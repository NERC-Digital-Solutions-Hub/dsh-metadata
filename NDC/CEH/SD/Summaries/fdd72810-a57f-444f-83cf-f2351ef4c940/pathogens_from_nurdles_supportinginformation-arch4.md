# Supporting information for:
Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

- Objective and dataset scope
  - Study of realistic environmental concentrations of potential pathogens colonising microplastic beads (nurdes) on Scottish beaches.
  - Data comprise twelve CSV files detailing field observations, nurdle characteristics, bacterial concentrations, sand and water metrics, virulence and genome data for Klebsiella isolates, and related analyses.

- Data assets (files and purpose)
  - FieldObservationsBeaches2023 – field observations per beach (water temp, salinity, organic matter, substrate, beach usage, weather, nurdles, colors, etc.)
  - NurdleColour2023 – counts by colour (white, yellow, blue, grey, green, red, purple, pink, black) and totals per site
  - BacterialConcentrationsOnNurdles2023 – CFU counts by bacteria species on nurdles, replicates, and CFU per 100 nurdles
  - BacterialConcentrationsInWater2023 – CFU counts in water by species, replicates
  - BacterialConcentrationsInSand2023 – CFU counts in sand by species, replicates, dry weight changes
  - SandDryWeight2023 – dry weight measurements for sand samples
  - VirulenceOfKlebsiellaIsolatesFromPlastics2023 – virulence assay results (Galleria mellonella survival) for Klebsiella from plastics
  - GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023 – genome assembly and quality statistics
  - CombinedGenomeSamplesOfKlebsiellaFromPlastics2023 – combined genome assembly data
  - VirulenceFinderOfKlebsiellaFromPlastics2023 – virulence gene findings
  - ResistanceFinderOfKlebsiellaFromPlastics2023 – antimicrobial resistance gene findings
  - PlasmidFinderOfKlebsiellaFromPlastics2023 – plasmid content findings
  - Note: Filenames do not strictly reflect data period, but content is correct.

- Study locations and timing
  - Ten Scottish beaches (Montrose, Broughty Ferry, Yellowcraig, Portobello, Eyemouth, Erskine, Largs, Turnberry, Ayr, Irvine).
  - Sampling occurred in November 2022 (with a map provided in the accompanying document).

- Sampling and laboratory methods
  - Microplastic beads collected via sterile forceps, sorted by polymer (PE or PS); white PE beads selected for analysis due to abundance.
  - Exclusion criterion: sites with fewer than 10 beads of each polymer excluded due to insufficient replicates.
  - Bacteria quantified on selective media after rinsing and pooling washes; CFU counted after incubation under specified conditions for each target organism.
  - Environmental metadata: salinity, electrical conductivity, turbidity measured with dedicated instruments; polymer identity confirmed via FTIR.

- Genomics and bioinformatics pipeline
  - DNA extraction, quality checks (NanoDrop, gel).
  - Ligation sequencing libraries prepared and Oxford Nanopore sequencing performed (MinION).
  - Basecalling with Guppy; reads filtered (Q>8, >1000 bp).
  - Genome assembly with Flye; trimming/normalisation with BBDuk/BBNorm.
  - Annotation and quality assessment (CheckM) and taxonomic placement (GTDBtk).
  - Phylogeny (SpeciesTree), pathogenicity (PathogenFinder), virulence genes (VirulenceFinder), resistance genes (ResFinder), plasmids (PlasmidFinder), and viral elements (VirSorter).
  - Taxonomy confirmation for combined assemblies; replicates consolidated, selecting the most complete genome for downstream analyses.

- In vivo virulence assessment
  - Galleria mellonella infection model using Klebsiella isolates from Site 2.
  - Standardized growth to exponential phase, injections into larvae hemocoel, with appropriate positive (clinical strain ATCC 13883) and negative controls.
  - Larval survival assessed at 24, 48, and 72 hours; experiments performed in biological triplicate.

- Data purpose and funding
  - Data generated to understand environmental concentrations and pathogenic potential of microbes attached to plastics.
  - Collected under UKRI NERC grants: Microbial hitchhikers of marine plastics (NE/S005196/1) and the SPACES project (NE/V005847/1).

- Data stewardship and responsibility
  - Primary responsibility for data collection and interpretation: Rebecca Metcalf.
  - Completeness checks performed; missing data indicated as “ND.”
  - Data files annotated with detailed field descriptions to aid reuse and discoverability.

- Data structure, metadata, and discoverability
  - Each data file (8.1–8.12) includes explicit column definitions and units.
  - Clear descriptions for variables such as site, replicate, CFU counts, concentration measures, and bioinformatics outputs (virulence, resistance, plasmids, genome statistics).

- Governance, quality, and reuse considerations for data leaders
  - Highlights the importance of centralized data assets with consistent metadata, transparent provenance, and rigorous quality checks.
  - Illustrates multi-disciplinary data integration (ecology, microbiology, genomics, in vivo virulence) and reproducible workflows with explicit tool usage and sequencing parameters.
  - Demonstrates need for cross-team coordination and documentation to ensure data remain discoverable, trustworthy, and reusable within wider data communities. 

- References and tools
  - Bibliography includes assembly and QC tools (CheckM, GTDBtk), genome analysis pipelines (SpeciesTree, PathogenFinder, VirulenceFinder, ResFinder, PlasmidFinder, VirSorter) and related methodological sources.