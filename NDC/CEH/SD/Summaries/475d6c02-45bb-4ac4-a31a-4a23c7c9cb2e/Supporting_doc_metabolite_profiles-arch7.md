# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted metabolomic profiles of paired cultures from four Streptomyces strains isolated in Minnesota, USA nature reserve.
- Daily samples collected from day 2 to day 6 in triplicate, in adjacent pairs on solid ISP2 medium.
- Metabolites extracted with cold methanol; data collected by LC-MS in both positive and negative ionisation modes.
- Raw LC-MS data stored in open-source mzML format, including mass-to-charge (m/z), elution time, and ion counts.
- Aimed at investigating how metabolism of interacting strains changes in response to neighbouring bacterial cultures.
- Funded by NERC (NE/T010959/1) and the National Science Foundation (USA, 1935458).

## Data and File Formats
- Primary data format: mzML (open-source, vendor-neutral LC-MS data).
- File contents: mass spectral data (m/z, ion counts, elution times) plus instrument metadata; suitable for various metabolomics tools (e.g., UmetaFlow).
- File naming convention (delimited by dashes): [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
  - [n/p] = negative (n) or positive (p) ionisation mode
  - [2/3/4/5/6] = day post inoculation
  - [A/B/C/D/agar] = first letter = bacterial strain; second letter = neighbouring strain; if second letter omitted, neighbouring strain is same as first; "agar" denotes background controls with no microbes
  - [1/2/3] = replicate number
- mzML files are complemented by a related deposit containing analysed peak datasets.

## Experimental Design and Sampling Regime
- Bacterial preparations: spores standardized to 1 × 10^9 CFU/mL in 20% glycerol; diluted 10-fold to 1 × 10^8 CFU/mL in ISP2 broth.
- Inoculation: 4 μL per culture pair, placed 1 cm apart on ISP2 agar; quadruplicate for each pairing per timepoint.
- Timepoints: 5 days (days 2–6), with metabolites and RNA sampling in triplicate daily plus one spare.
- Pairings: adjacent culture pairs on agar to study interactions; background controls with no microbes also included.

## Metabolite Extraction
- Sample collection: rectangular agar plugs (1 × 0.5 cm) including mycelia and surrounding agar, stored at −80 °C.
- Extraction: add 1 mL of precooled 100% methanol (−48 °C), perform three freeze-thaw cycles (liquid nitrogen, ice, vortex).
- Clarification: centrifuge at 8000 × g for 10 min at 4 °C; collect 1 mL supernatant.
- Drying and reconstitution: SpeedVac drying, reconstitute in 200 μL 20% methanol, sonicate 5 min, filter (0.2 μm).

## LC-MS Data Acquisition
- Instrumentation: Q Exactive Plus mass spectrometer coupled to Ultimate 3000 UHPLC; Hypersil GOLD C18 column.
- Chromatography: water + 0.1% formic acid (A) and methanol + 0.1% formic acid (B); gradient: 95% A to 95% B over 8 min, hold, then return to 95% A; total run time aligned with 0.4 mL/min flow, 5 μL injection.
- Quality controls: blank injections at batch start/end; pooled QC every 6th injection; randomised sample sequence.
- Acquisition: full MS mode, 90–1350 m/z, resolution 70,000, AGC target 3e6, maximum injection time 200 ms; separate acquisitions for positive and negative modes.
- Instrumentation details: Ultimate 3000 UHPLC and Q Exactive Plus Hybrid Quadrupole-Orbitrap MS.

## Data Processing and Analysis
- Data conversion: raw mzML files generated from the Q Exactive data using ProteoWizard MS converter.
- Data products: raw mzML files are deposited; analyzed peak datasets are available in a separate related deposit.
- Software compatibility: mzML format readable by multiple metabolomics tools (e.g., UmetaFlow).

## Quality Control and Experimental Rigor
- Carryover checks via blank injections at batch boundaries.
- Analytical drift assessment via pooled QC samples every 6th injection.
- Randomised sample sequence to mitigate systematic bias.
- Biological triplicates for sampling and analysis to ensure reproducibility.

## Practical Notes for Reuse
- Structure supports cross-timepoint and cross-pair comparisons to study interaction-driven metabolic changes.
- File naming embeds critical contextual metadata (mode, day, strains, replicate) for straightforward data filtering.
- Open mzML format enables integration with standard metabolomics pipelines and downstream analyses.

## Funding and Attribution
- Supported by NERC and the National Science Foundation (USA).