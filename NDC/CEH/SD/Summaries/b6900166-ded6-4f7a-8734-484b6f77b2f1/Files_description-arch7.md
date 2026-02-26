# COMPARATIVE TRANSCRIPTOMICS OF A COMPLEX OF FOUR EUROPEAN PINE SPECIES

- Overview
  - A comparative transcriptomics study across four European pine species, focused on transcriptome data from multiple geographic locations.
  - Reference transcriptome sequence from Scots pine sample Glen Tanar; libraries prepared with TruSeq RNA kit and sequenced on Illumina HiSeq 2000 to generate 100 bp paired-end reads.
  - Raw data include the reference plus 16 samples from four species; data deposited in European Nucleotide Archive (ENA) under accession PRJEB6877.
  - The reference transcriptome contains 40,798 contigs.

- Data files (catalog)
  - Reference_PS2_trinity.fna
    - Reference transcriptome sequence for Scots pine (Glen Tanar, Scotland).
    - Based on Illumina TruSeq library; HiSeq 2000 sequencing; 100 bp paired-end reads.
    - Contains 40,798 contigs.
  - PS1_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Shieldaig, Scotland, relative to the Reference_PS2_trinity.fna.
  - PS2_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Glen Tanar, Scotland, relative to the reference sequence.
  - PS3_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Punkaharju, Finland, relative to the reference sequence.
  - PS4_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Jarocin, Poland, relative to the reference sequence.
  - PS5_SNPs.vcf
    - SNPs detected in Pinus sylvestris from Trevenque, Spain, relative to the reference sequence.
  - M1_SNPs.vcf to M5_SNPs.vcf
    - SNPs detected in Pinus mugo from Romania (Southern Carpathians), Bosnia and Herzegovina (Bjelasnica Mts), Italy (Abruzzi), Austria (Karwendel Mts.), and Poland (Sudety Mts), respectively.
  - UN1_SNPs.vcf to UN4_SNPs.vcf
    - SNPs detected in Pinus uncinata from France (Col de la Croix de Morand), Spain (Pyrenees), Andorra (Eastern Pyrenees), and Spain (Sierra de Gudar), respectively.
  - UG1_SNPs.vcf to UG3_SNPs.vcf
    - SNPs detected in Pinus uliginosa from Poland (Low Silesian Pinewood_Wegliniec), Poland (Wielkie Torfowisko Batorowskie reserve), and Germany (Mittenwald), respectively.

- Data formats and access
  - Reference_PS2_trinity.fna: FASTA transcriptome sequence.
  - SNP files (PS1_SNPs.vcf, PS2_SNPs.vcf, ..., UG3_SNPs.vcf): VCF format containing SNP information per population.
  - Data source: ENA accession PRJEB6877.
  - Scope: reference plus 16 population samples across four pine species, totaling 18 SNP datasets.

- Spatial relevance and GIS considerations
  - Sampling locations are provided in the file descriptions (geographic coverage across Scotland, Finland, Poland, Spain, Romania, Bosnia and Herzegovina, Italy, Austria, France, Andorra, and Germany), enabling geospatial analysis of genomic variation.
  - Note: The files themselves do not include explicit geographic coordinates; coordinates would need to be sourced from sample metadata to map allele distributions.
  - Potential GIS uses:
    - Map SNP distributions by location to visualize geographic patterns of genetic variation.
    - Integrate SNP data with environmental layers to explore genotype-environment associations.
    - Compare spatial genetic structure across species complexes.

- Data quality, provenance, and reproducibility
  - Sequencing platform and library preparation are specified (Illumina HiSeq 2000; TruSeq RNA Sample Preparation Kit).
  - The reference transcriptome comprises 40,798 contigs; 100 bp paired-end reads used for assembly.
  - Described sampling across multiple geographic regions for robust comparative analyses.
  - All data are deposited and accessible via ENA PRJEB6877 for replication and reuse.

- Practical implications for GIS workflows
  - The dataset provides location-based genotype information suitable for creating map-backed visualizations of population structure and SNP diversity.
  - To enable spatial mapping, obtain precise coordinates from sample metadata and convert VCF-derived SNPs into geospatially joinable formats (e.g., allele frequency rasters or point layers per sampling site).
  - Combine with environmental rasters (climate, altitude, vegetation) to investigate geographic drivers of genetic variation.