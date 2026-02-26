# Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted metabolomics dataset from paired cultures of four interacting Streptomyces strains isolated from a Minnesota nature reserve.
- Daily sampling (days 2–6) in triplicate across paired cultures; four strains grown in adjacent pairs on ISP2 agar.
- Metabolites extracted with cold methanol; LC-MS data collected in positive and negative ionisation modes.
- Objective: compare relative abundance of detected features between strain pairs to understand metabolic changes during interaction.

## Data files and structure
- positive_peaks_table.csv: LC-MS data for features detected in positive ionisation mode; includes peak_ID, m/z, retention_time, and per-sample ion counts.
- negative_peaks_table.csv: LC-MS data for features detected in negative ionisation mode; same structure as positive table.
- sample_IDs.csv: metadata linking sample_IDs (sXX) to Day, Sampled_strain (A–D or '-' for controls), Next_to_strain (A–D or '-' for controls), and Replicate.
- Column descriptions define feature identifiers, mass-to-charge ratios (m/z), retention times (seconds), and sample-specific counts.
- The dataset is organized to enable cross-reference between LC-MS features and experimental conditions.

## Experimental design and sample metadata
- Four Streptomyces strains interacting in pairs; five timepoints (days 2–6) with inoculation defined as day 0.
- n = 20 biological replicates per pairing to support destructive daily sampling for mass spectrometry.
- LC-MS analysis performed in triplicate for each sample timepoint.
- Sampling and analysis performed with randomization and quality controls to support robust downstream analysis.

## Culturing and sample preparation methods
- Spores standardized and aliquoted at 1 x 10^9 CFU/mL in 20% glycerol; diluted 10-fold to 1 x 10^8 CFU/mL in ISP2 broth.
- 4 µL inoculated 1 cm apart in pairs on ISP2 agar; each pairing prepared in quadruplicate for each timepoint (n = 20 per pairing).
- ISP2 medium composition: yeast extract, malt extract, glucose, agar (optional); pH 7.2; autoclaved.

## Metabolite extraction
- Metabolites extracted from rectangular agar plugs (1 x 0.5 cm) including mycelia and surrounding agar.
- Extraction with 1 mL cold methanol (-48 °C), three freeze-thaw cycles, centrifugation, and drying of the supernatant.
- Reconstitution in 200 µL 20% methanol, sonication, filtration prior to injection.

## LC-MS data acquisition
- Instrumentation: Q Exactive Plus coupled to Ultimate 3000 UHPLC with Hypersil GOLD C18 column.
- Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
- Gradient: 95% A initial, ramp to 95% B, hold, return to 95% A; flow 0.4 mL/min; injection volume 5 µL.
- Run controls: blank injections at start/end; pooled QC every 6th injection; randomized sequence.
- Data acquisition: full MS mode, 90–1350 m/z, resolution 70,000; positive and negative mode analyzed separately.

## Data processing and analysis
- Raw data converted to mzML using ProteoWizard.
- Processing with mzMatch: noise removal, signal filtering, peak matching; grouping of features by molecule likelihood; only the most intense peak used for statistics.
- Putative annotation via Integrated Probabilistic Annotation (IPA).
- Pre-processing steps: signal drift and batch effect correction, probabilistic quotient normalization, missing value imputation (k-nearest neighbors), and variance stabilization (generalised logarithm, glog) using the pmp Bioconductor package.
- Experimental design integrated into analysis through cross-sample linkage with sample_IDs.csv and triplicate LC-MS runs.

## Quality control and reproducibility
- Blank injections to monitor carryover; pooled QC samples every 6 injections to assess analytical drift.
- Randomized sample sequence; analysis performed in biological triplicate.
- Use of open-source, well-documented pipelines (mzMatch, IPA, pmp) enhances transparency and reproducibility.

## Accessibility and reuse
- Data structured in standard CSV formats with explicit metadata to enable re-use and cross-study comparisons.
- Clear documentation of experimental conditions, sample mapping, and analysis workflow supports integration with other environmental datasets.
- The analytical workflow emphasizes reproducibility and data quality, aligning with environmental monitoring principles to track metabolic changes in microbial communities.

## Funding and references
- Funded by NERC (NE/T010959/1) and the National Science Foundation (USA, 1935458).
- References for IPA, ipaPy2, mzMatch, and related preprocessing tools provided to support reproducibility and annotation confidence.