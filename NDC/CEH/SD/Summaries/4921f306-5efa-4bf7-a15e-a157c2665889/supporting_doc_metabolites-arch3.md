# Working Title Features detected by untargeted metabolomic analysis of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Purpose: describe a dataset from untargeted metabolomics of paired cultures of four interacting Streptomyces strains, to assess changes in metabolite profiles across interactions.
- Origin: isolated from a Minnesota nature reserve; daily sampling of paired colonies on ISP2 medium from day 2 to day 6, in triplicate.
- Outcome: provides mass-to-charge (m/z), retention time, and ion intensities for detected features; enables comparison of feature abundances between interacting strain pairs.

## Data content and structure
- Files included (CSV format):
  - positive_peaks_table.csv: LC-MS features detected in positive ionization mode with intensities.
  - negative_peaks_table.csv: LC-MS features detected in negative ionization mode with intensities.
  - sample_IDs.csv: metadata linking sample IDs to time point, strain, partner strain, and replicate.
- Key columns:
  - peak_ID: feature identifier.
  - m/z: mass-to-charge ratio.
  - retention_time: elution time (seconds).
  - sXX: individual LC-MS run identifiers (samples).
  - sample_ID: links to sample_IDs.csv; Day (in days, inoculation day 0 = day 2), Sampled_strain, Next_to_strain, Replicate.
- Data interpretation: relative abundance of each feature compared across interacting strain pairs to infer metabolic changes.

## Experimental design
- Biological design: four Streptomyces strains interacting in pairs; each pairing sampled daily across days 2–6.
- Replication: n = 20 biological replicates per pairing for destructive daily sampling; LC-MS analysis performed in triplicate per timepoint.
- Culturing context: spores standardized to 1 x 10^9 CFU/mL, diluted to 1 x 10^8 CFU/mL, 4 μL inoculated 1 cm apart on ISP2 agar; quadruplicate preparations per pairing per timepoint.

## Methods

### Culturing and media
- ISP2 medium recipe described (yeast extract, malt extract, glucose, agar optional; pH 7.2).
- Autoclaving for sterilization.

### Metabolite extraction
- Tissue: rectangular agar plugs including mycelia and surrounding agar.
- Extraction: 1 mL precooled 100% methanol (-48 °C) with three freeze-thaw cycles; centrifugation; supernatant dried; reconstitution in 200 μL 20% methanol; filtration.

### LC-MS data acquisition
- Instrumentation: Q Exactive Plus MS coupled to Ultimate 3000 UHPLC with Hypersil GOLD C18 column.
- Chromatography: water with 0.1% formic acid (A) and methanol with 0.1% formic acid (B); specified gradient; 40 °C column temperature; 0.4 mL/min flow; 5 μL injection.
- ESI modes: data acquired in positive and negative modes separately; blanks before and after batch; pooled QC every 6th injection; randomized sample sequence.

## Data processing and analysis

### Raw data handling
- Conversion: mzML format using ProteoWizard MS converter.

### Feature processing
- Pipeline: mzMatch (Java/R) for noise removal, signal filtering, peak matching; grouping of features by molecule; only the most intense peak used for downstream analysis.
- Annotation: putative annotation with Integrated Probabilistic Annotation (IPA).

### Pre-processing and normalization
- Drift and batch effect correction; probabilistic quotient normalization (PQN); missing value imputation via k-nearest neighbors; variance stabilization via generalized logarithm (glog).
- Tools: processed with pmp Bioconductor R package.

### Experimental design alignment
- Data prepared for comparative analyses across interacting strain pairs; enabling interpretation of metabolite changes due to inter-strain interactions.

## Quality control and reproducibility
- QC measures: blank injections at start and end; pooled QC samples every 6th injection to monitor drift; randomized sample sequence.
- Replication: biological triplicates for analysis; overall experimental design supports robust comparison between interacting partners.

## Funding and references
- Funding: Natural Environment Research Council (NERC NE/T010959/1) and National Science Foundation (USA, 1935458).
- Key references for methods and tools: ipaPy2 (Integrated Probabilistic Annotation), IPA; mzMatch; pmp; PeakML/mzMatch framework.