# Supporting information for: Nurdle characteristics with associated bacterial concentrations and virulence of Klebsiella isolates from Scottish beaches, 2022

- Purpose and scope
  - Study assessing realistic environmental concentrations of potential pathogens on microplastic beads (nurdles) from Scottish beaches.
  - Aimed to inform environmental health monitoring and policy about plastics as pathogen carriers; linked to UKRI/NERC grants on marine microbial hitchhikers.

- Study design and sampling
  - Ten beaches sampled (Montrose, Broughty Ferry, Yellowcraig, Portobello, Eyemouth, Erskine, Largs, Turnberry, Ayr, Irvine).
  - Sampling period: November 2022; beads collected across five days.
  - Beads sorted by polymer (PE or PS); white PE beads analyzed; sites with fewer than 10 beads per polymer excluded.
  - Field metadata captured (e.g., water temperature, salinity, substrate type, weather, beach usage).

- Data collected and structure
  - 12 CSV data files, comprising:
    - FieldObservationsBeaches2023: site-level observations (water temp, salinity, organic matter, substrate, beach users, weather, nurdle counts and colours).
    - NurdleColour2023: counts by colour per site.
    - BacterialConcentrationsOnNurdles2023: CFU counts by species, replicate, material, and nurdle count.
    - BacterialConcentrationsInWater2023: CFU counts in water by species and replicate.
    - BacterialConcentrationsInSand2023: CFU counts in sand by species, replicate, and weight-based measures.
    - SandDryWeight2023: weights before/after drying, with percentage change.
    - VirulenceOfKlebsiellaIsolatesFromPlastics2023: virulence data from Galleria mellonella model.
    - GenomeStatisticsOfKlebsiellaIsolatesFromPlastics2023; CombinedGenomeSamplesOfKlebsiellaFromPlastics2023; VirulenceFinderOfKlebsiellaFromPlastics2023; ResistanceFinderOfKlebsiellaFromPlastics2023; PlasmidFinderOfKlebsiellaFromPlastics2023: genome and pathogenicity/resistance plasmid data.
  - Note: Filenames do not perfectly reflect data periods, but content is correct.

- Laboratory and analytical methods
  - Microbiology: selective media used to enumerate CFUs for multiple pathogens; standard incubation conditions and counting of colonies.
  - Physical/chemical context: salinity, conductivity, turbidity measured with field instruments; FTIR used to identify polymer composition.
  - Molecular biology and bioinformatics:
    - DNA extraction, Nanopore sequencing (Oxford Nanopore MinION) and basecalling; assembly (Flye) and processing (trim, normalize).
    - Genome annotation and quality assessment (CheckM, GTDBtk, SpeciesTree).
    - Species confirmation and downstream analyses (PathogenFinder, VirulenceFinder, ResFinder, PlasmidFinder, VirSorter).
    - Replicate data consolidated to the most complete genome per species for further analysis.
  - Virulence assessment: Galleria mellonella infection model using Klebsiella isolates to compare virulence over 24, 48, and 72 hours; controls included a clinical strain and PBS.

- Data quality, completeness and governance
  - Data checked for anomalies and plausible ranges; missing entries noted as ND.
  - Replicates and selection criteria described to ensure representative genome data.
  - Metadata coverage described in the data dictionaries; explicit data governance processes are not detailed, but data sharing and provenance are addressed through comprehensive documentation and cross-referencing with external tools/databases.

- Accessibility and documentation notes
  - Data are organized into clearly described CSV files with detailed variable descriptions; a note explains the filename period mismatch but confirms content accuracy.
  - Bibliography lists key software and methods used (assembly, taxonomy, virulence/resistance analysis, plasmid detection, and the infection model study cited).

- Implications for monitoring and policy
  - Provides multi-layered environmental health indicators: nurdle-associated bacterial concentrations, presence/level of Klebsiella and virulence/resistance determinants, and genomic context (plasmids, mobile elements).
  - Demonstrates a framework for integrating field microbiology, chemical/polymer characterization, genomics, and in vivo virulence assays to monitor plastic-associated microbial risks.
  - Highlights data management considerations relevant to monitoring frameworks: metadata completeness, data provenance, reproducibility, and governance for open sharing of underlying datasets.