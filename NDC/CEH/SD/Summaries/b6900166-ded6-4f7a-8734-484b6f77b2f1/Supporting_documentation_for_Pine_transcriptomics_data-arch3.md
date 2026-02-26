# Plant material and RNA extraction

- Sampling and material
  - Needles collected from four pine species: Pinus sylvestris, P. mugo, P. uncinata, and P. uliginosa.
  - Seedlings were two years old, grown in a glasshouse at the Centre for Ecology and Hydrology, Edinburgh, UK.
  - Seeds originated from 17 populations across Europe (five for P. sylvestris, five for P. mugo, four for P. uncinata, three for P. uliginosa) spanning environmental gradients.
  - Immediately after sampling, needles were frozen in liquid nitrogen and homogenized.

- RNA extraction and quality control
  - Total RNA extracted from 100 mg of needle powder using Spectrum™ Plant Total RNA Kit (Sigma).
  - RNA concentration and quality assessed with Qubit® Fluorometer.
  - 10 μg of input RNA used for normalized cDNA library preparation.

- cDNA library construction and sequencing
  - Template cDNA libraries prepared with TruSeq™ RNA Sample Preparation Kit (Illumina).
  - Poly-A mRNA purified in two steps using poly-T oligo-attached magnetic beads.
  - RNA fragmented to 120–210 bp inserts; first and second strand cDNA synthesis performed; RNase H treatment applied.
  - ds cDNA underwent end-repair, 3' adenylation, and Illumina paired-end adapter ligation.
  - PCR enrichment conducted to amplify libraries.
  - Normalization performed to enhance low-expression transcripts.
  - Quality control by Agilent 2100 Bioanalyzer; sequencing on Illumina HiSeq 2000.
  - Generated 100 bp paired-end reads for all samples, including Scots pine reference sample (2_GT_31, Scotland, Glen Tanar).

- Reference transcriptome assembly
  - Raw reads for reference sample 2_GT_31 filtered to remove adapters, contaminants, and poor-quality/ambiguous sequences.
  - De novo assembly performed with Trinity (v2012-06-08).
  - Final reference transcriptome consisting of 40,798 contigs.

- Alignment, SNP calling and filtering
  - A set of 40,798 transcripts used as reference to map reads from the remaining 16 samples.
  - Alignment performed with BWA (v0.6.1); duplicates marked with Picard.
  - Local realignment with GATK to minimize indel misalignment.
  - SNPs called for each sample and species relative to the reference using Samtools (samtools-0.1.18).