# What has been recorded and what form does the data take?

## What the data represent
- Summary statistics for performance of a genotyping microarray tested on 87 samples of Scots pine (Pinus sylvestris) and closely related Pinus mugo complex members.
- Metrics include conversion rate, mean allelic frequency (MAF), and call rate (CR) for ~50,000 SNPs on a 50K SNP Axiom array.

## When the data were collected
- Assembled during 2016.

## How the data were collected (methods)
- Array contained 49,829 SNPs from multiple sources:
  - 49,052 SNPs from transcriptome sequencing across four pine species: P. sylvestris, P. mugo, P. uncinata, P. uliginosa (including SNPs common to all species and SNPs fixed in one species but polymorphic in others).
  - SNPs filtered by the array manufacturer (Thermo Fisher) based on p-convert scores and guidance on recommended vs non-recommended probes (avoiding SNPs with polymorphisms within 35 bp).
  - 578 additional SNPs from candidate genes (279 total) previously resequenced in population studies.
  - 14 mtDNA-specific SNPs targeting mitochondrial variation.
  - 185 SNPs putatively linked to susceptibility to Dothistroma needle blight (sourced from Pinus radiata; ENA accession ERS1034542-53).
- Summary statistics provided for each locus: polymorphic/monomorphic status, mean allele frequency, and conversion rate, averaged across the 87 genotypes.
- Column headings:
  - SNP_ID: ID
  - ConversionType: Poly or Mono; MAF > 0.1 indicated as N/A, Y, or NA
  - CR: call rate

## Why the data were collected
- For the manufacture of a genotyping array for Scots pine and its close relatives in the Pinus mugo complex.

## Who was responsible for data collection and interpretation
- Stephen Cavers (scav@ceh.ac.uk)

## Completeness
- The document poses questions about data completeness and what data are included or excluded, but the corresponding answers are not provided in the text.