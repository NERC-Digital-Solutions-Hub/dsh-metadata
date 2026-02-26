# COMPARATIVE TRANSCRIPTOMICS OF A COMPLEX OF FOUR EUROPEAN PINE SPECIES

- Overview
  - Study of transcriptomic variation across four European pine species using a reference transcriptome and SNP analyses.
  - Reference transcriptome derived from Scots pine sample Glen Tanar (Scotland), assembled as Reference_PS2_trinity.fna.
  - Sequencing details: 100 base paired-end reads generated on Illumina HiSeq 2000; TruSeq RNA sample preparation; data used as reference for cross-species comparisons.
  - Raw data include the reference plus 16 additional samples from four species; raw data deposited in ENA under accession PRJEB6877.
  - Reference transcript sequence comprises 40,798 contigs.

- Data assets (files described)
  - 1) Reference_PS2_trinity.fna
    - Reference transcriptome sequence for Scots pine (Glen Tanar, Scotland).
  - 2) PS1_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Shieldaig, Scotland relative to the reference.
  - 3) PS2_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Glen Tanar, Scotland relative to the reference.
  - 4) PS3_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Punkaharju, Finland relative to the reference.
  - 5) PS4_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Jarocin, Poland relative to the reference.
  - 6) PS5_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Trevenque, Spain relative to the reference.
  - 7) M1_SNPs.vcf
    - SNPs detected in Pinus mugo from Southern Carpathians, Romania relative to the reference.
  - 8) M2_SNPs.vcf
    - SNPs detected in Pinus mugo from Bjelasnica Mountains, Bosnia and Herzegovina relative to the reference.
  - 9) M3_SNPs.vcf
    - SNPs detected in Pinus mugo from Abruzzi, Italy relative to the reference.
  - 10) M4_SNPs.vcf
    - SNPs detected in Pinus mugo from Karwendel Mountains, Austria relative to the reference.
  - 11) M5_SNPs.vcf
    - SNPs detected in Pinus mugo from Sudety Mountains, Poland relative to the reference.
  - 12) UN1_SNPs.vcf
    - SNPs detected in Pinus uncinata from Col de la Croix de Morand, France relative to the reference.
  - 13) UN2_SNPs.vcf
    - SNPs detected in Pinus uncinata from Pyrenees, Spain relative to the reference.
  - 14) UN3_SNPs.vcf
    - SNPs detected in Pinus uncinata from Andorra, Eastern Pyrenees relative to the reference.
  - 15) UN4_SNPs.vcf
    - SNPs detected in Pinus uncinata from Sierra de Gudar, Spain relative to the reference.
  - 16) UG1_SNPs.vcf
    - SNPs detected in Pinus uliginosa from Wegliniec, Poland relative to the reference.
  - 17) UG2_SNPs.vcf
    - SNPs detected in Pinus uliginosa from Wielkie Torfowisko Batorowskie reserve, Poland relative to the reference.
  - 18) UG3_SNPs.vcf
    - SNPs detected in Pinus uliginosa from Mittenwald, Germany relative to the reference.

- Data provenance and access
  - All raw sequencing data (reference plus 16 samples across four species) are deposited in the European Nucleotide Archive (ENA).
  - ENA accession: PRJEB6877.
  - The reference transcriptome contains 40,798 contigs.

- Data structure, formats, and interpretation
  - Reference_PS2_trinity.fna: assembled reference transcriptome in FASTA format.
  - Each PS*/SNPs.vcf file: variant call format (VCF) containing SNPs detected in the corresponding population/species relative to the reference transcriptome.
  - Data enable cross-species SNP comparisons, population-level variation analyses, and association of SNPs with transcript contigs.

- Suggested data uses and potential products
  - SNP matrices for population structure and diversity analyses across pine species and geographic locations.
  - Comparative transcriptomics investigations to link SNPs to expressed transcripts.
  - Data-derived dashboards or self-serve reports for researchers and stakeholders interested in pine genetics and adaptation.
  - Reuse in broader studies of conifer transcriptomics, SNP annotation, and functional interpretation.

- Considerations for data users
  - Data are focused on SNPs relative to a Scots pine reference transcriptome; cross-species interpretation should consider reference bias.
  - Sample distribution spans multiple populations per species, enabling broad geographic comparisons but with varying sample sizes.
  - Functional interpretation may require additional annotation and transcript-level context beyond SNP calls.