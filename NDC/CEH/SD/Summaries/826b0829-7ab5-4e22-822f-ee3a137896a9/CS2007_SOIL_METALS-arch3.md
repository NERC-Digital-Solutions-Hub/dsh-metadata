# Soil metals 2007 [Countryside Survey], Great Britain

## Purpose and scope
- Data from Countryside Survey 2007 detailing soil metal concentrations across Great Britain.
- Analytes include cadmium (Cd), chromium (Cr), copper (Cu), nickel (Ni), lead (Pb), zinc (Zn), aluminium (Al), titanium (Ti), manganese (Mn), arsenic (As), selenium (Se), molybdenum (Mo), mercury (Hg); up to 27 analytes analyzed in CEH’s standard suite.
- Dataset in CS2007_SOIL_METALS.csv covering 402 soil cores from up to 256 one-km squares; includes geographic and environmental context for national and country-level reporting.
- All use of Countryside Survey data must be acknowledged.

## Data contents
- Core file: CS2007_SOIL_METALS.csv
- Columns include:
  - SQUARE (1 km square sampling site code)
  - PLOT (plot identifier within each square)
  - YEAR (survey year)
  - Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg (concentrations, in ppm)
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07 (County or Council area)
  - EZ_DESC_07 (Countryside Survey Environmental Zone description)
- Units: concentration in ppm (mg/kg, µg/g)

## Methods and laboratory protocol
- Soil sampling and analysis:
  - 402 cores from up to 2 cores per site, randomly selected from the 5 X-plots within each square in the original 1978 design.
  - Analyses conducted by ICP-OES (2000 survey) and augmented by inductively coupled plasma mass spectrometry (ICP-MS) in 2007.
  - CEH Lancaster: standard suite up to 27 analytes.
  - Digestion: Aqua Regia digestion following The Standing Committee of Analysts method (1986).
- Laboratories and accreditation:
  - Analyses performed at CEH Lancaster; ISO 17025 accreditation (UKAS).
- Quality control and validation:
  - Cross-checks when methods changed; re-analysis of samples if issues detected.
  - Standard samples and blind replicates included in all runs.
  - Data verified against existing methodology; accreditation status documented.

## Quality assurance and QC
- QC target: total analytical error target of 20% (10% precision, 10% bias).
- Action limits: if a QC standard falls outside the action limit or two successive QC standards exceed warning limits, associated data are rejected.
- CRM results outside bias target trigger rejection of corresponding data.
- After 100 samples, re-evaluation of error targets for certain determinands may occur; previously rejected batches may be reintegrated if targets are met in subsequent runs.
- Cross-comparison and replication ensure robustness of results.

## Sampling design and data collection
- Stratified sampling based on Land Classes derived from major environmental gradients to ensure national representativeness and regional comparability.
- Sample framework:
  - 591 sample squares surveyed in 2007: 289 England, 107 Wales, 195 Scotland.
  - Earlier surveys used different corner sampling within main plots; 2007 sampled from the western corner of main plots.
- Power analyses:
  - For key metrics like pH and loss-on-ignition (soil carbon), full samples analyzed to ensure detectability at required confidence.
  - For trace metals, analyses supported by reduced sample sizes while maintaining required confidence.
- Field and laboratory protocols:
  - Clear field sampling protocol; processing, logging, chemical analysis, and archiving procedures outlined.
  - Archiving and data management procedures documented.

## Documentation, references, and governance
- Core documentation: Emmett et al. 2008 Countryside Survey: Soils Manual (Technical Report No. 3/07), plus Countryside Survey 2007 Soils Report (Emmett et al. 2010).
- Substantial references to land classification systems (ITE Merlewood) and related methodological papers.
- Acknowledgement requirements:
  - CS data owned by NERC-Centre for Ecology & Hydrology; all outputs must acknowledge this ownership.
  - Explicit acknowledgement language provided for use in copies, publications, and presentations.
- Data and protocol sources are publicly documented, with links to additional CS methodologies and reports.