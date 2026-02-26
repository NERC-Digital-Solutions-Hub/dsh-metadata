# Supporting information for: Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

- Purpose and scope
  - Describes data and methods for studying realistic environmental concentrations of potential pathogens on microplastic nurdles collected from Scottish beaches.
  - Supports data exploration, quality assurance, and re-use across related analyses (bacteria, virulence, genomics, and host-infection assays).

- Data files and contents
  - There are twelve CSV files, with content aligned to field observations, nurdle characteristics, bacterial concentrations, and genomic/virulence analyses.
  - File descriptions (high level):
    - FieldObservationsBeaches2023: field observations per beach (salinity, water temp, organic matter, substrate, beach usage, weather, nurdles, color).
    - NurdleColour2023: counts by nurdle color per site.
    - BacterialConcentrationsOnNurdles2023: CFU counts by site, nurdle material, bacteria species, replicates, and CFU per 100 nurdles.
    - BacterialConcentrationsInWater2023: CFU counts in water by site, bacteria, replicates, and concentrations in 12 ml and 100 ml samples.
    - BacterialConcentrationsInSand2023: CFU counts in sand by site, bacteria, replicates, and per-weights/dry-weight metrics.
    - SandDryWeight2023: dry weight measurements for sand samples (before/after drying, differences, percent changes).
    - VirulenceOfKlebsiellaIsolatesFromPlastics2023: virulence assay outcomes (Galleria alive counts) for Klebsiella isolates from plastics.
    - GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023: genome assembly statistics and quality metrics.
    - CombinedGenomeSamplesOfKlebsiellaFromPlastics2023: combined genome statistics across replicates.
    - VirulenceFinderOfKlebsiellaFromPlastics2023: virulence factor findings (where data available).
    - ResistanceFinderOfKlebsiellaFromPlastics2023: antimicrobial resistance findings.
    - PlasmidFinderOfKlebsiellaFromPlastics2023: plasmid content findings.
  - Note: Filenames may not reflect the data period, but content is correct.

- Sampling locations and timing
  - Ten Scottish beaches: Montrose, Broughty Ferry, Yellowcraig, Portobello, Eyemouth, Erskine, Largs, Turnberry, Ayr, Irvine.
  - Sampling occurred in November 2022.
  - A map (Figure 1) illustrates sampling sites along east and west coasts.

- Sample collection and laboratory methods (4.1)
  - Microplastic nurdles collected on five days in November 2022 using sterile tools; sorted by polymer (PE vs PS) and by color (white PE prioritized).
  - Exclusion criterion: sites with fewer than 10 nurdles of each polymer were excluded due to insufficient replicates.
  - Bacterial quantification: wash and filter approach; selective media for target organisms (Campylobacter, E. coli, Enterococci, Klebsiella, Pseudomonas, Salmonella, Vibrio); incubation conditions per organism; positive CFU enumerated.
  - Environmental measurements: salinity, electrical conductivity, turbidity measured with specified instruments.
  - Polymer identification: FTIR used to confirm polymer composition.

- Isolate sequencing and bioinformatics analysis (4.2)
  - DNA extraction and QC performed; sequencing with Oxford Nanopore MinION (ONT) using barcoding kit; basecalling with Guppy (Q > 8, reads > 1000 bp).
  - Genome assembly: long-read assembly (Flye) after trimming and normalization; annotation via K Base and DTU tools.
  - Quality checks: CheckM for completeness/contamination; GTDBtk for taxonomy; SpeciesTree for phylogeny.
  - Pathogen and resistance profiling: PathogenFinder; VirulenceFinder; ResFinder; PlasmidFinder; VirSorter for viral signals.
  - Taxonomy confirmation and replicate consolidation: multiple replicates per substrate; selection of the most complete genome for downstream analyses.

- Galleria mellonella infection model (4.3)
  - Larvae prepared and maintained under defined conditions; Klebsiella isolates grown to exponential phase, prepared in PBS.
  - Larvae injected with standardized bacterial doses; positive control included (clinical strain); negative PBS control.
  - Mortality assessed at 24, 48, and 72 hours post-injection to evaluate virulence of isolates from plastics.

- Purpose and funding (5)
  - Data collected to evaluate realistic environmental pathogen concentrations on microplastic beads.
  - Supports the UKRI NERC grants: Microbial hitchhikers of marine plastics and SPACES project (grant numbers NE/S005196/1 and NE/V005847/1).

- Data stewardship and responsibility (6)
  - Data collection and interpretation led by Rebecca Metcalf.

- Completeness and data quality (7)
  - Data checked for anomalies; upper/lower bounds considered.
  - Missing data is explicitly recorded as “ND” (no data).

- Data provenance and usage notes (8)
  - Data captured across multiple domains: field observations, nurdle characteristics, microbial concentrations, sand/water analyses, and genomics/virulence assessments.
  - Each data file uses standardized variable descriptors (e.g., SiteNumber, Rep, CFU values, virulence outcomes, genome metrics).
  - Content aligns with the study aims but may require alignment across files when integrating data for analyses.
  - Filenames may not match the data period, but the data content is period-appropriate.

- References and methodology context (9)
  - Cited methods and tools include long-read assembly with Flye, CheckM quality checks, GTDB-Tk taxonomy, SpeciesTree, PathogenFinder, VirulenceFinder, ResFinder, PlasmidFinder, VirSorter, and prior experimental and clinical pathogenicity literature.

- Practical takeaways for data use
  - The dataset enables multi-layer analyses: environmental microbiology (bacteria on nurdles, in water and sand), polymer-associated virulence potential (Klebsiella isolates), genome-level characterization (completeness, contamination, resistance and virulence gene content, plasmids), and functional virulence assessment (Galleria melanization/infection model).
  - Data products can support dashboards or self-serve exploration (e.g., per-site comparisons of CFU counts, virulence phenotypes, and genomic features) while ensuring traceability to sampling and laboratory workflows.
  - Awareness of data gaps and ND entries is important for robust analyses and reporting.