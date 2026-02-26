# Soil metals 2007 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey 2007 documenting soil metal concentrations across Great Britain.
- 402 soil cores from up to 256 1km squares; metals analyzed include Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg.
- Metadata includes 1km square site codes, plot within-square, year of survey, land classification (LC07 and numeric code), country, county, and environmental zone description (EZ_DESC_07).

## Dataset structure
- File: CS2007_SOIL_METALS.csv
- Key columns:
  - SQUARE, PLOT, YEAR
  - Metals: CD, CR, CU, NI, PB, ZN, AL, TI, MN, AS, SE, MO, HG
  - LC07, LC07_NUM (ITE Land Class 2007)
  - COUNTRY (ENG, SCO, WAL), COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Acknowledgement required for all CS data use.

## Sampling strategy and scope
- Field design based on Countryside Survey's robust statistical framework.
- Great Britain stratified by Land Classes; 591 sample squares surveyed in 2007 (England, Wales, Scotland distribution provided).
- Soils sampled from 0–15 cm depth; 2 cores selected per square from 5 X-plots in the original 1978 256 squares; 2007 sampling used the western corner of Main Plots.
- For metals, power analyses supported using a reduced sample size while maintaining confidence for reporting major analytes.

## Analytical methods
- 2000 survey: ICP-OES; 2007: augmented with ICP-MS to broaden analyte detection (up to 27 analytes at CEH Lancaster).
- Metals measured via Aqua Regia digestion following The Standing Committee of Analysts method (Method A) for soils, sediments, and related materials.
- Laboratories: CEH Lancaster; QA and calibration linked to ISO 17025 accreditation (UKAS).

## Quality assurance and quality control
- QA framework documented in CS Soils Manual; cross-checks and re-analyses as needed.
- QC targets: total analytical error <= 20% (10% precision, 10% bias).
- If QC standards fall outside action/warning limits, associated data are rejected; CRM results outside bias targets trigger rejection.
- After 100 samples, potential reevaluation of analytical error targets; possible reinstatement of previously rejected batches after review.

## Data usage, documentation, and references
- All CS data must be acknowledged as Countryside Survey data owned by NERC - CEH.
- Acknowledgement statement and copyright apply to copies, publications, and presentations.
- Protocols and methodological details drawn from Countryside Survey Soils Manual and related publications (Emmett et al. 2008; Emmett et al. 2010; CS Technical Reports 3/07 and 9/07).
- Key references and links cover: CS website, UK results report, soils manual, and land classification frameworks (ITE Merlewood).

## Practical notes for data supports
- Metadata enables cross-dataset joins (LC07/Land Class, COUNTRY, EZ_DESC_07) and regional analysis by country.
- Recognize potential patchiness and depth consistency (0–15 cm sampling) when integrating with other soil or environmental datasets.
- Use the QA and QC documentation to assess data reliability by analyte and batch; account for possible re-instated data after QC review.