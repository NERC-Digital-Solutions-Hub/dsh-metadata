# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Purpose and versions
  - Two publicly released versions: Raw Data Archive (RDA) containing unaltered laboratory-reported measurements with only transcription-correction edits, and an edited data set with high-confidence measurements.
  - RDA provides complete documentation and traceability for data editing; edited data is recommended for routine analyses.
  - Edited data remove unexplained flyers and outliers, and, in rare cases, remove entire blocks or specific values when unlikely to reflect real-world signals.

- Data editing philosophy and provenance
  - Edits are driven by maintaining consistency with expected chemistry, correlations among analytes, and flow.
  - Where possible, consistency checks (e.g., charge balance, pH-alkalinity, ionic strength, and major ion sums) guide outlier identification and data culling.
  - Red flags flagged in notes and plots; red entries in documentation indicate raw values removed or altered.
  - Duplicate same-day samples are removed from edited data to avoid over-representation of events.

- Handling of analytical method changes and lab transitions
  - Documented changes include metal analyses shifting from ICP-OES to ICP-MS (1988) and a laboratory transition from Wallingford to Lancaster (late 1990s).
  - Time-series inspection around these changes; abrupt shifts in mean/variance may lead to exclusion of affected portions.
  - Some blocks or entire time periods are omitted in edited data if changes are deemed to compromise reliability; others are kept with explicit notes.
  - Cross-site steps (e.g., Cr, Ni, Mo, Zn, Cd) show increased variance or mean shifts post-transition; Lancaster data often culled where contamination or calibration issues are suspected.

- Quality assurance and data integrity methods
  - Consistency checks: relationships among pH, alkalinity, conductivity, Gran alkalinity, and calculated ANC; comparisons of cations vs anions; flow-linked patterns.
  - Outlier detection tied to physical plausibility and chemical correlations; outliers removed or flagged based on multi-parameter checks.
  - Filtration vs unfiltered sampling noted: dissolved solids were measured on filtered samples while certain measures (conductivity, pH, alkalinity) were from settled (unfiltered) samples; historical testing suggested no significant difference for key analytes.
  - Data notes include explicit examples of corrections and reassignments (e.g., righting mislabeled samples, reassigning SO4 when calculated from S).

- Sampling design and data blocks
  - Long-term weekly sampling with a period of intensive 7-hourly sampling (2007–2009) for rainfall and two streams to compare time scales.
  - Discrepancies between weekly and 7-hourly data addressed via expert judgment; in some cases both series are retained if discrepancies are not large.
  - Large and abrupt shifts in variability across time blocks are examined; blocks with implausible patterns may be omitted.

- Analytes and editing highlights (general patterns)
  - Major inorganic and organic constituents edited for reliability; many elements show culling or caveats due to calibration issues, lab transitions, or contamination concerns.
  - Certain elements (e.g., W, Sb, Cs, La, Pr, Be, Ba, Mo, Cd, Cr, Cu, Zn, Se, Pb, U) have extensive site- and period-specific editing decisions or complete removal in parts of the time series.
  - Some data are re-derived (e.g., SO4_by_ICP) from edited ICP measurements to maintain consistent sulfate representation.
  - Don and DOC trends discussed; DON is computed from edited TDN and NOx values rather than raw DON data.
  - Several elements exhibit laboratory-transition-related variance increases or mean shifts; many post-transition values are culled where not consistent with the rest of the dataset.
  - Specific anomalies (e.g., tungsten, arsenic, sulfates, chlorides, and trace metals) are often culled when calibration issues or contamination are suspected; in cloudwater and certain sites (e.g., Nant Iago), some elements retain readings due to correlation patterns.

- Documentation and usage guidance
  - The dataset provides extensive notes and sample time-series plots highlighting edited values (red) and detailing rationale for edits.
  - For analyses sensitive to short-term variability, consult the Raw Data Archive with caution; for routine analyses, use the edited dataset.
  - Be cautious when performing trend analyses across periods that include laboratory or method changes; consult methodological notes to interpret potential biases.
  - The data structure groups analytes by measurement method and atomic number; specific data notes accompany each analyte to inform data suitability.

- Access and reproducibility
  - The archive emphasizes data provenance, with explicit notes on data edits, corrections, and the rationale behind each change.
  - If longer, uninterrupted time series are required, the Raw Data Archive offers the original measurements; the edited data offers a cleaned, analysis-ready version with transparency about edits.