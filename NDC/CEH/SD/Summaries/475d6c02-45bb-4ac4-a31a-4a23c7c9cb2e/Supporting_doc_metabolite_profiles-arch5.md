# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

## Overview
- Untargeted metabolomic profiles of four interacting Streptomyces strains isolated from a Minnesota nature reserve.
- Paired cultures grown in adjacent spots on ISP2 medium; samples collected day 2–6 in triplicate, with quadruplicate pairings for each timepoint (n=20 per pairing).
- Goal: understand how metabolism changes in response to neighboring bacterial cultures.
- Data funded by NERC (NE/T010959/1) and NSF (USA, 1935458).

## Data format and contents
- Primary data: raw LC-MS data in open-format mzML.
- Separate data included for metadata and instrument parameters; analyses of peak picking available in a related deposit.
- Modes: data collected in both positive and negative ionisation modes.
- Contents per file: mass-to-charge ratios (m/z), ion counts, elution times, and instrument metadata.

## File naming convention
- Delimited by dashes: [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
  - n/p: negative or positive mode.
  - 2–6: day post inoculation.
  - A/B/C/D/agar: first letter = bacterial strain; second letter = neighboring strain; "agar" denotes background controls without microbes.
  - 1/2/3: replicate number.

## Data provenance and metadata
- Metadata and experimental conditions captured (strains, pairing, timepoints, culture conditions, sampling).
- mzML is a standard open format readable by multiple metabolomics tools (e.g., UmetaFlow).
- Open data approach facilitates interoperability and reuse by the community.

## Experimental design and sample preparation
- Bacterial preparation: spores standardized to 1 × 10^9 CFU/mL in 20% glycerol, diluted to 1 × 10^8 CFU/mL in ISP2 broth before plating.
- Pairing: 4 strains in adjacent pairs on ISP2 agar; each pairing prepared in quadruplicate per timepoint (20 samples per pairing).
- ISP2 composition and pH (7.2) provided; autoclave sterilization used.
- Replication: daily sampling for mass spectrometry and RNA in triplicate, with one spare.

## Metabolite extraction
- Metabolites extracted from rectangular agar plugs containing mycelia and surrounding agar.
- Extraction: 1 mL of precooled 100% methanol (-48 °C) with three freeze-thaw cycles; centrifuge and collect supernatant.
- Drying: SpeedVac; reconstitute in 200 μL 20% methanol; sonication and 0.2 μm filtration prior to injection.

## LC-MS data acquisition and instrumentation
- Instrumentation: Q Exactive Plus mass spectrometer coupled to Ultimate 3000 UHPLC.
- Column: Hypersil GOLD C18; 3 μm, 2.1 mm × 100 mm.
- Chromatography: water with 0.1% formic acid (A) and methanol with 0.1% formic acid (B); gradient from 95% A to 95% B, with re-equilibration.
- Flow: 0.4 mL/min; injection volume 5 μL.
- Data acquisition: full MS mode, 90–1350 m/z, 70,000 resolution, AGC 3e6, max 200 ms; separate acquisitions for positive and negative modes.
- QC and blanks: blanks at start/end; pooled QC every 6th injection; randomized sample order.

## Data processing and availability
- Raw data conversion to mzML performed with ProteoWizard.
- This deposit contains raw mzML files; a separate related deposit contains analyzed peak datasets.
- Metadata and methodological details enable reproducibility and re-processing.

## Quality control and replication
- Biological triplicates for sampling; destructive daily sampling allowed (n=20 per pairing).
- Instrumental QC: blanks and pooled QC samples to monitor carryover and drift; randomized sequencing to mitigate batch effects.

## Governance, standards, and reuse considerations
- Data are provided in open, interoperable formats (mzML) to support broad reuse and tool compatibility.
- File naming encodes critical experimental variables (mode, day, strain pairing, replicate) to aid discoverability and interpretation.
- No explicit licensing stated; users should refer to deposit metadata and acknowledgments for usage and attribution.
- Potential data stewardship considerations:
  - Large dataset size due to multiple timepoints, modes, and replicates.
  - Processed data are available separately, so users should consult both deposits for comprehensive analysis.
  - Background controls (agar) are explicitly identified in file names for proper interpretation.

## Funding and acknowledgments
- Funded by NERC (NE/T010959/1) and NSF (USA, 1935458).