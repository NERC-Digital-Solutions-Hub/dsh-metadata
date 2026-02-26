# Supporting information for: Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

- Purpose: Report data and methods for assessing realistic environmental concentrations of potential pathogens on microplastic beads from Scottish beaches, in support of NERC-funded projects on marine plastics and microbial hitchhikers.

## Data and datasets

- There are twelve CSV data files collecting field observations, nurdle characteristics, bacterial concentrations, sand and water measurements, and genomic/virulence data for Klebsiella isolates.
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
- Filenames note: content is correct though file names do not precisely reflect data periods.

## Sampling locations and timing

- Data collected from ten Scottish beaches: Montrose, Broughty Ferry (2), Yellowcraig, Portobello, Eyemouth, Erskine, Largs, Turnberry, Ayr, Irvine.
- Sampling occurred in November 2022.

## Sample collection and data collection methods

- Microplastic beads collected on five days in November 2022 using sterile forceps; beads sorted by polymer (PE and PS) and by colour (white PE most abundant); beaches with fewer than 10 beads per polymer excluded due to insufficient replication.
- Bacteria quantified using selective media with standardized washes and serial dilutions; representative CFU counted after incubation on multiple selective media (Campylobacter, E. coli, Enterococci, Klebsiella, Pseudomonas, Salmonella, Vibrio) under specified conditions.
- Environmental measurements taken on sampling: salinity, electrical conductivity, turbidity; polymer identification via FTIR.

## Isolate sequencing and bioinformatics

- Klebsiella isolates from plastics underwent DNA extraction, quantification, quality checks, and Oxford Nanopore sequencing (MinION) with barcoding.
- Genome assembly: trimmed reads, normalisation, Flye assembler; quality checks with CheckM and taxonomy via GTDB-Tk.
- Analyses included: phylogeny, pathogenicity prediction, virulence genes (VirulenceFinder), resistance genes (ResFinder), plasmids (PlasmidFinder), mobile elements, and viral signals (VirSorter).
- Final genome selection: replicates confirmed to be the same species; the most complete genome among replicates used for downstream analysis.

## Galleria mellonella virulence testing

- In vivo infection model using Galleria mellonella larvae to assess virulence of Klebsiella isolates.
- Preparation: overnight Klebsiella cultures adjusted to exponential phase, washed, and serially diluted in PBS.
- Injections: groups of 10 larvae received 10 μL bacterial suspension (roughly 10^4–10^6 CFU) per larva; positive control with clinical pathogenic K. pneumoniae (ATCC 13883); negative PBS control; tests performed in triplicate.
- Outcomes: larval survival monitored at 24, 48, and 72 hours post-injection.

## Purpose and funding

- Data collected to understand realistic environmental concentrations and pathogenic potential of microbes associated with microplastics on beaches.
- Linked to UKRI NERC grants: “Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the Plastisphere” and the SPACES project.

## Roles and provenance

- Data collection, sequencing, bioinformatics, and interpretation overseen by Rebecca Metcalf.

## Completeness and data quality

- Data were screened for anomalies; missing values are marked as ND.
- Notes indicate some data may lack details such as administrative boundaries; data files include explicit field descriptions to enable reuse.

## Data file contents and field descriptions

- FieldObservationsBeaches2023: site name/number, water temperature, salinity, organic matter, substrate type, beach users, weather, nurdles counts (overall and PS), colour.
- NurdleColour2023: site-wise counts by nurdle colour (white, yellow, blue, grey, green, red, purple, pink, black) and totals.
- BacterialConcentrationsOnNurdles2023: site, nurdle material, bacteria species, replicate, CFU counts, number of nurdles, CFU per 100 nurdles.
- BacterialConcentrationsInWater2023: site, bacteria species, replicate, CFU counts in 12 mL and 100 mL.
- BacterialConcentrationsInSand2023: site, bacteria species, replicate, CFU per 2 g and 1 g (wet weight), percent weight change after drying, CFU per 100 g dry weight.
- SandDryWeight2023: site, replicate, weights before/after drying, difference, percent change.
- VirulenceOfKlebsiellaIsolatesFromPlastics2023: bacteria species, material, replicate, concentration, survival counts at 24/48/72 h.
- GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023: sequencing statistics per isolate (barcodes, sample, taxonomy, completeness, contamination, GC, coverage, contigs, gene counts, pathogen likelihood, etc.).
- CombinedGenomeSamplesOfKlebsiellaFromPlastics2023: integrated genome statistics across isolates (species_ID, contigs, completeness, contamination, GC, coverage, etc.).
- VirulenceFinderOfKlebsiellaFromPlastics2023: virulence-factor data with context (material, sample, contig, position, identity, coverage, etc.).
- ResistanceFinderOfKlebsiellaFromPlastics2023: antibiotic resistance findings with contig positions, gene names, phenotypes, identity/coverage.
- PlasmidFinderOfKlebsiellaFromPlastics2023: plasmid-related data with contig details, plasmid names, identity, notes.

## Bibliography

- References to assembly, quality assessment, taxonomy, pathogenicity tools, antimicrobial resistance detection, plasmid detection, and related infection-risk literature.