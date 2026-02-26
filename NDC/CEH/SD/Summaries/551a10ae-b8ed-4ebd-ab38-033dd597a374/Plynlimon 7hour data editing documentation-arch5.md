# Metadata: Quality control and data editing

- Describes the curation of the Plynlimon 7-hourly intensive hydrochemistry data set into two versions: a Raw Data Archive (RDA) and an edited data set.
- RDA contains raw laboratory measurements with traceable corrections; intended for documentation and potential re-editing, not for routine analyses.
- Edited data include only measurements with high confidence, having been corrected or excluded where necessary; provides consistency checks and documented editing decisions.
- Sampling sites and codes: rainfall (CR) and streams (LHF, UHF); 7-hourly samples vs long-term weekly samples, with differences in protocols (autosamplers vs manual sampling).

## Data editing methodology

- Comprehensive quality-control approach:
  - Consistency checks across analytes (e.g., SO4 vs S, Alk vs pH, charge balance, relationships such as Gran Alkalinity with calculated ANC, etc.).
  - Overlay and reconciliation of rainfall vs stream data; when discrepancies are large, expert judgment decides which values to keep.
  - Comparisons between 7-hourly and weekly data to identify and resolve systematic differences.
- Provenance and traceability:
  - Editing documented in sequence: broad editing changes first, then per-analyte notes.
  - Data values are flagged visually in their figures as raw (red) vs edited (blue) to show edits.
- Handling of sampling and instrument issues:
  - Corrected known mislabeling (notably a swap of acidified vs un-acidified analyses between trips 80 and 81 for UHF).
  - Blocking issues: removal or adjustment of entire analytical blocks associated with calibration problems or contamination.
  - Addressed carryover effects from check standards (leading to “picket fence” patterns) and other calibration artifacts.
- Use of cross-analyte correlations:
  - Scatterplot matrices used to distinguish real, co-varying signals from anomalous values.
  - Decisions guided by how analytes co-vary with others (e.g., DOC with Fe, La, Ce, Pr; Ca with Gran alkalinity and pH; etc.).
- Analyte groupings:
  - Analytes determined by IC, electrochemical methods, autoanalysis, etc., presented first, followed by cations/metals (ordered by atomic number).

## Editing actions and representative notes

- General actions:
  - Deletion of anomalous flyers/drop-outs unless supported by correlation with other analytes.
  - Omission of values from blocks with implausible variability or calibration issues.
  - Blocking corrections where necessary (e.g., contiguously edited blocks at UHF/LHF with calibration problems).
  - Correction of sample-switching and labeling errors; alignment of related signals (e.g., SO4 vs SO4_by_ICP).
- Site- and analyte-specific issues:
  - Ca spikes at LHF attributed to sample carousel contamination, not natural variability; spikes culled unless supported by other evidence.
  - Repeating “picket fence” effects in Sc, Mn, Co from check standards; affected values culled or offset adjustments applied.
  - Filtered vs unfiltered sample differences acknowledged; for certain measurements, no significant difference was found, but documentation notes when it matters.
  - Low-level analytes (e.g., Mo, Sn, Pb, W) frequently require culling due to calibration and background-correction issues; in some cases entire series were removed (e.g., Cd in precipitation data).
  - Swapping of analytical trips (80 vs 81) corrected to restore synchronization of correlated signals (e.g., SO4, DOC, Ca, Al).
- Outcome presentation:
  - For each analyte, a narrative of editing choices accompanies plotted time series; raw data (RDA) and edited data are contrasted, with major changes highlighted.

## Implications for data users and governance

- Data quality and transparency:
  - Edited data are designed for routine analyses; Raw Data Archive preserves full provenance and enables re-editing if needed.
  - Extensive documentation of edits supports reproducibility and auditability.
- Guidance for use:
  - Prefer edited data for analyses; consult analyte-specific editing notes for caveats (calibration issues, carryover, block-level anomalies).
  - Be cautious with very low-concentration analytes where absolute values may be uncertain; focus on relative changes and patterns.
- Data stewardship best practices:
  - Maintain raw archives alongside edited datasets; keep detailed edit logs and rationale.
  - Use cross-analyte consistency checks to inform ongoing data quality assurance.
  - Clearly document sampling-method differences, instrument issues, and corrective actions to support future data integration and reuse.

## Endnotes

- The document includes Notes on individual analytes with examples and time-series figures illustrating the editing decisions.
- The editing process emphasizes reproducibility, transparency, and alignment across related measurements, with explicit acknowledgment of remaining uncertainties in low-level data.