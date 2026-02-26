# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Contains untargeted metabolomic profiles of paired cultures of 4 interacting Streptomyces strains.
- Isolated from a nature reserve in Minnesota, USA.
- Daily samples collected from day 2 to day 6 in triplicate (paired cultures on ISP2 medium).
- Metabolites extracted by cold methanol; LC-MS data collected in both positive and negative ionisation modes.
- Data provided as raw LC-MS (.mzML) files with m/z, elution time, and ion counts; used to study how metabolism changes in response to neighboring bacteria.
- Funded by NERC (NE/T010959/1) and the National Science Foundation (USA, 1935458).

## Data Format and Access
- File format: .mzML (open-source, standardized LC-MS data).
- Includes mass spectral data (m/z, ion counts, elution times) and metadata (instrument settings, modes).
- mzML is readable by common metabolomics software (e.g., UmetaFlow).
- File naming convention: [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
  - [n/p]: negative (n) or positive (p) ionisation mode.
  - [2/3/4/5/6]: day post inoculation.
  - [A/B/C/D/agar]: first letter = bacterial strain; second letter = neighboring strain; "agar" indicates background control.
  - [1/2/3]: replicate number.
- Analyzed peak datasets are available in a separate related deposit.

## Experimental Context (Bacterial Culturing)
- Spores standardized and aliquoted at 1 × 10^9 CFU/mL in 20% glycerol.
- Diluted 10-fold to 1 × 10^8 CFU/mL in ISP2 broth; 4 μL inoculated 1 cm apart in pairs on ISP2 agar.
- Each pairing prepared in quadruplicate for 5 timepoints (n = 20 per pairing) to enable metabolite and RNA sampling in triplicate daily (with a spare).
- ISP2 composition: yeast extract, malt extract, D-glucose, optionally agar, pH 7.2.

## Metabolite Extraction
- 1 cm rectangular agar plugs including mycelia and surrounding agar collected and stored at -80 °C.
- Extraction: 1 mL 100% methanol (-48 °C) with three freeze-thaw cycles.
- Centrifuge at 8000 × g for 10 min at 4 °C; collect supernatant and dry by SpeedVac.
- Reconstitute in 200 μL 20% methanol; sonicate 5 min; filter through 0.2 μm.

## LC-MS Data Acquisition
- Instrumentation: Q Exactive Plus mass spectrometer coupled to Ultimate 3000 UHPLC.
- Column: Hypersil GOLD C18 (3 μm, 2.1 mm × 100 mm).
- Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
- Gradient: 95% A for 2 min → linear to 95% B over 8 min → hold 95% B for 2 min → return to 95% A; final hold.
- Column temp: 40 °C; autosampler 4 °C; flow 0.4 mL/min; injection volume 5 μL.
- Injections: blank injections at batch start and end; pooled QC every 6th injection; sequence randomized.
- Data: full MS mode, 90–1350 m/z; resolution 70,000; AGC target 3e6; max injection time 200 ms.
- Acquisition modes: separate runs for positive and negative ionisation modes.

## Data Processing and Metadata
- Raw data converted to mzML using ProteoWizard.
- Analyzed peak datasets are available in a separate related deposit.
- Metadata includes instrument settings, chromatographic conditions, and acquisition parameters.

## Experimental Design and Sampling
- 20 biological replicates per pairing to support daily destructive sampling for metabolomics.
- LC-MS analysis conducted in triplicate per timepoint.

## Laboratory Instrumentation
- UHPLC system: Ultimate 3000 (ThermoFisher) with Hypersil GOLD C18 column.
- Mass spectrometer: Q Exactive Plus Hybrid Quadrupole-Orbitrap.

## Quality Control
- Blanks to assess carryover; pooled QC samples every 6th injection to monitor analytical drift.
- Randomized sample sequence.
- Biological triplicates for sampling and analysis.