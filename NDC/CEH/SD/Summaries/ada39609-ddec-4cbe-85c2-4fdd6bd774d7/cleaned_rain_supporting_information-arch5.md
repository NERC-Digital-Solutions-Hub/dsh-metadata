# Details of Cleaned UK Rainfall Chemistry Data (1986 - 2011)

## Overview
- Source: UK-AIR database operated for Defra.
- Scope: Subset of 20 sites with the longest continuous data records from 1986 to 2011.
- Purpose: Provide cleaned, quality-assessed rainfall chemistry data suitable for assessing wet deposition and related analyses.

## Data and Coverage
- Data type: Rainfall samples from bulk collectors, collected weekly or biweekly and analyzed at a central laboratory.
- Contents: For each site, a dataset listing samples with concentrations for multiple ions, rainfall depth, and a data flag.
- Units: Ion concentrations in microequivalents per litre (µeq L-1). Deposition can be derived by multiplying by rainfall depth (mm) to yield µeq m-2.
- Site metadata: Each site has a dataset file named after the site, with corresponding UK-AIR ID and spatial identifiers (latitude/longitude).

## Data Quality Assessment and Cleaning Rules
- Ion balance check:
  - Balance = (Σ cations - Σ anions) / (Σ cations + Σ anions).
  - Acceptable if between -10% and +20%; if total ion concentration < 200 µeq L-1, acceptance range extends to -10% to +30%.
- Contamination screening:
  - Remove samples with phosphate > 10 µeq L-1.
  - Examine samples with ammonium > 100 µeq L-1; eliminate samples with potassium > 8 µeq L-1.
  - Exclude calcium > 50 µeq L-1 that have higher Ca than Na (in µeq L-1) as dust contamination (wind-blown dust). This is conservative; some dust-contaminated samples may remain, especially in low-volume samples.
- Missing data handling:
  - After contamination removal, missing values are estimated using statistical interpolation across time and space with the GENSTAT MULTMISSING procedure.
- Output flagging:
  - Final datasets include both accepted data and estimated values, each with appropriate flags.

## Data Structure and Contents
- Data file structure:
  - Columns per site: sample start date, sample end date, Ca2+, Cl-, H+, K+, Mg2+, NH4+, NO3-, Na+, PO4 3-, SO4 2-, non-sea SO4 2- (calc. from Na+ based on sea-salt), conductance, precipitation depth, flag.
- Flags:
  - 0 = raw data OK
  - 1 = contaminated and omitted (no correction possible)
  - 2 = rain sample volume but not analysed
  - 3 = missing data replaced by estimates
  - 4 = contaminated data replaced by estimates
  - -1 = raw data OK (note: exact coding may vary by site)
- Missing/NA indicators:
  - NA for chemical species and conductance = no analysis
  - No value in precipitation_depth = no sample
  - NA in precipitation_depth = sample where rain volume not recorded

## Processing, Metadata and Accessibility
- Data processing:
  - Cleaned data include both accepted and estimated values, with dataset-specific mobilization of flags.
  - Site names correspond to UK-AIR IDs; metadata and spatial identifiers accompany the datasets.
- Documentation and site list:
  - The document provides a complete list of the 20 sites with coordinates, UK-AIR IDs, and corresponding data files (e.g., Allt a’Mharcaidh, Bannisdale, Barcombe Mills, Bottesford, Eskdalemuir, Flatford Mill, Goonhilly, High Muffles, Hillsborough, Loch Dee, Lough Navar, Preston Montfort, Pumlumon, Stoke Ferry, Strathvaich, Thorganby, Tycanol Wood, Wardlow Hay Cop, Whiteadder, Yarner Wood).

## Implications for Data Stewardship
- Data quality governance:
  - Clear, rule-based QA/QC criteria ensure consistency across sites and over time.
  - Documented contamination and ion-balance rules support reproducibility and auditability.
- Metainformation and discoverability:
  - Site-level datasets with explicit file naming, IDs, and spatial coordinates facilitate discovery and integration.
  - Data flags and imputation details enable informed data use and transparency about treated data.
- Limitations and caveats:
  - Conservative contamination handling may leave some dust-contaminated samples.
  - Missing data are supplemented via statistical interpolation; users should consider uncertainties in estimates.
- Suitability for governance and sharing:
  - Ready-to-share cleaned datasets with explicit provenance, transformation rules, and deposition-ready units align with data steward objectives for governance, storage, sharing, and discoverability.