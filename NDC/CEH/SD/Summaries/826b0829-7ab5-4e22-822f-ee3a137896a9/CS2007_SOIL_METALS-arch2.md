# Soil metals 2007 [Countryside Survey], Great Britain

## Overview
- A dataset of soil metals from Countryside Survey 2007 in Great Britain.
- 402 soil cores collected from up to 256 1km squares across GB.
- Analytes include Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg; plus land class (LC07) and location metadata.
- Data intended for consistent environmental health monitoring and policy performance assessment.

## Data structure and variables
- Core identifiers and location:
  - SQUARE: 1km square sampling site code
  - PLOT: Plot identifier within each square
  - YEAR: Year of survey
- Metal concentrations (ppm, equivalent to mg/kg and µg/g):
  - CD, CR, CU, NI, PB, ZN, AL, TI, MN, AS, SE, MO, HG
- Classification and geography:
  - LC07, LC07_NUM: ITE Land Class 2007 codes
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: County or Council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data usage metadata:
  - All CS data must be acknowledged as Countryside Survey data owned by NERC - CEH

## Sampling design and scope
- Field strategy based on a rigorous statistical framework.
- GB stratified into Land Classes to capture environmental gradients.
- 591 sample squares surveyed in 2007 (England 289, Wales 107, Scotland 195).
- Soil samples collected from the top 0–15 cm, with sampling locations distributed across corners of plots to ensure representation and comparability with previous surveys (1978, 1998; 2007 used western corner of Main Plots).
- Metals analyzed from 402 cores; up to 2 cores randomly selected per 5 X-plots in the original design.

## Laboratory methods
- Analyses performed with ICP-OES; 2007 augmented with inductively coupled plasma mass spectrometry (ICP-MS) to enable more analytes per run.
- Standard analytical suite at CEH Lancaster includes up to 27 analytes (including As and Hg).
- Methods described in Emmett et al. 2008 and CS Soils Manual.

## Quality assurance and quality control
- Digestion: Aqua Regia following Standing Committee of Analysts (1986) method.
- Laboratory accreditation: ISO 17025 accredited (UKAS).
- QC targets: total analytical error target of 20% (10% precision, 10% bias).
- Data rejection criteria: any batch with QC standard outside action limit or two consecutive warnings outside limits; CRM results exceeding bias target also lead to data rejection.
- Post-analysis review: after ~100 samples, potential re-evaluation of analyte-specific targets; previously rejected batches may be reinstated if achievable.

## Data management and outputs
- Protocols and QA procedures drawn from Countryside Survey Soils Manual (CS Technical Report No. 3/07, 180pp).
- Documentation and cross-comparison results maintained; data suitable for national statistics and country-level reporting.
- Data stored and managed under Countryside Survey data governance; outputs delivered as maps, reports, and standard formats for environmental monitoring.

## Acknowledgement and references
- Acknowledgement required: Countryside Survey data owned by NERC - CEH.
- Key references: Emmett et al. 2008 (Soils Manual), CS 2007 Soils Manual, and related Countryside Survey technical reports and publications.