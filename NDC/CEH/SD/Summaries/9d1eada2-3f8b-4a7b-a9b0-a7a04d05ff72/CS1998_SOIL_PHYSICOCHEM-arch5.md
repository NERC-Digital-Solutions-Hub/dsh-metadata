# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey, GB, covering soil physico-chemical properties surveyed in 1998/1999.
- Up to 256 1km squares, with one of five plots per square.
- Version 1, dated 02-06-2016; data owned by NERC - Centre for Ecology & Hydrology; CS1998_SOIL_PHYSICOCHEM.csv.

## Data fields and structure
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier within each square (text)
- YEAR: Year of survey (numeric)
- PH: Soil pH (numeric)
- LOI: Loss on ignition (%; numeric)
- C_CONC_LOI: Carbon concentration from LOI (g/kg); computed as 0.55 × LOI (numeric)
- C_STOCK_LOI: Carbon stock from LOI (t/ha); computed as 0.55 × LOI (numeric)
- N_PERCENT: Total nitrogen (%; numeric)
- PO4_OLSEN: Olsen phosphorus (mg/kg) (numeric)
- LC07: ITE Land Class 2007 (text)
- LC07_NUM: Land Class 2007 numeric code (numeric)
- COUNTRY: Country (England ENG, Scotland SCO, Wales WAL) (text)
- COUNTY07: County or council name (text)
- EZ_DESC_07: Countryside Survey Environmental Zone description (text)

## Methods and processing
- LOI (loss on ignition)
  - Samples from top 15 cm of soil; up to 256 plots; 10 g soil per sample (post-sieving to 2 mm).
  - 375°C for 16 hours; 1 g sub-sample combusted at 550°C for 3 hours.
  - LOI converted to soil carbon concentration with a factor, originally 0.50, updated to 0.55 (used for all CS estimates of soil C concentration and carbon density).
- Soil pH
  - Measured in deionised water, 1:2 soil-to-water ratio; 30-minute equilibration then pH reading after 30 seconds.
  - Conducted by ITE Merlewood using Allen et al. (1989) protocol.
- Total nitrogen (N)
  - Up to 1,280 samples analysed at ITE Merlewood with Elementar Vario-EL analyzer (oxidative combustion, thermal conductivity detection).
  - Calibration with standard (acetanilide); QA via two in-house reference materials per batch.
  - Typical sample weights: 15 mg for peat; 15–60 mg for mineral soils.
- Olsen phosphorus (P)
  - Up to 1,280 cores analysed following 0.5 M NaHCO3 extraction at pH 8.5 (5 g soil, 100 ml extract).
  - Phosphorus in extract determined colorimetrically using molybdenum blue; dialysis step to mitigate reagent effects.
  - QA with two in-house reference materials per batch.

## Data governance, usage, and attribution
- Use of Countryside Survey data must be acknowledged on all copies, publications, and presentations.
- Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Copyright: Countryside Survey © Database Right/Copyright NERC-CEH. All rights reserved.
- Data provenance includes explicit references to related publications and methodologies (e.g., LAN classifications, LOI methodologies, and CS UK results).

## Data management and stewardship implications for Data Stewards
- Metadata completeness: clearly defined fields, units, and computation rules (e.g., C_CONC_LOI and C_STOCK_LOI as 0.55 × LOI).
- Provenance and versioning: Version 1 with a clear date; ensure traceability to 1998/1999 survey and CEH/NERC custodianship.
- Data quality controls: documented QA processes (in-house references, calibration standards, sample weights, replicate references).
- Interoperability and standards: consistent coding for LC07, LC07_NUM, COUNTRY, and EZ_DESC_07 to support cross-dataset linking (ITE Land Classification, environmental zones).
- Access and sharing: compatibility with portal uploads and data catalogues; maintain and communicate update procedures and any embargo or reuse limitations.
- Citation and reuse: ensure proper acknowledgement is included in any derived products or data reuse.

## References and links
- Related publications and methodologies cited for context (e.g., Countryside Survey, MASQ, ITE Land Classification, Allen 1989, Carey et al. 2008).
- Link to Countryside Survey resources and supporting documentation where applicable.

## Highlights for practical data stewardship
- Ensure derived fields (C_CONC_LOI, C_STOCK_LOI) are consistently computed using the 0.55 conversion factor.
- Maintain clear provenance: original 1998/1999 sampling, 1998 LOI methods, laboratory QA details, and responsible institutions.
- Preserve and enforce the required acknowledgement language in all disseminations.
- Align metadata with current data catalog standards to facilitate discoverability and reuse across datasets (LC07, COUNTRY, EZ_DESC_07, etc.).