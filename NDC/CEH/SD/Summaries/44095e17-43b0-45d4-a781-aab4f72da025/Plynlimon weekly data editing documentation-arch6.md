# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

## Overview
- Public release in two versions: Raw Data Archive (RDA) and Edited data (no RDA suffix).
- RDA preserves raw measurements with traceable corrections; not recommended for routine analyses due to substantial errors to be aware of.
- Edited data include only high-confidence measurements, with problematic values corrected or removed; notes document data edits and exceptions.

## Raw Data Archive vs Edited Data
- RDA: raw values plus corrections mapped to original lab files; complete documentation and the option to revisit original data if new information arises.
- Edited data: curated to remove unexplained outliers (flyers), blocks of implausible variability, and values inconsistent with known correlations; retains both pre- and post-method-change data only when justified and clearly documented in data notes.
- Some site- and time-specific misattributions and anomalies are corrected in the edited dataset (but preserved in RDA for traceability).

## Data Editing Approach and Rationale
- Aim: enable routine analyses with trustworthy data by removing questionable values and ensuring consistent time series.
- Method changes and lab transitions:
  - Metals analysis moved from ICP-OES to ICP-MS (1988 onward); later instrument and lab changes (Wallingford to Lancaster) around 1998–1999.
  - Time-series around these methodological shifts examined; decisions made to keep the most confident data; notes explain when pre- and post-change data are both retained.
- Consistency checks:
  - Cross-checks such as SO4 vs S, Alk vs pH, charge balance, Gran alkalinity vs ANC, N species vs TDN, ionic strength vs conductivity.
  - Outliers removed if clearly inconsistent with these relationships.
- Handling of anomalies:
  - Scrutinized blocks of data with abrupt changes in variability; culled if patterns were implausible (e.g., sudden spikes, calibration issues).
  - Singleton flyers and blocks of aberrant values removed; some blocks around rainfall or extreme events retained if plausible.
  - Duplicate same-day samples omitted to avoid over-representation of certain events.
- Site- and analyte-level issues:
  - Some elements show calibration problems, lab-specific artefacts, or joint block effects with the lab switch; many values culled post-1998 for affected analytes.
  - For several elements, the lab transition increased variance or introduced negative values; edited data reflect these cautions.
- Data notes and transparency:
  - Changes and anomalies are explicitly noted in data notes; raw data values culled or changed are shown in red in the provided figures.

## Data Coverage, Sampling, and Structure
- Timespan: nearly three decades.
- Intensive 7-hourly rainfall and two-stream sampling (2007–2009) supplemented regular weekly sampling for comparison; discrepancies between 7-hourly and weekly samples judged on plausibility.
- Analytes are presented in two groups:
  - Group 1: determined by ion chromatography, electrochemical methods, and autoanalysis (in order of increasing atomic number).
  - Group 2: cations and metals analyzed by ICP-OES/ICP-MS (in order of increasing atomic number).
- Derived and special variables:
  - SO4_by_ICP: sulfate calculated from total S (ICP) prior to 2007; separate from SO4 measured directly by IC; reflects method-based reassignments.
  - DON: calculated as TDN minus NO3 minus NO2 minus NH4 using edited values; negative DON values may occur due to estimation.
  - Cl daily dataset: a unique daily chloride record maintained for more than three years.
  - W, Sb, Cs, La, Pr, Ce, etc.: many elements have targeted culling or calibration-change notes; tungsten completely culled due to severe calibration problems; Sb largely culled except for cloudwater and Nant Iago.

## Practical Guidance for Data Use
- For routine analyses, use the Edited data to avoid artefacts from calibration issues, lab changes, or anomalous time blocks.
- For historical reconstructions or methodological studies, refer to the Raw Data Archive and the data notes to understand edits and to reconstruct longer time series with caution.
- Be aware of:
  - Potential biases introduced by the 1998–1999 lab transition (Wallingford to Lancaster) in several elements (notably Cr, Ni, Mo, Cd, Zn, Sb, Ba, Ce, Pr, La, Cs, W, etc.).
  - Elements with calibration issues or spurious variability that led to culling or shifting data blocks.
  - Differences between filtered and unfiltered sample measurements for certain parameters (e.g., conductivity, pH, alkalinity, major ions) and the design choice to report based on filtered for solutes while some measurements were taken on unfiltered samples.
  - The importance of using internal consistency checks (e.g., pH–alkalinity, ionic strength vs conductivity) when analyzing long-term trends.

## Important Notes on Interpretation and Quality
- The dataset emphasizes transparency about edits; the majority of long-term trends rely on edited values, with explicit caveats around data that were modified during method transitions.
- Some short-term dynamics, especially for trace metals, may reflect analytical noise or calibration issues; short-term fluctuations should be interpreted with caution.
- Daily Cl data and other high-resolution records provide valuable context but may require careful alignment with weekly or 7-hourly data when used for hydrological interpretation.

## Summary of Key Considerations for Data Support
- Data governance: clear separation between raw and edited data, with comprehensive editing rationale and documentation.
- Reproducibility: edited data accompanied by notes and, where needed, access to raw data for longer or differently scoped analyses.
- Data quality: extensive quality checks and consistency validation across analytes, with targeted culling of inconsistent values and anomalous blocks.
- User guidance: explicit warnings about laboratory changes, calibration issues, and the limitations of short-term dynamics for certain analytes.

## How to Access and Reference
- Edited data for routine use; Raw Data Archive for traceability and reconstruction; data notes provide detailed explanations of changes, culling decisions, and the effects of methodological shifts on time series.