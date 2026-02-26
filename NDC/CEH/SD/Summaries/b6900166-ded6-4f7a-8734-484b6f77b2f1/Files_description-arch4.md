# COMPARATIVE TRANSCRIPTOMICS OF A COMPLEX OF FOUR EUROPEAN PINE SPECIES

- This manuscript describes a multi-species transcriptomic data package focused on four European pine species, with both a reference transcriptome and numerous SNP datasets across populations and regions.

## Data assets

- Reference transcriptome
  - Reference_PS2_trinity.fna: Transcriptome sequence from Scots pine (Glen Tanar, Scotland). Library prepared with TruSeq RNA kit; sequencing on Illumina HiSeq 2000 to generate 100 base paired-end reads.
  - Contains 40,798 contigs.
  - Raw data for the reference and 16 additional samples (across four species) deposited in European Nucleotide Archive (ENA): PRJEB6877.
- SNP datasets (VCF files)
  - PS1_SNPs.vcf: SNPs in Pinus sylvestris from Shieldaig, Scotland, vs reference.
  - PS2_SNPs.vcf: SNPs in Pinus sylvestris from Glen Tanar, Scotland, vs reference.
  - PS3_SNPs.vcf: SNPs in Pinus sylvestris from Punkaharju, Finland, vs reference.
  - PS4_SNPs.vcf: SNPs in Pinus sylvestris from Jarocin, Poland, vs reference.
  - PS5_SNPs.vcf: SNPs in Pinus sylvestris from Trevenque, Spain, vs reference.
  - M1_SNPs.vcf to M5_SNPs.vcf: SNPs in Pinus mugo from Romania, Bosnia and Herzegovina, Italy, Austria, Poland respectively, vs reference.
  - UN1_SNPs.vcf to UN4_SNPs.vcf: SNPs in Pinus uncinata from France, Spain, Andorra, Spain respectively, vs reference.
  - UG1_SNPs.vcf to UG3_SNPs.vcf: SNPs in Pinus uliginosa from Poland, Poland, Germany respectively, vs reference.

## Access, provenance, and data formats

- Sequencing and library details
  - Illumina HiSeq 2000 platform; 100 bp paired-end reads; template cDNA library prepared with TruSeq RNA kit.
- Data provenance and scope
  - Reference plus 16 samples across four pine species (totaling 18 SNP datasets described).
- Availability and discoverability
  - Raw data and reference transcriptome are deposited in ENA under accession PRJEB6877.
- Data formats
  - Reference: FASTA (Reference_PS2_trinity.fna).
  - SNPs: VCF files (PS1_SNPs.vcf, PS2_SNPs.vcf, PS3_SNPs.vcf, PS4_SNPs.vcf, PS5_SNPs.vcf, M1–M5_SNPs.vcf, UN1–UN4_SNPs.vcf, UG1–UG3_SNPs.vcf).

## Data products and structure

- A single reference transcriptome served as the baseline for cross-population SNP calling.
- A comprehensive set of SNP datasets (18 VCF files) enabling comparative population genomics and cross-species analyses across geographic regions and species.

## Implications for data leadership and governance

- Data management demonstrates clear asset tracking (reference plus multiple SNP datasets) and explicit data access through ENA, supporting discoverability and reuse.
- Metadata is embedded in the file descriptions (sample origins, species, location), aiding context for data consumers and future integration efforts.
- The collection highlights the importance of standardized data products (reference sequence, harmonized SNP calls) to enable cross-study comparisons within a broader pine genomics community.

## Use cases and potential value

- Comparative genomics across four European pine species and their diverse geographic populations.
- Population genetics research leveraging SNP variation relative to a common reference.
- Cross-species analyses that may inform evolutionary studies or adaptation research in conifer species.

## Key considerations and challenges

- The dataset is distributed across many geographic regions and species, underscoring the need for consistent metadata and documentation to support interoperability.
- While raw data accessibility is provided via ENA, users will rely on the accompanying SNP VCFs and the reference transcriptome for analyses, emphasizing the importance of clear versioning and provenance.