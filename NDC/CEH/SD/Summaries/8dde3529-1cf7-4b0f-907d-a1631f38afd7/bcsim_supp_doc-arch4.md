# Genotyping of Drosophila backcross progeny for mate-choice loci using multiplexed shotgun genotyping

- Purpose and scope
  - Identify loci contributing to discrimination between male-related species (D. simulans vs D. sechellia) by genotyping female progeny from a D. simulans backcross (F2) in a two-choice mate assay.
  - Use a combination of phenotypic mate-choice data and genome-wide genotypes to map signals of divergence.

- Experimental design and data collection
  - Subjects and crossing scheme
    - Female progeny from a D. simulans backcross (F2 from F1 backcross to D. simulans).
  - Mate-choice assay
    - Test setup: three test females and three males of either species per vial, all aged within defined windows.
    - Observations: monitor for four hours or until copulation; after first mating, freeze the vial for later genotype determination of the mating male by species-specific genitalia.
  - Illumina data generation
    - Standard molecular biology protocols to prepare sequencing libraries (per Andolfatto et al., 2011).
    - ID column includes library ID with a unique barcode; pheno column encodes mating outcome (0 = mated with D. simulans; 1 = mated with D. sechellia).
  - Genomic data referenced
    - Target loci correspond to locations in the D. simulans genome as defined by Hu et al. (Genome Res. 2013).

- Data provenance and parental references
  - Parental genomes
    - D. simulans A2A2B (Tsimbazaza-derived)
    - D. sechellia D1A1C (13-derived)
  - Genotyping method
    - Multiplexed Shotgun Genotyping (Andolfatto et al., 2011)
  - Data thinning and processing
    - Thinning performed with pull_thin script (David Stern’s GitHub: pull_thin).

- Data fields and coding
  - ID: library name with unique barcode
  - pheno: 0 = female mated with D. simulans; 1 = female mated with D. sechellia
  - Genomic locations: specific sites in the D. simulans genome (Hu et al., 2013)
  - Allele coding
    - BB = sim/sim alleles
    - BA = sech/sim
    - NA = data not available

- Data quality and filtering
  - Issue: low DNA content caused incomplete/poor genotype calls
  - Quality control: remove genotyped individuals with more than 25% NA (ambiguous calls)

- Data management and stewardship
  - Metadata and traceability
    - Clear separation of libraries by ID and barcode; phenotype linkage via pheno.
    - Documentation ties to parental genomes and reference coordinates (Hu et al.).
  - Data standards and discoverability
    - Uses established references and a reproducible thinning script; maintains explicit allele codes and NA handling.
  - Reproducibility and collaboration
    - References and scripts cited/payment: Andolfatto 2011; Hu et al. 2013; pull_thin on GitHub.
  - Potential for reuse
    - Data suitable for rapid genetic mapping of mate-choice loci and for cross-study comparisons using standardized genotyping frameworks.

- References
  - Andolfatto et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping (Genome Res. 2011)
  - Hu et al. A second-generation assembly of the Drosophila simulans genome (Genome Res. 2013)
  - pull_thin script (David Stern, Janelia Farm) https://github.com/dstern/pull_thin