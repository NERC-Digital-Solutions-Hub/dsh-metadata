# Working Title Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

- A dataset of untargeted metabolomics features from paired cultures of four Streptomyces strains isolated from a Minnesota nature reserve.
- Samples collected daily from day 2 to day 6 in triplicate, via 1 cm agar plugs paired on ISP2 medium, with 5 timepoints in total.
- Metabolites extracted with cold methanol and analyzed by LC-MS in both positive and negative ionization modes.
- Features include mass-to-charge (m/z), retention time, and ion intensities across samples; relative abundances used to compare interacting strain pairs.

## Data files and structure

- positive_peaks_table.csv: LC-MS data for features detected in positive ionization mode; columns include peak_ID, m/z, retention_time, and per-sample intensity counts.
- negative_peaks_table.csv: LC-MS data for features detected in negative ionization mode; same column structure as positive table.
- sample_IDs.csv: mappings for each sample_ID to metadata (day, replicate, sampled strain, partner strain).

## Columns and data types

- peak_ID: Arbitrary feature identifier (integer).
- m/z: Mass-to-charge ratio (dimensionless).
- retention_time: Elution time on the C18 column (seconds).
- sXX: Sample run identifiers; columns containing ion counts for each sample.
- sample_ID: Identifier in the format sXX; corresponds to columns in peak tables.
- Day: Sampling day (days; inoculation day is day 0; e.g., day 2 = 48 hours post-inoculation).
- Sampled_strain: Strain being sampled (A, B, C, D) or '-' for agar-only controls.
- Next_to_strain: Strain grown next to the sampled strain on the plate (or '-' for controls).
- Replicate: Biological replicate number (1, 2, or 3).

## Experimental design

- n = 20 biological replicates per pairing to enable destructive daily sampling for MS analysis.
- LC-MS analysis of each sample timepoint performed in triplicate.
- Five timepoints (days 2–6) with paired strains, plus controls.

## Culturing and sample preparation

- Spores standardized to 1 x 10^9 CFU/mL in 20% glycerol, diluted to 1 x 10^8 CFU/mL in ISP2, then spotted 4 μL in pairs on ISP2 agar (1 cm apart).
- Each pairing prepared in quadruplicate per timepoint (n = 20 per pairing) for metabolomics and RNA sampling in triplicate daily.

## ISP2 medium details

- Composition per litre: 4 g yeast extract, 10 g malt extract, 4 g glucose, optional 20 g agar; pH 7.2 (adjusted with NaOH).
- Sterilized by autoclaving.

## Metabolite extraction

- 1 x 0.5 cm agar plugs including mycelia and surrounding agar collected and stored at -80 °C.
- Extraction with 1 mL of precooled 100% methanol (-48 °C), with three freeze-thaw cycles.
- Centrifugation, collection of supernatant, and drying by SpeedVac; reconstituted in 200 μL 20% methanol, sonicated, and filtered (0.2 μm).

## LC-MS data acquisition

- Instrumentation: Q Exactive Plus Orbitrap MS coupled to Ultimate 3000 UHPLC.
- Column: Hypersil GOLD C18, 3 μm, 2.1 mm × 100 mm.
- Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
- Gradient: 95% A (2 min) → 95% B (over 8 min) → hold 95% B (2 min) → return to 95% A (0.25 min) → hold (2 min).
- Column temperature: 40 °C; autosampler at 4 °C; flow rate 0.4 mL/min; injection volume 5 μL.
- Data acquisition: full MS (90–1350 m/z) at 70,000 resolution; positive and negative modes acquired separately; QC and blanks included; randomised sample sequence.

## Data processing and analysis

- Raw data converted to mzML with ProteoWizard.
- Feature detection and processing with mzMatch (Java/R); noise removal, filtering, peak matching; grouping to single molecule per feature (most intense peak retained).
- Putative annotation via Integrated Probabilistic Annotation (IPA).
- Pre-processing steps (applied before statistics): drift and batch correction, probabilistic quotient normalization, missing value imputation (k-nearest neighbours), variance stabilization via generalized log (glog); implemented with pmp Bioconductor package.
- Experimental design incorporated, with 20 biological replicates per pairing and triplicate LC-MS analysis per timepoint.

## Quality control

- Blanks analyzed at start and end of batch to assess carryover.
- Pooled QC samples injected every 6th run to monitor analytical drift.
- Randomised sample sequence to mitigate systematic bias.
- Analyses conducted in biological triplicate for sampling and technical triplicate for MS.

## Funding and references

- Funded by Natural Environment Research Council (NERC NE/T010959/1) and National Science Foundation (USA, 1935458).
- References for IPA, mzMatch, and pmp tools cited (Del Carratore et al. 2019, 2023; Jankevics et al. 2023; Scheltema et al. 2011).