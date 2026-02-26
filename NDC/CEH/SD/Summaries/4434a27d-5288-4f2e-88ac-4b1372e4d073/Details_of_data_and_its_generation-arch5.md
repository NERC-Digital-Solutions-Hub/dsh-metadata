# Details of data and its generation

- Purpose and scope
  - Describes the data generation and sequencing processes used in an experimental evolution study of Drosophila C virus (DCV) across 19 Drosophilidae host species.
  - Aims to enable reader understanding and reuse of the data, in line with the accompanying paper’s findings on parallel evolution and host–virus dynamics.

- Data generated
  - Virus production and cloning to minimise genetic variation; TCID50 measurements for DCV stock.
  - Experimental evolution: DCV passaged through 19 host species, with approximately 10 replicates per species (D. montana had 8 passages due to stock issues); about 100–200 generations estimated.
  - Sequencing data from evolved viral lineages:
    - cDNA synthesis and genome amplification covering ~97% of the genome (62–9050 bp of the reference genome).
    - 173 pooled amplicon libraries sequenced on Illumina MiSeq (600 cycles, 300 bp paired-end).
  - Host phylogeny data:
    - An ultrametric time-based phylogeny for the 19 host species inferred with BEAST and pruned to the study set.
  - Derived data products:
    - Derived allele frequencies for biallelic and triallelic sites per lineage.
    - First and second derived allele frequencies for triallelic sites.
    - Summary statistics and figures reproducing in the accompanying analyses.

- Data processing workflow
  - Quality control and pre-processing
    - FastQC for read quality assessment and primer contamination check.
    - Trimmomatic for quality trimming and adapter removal with specified parameters (MINLEN=30, TRAILING=15, SLIDINGWINDOW=4:20, ILLUMINACLIP settings).
  - Reference and alignment
    - Amplification and sequencing of an ancestral DCV reference sequence.
    - Reads aligned to reference using BWA-MEM with -M flag; high mapping quality observed (99.5% with phred > 60).
    - BAMs processed with SAMtools and PICARD to add read group information.
  - Variant discovery
    - Variant calling with GATK UnifiedGenotyper, ploidy set to 100 to detect low-frequency variants.
    - Filtering threshold: SNPs included if frequency > 0.05 in any lineage; tri-allelic sites retained with all three alleles.
  - Data accessibility and reproducibility
    - Supporting data and analysis scripts published to enable replication of figures and statistics.

- Data types and files available
  - Raw and processed data
    - FASTQ reads from 173 Illumina libraries (illuminated via the MiSeq platform).
    - BAM files for mapped reads with read-group metadata.
    - Ancestral DCV reference sequence and PCR-amplified genomes.
  - Derived data and metadata
    - Derived allele frequencies for biallelic and triallelic sites.
    - First and second derived allele frequencies for triallelic sites.
    - Host phylogeny file (time-calibrated tree for the 19 species).
    - Permutation test results and FST calculations for parallel evolution analyses.
  - Code and documentation
    - R scripts to reproduce all figures and statistics from the paper.
    - Supplementary materials detailing primers, PCR conditions, and table S2 primer sets.

- Data access and availability
  - Sequence data
    - FASTQ data available in NCBI SRA (Accession: SRP119720).
  - Processed data, phylogeny, derived frequencies, and analysis scripts
    - Hosted in the NERC data repository, including:
      - BAM files
      - Phylogeny file
      - Derived allele frequencies (biallelic and triallelic)
      - First and second derived allele frequencies for triallelic sites
      - R scripts to reproduce figures and statistics
  - Documentation and methods
    - Detailed methodology and references provided to support reproducibility and understanding of the analysis pipeline.

- Data quality, provenance, and limitations
  - Quality control and mapping
    - High-quality data with the majority of reads showing strong mapping quality (phred > 60 for 99.5% of reads).
  - Genome coverage
    - ~97% genome coverage across the amplified regions; not the full genome.
  - Sample and experimental design nuances
    - 19 host species with multiple replicates; one species (D. montana) had fewer passages due to stock issues.
    - 3-day infection window chosen based on viral load dynamics.
  - Statistical considerations
    - Ancestral SNP frequencies observed in controls; frequency threshold >0.05 used to identify SNPs in analyses.
    - Triallelic sites retained and analyzed with all three alleles.
  - Reproducibility and transparency
    - Data and scripts are provided to reproduce all figures and statistics from the study.

- Governance and stewardship implications for reuse
  - Clear data lineage and processing steps enable traceability from raw reads to derived allele frequencies and statistics.
  - Standardized formats (FASTQ, BAM, VCF-like allele frequencies, phylogeny files) support interoperability with other datasets and pipelines.
  Conceptual alignment with data stewardship principles:
  - Documentation of data generation, processing, and analytical steps is explicit to support reuse by data creators/sharers and data users.
  - Availability of both raw and derived data, along with reproducible scripts, facilitates verification and integration with broader datasets.
  - Metadata accompanying the datasets should capture experimental design (host species, passages, replicates), sequencing parameters, and analysis parameters to support discoverability and appropriate use.