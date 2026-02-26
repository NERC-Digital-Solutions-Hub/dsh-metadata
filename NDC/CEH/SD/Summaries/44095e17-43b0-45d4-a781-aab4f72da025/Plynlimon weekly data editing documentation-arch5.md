# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

## Overview
- Public release of a long-term hydrochemistry dataset in two versions: Raw Data Archive (RDA) and Edited data.
- RDA contains unaltered measurements (except for trace transcription corrections) to preserve documentation and enable reconstruction, but is not recommended for routine analyses due to known errors.
- Edited data includes measurements with high confidence, with problematic values corrected or removed to reflect reliable real-world variability.
- The document explains the data editing philosophy, checks, methods changes, and site-/analyte-specific curation rules.

## Data structure and naming
- RDA: raw measurements with "RDA" suffix; unchanged aside from trace corrections.
- Edited data: variables without the "RDA" suffix; previously edited values replace raw ones and are used for routine analyses.
- A small set of derived or reclassified variables exist, such as:
  - SO4_by_ICP (SO4 computed from ICP S measurements; prior SO4 may be misclassified as the ion).
  - ANC computed as a balance of major ions; ionic strength estimated from major ions, alkalinity, and pH.
  - DON computed from TDN, NO3, NO2, and NH4 using edited values.
- Documentation notes indicate where data values were culled, corrected, or reclassified, and where raw values remain available.

## Quality control and data editing practices
- Consistency checks and plausibility editing:
  - Cross-checks among related analytes (e.g., SO4 vs S, Alk vs pH, charge balance, Gran alkalinity vs ANC, etc.) to identify outliers.
  - Where discrepancies are found, the inconsistent analyte may be dropped from the edited data.
- Handling changes in analytical methods and laboratories:
  - Metals: pre-concentration and method changes (ICP-OES to ICP-MS; instrument/lab changes) are documented and assessed for impacts on means/variances.
  - Notable shifts (laboratory changes) are carefully evaluated; some time periods may be excluded or split to avoid artefacts.
  - Acknowledgement that Cr, Mn, Co, Ni, Mo, Cd, Zn, and other elements show shifts or variance changes associated with lab changes; such shifts guide culling decisions.
- Sampling cadence and data blocks:
  - 7-hourly intensive sampling (2007–2009) used for cross-checking with weekly data; blocks showing implausible variability or calibration issues are culled or heavily scrutinized.
  - Large, abrupt variability shifts between blocks are evaluated and sometimes omitted to retain plausible variability patterns.

## Analyte- and site-specific curation
- Extensive culling and correction are documented by analyte and site, including:
  - General culling of data with calibration issues, zero/negative values, or values not correlated with flow or other ions.
  - Removal of data from problematic sites or time periods, especially where calibration or lab changes introduced artefacts.
  - Exceptional cases preserved or reclassified when justified (e.g., some blocks retained if plausibly real; others kept in cloudwater samples where correlations are stronger).
  - Some elements (e.g., W, Sb) largely omitted due to pervasive issues; others show periods of calibration problems or lab contamination (e.g., Cs, Ba, La, Pr, Pb, etc.).
- Specific notes highlight patterns such as:
  - Apparent calibration problems across periods, baseline corrections, or coarse reporting intervals.
  - Instances where data could be real but are suspected to be artefacts due to cross-sample contamination or instrument changes.
  - Cases where data were corrected for known labeling or sample-handling errors, with corrections applied in the edited data and detailed in the data notes.

## Method changes and their impact
- Between 1980s and 1990s, and around 1998–1999, major methodological shifts occurred (labs, instruments, and labs changed):
  - ICP-OES to ICP-MS for metals; later instrument changes and lab transitions.
  - Introduction of new analytical laboratories (Wallingford to Lancaster) with different reporting behavior and variance.
- Because these changes alter means/variances, edited data may differ across the transition; users are advised to treat trend analyses spanning laboratory changes with caution.
- For some analytes, pre-change data are kept in edited form if the post-change data are judged to be more trustworthy; for others, data across the change are split or culled.

## Documentation and presentation
- Data notes and time-series plots accompany the dataset; red values indicate culled data in the edited presentation.
- Analyses are organized by analyte groups and presented with context for editing decisions and quality checks.
- The presence of both raw and edited data supports transparent audit trails and reproducibility.

## Practical guidance for data users (Data Stewards perspective)
- Use edited data for routine analyses to reflect high-confidence measurements; refer to Raw Data Archive for traceability and reconstruction only if necessary.
- Be mindful of method/lab changes when conducting temporal analyses; consider segmenting analyses at known transition points.
- Consult data notes for analyte- and site-specific culling decisions and calibration issues that may affect interpretation.
- Leverage the metadata on quality control, editing criteria, and derived variables to ensure governance, reproducibility, and appropriate use of the dataset.