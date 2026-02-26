# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- The Plynlimon long-term hydrochemistry data base is released in two versions: Raw Data Archive (RDA) and edited data.
- RDA contains raw measurements reported by laboratories with only transcription corrections; it is provided for documentation and reproducibility but is not recommended for routine analyses due to substantial likely errors.
- Edited data include measurements with high confidence, with problem values removed or corrected to align with expected correlations and flow dependencies. In rare cases, some correlated flyers remain if plausibly real. The edited dataset prioritizes consistency and reliability for routine use.

## Data editing philosophy and procedures

- Outliers and “flyers” are identified and removed or corrected to preserve plausible relationships among analytes and with flow.
- When there are inconsistent data blocks or abrupt changes in variability, expert judgment guides whether to keep or omit blocks.
- Duplicate same-day samples are omitted to reflect typical sampling rather than intensive event sampling.
- Where analyses were attributed to the wrong site, edits are applied in the edited data (raw data retained for traceability).
- Consistency checks are performed where possible (e.g., pH vs. alkalinity, charge balance, conductivity vs. ionic strength). Inconsistencies lead to dropping the offending analyte or data point.
- Notable edits are highlighted in time-series notes, with red indicating data culled or changed.

## Handling analytical method changes and their impact

- Metals: pre-concentration and analysis methods shifted from ICP-OES (until Jan 1988) to ICP-MS (from Jan 1988), with a later instrument and lab change in Dec 1998 (Wallingford to Lancaster).
- Time series are inspected around these changes; data with abrupt mean/variance shifts are treated with greater caution. In some cases, years/decades of measurements are excluded from the edited data; original measurements remain in the Raw Data Archive for careful reconstruction.
- In some instances, both pre- and post-change data are retained if the change is not consequential; notes document the effects on the series.
- Acknowledgement that method changes can create step-like shifts in several elements (e.g., Cr, Ni, Cu, Zn, Mo, Ba, La, Ce, Pr), so users should exercise caution when analyzing trends across laboratory shifts.

## Sampling design, measurement practices, and data interpretation

- Sampling cadence: long-term weekly sampling; intensive 7-hourly rainfall and two streams occurred from 2007 to 2009 for comparison with weekly data.
- Filtration differences: conductivity, pH, Gran alkalinity, and Gran acidity measured on settled (unfiltered) samples; solute concentrations measured on filtered samples (0.45 μm for cations/metals; GF/C for others). Tests in the 1980s indicated no significant difference between filtered and unfiltered for these analytes.
- Daily chloride records exist as a unique daily series, alongside the regular long-term data.

## Analyte culling and notes (high-level)

- Highly variable elements and calibration-sensitive periods are culled or flagged, especially after laboratory transitions; several elements show calibration issues or reproducibility issues across sites and times.
- Certain elements and blocks are omitted entirely in edited data (e.g., W, Sb largely removed except in cloudwater/Nant Iago time series).
- Major group patterns:
  - DOC: minimal culling; visible long-term increase in concentration and seasonal amplitude.
  - NO3-N, NO2-N, NH4-N, TDN, DON: culling focused on singleton flyers, calibration issues, and blocks not consistent with flow or other analytes; DON derived from edited NO3, NH4, and TDN values.
  - Inorganic ions and metals: many individual flyers removed if uncorrelated with related species or flow; shifts associated with method changes often require caution when spanning laboratory transitions.
  - Key ions (Cl, SO4, etc.) include selective culling of outliers and recalibration when needed; special treatment for SO4_by_ICP to separate sulfate measured by IC from sulfate inferred from total S.
  - Trace elements and metals (Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Pb, U, etc.) show site- and time-dependent calibration issues, with substantial culling and, in some sites, post-1999 data entirely discarded due to contamination or calibration problems.
- Daily and 7-hourly data often diverge; some sub-series are kept when patterns are plausible, otherwise culled.

## Data accessibility and guidance for analysts

- Edited data are intended for routine analyses; Raw Data Archive is available for reconstructing longer or alternative time series, with caution due to potential errors.
- The documentation emphasizes transparency: notes and time-series plots illustrate the editing decisions; red values indicate those culled or altered.
- For trend analyses spanning method changes, treat pre- and post-change data with caution; refer to the notes for site-specific caveats.
- The analyte set is presented with internal consistency checks and explicit rationale for edits; users should review the analyte-specific notes when conducting sensitive analyses.

## Important corrections and data issues to be aware of

- A number of misattributions and sampling labeling errors have been corrected in the edited data (e.g., site-label swaps, cross-site misassignments).
- Instances of anomalous blocks (calibration issues, cross-sample contamination) are identified and addressed, with several blocks omitted where problems could not be resolved.
- Some elements exhibit lab-dependent variance changes after the Lancaster transition; edited data reflect these cautions, and users should consider lab transition effects in cross-site comparisons.

- Overall, the dataset documents nearly three decades of hydrochemical measurements with careful quality control, offering a transparent, standardized basis for monitoring environmental health and policy performance over time.