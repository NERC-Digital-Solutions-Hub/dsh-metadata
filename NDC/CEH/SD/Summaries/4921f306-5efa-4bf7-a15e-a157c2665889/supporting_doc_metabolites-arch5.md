# Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted LC-MS metabolomics dataset from four interacting Streptomyces strains isolated from a Minnesota nature reserve.
- Daily sampling (days 2–6) in triplicate; paired cultures grown adjacently on ISP2 agar; quadruplicates per pairing for five timepoints (n=20 per pairing) to enable metabolite and RNA analyses.
- Metabolites extracted with cold methanol; data acquired in both positive and negative ionisation modes.
- Outputs include mass-to-charge (m/z), retention time, and ion intensity for identified features; relative abundance compared between interacting strain pairs to infer metabolic changes.
- Funded by NERC (NE/T010959/1) and NSF (USA, 1935458).

## Data contents and structure
- File formats: CSV.
- Files:
  - positive_peaks_table.csv: LC-MS data for features detected in positive ionisation mode, with peak IDs, m/z, retention time, and per-sample intensities.
  - negative_peaks_table.csv: LC-MS data for features detected in negative ionisation mode, with the same structure.
  - sample_IDs.csv: mapping of sample_IDs (sXX) to Day, Sampled_strain, Next_to_strain, and Replicate.
- Key columns:
  - peak_ID: arbitrary feature identifier.
  - m/z: mass-to-charge ratio (dimensionless).
  - retention_time: elution time (seconds).
  - sXX: sample column identifiers corresponding to LC-MS runs.
  - sample_ID: mapping identifiers for Day, Strains, and Replicate.
- Sample_IDs.csv fields:
  - Day (sampling day; inoculation is day 0; day 2 = 48 hours post-inoculation).
  - Sampled_strain and Next_to_strain (which strains were sampled and grown alongside).
  - Replicate (_arbitrary replicate number, e.g., 1, 2, 3).

## Experimental design and sampling
- Bacterial culture setup: spores standardized to 1×10^9 CFU/mL in 20% glycerol; diluted to 1×10^8 CFU/mL in ISP2; 4 μL inoculated 1 cm apart in pairs; each pairing prepared in quadruplicate for five timepoints.
- Timepoints: five sampling days (days 2–6), enabling destructive sampling for LC-MS and separate RNA analyses.
- Analysis: LC-MS data collected in triplicate per sample.

## Culturing and metabolite extraction
- ISP2 medium composition and preparation details (yeast extract, malt extract, glucose, optional agar; pH ~7.2).
- Metabolite extraction: rectangular agar plugs containing mycelia and surrounding agar; extraction with precooled methanol; three freeze-thaw cycles; centrifugation; drying; reconstitution and filtration prior to LC-MS.

## Instrumentation and LC-MS method
- LC-MS system: Q Exactive Plus Orbitrap MS coupled to Ultimate 3000 UHPLC.
- Column: Hypersil GOLD C18 (3 μm, 2.1 mm × 100 mm).
- Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
- Gradient: 95% A for 2 min, linear to 95% B over 8 min, hold 2 min, return to 95% A, hold.
- Conditions: column at 40°C; autosampler at 4°C; flow 0.4 mL/min; injection 5 μL.
- Quality controls: blanks at batch start/end; pooled QC samples every 6th injection; randomized sequence.
- Acquisition: full MS (90–1350 m/z); resolution 70,000; AGC target 3e6; max time 200 ms; separate runs for positive and negative modes.

## Data processing and analysis
- Raw data conversion: mzML via ProteoWizard.
- Processing pipeline: mzMatch (Java/R) for noise removal, filtering, peak matching; feature grouping; most intense peak retained for statistics.
- Annotation: putative annotations with Integrated Probabilistic Annotation (IPA).
- Pre-processing steps: drift/batch correction; probabilistic quotient normalization; missing value imputation (k-nearest neighbors); variance stabilization via generalized log (glog).
- Software: pmp Bioconductor R package used for pre-processing and normalization steps.
- Data management: experimental design linked to sample IDs; cross-referenced via sXX in peak tables and sample_IDs.csv.

## Quality control and provenance
- Instrument and method details provided to enable reproducibility (instrument model, column, gradient, MS settings).
- QA measures: blanks, pooled QC samples, randomization; sampling performed in biological triplicate with destructive sampling planned for LC-MS.
- References for software and methods cited (IPA, IPApy2, pmp, mzMatch) to support traceability and reanalysis.

## Data governance and reuse considerations (Data Steward perspective)
- Metadata adequacy: comprehensive sample mapping (Day, Strain, Neighbor, Replicate) and mode-specific peak tables; clear definitions of columns and units.
- Reusability: CSV format, explicit file naming, and cross-references between peak data and sample metadata facilitate reuse; full methodological details enable replication and validation.
- Provenance: instrument parameters, extraction, and LC-MS workflow are documented; data processing steps and software versions are specified.
- Limitations: putative annotations (IPA) may require experimental confirmation; some identifications remain putative; licensing and repository location are not specified in the text.
- Governance recommendations: consider attaching a dataset DOI and license; maintain versioning; publish accompanying metadata schema (e.g., an ISA-like descriptor) to enhance interoperability and discoverability; ensure explicit data sharing terms and update mechanisms if future data are added.