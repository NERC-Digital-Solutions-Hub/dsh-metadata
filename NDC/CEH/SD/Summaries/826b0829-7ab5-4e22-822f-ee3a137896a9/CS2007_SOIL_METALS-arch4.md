# Soil metals 2007 [Countryside Survey], Great Britain

## Overview
- CS2007_SOIL_METALS.csv contains soil metal concentrations from the Countryside Survey (Great Britain) conducted in 2007.
- Data come from 402 soil cores across up to 256 1km squares in Great Britain (England, Scotland, Wales).
- Analytes include Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg; additional fields include land classification and location metadata.
- Units are in ppm (mg/kg or µg/g). Acknowledgement of Countryside Survey data is required in all copies and publications.

## Data file and structure
- File: CS2007_SOIL_METALS.csv
- Columns:
  - SQUARE (1km square sampling site code)
  - PLOT (plot identifier within square)
  - YEAR (survey year)
  - CD, CR, CU, NI, PB, ZN, AL, TI, MN, AS, SE, MO, HG (metal concentrations, ppm)
  - LC07 (ITE Land Class 2007) and LC07_NUM (numeric code)
  - COUNTRY (ENG, SCO, WAL)
  - COUNTY07 (county/council)
  - EZ_DESC_07 (Environmental Zone description)
- Sampling involved up to 2 cores per 5 X-plots from the original 1978 256 squares; in 2007, cores were taken from the western corner of Main Plots.

## Methods

### Sampling strategy
- Great Britain stratified into Land Classes to capture environmental gradients; 591 sample squares surveyed in 2007 (England 289, Wales 107, Scotland 195).
- Soil samples collected from the top 0–15 cm; sampling locations shifted across survey years for comparability.
- Power analyses guided sample sizes: all samples analyzed for pH and loss-on-ignition; metals analyzed with potentially reduced per-annum sample numbers while preserving confidence.

### Field and processing protocols
- Field sampling guided by a standardized protocol; cores logged, processed, and archived consistently.
- Processing covered core logging, chemical analyses, and archiving of final samples.

### Laboratory analyses
- 2000 survey: ICP-OES for metal digests; 2007 added inductively coupled plasma mass spectrometry (ICP-MS) to detect more analytes.
- Current standard for CEH Lancaster includes up to 27 analytes (including As and Hg) beyond the core metals from earlier surveys.
- Digestion: Aqua Regia method following The Standing Committee of Analysts (1986) protocol; analyses conducted under CEH Lancaster’s system.
- QA and QC: Standard samples and blind replicates used; cross-method verification where methods changed; some samples re-analysed to confirm results; ISO 17025 accreditation for laboratories.

## Quality Assurance and Control
- QC target: total analytical error of 20% (10% precision, 10% bias).
- Action limits: if QC standard fails or two consecutive results exceed warning limits, data from that batch may be rejected; CRM results exceeding bias targets may trigger data rejection.
- After 100 samples, reassessment of error targets may occur; persistently failing batches may be reinstated if justifiable.
- Cross-checks and re-analysis ensure data reliability; documentation available in the Countryside Survey Soils Manual.

## Documentation and references
- Core documentation: Emmett et al. (2008) Countryside Survey: Soils Manual; CS Technical Report No. 3/07.
- Additional CS reports and UK results (Carey et al., 2008; Emmett et al., 2010) provide broader context and methodology.
- Protocols, cross-comparisons, and power analyses are detailed in the 2008 Soils Manual and related CS Technical Reports.
- Related classification references: ITE Land Classification of Great Britain (Bunce et al.).

## Data usage and attribution
- All CS data usage must include the specified acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; Database Rights/Copyright NERC-CEH. All rights reserved.
- Data and methods are documented to support reuse, analysis, and integration with broader Countryside Survey datasets.

## Key takeaways for data leaders
- A robust, QA’d dataset linking metal concentrations to spatial units (1km squares), time (2007), and environmental classifications (LC07, EZ_DESC_07).
- Comprehensive metadata supports discoverability, provenance, and cross-analysis with other Countryside Survey products.
- Provenance includes ISO 17025-accredited laboratories, standardized digestion and analytical methods, and formal QC targets to ensure data quality for policy and analytical use.