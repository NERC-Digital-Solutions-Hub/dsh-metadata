# Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

- Overview
  - Untargeted LC-MS metabolomic features detected from paired cultures of four interacting Streptomyces strains isolated from a Minnesota nature reserve.
  - Daily samples from day 2 to day 6, grown in adjacent pairs on solid ISP2 medium, in triplicate.
  - Metabolites extracted with cold methanol; LC-MS data collected in positive and negative ionisation modes.
  - Dataset includes mass-to-charge (m/z), retention time, and ion intensities for identified peaks; relative abundance compared between interacting strain pairs to infer metabolic changes.
  - Funded by NERC (NE/T010959/1) and NSF (USA, 1935458).

- Files and naming conventions
  - positive_peaks_table.csv: LC-MS data for features detected in positive ionisation mode; identified peaks and intensities.
  - negative_peaks_table.csv: LC-MS data for features detected in negative ionisation mode; identified peaks and intensities.
  - sample_IDs.csv: metadata linking sample IDs to time point, replicate, strain, and partner strain.

- Dataset structure and columns
  - Table columns (in both positive and negative peaks tables):
    - peak_ID: arbitrary feature identifier.
    - m/z: mass-to-charge ratio.
    - retention_time: time of elution from C18 column (seconds).
    - sXX: sample run identifier; counts per feature for each LC-MS run.
  - sample_IDs.csv columns:
    - sample_ID: identifier of format sXX.
    - Day: sampling day (day 0 = inoculation); e.g., day 2 = 48 hours post-inoculation.
    - Sampled_strain: which of A, B, C, D was sampled; '-' indicates agar-only controls.
    - Next_to_strain: which strain was grown next to the sampled strain; '-' indicates controls.
    - Replicate: replicate number (1, 2, or 3).

- Bacterial culturing and experimental design
  - Spores standardized to 1 x 10^9 CFU/mL in 20% glycerol; diluted 10-fold to 1 x 10^8 CFU/mL in ISP2 broth.
  - 4 μL inoculated 1 cm apart in pairs on ISP2 agar; each pairing prepared in quadruplicate for each of 5 timepoints (n=20 per pairing).
  - Designed to enable destructive daily sampling for metabolomics and parallel RNA sampling.

- ISP2 media details
  - Composition per litre: 4 g yeast extract, 10 g malt extract, 4 g glucose, optionally 20 g agar; pH adjusted to 7.2 with NaOH.
  - Autoclaved for sterilization.

- Metabolite extraction protocol
  - Excised rectangular agar plugs (1 x 0.5 cm) including mycelia and surrounding agar; stored at -80 °C.
  - Extraction: add 1 mL precooled 100% methanol (-48 °C), perform three freeze–thaw cycles.
  - Centrifuge at 8000 x g for 10 min at 4 °C; collect supernatant and dry by SpeedVac.
  - Reconstitute in 200 μL 20% methanol, sonicate 5 min, filter through 0.2 μm filter prior to injection.

- LC-MS instrumentation and run conditions
  - Instrumentation: Q Exactive Plus Mass Spectrometer coupled to Ultimate 3000 UHPLC; Hypersil GOLD C18 column.
  - Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
  - Gradient: 95% A for 2 min, linear to 95% B over 8 min, hold 95% B for 2 min, return to 95% A and hold for 2 min.
  - Column temp: 40 °C; autosampler at 4 °C; flow rate: 0.4 mL/min; injection volume: 5 μL.
  - Data acquisition: full MS scans from m/z 90–1350; resolution 70,000; AGC target 3e6; max injection time 200 ms.
  - Modes: separate runs for positive and negative ionisation.

- QC and experimental controls
  - Blank injections at start and end of batch to assess carryover.
  - Pooled QC samples every 6th injection to monitor analytical drift.
  - Randomised sample sequence.
  - Biological triplicates for sampling and analysis.

- Data processing and analysis workflow
  - Raw data converted to mzML using ProteoWizard MS converter.
  - Processing with mzMatch: noise removal, signal filtering, peak matching; grouping features by molecule and retaining the most intense peak for downstream analysis.
  - Putative feature annotation with Integrated Probabilistic Annotation (IPA).
  - Pre-processing prior to statistics:
    - Signal drift and batch effect correction.
    - Probabilistic quotient normalization.
    - Missing value imputation via k-nearest neighbours.
    - Variance stabilization using generalized log (glog) transformation.
  - Pipeline implemented with pmp Bioconductor R package.

- Experimental replication and data scale
  - 20 biological replicates per pairing to support daily destructive sampling.
  - LC-MS analysis performed in triplicate per timepoint.

- Data usage notes
  - Cross-reference sample_IDs.csv to map samples (day, strain, neighbor, replicate) to feature intensities in positive/negative peak tables.
  - Feature-level data include only the most intense peak per molecule after processing.

- References and software
  - IPA: Integrated Probabilistic Annotation (IPA) for metabolite annotation.
  - pmp: Peak Matrix Processing and batch correction for metabolomics data.
  - mzMatch: Peak detection, alignment, and data processing for LC-MS datasets.

- Funding
  - Natural Environment Research Council (NERC) NE/T010959/1.
  - National Science Foundation (USA) 1935458.