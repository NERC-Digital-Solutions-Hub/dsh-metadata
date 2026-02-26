# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted metabolomic profiles from paired cultures of four Streptomyces strains isolated from a Minnesota nature reserve.
- Daily samples (days 2–6) from paired cultures grown on solid ISP2 medium, in triplicate.
- Data collected as LC-MS in both positive and negative ionisation modes.
- Raw data provided in open-source mzML format, including m/z, elution time, and ion counts, plus metadata.
- Aimed at investigating how metabolism changes in response to neighboring bacterial cultures.
- Funded by NERC (NE/T010959/1) and NSF (USA, 1935458).

## Data Content and Format
- Raw LC-MS data converted to mzML format for each sample run in both positive and negative modes.
- mzML files include mass-to-charge ratios (m/z), ion counts, elution times, and instrument metadata.
- Related deposit contains analysed (picked) peak datasets; this deposit focuses on raw data.

## File Format and Naming
- File format: mzML (open-source LC-MS data format).
- File naming convention: [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
  - n/p = negative or positive ionisation mode.
  - 2–6 = day post inoculation.
  - A/B/C/D/agar = first letter = bacterial strain; second letter = neighboring strain; "agar" denotes background controls with no microbes.
  - 1/2/3 = replicate number.

## Experimental Design
- For each bacterial pairing, 4 replicates per timepoint (days 2–6), totaling 20 samples per pairing (n=20).
- Metabolites and RNA sampling performed in triplicate daily (mass spectrometry injections); one spare replicate included.

## Bacterial Culturing
- Spores standardized and aliquoted to 1 x 10^9 CFU/mL in 20% glycerol.
- Before use, diluted 10-fold to 1 x 10^8 CFU/mL in ISP2 broth.
- 4 μL inoculated 1 cm apart in pairs on ISP2 agar; quadruplicate per pairing for each timepoint.

## ISP2 Medium
- Composition per litre: 4 g yeast extract, 10 g malt extract, 4 g D-glucose, optional 20 g agar; pH 7.2 adjusted with NaOH.
- Autoclaved for sterilization.

## Metabolite Extraction
- 1 x 0.5 cm × 1 cm rectangular agar plugs (including mycelia and surrounding agar) stored at -80 °C.
- Extraction: 1 mL 100% cold methanol (-48 °C); three freeze–thaw cycles; centrifugation; collect supernatant; dry by SpeedVac.
- Reconstitution: 200 μL 20% methanol, 5 min sonication, 0.2 μm filtration prior to injection.

## LC-MS Data Acquisition
- Instrumentation: Q Exactive Plus Hybrid Quadrupole-Orbitrap MS with Ultimate 3000 UHPLC.
- Column: Hypersil GOLD C18, 3 μm, 2.1 mm × 100 mm.
- Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
- Gradient: 95% A (2 min) → linear to 95% B over 8 min → hold 95% B (2 min) → return to 95% A in 0.25 min and hold (2 min).
- Flow rate: 0.4 mL/min; injection volume: 5 μL.
- Quality control: blank injections at start/end; pooled QC every 6th injection; randomized sample sequence.
- Acquisition: full MS (90–1350 m/z); resolution 70,000; AGC target 3e6; max injection time 200 ms.
- Modes: data acquired separately in positive and negative ionisation modes.

## LC-MS Data Analysis
- Raw data converted to mzML format using ProteoWizard MS converter.
- Analyzed peak datasets available in a separate related deposit.
- Open-source workflows (e.g., UmetaFlow) applicable for high-throughput untargeted metabolomics data processing.

## Quality Control
- Blank injections to monitor carryover.
- Pooled QC samples analyzed every 6 injections to assess analytical drift.
- Randomized sample sequence to prevent batch effects.
- Biological triplicates for sampling and analysis.

## Data Access and Funding
- Data are provided as open mzML files with accompanying metadata.
- Funding acknowledged: NERC NE/T010959/1 and NSF USA 1935458.
- Includes background controls (agar) to differentiate microbial signals from environmental/background features.