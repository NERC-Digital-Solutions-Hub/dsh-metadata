# Plant material and RNA extraction

- Study design and sample provenance
  - Needles collected from two-year-old pine seedlings grown in a glasshouse at the Centre for Ecology and Hydrology, Edinburgh.
  - Seeds sourced from 17 populations across Europe: 5 P. sylvestris, 5 P. mugo, 4 P. uncinata, 3 P. uliginosa.
  - Scotland reference sample 2_GT_31 (Glen Tanar) used for sequencing reference.

- RNA extraction and quality control
  - Needle tissue frozen in liquid nitrogen and homogenized.
  - Total RNA extracted from 100 mg of needle powder using Spectrum Plant Total RNA Kit.
  - RNA concentration/quality assessed with Qubit; 10 μg input RNA per sample for library preparation.

- cDNA library construction and sequencing
  - Poly-A mRNA purified from total RNA using poly-T magnetic beads.
  - RNA fragmentation to 120–210 bp, first and second strand cDNA synthesis, adaptor ligation, and PCR enrichment.
  - Normalization performed to enrich for low-expression transcripts.
  - Quality control with Agilent 2100 Bioanalyzer (DNA1000 chip).
  - Libraries sequenced on Illumina HiSeq 2000 to generate 100 bp paired-end reads; Scots pine 2_GT_31 used as reference.

- Reference transcriptome assembly
  - Raw reads filtered to remove adapters, contaminants, and low-quality sequences (N-containing).
  - De novo assembly with Trinity (v r2012-06-08) to produce 40,798 contigs.

- Alignment, SNP calling and filtering
  - Reference comprises 40,798 transcripts; reads from 16 samples aligned to this reference.
  - Alignment performed with BWA (v0.6.1); duplicates marked with Picard.
  - Local realignment with GATK to minimize indel misalignment errors.
  - SNPs called for each sample/species against the reference using Samtools (v0.1.18).

- Data products and metadata implications for stewardship
  - Outputs include the reference transcriptome (40,798 contigs) and per-sample SNP data.
  - Key metadata to capture: sample IDs, species, population origin, reference sample details, sequencing platform and chemistry, software versions and parameters, and QC results.
  - Data formats to preserve for sharing and reuse: FASTA/contigs, FASTQ reads, VCF for SNPs, and associated QC reports.
  - Documentation of normalization, filtering, and realignment steps to support reproducibility and interoperability across systems.