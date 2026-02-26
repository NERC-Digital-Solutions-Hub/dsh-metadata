# Genotypes for samples used to validate a 50K single nucleotide polymorphism (SNP, DNA mutation) Axiom array for Scots pine (Pinus sylvestris) and closely related members of the Pinus mugo complex

## What the data are and their form
- Genotypes for samples used to validate a 50K SNP Axiom array for Scots pine and related Pinus mugo complex species.

## When the data were collected
- Assembled during 2016.

## How the data were collected (methods and instrumentation)
- Samples and DNA extraction:
  - Subset of 87 samples across four pine species: Pinus sylvestris (SY), P. mugo (MU), P. uncinata (UN), P. uliginosa (UL).
  - DNA extraction from needles using Qiagen DNeasy 96 kit; needles dried on silica gel prior to extraction.
  - DNA quantified with a Qubit; targeted minimum concentration of 35 ng/µl.
  - DNA quality checked visually for fragmentation on 1% agarose gel.
- Genotyping and SNP calling:
  - Genotyping conducted at Edinburgh Genomics using Affymetrix Axiom assay protocol.
  - 384-well format on a GeneTitan; genotype calls via Axiom Analysis Suite.
  - Samples assigned to analysis groups based on call rate (CR) and dish QC (DQC) thresholds:
    - DQC high ≥ 0.82; DQC low < 0.82
    - CR high ≥ 96; CR low < 96
  - Analyses:
    1) DQC high + CR high
    2) DQC high + CR low
    3) DQC low + CR low
  - High-quality samples (N=529) used to set thresholds for allele calls.
  - Posteriors for allele calls used as priors for analyses 2 (N=753) and 3 (N=251).

## Why the data were collected (purpose)
- For validation of a newly manufactured genotyping array for Scots pine and its close relatives in the Pinus mugo complex.

## Who was responsible for the collection and interpretation of the data
- Stephen Cavers (scav@ceh.ac.uk).

## Completeness
- The document’s completeness section (item 6) is not filled in, so explicit details on data completeness, inclusions, and exclusions beyond the reported sample counts and analysis groups are not provided.
- Key governance notes for data stewardship:
  - Include explicit completeness statements (which samples/data are included in final analyses vs. excluded, raw vs. processed data).
  - Capture data provenance, processing steps, and versioning of genotype calls and priors.
  - Align metadata with dataset standards (methods, thresholds, sample origins, species identifiers) to facilitate discoverability and reuse.