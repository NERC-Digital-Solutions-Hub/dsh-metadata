# Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

## Quick overview
- A study of realistic environmental concentrations of potential pathogens on microplastic nurdles collected from Scottish beaches in November 2022.
- Data are organized into twelve CSV files covering field observations, nurdle characteristics, microbial counts on nurdles, in water and sand, sand dry weight, and extensive genomic and virulence data for Klebsiella isolates recovered from plastics.
- Includes an infection model (Galleria mellonella) to assess virulence of Klebsiella isolates.
- Data intended to support understanding of pathogen presence on beach plastics and guide GIS-enabled mapping and risk assessment.

## Data collection and study design
- Sampling targeted microplastic beads (PE and PS) collected from ten Scottish beaches (Montrose; Broughty Ferry; Yellowcraig; Portobello; Eyemouth; Erskine; Largs; Turnberry; Ayr; Irvine).
- Beads collected on five days in November 2022; beads were sorted by polymer (PE vs PS) and PE beads sorted by color (white most analyzed).
- Sites with fewer than 10 beads of each polymer were excluded due to insufficient replication.

## Datasets included
- 12 CSV files covering field and lab data, as well as genomic and virulence analyses:
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

## Site locations
- Sampling locations mapped on the east and west coasts of Scotland (Figure 1). Ten beaches were selected to represent littoral environments and plastic pollution contexts.

## Methods

### Field sampling
- Microplastic beads collected with sterile forceps and placed into sterile bags.
- Sorting by material (PE or PS); white PE beads selected for further analysis due to abundance.
- Field measurements recorded: water temperature, salinity, organic matter, substrate type, beach usage, weather, and other observational data.

### Microbiological analysis
- Bacteria quantified using selective media for multiple genera/species (e.g., Campylobacter, E. coli, Enterococci, Klebsiella spp., Pseudomonas, Salmonella, Vibrio).
- Procedures included bead washes, filtration, incubation under specified conditions, and enumeration of CFUs.
- Environmental water and sand samples also analyzed for bacterial concentrations.

### Environmental measurements
- Salinity, electrical conductivity (EC), and turbidity measured in situ with appropriate instruments.
- FTIR used to identify polymer composition of nurdles.

## Genomic sequencing and bioinformatics
- Klebsiella isolates from plastics subjected to DNA extraction, sequencing (Oxford Nanopore MinION), and basecalling.
- Genome assembly and annotation conducted; quality assessed for completeness and contamination.
- Taxonomic confirmation and phylogeny built; pathogenicity assessed.
- Screening for virulence factors, antimicrobial resistance genes, plasmids, and mobile genetic elements using dedicated tools.
- Replicates merged to select the most complete genome for downstream analysis after confirming same-species replicates.

## Infection model
- Galleria mellonella larvae used to assess virulence of Klebsiella isolates from plastics.
- Standardized infection: injection of 10 μl bacterial suspension into larvae, with positive and negative controls.
- Larvae maintained at 37°C; survival assessed at 24, 48, and 72 hours post-injection.

## Purpose and funding
- Data collected to quantify realistic environmental concentrations of potential pathogens on microplastic beads.
- Aligns with UKRI NERC grants: Microbial hitchhikers of marine plastics (NE/S005196/1) and the SPACES project (NE/V005847/1).

## Data quality and completeness
- Data checked for anomalies; upper/lower limits reviewed.
- Missing data recorded as “ND” (No Data).
- Note on data filenames: content is correct despite filename mismatches with the data period.

## Data file contents (summary)
- FieldObservationsBeaches2023: Beach/site observations including SiteName, SiteNumber, WaterTemp (°C), Salinity (%), Organic matter (%), SubstrateType, BeachUsers, Weather, Nurdles, PS, Colour.
- NurdleColour2023: Counts by color per site (White, Yellow, Blue, Grey, Green, Red, Purple, Pink, Black) and totals.
- BacterialConcentrationsOnNurdles2023: Per-site, per-material nurdle bacterial counts by species, with replicate IDs, CFU counts, and CFU per 100 nurdles.
- BacterialConcentrationsInWater2023: Per-site water counts by bacterial species, with replicates and CFU in 12 ml and 100 ml samples.
- BacterialConcentrationsInSand2023: Per-site sand counts by species, replicates, CFU per 2 g, per 1 g (wet weight), percent change, and CFU per 100 g dry weight.
- SandDryWeight2023: Per-site dry weight measurements with replicates, including before/after drying weights and percentage change.
- VirulenceOfKlebsiellaIsolatesFromPlastics2023: Virulence data for Klebsiella isolates from plastics, including concentration used and larval survival at 24/48/72 h.
- GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023: Genomic stats such as barcode, isolate, sample source, number of sequences, taxonomy, strain, completeness, contamination, GC%, coverage, plasmids, MGEs, contigs, longest contig, rRNA genes.
- CombinedGenomeSamplesOfKlebsiellaFromPlastics2023: Combined genome statistics across isolates (species ID, strain number, completeness, contamination, GC%, coverage, contigs, longest contig).
- VirulenceFinderOfKlebsiellaFromPlastics2023: Virulence factor data (contigs, positions, factor names, protein functions, accession numbers, coverage, identity).
- ResistanceFinderOfKlebsiellaFromPlastics2023: Antimicrobial resistance findings (gene names, phenotypes, contig positions, coverage, identity, accession).
- PlasmidFinderOfKlebsiellaFromPlastics2023: Plasmid findings (contigs, positions, contig lengths, plasmid names, identity, notes, accession).

## Data provenance and usage notes
- Data were collected under the specified grants and produced by the study team led by Rebecca Metcalf.
- The collection, sequencing, and analysis workflow integrates field data with genomic and virulence data to enable GIS-based spatial analyses and cross-dataset visualizations.

## Responsible person
- Rebecca Metcalf

## References
- Includes methodological and software references for genome assembly, quality assessment, taxonomy, pathogenicity prediction, virulence/AMR gene detection, and plasmid analysis.