# COMPARATIVE TRANSCRIPTOMICS OF A COMPLEX OF FOUR EUROPEAN PINE SPECIES

## Overview
- Describes datasets and file descriptions accompanying the manuscript on comparative transcriptomics across four Pinus species.
- Key data products include a reference transcriptome and multiple SNP (VCF) datasets derived from different geographic samples.
- Raw sequencing data are deposited in ENA, enabling reproducibility and reuse.

## Datasets and Files

- Reference dataset
  - Reference_PS2_trinity.fna: reference transcriptome sequence for Scots pine (Glen Tanar, Scotland).
  - Library preparation: TruSeq RNA Sample Preparation Kit; sequencing on Illumina HiSeq 2000.
  - Read length: 100 base paired-end reads.
  - Sample: 2_GT_31, Scotland (Glen Tanar) as reference.
  - Assembly: 40,798 contigs.
  - Data availability: Raw data for all transcriptome samples (reference + 16 samples across four species) deposited in European Nucleotide Archive (ENA), PRJEB6877.

- Sample and species composition (16 samples across four Pinus species)
  - Pinus sylvestris (Scotland): 4 samples
  - Pinus mugo: 5 samples
  - Pinus uncinata: 4 samples
  - Pinus uliginosa: 3 samples

- SNP datasets (VCF files) relative to the reference
  - PS1_SNPs.vcf: SNPs in P. sylvestris from Shieldaig vs Reference_PS2_trinity.fna
  - PS2_SNPs.vcf: SNPs in P. sylvestris from Glen Tanar vs Reference_PS2_trinity.fna
  - PS3_SNPs.vcf: SNPs in P. sylvestris from Punkaharju, Finland vs reference
  - PS4_SNPs.vcf: SNPs in P. sylvestris from Jarocin, Poland vs reference
  - PS5_SNPs.vcf: SNPs in P. sylvestris from Trevenque, Spain vs reference
  - M1_SNPs.vcf: SNPs in P. mugo from Southern Carpathians, Romania vs reference
  - M2_SNPs.vcf: SNPs in P. mugo from Bjelasnica Mountains, Bosnia and Herzegovina vs reference
  - M3_SNPs.vcf: SNPs in P. mugo from Abruzzi, Italy vs reference
  - M4_SNPs.vcf: SNPs in P. mugo from Karwendel Mountains, Austria vs reference
  - M5_SNPs.vcf: SNPs in P. mugo from Sudety Mountains, Poland vs reference
  - UN1_SNPs.vcf: SNPs in P. uncinata from Col de la Croix de Morand, France vs reference
  - UN2_SNPs.vcf: SNPs in P. uncinata from Pyrenees, Spain vs reference
  - UN3_SNPs.vcf: SNPs in P. uncinata from Andorra, Eastern Pyrenees vs reference
  - UN4_SNPs.vcf: SNPs in P. uncinata from Sierra de Gudar, Spain vs reference
  - UG1_SNPs.vcf: SNPs in P. uliginosa from Wegliniec, Poland vs reference
  - UG2_SNPs.vcf: SNPs in P. uliginosa from Wielkie Torfowisko reserve, Poland vs reference
  - UG3_SNPs.vcf: SNPs in P. uliginosa from Mittenwald, Germany vs reference

- Access and provenance
  - ENA accession for raw transcriptome data: PRJEB6877
  - All SNP and reference data are described as being compared to the Reference_PS2_trinity.fna, establishing a consistent baseline for variation across species and locations.

## Data Governance and Stewardship Considerations

- Metadata and provenance
  - Ensure consistent metadata for each SNP file: species, population/location, country, sample identifiers, and reference baseline.
  - Link SNP datasets to the corresponding sample descriptions and geography to support reproducibility and downstream analyses.

- Data formats and standards
  - Primary formats include FASTA (reference transcriptome) and VCF (SNP calls).
  - Maintain clear versioning of the reference (Reference_PS2_trinity.fna) and associated SNP datasets.

- Data access, sharing, and updates
  - Data are deposited in ENA (PRJEB6877); track any updates or reprocessing to ensure alignment with the reference and SNP calls.
  - If new samples or re-analyses are added, provide updated VCFs and reference sequences with clear version identifiers.

- Compliance and usage
  - Ensure proper acknowledgment of the ENA dataset and the study authors when reused.
  - Document any usage restrictions or licensing terms associated with the data.

## Usage Considerations for Data Stewards

- Cross-dataset interoperability
  - The SNP datasets are all anchored to a single reference transcriptome; future integrations should maintain this baseline or provide a clear mapping when a new reference is introduced.

- Quality and completeness
  - Report any known limitations (e.g., sample representation per species, geographic coverage) to users.
  - Consider enabling metadata-driven filtering (by country, species, population) to support targeted reuse.

- Documentation and discoverability
  - Ensure dataset descriptions (as provided) are captured in data catalogs with consistent fields (project, organisms, tissue type if known, sequencing platform, read length, contigs, accession numbers).
  - Provide a concise data dictionary for the SNP VCF files to aid users in interpretation of sample identifiers and reference comparisons.