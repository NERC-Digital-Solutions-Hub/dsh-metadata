# Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- A dataset from untargeted LC-MS metabolomics of paired cultures involving four Streptomyces strains isolated from a Minnesota nature reserve.
- Daily samples (days 2–6) from adjacent paired cultures grown on solid ISP2 medium, analyzed in triplicate.
- Metabolites detected as mass-to-charge (m/z) features with retention times and ion intensities in both positive and negative ionisation modes.
- Aim: compare relative feature abundances between interacting strain pairs to understand metabolic changes.
- Funding: NERC and NSF (USA).

## Files and naming conventions
- positive_peaks_table.csv: peaks and intensities detected in positive ionisation mode.
- negative_peaks_table.csv: peaks and intensities detected in negative ionisation mode.
- sample_IDs.csv: mapping of sample IDs to time point, replicate, bacterial strain, and partner strain.

## Data fields and units
- Table 1 (negative_peaks_table.csv and positive_peaks_table.csv)
  - peak_ID: arbitrary feature identifier number.
  - m/z: mass-to-charge ratio (dimensionless).
  - retention_time: time of elution from C18 column (seconds).
  - sXX: sample identifiers (columns for each LC-MS run); counts per feature per sample.
- Table 2 (sample_IDs.csv)
  - sample_ID: like sXX, linking to peak data columns.
  - Day: sampling day (days since inoculation; e.g., day 2 = 48 hours).
  - Sampled_strain: which strain was sampled (A–D; '-' for agar-only controls).
  - Next_to_strain: which strain was grown next to the sampled strain (A–D; '-' for agar-only controls).
  - Replicate: replicate number (1, 2, or 3).

## Experimental design and sampling regime
- Four Streptomyces strains paired in quadruplicate for each pairing (n = 20 total replicates per pairing) to enable daily destructive sampling for MS and RNA analyses.
- Each timepoint has LC-MS analysis in triplicate.
- Spores standardized to 1 x 10^9 CFU/mL in 20% glycerol; diluted to 1 x 10^8 CFU/mL in ISP2 broth; 4 μL inoculated 1 cm apart on ISP2 agar.

## Metabolite extraction and LC-MS methods
- Metabolite extraction: cold methanol extraction with freeze-thaw cycles; samples dried and reconstituted before LC-MS.
- LC-MS instrumentation: Q Exactive Plus Hybrid Quadrupole-Orbitrap MS coupled to Ultimate 3000 UHPLC; Hypersil GOLD C18 column.
- Chromatography: gradient from 95% A to 95% B, with a 40 °C column temperature; flow 0.4 mL/min; injection volume 5 μL.
- Data acquisition: full MS in positive and negative modes, range 90–1350 m/z, resolution 70,000; QC and blank injections included; randomised sample sequence.

## Data processing and analysis
- Raw data converted to mzML via ProteoWizard.
- Processing with mzMatch: noise removal, signal filtering, peak matching; grouping by molecule, using the most intense peak for statistics.
- Putative annotation with Integrated Probabilistic Annotation (IPA).
- Pre-processing steps (via pmp R package): drift/batch correction, probabilistic quotient normalization, missing value imputation (k-nearest neighbors), variance stabilization (glog).
- Experimental design support: designed to enable cross-sample comparisons and robust statistics.

## Quality control and laboratory practices
- Blanks analyzed at start and end to assess carryover; pooled QC samples analysed every 6th injection.
- Randomised sample sequence to reduce bias.
- Biological replication confirmed (triplicate analyses).

## Instrumentation and references
- LC-MS: Thermo Scientific Q Exactive Plus and Ultimate 3000 UHPLC with Hypersil GOLD C18 column.
- Software and methods referenced: mzML (ProteoWizard), mzMatch, Integrated Probabilistic Annotation (IPA), ipaPy2, pmp (Bioconductor), and related methodological papers.

## GIS relevance and potential uses
- This dataset is non-spatial; it captures temporal metabolomic changes across strain pairings rather than geographic locations.
- For GIS applications, useful in contexts where metabolomic dynamics are linked to geolocated environmental samples, requiring added geospatial metadata.
- The structured sample_IDs mapping enables time-series visualization and cross-strain comparisons, which can be integrated with spatial datasets in GIS-enabled dashboards if geolocation data are incorporated in future work.
- Quality control and replication details support reproducibility and credible mapping of metabolomic features over time.