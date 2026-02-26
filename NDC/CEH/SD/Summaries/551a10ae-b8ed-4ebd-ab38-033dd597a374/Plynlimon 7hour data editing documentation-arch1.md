# Metadata: Quality control and data editing

- Context and versions
  - Plynlimon 7-hourly intensive hydrochemistry dataset: two versions released—Raw Data Archive (RDA) and edited data.
  - RDA contains raw laboratory measurements with minor glitch corrections; not recommended for routine analyses due to many values believed to be in error.
  - Edited data include measurements with high confidence; problematic values removed or corrected where possible; retains some flagged values if they plausibly fit with nearby analytes or flow.

- Sampling framework
  - Sites: rainfall at Carreg Wen (CR) and streams at Lower Hafren (LHF) and Upper Hafren (UHF).
  - Sampling cadence: 7-hourly data (autosamplers) and long-term weekly data; some differences in protocol and sample handling between rainfall and stream samples.
  - Unique sample codes combine site and sequence; major edits documented before analyte-by-analyte notes.

- Editing philosophy and methods
  - Data quality through consistency and correlation
    - Implement cross-analyte consistency checks (e.g., SO4 vs S, Gran alkalinity vs pH, charge balance, ANC, N species vs TDN).
    - Use scatterplot matrices to distinguish true co-variation from anomal flyers.
  - Expert judgment applied
    - Remove blocks with abnormal variability or calibration problems.
    - Omit problematic data when inconsistent with nearby values or known artifacts (e.g., sample labeling issues, carryover).
  - Treatment of low-level analytes
    - High sensitivity contaminants and carryover (e.g., check-standard carryover) culled.
    - Anomalies in trace metals often removed; some blocks entirely omitted (e.g., Cu in precipitation, W entirely removed).
  - Special handling for site-specific issues
    - Calcium spikes at LHF attributed to sample carousel contamination; spikes culled.
    - Two analytical trips mislabeling issue (Trips 80 and 81) at UHF; acidified vs un-acidified analyses swapped to align time series.

- Data editing execution and documentation
  - Transparent labeling of edited vs raw data in figures (blue edited, red raw).
  - Major changes disclosed (e.g., first precip block deleted; trip-based swaps; time-series alignment of SO4 and SO4_by_ICP).
  - Edits are disclosed analyte-by-analyte with rationale and examples; samples with widespread flyers removed (e.g., certain LHF/UHF samples) and blocks shifted to restore plausible patterns.

- Analyte-specific editing highlights
  - DOC and DON: DOC edited to remove spikes not tied to flow; DON computed as TDN − NO3 − NO2 − NH4 using edited values; negative DON values possible due to uncertainties.
  - NO3, NO2, NH4, TDN: NO3 spikes culled when inconsistent with TDN; NH4 blocks culled for negative DON or contamination concerns; NO2 kept with caution due to low signal.
  - Sulfate and sulfur-related metrics: SO4 (IC) and SO4_by_ICP aligned; culling when not matching other S metrics.
  - Metals and trace elements: extensive culling for many species (Cu, Cd, Sn, Pb, W omitted); carryover and calibration issues addressed; some blocks corrected by offsets or removed entirely.
  - Ca, Mg, Na, K, Sr, Li, Be, Al, Fe, Mn, Co, Ni, Zn, Cs, Ba, La, Ce, Pr, U, etc.: editing guided by correlations, with site- and block-specific caveats noted; recurring calibration issues and block boundaries addressed with shifts or removal.

- Practical guidance for users
  - Edited data are intended for routine analyses; raw data preserved for traceability and re-examination.
  - Be aware of site- and block-specific anomalies, calibration issues, and known carryover effects.
  - Pay attention to analyte notes for per-analyte cautions, correlation expectations, and any required corrections (e.g., trip swaps, carousel contamination).
  - Distinctions in measurement: conductivity, pH, Gran alkalinity, and Gran acidity measured on settled (unfiltered) samples; most solute concentrations measured on filtered samples.

- Takeaway
  - The dataset undergoes rigorous QC and targeted editing to ensure plausible, inter-consistent hydrochemical time series, prioritizing data integrity for analysis of correlations, patterns, and action impacts. Raw data remain available for auditing, with the edited dataset recommended for most analyses.