# Metadata: Quality control and data editing

## Overview
- Describes the Plynlimon 7-hourly intensive hydrochemistry data set, containing rainfall and streamflow chemical analyses collected roughly every 7 hours for ~2 years.
- Two public versions: Raw Data Archive (RDA) and edited data. RDA preserves raw measurements with minor glitch corrections; edited data includes measurements with high confidence after cleaning.
- Edited data is recommended for routine analyses; raw data remains for documentation and traceability to potential re-evaluation.

## Data versions and purpose
- Raw Data Archive (RDA): unaltered measurements with traceable corrections, suitable for transparency and backtracking if needed.
- Edited data: measurements with high confidence, where problematic values have been corrected or removed to ensure data quality and internal consistency.
- RDA and edited data may diverge when corrections or deletions are applied; editors provide rationale and documentation for changes.

## Sampling context
- Sites: rainfall sampled at Carreg Wen (CR), streamflow at Lower Hafren (LHF) and Upper Hafren (UHF).
- Sampling protocols differ between 7-hourly and long-term weekly data (autosamplers vs. manual, different sample locations and handling).
- Weekly data used for comparisons with 7-hourly data; where discrepancies are large, expert judgment determines which dataset is more plausible for editing.

## Editing workflow and criteria
- Core principles:
  - “Understand the ask”: determine what is needed and why, then source and verify data from appropriate sources.
  - Quality assurance: clean and transform data, check consistency (e.g., charge balance, alkalinity vs. pH, conductivity).
  - Self-serve outputs: provide dashboards/reports and offer guidance for using them.
- Data editing processes:
  - Identify and cull “flyers” (anomalous spikes/drops) not supported by related analyte patterns or flow correlations.
  - Use consistency checks to decide whether to drop or adjust data (e.g., SO4 with S, Gran alkalinity with pH, calculated ANC, TDN with N species).
  - Treat low-level analytes carefully due to contamination, blank issues, or carryover from check standards.
  - Apply expert judgment to retain blocks showing plausible variability and discard blocks showing calibration or contamination issues.
  - Document changes with color-coded notes (red = removed, blue = kept/edited) and reference to time-series figures.
- Data integrity tools:
  - Correlation matrices to identify co-varying analytes and separate real signals from anomalies.
  - Time-series overlays to diagnose sensor/calibration issues, sample swaps, and block boundaries.

## Notable edits and corrections
- Data integrity checks and cross-checks revealed calibration issues, sample swaps, and carryover.
- Specific corrections example:
  - A swap between acidified and un-acidified analyses (Trips 80 vs 81) was identified; corrected to align SO4 with its IC and ICP analyses.
  - Ad hoc adjustments to Ca spikes at LHF to account for recurring, non-chemical patterns likely due to carryover; removal of recurring spikes attributed to sampling hardware contamination.
  - W and many Cu, Sn, and other elements subjected to extensive culling due to calibration problems or contamination; some entire series (e.g., precipitation Cu) removed.
- Additional editing patterns:
  - Removal of “picket fence” effects from check standards in several elements (e.g., Sc, U) to reduce artificial periodicities.
  - Blocks with widespread anomalous values often culled entirely or adjusted to reflect plausible analytical performance.
  - Maintenance of a data-traceable record for each analyte, with explicit notes on blocks and samples affected.

## Analyte-specific notes (highlights)
- F, Cl, SO4, NO3/NO2, NH4, DOC, TDN, DON: generally edited with emphasis on preserving consistent relationships (e.g., correlations with flow, other species) and discarding inconsistent spikes.
- Low-level analytes (I, Li, Be, B, S, Ti, V, Cr, Mn, Co, Ni, Cu, Zn, Sn, Sb, Cs, Ba, La, Ce, Pr, Pb, U): more prone to calibration issues, carryover, or block-boundary effects; many were culled or corrected in blocks or entire time series.
- Ca: frequent spikes at LHF linked to carryover; after investigation, removal or adjustment of contaminated spikes was performed; notable interaction with Gran alkalinity and pH due to carbonate chemistry behavior.
- Si, Na, Mg, K, Sr, Mo, Cd, Se, Y, W: varied handling; some elements culled extensively due to calibration anomalies, block transitions, or inconsistent correlations.
- Iodine (I) and Tungsten (W): iodine record too short to support reliable editing; tungsten largely omitted from edited data due to pervasive low values and calibration issues.
- U (uranium): very low concentrations; many “picket fence” points attributed to check standards; retained only with caution, emphasizing relative rather than absolute values.

## How to use the data
- Edited data are designed for routine analysis and interpretation, with documented quality control decisions.
- Raw data should be consulted when full transparency is required or when investigating flagged anomalies; be aware that many raw values may be erroneous or influenced by calibration issues.
- Users should heed notes on carryover, calibration blocks, and sampling-related artifacts (e.g., biweekly Ca spikes, check-standard effects) when analyzing time-series trends.

## Documentation and access
- The document provides extensive notes on data editing decisions, sample codes (e.g., CR, LHF, UHF), and time-series figures illustrating changes.
- Data users are encouraged to refer to the detailed per-analyte notes and the accompanying quality-control figures to understand the rationale behind edits and to assess data suitability for specific analyses.