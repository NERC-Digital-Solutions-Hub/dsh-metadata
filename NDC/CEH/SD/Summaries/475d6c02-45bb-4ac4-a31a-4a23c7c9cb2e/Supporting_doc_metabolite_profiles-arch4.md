# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted metabolomic profiles of paired cultures from four interacting Streptomyces strains isolated in Minnesota, USA.
- Daily samples collected from day 2 to day 6 in triplicate, using adjacent pairings on solid ISP2 medium.
- Metabolites extracted by cold methanol and analyzed by LC-MS in both positive and negative ionisation modes.
- Data provided as raw LC-MS data in open-source mzML format, including m/z, elution time, and ion counts.
- Research goal: investigate how metabolism of interacting strains changes in response to neighboring cultures.
- Funding: NERC NE/T010959/1 and NSF USA 1935458.

## Data Content and Metadata
- Raw LC-MS data captured as mzML files (mass-to-charge, ion counts, elution times) with instrument metadata.
- Metadata supports interpretation across platforms; files readable by common metabolomics tools (e.g., UmetaFlow).
- Separate deposit contains analysed/peak datasets (processed data).

## File Formats and Naming
- File format: .mzML (open-source, standard for LC-MS data).
- File naming convention: [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
  - [n/p]: negative (n) or positive (p) ionisation mode.
  - [2/3/4/5/6]: day post inoculation.
  - [A–D/agar]: first letter = bacterial strain; second letter = neighboring cultured strain; "agar" indicates background controls with no microbes.
  - [1/2/3]: replicate number.

## Experimental Design and Sample Preparation
- Bacterial culturing: spores standardized to 1 × 10^9 CFU/mL in 20% glycerol, diluted 10-fold to 1 × 10^8 CFU/mL in ISP2 broth; 4 μL inoculated 1 cm apart in pairs on ISP2 agar.
- Replication: each pairing prepared in quadruplicate for each of 5 timepoints (n = 20 per pairing) to enable metabolite and RNA sampling in triplicate daily (with one spare).
- ISP2 composition and pH: yeast extract, malt extract, glucose, optional agar, pH 7.2.
- Metabolite extraction: agar plugs with mycelia excised; methanol extraction with freeze-thaw cycles; supernatant dried and reconstituted for LC-MS; filtered prior to injection.
- Storage: extracts kept at -80 °C prior to analysis.

## LC-MS Data Acquisition
- Instrumentation: Q Exactive Plus Hybrid Quadrupole-Orbitrap MS coupled to Ultimate 3000 UHPLC.
- Column: Hypersil GOLD C18, 3 μm, 2.1 mm × 100 mm.
- Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
- Gradient and run conditions: initial 95% A, ramp to 95% B over 8 min, hold 95% B for 2 min, return to 95% A, re-equilibrate.
- Flow rate: 0.4 mL/min; injection volume: 5 μL; column at 40 °C; autosampler at 4 °C.
- Quality control: blanks at batch start/end; pooled QC every 6th injection; randomized sample sequence.
- Data acquisition: full MS (m/z 90–1350) at 70,000 resolution; AGC target 3e6; max IT 200 ms.
- Modes: data collected separately for positive and negative modes.

## Data Processing and Availability
- Raw data converted to mzML format using ProteoWizard MS converter.
- Open-format mzML files constitute the deposited raw data.
- Processed/analysed peak datasets are available in a separate related deposit.
- Suggested analysis tools: UmetaFlow (and similar metabolomics workflows).

## Experimental Design Details
- Timepoints: days 2–6 post inoculation (5 timepoints).
- Biological replicates: n = 20 per pairing (4 strains × neighboring strains across timepoints with quadruplicate preparations).
- LC-MS analysis: performed in triplicate per timepoint per pairing.

## Quality Control and Reproducibility
- Run order randomized; inclusion of blanks and pooled QC to monitor carryover and drift.
- Biological triplicates for sampling and replication to support robustness and reproducibility.

## Data Use and Funding
- Data are provided in open mzML format to enable reanalysis and integration with metadata.
- Suitable for downstream statistical analyses, cross-study comparisons, and method development.
- Funding acknowledgments: NERC NE/T010959/1 and National Science Foundation (USA) 1935458.