# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

## Overview
- Documentation of the Plynlimon long-term hydrochemistry dataset, published in two versions: Raw Data Archive (RDA) and edited data.
- RDA contains unaltered laboratory measurements with minor transcription corrections; edited data are cleaned to reflect high-confidence measurements and to remove unexplained anomalies.
- Editing aims to enable routine analyses by ensuring consistency with expected correlations and flow relationships; raw data remain available for transparency and reconstruction if needed.

## Data Versions and Availability
- Raw Data Archive (RDA): unmodified measurements (with traceable transcription corrections). Not recommended for routine analyses due to known substantial errors in some values.
- Edited data: measurements with high confidence; problematic values removed or corrected (flyers, outliers, blocks with calibration issues). Includes notes on analytical-method changes and their effects.
- Both archives cover nearly three decades of data; original measurements remain accessible in the Raw Data Archive for careful, reconstructive work.

## Editing Philosophy and Procedures
- Edits focus on removing unexplained flyers, single outliers, and blocks with implausible variability, while preserving genuine signals where plausible.
- Consistency checks across analytes (e.g., SO4 vs S, Alk vs pH, charge balance, ANC vs ionic strength) guide corrections.
- When method changes or calibration issues cause abrupt changes, the edited dataset prioritizes values with the greatest confidence; sometimes years/decades are omitted from edited time series.
- Duplicates, mislabeling, and obviously erroneous site assignments are corrected in the edited data (while left in raw data for traceability).

## Method Changes and Their Effects
- Documented analytical-method changes over time (e.g., metals pre-concentration and analysis by ICP-OES, then ICP-MS; lab changes from CEH Wallingford to CEH Lancaster).
- Time series are inspected around method-change dates; abrupt shifts in means/variances may lead to exclusion of affected data or retention with notes.
- Caution advised for analyses spanning laboratory transitions due to changes in mean, variance, and calibration across sites (e.g., chromium, nickel, copper, zinc).

## Quality Assurance and Consistency Checks
- Conductivity, pH, Gran alkalinity, and Gran acidity measured on unfiltered samples; solute concentrations on filtered samples (0.45 μm or GF/C) with historical tests suggesting no significant difference.
- Systematic checks include pH–alkalinity relationships, flow correlations, and ion balance analyses to identify potential errors.
- Where consistency is lacking, affected analytes or blocks are culled; in some cases, derived variables (e.g., SO4_by_ICP) are used to maintain internal coherence.

## Analyte Notes and Data Culling (Selected Examples)
- broad grouping: analytes from ion chromatography/electrochemical methods followed by cations/metals from ICP-OES/ICP-MS.
- Some elements are heavily culled or flagged due to calibration issues, multiple laboratories, or between-week vs. 7-hourly sampling discrepancies (e.g., W, Sb, Cs, La, Ba, Ce, Pr, W, Pb, U).
- Specific notes highlight that a large number of flyers may reflect calibration issues, lab contamination, or instrument-specific artifacts; the edited data aim to minimize these artifacts while keeping true long-term signals where possible.
- Daily chloride data are preserved separately; some time-series (e.g., rainfall, cloudwater) require careful interpretation due to their different sampling regimes and potential anomalies.

## Data Structure and Visualisation Aids
- The document provides notes and sample time-series plots for each analyte to illustrate edits; red values indicate culls or changes from raw data.
- Analytes are listed and presented with both edited and raw context; additional plots expand across specific time ranges to show editing impacts.
- Separate variable: SO4_by_ICP reflects sulfate calculated from ICP-measured total sulfur, distinguishing between measured sulfate and calculated sulfate.

## Practical Guidance for GIS Use
- For routine GIS analyses and map-based visualization, use the edited data (highest confidence) rather than raw data.
- If long-term trend analyses spanning method changes are required, consult the method-change notes, plots, and metadata to account for potential shifts; consider cross-checking with the Raw Data Archive where reconstruction is needed.
- Be aware of censored or culled periods, calibration problems, and site-specific lab-transition effects that can impact spatial-temporal analyses.
- Use the accompanying analytical-method metadata to interpret abrupt shifts and to align time periods across sites for consistent mapping.

## Access and Documentation
- Editors’ notes, sample time-series plots, and comprehensive data notes accompany the data for transparency.
- The dataset includes explicit documentation on data handling decisions, outliers, blocks of data removed, and corrections to mislabeled or misassigned samples.