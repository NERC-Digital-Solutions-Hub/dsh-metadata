# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- The Plynlimon long-term hydrochemistry database is released in two versions: Raw Data Archive (RDA) and Edited data.
- RDA contains unaltered measurements as reported by laboratories, with only traceable transcription corrections. It supports transparency and re-creation of longer series, but contains many values considered substantially erroneous for routine analyses.
- Edited data exclude unreliable values and “flyers,” reflecting high confidence measurements after corrections, and are recommended for routine analyses.
- Edits and notes are designed to help users understand how and why data were changed, and original measurements remain accessible in the Raw Data Archive.

## Data Versions and Purpose

- Raw Data Archive (RDA):
  - Contains raw measurements with minor transcription corrections.
  - Suitable for documentation and potential re-examination if new information arises.
  - Not recommended for routine analyses due to substantial errors in some values.
- Edited data:
  - Includes measurements with high confidence, filtered of unexplained outliers and inconsistent values.
  - Some data blocks or years may be omitted where method changes or calibration issues create artifacts.
  - Derived with careful quality checks and metadata to accompany the edits.

## Editing Philosophy and Procedures

- Edits are guided by expert judgment and multiple consistency checks to identify and remove questionable data.
- Data editing decisions include:
  - Flagging and removing values that do not align with expected correlations (e.g., major ions, flow, and calculated relationships).
  - Handling method changes (lab and instrument transitions) by inspecting time-series around transition dates and omitting or adjusting affected periods when necessary.
  - Excluding blocks with implausible variability or calibration problems.
  - Omitting duplicate same-day samples to avoid over-representation of events.
  - Correcting mislabeled samples and documenting corrections made in the edited dataset.
- Where method changes occur (e.g., from Wallingford to Lancaster labs), the editors note potential shifts in mean/variance and advise caution when spanning these periods.

## Method Changes, Calibration, and Time-Series Integrity

- Major methodological transitions documented:
  - Metals: pre-concentration and analysis methods shifted from ICP-OES to ICP-MS at various dates, with further instrument/co-lab changes in 1998–1999.
  - Time-series integrity is maintained by comparing time-series around changes and removing data blocks tied to calibration shifts.
- The editors consult consistency checks (e.g., SO4 vs S, Alk vs pH, charge balance, ionic strength) to identify outliers and validate corrections.
- Some data are retained after changes if deemed not consequential, but impacts are clearly noted to inform downstream analyses.

## Consistency Checks and Data Quality Rules

- Consistency checks include plotting and comparing:
  - pH vs Gran alkalinity (titration curve) and pH/Alk vs flow.
  - ANC vs major ions and computed ionic strength vs conductivity.
  - Sum of cations vs sum of anions.
- Anomalies are investigated with these plots; inconsistent analytes are dropped.
- Specific care is taken for rainfall, cloudwater, and long-term streams where calibration or sampling differences can produce artifacts.

## Analyte- and Data-Specific Editing Highlights

- DOC: gradual rise over time; a few outliers culled; long-term trend preserved with attention to increasing seasonal amplitude.
- NO3-N, NO2-N, NH4-N, TDN, DON: singleton or non-systematic flyers culled; seasonal/winter spikes often retained if aligned across years and sites.
- SO4: data before 2007 reclassified as SO4_by_ICP when calculated from S; several outliers culled.
- Cl, Br, I, Li, Be, Na, Mg, Al, Si, S, K, Ca, Sc, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Y, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, W, Pb, U: editors culled or retained values based on correlations, calibration issues, lab transitions, and cross-site behaviors; several elements show lab-transition artifacts and may require cautious interpretation when combining pre- and post-transition data.
- Tungsten (W): all values culled due to severe calibration problems.
- Antimony (Sb): culled weekly data across sites except cloudwater and Nant Iago due to synchronous artifacts observed across sites.
- Cesium (Cs), Barium (Ba), Lanthanum (La), and others: culled during calibration issues or due to coarse reporting intervals or unreliable short-term dynamics.
- Some elements show gradual changes in variance or mean that are tied to non-method-related factors (e.g., lab contamination in Cu, Zn, Mo, Cd); editors keep both pre- and post-change data but flag cautions for analyses spanning transitions.

## Data Organization, Presentation, and Accessibility

- Analytes are organized by measurement method (ion chromatography, electrochemical methods, autoanalysis) and then by atomic number, followed by cations/metals (ICP-OES/ICP-MS) in atomic-number order.
- The database includes a separate daily chloride (Cl) series with long-time coverage, alongside the regular weekly sampling.
- Data notes document how editing was performed and highlight data flagged as red (modified or culled) versus unchanged in the edited dataset.
- For users needing the full historical record, Raw Data Archive provides the unedited measurements with all corrections traceable to original sources.

## Data Governance, Metadata, and Sharing

- The project emphasizes transparency: full documentation of edits, metadata, and method changes accompany the datasets.
- Data governance aspects include ensuring metadata availability, handling data quality flags, and providing a clear rationale for culling or adjusting data.
- Both datasets (Raw and Edited) are publicly accessible, with explicit guidance on their appropriate use cases.

## Guidance for Users and Applications

- Use Edited data for routine analyses, trend assessment, and reporting, while consulting Raw Data Archive for reconstruction or in-depth auditing.
- When analyzing data that spans laboratory or method changes, treat results with caution and reference the accompanying data notes.
- Consider calibration issues, spatial/temporal sampling differences, and potential artifacts (e.g., blocks of anomalous data, singletons, and zero/near-zero values) when interpreting time-series patterns.
- Leverage the embedded quality checks and consistency relationships (e.g., pH–alkalinity, ANC balance, and ion balance) to contextualize findings and identify potential data issues.