# Working Title Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted LC-MS metabolomics dataset from paired cultures of four interacting Streptomyces strains isolated in Minnesota, USA.
- Daily samples collected from day 2 to day 6 in triplicate; 20 biological replicates per pairing to enable destructively sampled timepoints.
- Data capture includes mass-to-charge (m/z), retention time, and ion intensity per feature, with analysis across strain-pair interactions to infer metabolic changes.
- Funded by NERC (NE/T010959/1) and the National Science Foundation (USA, 1935458).

## Data content and structure
- Files:
  - positive_peaks_table.csv: features detected in positive ionisation mode with intensities.
  - negative_peaks_table.csv: features detected in negative ionisation mode with intensities.
  - sample_IDs.csv: mapping of sample IDs to day, sampled strain, neighbor strain, and replicate.
- Key columns:
  - peak_ID: feature identifier; m/z: mass-to-charge ratio; retention_time: elution time (seconds); sXX: LC-MS run identifiers.
  - sample_ID: identifier for each LC-MS run; Day (in days from inoculation); Sampled_strain; Next_to_strain; Replicate.
- The dataset supports comparing feature abundances across interacting strain pairs and timepoints.

## Experimental setup
- Bacterial culturing:
  - Spores standardized to 1 x 10^9 CFU/mL in 20% glycerol, diluted to 1 x 10^8 CFU/mL in ISP2 broth.
  - 4 μL inocula placed 1 cm apart in pairs on ISP2 agar; each pairing prepared in quadruplicate for each timepoint (n=20 per pairing).
- ISP2 medium recipe and autoclaving details provided.

## Metabolite extraction and LC-MS acquisition
- Extraction: metabolites obtained from 1 x 0.5 cm agar plugs including mycelia; methanol extraction with freeze-thaw cycles; centrifugation; supernatant dried; reconstituted in 20% methanol and filtered.
- LC-MS instrumentation:
  - Q Exactive Plus MS coupled to Ultimate 3000 UHPLC.
  - Hypersil GOLD C18 column; mobile phases: water + 0.1% formic acid (A) and methanol + 0.1% formic acid (B).
  - Gradient: 95% A initially, linear to 95% B over 8 min, hold, then return to 95% A.
  - Flow: 0.4 mL/min; injection: 5 μL; column 40°C; autosampler 4°C.
  - Blanks at batch start/end; pooled QC every 6th injection; randomised sequence.
  - Data acquired in full MS mode (90–1350 m/z); separate acquisitions for positive and negative modes; resolution 70,000; AGC target 3e6; max IT 200 ms.

## Data processing and analysis
- Raw data converted to mzML; processed with mzMatch (noise removal, filtering, peak matching).
- Features grouped by molecule; only the most intense peak used for downstream analysis.
- Putative feature annotation via Integrated Probabilistic Annotation (IPA).
- Pre-processing:
  - drift and batch effect correction; probabilistic quotient normalization.
  - missing value imputation via k-nearest neighbors.
  - variance stabilization using generalized log (glog).
- Software framework: pmp Bioconductor R package.

## Experimental design details
- Destructive daily sampling with 20 biological replicates per pairing; LC-MS analysis performed in triplicate per timepoint.

## Quality control and reproducibility
- Blank injections to monitor carryover; pooled QC samples every 6th injection to monitor analytical drift.
- Randomised sample sequence; analyses performed in biological triplicate.

## Relevance to data management and leadership (Data Leaders perspective)
- Demonstrates end-to-end data lifecycle: generation, rich metadata capture (sample_IDs.csv), processing, annotation, and QC.
- Metadata and structured outputs (peak tables and sample mappings) support data discoverability, reuse, and cross-study integration.
- Highlights data stewardship considerations: fragmented data sources, need for clear metadata (e.g., sample-to-run mappings, timepoints, and strain pairings), and consistent quality controls.
- Illustrates potential for collaboration and community practices in metabolomics data through standardized formats and documented processing pipelines.
- Notes challenges for data leaders: coordinating multi-partner data, ensuring metadata clarity, and maintaining data quality across temporal, high-replicate experiments.