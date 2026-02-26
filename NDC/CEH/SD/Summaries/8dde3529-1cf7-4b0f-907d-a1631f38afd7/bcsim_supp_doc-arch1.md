# To identify loci that contribute to discrimination between males of related species

- Goal
  - Identify genomic loci contributing to discrimination between males of D. simulans and D. sechellia by genotyping female progeny from a D. simulans backcross in a two-choice mate selection assay.
  - Phenotype recorded as 0 (females mated with D. simulans males) or 1 (females mated with D. sechellia males).

- Experimental design
  - Subjects: female progeny from a D. simulans backcross (F2 from an F1 backcross to D. simulans); test with three females and three males of either species per vial.
  - Age and housing: adults sexed at eclosion; groups of three same-sex individuals; no yeast in vials.
  - Testing window: four hours or until copulation, whichever comes first.
  - Outcome: after first mating, vial frozen; species of copulating male determined by distinguishing male genitalia.

- Genotyping and sequencing
  - Library preparation: standard molecular biology methods to generate Illumina libraries.
  - Genotyping method: Multiplexed Shotgun Genotyping (Andolfatto et al., 2011).
  - Data format: ID column (library ID + unique barcode); pheno column (0 or 1 as above); remaining columns correspond to specific genomic loci (Hu et al., 2013).

- Parental genomes and references
  - D. simulans parental genome: A2A2B (from Tsimbazaza strain).
  - D. sechellia parental genome: D1A1C (from D. sechellia 13 strain).

- Data processing and quality control
  - Genotypes obtained and thinned with David Stern’s pull_thin script.
  - Filtering: remove individuals with more than 25% ambiguous calls (NA).

- Data coding notes
  - BB = sim/sim alleles
  - BA = sech/sim alleles
  - NA = data not available

- References
  - Andolfatto et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011.
  - Hu et al. A second-generation assembly of the Drosophila simulans genome. Genome Res. 2013.