# Genotypes for samples used to validate a 50K single nucleotide polymorphism (SNP, DNA mutation) Axiom array for Scots pine (Pinus sylvestris) and closely related members of the Pinus mugo complex

- What is recorded: Genotypes for samples used to validate a 50K SNP Axiom array for Scots pine and closely related Pinus mugo complex species.
- Data collection timeframe: 2016.
- How data were collected:
  - Samples and DNA extraction from needles using a Qiagen DNeasy 96 kit; needles dried on silica gel before extraction.
  - DNA quantified with a Qubit spectrophotometer to ensure a minimum concentration of 35 ng/µl; quality checked visually for fragmentation on 1% agarose gel.
  - Genotyping performed at Edinburgh Genomics following the Affymetrix Axiom assay protocol in a 384-well format on a GeneTitan.
  - Genotype calls produced with Axiom Analysis Suite; grouping based on call rate (CR) and dish QC (DQC) with thresholds:
    - DQC high ≥ 0.82; CR high ≥ 96
    - DQC high; CR low
    - DQC low; CR low
  - Analyses 1 (DQC high + CR high), 2 (DQC high + CR low), 3 (DQC low + CR low).
- Data processing and quality control:
  - High-quality samples (N=529) used to set thresholds for allele calls.
  - Posteriors for allele calls used as priors for analyses 2 (N=753) and 3 (N=251).
- Purpose: Validation of a newly manufactured genotyping array for Scots pine and its close relatives in the Pinus mugo complex.
- Responsible for data collection and interpretation: Stephen Cavers (scav@ceh.ac.uk).
- Completeness: Not provided in the document (the section is present but no explicit answer about data completeness or which data are included/excluded and why).